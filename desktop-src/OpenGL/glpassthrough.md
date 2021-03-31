---
title: função glPassThrough (GL. h)
description: A função glPassThrough coloca um marcador no buffer de comentários.
ms.assetid: 14664ac6-eb25-46ae-86d8-7ece31df103f
keywords:
- função glPassThrough OpenGL
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
ms.openlocfilehash: fd1174dd933d46813a89c35b781d0408c3ac5476
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644558"
---
# <a name="glpassthrough-function"></a>função glPassThrough

A função **glPassThrough** coloca um marcador no buffer de comentários.

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
| <span id="GL_PASS_THROUGH_TOKEN"></span><span id="gl_pass_through_token"></span><dl> <dt>**\_token de passagem GL \_ \_**</dt> </dl> | A ordem dos comandos **glPassThrough** em relação à especificação de primitivos gráficos é mantida.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .



| Name                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

Feedback é um modo de renderização OpenGL selecionado chamando [**glRenderMode**](glrendermode.md) com os \_ comentários GL. Quando OpenGL está no modo de comentários, nenhum pixel é produzido pela rasterização. Em vez disso, as informações sobre primitivas que teriam sido rasterizadas são alimentadas de volta para o aplicativo por OpenGL. Consulte [**glFeedbackBuffer**](glfeedbackbuffer.md) para obter uma descrição do buffer de comentários e os valores contidos nele.

A função **glPassThrough** insere um marcador definido pelo usuário no buffer de comentários quando ele é executado no modo de comentários. O parâmetro de *token* é retornado como se fosse um primitivo.

A função **glPassThrough** será ignorada se OpenGL não estiver no modo de comentários.

A função a seguir recupera informações relacionadas a **glPassThrough**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o \_ modo de renderização Argument GL \_

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glFeedbackBuffer**](glfeedbackbuffer.md)
</dt> <dt>

[**glRenderMode**](glrendermode.md)
</dt> </dl>

 

 





