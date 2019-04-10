# グラフのeps出力
WindowsでJupyter Notebookの実行結果をeps出力しようとしたら、思いの外手こずった。
Plotsというパッケージは、プロットのフロントエンドとして、様々なパッケージを動かせるが、日本語のグラフをepsで出力しようとするとどのバックエンドもうまくいかなかった。 
様々なパッケージを試した末に、Gastonというgnuplotを呼び出すパッケージに落ち着いた。 gnuplot5.0以降は日本語とも親和性が高いようだ。 PlotlyJSも良さそうであったが、Jupyter Notebookで連続してeps画像を出力しようとすると、2枚目で無限ループ？で停止した。

使用例は、D1.ipynbです。

# まとめ
StatPlots, Gadfly, PyPlot, Plotly→日本語がうまくいかない。あるいは、eps出力できない。

PlotlyJS→日本語出力できるが、eps出力しようとすると、停止する。IJuliaでは、うまく動いた。

Gaston→高速、eps、日本語対応

参考文献
Computational and Numerical Methods in Julia 
-Plotting in Julia I-
http://computationalnumericaljulia.com/plotting-in-julia-i/
