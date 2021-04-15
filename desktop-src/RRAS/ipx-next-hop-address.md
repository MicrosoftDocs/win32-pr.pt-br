---
title: Estrutura de IPX_NEXT_HOP_ADDRESS (RTM. h)
description: A \_ estrutura de endereço do próximo salto IPX \_ \_ contém o endereço do roteador do próximo salto para uma rota IPX.
ms.assetid: 079e3284-6238-4bcf-a17f-68ff86775f18
keywords:
- RAS da estrutura de IPX_NEXT_HOP_ADDRESS
- RAS de ponteiro de estrutura de PIPX_NEXT_HOP_ADDRESS
topic_type:
- apiref
api_name:
- IPX_NEXT_HOP_ADDRESS
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99c3eb135f1d87050cd190fe47d0088fd1ab86f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454593"
---
# <a name="ipx_next_hop_address-structure"></a><span data-ttu-id="2dda6-105">\_Estrutura de endereço do próximo salto do IPX \_ \_</span><span class="sxs-lookup"><span data-stu-id="2dda6-105">IPX\_NEXT\_HOP\_ADDRESS structure</span></span>

<span data-ttu-id="2dda6-106">\[Essa API foi substituída pela API do [Gerenciador de tabela de roteamento versão 2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="2dda6-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="2dda6-107">Os aplicativos devem usar a API da versão 2 do Gerenciador de tabela de roteamento.\]</span><span class="sxs-lookup"><span data-stu-id="2dda6-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="2dda6-108">A estrutura de **\_ endereço do próximo \_ salto \_ IPX** contém o endereço do roteador do próximo salto para uma rota IPX.</span><span class="sxs-lookup"><span data-stu-id="2dda6-108">The **IPX\_NEXT\_HOP\_ADDRESS** structure contains the address for the next-hop router for an IPX route.</span></span>

## <a name="syntax"></a><span data-ttu-id="2dda6-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2dda6-109">Syntax</span></span>


```C++
typedef struct _IPX_NEXT_HOP_ADDRESS {
  BYTE NHA_Mac[6];
} IPX_NEXT_HOP_ADDRESS, *PIPX_NEXT_HOP_ADDRESS;
```



## <a name="members"></a><span data-ttu-id="2dda6-110">Membros</span><span class="sxs-lookup"><span data-stu-id="2dda6-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="2dda6-111">**NHA \_ Mac**</span><span class="sxs-lookup"><span data-stu-id="2dda6-111">**NHA\_Mac**</span></span>
</dt> <dd>

<span data-ttu-id="2dda6-112">Especifica o endereço MAC do roteador do próximo salto.</span><span class="sxs-lookup"><span data-stu-id="2dda6-112">Specifies the MAC address of next-hop router.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2dda6-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2dda6-113">Requirements</span></span>



| <span data-ttu-id="2dda6-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2dda6-114">Requirement</span></span> | <span data-ttu-id="2dda6-115">Valor</span><span class="sxs-lookup"><span data-stu-id="2dda6-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2dda6-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2dda6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2dda6-117">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="2dda6-117">None supported</span></span><br/>                                                        |
| <span data-ttu-id="2dda6-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2dda6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2dda6-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2dda6-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2dda6-120">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="2dda6-120">End of server support</span></span><br/>    | <span data-ttu-id="2dda6-121">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2dda6-121">Windows Server 2003</span></span><br/>                                                   |
| <span data-ttu-id="2dda6-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2dda6-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2dda6-123"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="2dda6-123"><dt>Rtm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2dda6-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="2dda6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dda6-125">Referência da versão 1 do Gerenciador de tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="2dda6-125">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="2dda6-126">Estruturas da versão 1 do Gerenciador de tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="2dda6-126">Routing Table Manager Version 1 Structures</span></span>](routing-table-manager-version-1-structures.md)
</dt> <dt>

[<span data-ttu-id="2dda6-127">**\_rota IPX do RTM \_**</span><span class="sxs-lookup"><span data-stu-id="2dda6-127">**RTM\_IPX\_ROUTE**</span></span>](rtm-ipx-route.md)
</dt> </dl>

 

 





