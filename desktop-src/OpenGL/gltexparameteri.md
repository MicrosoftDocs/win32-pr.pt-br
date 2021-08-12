---
title: Função glTexParameteri (Gl.h)
description: Define parâmetros de textura. | Função glTexParameteri (Gl.h)
ms.assetid: 67705f63-7f86-47c1-81f7-deecc0cd2e16
keywords:
- Função glTexParameteri OpenGL
topic_type:
- apiref
api_name:
- glTexParameteri
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bcc269c92d2d233f8c0dae89438232830539c3f8f59c3f8e28ef2be6ba42e54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118613233"
---
# <a name="gltexparameteri-function"></a>Função glTexParameteri

Define parâmetros de textura.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glTexParameteri(
   GLenum target,
   GLenum pname,
   GLint  param
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



| Valor                                                                                                                                                                                   | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span><dl> <dt>**FILTRO MIN \_ \_ DE TEXTURA \_ GL**</dt> </dl> | A função de mineração de textura é usada sempre que o pixel que está sendo texturado é mapeado para uma área maior que um elemento de textura. Há seis funções de mineração definidas. Dois deles usam um ou quatro elementos de textura mais próximos para calcular o valor da textura. Os outros quatro usam mipmaps. <br/> Um mipmap é um conjunto ordenado de matrizes que representam a mesma imagem em resoluções progressivamente inferiores. Se a textura tiver dimensões de 2nx2<sup>m,</sup> haverá max(n, m) + 1 mipmaps. O primeiro mipmap é a textura original, com dimensões de 2nx2<sup>m.</sup> Cada mipmap subsequente tem dimensões 2<sup>k</sup>1x2<sup>l</sup>1, em que 2<sup>k</sup>x2<sup>l</sup> são as dimensões do mipmap anterior, até k = 0 ou l = 0. Nesse ponto, os mipmaps subsequentes têm a dimensão 1x2<sup>l</sup>1 ou 2<sup>k</sup>1x1 até o mipmap final, que tem a dimensão 1x1. Os Mipmaps são definidos usando [**glTexImage1D**](glteximage1d.md) ou [**glTexImage2D**](glteximage2d.md) com o argumento de nível de detalhes que indica a ordem dos mipmaps. Nível 0 é a textura original; level bold max(n, m) é o mipmap 1x1 final.<br/> |
| <span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span><dl> <dt>**FILTRO GL \_ TEXTURE \_ MAG \_**</dt> </dl> | A função de ampliação de textura é usada quando o pixel que está sendo texturado é mapeado para uma área menor ou igual a um elemento de textura. Ele define a função de ampliação de textura como GL \_ NEAREST ou GL \_ LINEAR.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="GL_TEXTURE_WRAP_S"></span><span id="gl_texture_wrap_s"></span><dl> <dt>**GL \_ TEXTURE \_ WRAP \_ S**</dt> </dl>             | Define o parâmetro wrap para as coordenadas de textura como GL \_ TEXTURE ou GL \_ REPEAT. GL CLAMP faz com que as coordenadas sejam fixadas ao intervalo \_ \[ 0,1 e é útil para evitar o quebra-quebra de artefatos ao mapear uma única imagem para \] um objeto . GL \_ REPEAT faz com que a parte inteira da coordenada s seja ignorada; O OpenGL usa apenas a parte fracionada, criando assim um padrão de repetição. Os elementos de textura da borda serão acessados somente se o empacotamento estiver definido como GL \_ FIX. Inicialmente, GL \_ TEXTURE WRAP S é definido como GL \_ \_ \_ REPEAT.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_TEXTURE_WRAP_T"></span><span id="gl_texture_wrap_t"></span><dl> <dt>**GL \_ TEXTURE \_ WRAP \_ T**</dt> </dl>             | Define o parâmetro wrap para a coordenada de textura t como GL \_ CLAMP ou GL \_ REPEAT. Confira a discussão em GL \_ TEXTURE \_ WRAP \_ S. Inicialmente, GL \_ TEXTURE WRAP T é definido como GL \_ \_ \_ REPEAT<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

</dd> <dt>

*param* 
</dt> <dd>

O valor de *pname*.

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

Suponha que a texturing está habilitada (chamando [**glEnable**](glenable.md) com o argumento GL TEXTURE 1D ou GL TEXTURE 2D) e GL TEXTURE MIN FILTER está definido como uma das funções que exigem \_ \_ um \_ \_ \_ \_ \_ mipmap. Se as dimensões das imagens de textura definidas atualmente (com chamadas anteriores para [**glTexImage1D**](glteximage1d.md) ou [**glTexImage2D)**](glteximage2d.md)não seguirem a sequência adequada para mipmaps ou houver menos imagens de textura definidas do que são necessárias ou se o conjunto de imagens de textura tiver números diferentes de componentes de textura, será como se o mapeamento de textura estivesse desabilitado. A filtragem linear acessa os quatro elementos de textura mais próximos somente em texturas 2D. Em texturas 1D, a filtragem linear acessa os dois elementos de textura mais próximos. A função a seguir recupera informações relacionadas a **glTexParameterf**, **glTexParameteri,** **glTexParameterfv** e **glTexParameteriv**:

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

 

 





