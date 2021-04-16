---
title: função glTexImage2D (GL. h)
description: A função glTexImage2D especifica uma imagem de textura bidimensional.
ms.assetid: e8b9c692-5239-47de-86eb-80c247c60e1d
keywords:
- função glTexImage2D OpenGL
topic_type:
- apiref
api_name:
- glTexImage2D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ba2d5bc6f966d9b10c0dadccb221086e64de827
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105751090"
---
# <a name="glteximage2d-function"></a>função glTexImage2D

A função **glTexImage2D** especifica uma imagem de textura bidimensional.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glTexImage2D(
         GLenum  target,
         GLint   level,
         GLint   internalformat,
         GLsizei width,
         GLsizei height,
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

A textura de destino. Deve ser GL de \_ textura \_ 2D.

</dd> <dt>

*level* 
</dt> <dd>

O número de nível de detalhe. Nível 0 é o nível de imagem base. O nível *n* é a imagem de redução *n* º mipmap.

</dd> <dt>

*internalformat* 
</dt> <dd>

O número de componentes de cor na textura. Deve ser 1, 2, 3 ou 4, ou uma das seguintes constantes simbólicas: GL \_ alfa, GL \_ ALPHA4, GL \_ ALPHA8, GL \_ ALPHA12, GL \_ ALPHA16, GL \_ luminescência, GL \_ LUMINANCE4, GL \_ LUMINANCE8, GL \_ LUMINANCE12, GL \_ LUMINANCE16, GL \_ luminância \_ alfa, GL \_ LUMINANCE4 \_ ALPHA4, GL \_ LUMINANCE6 \_ ALPHA2, GL \_ LUMINANCE8 \_ ALPHA8, GL \_ LUMINANCE12 \_ ALPHA4, GL \_ LUMINANCE12 \_ ALPHA12, GL \_ LUMINANCE16 \_ ALPHA16, GL \_ intensidade, GL \_ INTENSITY4, GL \_ INTENSITY8, GL \_ INTENSITY12, GL \_ INTENSITY16, GL \_ R3 \_ G3 \_ B2, GL \_ RGB, GL \_ RGB4, GL \_ RGB5, GL \_ RGB8, GL \_ RGB10, GL \_ RGB12, GL \_ RGB16, GL \_ RGBA, GL \_ RGBA2, GL \_ RGBA4, GL \_ RGB5 \_ a1, GL \_ RGBA8, GL RGB10 \_ \_ a2, GL \_ RGBA12 ou GL \_ RGBA16.

</dd> <dt>

*width* 
</dt> <dd>

A largura da imagem de textura. Deve ser 2 *n* + 2 (*Border*) para algum número inteiro *n*.

</dd> <dt>

*altura* 
</dt> <dd>

A altura da imagem de textura. Deve ser 2 *<sup>m</sup>* + 2 (*Border*) para um inteiro *m*.

</dd> <dt>

*borda* 
</dt> <dd>

A largura da borda. Deve ser 0 ou 1.

</dd> <dt>

*format* 
</dt> <dd>

O formato dos dados de pixel. Ele pode assumir um dos nove valores simbólicos.



| Valor                                                                                                                                                                         | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <dt>**\_índice de cores GL \_**</dt> </dl>             | Cada elemento é um único valor, um índice de cores. Ele é convertido em um ponto fixo (com um número não especificado de 0 bits à direita do ponto binário), deslocado para a esquerda ou para a direita, dependendo do valor e do sinal de \_ mudança de índice GL \_ , e adicionado ao \_ deslocamento de índice GL \_ (consulte [**glPixelTransfer**](glpixeltransfer.md)). O índice resultante é convertido em um conjunto de componentes de cor usando o \_ mapa de pixel GL \_ \_ i \_ para \_ R, o GL \_ pixel \_ map \_ i \_ para \_ G, GL \_ pixel \_ map \_ i \_ para \_ B e GL \_ pixel \_ MAP i \_ \_ para \_ tabelas e clamped para o intervalo \[ 0, 1 \] .<br/> |
| <span id="GL_RED"></span><span id="gl_red"></span><dl> <dt>**GL \_ vermelho**</dt> </dl>                                      | Cada elemento é um único componente vermelho. Ele é convertido em ponto flutuante e montado em um elemento RGBA anexando 0,0 para verde e azul e 1,0 para alfa. Em seguida, cada componente é multiplicado pela escala de c de fator de escala GL \_ \_ com assinatura, adicionado à diferença de c de tendência assinada \_ \_ e clamped ao intervalo de \[ 0, 1 \] (consulte **glPixelTransfer**).<br/>                                                                                                                                                                                               |
| <span id="GL_GREEN"></span><span id="gl_green"></span><dl> <dt>**GL \_ verde**</dt> </dl>                                | Cada elemento é um único componente verde. Ele é convertido em ponto flutuante e montado em um elemento RGBA anexando 0,0 para vermelho e azul e 1,0 para alfa. Em seguida, cada componente é multiplicado pela escala de c de fator de escala GL \_ \_ com assinatura, adicionado à diferença de c de tendência assinada \_ \_ e clamped ao intervalo de \[ 0, 1 \] (consulte [**glPixelTransfer**](glpixeltransfer.md)).<br/>                                                                                                                                                                        |
| <span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <dt>**\_azul GL**</dt> </dl>                                   | Cada elemento é um único componente azul. Ele é convertido em ponto flutuante e montado em um elemento RGBA anexando 0,0 para vermelho e verde e 1,0 para alfa. Em seguida, cada componente é multiplicado pela escala de c de fator de escala GL \_ \_ com assinatura, adicionado à diferença de c de tendência assinada \_ \_ e clamped ao intervalo de \[ 0, 1 \] (consulte **glPixelTransfer**).<br/>                                                                                                                                                                                               |
| <span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <dt>**GL \_ alfa**</dt> </dl>                                | Cada elemento é um único componente vermelho. Ele é convertido em ponto flutuante e montado em um elemento RGBA anexando 0,0 para vermelho, verde e azul. Em seguida, cada componente é multiplicado pela escala de c de fator de escala GL \_ \_ com assinatura, adicionado à diferença de c de tendência assinada \_ \_ e clamped ao intervalo de \[ 0, 1 \] (consulte [**glPixelTransfer**](glpixeltransfer.md)).<br/>                                                                                                                                                                                     |
| <span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <dt>**GL em \_ RGB**</dt> </dl>                                      | Cada elemento é um triplo RGB. Ele é convertido em ponto flutuante e montado em um elemento RGBA anexando 1,0 para alfa. Em seguida, cada componente é multiplicado pela escala de c de fator de escala GL \_ \_ com assinatura, adicionado à diferença de c de tendência assinada \_ \_ e clamped ao intervalo de \[ 0, 1 \] (consulte **glPixelTransfer**).<br/>                                                                                                                                                                                                                                    |
| <span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <dt>**Se \_ RGBA**</dt> </dl>                                   | Cada elemento é um elemento RGBA completo. Ele é convertido em ponto flutuante. Em seguida, cada componente é multiplicado pela escala de c de fator de escala GL \_ \_ com assinatura, adicionado à diferença de c de tendência assinada \_ \_ e clamped ao intervalo de \[ 0, 1 \] (consulte [**glPixelTransfer**](glpixeltransfer.md)).<br/>                                                                                                                                                                                                                                                                 |
| <span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <dt>**\_BGR \_ ext. GL**</dt> </dl>                         | Cada pixel é um grupo de três componentes nesta ordem: azul, verde e vermelho.<br/> GL \_ BGR \_ ext fornece um formato que corresponde ao layout de memória dos bitmaps independentes de dispositivo do Windows (DIBs). Assim, seus aplicativos podem usar os mesmos dados com chamadas de função do Windows e chamadas de função de pixel OpenGL.<br/>                                                                                                                                                                                                                                     |
| <span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <dt>**\_BGRA \_ ext. GL**</dt> </dl>                      | Cada pixel é um grupo de quatro componentes nesta ordem: azul, verde, vermelho, alfa. GL \_ BGRA \_ ext fornece um formato que corresponde ao layout de memória dos bitmaps independentes de dispositivo do Windows (DIBs). Assim, seus aplicativos podem usar os mesmos dados com chamadas de função do Windows e chamadas de função de pixel OpenGL.<br/>                                                                                                                                                                                                                                         |
| <span id="GL_LUMINANCE"></span><span id="gl_luminance"></span><dl> <dt>**\_luminância GL**</dt> </dl>                    | Cada elemento é um único valor de luminância. Ele é convertido em ponto flutuante e, em seguida, montado em um elemento RGBA replicando o valor de luminância três vezes para vermelho, verde e azul e anexando 1,0 para alfa. Em seguida, cada componente é multiplicado pela escala de c de fator de escala GL \_ \_ com assinatura, adicionado à diferença de c de tendência assinada \_ \_ e clamped ao intervalo de \[ 0, 1 \] (consulte **glPixelTransfer**).<br/>                                                                                                                                         |
| <span id="GL_LUMINANCE_ALPHA"></span><span id="gl_luminance_alpha"></span><dl> <dt>**luminância do GL \_ \_ alfa**</dt> </dl> | Cada elemento é um par de luminância/alfa. Ele é convertido em ponto flutuante e, em seguida, montado em um elemento RGBA replicando o valor de luminância três vezes para vermelho, verde e azul. Em seguida, cada componente é multiplicado pela escala de c de fator de escala GL \_ \_ com assinatura, adicionado à diferença de c de tendência assinada \_ \_ e clamped ao intervalo de \[ 0, 1 \] (consulte [**glPixelTransfer**](glpixeltransfer.md)).<br/>                                                                                                                                                 |



 

</dd> <dt>

*tipo* 
</dt> <dd>

O tipo de dados dos dados de pixel. Os seguintes valores simbólicos são aceitos: GL \_ não assinado \_ byte, GL byte, renomear \_ \_ bitmap, GL \_ não assinado \_ curto, GL \_ curto, GL \_ não assinado \_ int, GL \_ int e GL \_ float.

</dd> <dt>

*pixels* 
</dt> <dd>

Um ponteiro para os dados da imagem na memória.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | o *destino* não era um GL de \_ textura \_ 2D.<br/>                                                                                                                                                                                |
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | o *formato* não era uma constante de *formato* aceito. Somente as constantes de formato diferentes do \_ índice de estêncil GL e do \_ \_ componente de profundidade GL \_ são aceitas. Consulte a descrição do parâmetro do *formato* para obter uma lista de valores possíveis.<br/> |
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | o *tipo* não era uma constante de *tipo* .<br/>                                                                                                                                                                                   |
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | o *tipo* was \_ bitmap GL e *Format* não era um índice de \_ cores GL \_ .<br/>                                                                                                                                                        |
| <dl> <dt>**\_valor inválido do GL \_**</dt> </dl>     | o *nível* era menor que zero ou maior que log2 *Max*, em que *Max* era o valor RETORNADO de \_ tamanho de textura Max GL \_ \_ .<br/>                                                                                                |
| <dl> <dt>**\_valor inválido do GL \_**</dt> </dl>     | *internalformat* não era 1, 2, 3 ou 4.<br/>                                                                                                                                                                         |
| <dl> <dt>**\_valor inválido do GL \_**</dt> </dl>     | a *largura* ou a altura era menor que zero ou maior que 2 + GL \_ tamanho máximo de \_ textura \_ ou não pôde ser representada como 2 *n* + 2 (borda) para algum valor inteiro de *n*.<br/>                                                  |
| <dl> <dt>**\_valor inválido do GL \_**</dt> </dl>     | a *borda* não era 0 ou 1.<br/>                                                                                                                                                                                            |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/>                                                                                          |



## <a name="remarks"></a>Comentários

A função **glTexImage2D** especifica uma imagem de textura bidimensional. Texturing mapeia uma parte de uma *imagem de textura* especificada em cada primitiva gráfica para a qual texturing está habilitado. O texturing bidimensional é habilitado e desabilitado usando [**glEnable**](glenable.md) e **glDisable** com a textura do argumento GL \_ \_ 2D.

As imagens de textura são definidas com **glTexImage2D**. Os argumentos descrevem os parâmetros da imagem de textura, como altura, largura, largura da borda, número de nível de detalhe (consulte [**glTexParameter**](gltexparameter-functions.md)) e número de componentes de cores fornecidos. Os três últimos argumentos descrevem a maneira como a imagem é representada na memória. Esses argumentos são idênticos aos formatos de pixel usados para [**glDrawPixels**](gldrawpixels.md).

Os dados são lidos de *pixels* como uma sequência de bytes assinados ou sem sinal, curto ou longo ou valores de ponto flutuante de precisão única, dependendo do *tipo*. Esses valores são agrupados em conjuntos de um, dois, três ou quatro valores, dependendo do *formato*, para elementos de formulário. Se o *tipo* for \_ um bitmap GL, os dados serão considerados como uma cadeia de caracteres de bytes não assinados (e o *formato* deverá ser o índice de \_ cores GL \_ ). Cada byte de dados é tratado como elementos de 8 1 bits, com ordenação de bits determinada pelo GL \_ Unpack \_ LSB \_ First (consulte [**glPixelStore**](glpixelstore-functions.md)). Consulte [**glDrawPixels**](gldrawpixels.md) para obter uma descrição dos valores aceitáveis para o parâmetro de *tipo* .

Uma imagem de textura pode ter até quatro componentes por elemento de textura, dependendo dos *componentes*. Uma imagem de textura de um componente usa apenas o componente vermelho da cor RGBA extraída de *pixels*. Uma imagem de dois componentes usa o R e valores. Uma imagem de três componentes usa os valores R, G e B. Uma imagem de quatro componentes usa todos os componentes RGBA.

Texturing não tem efeito no modo de índice de cor.

A imagem de textura pode ser representada pelos mesmos formatos de dados que os pixels em um comando **glDrawPixels** , exceto que o \_ índice de estêncil GL e o componente de \_ \_ profundidade GL \_ não podem ser usados. Os modos [**glPixelStore**](glpixelstore-functions.md) e [**glPixelTransfer**](glpixeltransfer.md) afetam as imagens de textura exatamente como elas afetam o **glDrawPixels**.

Uma imagem de textura com altura ou largura zero indica a textura nula. Se a textura nula for especificada para o nível de detalhe 0, ela será como se texturing estivesse desabilitada.

As funções a seguir recuperam informações relacionadas ao **glTexImage2D**:

[**glGetTexImage**](glgetteximage.md)

[**glIsEnabled**](glisenabled.md) com a textura do argumento GL \_ \_ 2D

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glFog**](glfog.md)
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

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





