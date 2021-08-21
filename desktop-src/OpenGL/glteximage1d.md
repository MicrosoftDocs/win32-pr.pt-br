---
title: Função glTexImage1D (Gl.h)
description: A função glTexImage1D especifica uma imagem de textura unidimensional.
ms.assetid: 4f537b89-2ea2-4e2e-8c57-c372bf53f12c
keywords:
- Função glTexImage1D OpenGL
topic_type:
- apiref
api_name:
- glTexImage1D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efd443389439b6d012533d3184739dfa849d672d76a8eced0e8ea244601d4122
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119490246"
---
# <a name="glteximage1d-function"></a>Função glTexImage1D

A **função glTexImage1D** especifica uma imagem de textura unidimensional.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glTexImage1D(
         GLenum  target,
         GLint   level,
         GLint   internalformat,
         GLsizei width,
         GLint   border,
         GLint   format,
         GLenum  type,
   const GLvoid  *pixels
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*destino* 
</dt> <dd>

A textura de destino. Deve ser GL \_ TEXTURE \_ 1D.

</dd> <dt>

*level* 
</dt> <dd>

O número de nível de detalhes. Nível 0 é o nível de imagem base. O *nível n* é a imagem *de* redução de mipmap n.

</dd> <dt>

*internalformat* 
</dt> <dd>

Especifica o número de componentes de cores na textura. Deve ser 1, 2, 3 ou 4 ou uma das seguintes constantes simbólicas: GL \_ ALPHA, GL \_ ALPHA4, GL \_ ALPHA8, GL \_ ALPHA12, GL \_ ALPHA16, \_ GL LUMINANCE, GL \_ LUMINANCE4, GL \_ LUMINANCE8, GL \_ LUMINANCE12, GL \_ \_ LUMINANCE16, GL LUMINANCE \_ ALPHA, GL \_ LUMINANCE4 \_ ALPHA4, GL \_ LUMINANCE6 \_ ALPHA2, GL \_ LUMINANCE8 \_ ALPHA8, GL \_ LUMINANCE12 \_ ALPHA4, GL \_ LUMINANCE12 \_ ALPHA12, GL \_ LUMINANCE16 \_ ALPHA16, GL INTENSITY, GL \_ GL \_ INTENSITY4, GL \_ INTENSITY8, \_ GL INTENSITY12, GL \_ INTENSITY16, GL \_ RGB, GL \_ R3 \_ G3 \_ B2, GL \_ RGB4, GL \_ RGB5, GL \_ RGB8, GL \_ RGB10, GL \_ RGB12, GL RGB12, GL \_ RGBGB16, GL \_ RGBA, GL \_ RGBA2, GL \_ RGBA4, GL \_ RGB5 \_ A1, GL \_ RGBA8, GL \_ RGB10 \_ A2, GL \_ RGBA12 ou GL \_ RGBA16.

</dd> <dt>

*width* 
</dt> <dd>

A largura da imagem de textura. Deve ser 2 *n* + 2( *borda* ) para algum inteiro *n*. A altura da imagem de textura é 1.

</dd> <dt>

*Fronteira* 
</dt> <dd>

A largura da borda. Deve ser 0 ou 1.

</dd> <dt>

*format* 
</dt> <dd>

O formato dos dados de pixel. Ele pode assumir um dos nove valores simbólicos.



| Valor                                                                                                                                                                         | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <dt>**GL \_ COLOR \_ INDEX**</dt> </dl>             | Cada elemento é um único valor, um índice de cores. Ele é convertido em ponto fixo (com um número não especificado de 0 bits à direita do ponto binário), deslocado para a esquerda ou para a direita, dependendo do valor e do sinal de GL INDEX SHIFT e adicionado a \_ \_ GL INDEX OFFSET \_ \_ (consulte [**glPixelTransfer**](glpixeltransfer.md)). O índice resultante é convertido em um conjunto de componentes de cores usando o GL PIXEL MAP I TO R, GL PIXEL MAP I TO G, GL PIXEL MAP I TO B e GL PIXEL MAP I para tabelas A e fixados no intervalo \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \[ 0,1 \] .<br/> |
| <span id="GL_RED"></span><span id="gl_red"></span><dl> <dt>**GL \_ RED**</dt> </dl>                                      | Cada elemento é um único componente vermelho. Ele é convertido em ponto flutuante e montado em um elemento RGBA anexando 0,0 para verde e azul e 1,0 para alfa. Cada componente é multiplicado pelo fator de escala assinado GL c SCALE, adicionado ao desvio assinado GL c BIAS e fixado ao intervalo \_ \_ \_ \_ \[ 0,1 \] (consulte **glPixelTransfer**).<br/>                                                                                                                                                                                                |
| <span id="GL_GREEN"></span><span id="gl_green"></span><dl> <dt>**GL \_ GREEN**</dt> </dl>                                | Cada elemento é um único componente verde. Ele é convertido em ponto flutuante e montado em um elemento RGBA anexando 0,0 para vermelho e azul e 1,0 para alfa. Cada componente é multiplicado pelo fator de escala assinado GL c SCALE, adicionado ao desvio assinado GL c BIAS e fixado ao intervalo \_ \_ \_ \_ \[ 0,1 \] (consulte [**glPixelTransfer**](glpixeltransfer.md)).<br/>                                                                                                                                                                         |
| <span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <dt>**GL \_ BLUE**</dt> </dl>                                   | Cada elemento é um único componente azul. Ele é convertido em ponto flutuante e montado em um elemento RGBA anexando 0,0 para vermelho e verde e 1,0 para alfa. Cada componente é multiplicado pelo fator de escala assinado GL c SCALE, adicionado ao desvio assinado GL c BIAS e fixado ao intervalo \_ \_ \_ \_ \[ 0,1 \] (consulte **glPixelTransfer**).<br/>                                                                                                                                                                                                |
| <span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <dt>**GL \_ ALPHA**</dt> </dl>                                | Cada elemento é um único componente vermelho. Ele é convertido em ponto flutuante e montado em um elemento RGBA anexando 0,0 para vermelho, verde e azul. Cada componente é multiplicado pelo fator de escala assinado GL c SCALE, adicionado ao desvio assinado GL c BIAS e fixado ao intervalo \_ \_ \_ \_ \[ 0,1 \] (consulte [**glPixelTransfer**](glpixeltransfer.md)).<br/>                                                                                                                                                                                      |
| <span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <dt>**GL \_ RGB**</dt> </dl>                                      | Cada elemento é um triplo RGB. Ele é convertido em ponto flutuante e montado em um elemento RGBA anexando 1,0 para alfa. Cada componente é multiplicado pelo fator de escala assinado GL c SCALE, adicionado ao desvio assinado GL c BIAS e fixado ao intervalo \_ \_ \_ \_ \[ 0,1 \] (consulte **glPixelTransfer**).<br/>                                                                                                                                                                                                                                     |
| <span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <dt>**GL \_ RGBA**</dt> </dl>                                   | Cada elemento é um elemento RGBA completo. Ele é convertido em ponto flutuante. Cada componente é multiplicado pelo fator de escala assinado GL c SCALE, adicionado ao desvio assinado GL c BIAS e fixado ao intervalo \_ \_ \_ \_ \[ 0,1 \] (consulte **glPixelTransfer**).<br/>                                                                                                                                                                                                                                                                                         |
| <span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <dt>**GL \_ BGR \_ EXT**</dt> </dl>                         | Cada pixel é um grupo de três componentes nesta ordem: azul, verde, vermelho.<br/> GL BGR EXT fornece um formato que corresponde ao layout de memória \_ \_ Windows DIBs (bitmaps independentes de dispositivo). Portanto, seus aplicativos podem usar os mesmos dados com chamadas Windows função e chamadas de função de pixel OpenGL.<br/>                                                                                                                                                                                                                                      |
| <span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <dt>**GL \_ BGRA \_ EXT**</dt> </dl>                      | Cada pixel é um grupo de quatro componentes nessa ordem: azul, verde, vermelho, alfa.<br/> GL BGRA EXT fornece um formato que corresponde ao layout de memória \_ \_ Windows DIBs (bitmaps independentes de dispositivo). Portanto, seus aplicativos podem usar os mesmos dados com chamadas Windows função e chamadas de função de pixel OpenGL.<br/>                                                                                                                                                                                                                               |
| <span id="GL_LUMINANCE"></span><span id="gl_luminance"></span><dl> <dt>**GL \_ LUMINANCE**</dt> </dl>                    | Cada elemento é um único valor de luminância. Ele é convertido em ponto flutuante e, em seguida, montado em um elemento RGBA replicando o valor de luminância três vezes para vermelho, verde e azul e anexando 1,0 para alfa. Cada componente é multiplicado pelo fator de escala assinado GL c SCALE, adicionado ao desvio assinado GL c BIAS e fixado ao intervalo \_ \_ \_ \_ \[ 0,1 \] (consulte [**glPixelTransfer**](glpixeltransfer.md)).<br/>                                                                                                                   |
| <span id="GL_LUMINANCE_ALPHA"></span><span id="gl_luminance_alpha"></span><dl> <dt>**GL \_ LUMINANCE \_ ALPHA**</dt> </dl> | Cada elemento é um par de luminância/alfa. Ele é convertido em ponto flutuante e, em seguida, montado em um elemento RGBA replicando o valor de luminância três vezes para vermelho, verde e azul. Cada componente é multiplicado pelo fator de escala assinado GL c SCALE, adicionado ao desvio assinado GL c BIAS e fixado ao intervalo \_ \_ \_ \_ \[ 0,1 \] (consulte **glPixelTransfer**).<br/>                                                                                                                                                                         |



 

</dd> <dt>

*tipo* 
</dt> <dd>

O tipo de dados dos dados de pixel. Os seguintes valores simbólicos são aceitos: GL \_ \_ \_ UNSIGNED BYTE, GL BYTE, \_ GL BITMAP, GL \_ UNSIGNED \_ SHORT, GL \_ SHORT, GL \_ UNSIGNED \_ INT, GL \_ INT e GL \_ FLOAT.

</dd> <dt>

*pixels* 
</dt> <dd>

Um ponteiro para os dados de imagem na memória.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela [**função glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significado                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *target* não era um GL \_ TEXTURE.<br/>                                                                                                                                                                                    |
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *format* não era uma constante de *formato* aceita. Somente constantes de formato diferentes de GL \_ STENCIL \_ INDEX e GL DEPTH COMPONENT são \_ \_ aceitas. Consulte a descrição do parâmetro *de format* para ver uma lista de valores possíveis.<br/> |
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *type* não era uma *constante de* tipo.<br/>                                                                                                                                                                                   |
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *O tipo* era GL \_ BITMAP *e o formato* não era GL \_ COLOR \_ INDEX.<br/>                                                                                                                                                        |
| <dl> <dt>**VALOR INVÁLIDO DE GL \_ \_**</dt> </dl>     | *level* era menor que zero ou maior que log2 *max*, em que *max* era o valor retornado de GL \_ MAX TEXTURE \_ \_ SIZE.<br/>                                                                                                 |
| <dl> <dt>**VALOR INVÁLIDO DE GL \_ \_**</dt> </dl>     | *internalformat* não era 1, 2, 3 ou 4.<br/>                                                                                                                                                                         |
| <dl> <dt>**VALOR INVÁLIDO DE GL \_ \_**</dt> </dl>     | *width* era menor que zero ou maior que 2 + GL MAX TEXTURE SIZE ou não pôde ser representado como \_ \_ \_ 2 *n* + 2(border) para algum valor inteiro de n .<br/>                                                            |
| <dl> <dt>**VALOR INVÁLIDO DE GL \_ \_**</dt> </dl>     | *border* não era 0 ou 1.<br/>                                                                                                                                                                                            |
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd.**](glend.md)<br/>                                                                                          |



## <a name="remarks"></a>Comentários

A **função glTexImage1D** especifica uma imagem de textura unidimensional. A texturização mapeia uma parte de uma imagem *de textura especificada* para cada primitivo gráfico para o qual a texturização está habilitada. A texturagem unidimensional está habilitada e desabilitada usando [**glEnable**](glenable.md) e **glDisable** com o argumento GL \_ TEXTURE \_ 1D.

As imagens de textura são definidas **com glTexImage1D.** Os argumentos descrevem os parâmetros da imagem de textura, como largura, largura da borda, número de nível de detalhe (consulte [**glTexParameter**](gltexparameter-functions.md)) e número de componentes de cores fornecidos. Os últimos três argumentos descrevem a maneira como a imagem é representada na memória. Esses argumentos são idênticos aos formatos de pixel usados para [**glDrawPixels**](gldrawpixels.md).

Os dados são lidos de *pixels* como uma sequência de bytes assinados ou não assinados, shorts ou longs ou valores de ponto flutuante de precisão simples, dependendo do *tipo*. Esses valores são agrupados em conjuntos de um, dois, três ou quatro valores, dependendo do *formato*, para formar elementos. Se *o tipo* for GL BITMAP, os dados serão considerados como uma cadeia de caracteres de bytes não assinados (e o formato deverá \_ ser GL COLOR  \_ \_ INDEX). Cada byte de dados é tratado como oito elementos de 1 bit, com a ordenação de bits determinada por GL \_ UNPACK \_ LSB \_ FIRST (consulte [**glPixelStore**](glpixelstore-functions.md)).

Uma imagem de textura pode ter até quatro componentes por elemento de textura, dependendo dos *componentes*. Uma imagem de textura de um componente usa apenas o componente vermelho da cor RGBA extraída de *pixels*. Uma imagem de dois componentes usa os valores R e A. Uma imagem de três componentes usa os valores R, G e B. Uma imagem de quatro componentes usa todos os componentes RGBA.

A texturing não tem efeito no modo de índice de cores.

A imagem de textura pode ser representada pelos mesmos formatos de dados que os pixels em um [**comando glDrawPixels,**](gldrawpixels.md) exceto que GL STENCIL INDEX e GL DEPTH COMPONENT não podem \_ \_ ser \_ \_ usados. Os [**modos glPixelStore**](glpixelstore-functions.md) e [**glPixelTransfer**](glpixeltransfer.md) afetam as imagens de textura exatamente da maneira como afetam **glDrawPixels**.

Uma imagem de textura com largura zero indica a textura nula. Se a textura nula for especificada para o nível de detalhes 0, será como se a texturing estivesse desabilitada.

As funções a seguir recuperam informações relacionadas **a glTexImageID**:

[**glGetTexImage**](glgetteximage.md)

[**glIsEnabled com**](glisenabled.md) o argumento GL \_ TEXTURE \_ 1D

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glCopyTexImage1D**](glcopyteximage1d.md)
</dt> <dt>

[**glCopyTexImage2D**](glcopyteximage2d.md)
</dt> <dt>

[**glCopyTexSubImage1D**](glcopytexsubimage1d.md)
</dt> <dt>

[**glCopyTexSubImage2D**](glcopytexsubimage2d.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glFog**](glfog.md)
</dt> <dt>

[**glGetTexImage**](glgetteximage.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glTexEnv**](gltexenv-functions.md)
</dt> <dt>

[**glTexGen**](gltexgen-functions.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexSubImage1D**](gltexsubimage1d.md)
</dt> <dt>

[**glTexSubImage2D**](gltexsubimage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





