---
title: Estrutura de IPX_SPECIFIC_DATA (RTM. h)
description: A \_ estrutura de dados específica de IPX \_ contém dados específicos de IPX.
ms.assetid: 4d97092d-692c-4dc7-af7f-260dc76c6c08
keywords:
- RAS da estrutura de IPX_SPECIFIC_DATA
- RAS de ponteiro de estrutura de PIPX_SPECIFIC_DATA
topic_type:
- apiref
api_name:
- IPX_SPECIFIC_DATA
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56badfb6149e416c71b447aca93564b5eb5aba7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103917958"
---
# <a name="ipx_specific_data-structure"></a><span data-ttu-id="9d57b-105">\_Estrutura de dados específica de IPX \_</span><span class="sxs-lookup"><span data-stu-id="9d57b-105">IPX\_SPECIFIC\_DATA structure</span></span>

<span data-ttu-id="9d57b-106">\[Essa API foi substituída pela API do [Gerenciador de tabela de roteamento versão 2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="9d57b-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="9d57b-107">Os aplicativos devem usar a API da versão 2 do Gerenciador de tabela de roteamento.\]</span><span class="sxs-lookup"><span data-stu-id="9d57b-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="9d57b-108">A estrutura de **\_ \_ dados específica de IPX** contém dados específicos de IPX.</span><span class="sxs-lookup"><span data-stu-id="9d57b-108">The **IPX\_SPECIFIC\_DATA** structure contains IPX-specific data.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d57b-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9d57b-109">Syntax</span></span>


```C++
typedef struct _IPX_SPECIFIC_DATA {
  DWORD  FSD_Flags;
  USHORT FSD_TickCount;
  USHORT FSD_HopCount;
} IPX_SPECIFIC_DATA, *PIPX_SPECIFIC_DATA;
```



## <a name="members"></a><span data-ttu-id="9d57b-110">Membros</span><span class="sxs-lookup"><span data-stu-id="9d57b-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="9d57b-111">**Sinalizadores de FSD \_**</span><span class="sxs-lookup"><span data-stu-id="9d57b-111">**FSD\_Flags**</span></span>
</dt> <dd>

<span data-ttu-id="9d57b-112">Especifica sinalizadores que descrevem a rota.</span><span class="sxs-lookup"><span data-stu-id="9d57b-112">Specifies flags that describe the route.</span></span> <span data-ttu-id="9d57b-113">Atualmente, esse membro é zero ou o seguinte valor de sinalizador.</span><span class="sxs-lookup"><span data-stu-id="9d57b-113">Currently, this member is either zero or the following flag value.</span></span>



| <span data-ttu-id="9d57b-114">Valor</span><span class="sxs-lookup"><span data-stu-id="9d57b-114">Value</span></span>                                                                                                                                                                                                      | <span data-ttu-id="9d57b-115">Significado</span><span class="sxs-lookup"><span data-stu-id="9d57b-115">Meaning</span></span>                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="IPX_GLOBAL_CLIENT_WAN_ROUTE"></span><span id="ipx_global_client_wan_route"></span><dl> <span data-ttu-id="9d57b-116"><dt>**\_rota de \_ WAN do cliente global \_ IPX \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9d57b-116"><dt>**IPX\_GLOBAL\_CLIENT\_WAN\_ROUTE**</dt></span></span> </dl> | <span data-ttu-id="9d57b-117">Especifica que essa rota é para a rede global alocada para todos os clientes WAN.</span><span class="sxs-lookup"><span data-stu-id="9d57b-117">Specifies that this route is for the global network allocated for all WAN clients.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9d57b-118">**FSD \_**</span><span class="sxs-lookup"><span data-stu-id="9d57b-118">**FSD\_TickCount**</span></span>
</dt> <dd>

<span data-ttu-id="9d57b-119">Especifica o número de tiques que leva para alcançar a rede de destino.</span><span class="sxs-lookup"><span data-stu-id="9d57b-119">Specifies the number of ticks it takes to reach the destination network.</span></span> <span data-ttu-id="9d57b-120">Protocolos de roteamento diferentes do RIP devem converter suas métricas em tiques.</span><span class="sxs-lookup"><span data-stu-id="9d57b-120">Routing protocols other than RIP should convert their metrics into ticks.</span></span>

</dd> <dt>

<span data-ttu-id="9d57b-121">**FSD \_ HopCount**</span><span class="sxs-lookup"><span data-stu-id="9d57b-121">**FSD\_HopCount**</span></span>
</dt> <dd>

<span data-ttu-id="9d57b-122">Especifica a contagem de saltos associada à rota.</span><span class="sxs-lookup"><span data-stu-id="9d57b-122">Specifies the hop count associated with the route.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9d57b-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d57b-123">Requirements</span></span>



| <span data-ttu-id="9d57b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d57b-124">Requirement</span></span> | <span data-ttu-id="9d57b-125">Valor</span><span class="sxs-lookup"><span data-stu-id="9d57b-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9d57b-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9d57b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9d57b-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="9d57b-127">None supported</span></span><br/>                                                        |
| <span data-ttu-id="9d57b-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9d57b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9d57b-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9d57b-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9d57b-130">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="9d57b-130">End of server support</span></span><br/>    | <span data-ttu-id="9d57b-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9d57b-131">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="9d57b-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9d57b-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d57b-133"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d57b-133"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d57b-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="9d57b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d57b-135">Referência da versão 1 do Gerenciador de tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="9d57b-135">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="9d57b-136">Estruturas da versão 1 do Gerenciador de tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="9d57b-136">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="9d57b-137">**\_rota IPX do RTM \_**</span><span class="sxs-lookup"><span data-stu-id="9d57b-137">**RTM\_IPX\_ROUTE**</span></span>](rtm-ipx-route.md)
</dt> </dl>

 

 





