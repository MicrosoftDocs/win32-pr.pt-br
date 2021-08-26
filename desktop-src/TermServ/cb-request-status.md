---
title: CB_REQUEST_STATUS enumeração (Cbclient.h)
description: Especifica o status de uma solicitação assíncrona.
ms.assetid: 35FAC8EA-BA17-405F-AE10-33A816029F62
ms.tgt_platform: multiple
keywords:
- CB_REQUEST_STATUS enumeração Serviços de Área de Trabalho Remota
topic_type:
- apiref
api_name:
- CB_REQUEST_STATUS
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6647f10ab91fd5cb1919d49c4c00d22b8b1722de9b20d9b83fdee8fcceaef95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871966"
---
# <a name="cb_request_status-enumeration"></a>\_Enumeração CB REQUEST \_ STATUS

Especifica o status de uma solicitação assíncrona. Essa enumeração é usada com o [**método IConnectionBrokerRequest::CheckStatus.**](iconnectionbrokerrequest-checkstatus.md)

## <a name="syntax"></a>Syntax


```C++
typedef enum _CB_REQUEST_STATUS { 
  CB_STATUS_INVALID                     = 1,
  CB_STATUS_INITIATING_REQUEST          = 0,
  CB_STATUS_REQUEST_COMPLETED,
  CB_STATUS_REQUEST_FAILED,
  CB_STATUS_REQUEST_ABORTED,
  CB_STATUS_FINDING_DESTINATION,
  CB_STATUS_LOADING_DESTINATION,
  CB_STATUS_BRINGING_SESSION_ONLINE,
  CB_STATUS_REDIRECTING_TO_DESTINATION
} CB_REQUEST_STATUS;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="CB_STATUS_INVALID"></span><span id="cb_status_invalid"></span>**STATUS \_ DO CB \_ INVÁLIDO**
</dt> <dd>

O objeto de solicitação não é inicializado.

</dd> <dt>

<span id="CB_STATUS_INITIATING_REQUEST"></span><span id="cb_status_initiating_request"></span>**SOLICITAÇÃO \_ DE INICIALIZAÇÃO DO STATUS \_ \_ CB**
</dt> <dd>

Não usado.

</dd> <dt>

<span id="CB_STATUS_REQUEST_COMPLETED"></span><span id="cb_status_request_completed"></span>**SOLICITAÇÃO \_ DE STATUS CB \_ \_ CONCLUÍDA**
</dt> <dd>

A solicitação foi concluída.

</dd> <dt>

<span id="CB_STATUS_REQUEST_FAILED"></span><span id="cb_status_request_failed"></span>**FALHA NA \_ SOLICITAÇÃO DE STATUS \_ DO \_ CB**
</dt> <dd>

A solicitação falhou.

</dd> <dt>

<span id="CB_STATUS_REQUEST_ABORTED"></span><span id="cb_status_request_aborted"></span>**SOLICITAÇÃO \_ DE STATUS CB \_ \_ ANULADA**
</dt> <dd>

A solicitação foi anulada.

</dd> <dt>

<span id="CB_STATUS_FINDING_DESTINATION"></span><span id="cb_status_finding_destination"></span>**DESTINO DE \_ LOCALIZAR STATUS \_ DO \_ CB**
</dt> <dd>

Não usado.

</dd> <dt>

<span id="CB_STATUS_LOADING_DESTINATION"></span><span id="cb_status_loading_destination"></span>**DESTINO DE \_ CARREGAMENTO DO STATUS DO \_ \_ CB**
</dt> <dd>

Não usado.

</dd> <dt>

<span id="CB_STATUS_BRINGING_SESSION_ONLINE"></span><span id="cb_status_bringing_session_online"></span>**STATUS \_ DO CB COLOCAR A SESSÃO \_ \_ \_ ONLINE**
</dt> <dd>

Não usado.

</dd> <dt>

<span id="CB_STATUS_REDIRECTING_TO_DESTINATION"></span><span id="cb_status_redirecting_to_destination"></span>**REDIRECIONAMENTO \_ DE STATUS CB PARA \_ \_ \_ DESTINO**
</dt> <dd>

Não usado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                        |
| Cabeçalho<br/>                   | <dl> <dt>Cbclient.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IConnectionBrokerRequest::CheckStatus**](iconnectionbrokerrequest-checkstatus.md)
</dt> </dl>

 

 





