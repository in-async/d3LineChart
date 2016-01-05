# d3LineChart

csv,tsvファイルを基にラインチャートを起こすライブラリです。

## 使い方

#### head内

    <link rel="stylesheet" type="text/css" href="d3LineChart.css">

#### body内

    <div id="selectWrapper"></div>  <!--　セレクタを格納するラッパー -->
    <div id="graphWrapper"></div>   <!--　svgを格納するラッパー -->
    <script>
    var url = "data.csv";
    var options = {
  
      margin: { //  svg要素に対するグラフのマージン
    
        top: 20,
        right: 30,
        bottom: 30,
        left: 60
    
      },
      height: 500,  //  svg要素の高さ（幅はラッパーに合わせ自動的にリサイズします）
      selectWrapperId: "selectWrapper", //  セレクタのラッパーID
      graphWrapperId: "graphWrapper", //  グラフのラッパーID
      charset: "Shift_JIS", //  ファイルの文字コード
      timeFormat: "%Y/%m/%d", //  csvファイルの時間フォーマット（https://github.com/mbostock/d3/wiki/Time-Formatting）
      xAxisformat: "%m月%d日", //   x軸の時間フォーマット
      fileFormat: "csv" //  ファイル形式
  
    };
    var graph = new d3LineChart(url, options);

    </script>
  
  オプションで値を指定されなかった場合は、既定値が自動的に入ります。（上の例が既定値です。）  
  データベースのカラム一行目が横軸、それ以外のカラムが縦軸になります。  
  縦軸はセレクタで選択できます。

サンプル http://suntokaede.github.io/d3LineChart/

### Lisense

MIT
