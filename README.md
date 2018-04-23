# Julia_Gaston

Juliaでグラフを出力しようとしたら、思いの外手こずった。

色々なバックエンドをPlotsというフロントエンドによって、動かせるようだが、日本語やepsで出力しようとするとどれもうまくいかなかった。
色々なパッケージを試した末に、Gastonというgnuplotを呼び出すパッケージに落ち着いた。
gnuplot5.0以降は日本語とも親和性が高いようだ。
PlotlyJSも良さそうであったが、Jupyter Notebookでで連続してeps画像を出力しようとすると、2枚目で無限ループ？で停止した。

# まとめ
StatPlots, Gadfly, PyPlot, Plotly→日本語がうまくいかない。あるいは、eps出力できない。
PlotlyJS→日本語出力できるが、eps出力しようとすると、停止する。IJuliaでは、うまく動いた。
Gaston→高速、eps、日本語対応

参考文献
Computational and Numerical Methods in Julia 
-Plotting in Julia I-
