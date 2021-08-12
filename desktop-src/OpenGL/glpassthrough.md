---
title: Função glPassThrough (Gl.h)
description: A função glPassThrough coloca um marcador no buffer de comentários.
ms.assetid: 14664ac6-eb25-46ae-86d8-7ece31df103f
keywords:
- Função glPassThrough OpenGL
topic_type:
- apiref
api_name:
- glPassThrough
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5edf1b0fb2dbda1ef1e0a2c4b9ab67b8e7e6305998a8f5a6de9c461e4e148bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118615413"
---
# <a name="glpassthrough-function"></a>Função glPassThrough

A **função glPassThrough** coloca um marcador no buffer de comentários.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glPassThrough(
   GLfloat token
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*token* 
</dt> <dd>

Um valor de marcador a ser colocado no buffer de comentários. Ele é indicado com o seguinte valor de identificação exclusivo.



| Valor                                                                                                                                                                                   | Significado                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_PASS_THROUGH_TOKEN"></span><span id="gl_pass_through_token"></span><dl> <dt>**TOKEN DE \_ \_ PASSAGEM GL \_**</dt> </dl> | A ordem dos **comandos glPassThrough** em relação à especificação de primitivos gráficos é mantida.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

O código de erro a seguir pode ser recuperado pela [**função glGetError.**](glgeterror.md)



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERAÇÃO \_ GL \_ INVÁLIDA**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd.**](glend.md)<br/> |



## <a name="remarks"></a>Comentários

Feedback é um modo de renderização OpenGL selecionado chamando [**glRenderMode**](glrendermode.md) com GL \_ FEEDBACK. Quando o OpenGL está no modo de comentários, nenhum pixel é produzido pela rasterização. Em vez disso, as informações sobre primitivos que teriam sido rasterizados são alimentadas novamente para o aplicativo pelo OpenGL. Consulte [**glFeedbackBuffer para**](glfeedbackbuffer.md) ver uma descrição do buffer de comentários e os valores nele.

A **função glPassThrough** insere um marcador definido pelo usuário no buffer de comentários quando ele é executado no modo de comentários. O parâmetro de *token* é retornado como se fosse um primitivo.

A **função glPassThrough** será ignorada se o OpenGL não estiver no modo de comentários.

A função a seguir recupera informações relacionadas a **glPassThrough**:

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

[**glRenderMode**](glrendermode.md)
</dt> </dl>

 

 





