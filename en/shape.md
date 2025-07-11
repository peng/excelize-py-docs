# Shape

## Add Shape

```python
def add_shape(sheet: str, opts: Shape) -> None
```

Add shape in a sheet by given worksheet index, shape format set (such as offset, scale, aspect ratio setting and print settings) and properties set. For example, add text box (rect shape) in `Sheet1`:

```python
import excelize

f = excelize.new_file()
try:
    f.add_shape(
        "Sheet1",
        excelize.Shape(
            cell="G6",
            type="rect",
            line=excelize.ShapeLine(
                color="4286F4",
                width=1.2,
            ),
            fill=excelize.Fill(
                color=["8EB9FF"],
                pattern=1,
            ),
            paragraph=[
                excelize.RichTextRun(
                    text="Rectangle Shape",
                    font=excelize.Font(
                        bold=True,
                        italic=True,
                        family="Times New Roman",
                        size=19,
                        color="777777",
                        underline="sng",
                    ),
                )
            ],
            width=80,
            height=40,
        ),
    )
    f.save_as("Book1.xlsx")
except RuntimeError as err:
    print(err)
finally:
    err = f.close()
    if err:
        print(err)
```

The following shows the type of shape supported by excelize:

Type|Shape|Preview
---|---|---
accentBorderCallout1 | Callout 1 with Border and Accent Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/accentBorderCallout1.svg" height="50" width="50"></p>
accentBorderCallout2 | Callout 2 with Border and Accent Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/accentBorderCallout2.svg" height="50" width="50"></p>
accentBorderCallout3 | Callout 3 with Border and Accent Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/accentBorderCallout3.svg" height="50" width="50"></p>
accentCallout1 | Callout 1 Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/accentCallout1.svg" height="50" width="50"></p>
accentCallout2 | Callout 2 Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/accentCallout2.svg" height="50" width="50"></p>
accentCallout3 | Callout 3 Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/accentCallout3.svg" height="50" width="50"></p>
actionButtonBackPrevious | Back or Previous Button Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/actionButtonBackPrevious.svg" height="50" width="50"></p>
actionButtonBeginning | Beginning Button Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/actionButtonBeginning.svg" height="50" width="50"></p>
actionButtonBlank | Blank Button Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/actionButtonBlank.svg" height="50" width="50"></p>
actionButtonDocument | Document Button Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/actionButtonDocument.svg" height="50" width="50"></p>
actionButtonEnd | End Button Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/actionButtonEnd.svg" height="50" width="50"></p>
actionButtonForwardNext | Forward or Next Button Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/actionButtonForwardNext.svg" height="50" width="50"></p>
actionButtonHelp | Help Button Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/actionButtonHelp.svg" height="50" width="50"></p>
actionButtonHome | Home Button Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/actionButtonHome.svg" height="50" width="50"></p>
actionButtonInformation | Information Button Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/actionButtonInformation.svg" height="50" width="50"></p>
actionButtonMovie | Movie Button Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/actionButtonMovie.svg" height="50" width="50"></p>
actionButtonReturn | Return Button Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/actionButtonReturn.svg" height="50" width="50"></p>
actionButtonSound | Sound Button Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/actionButtonSound.svg" height="50" width="50"></p>
arc | Curved Arc Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/arc.svg" height="50" width="50"></p>
bentArrow | Bent Arrow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/bentArrow.svg" height="50" width="50"></p>
bentConnector2 | Bent Connector 2 Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/bentConnector2.svg" height="50" width="50"></p>
bentConnector3 | Bent Connector 3 Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/bentConnector3.svg" height="50" width="50"></p>
bentConnector4 | Bent Connector 4 Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/bentConnector4.svg" height="50" width="50"></p>
bentConnector5 | Bent Connector 5 Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/bentConnector5.svg" height="50" width="50"></p>
bentUpArrow | Bent Up Arrow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/bentUpArrow.svg" height="50" width="50"></p>
bevel | Bevel Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/bevel.svg" height="50" width="50"></p>
blockArc | Block Arc Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/blockArc.svg" height="50" width="50"></p>
borderCallout1 | Callout 1 with Border Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/borderCallout1.svg" height="50" width="50"></p>
borderCallout2 | Callout 2 with Border Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/borderCallout2.svg" height="50" width="50"></p>
borderCallout3 | Callout 3 with Border Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/borderCallout3.svg" height="50" width="50"></p>
bracePair | Brace Pair Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/bracePair.svg" height="50" width="50"></p>
bracketPair | Bracket Pair Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/bracketPair.svg" height="50" width="50"></p>
callout1 | Callout 1 Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/callout1.svg" height="50" width="50"></p>
callout2 | Callout 2 Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/callout2.svg" height="50" width="50"></p>
callout3 | Callout 3 Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/callout3.svg" height="50" width="50"></p>
can | Can Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/can.svg" height="50" width="50"></p>
chartPlus | Chart Plus Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/chartPlus.svg" height="50" width="50"></p>
chartStar | Chart Star Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/chartStar.svg" height="50" width="50"></p>
chartX | Chart X Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/chartX.svg" height="50" width="50"></p>
chevron | Chevron Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/chevron.svg" height="50" width="50"></p>
chord | Chord Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/chord.svg" height="50" width="50"></p>
circularArrow | Circular Arrow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/circularArrow.svg" height="50" width="50"></p>
cloud | Cloud Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/cloud.svg" height="50" width="50"></p>
cloudCallout | Callout Cloud Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/cloudCallout.svg" height="50" width="50"></p>
corner | Corner Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/corner.svg" height="50" width="50"></p>
cornerTabs | Corner Tabs Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/cornerTabs.svg" height="50" width="50"></p>
cube | Cube Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/cube.svg" height="50" width="50"></p>
curvedConnector2 | Curved Connector 2 Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/curvedConnector2.svg" height="50" width="50"></p>
curvedConnector3 | Curved Connector 3 Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/curvedConnector3.svg" height="50" width="50"></p>
curvedConnector4 | Curved Connector 4 Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/curvedConnector4.svg" height="50" width="50"></p>
curvedConnector5 | Curved Connector 5 Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/curvedConnector5.svg" height="50" width="50"></p>
curvedDownArrow | Curved Down Arrow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/curvedDownArrow.svg" height="50" width="50"></p>
curvedLeftArrow | Curved Left Arrow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/curvedLeftArrow.svg" height="50" width="50"></p>
curvedRightArrow | Curved Right Arrow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/curvedRightArrow.svg" height="50" width="50"></p>
curvedUpArrow | Curved Up Arrow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/curvedUpArrow.svg" height="50" width="50"></p>
decagon | Decagon Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/decagon.svg" height="50" width="50"></p>
diagStripe | Diagonal Stripe Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/diagStripe.svg" height="50" width="50"></p>
diamond | Diamond Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/diamond.svg" height="50" width="50"></p>
dodecagon | Dodecagon Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/dodecagon.svg" height="50" width="50"></p>
donut | Donut Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/donut.svg" height="50" width="50"></p>
doubleWave | Double Wave Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/doubleWave.svg" height="50" width="50"></p>
downArrow | Down Arrow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/downArrow.svg" height="50" width="50"></p>
downArrowCallout | Callout Down Arrow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/downArrowCallout.svg" height="50" width="50"></p>
ellipse | Ellipse Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/ellipse.svg" height="50" width="50"></p>
ellipseRibbon | Ellipse Ribbon Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/ellipseRibbon.svg" height="50" width="50"></p>
ellipseRibbon2 | Ellipse Ribbon 2 Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/ellipseRibbon2.svg" height="50" width="50"></p>
flowChartAlternateProcess | Alternate Process Flow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/flowChartAlternateProcess.svg" height="50" width="50"></p>
flowChartCollate | Collate Flow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/flowChartCollate.svg" height="50" width="50"></p>
flowChartConnector | Connector Flow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/flowChartConnector.svg" height="50" width="50"></p>
flowChartDecision | Decision Flow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/flowChartDecision.svg" height="50" width="50"></p>
flowChartDelay | Delay Flow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/flowChartDelay.svg" height="50" width="50"></p>
flowChartDisplay | Display Flow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/flowChartDisplay.svg" height="50" width="50"></p>
flowChartDocument | Document Flow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/flowChartDocument.svg" height="50" width="50"></p>
flowChartExtract | Extract Flow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/flowChartExtract.svg" height="50" width="50"></p>
flowChartInputOutput | Input Output Flow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/flowChartInternalStorage.svg" height="50" width="50"></p>
flowChartInternalStorage | Internal Storage Flow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/flowChartInternalStorage.svg" height="50" width="50"></p>
flowChartMagneticDisk | Magnetic Disk Flow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/flowChartMagneticDisk.svg" height="50" width="50"></p>
flowChartMagneticDrum | Magnetic Drum Flow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/flowChartMagneticDrum.svg" height="50" width="50"></p>
flowChartMagneticTape | Magnetic Tape Flow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/flowChartMagneticTape.svg" height="50" width="50"></p>
flowChartManualInput | Manual Input Flow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/flowChartManualInput.svg" height="50" width="50"></p>
flowChartManualOperation | Manual Operation Flow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/flowChartManualOperation.svg" height="50" width="50"></p>
flowChartMerge | Merge Flow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/flowChartMerge.svg" height="50" width="50"></p>
flowChartMultidocument | Multi-Document Flow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/flowChartMultidocument.svg" height="50" width="50"></p>
flowChartOfflineStorage | Offline Storage Flow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/flowChartOfflineStorage.svg" height="50" width="50"></p>
flowChartOffpageConnector | Off-Page Connector Flow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/flowChartOffpageConnector.svg" height="50" width="50"></p>
flowChartOnlineStorage | Online Storage Flow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/flowChartOnlineStorage.svg" height="50" width="50"></p>
flowChartOr | Or Flow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/flowChartOr.svg" height="50" width="50"></p>
flowChartPredefinedProcess | Predefined Process Flow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/flowChartPredefinedProcess.svg" height="50" width="50"></p>
flowChartPreparation | Preparation Flow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/flowChartPredefinedProcess.svg" height="50" width="50"></p>
flowChartProcess | Process Flow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/flowChartPreparation.svg" height="50" width="50"></p>
flowChartPunchedCard | Punched Card Flow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/flowChartPunchedCard.svg" height="50" width="50"></p>
flowChartPunchedTape | Punched Tape Flow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/flowChartPunchedTape.svg" height="50" width="50"></p>
flowChartSort | Sort Flow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/flowChartSort.svg" height="50" width="50"></p>
flowChartSummingJunction | Summing Junction Flow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/flowChartSummingJunction.svg" height="50" width="50"></p>
flowChartTerminator | Terminator Flow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/flowChartTerminator.svg" height="50" width="50"></p>
foldedCorner | Folded Corner Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/foldedCorner.svg" height="50" width="50"></p>
frame | Frame Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/frame.svg" height="50" width="50"></p>
funnel | Funnel Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/funnel.svg" height="50" width="50"></p>
gear6 | Gear 6 Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/gear6.svg" height="50" width="50"></p>
gear9 | Gear 9 Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/gear9.svg" height="50" width="50"></p>
halfFrame | Half Frame Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/halfFrame.svg" height="50" width="50"></p>
heart | Heart Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/heart.svg" height="50" width="50"></p>
heptagon | Heptagon Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/heptagon.svg" height="50" width="50"></p>
hexagon | Hexagon Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/hexagon.svg" height="50" width="50"></p>
homePlate | Home Plate Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/homePlate.svg" height="50" width="50"></p>
horizontalScroll | Horizontal Scroll Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/horizontalScroll.svg" height="50" width="50"></p>
irregularSeal1 | Irregular Seal 1 Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/irregularSeal1.svg" height="50" width="50"></p>
irregularSeal2 | Irregular Seal 2 Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/irregularSeal2.svg" height="50" width="50"></p>
leftArrow | Left Arrow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/leftArrow.svg" height="50" width="50"></p>
leftArrowCallout | Callout Left Arrow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/leftArrowCallout.svg" height="50" width="50"></p>
leftBrace | Left Brace Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/leftBrace.svg" height="50" width="50"></p>
leftBracket | Left Bracket Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/leftBracket.svg" height="50" width="50"></p>
leftCircularArrow | Left Circular Arrow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/leftCircularArrow.svg" height="50" width="50"></p>
leftRightArrow | Left Right Arrow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/leftRightArrow.svg" height="50" width="50"></p>
leftRightArrowCallout | Callout Left Right Arrow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/leftRightArrowCallout.svg" height="50" width="50"></p>
leftRightCircularArrow | Left Right Circular Arrow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/leftRightCircularArrow.svg" height="50" width="50"></p>
leftRightRibbon | Left Right Ribbon Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/leftRightRibbon.svg" height="50" width="50"></p>
leftRightUpArrow | Left Right Up Arrow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/leftRightUpArrow.svg" height="50" width="50"></p>
leftUpArrow | Left Up Arrow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/leftUpArrow.svg" height="50" width="50"></p>
lightningBolt | Lightning Bolt Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/lightningBolt.svg" height="50" width="50"></p>
line | Line Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/line.svg" height="50" width="50"></p>
lineInv | Line Inverse Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/lineInv.svg" height="50" width="50"></p>
mathDivide | Divide Math Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/mathDivide.svg" height="50" width="50"></p>
mathEqual | Equal Math Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/mathEqual.svg" height="50" width="50"></p>
mathMinus | Minus Math Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/mathMinus.svg" height="50" width="50"></p>
mathMultiply | Multiply Math Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/mathMultiply.svg" height="50" width="50"></p>
mathNotEqual | Not Equal Math Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/mathNotEqual.svg" height="50" width="50"></p>
mathPlus | Plus Math Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/mathPlus.svg" height="50" width="50"></p>
moon | Moon Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/moon.svg" height="50" width="50"></p>
nonIsoscelesTrapezoid | Non-Isosceles Trapezoid Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/nonIsoscelesTrapezoid.svg" height="50" width="50"></p>
noSmoking | No Smoking Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/noSmoking.svg" height="50" width="50"></p>
notchedRightArrow | Notched Right Arrow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/notchedRightArrow.svg" height="50" width="50"></p>
octagon | Octagon Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/octagon.svg" height="50" width="50"></p>
parallelogram | Parallelogram Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/parallelogram.svg" height="50" width="50"></p>
pentagon | Pentagon Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/pentagon.svg" height="50" width="50"></p>
pie | Pie Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/pie.svg" height="50" width="50"></p>
pieWedge | Pie Wedge Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/pieWedge.svg" height="50" width="50"></p>
plaque | Plaque Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/plaque.svg" height="50" width="50"></p>
plaqueTabs | Plaque Tabs Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/plaqueTabs.svg" height="50" width="50"></p>
plus | Plus Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/plus.svg" height="50" width="50"></p>
quadArrow | Quad-Arrow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/quadArrow.svg" height="50" width="50"></p>
quadArrowCallout | Callout Quad-Arrow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/quadArrowCallout.svg" height="50" width="50"></p>
rect | Rectangle Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/rect.svg" height="50" width="50"></p>
ribbon | Ribbon Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/ribbon.svg" height="50" width="50"></p>
ribbon2 | Ribbon 2 Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/ribbon2.svg" height="50" width="50"></p>
rightArrow | Right Arrow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/rightArrow.svg" height="50" width="50"></p>
rightArrowCallout | Callout Right Arrow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/rightArrowCallout.svg" height="50" width="50"></p>
rightBrace | Right Brace Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/rightBrace.svg" height="50" width="50"></p>
rightBracket | Right Bracket Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/rightBracket.svg" height="50" width="50"></p>
round1Rect | One Round Corner Rectangle Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/round1Rect.svg" height="50" width="50"></p>
round2DiagRect | Two Diagonal Round Corner Rectangle Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/round2DiagRect.svg" height="50" width="50"></p>
round2SameRect | Two Same-side Round Corner Rectangle Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/round2SameRect.svg" height="50" width="50"></p>
roundRect | Round Corner Rectangle Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/roundRect.svg" height="50" width="50"></p>
rtTriangle | Right Triangle Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/rtTriangle.svg" height="50" width="50"></p>
smileyFace | Smiley Face Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/smileyFace.svg" height="50" width="50"></p>
snip1Rect | One Snip Corner Rectangle Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/snip1Rect.svg" height="50" width="50"></p>
snip2DiagRect | Two Diagonal Snip Corner Rectangle Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/snip2DiagRect.svg" height="50" width="50"></p>
snip2SameRect | Two Same-side Snip Corner Rectangle Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/snip2SameRect.svg" height="50" width="50"></p>
snipRoundRect | One Snip One Round Corner Rectangle Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/snipRoundRect.svg" height="50" width="50"></p>
squareTabs | Square Tabs Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/squareTabs.svg" height="50" width="50"></p>
star10 | Ten Pointed Star Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/star10.svg" height="50" width="50"></p>
star12 | Twelve Pointed Star Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/star12.svg" height="50" width="50"></p>
star16 | Sixteen Pointed Star Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/star16.svg" height="50" width="50"></p>
star24 | Twenty Four Pointed Star Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/star24.svg" height="50" width="50"></p>
star32 | Thirty Two Pointed Star Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/star32.svg" height="50" width="50"></p>
star4 | Four Pointed Star Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/star4.svg" height="50" width="50"></p>
star5 | Five Pointed Star Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/star5.svg" height="50" width="50"></p>
star6 | Six Pointed Star Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/star6.svg" height="50" width="50"></p>
star7 | Seven Pointed Star Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/star7.svg" height="50" width="50"></p>
star8 | Eight Pointed Star Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/star8.svg" height="50" width="50"></p>
straightConnector1 | Straight Connector 1 Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/straightConnector1.svg" height="50" width="50"></p>
stripedRightArrow | Striped Right Arrow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/stripedRightArrow.svg" height="50" width="50"></p>
sun | Sun Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/sun.svg" height="50" width="50"></p>
swooshArrow | Swoosh Arrow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/swooshArrow.svg" height="50" width="50"></p>
teardrop | Teardrop Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/teardrop.svg" height="50" width="50"></p>
trapezoid | Trapezoid Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/trapezoid.svg" height="50" width="50"></p>
triangle | Triangle Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/triangle.svg" height="50" width="50"></p>
upArrow | Up Arrow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/upArrow.svg" height="50" width="50"></p>
upArrowCallout | Callout Up Arrow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/upArrowCallout.svg" height="50" width="50"></p>
upDownArrow | Up Down Arrow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/upDownArrow.svg" height="50" width="50"></p>
upDownArrowCallout | Callout Up Down Arrow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/upDownArrowCallout.svg" height="50" width="50"></p>
uturnArrow | U-Turn Arrow Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/uturnArrow.svg" height="50" width="50"></p>
verticalScroll | Vertical Scroll Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/verticalScroll.svg" height="50" width="50"></p>
wave | Wave Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/wave.svg" height="50" width="50"></p>
wedgeEllipseCallout | Callout Wedge Ellipse Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/wedgeEllipseCallout.svg" height="50" width="50"></p>
wedgeRectCallout | Callout Wedge Rectangle Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/wedgeRectCallout.svg" height="50" width="50"></p>
wedgeRoundRectCallout | Callout Wedge Round Rectangle Shape | <p style="text-align: center;"><img src="https://xuri.me/excelize/images/shapes/wedgeRoundRectCallout.svg" height="50" width="50"></p>
