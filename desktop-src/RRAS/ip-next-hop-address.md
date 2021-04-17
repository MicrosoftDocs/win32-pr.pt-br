---
title: Estrutura de IP_NEXT_HOP_ADDRESS (RTM. h)
description: A \_ estrutura de endereço do próximo salto IP \_ \_ contém o endereço do roteador do próximo salto para uma rota IP.
ms.assetid: a97b3995-dfaa-4e53-be86-3ad46b8be691
keywords:
- RAS da estrutura de IP_NEXT_HOP_ADDRESS
- RAS da estrutura de PIP_NEXT_HOP_ADDRESS
topic_type:
- apiref
api_name:
- IP_NEXT_HOP_ADDRESS
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1818a49e7977dbb4dfa31ebac1dae7651adb8d45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105747937"
---
# <a name="ip_next_hop_address-structure"></a><span data-ttu-id="292a0-105">\_Estrutura de endereço do próximo \_ salto IP \_</span><span class="sxs-lookup"><span data-stu-id="292a0-105">IP\_NEXT\_HOP\_ADDRESS structure</span></span>

<span data-ttu-id="292a0-106">\[Essa API foi substituída pela API do [Gerenciador de tabela de roteamento versão 2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="292a0-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="292a0-107">Os aplicativos devem usar a API da versão 2 do Gerenciador de tabela de roteamento.\]</span><span class="sxs-lookup"><span data-stu-id="292a0-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="292a0-108">A estrutura de **\_ endereço do próximo \_ salto \_ IP** contém o endereço do roteador do próximo salto para uma rota IP.</span><span class="sxs-lookup"><span data-stu-id="292a0-108">The **IP\_NEXT\_HOP\_ADDRESS** structure contains the address for the next-hop router for an IP route.</span></span>

## <a name="syntax"></a><span data-ttu-id="292a0-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="292a0-109">Syntax</span></span>


```C++
typedef struct _IP_NEXT_HOP_ADDRESS {
  DWORD N_NetNumber;
  DWORD N_NetMask;
} IP_NEXT_HOP_ADDRESS, *PIP_NEXT_HOP_ADDRESS;
```



## <a name="members"></a><span data-ttu-id="292a0-110">Membros</span><span class="sxs-lookup"><span data-stu-id="292a0-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="292a0-111">**N \_ Netnumber**</span><span class="sxs-lookup"><span data-stu-id="292a0-111">**N\_NetNumber**</span></span>
</dt> <dd>

<span data-ttu-id="292a0-112">Especifica o endereço de rede IP expresso como um endereço IP na ordem de bytes de máquina.</span><span class="sxs-lookup"><span data-stu-id="292a0-112">Specifies the IP network address expressed as an IP address in machine-byte order.</span></span>

</dd> <dt>

<span data-ttu-id="292a0-113">**N \_ máscara de rede**</span><span class="sxs-lookup"><span data-stu-id="292a0-113">**N\_NetMask**</span></span>
</dt> <dd>

<span data-ttu-id="292a0-114">Especifica a máscara de rede.</span><span class="sxs-lookup"><span data-stu-id="292a0-114">Specifies the network mask.</span></span> <span data-ttu-id="292a0-115">Aplique essa máscara ao endereço IP para extrair o endereço de rede.</span><span class="sxs-lookup"><span data-stu-id="292a0-115">Apply this mask to the IP address in order to extract the network address.</span></span> <span data-ttu-id="292a0-116">A máscara de rede está na ordem de bytes de máquina.</span><span class="sxs-lookup"><span data-stu-id="292a0-116">The network mask is in machine-byte order.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="292a0-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="292a0-117">Remarks</span></span>

<span data-ttu-id="292a0-118">A estrutura de **\_ endereço do próximo \_ salto \_ IP** é um typedef da estrutura de [**\_ rede IP**](ip-network.md) .</span><span class="sxs-lookup"><span data-stu-id="292a0-118">The **IP\_NEXT\_HOP\_ADDRESS** structure is a typedef of the [**IP\_NETWORK**](ip-network.md) structure.</span></span> <span data-ttu-id="292a0-119">O TypeDef está no RTM. h.</span><span class="sxs-lookup"><span data-stu-id="292a0-119">The typedef is in Rtm.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="292a0-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="292a0-120">Requirements</span></span>



| <span data-ttu-id="292a0-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="292a0-121">Requirement</span></span> | <span data-ttu-id="292a0-122">Valor</span><span class="sxs-lookup"><span data-stu-id="292a0-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="292a0-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="292a0-123">Minimum supported client</span></span><br/> | <span data-ttu-id="292a0-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="292a0-124">None supported</span></span><br/>                                                        |
| <span data-ttu-id="292a0-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="292a0-125">Minimum supported server</span></span><br/> | <span data-ttu-id="292a0-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="292a0-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="292a0-127">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="292a0-127">End of server support</span></span><br/>    | <span data-ttu-id="292a0-128">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="292a0-128">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="292a0-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="292a0-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="292a0-130"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="292a0-130"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="292a0-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="292a0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="292a0-132">Referência da versão 1 do Gerenciador de tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="292a0-132">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="292a0-133">Estruturas da versão 1 do Gerenciador de tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="292a0-133">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="292a0-134">**\_rede IP**</span><span class="sxs-lookup"><span data-stu-id="292a0-134">**IP\_NETWORK**</span></span>](ip-network.md)
</dt> <dt>

[<span data-ttu-id="292a0-135">**\_rota de IP RTM \_**</span><span class="sxs-lookup"><span data-stu-id="292a0-135">**RTM\_IP\_ROUTE**</span></span>](rtm-ip-route.md)
</dt> </dl>

 

 





