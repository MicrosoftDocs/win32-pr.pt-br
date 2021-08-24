---
title: Função glRenderMode (Gl.h)
description: A função glRenderMode define o modo de rasterização.
ms.assetid: bcbc3bba-c552-425b-8284-6cadff0c9f56
keywords:
- Função glRenderMode OpenGL
topic_type:
- apiref
api_name:
- glRenderMode
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93eb3c7e2d7f4a6d261632e0f010cf0e1c7a2410a5a8364a6cf1fd65f36ada99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777926"
---
# <a name="glrendermode-function"></a>Função glRenderMode

A **função glRenderMode** define o modo de rasterização.

## <a name="syntax"></a>Sintaxe


```C++
GLint WINAPI glRenderMode(
   GLenum mode
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*mode* 
</dt> <dd>

O modo de rasterização. Os três valores a seguir são aceitos. O valor padrão é GL \_ RENDER.



| Valor                                                                                                                                                   | Significado                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_RENDER"></span><span id="gl_render"></span><dl> <dt>**RENDERIZAÇÃO GL \_**</dt> </dl>       | Modo de renderização. Os primitivos são rasterizados, produzindo fragmentos de pixel, que são gravados no framebuffer. Esse é o modo normal e também o modo padrão.<br/>                                                                                                                                                                                                      |
| <span id="GL_SELECT"></span><span id="gl_select"></span><dl> <dt>**GL \_ SELECT**</dt> </dl>       | Modo de seleção. Nenhum fragmento de pixel é produzido e nenhuma alteração no conteúdo do framebuffer é feita. Em vez disso, um registro dos nomes de primitivos que teria sido desenhado se o modo de renderização fosse GL RENDER é retornado em um buffer selecionado, que deve ser criado \_ (consulte [**glSelectBuffer**](glselectbuffer.md)) antes que o modo de seleção seja inserido.<br/>               |
| <span id="GL_FEEDBACK"></span><span id="gl_feedback"></span><dl> <dt>**COMENTÁRIOS SOBRE GL \_**</dt> </dl> | Modo de comentários. Nenhum fragmento de pixel é produzido e nenhuma alteração no conteúdo do framebuffer é feita. Em vez disso, as coordenadas e os atributos dos vértices que teriam sido desenhados se o modo de renderização fosse GL RENDER são retornados em um buffer de comentários, que deve ser criado \_ (consulte [**glFeedbackBuffer**](glfeedbackbuffer.md)) antes que o modo de comentários seja inserido.<br/> |



 

</dd> </dl>

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela [**função glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significado                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *mode* não era um dos três valores aceitos.<br/>                                                                                     |
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | A função foi chamada com o argumento GL \_ SELECT antes [**de glSelectBuffer**](glselectbuffer.md) ter sido chamado pelo menos uma vez.<br/>       |
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | A função foi chamada com o argumento GL \_ FEEDBACK antes [**de glBeedbackBuffer**](glfeedbackbuffer.md) ter sido chamado pelo menos uma vez.<br/> |
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd.**](glend.md)<br/>       |



## <a name="remarks"></a>Comentários

A **função glRenderMode** aceita um argumento, *modo*, que pode assumir um dos três valores predefinidos acima.

O valor de retorno da **função glRenderMode** é determinado pelo modo de renderização no momento em que **glRenderMode** é chamado, em vez de pelo *modo*. Os valores retornados para os três modos de renderização são os a seguir.



| Valor        | Significado                                                                 |
|--------------|-------------------------------------------------------------------------|
| RENDERIZAÇÃO GL \_   | Zero.                                                                   |
| GL \_ SELECT   | O número de registros de ocorrência transferidos para o buffer selecionado.             |
| COMENTÁRIOS SOBRE GL \_ | O número de valores (não vértices) transferidos para o buffer de comentários. |



 

Consulte [**glSelectBuffer e**](glselectbuffer.md) [**glFeedbackBuffer**](glfeedbackbuffer.md) para obter mais detalhes sobre a seleção e a operação de comentários.

Se um erro for gerado, **glRenderMode** retornará zero, independentemente do modo de renderização atual.

A função a seguir recupera informações relacionadas a **glRenderMode**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o argumento GL \_ RENDER \_ MODE

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

[**glFeedbackBuffer**](glfeedbackbuffer.md)
</dt> <dt>

[**glInitNames**](glinitnames.md)
</dt> <dt>

[**glLoadName**](glloadname.md)
</dt> <dt>

[**glPassThrough**](glpassthrough.md)
</dt> <dt>

[**glPushName**](glpushname.md)
</dt> <dt>

[**glSelectBuffer**](glselectbuffer.md)
</dt> </dl>

 

 





