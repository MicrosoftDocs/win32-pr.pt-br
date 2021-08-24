---
description: Fornece ao sistema informações sobre um documento antes que uma operação de colar da área de transferência seja iniciada.
title: Função DlpNotifyPrePasteFromClipboard (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPrePasteFromClipboard
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: b490f4f5a258805c785822d815d9e341feb8bbd494e428eb7bf1be6da843d775
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778176"
---
# <a name="dlpnotifyprepastefromclipboard-function"></a>Função DlpNotifyPrePasteFromClipboard

Fornece ao sistema informações sobre um documento antes que uma operação de colar da área de transferência seja iniciada.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI DlpNotifyPrePasteFromClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*DocumentInfo* \[ Em\]
</dt> <dd>

Um ponteiro para uma [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) que contém informações sobre o documento no qual o conteúdo está sendo colar.

</dd> </dl>




## <a name="return-value"></a>Valor retornado

Retornar nulo.

## <a name="remarks"></a>Comentários


## <a name="requirements"></a>Requisitos



| Requisito          |    Valor                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1809 (10.0; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |