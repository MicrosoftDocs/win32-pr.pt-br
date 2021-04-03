---
title: função glTexParameteriv (GL. h)
description: Define parâmetros de textura. | função glTexParameteriv (GL. h)
ms.assetid: c6381ee5-5323-4e11-9c32-bc70f25f8f4e
keywords:
- função glTexParameterfv OpenGL
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
ms.openlocfilehash: 315f9b447742cfe40219877bb947c7cc5584a3e7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103930436"
---
# <a name="gltexparameteriv-function"></a>função glTexParameteriv

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

A textura de destino, que deve ser a textura GL \_ \_ 1D ou GL de \_ \_ 2D.

</dd> <dt>

*pname* 
</dt> <dd>

O nome simbólico de um parâmetro de textura de valor único. Os símbolos a seguir são aceitos em *pname*.



| Valor                                                                                                                                                                                         | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span><dl> <dt>**\_filtro de \_ mínimo de textura GL \_**</dt> </dl>       | A função minificar de textura é usada sempre que o pixel que está sendo texturizado é mapeado para uma área maior do que um elemento de textura. Há seis funções minificar definidas. Dois deles usam os elementos de textura mais próximos um ou mais próximo para calcular o valor de textura. Os outros quatro usam mipmaps. <br/> Um mipmap é um conjunto ordenado de matrizes que representam a mesma imagem em resoluções progressivamente inferiores. Se a textura tiver dimensões 2nx2<sup>m</sup> , haverá Max (n, m) + 1 mipmaps. O primeiro mipmap é a textura original, com as dimensões 2nx2<sup>m</sup>. Cada mipmap subsequente tem dimensões 2<sup>k</sup>1x2<sup>l</sup>1, em que 2<sup>k</sup>X2<sup>l</sup> são as dimensões da mipmap anterior, até k = 0 ou l = 0. Nesse ponto, os mipmaps subsequentes têm Dimension 1x2<sup>l</sup>1 ou 2<sup>k</sup>1x1 até o mipmap final, que tem a dimensão 1x1. Mipmaps são definidos usando [**glTexImage1D**](glteximage1d.md) ou [**glTexImage2D**](glteximage2d.md) com o argumento de nível de detalhe que indica a ordem do mipmaps. Nível 0 é a textura original; o nível máximo em negrito (n, m) é o 1x1 final mipmap.<br/> |
| <span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span><dl> <dt>**\_ \_ filtro mag de textura GL \_**</dt> </dl>       | A função de ampliação de textura é usada quando o pixel que está sendo texturizado é mapeado para uma área menor ou igual a um elemento de textura. Ele define a função de ampliação de textura como GL \_ mais próximo ou GL \_ linear.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="GL_TEXTURE_WRAP_S"></span><span id="gl_texture_wrap_s"></span><dl> <dt>**\_S de \_ encapsulamento de textura GL \_**</dt> </dl>                   | Define o parâmetro Wrap para a coordenada de textura s para GL \_ fixe ou GL \_ REPEAT. GL \_ fixe faz com que as coordenadas de s sejam clampeddas para o intervalo de \[ 0, 1 \] e é útil para evitar a quebra de artefatos ao mapear uma única imagem em um objeto. O GL \_ REPEAT faz com que a parte inteira da coordenada s seja ignorada; O OpenGL usa apenas a parte fracionária, criando assim um padrão de repetição. Os elementos de textura de borda serão acessados somente se o encapsulamento estiver definido como GL \_ fixe. Inicialmente, \_ a textura GL \_ encapsula \_ S está definida como GL \_ REPEAT.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_TEXTURE_WRAP_T"></span><span id="gl_texture_wrap_t"></span><dl> <dt>**\_ \_ & encapsulamento de textura GL \_**</dt> </dl>                   | Define o parâmetro Wrap para a coordenada de textura t para GL \_ fixe ou GL \_ REPEAT. Consulte a discussão em GL \_ Texture \_ Wrap \_ S. Inicialmente, o \_ GL \_ de textura de \_ redefinição de codificação T é definido como GL \_ REPEAT.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span><dl> <dt>**\_cor da \_ borda da textura GL \_**</dt> </dl> | Define uma cor de borda. O parâmetro *params* contém quatro valores que compõem a cor RGBA da borda da textura. Os componentes de cor de inteiro são interpretados linearmente de forma que o inteiro mais positivo seja mapeado para 1,0 e o número inteiro mais negativo seja mapeado para 1,0. Os valores são clamped para o intervalo de \[ 0, 1 \] quando são especificados. Inicialmente, a cor da borda é (0, 0, 0, 0).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_TEXTURE_PRIORITY"></span><span id="gl_texture_priority"></span><dl> <dt>**\_prioridade de textura GL \_**</dt> </dl>              | Especifica a prioridade de residência de textura da textura associada no momento. Os valores permitidos estão no intervalo de \[ 0, 1 \] . Consulte [**glPrioritizeTextures**](glprioritizetextures.md) e [**glBindTexture**](glbindtexture.md) para obter mais informações.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

