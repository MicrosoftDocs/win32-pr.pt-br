---
description: Fornece ao sistema informações sobre um documento antes que a operação de fechamento do arquivo de documento seja iniciada.
title: Função DlpNotifyCloseDocumentFile (endpointdlp.h)
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
ms.openlocfilehash: fc4aff982ebfa8e16f4a7d2c0cd42a847825b422af761416d4a410a03df66446
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062136"
---
# <a name="dlpnotifyclosedocumentfile-function"></a>Função DlpNotifyCloseDocumentFile

Fornece ao sistema informações sobre um documento antes que a operação de fechamento do arquivo de documento seja iniciada.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI DlpNotifyCloseDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*DocumentInfo* \[ Em\]
</dt> <dd>

Um ponteiro para uma [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) que contém informações sobre o documento a ser aberto.

</dd> </dl>


## <a name="return-value"></a>Valor retornado

Retornar nulo.

## <a name="remarks"></a>Comentários


## <a name="requirements"></a>Requisitos


| Requisito          |    Valor                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1809 (10.0; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |