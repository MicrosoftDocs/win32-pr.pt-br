---
title: Estrutura de IP_NETWORK (RTM. h)
description: A \_ estrutura de rede IP descreve um endereço de rede IP.
ms.assetid: 5dcc733f-c86f-407e-8727-64f3ae71dd48
keywords:
- RAS da estrutura de IP_NETWORK
- RAS de ponteiro de estrutura de PIP_NETWORK
topic_type:
- apiref
api_name:
- IP_NETWORK
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2541c493b1b2e3805e3705c71e890c6a6aaa98ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644894"
---
# <a name="ip_network-structure"></a><span data-ttu-id="e3435-105">\_Estrutura de rede IP</span><span class="sxs-lookup"><span data-stu-id="e3435-105">IP\_NETWORK structure</span></span>

<span data-ttu-id="e3435-106">\[Essa API foi substituída pela API do [Gerenciador de tabela de roteamento versão 2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e3435-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="e3435-107">Os aplicativos devem usar a API da versão 2 do Gerenciador de tabela de roteamento.\]</span><span class="sxs-lookup"><span data-stu-id="e3435-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="e3435-108">A estrutura de **\_ rede IP** descreve um endereço de rede IP.</span><span class="sxs-lookup"><span data-stu-id="e3435-108">The **IP\_NETWORK** structure describes an IP network address.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3435-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e3435-109">Syntax</span></span>


```C++
typedef struct _IP_NETWORK {
  DWORD N_NetNumber;
  DWORD N_NetMask;
} IP_NETWORK, *PIP_NETWORK;
```



## <a name="members"></a><span data-ttu-id="e3435-110">Membros</span><span class="sxs-lookup"><span data-stu-id="e3435-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="e3435-111">**N \_ Netnumber**</span><span class="sxs-lookup"><span data-stu-id="e3435-111">**N\_NetNumber**</span></span>
</dt> <dd>

<span data-ttu-id="e3435-112">Especifica o número de rede IP expresso como um endereço IP na ordem de bytes de máquina.</span><span class="sxs-lookup"><span data-stu-id="e3435-112">Specifies the IP network number expressed as an IP address in machine-byte order.</span></span>

</dd> <dt>

<span data-ttu-id="e3435-113">**N \_ máscara de rede**</span><span class="sxs-lookup"><span data-stu-id="e3435-113">**N\_NetMask**</span></span>
</dt> <dd>

<span data-ttu-id="e3435-114">Especifica a máscara de rede.</span><span class="sxs-lookup"><span data-stu-id="e3435-114">Specifies the network mask.</span></span> <span data-ttu-id="e3435-115">Aplique essa máscara ao endereço IP para extrair o endereço de rede.</span><span class="sxs-lookup"><span data-stu-id="e3435-115">Apply this mask to the IP address in order to extract the network address.</span></span> <span data-ttu-id="e3435-116">A máscara de rede está na ordem de bytes de máquina.</span><span class="sxs-lookup"><span data-stu-id="e3435-116">The network mask is in machine-byte order.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e3435-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3435-117">Requirements</span></span>



| <span data-ttu-id="e3435-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3435-118">Requirement</span></span> | <span data-ttu-id="e3435-119">Valor</span><span class="sxs-lookup"><span data-stu-id="e3435-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e3435-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e3435-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e3435-121">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e3435-121">None supported</span></span><br/>                                                        |
| <span data-ttu-id="e3435-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e3435-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e3435-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e3435-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e3435-124">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="e3435-124">End of server support</span></span><br/>    | <span data-ttu-id="e3435-125">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e3435-125">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="e3435-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e3435-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3435-127"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3435-127"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3435-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="e3435-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3435-129">Referência da versão 1 do Gerenciador de tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="e3435-129">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="e3435-130">Estruturas da versão 1 do Gerenciador de tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="e3435-130">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="e3435-131">**\_rota de IP RTM \_**</span><span class="sxs-lookup"><span data-stu-id="e3435-131">**RTM\_IP\_ROUTE**</span></span>](rtm-ip-route.md)
</dt> </dl>

 

 





