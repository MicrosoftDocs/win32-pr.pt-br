---
description: Fornece ao sistema informações sobre um documento antes de uma operação de área de transferência de stash ser iniciada.
title: Função DlpNotifyPreStashClipboard (endpointdlp. h)
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
ms.openlocfilehash: 72ecabb2bbfb7517b52790c0d3b7c1ab8075dbd0
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495308"
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