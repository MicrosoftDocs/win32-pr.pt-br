---
description: Especifica informações de status sobre uma operação de DLP de ponto de extremidade.
title: Estrutura de DLP_POSTOP_STATUS (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_POSTOP_STATUS
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: c0221926700fc8960de5ef4d25c36136c3fc9737
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495309"
---
# <a name="dlp_postop_status-structure"></a>Estrutura de DLP_POSTOP_STATUS

Especifica informações de status sobre uma operação de DLP de ponto de extremidade.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _DLP_POSTOP_STATUS {
    
    DWORD Version;    
    BOOL OperationSuccess;  

} DLP_POSTOP_STATUS, *PDLP_POSTOP_STATUS; 
```


## <a name="members"></a>Membros

<dl> <dt>

*Versão* \[ do no\]
</dt> <dd>

Um DWORD que especifica a versão da API. Esse valor sempre deve ser **DLP_POSTOP_STATUS_V_LATEST**. Essa constante é definida na listagem de arquivos de cabeçalho de exemplo endpointdlp. h no artigo [prevenção de perda de dados do ponto de extremidade](endpointdlp-endpoint-data-loss-prevention.md)

</dd> </dl>

<dl> <dt>

*OperationSuccess* \[ no\]
</dt> <dd>

Um BOOL que indica se a operação aberta foi bem-sucedida.

</dd> </dl>





## <a name="remarks"></a>Comentários


## <a name="requirements"></a>Requisitos



| Requisito          |    Valor                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1809 (10,0; Build 17763)           |
