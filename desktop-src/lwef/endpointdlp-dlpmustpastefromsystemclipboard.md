---
description: Determina se o aplicativo deve receber os dados da área de transferência do sistema em vez de replicação de seu cache interno.
title: Função DlpMustPasteFromSystemClipboard (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpMustPasteFromSystemClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: e111cb85c6eada6f84f7bc10eb240e89447a173e741b26b316b232d742f8de48
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888576"
---
# <a name="dlpmustpastefromsystemclipboard-function"></a>Função DlpMustPasteFromSystemClipboard

Determina se o aplicativo deve receber os dados da área de transferência do sistema em vez de replicação de seu cache interno.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI DlpMustPasteFromSystemClipboard();
```


## <a name="return-value"></a>Valor retornado

TRUE se chamar na área de transferência do sistema operacional for obrigatório; caso contrário, FALSE.

## <a name="remarks"></a>Comentários


## <a name="requirements"></a>Requisitos



| Requisito          |    Valor                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1809 (10.0; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |