---
title: Filtrando identificadores de subcamadas (Fwpmu. h)
description: As constantes de identificador de subcamadas para filtragem de gerenciamento de API WFP.
ms.assetid: 4c8dbe35-e84b-4490-bf7a-7ff8b94e2022
topic_type:
- apiref
api_name:
- FWPM_SUBLAYER_EDGE_TRAVERSAL / FWPM_SUBLAYER_TEREDO
- FWPM_SUBLAYER_INSPECTION
- FWPM_SUBLAYER_IPSEC_DOSP
- FWPM_SUBLAYER_IPSEC_FORWARD_OUTBOUND_TUNNEL
- FWPM_SUBLAYER_IPSEC_TUNNEL
- FWPM_SUBLAYER_LIPS
- FWPM_SUBLAYER_RPC_AUDIT
- FWPM_SUBLAYER_SECURE_SOCKET
- FWPM_SUBLAYER_TCP_CHIMNEY_OFFLOAD
- FWPM_SUBLAYER_TCP_TEMPLATES
- FWPM_SUBLAYER_UNIVERSAL
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e015d590c19395987bbd47d1c3c4b918296ab5f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824658"
---
# <a name="filtering-sublayer-identifiers"></a><span data-ttu-id="5df25-103">Filtrando identificadores de subcamadas</span><span class="sxs-lookup"><span data-stu-id="5df25-103">Filtering Sublayer Identifiers</span></span>

<span data-ttu-id="5df25-104">Os identificadores de subcamadas da WFP (plataforma de filtragem do Windows) são representados por um GUID.</span><span class="sxs-lookup"><span data-stu-id="5df25-104">The Windows Filtering Platform (WFP) sublayer identifiers are each represented by a GUID.</span></span>

<span data-ttu-id="5df25-105">Esses identificadores são definidos da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="5df25-105">These identifiers are defined as follows.</span></span>

<dl> <dt>

<span data-ttu-id="5df25-106"><span id="FWPM_SUBLAYER_EDGE_TRAVERSAL________________________FWPM_SUBLAYER_TEREDO"></span><span id="fwpm_sublayer_edge_traversal________________________fwpm_sublayer_teredo"></span>**FWPM de \_ borda de SUBcamadas \_ \_ /FWPM \_ \_ TEREDO**</span><span class="sxs-lookup"><span data-stu-id="5df25-106"><span id="FWPM_SUBLAYER_EDGE_TRAVERSAL________________________FWPM_SUBLAYER_TEREDO"></span><span id="fwpm_sublayer_edge_traversal________________________fwpm_sublayer_teredo"></span>**FWPM\_SUBLAYER\_EDGE\_TRAVERSAL / FWPM\_SUBLAYER\_TEREDO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5df25-107">Os filtros de percurso de borda são adicionados a essa subcamada.</span><span class="sxs-lookup"><span data-stu-id="5df25-107">Edge traversal filters are added to this sublayer.</span></span>

> [!Note]  
> <span data-ttu-id="5df25-108">Para o Windows 7 e posterior, use a **\_ travessia de \_ borda \_ da subcamada FWPM**.</span><span class="sxs-lookup"><span data-stu-id="5df25-108">For Windows 7 and later, use **FWPM\_SUBLAYER\_EDGE\_TRAVERSAL**.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="5df25-109"><span id="FWPM_SUBLAYER_INSPECTION"></span><span id="fwpm_sublayer_inspection"></span>**\_inspeção de SUBcamada FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="5df25-109"><span id="FWPM_SUBLAYER_INSPECTION"></span><span id="fwpm_sublayer_inspection"></span>**FWPM\_SUBLAYER\_INSPECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5df25-110">Esta é a subcamada com o menor peso.</span><span class="sxs-lookup"><span data-stu-id="5df25-110">This is the lowest weighted sublayer.</span></span> <span data-ttu-id="5df25-111">Ele é usado somente para filtros de inspeção.</span><span class="sxs-lookup"><span data-stu-id="5df25-111">It is used only for inspection filters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5df25-112"><span id="FWPM_SUBLAYER_IPSEC_DOSP"></span><span id="fwpm_sublayer_ipsec_dosp"></span>**FWPM \_ DOSP IPSec SUBcamada \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5df25-112"><span id="FWPM_SUBLAYER_IPSEC_DOSP"></span><span id="fwpm_sublayer_ipsec_dosp"></span>**FWPM\_SUBLAYER\_IPSEC\_DOSP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5df25-113">Os filtros de proteção de DoS IPsec são adicionados a essa subcamada.</span><span class="sxs-lookup"><span data-stu-id="5df25-113">IPsec DoS Protection filters are added to this sublayer.</span></span>

