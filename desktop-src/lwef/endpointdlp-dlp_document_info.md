---
description: Especifica informações sobre um documento associado a uma operação DLP de ponto de extremidade.
title: Estrutura DLP_DOCUMENT_INFO (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_DOCUMENT_INFO
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: 8aa4b6c961b4e80786e9ada480949245b032750499b38f0deead44f97a2d88fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118479759"
---
# <a name="dlp_document_info-structure"></a>DLP_DOCUMENT_INFO estrutura

Especifica informações sobre um documento associado a uma operação DLP de ponto de extremidade.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _DLP_DOCUMENT_INFO {

    DWORD Version;    
    LPCWSTR PersistentFileName;
    LPCWSTR LocalFileName;

}DLP_DOCUMENT_INFO, *PDLP_DOCUMENT_INFO;
```


## <a name="members"></a>Membros

<dl> <dt>

*Versão* \[ Em\]
</dt> <dd>

Um DWORD que especifica a versão da API. Esse valor sempre deve ser **DLP_DOCUMENT_INFO_V_LATEST**. Essa constante é definida na listagem de arquivo de header de exemplo endpointdlp.h no artigo [Prevenção contra](endpointdlp-endpoint-data-loss-prevention.md)perda de dados do ponto de extremidade .

</dd> </dl>

<dl> <dt>

*PersistentFileName* \[ Em\]
</dt> <dd>

Um LPCWSTR que especifica o caminho original do documento.

</dd> </dl>

<dl> <dt>

*LocalFileName* \[ Em\]
</dt> <dd>

Um LPCWSTR que especifica o caminho para o arquivo de backing real do documento.

</dd> </dl>



## <a name="remarks"></a>Comentários


## <a name="requirements"></a>Requisitos



| Requisito          |    Valor                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1809 (10.0; Build 17763)           |

