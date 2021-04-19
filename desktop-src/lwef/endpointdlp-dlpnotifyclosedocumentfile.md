---
description: Fornece ao sistema informações sobre um documento antes da operação de fechamento do arquivo de documento ser iniciada.
title: Função DlpNotifyCloseDocumentFile (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyCloseDocumentFile
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 2438829cde84e9029a86d74e4ed704e1e8d33511
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495346"
---
# <a name="dlpnotifyclosedocumentfile-function"></a>Função DlpNotifyCloseDocumentFile

Fornece ao sistema informações sobre um documento antes da operação de fechamento do arquivo de documento ser iniciada.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI DlpNotifyCloseDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*DocumentInfo* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura de [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) que contém informações sobre o documento a ser aberto.

</dd> </dl>


## <a name="return-value"></a>Retornar valor

Retornar void.

## <a name="remarks"></a>Comentários


## <a name="requirements"></a>Requisitos


| Requisito          |    Valor                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1809 (10,0; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |