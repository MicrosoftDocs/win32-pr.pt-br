---
description: Libera o identificador associado à lista MRU (usados mais recentemente) e grava os dados armazenados em cache no registro.
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
ms.openlocfilehash: 8140586d5f428a66f27a71ea665ae6761380e3a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967925"
---
# <a name="freemrulist-function"></a>Função FreeMRUList

Libera o identificador associado à lista MRU (usados mais recentemente) e grava os dados armazenados em cache no registro.

## <a name="syntax"></a>Sintaxe


```C++
int FreeMRUList(
  _In_ HANDLE hMRU
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hMRU* \[ no\]
</dt> <dd>

Tipo: **identificador**

O identificador da lista MRU como livre.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **int**

Retorna um valor não negativo se for bem-sucedido,-1 caso contrário.

## <a name="remarks"></a>Comentários

Se a lista MRU tiver sido criada usando o sinalizador **\_ CACHEWRITE MRU** , chamar **FreeMRUList** fará com que todas as alterações ainda não gravadas na versão da lista MRU armazenada no registro sejam gravadas neste momento.

Essa função não está incluída em um cabeçalho ou biblioteca pública. Ele deve ser extraído de comctl32.dll pelo ordinal 152.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (versão 5,0 ou posterior)</dt> </dl> |



 

 




