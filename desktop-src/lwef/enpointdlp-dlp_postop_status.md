---
description: Especifica informações de status sobre uma operação de DLP de ponto de extremidade.
title: Estrutura DLP_POSTOP_STATUS (endpointdlp.h)
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
ms.openlocfilehash: 6b8922bee5fb93ee4412833418a63c19dd311c8809cf64132a0f28fbe91d11bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610226"
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
