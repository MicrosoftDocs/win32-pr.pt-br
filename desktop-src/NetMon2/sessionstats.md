---
description: A estrutura SESSIONSTATS fornece estatísticas sobre uma sessão.
ms.assetid: 51a6a601-634e-4d97-8c85-d3961400a2d1
title: Estrutura SESSIONSTATS (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SESSIONSTATS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4eddfa6b0a45627c59e61fd083eb11b8d5f26caf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165346"
---
# <a name="sessionstats-structure"></a><span data-ttu-id="3fa58-103">Estrutura SESSIONSTATS</span><span class="sxs-lookup"><span data-stu-id="3fa58-103">SESSIONSTATS structure</span></span>

<span data-ttu-id="3fa58-104">A estrutura **SESSIONSTATS** fornece estatísticas sobre uma [*sessão*](s.md).</span><span class="sxs-lookup"><span data-stu-id="3fa58-104">The **SESSIONSTATS** structure provides statistics about a [*session*](s.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3fa58-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3fa58-105">Syntax</span></span>


```C++
typedef struct _SESSIONSTATS {
  DWORD NextSession;
  DWORD StationOwner;
  DWORD StationPartner;
  DWORD Flags;
  DWORD TotalPacketsSent;
} SESSIONSTATS, *LPSESSIONSTATS;
```



## <a name="members"></a><span data-ttu-id="3fa58-106">Membros</span><span class="sxs-lookup"><span data-stu-id="3fa58-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="3fa58-107">**NextSession**</span><span class="sxs-lookup"><span data-stu-id="3fa58-107">**NextSession**</span></span>
</dt> <dd>

<span data-ttu-id="3fa58-108">Índice da próxima sessão do proprietário da estação.</span><span class="sxs-lookup"><span data-stu-id="3fa58-108">Index of the station owner's next session.</span></span>

</dd> <dt>

<span data-ttu-id="3fa58-109">**StationOwner**</span><span class="sxs-lookup"><span data-stu-id="3fa58-109">**StationOwner**</span></span>
</dt> <dd>

<span data-ttu-id="3fa58-110">Índice de uma estação proprietária dentro da matriz de estrutura [STATIONSTATS](stationstats.md) associada.</span><span class="sxs-lookup"><span data-stu-id="3fa58-110">Index of a owner station within the associated [STATIONSTATS](stationstats.md) structure array.</span></span> <span data-ttu-id="3fa58-111">A estação do proprietário é a estação que iniciou a sessão, a estação que enviou os pacotes da sessão.</span><span class="sxs-lookup"><span data-stu-id="3fa58-111">The owner station is the station that initiated the session, the station that sent the packets of the session.</span></span>

</dd> <dt>

<span data-ttu-id="3fa58-112">**StationPartner**</span><span class="sxs-lookup"><span data-stu-id="3fa58-112">**StationPartner**</span></span>
</dt> <dd>

<span data-ttu-id="3fa58-113">Índice da outra estação dentro da matriz de estrutura [STATIONSTATS](stationstats.md) associada.</span><span class="sxs-lookup"><span data-stu-id="3fa58-113">Index of the other station within the associated [STATIONSTATS](stationstats.md) structure array.</span></span> <span data-ttu-id="3fa58-114">A estação de parceiro é a estação que recebeu os pacotes da sessão.</span><span class="sxs-lookup"><span data-stu-id="3fa58-114">The partner station is the station that received the packets of the session.</span></span>

</dd> <dt>

<span data-ttu-id="3fa58-115">**Sinalizadores**</span><span class="sxs-lookup"><span data-stu-id="3fa58-115">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="3fa58-116">Este membro está obsoleto.</span><span class="sxs-lookup"><span data-stu-id="3fa58-116">This member is obsolete.</span></span>

</dd> <dt>

<span data-ttu-id="3fa58-117">**TotalPacketsSent**</span><span class="sxs-lookup"><span data-stu-id="3fa58-117">**TotalPacketsSent**</span></span>
</dt> <dd>

<span data-ttu-id="3fa58-118">Número de pacotes enviados na sessão.</span><span class="sxs-lookup"><span data-stu-id="3fa58-118">Number of packets sent in the session.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3fa58-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="3fa58-119">Remarks</span></span>

<span data-ttu-id="3fa58-120">O Monitor de Rede armazena informações de sessão e de estação em duas matrizes associadas, cujos elementos são estruturas **SESSIONSTATS** e [STATIONSTATS](stationstats.md) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="3fa58-120">Network Monitor stores session and station information in two associated arrays, whose elements are **SESSIONSTATS** and [STATIONSTATS](stationstats.md) structures respectively.</span></span> <span data-ttu-id="3fa58-121">Os membros dessas estruturas podem ser usados para navegar entre eles.</span><span class="sxs-lookup"><span data-stu-id="3fa58-121">The members of these structures can be used to navigate between them.</span></span> <span data-ttu-id="3fa58-122">Por exemplo, para mover para a próxima sessão para um proprietário de estação específico, use **NextSession**.</span><span class="sxs-lookup"><span data-stu-id="3fa58-122">For example, to move to the next session for a specific station owner, use **NextSession**.</span></span> <span data-ttu-id="3fa58-123">Para saltar para o proprietário e a estação de parceiro da sessão na matriz STATIONSTATS, use o índice fornecido em **StationOwner** e **StationPartner**.</span><span class="sxs-lookup"><span data-stu-id="3fa58-123">To jump to the owner and partner station of the session in the STATIONSTATS array, use the index provided in **StationOwner** and **StationPartner**.</span></span>

> [!Note]  
> <span data-ttu-id="3fa58-124">A matriz SESSIONSTATS contém um elemento para cada sessão na captura atual.</span><span class="sxs-lookup"><span data-stu-id="3fa58-124">The SESSIONSTATS array contains an element for each session in the current capture.</span></span> <span data-ttu-id="3fa58-125">O algoritmo Monitor de Rede usado para adicionar elementos à matriz SESSIONSTATS baseia-se em informações de gravação eficiente enquanto a captura está em andamento.</span><span class="sxs-lookup"><span data-stu-id="3fa58-125">The algorithm Network Monitor uses to add elements to the SESSIONSTATS array is based on efficiently recording information while the capture is in progress.</span></span> <span data-ttu-id="3fa58-126">Consequentemente, a próxima sessão para uma estação de proprietário específica nem sempre é o próximo elemento na matriz.</span><span class="sxs-lookup"><span data-stu-id="3fa58-126">Consequently, the next session for a specific owner station is not always the next element in the array.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3fa58-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3fa58-127">Requirements</span></span>



| <span data-ttu-id="3fa58-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fa58-128">Requirement</span></span> | <span data-ttu-id="3fa58-129">Valor</span><span class="sxs-lookup"><span data-stu-id="3fa58-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3fa58-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3fa58-130">Minimum supported client</span></span><br/> | <span data-ttu-id="3fa58-131">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3fa58-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3fa58-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3fa58-132">Minimum supported server</span></span><br/> | <span data-ttu-id="3fa58-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3fa58-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3fa58-134">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3fa58-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="3fa58-135"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="3fa58-135"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fa58-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="3fa58-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fa58-137">IDelaydC::GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="3fa58-137">IDelaydC::GetConversationStatistics</span></span>](idelaydc-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="3fa58-138">IRTC::GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="3fa58-138">IRTC::GetConversationStatistics</span></span>](irtc-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="3fa58-139">IStats::GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="3fa58-139">IStats::GetConversationStatistics</span></span>](istats-getconversationstatistics.md)
</dt> </dl>

 

 




