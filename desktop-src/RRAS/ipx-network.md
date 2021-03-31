---
title: Estrutura de IPX_NETWORK (RTM. h)
description: A \_ estrutura de rede IPX descreve um endereço de rede IPX.
ms.assetid: 83fc4022-8515-4a51-ac47-f92572447fbf
keywords:
- RAS da estrutura de IPX_NETWORK
- RAS de ponteiro de estrutura de PIPX_NETWORK
topic_type:
- apiref
api_name:
- IPX_NETWORK
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04aabf363c0152ba520bb5c8894142715b5bff56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103917959"
---
# <a name="ipx_network-structure"></a><span data-ttu-id="f5e9e-105">\_Estrutura de rede IPX</span><span class="sxs-lookup"><span data-stu-id="f5e9e-105">IPX\_NETWORK structure</span></span>

<span data-ttu-id="f5e9e-106">\[Essa API foi substituída pela API do [Gerenciador de tabela de roteamento versão 2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f5e9e-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="f5e9e-107">Os aplicativos devem usar a API da versão 2 do Gerenciador de tabela de roteamento.\]</span><span class="sxs-lookup"><span data-stu-id="f5e9e-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="f5e9e-108">A estrutura de **\_ rede IPX** descreve um endereço de rede IPX.</span><span class="sxs-lookup"><span data-stu-id="f5e9e-108">The **IPX\_NETWORK** structure describes an IPX network address.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5e9e-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f5e9e-109">Syntax</span></span>


```C++
typedef struct _IPX_NETWORK {
  DWORD N_NetNumber;
} IPX_NETWORK, *PIPX_NETWORK;
```



## <a name="members"></a><span data-ttu-id="f5e9e-110">Membros</span><span class="sxs-lookup"><span data-stu-id="f5e9e-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="f5e9e-111">**N \_ Netnumber**</span><span class="sxs-lookup"><span data-stu-id="f5e9e-111">**N\_NetNumber**</span></span>
</dt> <dd>

<span data-ttu-id="f5e9e-112">Contém o número de rede IPX na ordem de bytes de máquina.</span><span class="sxs-lookup"><span data-stu-id="f5e9e-112">Contains the IPX network number in machine-byte order.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f5e9e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5e9e-113">Requirements</span></span>



| <span data-ttu-id="f5e9e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5e9e-114">Requirement</span></span> | <span data-ttu-id="f5e9e-115">Valor</span><span class="sxs-lookup"><span data-stu-id="f5e9e-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f5e9e-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5e9e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f5e9e-117">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="f5e9e-117">None supported</span></span><br/>                                                        |
| <span data-ttu-id="f5e9e-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5e9e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f5e9e-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f5e9e-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f5e9e-120">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="f5e9e-120">End of server support</span></span><br/>    | <span data-ttu-id="f5e9e-121">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f5e9e-121">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="f5e9e-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f5e9e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5e9e-123"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5e9e-123"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5e9e-124">Consulte também</span><span class="sxs-lookup"><span data-stu-id="f5e9e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5e9e-125">Referência da versão 1 do Gerenciador de tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="f5e9e-125">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="f5e9e-126">Estruturas da versão 1 do Gerenciador de tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="f5e9e-126">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="f5e9e-127">**\_rota IPX do RTM \_**</span><span class="sxs-lookup"><span data-stu-id="f5e9e-127">**RTM\_IPX\_ROUTE**</span></span>](rtm-ipx-route.md)
</dt> </dl>

 

 