> [!Note]  
> <span data-ttu-id="5df25-114">Disponível apenas no Windows Vista com SP1, Windows Server 2008 e posterior.</span><span class="sxs-lookup"><span data-stu-id="5df25-114">Available only on Windows Vista with SP1, Windows Server 2008, and later.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="5df25-115"><span id="FWPM_SUBLAYER_IPSEC_FORWARD_OUTBOUND_TUNNEL"></span><span id="fwpm_sublayer_ipsec_forward_outbound_tunnel"></span>**\_túnel de saída de \_ \_ encaminhamento IPsec do FWPM \_ subcamada \_**</span><span class="sxs-lookup"><span data-stu-id="5df25-115"><span id="FWPM_SUBLAYER_IPSEC_FORWARD_OUTBOUND_TUNNEL"></span><span id="fwpm_sublayer_ipsec_forward_outbound_tunnel"></span>**FWPM\_SUBLAYER\_IPSEC\_FORWARD\_OUTBOUND\_TUNNEL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5df25-116">Os filtros de túnel de saída de encaminhamento IPsec são adicionados a essa subcamada.</span><span class="sxs-lookup"><span data-stu-id="5df25-116">IPsec forward outbound tunnel filters are added to this sublayer.</span></span>

> [!Note]  
> <span data-ttu-id="5df25-117">Disponível apenas no Windows 7, Windows Server 2008 R2 e posterior.</span><span class="sxs-lookup"><span data-stu-id="5df25-117">Available only on Windows 7, Windows Server 2008 R2, and later.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="5df25-118"><span id="FWPM_SUBLAYER_IPSEC_TUNNEL"></span><span id="fwpm_sublayer_ipsec_tunnel"></span>**\_túnel IPSec de SUBcamada FWPM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5df25-118"><span id="FWPM_SUBLAYER_IPSEC_TUNNEL"></span><span id="fwpm_sublayer_ipsec_tunnel"></span>**FWPM\_SUBLAYER\_IPSEC\_TUNNEL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5df25-119">Os filtros de túnel IPsec são adicionados a essa subcamada.</span><span class="sxs-lookup"><span data-stu-id="5df25-119">IPsec tunnel filters are added to this sublayer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5df25-120"><span id="FWPM_SUBLAYER_LIPS"></span><span id="fwpm_sublayer_lips"></span>**\_Lips de SUBcamadas FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="5df25-120"><span id="FWPM_SUBLAYER_LIPS"></span><span id="fwpm_sublayer_lips"></span>**FWPM\_SUBLAYER\_LIPS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5df25-121">Os filtros IPsec herdados são adicionados a essa subcamada.</span><span class="sxs-lookup"><span data-stu-id="5df25-121">Legacy IPsec filters are added to this sublayer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5df25-122"><span id="FWPM_SUBLAYER_RPC_AUDIT"></span><span id="fwpm_sublayer_rpc_audit"></span>**\_auditoria de RPC da SUBcamada FWPM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5df25-122"><span id="FWPM_SUBLAYER_RPC_AUDIT"></span><span id="fwpm_sublayer_rpc_audit"></span>**FWPM\_SUBLAYER\_RPC\_AUDIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5df25-123">Os filtros de auditoria RPC são adicionados a essa subcamada.</span><span class="sxs-lookup"><span data-stu-id="5df25-123">RPC audit filters are added to this sublayer.</span></span> <span data-ttu-id="5df25-124">Esses filtros auditam chamadas de entrada RPC como parte do C2 e da conformidade dos critérios comuns.</span><span class="sxs-lookup"><span data-stu-id="5df25-124">These filters audit RPC incoming calls as part of C2 and common criteria compliance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5df25-125"><span id="FWPM_SUBLAYER_SECURE_SOCKET"></span><span id="fwpm_sublayer_secure_socket"></span>**\_soquete seguro de SUBcamada FWPM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5df25-125"><span id="FWPM_SUBLAYER_SECURE_SOCKET"></span><span id="fwpm_sublayer_secure_socket"></span>**FWPM\_SUBLAYER\_SECURE\_SOCKET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5df25-126">Os filtros de soquete seguro são adicionados a essa subcamada.</span><span class="sxs-lookup"><span data-stu-id="5df25-126">Secure socket filters are added to this sublayer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5df25-127"><span id="FWPM_SUBLAYER_TCP_CHIMNEY_OFFLOAD"></span><span id="fwpm_sublayer_tcp_chimney_offload"></span>**descarregamento de CHIMNEY TCP de FWPM de \_ SUBcamadas \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5df25-127"><span id="FWPM_SUBLAYER_TCP_CHIMNEY_OFFLOAD"></span><span id="fwpm_sublayer_tcp_chimney_offload"></span>**FWPM\_SUBLAYER\_TCP\_CHIMNEY\_OFFLOAD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5df25-128">Os filtros de descarregamento TCP Chimney são adicionados a essa subcamada.</span><span class="sxs-lookup"><span data-stu-id="5df25-128">TCP Chimney Offload filters are added to this sublayer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5df25-129"><span id="FWPM_SUBLAYER_TCP_TEMPLATES______________________"></span><span id="fwpm_sublayer_tcp_templates______________________"></span>**\_modelos TCP de SUBcamadas FWPM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5df25-129"><span id="FWPM_SUBLAYER_TCP_TEMPLATES______________________"></span><span id="fwpm_sublayer_tcp_templates______________________"></span>**FWPM\_SUBLAYER\_TCP\_TEMPLATES**</span></span> 
</dt> <dd> <dl> <dt>



