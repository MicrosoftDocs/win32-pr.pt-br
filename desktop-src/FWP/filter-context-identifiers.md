---
title: Identificadores de contexto de filtro (Fwpmu. h)
description: Identificadores para os contextos de filtro que são internos à plataforma de filtragem do Windows.
ms.assetid: bcfae832-5386-43c5-b916-89577765ee5d
topic_type:
- apiref
api_name:
- FWPM_CONTEXT_IPSEC_INBOUND_PASSTHRU, FWPM_CONTEXT_IPSEC_INBOUND_PERSIST_CONNECTION_SECURITY, FWPM_CONTEXT_IPSEC_INBOUND_RESERVED
- FWPM_CONTEXT_IPSEC_OUTBOUND_NEGOTIATE_DISCOVER, FWPM_CONTEXT_IPSEC_OUTBOUND_SUPPRESS_NEGOTIATION
- FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_SECURITY, FWPM_CONTEXT_ALE_SET_CONNECTION_LAZY_SD_EVALUATION
- FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_ENCRYPTION, FWPM_CONTEXT_ALE_SET_CONNECTION_ALLOW_FIRST_INBOUND_PKT_UNENCRYPTED, FWPM_CONTEXT_ALE_ALLOW_AUTH_FW
- FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_ENABLE, FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_DISABLE
- FWPM_CONTEXT_RPC_AUDIT_ENABLED
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c09968f1ab68016405f22460409e83cfd826b716
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105787539"
---
# <a name="filter-context-identifiers"></a>Identificadores de contexto de filtro

Os identificadores para os contextos de filtro que são internos à plataforma de filtragem do Windows são definidos da seguinte maneira.

<dl> <dt>

<span id="FWPM_CONTEXT_IPSEC_INBOUND_PASSTHRU__FWPM_CONTEXT_IPSEC_INBOUND_PERSIST_CONNECTION_SECURITY___FWPM_CONTEXT_IPSEC_INBOUND_RESERVED"></span><span id="fwpm_context_ipsec_inbound_passthru__fwpm_context_ipsec_inbound_persist_connection_security___fwpm_context_ipsec_inbound_reserved"></span>**FWPM \_ \_ de contexto IPSec \_ de entrada de IP \_ , contexto de FWPM de \_ saída de \_ \_ \_ persistência de IPSec de entrada, segurança do contexto \_ \_ de FWPM de entrada \_ \_ \_ \_ reservado**
</dt> <dd> <dl> <dt>



Contextos de filtro de transporte IPsec na camada de entrada.


</dt> </dl> </dd> <dt>

<span id="FWPM_CONTEXT_IPSEC_OUTBOUND_NEGOTIATE_DISCOVER__FWPM_CONTEXT_IPSEC_OUTBOUND_SUPPRESS_NEGOTIATION"></span><span id="fwpm_context_ipsec_outbound_negotiate_discover__fwpm_context_ipsec_outbound_suppress_negotiation"></span>**\_ \_ \_ \_ \_ descoberta de negociação de saída IPSec de contexto de FWPM, contexto de FWPM \_ \_ IPSec \_ \_ suprimir negociação de saída \_**
</dt> <dd> <dl> <dt>



Contextos de filtro de transporte IPsec na camada de saída.

> [!Note]  
> Para o Windows 7, use a **\_ negociação de \_ \_ \_ supressão \_ de saída IPSec de contexto FWPM**.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_SECURITY__FWPM_CONTEXT_ALE_SET_CONNECTION_LAZY_SD_EVALUATION"></span><span id="fwpm_context_ale_set_connection_require_ipsec_security__fwpm_context_ale_set_connection_lazy_sd_evaluation"></span>**\_ \_ \_ conexão de definição de \_ Ale \_ de contexto de FWPM requer \_ \_ segurança IPSec, contexto de FWPM \_ \_ Ale \_ set \_ Connection \_ \_ avaliação de SD lenta \_**
</dt> <dd> <dl> <dt>



Contextos de filtro usados na camada de conexão ALE.


</dt> </dl> </dd> <dt>

<span id="FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_ENCRYPTION__FWPM_CONTEXT_ALE_SET_CONNECTION_ALLOW_FIRST_INBOUND_PKT_UNENCRYPTED__FWPM_CONTEXT_ALE_ALLOW_AUTH_FW"></span><span id="fwpm_context_ale_set_connection_require_ipsec_encryption__fwpm_context_ale_set_connection_allow_first_inbound_pkt_unencrypted__fwpm_context_ale_allow_auth_fw"></span>**\_conexão do \_ conjunto de Ale de contexto FWPM \_ \_ \_ requer \_ \_ criptografia IPSec, FWPM \_ contexto \_ Ale \_ set \_ conexão \_ permitir \_ primeiro \_ entrada não \_ \_ criptografada, FWPM \_ contexto \_ Ale \_ permitir \_ autenticação \_ FW**
</dt> <dd> <dl> <dt>



Contextos de filtro usados na camada de conexão ou de aceitação ALE.

> [!Note]  
> Para o Windows 7, use a **\_ Ale de contexto FWPM \_ \_ definir \_ conexão permitir a \_ \_ primeira \_ entrada não \_ \_ criptografada** ou a **Ale de contexto de FWPM \_ \_ \_ permitir \_ autenticação \_ FW**.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_ENABLE__FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_DISABLE"></span><span id="fwpm_context_tcp_chimney_offload_enable__fwpm_context_tcp_chimney_offload_disable"></span>**\_ \_ \_ \_ habilitar descarregamento de Chimney TCP \_ de contexto de FWPM, contexto de FWPM \_ \_ TCP \_ Chimney \_ descarregamento \_**
</dt> <dd> <dl> <dt>



Contextos usados pelos textos explicativos de descarga TCP Chimney.


</dt> </dl> </dd> <dt>

<span id="FWPM_CONTEXT_RPC_AUDIT_ENABLED"></span><span id="fwpm_context_rpc_audit_enabled"></span>**\_auditoria de RPC de contexto FWPM \_ \_ \_ habilitada**
</dt> <dd> <dl> <dt>



Contextos usados na subcamada de auditoria RPC.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Fwpmu. h</dt> </dl> |



 

 





