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
# <a name="filter-context-identifiers"></a><span data-ttu-id="bde36-103">Identificadores de contexto de filtro</span><span class="sxs-lookup"><span data-stu-id="bde36-103">Filter Context Identifiers</span></span>

<span data-ttu-id="bde36-104">Os identificadores para os contextos de filtro que são internos à plataforma de filtragem do Windows são definidos da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="bde36-104">The identifiers for the filter contexts that are built in to the Windows Filtering Platform are defined as follows.</span></span>

<dl> <dt>

<span data-ttu-id="bde36-105"><span id="FWPM_CONTEXT_IPSEC_INBOUND_PASSTHRU__FWPM_CONTEXT_IPSEC_INBOUND_PERSIST_CONNECTION_SECURITY___FWPM_CONTEXT_IPSEC_INBOUND_RESERVED"></span><span id="fwpm_context_ipsec_inbound_passthru__fwpm_context_ipsec_inbound_persist_connection_security___fwpm_context_ipsec_inbound_reserved"></span>**FWPM \_ \_ de contexto IPSec \_ de entrada de IP \_ , contexto de FWPM de \_ saída de \_ \_ \_ persistência de IPSec de entrada, segurança do contexto \_ \_ de FWPM de entrada \_ \_ \_ \_ reservado**</span><span class="sxs-lookup"><span data-stu-id="bde36-105"><span id="FWPM_CONTEXT_IPSEC_INBOUND_PASSTHRU__FWPM_CONTEXT_IPSEC_INBOUND_PERSIST_CONNECTION_SECURITY___FWPM_CONTEXT_IPSEC_INBOUND_RESERVED"></span><span id="fwpm_context_ipsec_inbound_passthru__fwpm_context_ipsec_inbound_persist_connection_security___fwpm_context_ipsec_inbound_reserved"></span>**FWPM\_CONTEXT\_IPSEC\_INBOUND\_PASSTHRU, FWPM\_CONTEXT\_IPSEC\_INBOUND\_PERSIST\_CONNECTION\_SECURITY, FWPM\_CONTEXT\_IPSEC\_INBOUND\_RESERVED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bde36-106">Contextos de filtro de transporte IPsec na camada de entrada.</span><span class="sxs-lookup"><span data-stu-id="bde36-106">IPsec transport filter contexts in inbound layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bde36-107"><span id="FWPM_CONTEXT_IPSEC_OUTBOUND_NEGOTIATE_DISCOVER__FWPM_CONTEXT_IPSEC_OUTBOUND_SUPPRESS_NEGOTIATION"></span><span id="fwpm_context_ipsec_outbound_negotiate_discover__fwpm_context_ipsec_outbound_suppress_negotiation"></span>**\_ \_ \_ \_ \_ descoberta de negociação de saída IPSec de contexto de FWPM, contexto de FWPM \_ \_ IPSec \_ \_ suprimir negociação de saída \_**</span><span class="sxs-lookup"><span data-stu-id="bde36-107"><span id="FWPM_CONTEXT_IPSEC_OUTBOUND_NEGOTIATE_DISCOVER__FWPM_CONTEXT_IPSEC_OUTBOUND_SUPPRESS_NEGOTIATION"></span><span id="fwpm_context_ipsec_outbound_negotiate_discover__fwpm_context_ipsec_outbound_suppress_negotiation"></span>**FWPM\_CONTEXT\_IPSEC\_OUTBOUND\_NEGOTIATE\_DISCOVER, FWPM\_CONTEXT\_IPSEC\_OUTBOUND\_SUPPRESS\_NEGOTIATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bde36-108">Contextos de filtro de transporte IPsec na camada de saída.</span><span class="sxs-lookup"><span data-stu-id="bde36-108">IPsec transport filter contexts in outbound layer.</span></span>