*params* 
</dt> <dd>

Um ponteiro para uma matriz em que o valor ou os valores de pname são armazenados. O parâmetro params fornece uma função para minificar a textura como uma das opções a seguir.



| Valor                                                                                                                                                                                               | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_NEAREST_"></span><span id="gl_nearest_"></span><dl> <dt>**GL \_ Mais próximo**</dt> </dl>                                             | Retorna o valor do elemento Texture que é mais próximo (em Manhattan Distance) para o centro do pixel que está sendo texturizado. <br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_LINEAR"></span><span id="gl_linear"></span><dl> <dt>**GL \_ linear**</dt> </dl>                                                   | Retorna a média ponderada dos quatro elementos de textura mais próximos do centro do pixel que está sendo texturizado. Eles podem incluir elementos de textura de borda, dependendo dos valores de \_ reencapsulamento de textura GL S, GL de textura de retratação \_ \_ \_ \_ \_ e no mapeamento exato. \_O GL mais próximo é geralmente mais rápido que \_ o GL linear, mas pode produzir imagens texturizadas com bordas mais nítidas, pois a transição entre elementos de textura não é tão suave. O valor padrão do \_ filtro mag de textura do GL \_ \_ é GL \_ linear.<br/> |
| <span id="GL_NEAREST_MIPMAP_NEAREST"></span><span id="gl_nearest_mipmap_nearest"></span><dl> <dt>**GL \_ mais próximo \_ MIPMAP \_ mais próximo**</dt> </dl> | Escolhe o mipmap que mais se aproxima do tamanho do pixel que está sendo texturizado e usa o \_ critério mais próximo do GL (o elemento Texture mais próximo ao centro do pixel) para produzir um valor de textura. <br/>                                                                                                                                                                                                                                                                                              |
| <span id="GL_LINEAR_MIPMAP_NEAREST"></span><span id="gl_linear_mipmap_nearest"></span><dl> <dt>**GL \_ linear \_ MIPMAP \_ mais próximo**</dt> </dl>    | Escolhe o mipmap que mais se aproxima do tamanho do pixel que está sendo texturizado e usa o \_ critério linear do GL (uma média ponderada dos quatro elementos de textura mais próximos do centro do pixel) para produzir um valor de textura. <br/>                                                                                                                                                                                                                                                          |
| <span id="GL_NEAREST_MIPMAP_LINEAR"></span><span id="gl_nearest_mipmap_linear"></span><dl> <dt>**GL \_ mais próximo \_ MIPMAP \_ linear**</dt> </dl>    | Escolhe as duas mipmaps que mais se aproximam do tamanho do pixel que está sendo texturizado e usa o \_ critério mais próximo do GL (o elemento Texture mais próximo ao centro do pixel) para produzir um valor de textura de cada mipmap. O valor final da textura é uma média ponderada desses dois valores. <br/>                                                                                                                                                                                                       |
| <span id="GL_LINEAR_MIPMAP_LINEAR"></span><span id="gl_linear_mipmap_linear"></span><dl> <dt>**GL \_ linear \_ MIPMAP \_ linear**</dt> </dl>       | Escolhe as duas mipmaps que mais se aproximam do tamanho do pixel que está sendo texturizado e usa o \_ critério linear do GL (uma média ponderada dos quatro elementos de textura mais próximos do centro do pixel) para produzir um valor de textura de cada mipmap. O valor final da textura é uma média ponderada desses dois valores.<br/>                                                                                                                                                                    |



 

O parâmetro *params* fornece uma função para ampliar a textura como uma das opções a seguir.



| Valor                                                                                                                                                   | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_NEAREST_"></span><span id="gl_nearest_"></span><dl> <dt>**GL \_ Mais próximo**</dt> </dl> | Retorna o valor do elemento Texture que é mais próximo (em Manhattan Distance) para o centro do pixel que está sendo texturizado. <br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_LINEAR"></span><span id="gl_linear"></span><dl> <dt>**GL \_ linear**</dt> </dl>       | Retorna a média ponderada dos quatro elementos de textura mais próximos do centro do pixel que está sendo texturizado. Eles podem incluir elementos de textura de borda, dependendo dos valores de \_ reencapsulamento de textura GL S, GL de textura de retratação \_ \_ \_ \_ \_ e no mapeamento exato. \_O GL mais próximo é geralmente mais rápido que \_ o GL linear, mas pode produzir imagens texturizadas com bordas mais nítidas, pois a transição entre elementos de textura não é tão suave. O valor padrão do \_ filtro mag de textura do GL \_ \_ é GL \_ linear.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ \_Enumeração INválida**</dt> </dl>     | *target* ou *pname* não era um dos valores definidos aceitos, ou quando *param* deveria ter um valor constante definido (com base no valor de *pname*) e não.<br/> |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/>                                            |



## <a name="remarks"></a>Comentários

O mapeamento de textura é uma técnica que aplica uma imagem à superfície de um objeto como se a imagem fosse um Decal ou uma redução de encolhimento de Cellophane. A imagem é criada no espaço de textura, com um sistema de coordenadas (*s*, *t*). Uma textura é uma imagem única ou bidimensional e um conjunto de parâmetros que determinam como os exemplos são derivados da imagem.

A função **glTexParameter** atribui o valor ou valores em params para o parâmetro Texture especificado como pname. O parâmetro de destino define a textura de destino, ou seja, GL \_ textura \_ 1D ou GL de \_ textura \_ 2D.

Como mais elementos de textura são amostrados no processo de minificação, menos artefatos de alias serão aparentes. Embora as \_ \_ funções minificação lineares mais próximas e GL possam ser mais rápidas do que as outras quatro, elas amostram apenas um ou quatro elementos de textura para determinar o valor de textura do pixel que está sendo renderizado e podem produzir padrões de moire ou transições irregulares. O valor padrão do filtro GL de \_ textura \_ mínimo \_ é GL \_ \_ MIPMAP linear mais próximo \_ .

Suponha que texturing esteja habilitado (chamando [**glEnable**](glenable.md) com o argumento GL \_ Texture \_ 1D ou GL \_ Texture \_ 2D) e \_ \_ o filtro GL min Texture \_ seja definido como uma das funções que exigem um mipmap. Se as dimensões das imagens de textura definidas no momento (com chamadas anteriores para [**glTexImage1D**](glteximage1d.md) ou [**glTexImage2D**](glteximage2d.md)) não seguirem a sequência correta para mipmaps, ou se houver menos imagens de textura definidas do que o necessário, ou o conjunto de imagens de textura tiver diferentes números de componentes de textura, será como se o mapeamento de textura estivesse desabilitado. A filtragem linear acessa os quatro elementos de textura mais próximos somente em texturas 2D. Em texturas 1D, a filtragem linear acessa os dois elementos de textura mais próximos. A função a seguir recupera informações relacionadas a **glTexParameterf**, **glTexParameteri**, **glTexParameterfv** e **glTexParameteriv**:

[**glGetTexParameter**](glgettexparameter.md)

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

 

 





