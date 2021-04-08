---
description: A estrutura STATIONSTATS fornece estatísticas sobre uma estação específica descrita pela captura atual.
ms.assetid: f85d53d6-f496-4242-875f-e173c76b046a
title: Estrutura STATIONSTATS (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STATIONSTATS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 0b37d4570fe8f4c27ea66e6350b79e14a10e544e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010830"
---
# <a name="stationstats-structure"></a><span data-ttu-id="03002-103">Estrutura STATIONSTATS</span><span class="sxs-lookup"><span data-stu-id="03002-103">STATIONSTATS structure</span></span>

<span data-ttu-id="03002-104">A estrutura **STATIONSTATS** fornece estatísticas sobre uma [*estação*](s.md) específica descrita pela captura atual.</span><span class="sxs-lookup"><span data-stu-id="03002-104">The **STATIONSTATS** structure provides statistics about a specific [*station*](s.md) described by the current capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="03002-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="03002-105">Syntax</span></span>


```C++
typedef struct _STATIONSTATS {
  DWORD NextStationStats;
  DWORD SessionPartnerList;
  DWORD Flags;
  BYTE  StationAddress[6];
  WORD  Pad;
  DWORD TotalPacketsReceived;
  DWORD TotalDirectedPacketsSent;
  DWORD TotalBroadcastPacketsSent;
  DWORD TotalMulticastPacketsSent;
  DWORD TotalBytesReceived;
  DWORD TotalBytesSent;
} STATIONSTATS, *LPSTATIONSTATS;
```



## <a name="members"></a><span data-ttu-id="03002-106">Membros</span><span class="sxs-lookup"><span data-stu-id="03002-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="03002-107">**NextStationStats**</span><span class="sxs-lookup"><span data-stu-id="03002-107">**NextStationStats**</span></span>
</dt> <dd>

<span data-ttu-id="03002-108">Índice da próxima estação registrada na matriz de estrutura **STATIONSTATS** .</span><span class="sxs-lookup"><span data-stu-id="03002-108">Index of the next station recorded in the **STATIONSTATS** structure array.</span></span>

</dd> <dt>

<span data-ttu-id="03002-109">**SessionPartnerList**</span><span class="sxs-lookup"><span data-stu-id="03002-109">**SessionPartnerList**</span></span>
</dt> <dd>

<span data-ttu-id="03002-110">Índice da lista de parceiros de estação.</span><span class="sxs-lookup"><span data-stu-id="03002-110">Index of the station partner list.</span></span>

</dd> <dt>

<span data-ttu-id="03002-111">**Sinalizadores**</span><span class="sxs-lookup"><span data-stu-id="03002-111">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="03002-112">Este membro está obsoleto.</span><span class="sxs-lookup"><span data-stu-id="03002-112">This member is obsolete.</span></span>

</dd> <dt>

<span data-ttu-id="03002-113">**StationAddress**</span><span class="sxs-lookup"><span data-stu-id="03002-113">**StationAddress**</span></span>
</dt> <dd>

<span data-ttu-id="03002-114">O endereço MAC da estação.</span><span class="sxs-lookup"><span data-stu-id="03002-114">The MAC address of the station.</span></span>

</dd> <dt>

<span data-ttu-id="03002-115">**Bloco**</span><span class="sxs-lookup"><span data-stu-id="03002-115">**Pad**</span></span>
</dt> <dd>

<span data-ttu-id="03002-116">Alinhamento de **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="03002-116">**DWORD** alignment.</span></span>

</dd> <dt>

<span data-ttu-id="03002-117">**TotalPacketsReceived**</span><span class="sxs-lookup"><span data-stu-id="03002-117">**TotalPacketsReceived**</span></span>
</dt> <dd>

<span data-ttu-id="03002-118">Número total de pacotes enviados para a estação.</span><span class="sxs-lookup"><span data-stu-id="03002-118">Total number of packets sent to the station.</span></span>

</dd> <dt>

<span data-ttu-id="03002-119">**TotalDirectedPacketsSent**</span><span class="sxs-lookup"><span data-stu-id="03002-119">**TotalDirectedPacketsSent**</span></span>
</dt> <dd>

<span data-ttu-id="03002-120">Número total de pacotes direcionados enviados pela estação.</span><span class="sxs-lookup"><span data-stu-id="03002-120">Total number of directed packets sent by the station.</span></span>

</dd> <dt>

<span data-ttu-id="03002-121">**TotalBroadcastPacketsSent**</span><span class="sxs-lookup"><span data-stu-id="03002-121">**TotalBroadcastPacketsSent**</span></span>
</dt> <dd>

<span data-ttu-id="03002-122">Número total de pacotes direcionados à difusão (endereço MAC FF FF FF FF TT FF) enviados pela estação.</span><span class="sxs-lookup"><span data-stu-id="03002-122">Total number of broadcast-directed packets (MAC address FF FF FF FF FF FF) sent by the station.</span></span>

</dd> <dt>

<span data-ttu-id="03002-123">**TotalMulticastPacketsSent**</span><span class="sxs-lookup"><span data-stu-id="03002-123">**TotalMulticastPacketsSent**</span></span>
</dt> <dd>

<span data-ttu-id="03002-124">Número total de pacotes multicast (conjunto de bits do grupo no endereço de destino) enviados pela estação.</span><span class="sxs-lookup"><span data-stu-id="03002-124">Total number of multicast packets (Group bit set in destination address) sent by the station.</span></span>

</dd> <dt>

<span data-ttu-id="03002-125">**TotalBytesReceived**</span><span class="sxs-lookup"><span data-stu-id="03002-125">**TotalBytesReceived**</span></span>
</dt> <dd>

<span data-ttu-id="03002-126">Número total de bytes enviados à estação.</span><span class="sxs-lookup"><span data-stu-id="03002-126">Total number of bytes sent to the station.</span></span>

</dd> <dt>

<span data-ttu-id="03002-127">**TotalBytesSent**</span><span class="sxs-lookup"><span data-stu-id="03002-127">**TotalBytesSent**</span></span>
</dt> <dd>

<span data-ttu-id="03002-128">Número total de bytes enviados pela estação.</span><span class="sxs-lookup"><span data-stu-id="03002-128">Total number of bytes sent by the station.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="03002-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="03002-129">Remarks</span></span>

<span data-ttu-id="03002-130">Monitor de Rede armazena informações de sessão e de estação em duas matrizes associadas.</span><span class="sxs-lookup"><span data-stu-id="03002-130">Network Monitor stores session and station information in two associated arrays.</span></span> <span data-ttu-id="03002-131">cujos elementos são estruturas [SESSIONSTATS](sessionstats.md) e **STATIONSTATS** , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="03002-131">whose elements are [SESSIONSTATS](sessionstats.md) and **STATIONSTATS** structures respectively.</span></span> <span data-ttu-id="03002-132">Os membros dessas estruturas podem ser usados para navegar entre eles.</span><span class="sxs-lookup"><span data-stu-id="03002-132">The members of these structures can be used to navigate between them.</span></span> <span data-ttu-id="03002-133">Por exemplo, para mover para a próxima estação, use **NextStationStats**.</span><span class="sxs-lookup"><span data-stu-id="03002-133">For example, to move to the next station use **NextStationStats**.</span></span> <span data-ttu-id="03002-134">Para saltar para a lista de parceiros de sessão na matriz SESSIONSTATS, use o índice fornecido em **SessionPartnerList**.</span><span class="sxs-lookup"><span data-stu-id="03002-134">To jump to the session partner list in the SESSIONSTATS array, use the index provided in **SessionPartnerList**.</span></span>

> [!Note]  
> <span data-ttu-id="03002-135">A matriz **STATIONSTATS** contém um elemento para cada estação usada durante a captura atual.</span><span class="sxs-lookup"><span data-stu-id="03002-135">The **STATIONSTATS** array contains an element for each station used during the current capture.</span></span> <span data-ttu-id="03002-136">O algoritmo que Monitor de Rede usa para adicionar elementos a essa matriz baseia-se na maneira mais eficiente de registrar informações enquanto a captura está em andamento.</span><span class="sxs-lookup"><span data-stu-id="03002-136">The algorithm Network Monitor uses to add elements to this array is based on the most efficient way to record information while the capture is in progress.</span></span> <span data-ttu-id="03002-137">Consequentemente, a próxima estação nem sempre é o próximo elemento na matriz.</span><span class="sxs-lookup"><span data-stu-id="03002-137">Consequently, the next station is not always the next element in the array.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="03002-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03002-138">Requirements</span></span>



| <span data-ttu-id="03002-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="03002-139">Requirement</span></span> | <span data-ttu-id="03002-140">Valor</span><span class="sxs-lookup"><span data-stu-id="03002-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="03002-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="03002-141">Minimum supported client</span></span><br/> | <span data-ttu-id="03002-142">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="03002-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="03002-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="03002-143">Minimum supported server</span></span><br/> | <span data-ttu-id="03002-144">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="03002-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="03002-145">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="03002-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="03002-146"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="03002-146"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03002-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="03002-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03002-148">IDelaydC::GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="03002-148">IDelaydC::GetConversationStatistics</span></span>](idelaydc-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="03002-149">IRTC::GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="03002-149">IRTC::GetConversationStatistics</span></span>](irtc-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="03002-150">IStats::GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="03002-150">IStats::GetConversationStatistics</span></span>](istats-getconversationstatistics.md)
</dt> </dl>

 

 




