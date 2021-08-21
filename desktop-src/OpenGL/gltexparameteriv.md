---
title: Função glTexParameteriv (Gl.h)
description: Define parâmetros de textura. | Função glTexParameteriv (Gl.h)
ms.assetid: c6381ee5-5323-4e11-9c32-bc70f25f8f4e
keywords:
- Função glTexParameterfv OpenGL
topic_type:
- apiref
api_name:
- glTexParameterfv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40df39c0d95d5719b0e066a1fadc089212619ecabf7868400e246001b69f579b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119490036"
---
# <a name="gltexparameteriv-function"></a>Função glTexParameteriv

Define parâmetros de textura.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glTexParameterfv(
         GLenum target,
         GLenum pname,
   const GLint  *params
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*destino* 
</dt> <dd>

A textura de destino, que deve ser GL \_ TEXTURE \_ 1D ou GL \_ TEXTURE \_ 2D.

</dd> <dt>

*Pname* 
</dt> <dd>

O nome simbólico de um único parâmetro de textura com valor. Os símbolos a seguir são aceitos em *pname*.



| Valor                                                                                                                                                                                         | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span><dl> <dt>**FILTRO MIN \_ \_ DE TEXTURA \_ GL**</dt> </dl>       | A função de mineração de textura é usada sempre que o pixel que está sendo texturado é mapeado para uma área maior que um elemento de textura. Há seis funções de mineração definidas. Dois deles usam um ou quatro elementos de textura mais próximos para calcular o valor da textura. Os outros quatro usam mipmaps. <br/> Um mipmap é um conjunto ordenado de matrizes que representam a mesma imagem em resoluções progressivamente inferiores. Se a textura tiver dimensões de 2nx2<sup>m,</sup> haverá max(n, m) + 1 mipmaps. O primeiro mipmap é a textura original, com dimensões de 2nx2<sup>m.</sup> Cada mipmap subsequente tem dimensões 2<sup>k</sup>1x2<sup>l</sup>1, em que 2<sup>k</sup>x2<sup>l</sup> são as dimensões do mipmap anterior, até k = 0 ou l = 0. Nesse ponto, os mipmaps subsequentes têm a dimensão 1x2<sup>l</sup>1 ou 2<sup>k</sup>1x1 até o mipmap final, que tem a dimensão 1x1. Os Mipmaps são definidos usando [**glTexImage1D**](glteximage1d.md) ou [**glTexImage2D**](glteximage2d.md) com o argumento de nível de detalhes que indica a ordem dos mipmaps. Nível 0 é a textura original; level bold max(n, m) é o mipmap 1x1 final.<br/> |
| <span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span><dl> <dt>**FILTRO GL \_ TEXTURE \_ MAG \_**</dt> </dl>       | A função de ampliação de textura é usada quando o pixel que está sendo texturado é mapeado para uma área menor ou igual a um elemento de textura. Ele define a função de ampliação de textura como GL \_ NEAREST ou GL \_ LINEAR.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="GL_TEXTURE_WRAP_S"></span><span id="gl_texture_wrap_s"></span><dl> <dt>**GL \_ TEXTURE \_ WRAP \_ S**</dt> </dl>                   | Define o parâmetro wrap para as coordenadas de textura como GL \_ TEXTURE ou GL \_ REPEAT. GL CLAMP faz com que as coordenadas sejam fixadas ao intervalo \_ \[ 0,1 e é útil para evitar o quebra-quebra de artefatos ao mapear uma única imagem para \] um objeto . GL \_ REPEAT faz com que a parte inteira da coordenada s seja ignorada; O OpenGL usa apenas a parte fracionada, criando assim um padrão de repetição. Os elementos de textura da borda serão acessados somente se o empacotamento estiver definido como GL \_ FIX. Inicialmente, GL \_ TEXTURE WRAP S é definido como GL \_ \_ \_ REPEAT.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_TEXTURE_WRAP_T"></span><span id="gl_texture_wrap_t"></span><dl> <dt>**GL \_ TEXTURE \_ WRAP \_ T**</dt> </dl>                   | Define o parâmetro wrap para a coordenada de textura t como GL \_ CLAMP ou GL \_ REPEAT. Confira a discussão em GL \_ TEXTURE \_ WRAP \_ S. Inicialmente, GL \_ TEXTURE WRAP T é definido como GL \_ \_ \_ REPEAT.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span><dl> <dt>**COR DA \_ BORDA \_ DA TEXTURA \_ GL**</dt> </dl> | Define uma cor da borda. O *parâmetro params* contém quatro valores que compõem a cor RGBA da borda de textura. Os componentes de cor de inteiro são interpretados linearmente, de modo que o inteiro mais positivo é mapeado para 1,0 e o inteiro mais negativo é mapeado para 1,0. Os valores são fixados no intervalo \[ 0,1 \] quando são especificados. Inicialmente, a cor da borda é (0, 0, 0, 0).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_TEXTURE_PRIORITY"></span><span id="gl_texture_priority"></span><dl> <dt>**PRIORIDADE \_ DE TEXTURA \_ GL**</dt> </dl>              | Especifica a prioridade de residência de textura da textura atualmente vinculada. Os valores permitidos estão no intervalo \[ 0, 1 \] . Consulte [**glPrioritizeTextures**](glprioritizetextures.md) e [**glBindTexture**](glbindtexture.md) para obter mais informações.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

*params* 
</dt> <dd>

Um ponteiro para uma matriz em que o valor ou os valores de pname são armazenados. O parâmetro params fornece uma função para minerar a textura como uma das seguintes.



| Valor                                                                                                                                                                                               | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_NEAREST_"></span><span id="gl_nearest_"></span><dl> <dt>**GL \_ MAIS PRÓXIMO**</dt> </dl>                                             | Retorna o valor do elemento de textura mais próximo (na distância de York) ao centro do pixel que está sendo texturado. <br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_LINEAR"></span><span id="gl_linear"></span><dl> <dt>**GL \_ LINEAR**</dt> </dl>                                                   | Retorna a média ponderada dos quatro elementos de textura mais próximos ao centro do pixel que está sendo texturado. Eles podem incluir elementos de textura de borda, dependendo dos valores de GL TEXTURE WRAP S, GL TEXTURE WRAP T e \_ no mapeamento \_ \_ \_ \_ \_ exato. GL NEAREST geralmente é mais rápido do que GL LINEAR, mas pode produzir imagens texturizada com bordas mais estreitas porque a transição entre elementos de textura \_ \_ não é tão suave. O valor padrão de GL \_ TEXTURE MAG FILTER é GL \_ \_ \_ LINEAR.<br/> |
| <span id="GL_NEAREST_MIPMAP_NEAREST"></span><span id="gl_nearest_mipmap_nearest"></span><dl> <dt>**GL \_ MAIS PRÓXIMO DE \_ MIPMAP \_**</dt> </dl> | Escolhe o mipmap que mais corresponde ao tamanho do pixel que está sendo texturado e usa o critério GL NEAREST (o elemento de textura mais próximo ao centro do pixel) para produzir um valor de \_ textura. <br/>                                                                                                                                                                                                                                                                                              |
| <span id="GL_LINEAR_MIPMAP_NEAREST"></span><span id="gl_linear_mipmap_nearest"></span><dl> <dt>**GL \_ LINEAR \_ MIPMAP \_ MAIS PRÓXIMO**</dt> </dl>    | Escolhe o mipmap que mais corresponde ao tamanho do pixel que está sendo texturado e usa o critério LINEAR GL (uma média ponderada dos quatro elementos de textura mais próximos ao centro do pixel) para produzir um valor de \_ textura. <br/>                                                                                                                                                                                                                                                          |
| <span id="GL_NEAREST_MIPMAP_LINEAR"></span><span id="gl_nearest_mipmap_linear"></span><dl> <dt>**GL \_ NEAREST \_ MIPMAP \_ LINEAR**</dt> </dl>    | Escolhe os dois mipmaps que mais se aproximam do tamanho do pixel que está sendo texturado e usa o critério GL NEAREST (o elemento de textura mais próximo ao centro do pixel) para produzir um valor de textura de cada \_ mipmap. O valor final da textura é uma média ponderada desses dois valores. <br/>                                                                                                                                                                                                       |
| <span id="GL_LINEAR_MIPMAP_LINEAR"></span><span id="gl_linear_mipmap_linear"></span><dl> <dt>**GL \_ LINEAR \_ MIPMAP \_ LINEAR**</dt> </dl>       | Escolhe os dois mipmaps que mais se aproximam do tamanho do pixel que está sendo texturado e usa o critério LINEAR GL (uma média ponderada dos quatro elementos de textura mais próximos ao centro do pixel) para produzir um valor de textura de cada \_ mipmap. O valor final da textura é uma média ponderada desses dois valores.<br/>                                                                                                                                                                    |



 

O *parâmetro params* fornece uma função para ampliar a textura como uma das seguintes.



| Valor                                                                                                                                                   | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_NEAREST_"></span><span id="gl_nearest_"></span><dl> <dt>**GL \_ MAIS PRÓXIMO**</dt> </dl> | Retorna o valor do elemento de textura mais próximo (na distância de York) ao centro do pixel que está sendo texturado. <br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_LINEAR"></span><span id="gl_linear"></span><dl> <dt>**GL \_ LINEAR**</dt> </dl>       | Retorna a média ponderada dos quatro elementos de textura mais próximos ao centro do pixel que está sendo texturado. Eles podem incluir elementos de textura de borda, dependendo dos valores de GL TEXTURE WRAP S, GL TEXTURE WRAP T e \_ no mapeamento \_ \_ \_ \_ \_ exato. GL NEAREST geralmente é mais rápido do que GL LINEAR, mas pode produzir imagens texturizada com bordas mais estreitas porque a transição entre elementos de textura \_ \_ não é tão suave. O valor padrão de GL \_ TEXTURE MAG FILTER é GL \_ \_ \_ LINEAR.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela [**função glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significado                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ \_ENUM INVÁLIDO**</dt> </dl>     | *target* ou *pname* não era um dos valores definidos aceitos ou quando *o param* deveria ter um valor constante definido (com base no valor *de pname*) e não tinha.<br/> |
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd.**](glend.md)<br/>                                            |



## <a name="remarks"></a>Comentários

O mapeamento de textura é uma técnica que aplica uma imagem à superfície de um objeto como se a imagem fosse um decalque ou quebra de célula. A imagem é criada no espaço de textura, com um sistema *de coordenadas*( s , *t*). Uma textura é uma imagem unidimensional ou bidimensional e um conjunto de parâmetros que determinam como as amostras são derivadas da imagem.

A **função glTexParameter** atribui o valor ou valores em parâmetros ao parâmetro de textura especificado como pname. O parâmetro de destino define a textura de destino, GL \_ TEXTURE \_ 1D ou GL \_ TEXTURE \_ 2D.

À medida que mais elementos de textura são amostrados no processo de minificação, menos artefatos de alias serão aparentes. Embora as funções de minificação GL NEAREST e GL LINEAR possam ser mais rápidas do que as outras quatro, elas amostram apenas um ou quatro elementos de textura para determinar o valor de textura do pixel que está sendo renderizado e podem produzir padrões de moire ou transições \_ \_ irregulares. O valor padrão de GL \_ TEXTURE MIN FILTER é GL \_ \_ \_ NEAREST \_ MIPMAP \_ LINEAR.

Suponha que a texturing está habilitada (chamando [**glEnable**](glenable.md) com o argumento GL TEXTURE 1D ou GL TEXTURE 2D) e GL TEXTURE MIN FILTER é definido como uma das funções que exigem \_ \_ um \_ \_ \_ \_ \_ mipmap. Se as dimensões das imagens de textura definidas atualmente (com chamadas anteriores para [**glTexImage1D**](glteximage1d.md) ou [**glTexImage2D)**](glteximage2d.md)não seguirem a sequência adequada para mipmaps ou houver menos imagens de textura definidas do que são necessárias ou se o conjunto de imagens de textura tiver números diferentes de componentes de textura, será como se o mapeamento de textura estivesse desabilitado. A filtragem linear acessa os quatro elementos de textura mais próximos somente em texturas 2D. Em texturas 1D, a filtragem linear acessa os dois elementos de textura mais próximos. A função a seguir recupera informações relacionadas a **glTexParameterf**, **glTexParameteri**, **glTexParameterfv** e **glTexParameteriv**:

[**glGetTexParameter**](glgettexparameter.md)

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

[**glBindTexture**](glbindtexture.md)
</dt> <dt>

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glCopyTexImage1D**](glcopyteximage1d.md)
</dt> <dt>

[**glCopyTexImage2D**](glcopyteximage2d.md)
</dt> <dt>

[**glCopyTexSubImage2D**](glcopytexsubimage2d.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glPixelStore**](glpixelstore-functions.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glPrioritizeTextures**](glprioritizetextures.md)
</dt> <dt>

[glTexEnv](gltexenv-functions.md)
</dt> <dt>

[glTexGen](gltexgen-functions.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexSubImage1D**](gltexsubimage1d.md)
</dt> <dt>

[**glTexSubImage2D**](gltexsubimage2d.md)
</dt> </dl>

 

 





