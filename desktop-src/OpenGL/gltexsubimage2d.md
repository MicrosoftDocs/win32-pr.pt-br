---
title: Função glTexSubImage2D (Gl.h)
description: A função glTexSubImage2D especifica uma parte de uma imagem de textura unidimensional existente. Não é possível definir uma nova textura com glTexSubImage2D.
ms.assetid: 2b6cb663-8e1d-4270-b8ba-5a8b43a2ece7
keywords:
- Função GlTexSubImage2D OpenGL
topic_type:
- apiref
api_name:
- glTexSubImage2D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c568afbe63ab01bd2866f180f968ea80101fec2ff22062707f4929d662ea47ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519696"
---
# <a name="gltexsubimage2d-function"></a>Função glTexSubImage2D

A **função glTexSubImage2D** especifica uma parte de uma imagem de textura unidimensional existente. Não é possível definir uma nova textura com **glTexSubImage2D.**

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glTexSubImage2D(
         GLenum  target,
         GLint   level,
         GLint   xoffset,
         GLint   yoffset,
         GLsizei width,
         GLsizei height,
         GLenum  format,
         GLenum  type,
   const GLvoid  *pixels
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*destino* 
</dt> <dd>

A textura de destino. Deve ser GL \_ TEXTURE \_ 2D.

</dd> <dt>

*level* 
</dt> <dd>

O número de nível de detalhes. Nível 0 é a imagem base. O *nível n* é a n *imagem* de redução de mipmap.

</dd> <dt>

*xoffset* 
</dt> <dd>

Um deslocamento de texel na direção *x* dentro da matriz de textura.

</dd> <dt>

*yoffset* 
</dt> <dd>

Um deslocamento de texel na direção *y* dentro da matriz de textura.

</dd> <dt>

*width* 
</dt> <dd>

A largura da subimagem de textura.

</dd> <dt>

*altura* 
</dt> <dd>

A altura da subimagem de textura.

</dd> <dt>

*format* 
</dt> <dd>

O formato dos dados de pixel. Ele pode assumir um dos seguintes valores simbólicos.



| Valor                                                                                                                                                                         | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_INDEX"></span><span id="gl_color_index"></span><dl> <dt>**GL \_ COLOR \_ INDEX**</dt> </dl>             | Cada elemento é um único valor, um índice de cores. Ele é convertido em formato de ponto fixo (com um número não especificado de 0 bits à direita do ponto binário), deslocado para a esquerda ou para a direita, dependendo do valor e do sinal de GL INDEX SHIFT e adicionado a \_ \_ GL INDEX OFFSET \_ \_ (consulte [**glPixelTransfer**](glpixeltransfer.md)). O índice resultante é convertido em um conjunto de componentes de cores usando o GL PIXEL MAP I TO R, GL PIXEL MAP I TO G, GL PIXEL MAP I TO B e GL PIXEL MAP I para tabelas A e fixados no intervalo \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \[ 0,1 \] .<br/> |
| <span id="GL_RED"></span><span id="gl_red"></span><dl> <dt>**GL \_ RED**</dt> </dl>                                      | Cada elemento é um único componente vermelho. Ele é convertido em formato de ponto flutuante e montado em um elemento RGBA anexando 0,0 para verde e azul e 1,0 para alfa. Cada componente é multiplicado pelo fator de escala assinado GL c SCALE, adicionado ao desvio assinado GL c BIAS e fixado ao intervalo \_ \_ \_ \_ \[ 0,1 \] (consulte **glPixelTransfer**).<br/>                                                                                                                                                                                                |
| <span id="GL_GREEN"></span><span id="gl_green"></span><dl> <dt>**GL \_ GREEN**</dt> </dl>                                | Cada elemento é um único componente verde. Ele é convertido em formato de ponto flutuante e montado em um elemento RGBA anexando 0,0 para vermelho e azul e 1,0 para alfa. Cada componente é multiplicado pelo fator de escala assinado GL c SCALE, adicionado ao desvio assinado GL c BIAS e fixado ao intervalo \_ \_ \_ \_ \[ 0,1 \] (consulte [**glPixelTransfer**](glpixeltransfer.md)).<br/>                                                                                                                                                                         |
| <span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <dt>**GL \_ BLUE**</dt> </dl>                                   | Cada elemento é um único componente azul. Ele é convertido em formato de ponto flutuante e montado em um elemento RGBA anexando 0,0 para vermelho e verde e 1,0 para alfa. Cada componente é multiplicado pelo fator de escala assinado GL c SCALE, adicionado ao desvio assinado GL c BIAS e fixado ao intervalo \_ \_ \_ \_ \[ 0,1 \] (consulte **glPixelTransfer**).<br/>                                                                                                                                                                                                |
| <span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <dt>**GL \_ ALPHA**</dt> </dl>                                | Cada elemento é um único componente alfa. Ele é convertido em formato de ponto flutuante e montado em um elemento RGBA anexando 0,0 para vermelho, verde e azul. Cada componente é multiplicado pelo fator de escala assinado GL c SCALE, adicionado ao desvio assinado GL c BIAS e fixado ao intervalo \_ \_ \_ \_ \[ 0,1 \] (consulte [**glPixelTransfer**](glpixeltransfer.md)).<br/>                                                                                                                                                                                    |
| <span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <dt>**GL \_ RGB**</dt> </dl>                                      | Cada elemento é um triplo RGB. Ele é convertido em formato de ponto flutuante e montado em um elemento RGBA anexando 1.0 para alfa. Cada componente é multiplicado pelo fator de escala assinado GL c SCALE, adicionado ao desvio assinado GL c BIAS e fixado ao intervalo \_ \_ \_ \_ \[ 0,1 \] (consulte **glPixelTransfer**).<br/>                                                                                                                                                                                                                                     |
| <span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <dt>**GL \_ RGBA**</dt> </dl>                                   | Cada elemento é um elemento RGBA completo. Ele é convertido em ponto flutuante. Cada componente é multiplicado pelo fator de escala assinado GL c SCALE, adicionado ao desvio assinado GL c BIAS e fixado ao intervalo \_ \_ \_ \_ \[ 0,1 \] (consulte **glPixelTransfer**).<br/>                                                                                                                                                                                                                                                                                                |
| <span id="GL_LUMINANCE"></span><span id="gl_luminance"></span><dl> <dt>**GL \_ LUMINANCE**</dt> </dl>                    | Cada elemento é um único valor de luminância. Ele é convertido em formato de ponto flutuante e, em seguida, montado em um elemento RGBA replicando o valor de luminância três vezes para vermelho, verde e azul e anexando 1,0 para alfa. Cada componente é multiplicado pelo fator de escala assinado GL c SCALE, adicionado ao desvio assinado GL c BIAS e fixado ao intervalo \_ \_ \_ \_ \[ 0,1 \] (consulte [**glPixelTransfer**](glpixeltransfer.md)).<br/>                                                                                                                   |
| <span id="GL_LUMINANCE_ALPHA"></span><span id="gl_luminance_alpha"></span><dl> <dt>**GL \_ LUMINANCE \_ ALPHA**</dt> </dl> | Cada elemento é um par de luminância/alfa. Ele é convertido em formato de ponto flutuante e, em seguida, montado em um elemento RGBA replicando o valor de luminância três vezes para vermelho, verde e azul. Cada componente é multiplicado pelo fator de escala assinado GL c SCALE, adicionado ao desvio assinado GL c BIAS e fixado ao intervalo \_ \_ \_ \_ \[ 0,1 \] (consulte **glPixelTransfer**).<br/>                                                                                                                                                                         |



 

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



| Nome                                                                                                  | Significado                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *target* não era GL \_ TEXTURE \_ 2D.<br/>                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *format* não era uma constante aceita.<br/>                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *type* não era uma constante aceita.<br/>                                                                                                                                                                                                                                                                                                                                                              |
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *O tipo* era GL \_ BITMAP *e o formato* não era GL \_ COLOR \_ INDEX.<br/>                                                                                                                                                                                                                                                                                                                                      |
| <dl> <dt>**VALOR INVÁLIDO DE GL \_ \_**</dt> </dl>     | *level* era menor que zero ou maior que log2 *max*, em que *max* era o valor retornado de GL \_ MAX TEXTURE \_ \_ SIZE.<br/>                                                                                                                                                                                                                                                                              |
| <dl> <dt>**VALOR INVÁLIDO DE GL \_ \_**</dt> </dl>     | *xoffset* era menor que -*b*; ou a largura *xoffset* era maior que w b ; ou  +     -   *yoffset* era menor que - b ; ou a altura do *yoffset*  +     -    \_ \_  \_ \_  era \_ \_ maior que h b , em que w é a LARGURA DE TEXTURA GL, h é a ALTURA DA TEXTURA GL e b é a largura da BORDA DE TEXTURA GL da imagem de textura que está sendo modificada. <br/> Observe que *w* e *h incluem* duas vezes a largura da borda.<br/> |
| <dl> <dt>**VALOR INVÁLIDO DE GL \_ \_**</dt> </dl>     | *width* era menor que *b*, em *que b* é a largura da borda da matriz de textura.<br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>**VALOR INVÁLIDO DE GL \_ \_**</dt> </dl>     | *border* não era zero ou 1.<br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | A matriz de textura não foi definida por uma **operação glTexImage2D** anterior.<br/>                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd.**](glend.md)<br/>                                                                                                                                                                                                                                                                        |



