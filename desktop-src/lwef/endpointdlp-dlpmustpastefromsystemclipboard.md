---
description: Determina se o aplicativo deve extrair os dados da área de transferência do sistema em vez de retirá-los de seu cache interno.
title: Função DlpMustPasteFromSystemClipboard (endpointdlp. h)
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
ms.openlocfilehash: 5863173b02cb5c63a2de46653c2d268464e82e65
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495349"
---
# <a name="dlpmustpastefromsystemclipboard-function"></a>Função DlpMustPasteFromSystemClipboard

Determina se o aplicativo deve extrair os dados da área de transferência do sistema em vez de retirá-los de seu cache interno.

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI DlpMustPasteFromSystemClipboard();
```


## <a name="return-value"></a>Retornar valor

TRUE se a chamada para a área de transferência do sistema operacional for obrigatória; caso contrário, FALSE.

## <a name="remarks"></a>Comentários


## <a name="requirements"></a>Requisitos



| Requisito          |    Valor                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1809 (10,0; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |