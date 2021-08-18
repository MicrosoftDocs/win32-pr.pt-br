---
description: Fornece ao sistema informações sobre um documento antes que uma operação salvar como seja iniciada.
title: Função DlpNotifyPreSaveAsDocument (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpNotifyPreSaveAsDocument
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: 1dbd565ac7a86e381e1e70facf79a2883182260f82c31a2e8a9a3de4f6da8f2a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778216"
---
# <a name="dlpnotifypresaveasdocument-function"></a>Função DlpNotifyPreSaveAsDocument

Fornece ao sistema informações sobre um documento antes que uma operação salvar como seja iniciada.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI DlpNotifyPreSaveAsDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ LPCWSTR Destination);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*DocumentInfo* \[ Em\]
</dt> <dd>

Um ponteiro para uma [PDLP_DOCUMENT_INFO](endpointdlp-dlp_document_info.md) que contém informações sobre o documento a ser salvo.

</dd> </dl>

<dl> <dt>

*Destino* \[ Em\]
</dt> <dd>

Um **LPCWSTR que** contém o caminho de destino do documento a ser salvo.

</dd> </dl>


## <a name="return-value"></a>Valor retornado

Retornar nulo.

## <a name="remarks"></a>Comentários


## <a name="requirements"></a>Requisitos



| Requisito          |    Valor                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1809 (10.0; Build 17763)           |
| DLL<br/>                      | EndpointDlp.dll |