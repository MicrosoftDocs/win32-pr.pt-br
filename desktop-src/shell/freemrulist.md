---
description: Libera o handle associado à lista de MRU (usados mais recentemente) e grava dados armazenados em cache no Registro.
title: Função FreeMRUList
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreeMRUList
api_type:
- DllExport
api_location:
- Comctl32.dll
ms.assetid: 51db9352-7188-4fb7-9c92-1d9579cd7250
ms.openlocfilehash: 7d31d261629853c3b82b9d1564c5e8755e047570
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840617"
---
# <a name="freemrulist-function"></a>Função FreeMRUList

Libera o handle associado à lista de MRU (usados mais recentemente) e grava dados armazenados em cache no Registro.

## <a name="syntax"></a>Sintaxe


```C++
int FreeMRUList(
  _In_ HANDLE hMRU
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hMRU* \[ Em\]
</dt> <dd>

Tipo: **HANDLE**

O alça da lista mru para liberar.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **int**

Retornará um valor não negativo se for bem-sucedido; caso contrário, -1.

## <a name="remarks"></a>Comentários

Se a lista mru foi criada usando o sinalizador **\_ MRU CACHEWRITE,** chamar **FreeMRUList** faz com que todas as alterações ainda não gravadas na versão da lista mru armazenada no registro sejam gravadas no momento.

Essa função não está incluída em um header ou biblioteca público. Ele deve ser extraído da comctl32.dll pelo ordinal 152.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (versão 5.0 ou posterior)</dt> </dl> |



 

 