<span data-ttu-id="5df25-130">Os filtros de modelo TCP são adicionados a essa subcamada.</span><span class="sxs-lookup"><span data-stu-id="5df25-130">TCP template filters are added to this sublayer.</span></span>

> [!Note]  
> <span data-ttu-id="5df25-131">Disponível somente no Windows 8, Windows Server 2012 e posterior.</span><span class="sxs-lookup"><span data-stu-id="5df25-131">Available only on Windows 8, Windows Server 2012, and later.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="5df25-132"><span id="FWPM_SUBLAYER_UNIVERSAL"></span><span id="fwpm_sublayer_universal"></span>**FWPM de \_ SUBcamamento \_ Universal**</span><span class="sxs-lookup"><span data-stu-id="5df25-132"><span id="FWPM_SUBLAYER_UNIVERSAL"></span><span id="fwpm_sublayer_universal"></span>**FWPM\_SUBLAYER\_UNIVERSAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5df25-133">Essa subcamada hospeda todos os filtros que não estão atribuídos a nenhuma das outras subcamadas.</span><span class="sxs-lookup"><span data-stu-id="5df25-133">This sublayer hosts all filters that are not assigned to any of the other sublayers.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5df25-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5df25-134">Requirements</span></span>



| <span data-ttu-id="5df25-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="5df25-135">Requirement</span></span> | <span data-ttu-id="5df25-136">Valor</span><span class="sxs-lookup"><span data-stu-id="5df25-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5df25-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5df25-137">Minimum supported client</span></span><br/> | <span data-ttu-id="5df25-138">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5df25-138">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5df25-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5df25-139">Minimum supported server</span></span><br/> | <span data-ttu-id="5df25-140">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5df25-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5df25-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5df25-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="5df25-142"><dt>Fwpmu. h</dt></span><span class="sxs-lookup"><span data-stu-id="5df25-142"><dt>Fwpmu.h</dt></span></span> </dl> |



 

 





