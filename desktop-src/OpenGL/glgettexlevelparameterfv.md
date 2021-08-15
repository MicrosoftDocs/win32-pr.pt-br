---
title: função glGetTexLevelParameterfv (GL. h)
description: As funções glGetTexLevelParameterfv e glGetTexLevelParameteriv retornam valores de parâmetro de textura para um nível específico de detalhes. | função glGetTexLevelParameterfv (GL. h)
ms.assetid: 5ea91f2e-c0cd-41ee-be95-df096f1c78ef
keywords:
- função glGetTexLevelParameterfv OpenGL
topic_type:
- apiref
api_name:
- glGetTexLevelParameterfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b4068b6544c334c4ca1c8e6640ccb4752669240cdde16d0522a4e13d06ebc8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118359772"
---
# <a name="glgettexlevelparameterfv-function"></a>função glGetTexLevelParameterfv

As funções **glGetTexLevelParameterfv** e [**glGetTexLevelParameteriv**](glgettexlevelparameteriv.md) retornam valores de parâmetro de textura para um nível específico de detalhes.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glGetTexLevelParameterfv(
   GLenum  target,
   GLint   level,
   GLenum  pname,
   GLfloat *params
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*destino* 
</dt> <dd>

O nome simbólico da textura de destino: uma textura \_ GL \_ 1D, GL \_ Texture \_ 2D, GL \_ proxybinding bidirecionalmente ou o \_ \_ \_ proxy GL \_ textura \_ 2D.

</dd> <dt>

*level* 
</dt> <dd>

O número de nível de detalhe da imagem desejada. Nível 0 é o nível de imagem base. O nível *n* é a imagem de redução *n* º mipmap.

</dd> <dt>

*pname* 
</dt> <dd>

O nome simbólico de um parâmetro de textura. Os nomes de parâmetro a seguir são aceitos.



| Valor                                                                                                                                                                                                  | Significado                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_WIDTH"></span><span id="gl_texture_width"></span><dl> <dt>**\_largura da textura GL \_**</dt> </dl>                                | O parâmetro *params* retorna um único valor que contém a largura da imagem de textura. Esse valor inclui a borda da imagem de textura.<br/>                                                                                                                                          |
| <span id="GL_TEXTURE_HEIGHT"></span><span id="gl_texture_height"></span><dl> <dt>**\_altura da textura GL \_**</dt> </dl>                             | O parâmetro *params* retorna um único valor que contém a altura da imagem de textura. Esse valor inclui a borda da imagem de textura.<br/>                                                                                                                                         |
| <span id="GL_TEXTURE_INTERNAL_FORMAT"></span><span id="gl_texture_internal_format"></span><dl> <dt>**\_ \_ formato interno de textura GL \_**</dt> </dl> | O parâmetro *params* retorna um único valor que descreve o formato Texel da textura.<br/>                                                                                                                                                                                         |
| <span id="GL_TEXTURE_BORDER"></span><span id="gl_texture_border"></span><dl> <dt>**\_borda de textura GL \_**</dt> </dl>                             | O parâmetro *params* retorna um único valor: a largura em pixels da borda da imagem de textura.<br/>                                                                                                                                                                                 |
| <span id="GL_TEXTURE_RED_SIZE"></span><span id="gl_texture_red_size"></span><dl> <dt>**\_ \_ tamanho vermelho da textura GL \_**</dt> </dl>                      | A resolução de armazenamento interno do componente vermelho de um Texel. A resolução escolhida pelo OpenGL será uma correspondência próxima para a resolução solicitada pelo usuário com o argumento de componente de [**glTexImage1D**](glteximage1d.md) ou [**glTexImage2D**](glteximage2d.md).<br/>       |
| <span id="GL_TEXTURE_GREEN_SIZE"></span><span id="gl_texture_green_size"></span><dl> <dt>**\_ \_ Tamanho verde de textura GL \_**</dt> </dl>                | A resolução de armazenamento interno do componente verde de um Texel. A resolução escolhida pelo OpenGL será uma correspondência próxima para a resolução solicitada pelo usuário com o argumento de componente de [**glTexImage1D**](glteximage1d.md) ou [**glTexImage2D**](glteximage2d.md).<br/>     |
| <span id="GL_TEXTURE_BLUE_SIZE"></span><span id="gl_texture_blue_size"></span><dl> <dt>**\_ \_ tamanho azul de textura GL \_**</dt> </dl>                   | A resolução de armazenamento interno do componente azul de um Texel. A resolução escolhida pelo OpenGL será uma correspondência próxima para a resolução solicitada pelo usuário com o argumento de componente de [**glTexImage1D**](glteximage1d.md) ou [**glTexImage2D**](glteximage2d.md).<br/>      |
| <span id="GL_TEXTURE_ALPHA_SIZE"></span><span id="gl_texture_alpha_size"></span><dl> <dt>**\_ \_ tamanho alfa da textura GL \_**</dt> </dl>                | A resolução de armazenamento interno do componente alfa de um Texel. A resolução escolhida pelo OpenGL será uma correspondência próxima para a resolução solicitada pelo usuário com o argumento de componente de [**glTexImage1D**](glteximage1d.md) ou [**glTexImage2D**](glteximage2d.md).<br/>     |
| <span id="GL_TEXTURE_LUMINANCE_SIZE"></span><span id="gl_texture_luminance_size"></span><dl> <dt>**\_tamanho de \_ luminância de textura GL \_**</dt> </dl>    | A resolução de armazenamento interno do componente de luminância de um Texel. A resolução escolhida pelo OpenGL será uma correspondência próxima para a resolução solicitada pelo usuário com o argumento de componente de [**glTexImage1D**](glteximage1d.md) ou [**glTexImage2D**](glteximage2d.md).<br/> |
| <span id="GL_TEXTURE_INTENSITY_SIZE"></span><span id="gl_texture_intensity_size"></span><dl> <dt>**\_tamanho de \_ intensidade de textura GL \_**</dt> </dl>    | A resolução de armazenamento interno do componente de intensidade de um Texel. A resolução escolhida pelo OpenGL será uma correspondência próxima para a resolução solicitada pelo usuário com o argumento de componente de [**glTexImage1D**](glteximage1d.md) ou [**glTexImage2D**](glteximage2d.md).<br/> |
| <span id="GL_TEXTURE_COMPONENTS"></span><span id="gl_texture_components"></span><dl> <dt>**\_componentes de textura GL \_**</dt> </dl>                 | O parâmetro *params* retorna um único valor: o número de componentes na imagem de textura.<br/>                                                                                                                                                                                          |



 

</dd> <dt>

*params* 
</dt> <dd>

Retorna os dados solicitados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | *target* ou *pname* não era um valor aceito.<br/>                                                                             |
| <dl> <dt>**\_valor inválido do GL \_**</dt> </dl>     | o *nível* é menor que zero ou maior que o *log* 2 *(max)*, em que *Max* é o valor retornado do \_ tamanho de textura Max GL \_ \_ .<br/>      |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

A função **glGetTexLevelParameter** retorna nos valores de parâmetro de textura de *params* para um valor de nível de detalhe específico, especificado como *nível*. O parâmetro de *destino* define a textura de destino, tanto a \_ textura GL \_ 1D, GL \_ Texture \_ 2D, GL \_ proxy \_ \_ de textura 1D ou GL \_ proxy de destino \_ \_ 2D para especificar um texturing unidimensional ou bidimensional. O parâmetro *pname* especifica o parâmetro de textura cujo valor ou valores serão retornados.

Se um erro for gerado, nenhuma alteração será feita no conteúdo de *params*.

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

[**glEnd**](glend.md)
</dt> <dt>

[**glGetTexParameter**](glgettexparameter.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> <dt>

[**glTexParameter**](gltexparameter-functions.md)
</dt> </dl>

 

 





