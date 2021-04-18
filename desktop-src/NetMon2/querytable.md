---
description: A estrutura de QUERYTABLE fornece uma lista dos computadores que atualmente estão usando Monitor de Rede para capturar dados de rede.
ms.assetid: b701a6d5-df6d-4ee9-b008-a568a410dc14
title: Estrutura de QUERYTABLE (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- QUERYTABLE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 2b2976a56b43c55fccb9acb0c593b0dfd37e4404
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770141"
---
# <a name="querytable-structure"></a><span data-ttu-id="9d921-103">Estrutura de QUERYTABLE</span><span class="sxs-lookup"><span data-stu-id="9d921-103">QUERYTABLE structure</span></span>

<span data-ttu-id="9d921-104">A estrutura de **QUERYTABLE** fornece uma lista dos computadores que atualmente estão usando monitor de rede para capturar dados de rede.</span><span class="sxs-lookup"><span data-stu-id="9d921-104">The **QUERYTABLE** structure provides a list of the computers that are currently using Network Monitor to capture network data.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d921-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9d921-105">Syntax</span></span>


```C++
typedef struct _QUERYTABLE {
  DWORD        nStationQueries;
  STATIONQUERY StationQuery[1];
} QUERYTABLE, *LPQUERYTABLE;
```



## <a name="members"></a><span data-ttu-id="9d921-106">Membros</span><span class="sxs-lookup"><span data-stu-id="9d921-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9d921-107">**nStationQueries**</span><span class="sxs-lookup"><span data-stu-id="9d921-107">**nStationQueries**</span></span>
</dt> <dd>

<span data-ttu-id="9d921-108">Na entrada, o número máximo de computadores que você deseja que Monitor de Rede retorne.</span><span class="sxs-lookup"><span data-stu-id="9d921-108">On input, the maximum number of computers you want Network Monitor to return.</span></span>

<span data-ttu-id="9d921-109">Na saída, o número de estruturas [STATIONQUERY](stationquery.md) retornadas pelo monitor de rede.</span><span class="sxs-lookup"><span data-stu-id="9d921-109">On output, the number of [STATIONQUERY](stationquery.md) structures returned by Network Monitor.</span></span> <span data-ttu-id="9d921-110">Cada estrutura **STATIONQUERY** representa um computador que está capturando dados no momento.</span><span class="sxs-lookup"><span data-stu-id="9d921-110">Each **STATIONQUERY** structure represents a computer that is currently capturing data.</span></span>

</dd> <dt>

<span data-ttu-id="9d921-111">**StationQuery**</span><span class="sxs-lookup"><span data-stu-id="9d921-111">**StationQuery**</span></span>
</dt> <dd>

<span data-ttu-id="9d921-112">Na entrada, uma matriz de estruturas [STATIONQUERY](stationquery.md) vazias que contém o número de elementos especificados em **nStationQueries**.</span><span class="sxs-lookup"><span data-stu-id="9d921-112">On input, an array of empty [STATIONQUERY](stationquery.md) structures that contains the number of elements specified in **nStationQueries**.</span></span>

<span data-ttu-id="9d921-113">Na saída, uma estrutura [STATIONQUERY](stationquery.md) preenchida para cada computador que está capturando dados.</span><span class="sxs-lookup"><span data-stu-id="9d921-113">On output, a filled [STATIONQUERY](stationquery.md) structure for each computer that is capturing data.</span></span> <span data-ttu-id="9d921-114">O número de elementos preenchidos é retornado por **nStationQueries**.</span><span class="sxs-lookup"><span data-stu-id="9d921-114">The number of filled elements is returned by **nStationQueries**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9d921-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="9d921-115">Remarks</span></span>

<span data-ttu-id="9d921-116">A memória para essa estrutura e a matriz [STATIONQUERY](stationquery.md) devem ser alocadas pelo aplicativo de chamada e liberadas depois que as informações não forem mais necessárias.</span><span class="sxs-lookup"><span data-stu-id="9d921-116">The memory for this structure and the [STATIONQUERY](stationquery.md) array must be allocated by the calling application and freed after the information is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d921-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d921-117">Requirements</span></span>



| <span data-ttu-id="9d921-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d921-118">Requirement</span></span> | <span data-ttu-id="9d921-119">Valor</span><span class="sxs-lookup"><span data-stu-id="9d921-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9d921-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9d921-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9d921-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9d921-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="9d921-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9d921-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9d921-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9d921-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9d921-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9d921-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d921-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d921-125"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d921-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="9d921-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d921-127">IDelaydC::QueryStations</span><span class="sxs-lookup"><span data-stu-id="9d921-127">IDelaydC::QueryStations</span></span>](idelaydc-querystations.md)
</dt> <dt>

[<span data-ttu-id="9d921-128">IESP::QueryStations</span><span class="sxs-lookup"><span data-stu-id="9d921-128">IESP::QueryStations</span></span>](iesp-querystations.md)
</dt> <dt>

[<span data-ttu-id="9d921-129">IRTC::QueryStations</span><span class="sxs-lookup"><span data-stu-id="9d921-129">IRTC::QueryStations</span></span>](irtc-querystations.md)
</dt> <dt>

[<span data-ttu-id="9d921-130">IStats::QueryStations</span><span class="sxs-lookup"><span data-stu-id="9d921-130">IStats::QueryStations</span></span>](istats-querystations.md)
</dt> <dt>

[<span data-ttu-id="9d921-131">STATIONQUERY</span><span class="sxs-lookup"><span data-stu-id="9d921-131">STATIONQUERY</span></span>](stationquery.md)
</dt> </dl>

 

 




