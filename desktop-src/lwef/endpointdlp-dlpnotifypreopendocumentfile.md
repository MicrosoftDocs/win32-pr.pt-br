---
description: Fornece ao sistema informações sobre um arquivo de documento antes que uma operação aberta seja iniciada.
title: Função DlpNotifyPreOpenDocumentFile (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreOpenDocumentFile
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: f2be797d0f4045f17e753031247797406f332afa2fcc47b3ca83973527d99216
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778226"
---
# <a name="dlpnotifypreopendocumentfile-function"></a>Função DlpNotifyPreOpenDocumentFile

Fornece ao sistema informações sobre um arquivo de documento antes que uma operação aberta seja iniciada.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI DlpNotifyPreOpenDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
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