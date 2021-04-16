---
description: Armazena informações sobre as seções de memória compartilhada.
ms.assetid: 73a650ee-110c-43f2-a5e2-783d52fd29ee
title: Estrutura de SHAREDMEMORY_HEADER
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SHAREDMEMORY_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: 695f3ef09cb5e7e67de757ee3926df6fde7ddff5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105775647"
---
# <a name="sharedmemory_header-structure"></a><span data-ttu-id="40d32-103">\_Estrutura de cabeçalho SHAREDMEMORY</span><span class="sxs-lookup"><span data-stu-id="40d32-103">SHAREDMEMORY\_HEADER structure</span></span>

<span data-ttu-id="40d32-104">Armazena informações sobre as seções de memória compartilhada.</span><span class="sxs-lookup"><span data-stu-id="40d32-104">Stores information about shared memory sections.</span></span>

## <a name="syntax"></a><span data-ttu-id="40d32-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="40d32-105">Syntax</span></span>


```C++
typedef struct _SHAREDMEMORY_HEADER {
  DWORD             cbTotal;
  DWORD             cbOffsetSns;
  DWORD             idxEvent;
  DWORD             dwEvent;
  CURSOR_ID         cid;
  DWORD             sn;
  SYSTEM_EVENT      sysEvt;
  SYSTEM_EVENT_DATA sysEvtData;
  DWORD             cPackets;
  DWORD             cbPackets;
  BOOL              fSnsPresent;
} SHAREDMEMORY_HEADER, *PSHAREDMEMORY_HEADER;
```



## <a name="members"></a><span data-ttu-id="40d32-106">Membros</span><span class="sxs-lookup"><span data-stu-id="40d32-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="40d32-107">**cbTotal**</span><span class="sxs-lookup"><span data-stu-id="40d32-107">**cbTotal**</span></span>
</dt> <dd>

<span data-ttu-id="40d32-108">O tamanho, em bytes, dos dados referenciados por essa estrutura de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="40d32-108">The size, in bytes, of the data referenced by this header structure.</span></span>

</dd> <dt>

<span data-ttu-id="40d32-109">**cbOffsetSns**</span><span class="sxs-lookup"><span data-stu-id="40d32-109">**cbOffsetSns**</span></span>
</dt> <dd>

<span data-ttu-id="40d32-110">O tamanho, em bytes, que os números de série são deslocados da estrutura de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="40d32-110">The size, in bytes, that the serial numbers are offset from the header structure.</span></span>

</dd> <dt>

<span data-ttu-id="40d32-111">**idxEvent**</span><span class="sxs-lookup"><span data-stu-id="40d32-111">**idxEvent**</span></span>
</dt> <dd>

<span data-ttu-id="40d32-112">O índice de eventos.</span><span class="sxs-lookup"><span data-stu-id="40d32-112">The event index.</span></span> <span data-ttu-id="40d32-113">Esse valor é incrementado com eventos sucessivos.</span><span class="sxs-lookup"><span data-stu-id="40d32-113">This value is incremented with successive events.</span></span>

</dd> <dt>

<span data-ttu-id="40d32-114">**dwEvent**</span><span class="sxs-lookup"><span data-stu-id="40d32-114">**dwEvent**</span></span>
</dt> <dd>

<span data-ttu-id="40d32-115">O evento associado a este cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="40d32-115">The event associated with this header.</span></span>

</dd> <dt>

<span data-ttu-id="40d32-116">**CID**</span><span class="sxs-lookup"><span data-stu-id="40d32-116">**cid**</span></span>
</dt> <dd>

<span data-ttu-id="40d32-117">O identificador de cursor referenciado pelo cabeçalho da memória compartilhada.</span><span class="sxs-lookup"><span data-stu-id="40d32-117">The cursor identifier referenced by the shared memory header.</span></span>

</dd> <dt>

<span data-ttu-id="40d32-118">**sn**</span><span class="sxs-lookup"><span data-stu-id="40d32-118">**sn**</span></span>
</dt> <dd>

