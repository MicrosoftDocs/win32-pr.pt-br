---
title: Enumeração de CB_REQUEST_STATUS (Cbclient. h)
description: Especifica o status de uma solicitação assíncrona.
ms.assetid: 35FAC8EA-BA17-405F-AE10-33A816029F62
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de enumeração de CB_REQUEST_STATUS
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
ms.openlocfilehash: cd57efd12d3fb5c708d5c4861ee144543bb49f6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104294791"
---
# <a name="cb_request_status-enumeration"></a>Enumeração de status de \_ solicitação CB \_

Especifica o status de uma solicitação assíncrona. Essa enumeração é usada com o método [**IConnectionBrokerRequest:: CheckStatus**](iconnectionbrokerrequest-checkstatus.md) .

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

<span id="CB_STATUS_INVALID"></span><span id="cb_status_invalid"></span>**STATUS de CB \_ \_ inválido**
</dt> <dd>

O objeto de solicitação não foi inicializado.

</dd> <dt>

<span id="CB_STATUS_INITIATING_REQUEST"></span><span id="cb_status_initiating_request"></span>**\_solicitação de \_ início do status CB \_**
</dt> <dd>

Não usado.

</dd> <dt>

<span id="CB_STATUS_REQUEST_COMPLETED"></span><span id="cb_status_request_completed"></span>**\_solicitação de status CB \_ \_ concluída**
</dt> <dd>

A solicitação foi concluída.

</dd> <dt>

<span id="CB_STATUS_REQUEST_FAILED"></span><span id="cb_status_request_failed"></span>**\_ \_ falha na solicitação de status CB \_**
</dt> <dd>

A solicitação falhou.

</dd> <dt>

<span id="CB_STATUS_REQUEST_ABORTED"></span><span id="cb_status_request_aborted"></span>**\_solicitação de status CB \_ \_ anulada**
</dt> <dd>

A solicitação foi anulada.

</dd> <dt>

<span id="CB_STATUS_FINDING_DESTINATION"></span><span id="cb_status_finding_destination"></span>**STATUS do CB \_ \_ encontrando \_ destino**
</dt> <dd>

Não usado.

</dd> <dt>

<span id="CB_STATUS_LOADING_DESTINATION"></span><span id="cb_status_loading_destination"></span>**\_destino de \_ carregamento de status CB \_**
</dt> <dd>

Não usado.

</dd> <dt>

<span id="CB_STATUS_BRINGING_SESSION_ONLINE"></span><span id="cb_status_bringing_session_online"></span>**\_status CB \_ trazendo \_ sessão \_ online**
</dt> <dd>

Não usado.

</dd> <dt>

<span id="CB_STATUS_REDIRECTING_TO_DESTINATION"></span><span id="cb_status_redirecting_to_destination"></span>**\_ \_ redirecionamento de status CB \_ para \_ destino**
</dt> <dd>

Não usado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                        |
| parâmetro<br/>                   | <dl> <dt>Cbclient. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IConnectionBrokerRequest:: CheckStatus**](iconnectionbrokerrequest-checkstatus.md)
</dt> </dl>

 

 





