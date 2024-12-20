<xml xmlns="https://developers.google.com/blockly/xml" is_dbot="true" collection="false">
  <variables>
    <variable id="/~-+mmFsYGB%~WTzS%,g">Stake</variable>
    <variable id="{7yeazK[c_W:Gc`5f6!/">currentPrediction</variable>
    <variable id="63RXsB.,!h.qxxT/Squh">list</variable>
  </variables>
  <block type="trade_definition" id="X83_Zw!nF_Y?cq$A[1AV" deletable="false" x="0" y="0">
    <statement name="TRADE_OPTIONS">
      <block type="trade_definition_market" id="W)zMk3t;hhS2q:u:hw@u" deletable="false" movable="false">
        <field name="MARKET_LIST">synthetic_index</field>
        <field name="SUBMARKET_LIST">random_index</field>
        <field name="SYMBOL_LIST">1HZ10V</field>
        <next>
          <block type="trade_definition_tradetype" id="|$hG~eN)4ckv()Nbozg!" deletable="false" movable="false">
            <field name="TRADETYPECAT_LIST">digits</field>
            <field name="TRADETYPE_LIST">overunder</field>
            <next>
              <block type="trade_definition_contracttype" id="/m(FM+jcN{LwHEI`Bx6T" deletable="false" movable="false">
                <field name="TYPE_LIST">both</field>
                <next>
                  <block type="trade_definition_candleinterval" id="ng,K$-qjDi?HAhRojfPX" deletable="false" movable="false">
                    <field name="CANDLEINTERVAL_LIST">60</field>
                    <next>
                      <block type="trade_definition_restartbuysell" id="Ao@_v6;=|`yO@:0[d-!q" deletable="false" movable="false">
                        <field name="TIME_MACHINE_ENABLED">FALSE</field>
                        <next>
                          <block type="trade_definition_restartonerror" id="pQVdPuih*Ov!n58-#3`@" deletable="false" movable="false">
                            <field name="RESTARTONERROR">TRUE</field>
                          </block>
                        </next>
                      </block>
                    </next>
                  </block>
                </next>
              </block>
            </next>
          </block>
        </next>
      </block>
    </statement>
    <statement name="INITIALIZATION">
      <block type="variables_set" id="8nHMs|)JSATgz,^NYx0y">
        <field name="VAR" id="/~-+mmFsYGB%~WTzS%,g">Stake</field>
        <value name="VALUE">
          <block type="math_number" id=".d5K/q;[M.~%rt*6!xN;">
            <field name="NUM">20</field>
          </block>
        </value>
        <next>
          <block type="lists_create_with" id="L[J4IHR%YP%$;pc2*U=0">
            <field name="VARIABLE" id="63RXsB.,!h.qxxT/Squh">list</field>
            <statement name="STACK">
              <block type="lists_statement" id="kXY$^%)H=a4w~M?j/Kp@" movable="false">
                <value name="VALUE">
                  <block type="math_number" id="m3z5@M/*[Mp4$|SjTS|%">
                    <field name="NUM">9</field>
                  </block>
                </value>
                <next>
                  <block type="lists_statement" id="(G#`s__|QDq)7pIlo6AB" movable="false">
                    <value name="VALUE">
                      <block type="math_number" id="Zy3I~Hc_9QS[a:L03DGb">
                        <field name="NUM">4</field>
                      </block>
                    </value>
                    <next>
                      <block type="lists_statement" id="zVGLaA+^5?Juzcv2mKyq" movable="false">
                        <value name="VALUE">
                          <block type="math_number" id="7(*Y%4#:~8Pm7:)^xspb">
                            <field name="NUM">3</field>
                          </block>
                        </value>
                        <next>
                          <block type="lists_statement" id=";8}bv-YJf}lF0u4lK0~=" movable="false">
                            <value name="VALUE">
                              <block type="math_number" id="N*J7X/~U[SLBTv~?|nxq">
                                <field name="NUM">2</field>
                              </block>
                            </value>
                            <next>
                              <block type="lists_statement" id="aYKm@/e6~y$whg?-Hd2s" movable="false">
                                <value name="VALUE">
                                  <block type="math_number" id="IPB]fGn|TEnKi`YM4G4g">
                                    <field name="NUM">1</field>
                                  </block>
                                </value>
                              </block>
                            </next>
                          </block>
                        </next>
                      </block>
                    </next>
                  </block>
                </next>
              </block>
            </statement>
          </block>
        </next>
      </block>
    </statement>
    <statement name="SUBMARKET">
      <block type="math_change" id="qNG#~#;IKE`gq~t}um45">
        <field name="VAR" id="{7yeazK[c_W:Gc`5f6!/">currentPrediction</field>
        <value name="DELTA">
          <shadow type="math_number" id="LKRy)5g%xKM{7U*ZQf.P">
            <field name="NUM">1</field>
          </shadow>
        </value>
        <next>
          <block type="trade_definition_tradeoptions" id="x+Yma/.l2xSZ/lA[O_[X">
            <mutation xmlns="http://www.w3.org/1999/xhtml" has_first_barrier="false" has_second_barrier="false" has_prediction="true"></mutation>
            <field name="DURATIONTYPE_LIST">t</field>
            <value name="DURATION">
              <shadow type="math_number_positive" id="~OC.{bf~+IS8=,X%*4Dx">
                <field name="NUM">1</field>
              </shadow>
            </value>
            <value name="AMOUNT">
              <shadow type="math_number_positive" id=".TA9,v2GNoV6nI5?byhO">
                <field name="NUM">1</field>
              </shadow>
              <block type="variables_get" id="Kn=aJ!*feL~vJ;2yabeO">
                <field name="VAR" id="/~-+mmFsYGB%~WTzS%,g">Stake</field>
              </block>
            </value>
            <value name="PREDICTION">
              <shadow type="math_number_positive" id="(d}qK2.N9YeoNY%Gf2dW" inline="true">
                <field name="NUM">1</field>
              </shadow>
              <block type="lists_getIndex" id="S,{n?{w.+*$XS~-Ze(ze">
                <mutation xmlns="http://www.w3.org/1999/xhtml" statement="false" at="true"></mutation>
                <field name="MODE">GET</field>
                <field name="WHERE">FROM_START</field>
                <value name="VALUE">
                  <block type="variables_get" id="IPA=4bGbcJb7mbBGqdr3">
                    <field name="VAR" id="63RXsB.,!h.qxxT/Squh">list</field>
                  </block>
                </value>
                <value name="AT">
                  <block type="variables_get" id="`p=f65{ERHhwA7WFFoAu">
                    <field name="VAR" id="{7yeazK[c_W:Gc`5f6!/">currentPrediction</field>
                  </block>
                </value>
              </block>
            </value>
          </block>
        </next>
      </block>
    </statement>
  </block>
  <block type="during_purchase" id="QeUu``I2!~IIM,SvA{`3" x="1005" y="0">
    <statement name="DURING_PURCHASE_STACK">
      <block type="controls_if" id="xhm_:DB:lS|e?7vv,zgZ">
        <value name="IF0">
          <block type="check_sell" id="*!O5V.Pd!u29W7-ULdjP"></block>
        </value>
      </block>
    </statement>
  </block>
  <block type="after_purchase" id="Z9Lw[3+2h{0kfug-C1L/" x="1005" y="232">
    <statement name="AFTERPURCHASE_STACK">
      <block type="controls_if" id="AQpJsuv2V^VTUd9B}U,B">
        <value name="IF0">
          <block type="contract_check_result" id="`LU=1V6Pmvg_D@H-T`_*">
            <field name="CHECK_RESULT">win</field>
          </block>
        </value>
        <statement name="DO0">
          <block type="variables_set" id="%u/dlROTgrE|3G`vY):=">
            <field name="VAR" id="{7yeazK[c_W:Gc`5f6!/">currentPrediction</field>
            <value name="VALUE">
              <block type="math_number" id="R|4|21;I{s.-JgTEP;3$">
                <field name="NUM">0</field>
              </block>
            </value>
          </block>
        </statement>
        <next>
          <block type="trade_again" id="n#J??vA$sh1^;9-XSOy*"></block>
        </next>
      </block>
    </statement>
  </block>
  <block type="before_purchase" id="~:qI#Y|0yU)LyXScyrh3" deletable="false" x="0" y="1000">
    <statement name="BEFOREPURCHASE_STACK">
      <block type="controls_if" id="check_last_digit">
        <value name="IF0">
          <block type="math_modulo" id="modulo_check">
            <value name="DIVIDEND">
              <block type="lists_getIndex" id="get_prediction_value">
                <mutation xmlns="http://www.w3.org/1999/xhtml" statement="false" at="true"></mutation>
                <field name="MODE">GET</field>
                <field name="WHERE">FROM_START</field>
                <value name="VALUE">
                  <block type="variables_get" id="current_prediction">
                    <field name="VAR" id="{7yeazK[c_W:Gc`5f6!/">currentPrediction</field>
                  </block>
                </value>
              </block>
            </value>
            <value name="DIVISOR">
              <block type="math_number" id="last_digit_divisor">
                <field name="NUM">10</field>
              </block>
            </value>
          </block>
        </value>
        <statement name="DO0">
          <block type="purchase" id="_~Hc_YPMsa+9C%=Q*(Dy">
            <field name="PURCHASE_LIST">DIGITUNDER</field>
          </block>
        </statement>
      </block>
    </statement>
  </block>
</xml>
