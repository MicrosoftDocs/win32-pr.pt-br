---
description: Fornece ao sistema informações sobre um documento após a conclusão de uma operação de impressão.
title: Função DlpNotifyPostPrint (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPostPrint
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: b1206aa4e358e0763c10a0d9b5028acae25f5683
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495329"
---
# <a name="dlpnotifypostprint-function"></a>Função DlpNotifyPostPrint

Fornece ao sistema informações sobre um documento após a conclusão de uma operação de impressão.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI DlpNotifyPostPrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*DocumentInfo* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura de [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) que contém informações sobre o documento associado à operação de impressão.

</dd> </dl>

<dl> <dt>

*Informações* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura de [DLP_PRINT_INFO](endpointdlp-dlp_print_info.md) que contém informações sobre a operação de impressão.

</dd> </dl>

<dl> <dt>

*OpStatus* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura de [DLP_POSTOP_STATUS](enpointdlp-dlp_postop_status.md) que contém informações de status sobre a operação de impressão.

</dd> </dl>


## <a name="return-value"></a>Retornar valor

Retornar void.

## <a name="remarks"></a>Comentários


## <a name="requirements"></a>Requisitos



| Requisito          |    Valor                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1809 (10,0; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |