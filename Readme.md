# Encriptx 
**Sitio para encriptar un mensaje con caracteres añadidos**

/*![Demo](https://github.com/jmanueltorress/Encriptx/blob/main/assets/img/demo.png "Demo")*/


###### Encriptara texto a caracteres especificos los cuales son:  "e: enter", "i: imes", "a: ai", "o: ober","u: ufat" ######
/*![Demo](https://github.com/jmanueltorress/Encriptx/blob/main/assets/img/demo2.png "Demo")*/

_Java Scrtipt_
**Encriptar:**


` function encriptar(stringEncriptada) {
    let matrizCodigo = [["e", "enter"], ["i", "imes"], ["a", "ai"], ["o","ober"], ["u","ufat"]];
    stringEncriptada = stringEncriptada.toLowerCase(); `

    for(let i=0; i < matrizCodigo.length; i++) {
        if(stringEncriptada.includes(matrizCodigo[i][0])) {
            stringEncriptada = stringEncriptada.replaceAll(matrizCodigo[i][0], matrizCodigo[i][1])
        }                
    }
    return stringEncriptada; 
    
 
**Y para desencriptar mensaje:**

` function btnDesencriptar() {
    const textoEncriptado = desencriptar(inputTexto.value)
    mensaje.value = textoEncriptado
    inputTexto.value = ""  
} 
function desencriptar(stringDesencriptada) {
    let matrizCodigo = [ ["e", "enter"], ["i", "imes"], ["a", "ai"], ["o","ober"], ["u","ufat"]];
    stringDesencriptada = stringDesencriptada.toLowerCase(); `

    for(let i=0; i < matrizCodigo.length; i++) {
        if(stringDesencriptada.includes(matrizCodigo[i][1])) {
            stringDesencriptada = stringDesencriptada.replaceAll(matrizCodigo[i][1], matrizCodigo[i][0])
        }
    }

    return stringDesencriptada;
}
