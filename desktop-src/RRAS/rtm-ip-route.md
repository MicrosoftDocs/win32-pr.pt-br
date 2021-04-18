---
title: Estrutura de RTM_IP_ROUTE (RTM. h)
description: A \_ estrutura de rota de IP RTM \_ contém informações que descrevem uma rota de propriedade da família de protocolos IP.
ms.assetid: e752a4ae-a6bf-4cd3-9638-7615ff3901b7
keywords:
- RAS da estrutura de RTM_IP_ROUTE
- RAS de ponteiro de estrutura de PRTM_IP_ROUTE
topic_type:
- apiref
api_name:
- RTM_IP_ROUTE
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1978503a3ec37e0c39716569030d5ea6599e19d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105778525"
---
# <a name="rtm_ip_route-structure"></a><span data-ttu-id="0607c-105">Estrutura de rota de \_ IP RTM \_</span><span class="sxs-lookup"><span data-stu-id="0607c-105">RTM\_IP\_ROUTE structure</span></span>

<span data-ttu-id="0607c-106">\[Essa API foi substituída pela API do [Gerenciador de tabela de roteamento versão 2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="0607c-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="0607c-107">Os aplicativos devem usar a API da versão 2 do Gerenciador de tabela de roteamento.\]</span><span class="sxs-lookup"><span data-stu-id="0607c-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="0607c-108">A estrutura de **\_ \_ rota de IP RTM** contém informações que descrevem uma rota de propriedade da família de protocolos IP.</span><span class="sxs-lookup"><span data-stu-id="0607c-108">The **RTM\_IP\_ROUTE** structure contains information that describes a route owned by the IP protocol family.</span></span>

## <a name="syntax"></a><span data-ttu-id="0607c-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0607c-109">Syntax</span></span>


```C++
typedef struct _RTM_IP_ROUTE {
  FILETIME               RR_TimeStamp;
  DWORD                  RR_RoutingProtocol;
  DWORD                  RR_InterfaceID;
  PROTOCOL_SPECIFIC_DATA RR_ProtocolSpecificData;
  IP_NETWORK             RR_Network;
  IP_NEXT_HOP_ADDRESS    RR_NextHopAddress;
  IP_SPECIFIC_DATA       RR_FamilySpecificData;
} RTM_IP_ROUTE, *PRTM_IP_ROUTE;
```



## <a name="members"></a><span data-ttu-id="0607c-110">Membros</span><span class="sxs-lookup"><span data-stu-id="0607c-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="0607c-111">**\_Carimbo de data/hora RR**</span><span class="sxs-lookup"><span data-stu-id="0607c-111">**RR\_TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="0607c-112">Especifica a hora em que a entrada de rota foi criada ou atualizada pela última vez.</span><span class="sxs-lookup"><span data-stu-id="0607c-112">Specifies the time that the route entry was created or last updated.</span></span> <span data-ttu-id="0607c-113">Esse membro é definido pelo Gerenciador de tabela de roteamento.</span><span class="sxs-lookup"><span data-stu-id="0607c-113">This member is set by the routing table manager.</span></span> <span data-ttu-id="0607c-114">O tempo é expresso como uma estrutura FILETIME.</span><span class="sxs-lookup"><span data-stu-id="0607c-114">The time is expressed as a FILETIME structure.</span></span>

</dd> <dt>

<span data-ttu-id="0607c-115">**\_ROUTINGPROTOCOL RR**</span><span class="sxs-lookup"><span data-stu-id="0607c-115">**RR\_RoutingProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="0607c-116">Especifica o protocolo de roteamento que adicionou a rota.</span><span class="sxs-lookup"><span data-stu-id="0607c-116">Specifies the routing protocol that added the route.</span></span>

</dd> <dt>

<span data-ttu-id="0607c-117">**Tipo de registro de recurso \_**</span><span class="sxs-lookup"><span data-stu-id="0607c-117">**RR\_InterfaceID**</span></span>
</dt> <dd>

<span data-ttu-id="0607c-118">Especifica a interface pela qual a rota foi obtida.</span><span class="sxs-lookup"><span data-stu-id="0607c-118">Specifies the interface through which the route was obtained.</span></span>

</dd> <dt>

<span data-ttu-id="0607c-119">**\_PROTOCOLSPECIFICDATA RR**</span><span class="sxs-lookup"><span data-stu-id="0607c-119">**RR\_ProtocolSpecificData**</span></span>
</dt> <dd>

<span data-ttu-id="0607c-120">Especifica uma estrutura de [**\_ \_ dados específica de protocolo**](protocol-specific-data.md) que contém memória reservada para dados específicos do protocolo de roteamento.</span><span class="sxs-lookup"><span data-stu-id="0607c-120">Specifies a [**PROTOCOL\_SPECIFIC\_DATA**](protocol-specific-data.md) structure that contains memory reserved for routing-protocol-specific data.</span></span>

</dd> <dt>

<span data-ttu-id="0607c-121">**\_Rede RR**</span><span class="sxs-lookup"><span data-stu-id="0607c-121">**RR\_Network**</span></span>
</dt> <dd>

<span data-ttu-id="0607c-122">Especifica uma estrutura de [**\_ rede IP**](ip-network.md) que contém um endereço de rede IP.</span><span class="sxs-lookup"><span data-stu-id="0607c-122">Specifies an [**IP\_NETWORK**](ip-network.md) structure that contains an IP network address.</span></span>

</dd> <dt>

<span data-ttu-id="0607c-123">**\_NEXTHOPADDRESS RR**</span><span class="sxs-lookup"><span data-stu-id="0607c-123">**RR\_NextHopAddress**</span></span>
</dt> <dd>

<span data-ttu-id="0607c-124">Especifica uma estrutura de [**\_ endereço de próximo \_ salto \_ IP**](ip-next-hop-address.md) que contém o endereço do roteador do próximo salto.</span><span class="sxs-lookup"><span data-stu-id="0607c-124">Specifies an [**IP\_NEXT\_HOP\_ADDRESS**](ip-next-hop-address.md) structure that contains the address of the next-hop router.</span></span>

</dd> <dt>

<span data-ttu-id="0607c-125">**\_FAMILYSPECIFICDATA RR**</span><span class="sxs-lookup"><span data-stu-id="0607c-125">**RR\_FamilySpecificData**</span></span>
</dt> <dd>

<span data-ttu-id="0607c-126">Especifica uma estrutura de [**\_ \_ dados específica de IP**](ip-specific-data.md) que contém dados específicos da família de protocolos IP.</span><span class="sxs-lookup"><span data-stu-id="0607c-126">Specifies an [**IP\_SPECIFIC\_DATA**](ip-specific-data.md) structure that contains IP protocol-family-specific data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0607c-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="0607c-127">Remarks</span></span>

<span data-ttu-id="0607c-128">Os membros da estrutura **de \_ \_ rota de IP RTM** são alinhados em **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="0607c-128">The members of the **RTM\_IP\_ROUTE** structure are all **DWORD** aligned.</span></span>

## <a name="requirements"></a><span data-ttu-id="0607c-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0607c-129">Requirements</span></span>



| <span data-ttu-id="0607c-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="0607c-130">Requirement</span></span> | <span data-ttu-id="0607c-131">Valor</span><span class="sxs-lookup"><span data-stu-id="0607c-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0607c-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0607c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="0607c-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="0607c-133">None supported</span></span><br/>                                                        |
| <span data-ttu-id="0607c-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0607c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="0607c-135">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0607c-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0607c-136">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="0607c-136">End of server support</span></span><br/>    | <span data-ttu-id="0607c-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0607c-137">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="0607c-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0607c-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="0607c-139"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="0607c-139"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0607c-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="0607c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0607c-141">Referência da versão 1 do Gerenciador de tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="0607c-141">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="0607c-142">Estruturas da versão 1 do Gerenciador de tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="0607c-142">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="0607c-143">**\_rede IP**</span><span class="sxs-lookup"><span data-stu-id="0607c-143">**IP\_NETWORK**</span></span>](ip-network.md)
</dt> <dt>

[<span data-ttu-id="0607c-144">**\_endereço do próximo \_ salto \_ IP**</span><span class="sxs-lookup"><span data-stu-id="0607c-144">**IP\_NEXT\_HOP\_ADDRESS**</span></span>](ip-next-hop-address.md)
</dt> <dt>

[<span data-ttu-id="0607c-145">**\_dados específicos de IP \_**</span><span class="sxs-lookup"><span data-stu-id="0607c-145">**IP\_SPECIFIC\_DATA**</span></span>](ip-specific-data.md)
</dt> </dl>

 

 





