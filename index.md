<html>
    <head>
        <meta charset="utf-8">
        <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
        <link rel="stylesheet" href="inex.css">
        <link rel="stylesheet" href="draw.css">

    </head>
    <body>
        <div class="middle-box">
            <h1>Mining Simulation</h1>
        <form>
            <fieldset style="font-size:120%; padding:0px 0.5em; border-color: #fff">
                <legend>Pool's Variables</legend>
                <div class="slidecontainer">
                    <p>&alpha; : <span id="demoAlpha"></span>
                        <br>(Your relative hashing power to hashing powers of all the miners.)
                    </p>
                    <input type="range" min="0.01" max="0.5" step="0.01" value="0.25" class="slider" id="alpha">
                    <br>
                    <br>
                    <p>&gamma; : <span id="demoGamma"></span>
                        <br>(Proportion of honest miners which mine on your pool when there is a fork.)
                    </p>
                    <input type="range" min="0.01" max="1" step="0.01" value="0.5" class="slider" id="gamma">
                    <br>
                    <br>
                    <p>Number of Attempts&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&VerticalBar;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span id="demoAttempts"></span>
                    </p>
                    <input type="range" min="1" max="100000" value="10080" step="1" class="slider" id="attempts">
                </div>
                <br>
                <br>
            </fieldset>
        </form>
        <div style="text-align:center;">
            <button class="button" type="button" onclick="simulate(),profitabilityChart(),table()"> <span> Simulate </span>
            </button>





        </div>


        <p id="t1111"></p>            
        <p id="t1112"></p>            
        <p id="t1113"></p>            
        <p id="t1114"></p>
        <p id="t1115"></p>
        <p id="t1116"></p>
        <p id="t1117"></p>





        <div class="chart-container">
            <canvas id="chart1"></canvas>
        </div>
        <div class="chart-container">
            <canvas id="chart2"></canvas>
        </div>
        
        
        
        <div>
            <p>1</p>
        </div>
        <div>
            <p>2</p>
        </div>
        <div>
            <p>1</p>
        </div>
        <div>
            <p>2</p>
        </div>
        <div>
            <p>1</p>
        </div>
        <div>
            <p>2</p>
        </div>
        
        
        
        
        </div>

        <div class="middle-box">
        <h1>POOL STATS</h1>
        <div class="tbl-header">
            <table cellpadding="0" cellspacing="0" border="0">
                <thead>
                    <tr>
                        <th></th>
                        <th>Honest Mining Strategy</th>
                        <th>Selfish Mining Strategy</th>
                        <th>Lead Stubborn Mining Strategy</th>
                        <th>Equal Fork Stubborn Mining Strategy</th>
                    </tr>
                </thead>
            </table>
        </div>
        <div class="tbl-content">
            <table cellpadding="0" cellspacing="0" border="0">
                <tbody>
                    <tr>
                        <td>You Published</td>
                        <td id="hyp"></td>
                        <td id="syp"></td>
                        <td id="lyp"></td>
                        <td id="eyp"></td>
                    </tr>
                    <tr>
                        <td>Others Published</td>
                        <td id="hop"></td>
                        <td id="sop"></td>
                        <td id="lop"></td>
                        <td id="eop"></td>
                    </tr>
                    <tr>
                        <td>Total Blocks Published</td>
                        <td id="htbp"></td>
                        <td id="stbp"></td>
                        <td id="ltbp"></td>
                        <td id="etbp"></td>
                    </tr>
                    <tr>
                        <td>Orphaned Blocks</td>
                        <td id="hob"></td>
                        <td id="sob"></td>
                        <td id="lob"></td>
                        <td id="eob"></td>
                    </tr>
                    <tr>
                        <td>Total Blocks Mined</td>
                        <td id="htbm"></td>
                        <td id="stbm"></td>
                        <td id="ltbm"></td>
                        <td id="etbm"></td>
                    </tr>
                    <tr>
                        <td>Orphaned Percentage</td>
                        <td id="hobp"></td>
                        <td id="sobp"></td>
                        <td id="lobp"></td>
                        <td id="eobp"></td>
                    </tr>
                    <tr>
                        <td>You Published % of all blocks</td>
                        <td id="hypp"></td>
                        <td id="sypp"></td>
                        <td id="lypp"></td>
                        <td id="eypp"></td>
                    </tr>
                    <tr>
                        <td>Others Published % of all blocks</td>
                        <td id="hopp"></td>
                        <td id="sopp"></td>
                        <td id="lopp"></td>
                        <td id="eopp"></td>
                    </tr>
                </tbody>
            </table>
        </div>
        </div>
        <div class="middle-box">
        <h1>PROFITABILITY</h1>
        <div class="tbl-header">
            <table cellpadding="0" cellspacing="0" border="0">
                <thead>
                    <tr>
                        <th></th>
                        <th>Honest Mining Strategy</th>
                        <th>Selfish Mining Strategy</th>
                        <th>Lead Stubborn Mining Strategy</th>
                        <th>Equal Fork Stubborn Mining Strategy</th>
                    </tr>
                </thead>
            </table>
        </div>
        <div class="tbl-content">
            <table cellpadding="0" cellspacing="0" border="0">
                <tbody>
                    <tr>
                        <td>Your Real Hash Rate</td>
                        <td id="hyrh"></td>
                        <td id="syrh"></td>
                        <td id="lyrh"></td>
                        <td id="eyrh"></td>
                    </tr>
                    <tr>
                        <td>Your Apparent Hash Rate</td>
                        <td id="hyah"></td>
                        <td id="syah"></td>
                        <td id="lyah"></td>
                        <td id="eyah"></td>
                    </tr>
                    <tr>
                        <td>Your Profitability Ratio</td>
                        <td id="hypr"></td>
                        <td id="sypr"></td>
                        <td id="lypr"></td>
                        <td id="eypr"></td>
                    </tr>
                    <tr>
                        <td>Difficulty Changed</td>
                        <td id="hdc"></td>
                        <td id="sdc"></td>
                        <td id="ldc"></td>
                        <td id="edc"></td>
                    </tr>
                    <tr>
                        <td>Difficulty Will Changed To</td>
                        <td id="hdwc"></td>
                        <td id="sdwc"></td>
                        <td id="ldwc"></td>
                        <td id="edwc"></td>
                    </tr>
                <td>Attack Cycles Duration</td>
                <td id="hacd"></td>
                <td id="sacd"></td>
                <td id="lacd"></td>
                <td id="eacd"></td>
                </tbody>
            </table>
        </div>
        </div>
        <div class="middle-box">
        <h1>THEORETICS</h1>
        <div class="tbl-header">
            <table cellpadding="0" cellspacing="0" border="0">
                <thead>
                    <tr>
                        <th></th>
                        <th>Honest Mining Strategy</th>
                        <th>Selfish Mining Strategy</th>
                        <th>Lead Stubborn Mining Strategy</th>
                        <th>Equal Fork Stubborn Mining Strategy</th>
                    </tr>
                </thead>
            </table>
        </div>
        <div class="tbl-content">
            <table cellpadding="0" cellspacing="0" border="0">
                <tbody>
                    <tr>
                        <td>Your Apparent Hash Rate Would Be</td>
                        <td id="htah"></td>
                        <td id="stah"></td>
                        <td id="ltah"></td>
                        <td id="etah"></td>
                    </tr>
                    <tr>
                        <td>Your Profitability Ratio Would Be</td>
                        <td id="htpr"></td>
                        <td id="stpr"></td>
                        <td id="ltpr"></td>
                        <td id="etpr"></td>
                    </tr>
                </tbody>
            </table>
        </div>
        </div>
        <script src="strategies.js"></script>
        <script src="draw.js"></script>
        <script src="profitability.js"></script>
        <script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/2.7.3/Chart.js"></script>
    </body>
</html>
