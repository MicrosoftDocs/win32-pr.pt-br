---
description: Fornece ao sistema informações sobre um documento após a conclusão de uma operação de cópia para a área de transferência.
title: Função DlpNotifyPostCopyToClipboard (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostCopyToClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: afd054aa0728f3eeb70a5ecbbdeab88460deee2146aa10000665eb56f8d76b65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118751845"
---
# <a name="dlpnotifypostcopytoclipboard-function"></a>Função DlpNotifyPostCopyToClipboard

Fornece ao sistema informações sobre um documento após a conclusão de uma operação de cópia para a área de transferência.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI DlpNotifyPostCopyToClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*DocumentInfo* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura de [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) que contém informações sobre o documento do qual o conteúdo foi copiado.

</dd> </dl>

<dl> <dt>

*OpStatus* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura de [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) que contém informações de status sobre a operação de copiar para a área de transferência.

</dd> </dl>


## <a name="return-value"></a>Valor retornado

Retornar void.

## <a name="remarks"></a>Comentários


## <a name="requirements"></a>Requisitos



| Requisito          |    Valor                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1809 (10,0; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |