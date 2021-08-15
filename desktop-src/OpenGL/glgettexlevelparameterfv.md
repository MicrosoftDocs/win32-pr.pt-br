---
title: Função glGetTexLevelParameterfv (Gl.h)
description: As funções glGetTexLevelParameterfv e glGetTexLevelParameteriv retornam valores de parâmetro de textura para um nível específico de detalhes. | Função glGetTexLevelParameterfv (Gl.h)
ms.assetid: 5ea91f2e-c0cd-41ee-be95-df096f1c78ef
keywords:
- Função glGetTexLevelParameterfv OpenGL
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
# <a name="glgettexlevelparameterfv-function"></a>Função glGetTexLevelParameterfv

As **funções glGetTexLevelParameterfv** e [**glGetTexLevelParameteriv**](glgettexlevelparameteriv.md) retornam valores de parâmetro de textura para um nível específico de detalhe.

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

O nome simbólico da textura de destino: GL \_ TEXTURE \_ 1D, GL \_ TEXTURE \_ 2D, GL \_ PROXY TEXTURE 1D ou GL PROXY TEXTURE \_ \_ \_ \_ \_ 2D.

</dd> <dt>

*level* 
</dt> <dd>

O número de nível de detalhe da imagem desejada. Nível 0 é o nível de imagem base. O *nível n* é a n *imagem* de redução de mipmap.

</dd> <dt>

*Pname* 
</dt> <dd>

O nome simbólico de um parâmetro de textura. Os seguintes nomes de parâmetro são aceitos.



