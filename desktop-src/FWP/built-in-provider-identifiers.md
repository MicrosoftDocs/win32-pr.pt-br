---
title: Identificadores de provedor interno (Fwpmu. h)
description: Os identificadores para os provedores que são internos para a WFP (Windows Filtering Platform) são representados por um GUID.
ms.assetid: 61bc1e2d-f6ee-45db-892f-c49680d27072
topic_type:
- apiref
api_name:
- FWPM_PROVIDER_IKEEXT
- FWPM_PROVIDER_IPSEC_DOS_CONFIG
- FWPM_PROVIDER_TCP_CHIMNEY_OFFLOAD
- FWPM_PROVIDER_TCP_TEMPLATES
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 060f6d63d703d7c91e5538b7bfdd8758ee2e1cde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753485"
---
# <a name="built-in-provider-identifiers"></a><span data-ttu-id="ce2aa-103">Identificadores de provedor internos</span><span class="sxs-lookup"><span data-stu-id="ce2aa-103">Built-in Provider Identifiers</span></span>

<span data-ttu-id="ce2aa-104">Os identificadores para os provedores que são internos para a WFP (Windows Filtering Platform) são representados por um GUID.</span><span class="sxs-lookup"><span data-stu-id="ce2aa-104">The identifiers for the providers that are built in to the Windows Filtering Platform (WFP) are each represented by a GUID.</span></span>

<span data-ttu-id="ce2aa-105">Esses identificadores são definidos da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="ce2aa-105">These identifiers are defined as follows.</span></span>

<dl> <dt>

<span data-ttu-id="ce2aa-106"><span id="FWPM_PROVIDER_IKEEXT"></span><span id="fwpm_provider_ikeext"></span>**provedor de FWPM \_ \_ IKEEXT**</span><span class="sxs-lookup"><span data-stu-id="ce2aa-106"><span id="FWPM_PROVIDER_IKEEXT"></span><span id="fwpm_provider_ikeext"></span>**FWPM\_PROVIDER\_IKEEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce2aa-107">{10ad9216-ccde-456c-8b16-e9f04e60a90b}</span><span class="sxs-lookup"><span data-stu-id="ce2aa-107">{10ad9216-ccde-456c-8b16-e9f04e60a90b}</span></span>
</dt> <dt>



<span data-ttu-id="ce2aa-108">Usado para identificar todos os filtros adicionados por IKE/AuthIP.</span><span class="sxs-lookup"><span data-stu-id="ce2aa-108">Used to identify all the filters added by IKE/AuthIP.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce2aa-109"><span id="FWPM_PROVIDER_IPSEC_DOS_CONFIG"></span><span id="fwpm_provider_ipsec_dos_config"></span>**configuração de dos do provedor de FWPM \_ \_ IPSec \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ce2aa-109"><span id="FWPM_PROVIDER_IPSEC_DOS_CONFIG"></span><span id="fwpm_provider_ipsec_dos_config"></span>**FWPM\_PROVIDER\_IPSEC\_DOS\_CONFIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce2aa-110">{3c6c0519-c05c-4bb9-8338-2327814ce8bf}</span><span class="sxs-lookup"><span data-stu-id="ce2aa-110">{3c6c0519-c05c-4bb9-8338-2327814ce8bf}</span></span>
</dt> <dt>



<span data-ttu-id="ce2aa-111">Usado para identificar todos os filtros adicionados pela proteção de DoS IPsec.</span><span class="sxs-lookup"><span data-stu-id="ce2aa-111">Used to identify all the filters added by IPsec DoS Protection.</span></span>

> [!Note]  
> <span data-ttu-id="ce2aa-112">Disponível apenas no Windows 7 e no Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="ce2aa-112">Available only on Windows 7 and Windows Server 2008 R2.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce2aa-113"><span id="FWPM_PROVIDER_TCP_CHIMNEY_OFFLOAD"></span><span id="fwpm_provider_tcp_chimney_offload"></span>**\_descarregamento \_ de \_ CHIMNEY \_ TCP do provedor FWPM**</span><span class="sxs-lookup"><span data-stu-id="ce2aa-113"><span id="FWPM_PROVIDER_TCP_CHIMNEY_OFFLOAD"></span><span id="fwpm_provider_tcp_chimney_offload"></span>**FWPM\_PROVIDER\_TCP\_CHIMNEY\_OFFLOAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce2aa-114">{896aa19e-9a34-4bcb-ae79-beb9127c84b9}</span><span class="sxs-lookup"><span data-stu-id="ce2aa-114">{896aa19e-9a34-4bcb-ae79-beb9127c84b9}</span></span>
</dt> <dt>



<span data-ttu-id="ce2aa-115">Usado para identificar todos os filtros adicionados pelo descarregamento de Chimney TCP.</span><span class="sxs-lookup"><span data-stu-id="ce2aa-115">Used to identify all the filters added by TCP Chimney Offload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ce2aa-116"><span id="FWPM_PROVIDER_TCP_TEMPLATES"></span><span id="fwpm_provider_tcp_templates"></span>**\_modelos de \_ TCP do provedor de FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="ce2aa-116"><span id="FWPM_PROVIDER_TCP_TEMPLATES"></span><span id="fwpm_provider_tcp_templates"></span>**FWPM\_PROVIDER\_TCP\_TEMPLATES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ce2aa-117">{76cfcd30-3394-432d-bed3-441ae50e63c3}</span><span class="sxs-lookup"><span data-stu-id="ce2aa-117">{76cfcd30-3394-432d-bed3-441ae50e63c3}</span></span>
</dt> <dt>



<span data-ttu-id="ce2aa-118">Usado para identificar todos os filtros adicionados por modelos TCP.</span><span class="sxs-lookup"><span data-stu-id="ce2aa-118">Used to identify all the filters added by TCP templates.</span></span>

> [!Note]  
> <span data-ttu-id="ce2aa-119">Disponível somente no Windows 8 e no Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="ce2aa-119">Available only on Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ce2aa-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce2aa-120">Requirements</span></span>



| <span data-ttu-id="ce2aa-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce2aa-121">Requirement</span></span> | <span data-ttu-id="ce2aa-122">Valor</span><span class="sxs-lookup"><span data-stu-id="ce2aa-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ce2aa-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ce2aa-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ce2aa-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ce2aa-124">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ce2aa-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ce2aa-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ce2aa-126">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ce2aa-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ce2aa-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ce2aa-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce2aa-128"><dt>Fwpmu. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce2aa-128"><dt>Fwpmu.h</dt></span></span> </dl> |



 

 