<span data-ttu-id="40d32-119">O número de série do cabeçalho da memória compartilhada.</span><span class="sxs-lookup"><span data-stu-id="40d32-119">The serial number for the shared memory header.</span></span>

</dd> <dt>

<span data-ttu-id="40d32-120">**sysEvt**</span><span class="sxs-lookup"><span data-stu-id="40d32-120">**sysEvt**</span></span>
</dt> <dd>

<span data-ttu-id="40d32-121">O evento do sistema, prefixado SE \_ \* , associado a esse cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="40d32-121">The system event, prefixed SE\_\*, associated with this header.</span></span> <span data-ttu-id="40d32-122">Consulte a seção de comentários para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="40d32-122">See the remarks section for more information.</span></span>

</dd> <dt>

<span data-ttu-id="40d32-123">**sysEvtData**</span><span class="sxs-lookup"><span data-stu-id="40d32-123">**sysEvtData**</span></span>
</dt> <dd>

<span data-ttu-id="40d32-124">A estrutura de [**\_ \_ dados de evento do sistema**](/windows/win32/api/tpcshrd/ns-tpcshrd-system_event_data) associada ao evento do sistema.</span><span class="sxs-lookup"><span data-stu-id="40d32-124">The [**SYSTEM\_EVENT\_DATA**](/windows/win32/api/tpcshrd/ns-tpcshrd-system_event_data) structure associated with the system event.</span></span>

</dd> <dt>

<span data-ttu-id="40d32-125">**cPackets**</span><span class="sxs-lookup"><span data-stu-id="40d32-125">**cPackets**</span></span>
</dt> <dd>

<span data-ttu-id="40d32-126">Uma contagem dos pacotes associados à seção de memória compartilhada atual.</span><span class="sxs-lookup"><span data-stu-id="40d32-126">A count of the packets associated with the current shared memory section.</span></span>

</dd> <dt>

<span data-ttu-id="40d32-127">**cbPackets**</span><span class="sxs-lookup"><span data-stu-id="40d32-127">**cbPackets**</span></span>
</dt> <dd>

<span data-ttu-id="40d32-128">O tamanho, em bytes, dos pacotes associados à seção de memória compartilhada atual.</span><span class="sxs-lookup"><span data-stu-id="40d32-128">The size, in bytes, of the packets associated with the current shared memory section.</span></span>

</dd> <dt>

<span data-ttu-id="40d32-129">**fSnsPresent**</span><span class="sxs-lookup"><span data-stu-id="40d32-129">**fSnsPresent**</span></span>
</dt> <dd>

<span data-ttu-id="40d32-130">Um sinalizador que indica se os números de série estão presentes na seção de memória compartilhada atual.</span><span class="sxs-lookup"><span data-stu-id="40d32-130">A flag indicating whether serial numbers are present in the current shared memory section.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="40d32-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="40d32-131">Remarks</span></span>

<span data-ttu-id="40d32-132">Os valores a seguir são definidos para o membro **sysEvt** .</span><span class="sxs-lookup"><span data-stu-id="40d32-132">The following values are defined for the **sysEvt** member.</span></span>


```C++
#define SE_NONE                  0x00000000
#define SE_TAP                   0x00000010
#define SE_DBL_TAP               0x00000011
#define SE_RIGHT_TAP             0x00000012
#define SE_DRAG                  0x00000013
#define SE_RIGHT_DRAG            0x00000014
#define SE_HOLD_ENTER            0x00000015
#define SE_HOLD_LEAVE            0x00000016
#define SE_HOVER_ENTER           0x00000017
#define SE_HOVER_LEAVE           0x00000018
#define SE_FLICK                 0x0000001F
```



## <a name="see-also"></a><span data-ttu-id="40d32-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="40d32-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40d32-134">**\_dados de evento do sistema \_**</span><span class="sxs-lookup"><span data-stu-id="40d32-134">**SYSTEM\_EVENT\_DATA**</span></span>](/windows/win32/api/tpcshrd/ns-tpcshrd-system_event_data)
</dt> </dl>

 

 