| Valor                                                                                                                                                                                                  | Significado                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_WIDTH"></span><span id="gl_texture_width"></span><dl> <dt>**LARGURA \_ DA TEXTURA \_ GL**</dt> </dl>                                | O *parâmetro params* retorna um único valor que contém a largura da imagem de textura. Esse valor inclui a borda da imagem de textura.<br/>                                                                                                                                          |
| <span id="GL_TEXTURE_HEIGHT"></span><span id="gl_texture_height"></span><dl> <dt>**ALTURA \_ DA TEXTURA \_ GL**</dt> </dl>                             | O *parâmetro params* retorna um único valor que contém a altura da imagem de textura. Esse valor inclui a borda da imagem de textura.<br/>                                                                                                                                         |
| <span id="GL_TEXTURE_INTERNAL_FORMAT"></span><span id="gl_texture_internal_format"></span><dl> <dt>**FORMATO \_ INTERNO DA TEXTURA \_ \_ GL**</dt> </dl> | O *parâmetro params* retorna um único valor que descreve o formato de texel da textura.<br/>                                                                                                                                                                                         |
| <span id="GL_TEXTURE_BORDER"></span><span id="gl_texture_border"></span><dl> <dt>**BORDA DE \_ TEXTURA \_ GL**</dt> </dl>                             | O *parâmetro params* retorna um único valor: a largura em pixels da borda da imagem de textura.<br/>                                                                                                                                                                                 |
| <span id="GL_TEXTURE_RED_SIZE"></span><span id="gl_texture_red_size"></span><dl> <dt>**TAMANHO \_ VERMELHO DA TEXTURA \_ \_ GL**</dt> </dl>                      | A resolução de armazenamento interno do componente vermelho de um texel. A resolução escolhida pelo OpenGL será uma combinação próxima para a resolução solicitada pelo usuário com o argumento de componente [**glTexImage1D**](glteximage1d.md) ou [**glTexImage2D.**](glteximage2d.md)<br/>       |
| <span id="GL_TEXTURE_GREEN_SIZE"></span><span id="gl_texture_green_size"></span><dl> <dt>**TAMANHO VERDE \_ \_ DA TEXTURA \_ GL**</dt> </dl>                | A resolução de armazenamento interno do componente verde de um texel. A resolução escolhida pelo OpenGL será uma combinação próxima para a resolução solicitada pelo usuário com o argumento de componente [**glTexImage1D**](glteximage1d.md) ou [**glTexImage2D.**](glteximage2d.md)<br/>     |
| <span id="GL_TEXTURE_BLUE_SIZE"></span><span id="gl_texture_blue_size"></span><dl> <dt>**TAMANHO \_ AZUL DA TEXTURA \_ \_ GL**</dt> </dl>                   | A resolução de armazenamento interno do componente azul de um texel. A resolução escolhida pelo OpenGL será uma combinação próxima para a resolução solicitada pelo usuário com o argumento de componente [**glTexImage1D**](glteximage1d.md) ou [**glTexImage2D.**](glteximage2d.md)<br/>      |
| <span id="GL_TEXTURE_ALPHA_SIZE"></span><span id="gl_texture_alpha_size"></span><dl> <dt>**TAMANHO ALFA \_ \_ DA TEXTURA \_ GL**</dt> </dl>                | A resolução de armazenamento interno do componente alfa de um texel. A resolução escolhida pelo OpenGL será uma combinação próxima para a resolução solicitada pelo usuário com o argumento de componente [**glTexImage1D**](glteximage1d.md) ou [**glTexImage2D.**](glteximage2d.md)<br/>     |
| <span id="GL_TEXTURE_LUMINANCE_SIZE"></span><span id="gl_texture_luminance_size"></span><dl> <dt>**TAMANHO \_ DA \_ LUMINÂNCIA DA TEXTURA \_ GL**</dt> </dl>    | A resolução de armazenamento interno do componente de luminância de um texel. A resolução escolhida pelo OpenGL será uma combinação próxima para a resolução solicitada pelo usuário com o argumento de componente [**glTexImage1D**](glteximage1d.md) ou [**glTexImage2D.**](glteximage2d.md)<br/> |
| <span id="GL_TEXTURE_INTENSITY_SIZE"></span><span id="gl_texture_intensity_size"></span><dl> <dt>**TAMANHO \_ DA INTENSIDADE DA TEXTURA \_ \_ GL**</dt> </dl>    | A resolução de armazenamento interno do componente de intensidade de um texel. A resolução escolhida pelo OpenGL será uma combinação próxima para a resolução solicitada pelo usuário com o argumento de componente [**glTexImage1D**](glteximage1d.md) ou [**glTexImage2D.**](glteximage2d.md)<br/> |
| <span id="GL_TEXTURE_COMPONENTS"></span><span id="gl_texture_components"></span><dl> <dt>**COMPONENTES \_ DE TEXTURA \_ GL**</dt> </dl>                 | O *parâmetro params* retorna um único valor: o número de componentes na imagem de textura.<br/>                                                                                                                                                                                          |



 

</dd> <dt>

*params* 
</dt> <dd>

Retorna os dados solicitados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela [**função glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *target* ou *pname* não era um valor aceito.<br/>                                                                             |
| <dl> <dt>**VALOR INVÁLIDO DE GL \_ \_**</dt> </dl>     | *level* é menor que zero ou maior que *o log* 2 *(máx.),* em que *max* é o valor retornado de GL MAX \_ TEXTURE \_ \_ SIZE.<br/>      |
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd.**](glend.md)<br/> |



## <a name="remarks"></a>Comentários

A **função glGetTexLevelParameter** retorna em valores de parâmetro de textura *params* para um valor de nível de detalhe específico, especificado como *nível*. O  parâmetro de destino define a textura de destino, GL \_ TEXTURE \_ 1D, GL \_ TEXTURE \_ 2D, GL \_ PROXY TEXTURE 1D ou GL PROXY TEXTURE 2D para especificar \_ \_ \_ \_ \_ texturagem unidimensional ou bidimensional. O *parâmetro pname* especifica o parâmetro de textura cujos valores ou valores serão retornados.

Se um erro for gerado, nenhuma alteração será feita no conteúdo *de params*.

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

 

 





