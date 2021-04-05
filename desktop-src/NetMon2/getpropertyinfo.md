---
description: A função GetPropertyInfo retorna um ponteiro para as informações de propriedade de um determinado protocolo.
ms.assetid: f65166ba-1d94-4d65-b9d7-edb84ada0826
title: Função GetPropertyInfo (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPropertyInfo
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 007332a85f170f865604526199681cad6d68cdcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826833"
---
# <a name="getpropertyinfo-function"></a>Função GetPropertyInfo

A função **GetPropertyInfo** retorna um ponteiro para as informações de propriedade de um determinado protocolo.

## <a name="syntax"></a>Sintaxe


```C++
LPPROPERTYINFO WINAPI GetPropertyInfo(
  _In_ HPROPERTY hProperty
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hProperty* \[ no\]
</dt> <dd>

Identificador para uma propriedade.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será um ponteiro para a propriedade.

Se a função não for bem-sucedida, o valor de retorno será **nulo**.

## <a name="remarks"></a>Comentários

Os [*especialistas*](e.md) e os [*analisadores*](p.md) podem chamar a função **GetPropertyInfo** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




