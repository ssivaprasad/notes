

---------------------------------------------------------------- Comparative Relative Strength --------------------------------------------------------------

//NIFTYPVTBANK : Nifty Private Bank
//CNXIT : Nifty IT

//@version=4
study("Comparative Relative Strength", shorttitle="RS Comparative") 
base_sym = security(syminfo.tickerid, timeframe.period, close)

index_sym = "NIFTYPVTBANK"

compare_ticker = input(index_sym, type=input.symbol, title="Comparative Symbol")
compare_sym = security(compare_ticker, timeframe.period, close)

rs = base_sym/compare_sym
plot(rs, title="RS", color=color.black, linewidth=1)
