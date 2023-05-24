# 5kyu

## RGB To Hex Conversion

```JS
#1:
function rgb(r, g, b){

  let string = []
  string.push(r,g,b)
  string = string.map((e) => e < 16 && e >= 0 ? "0" + e.toString(16).toUpperCase() : e )
  string = string.map((e) => e >= 255 ? "FF" : e )
  string = string.map((e) => e < 0 ? "00" : e )
  string = string.map((e) => e > 0 && e < 255 ? e.toString(16).toUpperCase() : e )

return string.join("")
}

#2:
function rgb(r, g, b){
	return toHex(r)+toHex(g)+toHex(b);
}

function toHex(d) {
    if(d < 0 ) {return "00";}
    if(d > 255 ) {return "FF";}
    return  ("0"+(Number(d).toString(16))).slice(-2).toUpperCase()
}

```
