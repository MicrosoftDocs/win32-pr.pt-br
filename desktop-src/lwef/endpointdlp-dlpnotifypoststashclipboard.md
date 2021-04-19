---
description: Fornece o sistema com informações de status após a conclusão de uma operação de área de transferência de stash.
title: Função DlpNotifyPostStashClipboard (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostStashClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: e549593acab6d74edf838a0f82952d8f3034bfcc
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495326"
---
# <a name="dlpnotifypoststashclipboard-function"></a>Função DlpNotifyPostStashClipboard

Fornece o sistema com informações de status após a conclusão de uma operação de área de transferência de stash.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI DlpNotifyPostStashClipboard(_In_ const PDLP_POSTOP_STATUS OpStatus);
```



## <a name="parameters"></a>Parâmetros


<dl> <dt>

*OpStatus* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura de [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) que contém informações de status sobre a operação de área de transferência de stash.

</dd> </dl>


## <a name="return-value"></a>Retornar valor

Retornar void.

## <a name="remarks"></a>Comentários


## <a name="requirements"></a>Requisitos



| Requisito          |    Valor                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1809 (10,0; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |