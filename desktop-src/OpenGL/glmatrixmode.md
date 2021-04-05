---
title: função glMatrixMode (GL. h)
description: A função glMatrixMode especifica qual matriz é a matriz atual.
ms.assetid: f1006ea3-322a-42a9-b33c-6c7181985ef9
keywords:
- função glMatrixMode OpenGL
topic_type:
- apiref
api_name:
- glMatrixMode
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9877d62fc6e721cc6757206c7c2d07d24f3e879b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085889"
---
# <a name="glmatrixmode-function"></a>função glMatrixMode

A função **glMatrixMode** especifica qual matriz é a matriz atual.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glMatrixMode(
   GLenum mode
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*mode* 
</dt> <dd>

A pilha de matriz que é o destino para operações de matriz subsequentes. O parâmetro *Mode* pode assumir um dos três valores.



| Valor                                                                                                                                                         | Significado                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="GL_MODELVIEW"></span><span id="gl_modelview"></span><dl> <dt>**\_MODELVIEW GL**</dt> </dl>    | Aplica operações de matriz subsequentes à pilha de matriz modelview.<br/>  |
| <span id="GL_PROJECTION"></span><span id="gl_projection"></span><dl> <dt>**\_projeção GL**</dt> </dl> | Aplica operações de matriz subsequentes à pilha de matriz de projeção.<br/> |
| <span id="GL_TEXTURE"></span><span id="gl_texture"></span><dl> <dt>**\_textura GL**</dt> </dl>          | Aplica operações de matriz subsequentes à pilha de matriz de textura.<br/>    |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ inválido de \_ enumeração**</dt> </dl>      | o *modo* não era um valor aceito.<br/>                                                                                          |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

A função **glMatrixMode** define o modo de matriz atual.

A função a seguir recupera informações relacionadas a **glMatrixMode**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o \_ modo de matriz GL de argumento \_

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

[**glLoadMatrix**](glloadmatrix.md)
</dt> <dt>

[**glPushMatrix**](glpushmatrix.md)
</dt> </dl>

 

 





