# MLLayout (swift版，自行添加桥接)
小型轻量级自动布局，基于UIView的分类。

#  对齐类型枚举，设置控件相对于父视图的位置
# - TopLeft:      左上
# - TopRight:     右上
# - TopCenter:    中上
# - BottomLeft:   左下
# - BottomRight:  右下
# - BottomCenter: 中下
# - CenterLeft:   左中
# - CenterRight:  右中
# - CenterCenter: 中中


# MLView 位于 view 内部，左上点对齐，大小 默认 设置nil
MLView.ff_AlignInner(type: ff_AlignType.TopLeft, referView: view, size: nil)

# 垂直布局：相对于 view 的右上点对齐 ，大小默认 设置nil
MLView.ff_AlignVertical(type: ff_AlignType.TopRight, referView: view, size: nil)

# 水平布局：相对于 view 的中心点对齐 ，大小默认 设置nil，偏移量 0 设置nil
MLView.ml_AlignHorizontal(type: ml_AlignType.CenterCenter, referView: view, size: nil, offset: nil);

# 水平自动平分多个 view 可以指定数组，根据数组中的 view 平分， insets 指定边距
MLView.ml_HorizontalTile([view], insets: nil);

# 垂直自动平分多个 view 可以指定数组，根据数组中的 view 平分， insets 指定边距
MLView.ml_VerticalTile([view], insets: nil);

# 填充 某个视图，insets 指定边距
MLView.ml_Fill(view, insets: nil);