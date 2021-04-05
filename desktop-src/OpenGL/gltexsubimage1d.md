---
title: função glTexSubImage1D (GL. h)
description: A função glTexSubImage1D especifica uma parte de uma imagem de textura unidimensional existente. Você não pode definir uma nova textura com glTexSubImage1D.
ms.assetid: e5fcb1a3-96f8-47a6-a9a7-0061faaaa6ac
keywords:
- função glTexSubImage1D OpenGL
topic_type:
- apiref
api_name:
- glTexSubImage1D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfe5510221b738a81f428f9e982a2f9bb2c23588
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644433"
---
# <a name="gltexsubimage1d-function"></a>função glTexSubImage1D

A função **glTexSubImage1D** especifica uma parte de uma imagem de textura unidimensional existente. Você não pode definir uma nova textura com **glTexSubImage1D**.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glTexSubImage1D(
         GLenum  target,
         GLint   level,
         GLint   xoffset,
         GLsizei width,
         GLenum  format,
         GLenum  type,
   const GLvoid  *pixels
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*destino* 
</dt> <dd>

A textura de destino. Deve ser GL \_ Texture \_ 1D.

</dd> <dt>

*level* 
</dt> <dd>

O número de nível de detalhe. Nível 0 é a imagem base. O nível *n* é a imagem de redução *n* º mipmap.

</dd> <dt>

*xoffset* 
</dt> <dd>

Um deslocamento de Texel na direção *x* dentro da matriz de textura.

</dd> <dt>

*width* 
</dt> <dd>

A largura da subimagem de textura.

</dd> <dt>

*format* 
</dt> <dd>

O formato dos dados de pixel. Esse parâmetro pode assumir um dos seguintes valores simbólicos.



| Valor                                                                                                                                                                         | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <dt>**\_índice de cores GL \_**</dt> </dl>             | Cada elemento é um único valor, um índice de cores. Ele é convertido em formato de ponto fixo (com um número não especificado de 0 bits à direita do ponto binário), deslocado para a esquerda ou para a direita, dependendo do valor e do sinal de \_ mudança de índice GL \_ e adicionado ao \_ deslocamento de índice GL \_ (consulte [**glPixelTransfer**](glpixeltransfer.md)). O índice resultante é convertido em um conjunto de componentes de cor usando o \_ mapa de pixel GL \_ \_ i \_ para \_ R, o GL \_ pixel \_ map \_ i \_ para \_ G, GL \_ pixel \_ map \_ i \_ para \_ B e GL \_ pixel \_ MAP i \_ \_ para \_ tabelas e clamped para o intervalo \[ 0, 1 \] .<br/> |
| <span id="GL_RED"></span><span id="gl_red"></span><dl> <dt>**GL \_ vermelho**</dt> </dl>                                      | Cada elemento é um único componente vermelho. Ele é convertido em formato de ponto flutuante e montado em um elemento RGBA anexando 0,0 para verde e azul e 1,0 para alfa. Em seguida, cada componente é multiplicado pela escala de c de fator de escala GL \_ \_ com assinatura, adicionado à diferença de c de tendência assinada \_ \_ e clamped ao intervalo de \[ 0, 1 \] (consulte **glPixelTransfer**).<br/>                                                                                                                                                                                                |
| <span id="GL_GREEN"></span><span id="gl_green"></span><dl> <dt>**GL \_ verde**</dt> </dl>                                | Cada elemento é um único componente verde. Ele é convertido em formato de ponto flutuante e montado em um elemento RGBA anexando 0,0 para vermelho e azul e 1,0 para alfa. Em seguida, cada componente é multiplicado pela escala de c de fator de escala GL \_ \_ com assinatura, adicionado à diferença de c de tendência assinada \_ \_ e clamped ao intervalo de \[ 0, 1 \] (consulte [**glPixelTransfer**](glpixeltransfer.md)).<br/>                                                                                                                                                                         |
| <span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <dt>**\_azul GL**</dt> </dl>                                   | Cada elemento é um único componente azul. Ele é convertido em formato de ponto flutuante e montado em um elemento RGBA anexando 0,0 para vermelho e verde e 1,0 para alfa. Em seguida, cada componente é multiplicado pela escala de c de fator de escala GL \_ \_ com assinatura, adicionado à diferença de c de tendência assinada \_ \_ e clamped ao intervalo de \[ 0, 1 \] (consulte **glPixelTransfer**).<br/>                                                                                                                                                                                                |
| <span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <dt>**GL \_ alfa**</dt> </dl>                                | Cada elemento é um único componente alfa. Ele é convertido em formato de ponto flutuante e montado em um elemento RGBA anexando 0,0 para vermelho, verde e azul. Em seguida, cada componente é multiplicado pela escala de c de fator de escala GL \_ \_ com assinatura, adicionado à diferença de c de tendência assinada \_ \_ e clamped ao intervalo de \[ 0, 1 \] (consulte [**glPixelTransfer**](glpixeltransfer.md)).<br/>                                                                                                                                                                                    |
| <span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <dt>**GL em \_ RGB**</dt> </dl>                                      | Cada elemento é um triplo RGB. Ele é convertido em ponto flutuante e montado em um elemento RGBA anexando 1,0 para alfa. Em seguida, cada componente é multiplicado pela escala de c de fator de escala GL \_ \_ com assinatura, adicionado à diferença de c de tendência assinada \_ \_ e clamped ao intervalo de \[ 0, 1 \] (consulte **glPixelTransfer**).<br/>                                                                                                                                                                                                                                            |
| <span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <dt>**Se \_ RGBA**</dt> </dl>                                   | Cada elemento é um elemento RGBA completo. Ele é convertido em formato de ponto flutuante. Em seguida, cada componente é multiplicado pela escala de c de fator de escala GL \_ \_ com assinatura, adicionado à diferença de c de tendência assinada \_ \_ e clamped ao intervalo de \[ 0, 1 \] (consulte **glPixelTransfer**).<br/>                                                                                                                                                                                                                                                                                         |
| <span id="GL_LUMINANCE"></span><span id="gl_luminance"></span><dl> <dt>**\_luminância GL**</dt> </dl>                    | Cada elemento é um único valor de luminância. Ele é convertido em formato de ponto flutuante e, em seguida, montado em um elemento RGBA replicando o valor de luminância três vezes para vermelho, verde e azul e anexando 1,0 para alfa. Em seguida, cada componente é multiplicado pela escala de c de fator de escala GL \_ \_ com assinatura, adicionado à diferença de c de tendência assinada \_ \_ e clamped ao intervalo de \[ 0, 1 \] (consulte [**glPixelTransfer**](glpixeltransfer.md)).<br/>                                                                                                                   |
| <span id="GL_LUMINANCE_ALPHA"></span><span id="gl_luminance_alpha"></span><dl> <dt>**luminância do GL \_ \_ alfa**</dt> </dl> | Cada elemento é um par de luminância/alfa. Ele é convertido em formato de ponto flutuante e, em seguida, montado em um elemento RGBA replicando o valor de luminância três vezes para vermelho, verde e azul. Em seguida, cada componente é multiplicado pela escala de c de fator de escala GL \_ \_ com assinatura, adicionado à diferença de c de tendência assinada \_ \_ e clamped ao intervalo de \[ 0, 1 \] (consulte **glPixelTransfer**).<br/>                                                                                                                                                                         |



 

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



| Nome                                                                                                  | Significado                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | o *destino* não era GL \_ Texture \_ 1D.<br/>                                                                                                                                                                                                                             |
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | o *formato* não era uma constante aceita.<br/>                                                                                                                                                                                                                        |
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | o *tipo* não era uma constante aceita.<br/>                                                                                                                                                                                                                          |
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | o *tipo* was \_ bitmap GL e *Format* não era um índice de \_ cores GL \_ .<br/>                                                                                                                                                                                                  |
| <dl> <dt>**\_valor inválido do GL \_**</dt> </dl>     | o *nível* era menor que zero ou maior que log2 *Max*, em que *Max* era o valor RETORNADO de \_ tamanho de textura Max GL \_ \_ .<br/>                                                                                                                                          |
| <dl> <dt>**\_valor inválido do GL \_**</dt> </dl>     | *xoffset* era menor que *b*, ou   +  a *largura* de deslocamento era maior que *WB*, em que *w* é a largura de \_ textura GL \_ , e *b* é a largura da borda de \_ textura GL \_ da imagem de textura que está sendo modificada.<br/> Observe que *w* inclui duas vezes a largura da borda.<br/> |
| <dl> <dt>**\_valor inválido do GL \_**</dt> </dl>     | a *largura* era menor que *b*, onde *b* é a largura da borda da matriz de textura.<br/>                                                                                                                                                                            |
| <dl> <dt>**\_valor inválido do GL \_**</dt> </dl>     | a *borda* não era zero ou 1.<br/>                                                                                                                                                                                                                                   |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A matriz texure não foi definida por uma operação **glTexImage1D** anterior.<br/>                                                                                                                                                                                    |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/>                                                                                                                                    |



## <a name="remarks"></a>Comentários

Um texturing unidimensional para um primitivo é habilitado usando [**glEnable**](glenable.md) e **glDisable** com o argumento GL \_ Texture \_ 1D. Durante a texturing, parte de uma imagem de textura especificada é mapeada em cada primitiva habilitada. Use a função **glTexSubImage1D** para especificar uma subimagem contígua de uma imagem de textura unidimensional existente para texturing.

O texels referenciado por *pixels* substitui uma região da matriz de textura existente por índices *x* de *xoffset* e *xoffset* + (*largura* 1), inclusive. Essa região não pode incluir nenhum texels fora do intervalo da matriz de textura especificada originalmente.

A especificação de uma subimagem com uma *largura* igual a zero não tem nenhum efeito e não gera um erro.

Texturing não tem efeito no modo de índice de cor.

Em geral, as imagens de textura podem ser representadas pelos mesmos formatos de dados que os pixels em um comando [**glDrawPixels**](gldrawpixels.md) , exceto que o \_ índice de estêncil GL e o componente de \_ \_ profundidade GL \_ não podem ser usados. Os modos [**glPixelStore**](glpixelstore-functions.md) e [**glPixelTransfer**](glpixeltransfer.md) afetam as imagens de textura exatamente como elas afetam o **glDrawPixels**.

As funções a seguir recuperam informações relacionadas ao **glTexSubImage1D**:

[**glGetTexImage**](glgetteximage.md)

[**glIsEnabled**](glisenabled.md) com a textura do argumento GL \_ \_ 1D

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

[**glEnable**](glenable.md)
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

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> <dt>

[**glTexSubImage2D**](gltexsubimage2d.md)
</dt> </dl>

 

 





