---
title: Enumeração SwarmStatus (Deliveryoptimization. h)
description: Define o status de um arquivo dentro do cliente de otimização de entrega.
ms.assetid: D40ABDD3-5573-4A8D-8608-4CB0F396CCAD
keywords:
- Enumeração SwarmStatus
topic_type:
- apiref
api_name:
- SwarmStatus
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3622f819679c2fd2b28d66e371a8b88e0a2d2f70
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086102"
---
# <a name="swarmstatus-enumeration"></a><span data-ttu-id="7d3fb-104">Enumeração SwarmStatus</span><span class="sxs-lookup"><span data-stu-id="7d3fb-104">SwarmStatus enumeration</span></span>

<span data-ttu-id="7d3fb-105">Define o status de um arquivo dentro do cliente de otimização de entrega.</span><span class="sxs-lookup"><span data-stu-id="7d3fb-105">Defines the status of a file within the delivery optimization client.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d3fb-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d3fb-106">Syntax</span></span>


```C++
typedef enum _SwarmStatus { 
  SwarmStatus_Downloading  = 0,
  SwarmStatus_Complete     = 1,
  SwarmStatus_Caching      = 2,
  SwarmStatus_Paused       = 3
} SwarmStatus;
```



## <a name="constants"></a><span data-ttu-id="7d3fb-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="7d3fb-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7d3fb-108"><span id="SwarmStatus_Downloading"></span><span id="swarmstatus_downloading"></span><span id="SWARMSTATUS_DOWNLOADING"></span>**SwarmStatus_Downloading**</span><span class="sxs-lookup"><span data-stu-id="7d3fb-108"><span id="SwarmStatus_Downloading"></span><span id="swarmstatus_downloading"></span><span id="SWARMSTATUS_DOWNLOADING"></span>**SwarmStatus_Downloading**</span></span>
</dt> <dd>

<span data-ttu-id="7d3fb-109">O arquivo está sendo baixado.</span><span class="sxs-lookup"><span data-stu-id="7d3fb-109">The file is downloading.</span></span>

</dd> <dt>

<span data-ttu-id="7d3fb-110"><span id="SwarmStatus_Complete"></span><span id="swarmstatus_complete"></span><span id="SWARMSTATUS_COMPLETE"></span>**SwarmStatus_Complete**</span><span class="sxs-lookup"><span data-stu-id="7d3fb-110"><span id="SwarmStatus_Complete"></span><span id="swarmstatus_complete"></span><span id="SWARMSTATUS_COMPLETE"></span>**SwarmStatus_Complete**</span></span>
</dt> <dd>

<span data-ttu-id="7d3fb-111">O download do arquivo foi concluído.</span><span class="sxs-lookup"><span data-stu-id="7d3fb-111">The file download is complete.</span></span>

</dd> <dt>

<span data-ttu-id="7d3fb-112"><span id="SwarmStatus_Caching"></span><span id="swarmstatus_caching"></span><span id="SWARMSTATUS_CACHING"></span>**SwarmStatus_Caching**</span><span class="sxs-lookup"><span data-stu-id="7d3fb-112"><span id="SwarmStatus_Caching"></span><span id="swarmstatus_caching"></span><span id="SWARMSTATUS_CACHING"></span>**SwarmStatus_Caching**</span></span>
</dt> <dd>

<span data-ttu-id="7d3fb-113">O arquivo está sendo armazenado em cache.</span><span class="sxs-lookup"><span data-stu-id="7d3fb-113">The file is being cached.</span></span>

</dd> <dt>

<span data-ttu-id="7d3fb-114"><span id="SwarmStatus_Paused"></span><span id="swarmstatus_paused"></span><span id="SWARMSTATUS_PAUSED"></span>**SwarmStatus_Paused**</span><span class="sxs-lookup"><span data-stu-id="7d3fb-114"><span id="SwarmStatus_Paused"></span><span id="swarmstatus_paused"></span><span id="SWARMSTATUS_PAUSED"></span>**SwarmStatus_Paused**</span></span>
</dt> <dd>

<span data-ttu-id="7d3fb-115">O download do arquivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="7d3fb-115">The file download is paused.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7d3fb-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d3fb-116">Requirements</span></span>



| <span data-ttu-id="7d3fb-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d3fb-117">Requirement</span></span> | <span data-ttu-id="7d3fb-118">Valor</span><span class="sxs-lookup"><span data-stu-id="7d3fb-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d3fb-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7d3fb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7d3fb-120">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="7d3fb-120">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7d3fb-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7d3fb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7d3fb-122">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="7d3fb-122">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7d3fb-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7d3fb-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d3fb-124"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d3fb-124"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



 

 





