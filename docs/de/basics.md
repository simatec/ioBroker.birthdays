![Logo](../../admin/birthdays.png)

# ioBroker.birthdays

## iCal

Du kannst eine iCal-URL nutzen, welche alle Geburtstage enthält. Der Adapter sucht nach allen Terminen in dieser Datei.

Deine Termine

1. müssen das Geburtsjahr in der Beschreibung enthalten (z.B. 1987)
2. sind ganztäging
3. stehen auf "jährlich wiederholen"

Es ist NICHT zwingend erforderlich die iCal-Option zu nutzen. Du kannst alternativ auch alle Geburtstage manuell in der Instanz eintragen. *Falls Du beide Optionen nutzt, werden die Informationen zusammengeführt.*

![Calendar example](../exampleCalendar.png)

## Beispiel (Blockly)

(erfordert pushover)

![Blockly example](../exampleBlockly.png)

```xml
<xml xmlns="https://developers.google.com/blockly/xml">
  <variables>
    <variable id="p+Z^g1!hvR3!J9i,X(AI">text</variable>
  </variables>
  <block type="procedures_defnoreturn" id="gJY_AOXgo;b#ej2CXe3/" x="87" y="-212">
    <mutation>
      <arg name="text" varid="p+Z^g1!hvR3!J9i,X(AI"></arg>
    </mutation>
    <field name="NAME">sendText</field>
    <comment pinned="false" h="80" w="160">Beschreibe diese Funktion …</comment>
    <statement name="STACK">
      <block type="pushover" id="D7E4hKm%5=|Yi-b-)9(A">
        <field name="INSTANCE"></field>
        <field name="SOUND"></field>
        <field name="PRIORITY">0</field>
        <field name="LOG"></field>
        <value name="MESSAGE">
          <shadow type="text" id="prP3?f.yGgkkp))l]A07">
            <field name="TEXT">text</field>
          </shadow>
          <block type="variables_get" id="iMSl1Pg7ZEvE%hQd6B9{">
            <field name="VAR" id="p+Z^g1!hvR3!J9i,X(AI">text</field>
          </block>
        </value>
        <value name="TITLE">
          <block type="text" id="T96y]A^n-1TV52cw%+Gk">
            <field name="TEXT">Geburtstags-Kalender</field>
          </block>
        </value>
      </block>
    </statement>
  </block>
  <block type="schedule" id="6#((PC;76=!e/P3^ZsKI" x="88" y="113">
    <field name="SCHEDULE">0 7 * * *</field>
    <statement name="STATEMENT">
      <block type="controls_if" id="oZ%5t{r{bO3c{Xhl-|_a">
        <mutation elseif="1"></mutation>
        <value name="IF0">
          <block type="logic_compare" id=",Ui1[S(n}f`O*5_zS=:K">
            <field name="OP">EQ</field>
            <value name="A">
              <block type="get_value" id="L/Vh`N_zLwYK$+90B)l.">
                <field name="ATTR">val</field>
                <field name="OID">birthdays.0.next.daysLeft</field>
              </block>
            </value>
            <value name="B">
              <block type="math_number" id="W87L*`2V7yMC5j};TO0,">
                <field name="NUM">0</field>
              </block>
            </value>
          </block>
        </value>
        <statement name="DO0">
          <block type="procedures_callnoreturn" id="|%0O9GCBWm-9UV_Z~/%^">
            <mutation name="sendText">
              <arg name="text"></arg>
            </mutation>
            <value name="ARG0">
              <block type="text_join" id="rQa(!TVIvOgf/Vnn,nWG">
                <mutation items="2"></mutation>
                <value name="ADD0">
                  <block type="text" id="h770a|!zX%7)X[Vk.2,[">
                    <field name="TEXT">Geburtstage heute: </field>
                  </block>
                </value>
                <value name="ADD1">
                  <block type="get_value" id="U2%GgLhMX(ra$S;y1/_K">
                    <field name="ATTR">val</field>
                    <field name="OID">birthdays.0.next.text</field>
                  </block>
                </value>
              </block>
            </value>
            <next>
              <block type="controls_if" id="$QQRR`a-vzSUU}88$?~`">
                <value name="IF0">
                  <block type="logic_compare" id="eg:?F}+ID`%G1LHM5PAZ">
                    <field name="OP">EQ</field>
                    <value name="A">
                      <block type="get_value" id="Ato::k3GO0QfM_Fs.6s;">
                        <field name="ATTR">val</field>
                        <field name="OID">birthdays.0.nextAfter.daysLeft</field>
                      </block>
                    </value>
                    <value name="B">
                      <block type="math_number" id="n(N#~`eD{7Q,X!c=+/(V">
                        <field name="NUM">1</field>
                      </block>
                    </value>
                  </block>
                </value>
                <statement name="DO0">
                  <block type="procedures_callnoreturn" id="T6*=i:ILlcQ^z%0.w~yK">
                    <mutation name="sendText">
                      <arg name="text"></arg>
                    </mutation>
                    <value name="ARG0">
                      <block type="text_join" id="*ne-l72dQ??5^6Dj2gV$">
                        <mutation items="2"></mutation>
                        <value name="ADD0">
                          <block type="text" id="ba}815_R_35-Y~GG*}/R">
                            <field name="TEXT">Geburtstage morgen: </field>
                          </block>
                        </value>
                        <value name="ADD1">
                          <block type="get_value" id="u?8B|PylEzphdFq{f]QK">
                            <field name="ATTR">val</field>
                            <field name="OID">birthdays.0.nextAfter.text</field>
                          </block>
                        </value>
                      </block>
                    </value>
                  </block>
                </statement>
              </block>
            </next>
          </block>
        </statement>
        <value name="IF1">
          <block type="logic_compare" id="4E5@w,gT+=q(NaaGdT?U">
            <field name="OP">EQ</field>
            <value name="A">
              <block type="get_value" id="~~U^$SjlNI3ns6I5Yz~O">
                <field name="ATTR">val</field>
                <field name="OID">birthdays.0.next.daysLeft</field>
              </block>
            </value>
            <value name="B">
              <block type="math_number" id="T{[v+psC[IzHkn.LkZP4">
                <field name="NUM">1</field>
              </block>
            </value>
          </block>
        </value>
        <statement name="DO1">
          <block type="procedures_callnoreturn" id="I5L?1ZB,[|2x[Nm$8s4Z">
            <mutation name="sendText">
              <arg name="text"></arg>
            </mutation>
            <value name="ARG0">
              <block type="text_join" id="!EFb@yB_*Hm!QU{gcA]I">
                <mutation items="2"></mutation>
                <value name="ADD0">
                  <block type="text" id="{ofc`NkX8NjN`:`DEIH*">
                    <field name="TEXT">Geburtstage morgen: </field>
                  </block>
                </value>
                <value name="ADD1">
                  <block type="get_value" id=",%aRO_hL*tODl=By@eru">
                    <field name="ATTR">val</field>
                    <field name="OID">birthdays.0.next.text</field>
                  </block>
                </value>
              </block>
            </value>
          </block>
        </statement>
      </block>
    </statement>
  </block>
</xml>
```