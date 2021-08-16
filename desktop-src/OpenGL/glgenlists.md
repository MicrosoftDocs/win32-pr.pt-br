---
title: função glGenLists (GL. h)
description: A função glGenLists gera um conjunto contíguo de listas de exibição vazias.
ms.assetid: 07a97e89-1fbe-4405-b1b0-c4c47b098633
keywords:
- função glGenLists OpenGL
topic_type:
- apiref
api_name:
- glGenLists
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a916b163f2ec04e51da06263aed0f76f5e4dd6b51b7eca9fdbca8965644fdd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118360393"
---
# <a name="glgenlists-function"></a>função glGenLists

A função **glGenLists** gera um conjunto contíguo de listas de exibição vazias.

## <a name="syntax"></a>Sintaxe


```C++
GLuint WINAPI glGenLists(
   GLsizei range
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*range* 
</dt> <dd>

O número de listas de exibição vazias contíguas a serem geradas.

</dd> </dl>

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valor inválido do GL \_**</dt> </dl>     | o *intervalo* era negativo.<br/>                                                                                                      |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

A função **glGenLists** tem um argumento, *Range*. Ele retorna um número inteiro *n* , dessa forma, lista de exibição vazia de *intervalo* , chamada *n*, *n* + 1,. . ., *n* + (*Range* -1), são criados. Se *Range* for zero, se não houver nenhum grupo de nomes contíguos de *intervalo* disponíveis, ou se qualquer erro for gerado, nenhuma lista de exibição será gerada e zero será retornado.

A função a seguir recupera informações relacionadas a **glGenLists**:

[**glIsList**](glislist.md)

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

[**glCallList**](glcalllist.md)
</dt> <dt>

[**glCallLists**](glcalllists.md)
</dt> <dt>

[**glDeleteLists**](gldeletelists.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glIsList**](glislist.md)
</dt> <dt>

[**glNewList**](glnewlist.md)
</dt> </dl>

 

 





