---
description: Especifica informações sobre um documento associado a uma operação de DLP de ponto de extremidade.
title: Estrutura de DLP_DOCUMENT_INFO (endpointdlp. h)
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
ms.openlocfilehash: d588b627a4d5a88162cb0af67df1b5bf4fd943f1
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495364"
---
# <a name="dlp_document_info-structure"></a>Estrutura de DLP_DOCUMENT_INFO

Especifica informações sobre um documento associado a uma operação de DLP de ponto de extremidade.

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

*Versão* \[ do no\]
</dt> <dd>

Um DWORD que especifica a versão da API. Esse valor sempre deve ser **DLP_DOCUMENT_INFO_V_LATEST**. Essa constante é definida na listagem de arquivos de cabeçalho de exemplo endpointdlp. h no artigo [prevenção de perda de dados do ponto de extremidade](endpointdlp-endpoint-data-loss-prevention.md).

</dd> </dl>

<dl> <dt>

*PersistentFileName* \[ no\]
</dt> <dd>

Um LPCWSTR que especifica o caminho original do documento.

</dd> </dl>

<dl> <dt>

*LocalFileName* \[ no\]
</dt> <dd>

Um LPCWSTR especificando o caminho para o arquivo de backup real do documento.

</dd> </dl>



## <a name="remarks"></a>Comentários


## <a name="requirements"></a>Requisitos



| Requisito          |    Valor                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1809 (10,0; Build 17763)           |