## <a name="remarks"></a>Comentários

A texturagem bidimensional para um primitivo é habilitada usando [**glEnable**](glenable.md) e **glDisable** com o argumento GL \_ TEXTURE \_ 2D. Durante a texturagem, parte de uma imagem de textura especificada é mapeada em cada primitivo habilitado. Use a função **glTexSubImage2D** para especificar uma subimagem contígua de uma imagem de textura bidimensional existente para texturing.

O texels referenciado por *pixels* substitui uma região da matriz de textura existente por índices *x* de *xoffset* e *xoffset* +*(largura* 1) índices inclusivos e *y* de *yoffset* e *yoffset* + (*altura* 1), inclusive. Essa região não pode incluir nenhum texels fora do intervalo da matriz de textura especificada originalmente.

A especificação de uma subimagem com uma *largura* igual a zero não tem nenhum efeito e não gera um erro.

Texturing não tem efeito no modo de índice de cor.

Em geral, as imagens de textura podem ser representadas pelos mesmos formatos de dados que os pixels em um comando [**glDrawPixels**](gldrawpixels.md) , exceto que o \_ índice de estêncil GL e o componente de \_ \_ profundidade GL \_ não podem ser usados. Os modos [**glPixelStore**](glpixelstore-functions.md) e [**glPixelTransfer**](glpixeltransfer.md) afetam as imagens de textura exatamente como elas afetam o **glDrawPixels**.

As funções a seguir recuperam informações relacionadas ao **glTexSubImage2D**:

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

[**glTexSubImage1D**](gltexsubimage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





