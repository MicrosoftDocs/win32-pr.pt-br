---
description: Fornece ao sistema informações sobre um documento antes de uma operação de impressão ser iniciada.
title: Função DlpNotifyPrePrint (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPrePrint
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 1cf0ef44031677495d9b9bedf990877ee931cae245b217faa4225b334df1b3b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118479437"
---
# <a name="dlpnotifypreprint-function"></a>Função DlpNotifyPrePrint

Fornece ao sistema informações sobre um documento antes de uma operação de impressão ser iniciada.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI DlpNotifyPrePrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*DocumentInfo* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura de [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) que contém informações sobre o documento a ser impresso.

</dd> </dl>

<dl> <dt>

*Informações* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura de [DLP_PRINT_INFO](endpointdlp-dlp_print_info.md) que contém informações sobre a operação de impressão.

</dd> </dl>


## <a name="return-value"></a>Valor retornado

Retornar void.

## <a name="remarks"></a>Comentários


## <a name="requirements"></a>Requisitos



| Requisito          |    Valor                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1809 (10,0; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |