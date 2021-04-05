---
title: Estrutura de RTM_IPX_ROUTE (RTM. h)
description: A \_ estrutura de rota IPX do RTM \_ contém informações que descrevem uma rota para a família de protocolos IPX.
ms.assetid: ffa0637c-2197-4ebd-a5ef-e174dd0ccb15
keywords:
- RAS da estrutura de RTM_IPX_ROUTE
- RAS de ponteiro de estrutura de PRTM_IPX_ROUTE
topic_type:
- apiref
api_name:
- RTM_IPX_ROUTE
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d32333dd6a6b53ee4600dda388a318bdf9404b6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918224"
---
# <a name="rtm_ipx_route-structure"></a><span data-ttu-id="702a7-105">\_Estrutura de rota IPX do RTM \_</span><span class="sxs-lookup"><span data-stu-id="702a7-105">RTM\_IPX\_ROUTE structure</span></span>

<span data-ttu-id="702a7-106">\[Essa API foi substituída pela API do [Gerenciador de tabela de roteamento versão 2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="702a7-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="702a7-107">Os aplicativos devem usar a API da versão 2 do Gerenciador de tabela de roteamento.\]</span><span class="sxs-lookup"><span data-stu-id="702a7-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="702a7-108">A estrutura de **\_ \_ rota IPX do RTM** contém informações que descrevem uma rota para a família de protocolos IPX.</span><span class="sxs-lookup"><span data-stu-id="702a7-108">The **RTM\_IPX\_ROUTE** structure contains information that describes a route for the IPX protocol family.</span></span>

## <a name="syntax"></a><span data-ttu-id="702a7-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="702a7-109">Syntax</span></span>


```C++
typedef struct _RTM_IPX_ROUTE {
  FILETIME               RR_TimeStamp;
  DWORD                  RR_RoutingProtocol;
  DWORD                  RR_InterfaceID;
  PROTOCOL_SPECIFIC_DATA RR_ProtocolSpecificData;
  IPX_NETWORK            RR_Network;
  IPX_NEXT_HOP_ADDRESS   RR_NextHopAddress;
  IPX_SPECIFIC_DATA      RR_FamilySpecificData;
} RTM_IPX_ROUTE, *PRTM_IPX_ROUTE;
```



## <a name="members"></a><span data-ttu-id="702a7-110">Membros</span><span class="sxs-lookup"><span data-stu-id="702a7-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="702a7-111">**\_Carimbo de data/hora RR**</span><span class="sxs-lookup"><span data-stu-id="702a7-111">**RR\_TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="702a7-112">Especifica a hora em que a entrada de rota foi criada ou atualizada pela última vez.</span><span class="sxs-lookup"><span data-stu-id="702a7-112">Specifies the time that the route entry was created or last updated.</span></span> <span data-ttu-id="702a7-113">Esse membro é definido pelo Gerenciador de tabela de roteamento.</span><span class="sxs-lookup"><span data-stu-id="702a7-113">This member is set by the routing table manager.</span></span> <span data-ttu-id="702a7-114">O tempo é expresso como uma estrutura FILETIME.</span><span class="sxs-lookup"><span data-stu-id="702a7-114">The time is expressed as a FILETIME structure.</span></span>

</dd> <dt>

<span data-ttu-id="702a7-115">**\_ROUTINGPROTOCOL RR**</span><span class="sxs-lookup"><span data-stu-id="702a7-115">**RR\_RoutingProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="702a7-116">Especifica o protocolo de roteamento que adicionou a rota.</span><span class="sxs-lookup"><span data-stu-id="702a7-116">Specifies the routing protocol that added the route.</span></span>

</dd> <dt>

<span data-ttu-id="702a7-117">**Tipo de registro de recurso \_**</span><span class="sxs-lookup"><span data-stu-id="702a7-117">**RR\_InterfaceID**</span></span>
</dt> <dd>

<span data-ttu-id="702a7-118">Especifica a interface pela qual a rota foi obtida.</span><span class="sxs-lookup"><span data-stu-id="702a7-118">Specifies the interface through which the route was obtained.</span></span>

</dd> <dt>

<span data-ttu-id="702a7-119">**\_PROTOCOLSPECIFICDATA RR**</span><span class="sxs-lookup"><span data-stu-id="702a7-119">**RR\_ProtocolSpecificData**</span></span>
</dt> <dd>

<span data-ttu-id="702a7-120">Especifica uma estrutura de [**\_ \_ dados específica de protocolo**](protocol-specific-data.md) que contém a memória reservada para dados específicos para protocolos de roteamento.</span><span class="sxs-lookup"><span data-stu-id="702a7-120">Specifies a [**PROTOCOL\_SPECIFIC\_DATA**](protocol-specific-data.md) structure containing memory reserved for data specific to routing protocols.</span></span>

</dd> <dt>

<span data-ttu-id="702a7-121">**\_Rede RR**</span><span class="sxs-lookup"><span data-stu-id="702a7-121">**RR\_Network**</span></span>
</dt> <dd>

<span data-ttu-id="702a7-122">Especifica uma estrutura de [**\_ rede IPX**](ipx-network.md) que contém um endereço de rede IP.</span><span class="sxs-lookup"><span data-stu-id="702a7-122">Specifies an [**IPX\_NETWORK**](ipx-network.md) structure that contains an IP network address.</span></span>

</dd> <dt>

<span data-ttu-id="702a7-123">**\_NEXTHOPADDRESS RR**</span><span class="sxs-lookup"><span data-stu-id="702a7-123">**RR\_NextHopAddress**</span></span>
</dt> <dd>

<span data-ttu-id="702a7-124">Especifica uma estrutura de [**\_ endereço de próximo \_ salto \_ IPX**](ipx-next-hop-address.md) que contém o endereço do roteador de próximo salto.</span><span class="sxs-lookup"><span data-stu-id="702a7-124">Specifies an [**IPX\_NEXT\_HOP\_ADDRESS**](ipx-next-hop-address.md) structure that contains the address of the next-hop router.</span></span>

</dd> <dt>

<span data-ttu-id="702a7-125">**\_FAMILYSPECIFICDATA RR**</span><span class="sxs-lookup"><span data-stu-id="702a7-125">**RR\_FamilySpecificData**</span></span>
</dt> <dd>

<span data-ttu-id="702a7-126">Especifica uma estrutura de [**\_ \_ dados específica de IPX**](ipx-specific-data.md) que contém dados específicos para a família de protocolo IPX.</span><span class="sxs-lookup"><span data-stu-id="702a7-126">Specifies an [**IPX\_SPECIFIC\_DATA**](ipx-specific-data.md) structure that contains data specific to the IPX protocol family.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="702a7-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="702a7-127">Remarks</span></span>

<span data-ttu-id="702a7-128">Os membros da estrutura **de \_ \_ rota IPX do RTM** são todos alinhados em **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="702a7-128">The members of the **RTM\_IPX\_ROUTE** structure are all **DWORD** aligned.</span></span>

## <a name="requirements"></a><span data-ttu-id="702a7-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="702a7-129">Requirements</span></span>



| <span data-ttu-id="702a7-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="702a7-130">Requirement</span></span> | <span data-ttu-id="702a7-131">Valor</span><span class="sxs-lookup"><span data-stu-id="702a7-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="702a7-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="702a7-132">Minimum supported client</span></span><br/> | <span data-ttu-id="702a7-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="702a7-133">None supported</span></span><br/>                                                        |
| <span data-ttu-id="702a7-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="702a7-134">Minimum supported server</span></span><br/> | <span data-ttu-id="702a7-135">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="702a7-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="702a7-136">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="702a7-136">End of server support</span></span><br/>    | <span data-ttu-id="702a7-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="702a7-137">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="702a7-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="702a7-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="702a7-139"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="702a7-139"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="702a7-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="702a7-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="702a7-141">Referência da versão 1 do Gerenciador de tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="702a7-141">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="702a7-142">Estruturas da versão 1 do Gerenciador de tabela de roteamento \_ \_</span><span class="sxs-lookup"><span data-stu-id="702a7-142">Routing Table Manager Version\_1\_Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="702a7-143">**\_rede IPX**</span><span class="sxs-lookup"><span data-stu-id="702a7-143">**IPX\_NETWORK**</span></span>](ipx-network.md)
</dt> <dt>

[<span data-ttu-id="702a7-144">**\_endereço do próximo \_ salto \_ IPX**</span><span class="sxs-lookup"><span data-stu-id="702a7-144">**IPX\_NEXT\_HOP\_ADDRESS**</span></span>](ipx-next-hop-address.md)
</dt> <dt>

[<span data-ttu-id="702a7-145">**\_dados específicos de IPX \_**</span><span class="sxs-lookup"><span data-stu-id="702a7-145">**IPX\_SPECIFIC\_DATA**</span></span>](ipx-specific-data.md)
</dt> </dl>

 

 





