---
title: função glRenderMode (GL. h)
description: A função glRenderMode define o modo de rasterização.
ms.assetid: bcbc3bba-c552-425b-8284-6cadff0c9f56
keywords:
- função glRenderMode OpenGL
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
ms.openlocfilehash: af07d2492d70f9c0a3a764d767b52b2f71204939
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086395"
---
# <a name="glrendermode-function"></a>função glRenderMode

A função **glRenderMode** define o modo de rasterização.

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

O modo de rasterização. Os três valores a seguir são aceitos. O valor padrão é GL \_ render.



| Valor                                                                                                                                                   | Significado                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_RENDER"></span><span id="gl_render"></span><dl> <dt>**\_RENDERIZAÇÃO GL**</dt> </dl>       | Modo de renderização. Os primitivos são rasterizados, produzindo fragmentos de pixel, que são gravados no framebuffer. Esse é o modo normal e também o modo padrão.<br/>                                                                                                                                                                                                      |
| <span id="GL_SELECT"></span><span id="gl_select"></span><dl> <dt>**\_Select GL**</dt> </dl>       | Modo de seleção. Nenhum fragmento de pixel é produzido e nenhuma alteração no conteúdo de framebuffer é feita. Em vez disso, um registro dos nomes de primitivos que teriam sido desenhados se o modo render era o \_ render GL ser retornado em um buffer Select, que deve ser criado (consulte [**glSelectBuffer**](glselectbuffer.md)) antes de o modo de seleção ser inserido.<br/>               |
| <span id="GL_FEEDBACK"></span><span id="gl_feedback"></span><dl> <dt>**Comentários do GL \_**</dt> </dl> | Modo de comentários. Nenhum fragmento de pixel é produzido e nenhuma alteração no conteúdo de framebuffer é feita. Em vez disso, as coordenadas e os atributos dos vértices que teriam sido desenhados no modo de renderização eram \_ retornados em um buffer de comentários, que deve ser criado (consulte [**glFeedbackBuffer**](glfeedbackbuffer.md)) antes que o modo de comentários seja inserido.<br/> |



 

</dd> </dl>

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | o *modo* não era um dos três valores aceitos.<br/>                                                                                     |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada com o argumento GL \_ Select antes de [**glSelectBuffer**](glselectbuffer.md) ser chamado pelo menos uma vez.<br/>       |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada com comentários do Argument GL \_ antes que [**glBeedbackBuffer**](glfeedbackbuffer.md) fosse chamado pelo menos uma vez.<br/> |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/>       |



## <a name="remarks"></a>Comentários

A função **glRenderMode** usa um argumento, *modo*, que pode assumir um dos três valores predefinidos acima.

O valor de retorno da função **glRenderMode** é determinado pelo modo render no momento em que **glRenderMode** é chamado, e não por *modo*. Os valores retornados para os três modos de renderização são os seguintes.



| Valor        | Significado                                                                 |
|--------------|-------------------------------------------------------------------------|
| \_RENDERIZAÇÃO GL   | Zero.                                                                   |
| \_Select GL   | O número de registros de acesso transferido para o buffer selecionado.             |
| Comentários do GL \_ | O número de valores (não vértices) transferidos para o buffer de comentários. |



 

Consulte [**glSelectBuffer**](glselectbuffer.md) e [**glFeedbackBuffer**](glfeedbackbuffer.md) para obter mais detalhes sobre a operação de seleção e de comentários.

Se um erro for gerado, **glRenderMode** retornará zero, independentemente do modo de processamento atual.

A função a seguir recupera informações relacionadas a **glRenderMode**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o \_ modo de renderização Argument GL \_

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

 

 





