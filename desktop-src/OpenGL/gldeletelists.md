---
title: função glDeleteLists (GL. h)
description: A função glDeleteLists exclui um grupo contíguo de listas de exibição.
ms.assetid: 979ab352-99db-4822-922c-a1813b9fcfce
keywords:
- função glDeleteLists OpenGL
topic_type:
- apiref
api_name:
- glDeleteLists
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c11ae41273cba5bd050a62ea330cef9da0647769
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105789880"
---
# <a name="gldeletelists-function"></a>função glDeleteLists

A função **glDeleteLists** exclui um grupo contíguo de listas de exibição.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI glDeleteLists(
   GLuint  list,
   GLsizei range
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*list* 
</dt> <dd>

O nome inteiro da primeira lista de exibição a ser excluída.

</dd> <dt>

*range* 
</dt> <dd>

O número de listas de exibição a serem excluídas.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="error-codes"></a>Códigos do Erro

Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .



| Nome                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valor inválido do GL \_**</dt> </dl>     | o *intervalo* era negativo.<br/>                                                                                                      |
| <dl> <dt>**GL \_ operação inválida \_**</dt> </dl> | A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentários

A função **glDeleteLists** faz com que um grupo contíguo de listas de exibição seja excluído. O parâmetro *list* é o nome da primeira lista de exibição a ser excluída e *Range* é o número de listas de exibição a serem excluídas. Todas as listas de exibição *d* *com list*  =  *d*  =  *listar*  +  *intervalo* -1 são excluídas.

Todos os locais de armazenamento alocados para as listas de exibição especificadas são liberados e os nomes estão disponíveis para reutilização posteriormente. Os nomes dentro do intervalo que não têm uma lista de exibição associada são ignorados. Se o *intervalo* for zero, nada acontecerá.

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

[**glEnd**](glend.md)
</dt> <dt>

[**glGenLists**](glgenlists.md)
</dt> <dt>

[**glIsList**](glislist.md)
</dt> <dt>

[**glNewList**](glnewlist.md)
</dt> </dl>

 

 