> [!Note]  
> <span data-ttu-id="bde36-109">Para o Windows 7, use a **\_ negociação de \_ \_ \_ supressão \_ de saída IPSec de contexto FWPM**.</span><span class="sxs-lookup"><span data-stu-id="bde36-109">For Windows 7, use **FWPM\_CONTEXT\_IPSEC\_OUTBOUND\_SUPPRESS\_NEGOTIATION**.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="bde36-110"><span id="FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_SECURITY__FWPM_CONTEXT_ALE_SET_CONNECTION_LAZY_SD_EVALUATION"></span><span id="fwpm_context_ale_set_connection_require_ipsec_security__fwpm_context_ale_set_connection_lazy_sd_evaluation"></span>**\_ \_ \_ conexão de definição de \_ Ale \_ de contexto de FWPM requer \_ \_ segurança IPSec, contexto de FWPM \_ \_ Ale \_ set \_ Connection \_ \_ avaliação de SD lenta \_**</span><span class="sxs-lookup"><span data-stu-id="bde36-110"><span id="FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_SECURITY__FWPM_CONTEXT_ALE_SET_CONNECTION_LAZY_SD_EVALUATION"></span><span id="fwpm_context_ale_set_connection_require_ipsec_security__fwpm_context_ale_set_connection_lazy_sd_evaluation"></span>**FWPM\_CONTEXT\_ALE\_SET\_CONNECTION\_REQUIRE\_IPSEC\_SECURITY, FWPM\_CONTEXT\_ALE\_SET\_CONNECTION\_LAZY\_SD\_EVALUATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bde36-111">Contextos de filtro usados na camada de conexão ALE.</span><span class="sxs-lookup"><span data-stu-id="bde36-111">Filter contexts used in the ALE connect layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bde36-112"><span id="FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_ENCRYPTION__FWPM_CONTEXT_ALE_SET_CONNECTION_ALLOW_FIRST_INBOUND_PKT_UNENCRYPTED__FWPM_CONTEXT_ALE_ALLOW_AUTH_FW"></span><span id="fwpm_context_ale_set_connection_require_ipsec_encryption__fwpm_context_ale_set_connection_allow_first_inbound_pkt_unencrypted__fwpm_context_ale_allow_auth_fw"></span>**\_conexão do \_ conjunto de Ale de contexto FWPM \_ \_ \_ requer \_ \_ criptografia IPSec, FWPM \_ contexto \_ Ale \_ set \_ conexão \_ permitir \_ primeiro \_ entrada não \_ \_ criptografada, FWPM \_ contexto \_ Ale \_ permitir \_ autenticação \_ FW**</span><span class="sxs-lookup"><span data-stu-id="bde36-112"><span id="FWPM_CONTEXT_ALE_SET_CONNECTION_REQUIRE_IPSEC_ENCRYPTION__FWPM_CONTEXT_ALE_SET_CONNECTION_ALLOW_FIRST_INBOUND_PKT_UNENCRYPTED__FWPM_CONTEXT_ALE_ALLOW_AUTH_FW"></span><span id="fwpm_context_ale_set_connection_require_ipsec_encryption__fwpm_context_ale_set_connection_allow_first_inbound_pkt_unencrypted__fwpm_context_ale_allow_auth_fw"></span>**FWPM\_CONTEXT\_ALE\_SET\_CONNECTION\_REQUIRE\_IPSEC\_ENCRYPTION, FWPM\_CONTEXT\_ALE\_SET\_CONNECTION\_ALLOW\_FIRST\_INBOUND\_PKT\_UNENCRYPTED, FWPM\_CONTEXT\_ALE\_ALLOW\_AUTH\_FW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bde36-113">Contextos de filtro usados na camada de conexão ou de aceitação ALE.</span><span class="sxs-lookup"><span data-stu-id="bde36-113">Filter contexts used in the ALE connect or accept layer.</span></span>

> [!Note]  
> <span data-ttu-id="bde36-114">Para o Windows 7, use a **\_ Ale de contexto FWPM \_ \_ definir \_ conexão permitir a \_ \_ primeira \_ entrada não \_ \_ criptografada** ou a **Ale de contexto de FWPM \_ \_ \_ permitir \_ autenticação \_ FW**.</span><span class="sxs-lookup"><span data-stu-id="bde36-114">For Windows 7, use **FWPM\_CONTEXT\_ALE\_SET\_CONNECTION\_ALLOW\_FIRST\_INBOUND\_PKT\_UNENCRYPTED** or **FWPM\_CONTEXT\_ALE\_ALLOW\_AUTH\_FW**.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="bde36-115"><span id="FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_ENABLE__FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_DISABLE"></span><span id="fwpm_context_tcp_chimney_offload_enable__fwpm_context_tcp_chimney_offload_disable"></span>**\_ \_ \_ \_ habilitar descarregamento de Chimney TCP \_ de contexto de FWPM, contexto de FWPM \_ \_ TCP \_ Chimney \_ descarregamento \_**</span><span class="sxs-lookup"><span data-stu-id="bde36-115"><span id="FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_ENABLE__FWPM_CONTEXT_TCP_CHIMNEY_OFFLOAD_DISABLE"></span><span id="fwpm_context_tcp_chimney_offload_enable__fwpm_context_tcp_chimney_offload_disable"></span>**FWPM\_CONTEXT\_TCP\_CHIMNEY\_OFFLOAD\_ENABLE, FWPM\_CONTEXT\_TCP\_CHIMNEY\_OFFLOAD\_DISABLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bde36-116">Contextos usados pelos textos explicativos de descarga TCP Chimney.</span><span class="sxs-lookup"><span data-stu-id="bde36-116">Contexts used by the TCP Chimney Offload callouts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="bde36-117"><span id="FWPM_CONTEXT_RPC_AUDIT_ENABLED"></span><span id="fwpm_context_rpc_audit_enabled"></span>**\_auditoria de RPC de contexto FWPM \_ \_ \_ habilitada**</span><span class="sxs-lookup"><span data-stu-id="bde36-117"><span id="FWPM_CONTEXT_RPC_AUDIT_ENABLED"></span><span id="fwpm_context_rpc_audit_enabled"></span>**FWPM\_CONTEXT\_RPC\_AUDIT\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="bde36-118">Contextos usados na subcamada de auditoria RPC.</span><span class="sxs-lookup"><span data-stu-id="bde36-118">Contexts used in the RPC audit sublayer.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bde36-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bde36-119">Requirements</span></span>



| <span data-ttu-id="bde36-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="bde36-120">Requirement</span></span> | <span data-ttu-id="bde36-121">Valor</span><span class="sxs-lookup"><span data-stu-id="bde36-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bde36-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bde36-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bde36-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bde36-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="bde36-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bde36-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bde36-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bde36-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="bde36-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bde36-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="bde36-127"><dt>Fwpmu. h</dt></span><span class="sxs-lookup"><span data-stu-id="bde36-127"><dt>Fwpmu.h</dt></span></span> </dl> |



 

 





