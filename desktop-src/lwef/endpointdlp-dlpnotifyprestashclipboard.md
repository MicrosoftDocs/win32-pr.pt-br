---
description: Fornece ao sistema informações sobre um documento antes de uma operação de área de transferência de stash ser iniciada.
title: Função DlpNotifyPreStashClipboard (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreStashClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 920385d9cd57b428ce454415bf1dc57bed7ec4eb1373fa65d42f32668112bb0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976506"
---
# <a name="dlpnotifyprestashclipboard-function"></a>Função DlpNotifyPreStashClipboard

Notifica o sistema antes que uma operação de área de transferência de stash seja iniciada.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI DlpNotifyPreStashClipboard();
```



## <a name="parameters"></a>Parâmetros




## <a name="return-value"></a>Valor retornado

Retornar void.

## <a name="remarks"></a>Comentários


## <a name="requirements"></a>Requisitos



| Requisito          |    Valor                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1809 (10,0; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |