---
description: Contém informações sobre um processador.
ms.assetid: fa8c533c-3a54-4eb5-893f-649dfd8b4609
title: Estrutura de PROCESSOR_POWER_INFORMATION
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROCESSOR_POWER_INFORMATION
api_type:
- NA
api_location: ''
ms.openlocfilehash: 500a346080d7bf0c44d392a63a71310db74225a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296746"
---
# <a name="processor_power_information-structure"></a><span data-ttu-id="634de-103">Estrutura de informações de \_ energia do processador \_</span><span class="sxs-lookup"><span data-stu-id="634de-103">PROCESSOR\_POWER\_INFORMATION structure</span></span>

<span data-ttu-id="634de-104">Contém informações sobre um processador.</span><span class="sxs-lookup"><span data-stu-id="634de-104">Contains information about a processor.</span></span>

## <a name="syntax"></a><span data-ttu-id="634de-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="634de-105">Syntax</span></span>


```C++
typedef struct _PROCESSOR_POWER_INFORMATION {
  ULONG Number;
  ULONG MaxMhz;
  ULONG CurrentMhz;
  ULONG MhzLimit;
  ULONG MaxIdleState;
  ULONG CurrentIdleState;
} PROCESSOR_POWER_INFORMATION, *PPROCESSOR_POWER_INFORMATION;
```



## <a name="members"></a><span data-ttu-id="634de-106">Membros</span><span class="sxs-lookup"><span data-stu-id="634de-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="634de-107">**Número**</span><span class="sxs-lookup"><span data-stu-id="634de-107">**Number**</span></span>
</dt> <dd>

<span data-ttu-id="634de-108">O número do processador do sistema.</span><span class="sxs-lookup"><span data-stu-id="634de-108">The system processor number.</span></span>

</dd> <dt>

<span data-ttu-id="634de-109">**MaxMhz**</span><span class="sxs-lookup"><span data-stu-id="634de-109">**MaxMhz**</span></span>
</dt> <dd>

<span data-ttu-id="634de-110">A frequência de relógio máxima especificada do processador do sistema, em megahertz.</span><span class="sxs-lookup"><span data-stu-id="634de-110">The maximum specified clock frequency of the system processor, in megahertz.</span></span>

</dd> <dt>

<span data-ttu-id="634de-111">**CurrentMhz**</span><span class="sxs-lookup"><span data-stu-id="634de-111">**CurrentMhz**</span></span>
</dt> <dd>

<span data-ttu-id="634de-112">A frequência do relógio do processador, em megahertz.</span><span class="sxs-lookup"><span data-stu-id="634de-112">The processor clock frequency, in megahertz.</span></span> <span data-ttu-id="634de-113">Esse número é a frequência máxima de relógio do processador especificada multiplicada pelo acelerador atual do processador.</span><span class="sxs-lookup"><span data-stu-id="634de-113">This number is the maximum specified processor clock frequency multiplied by the current processor throttle.</span></span>

</dd> <dt>

<span data-ttu-id="634de-114">**MhzLimit**</span><span class="sxs-lookup"><span data-stu-id="634de-114">**MhzLimit**</span></span>
</dt> <dd>

<span data-ttu-id="634de-115">O limite da frequência do relógio do processador, em megahertz.</span><span class="sxs-lookup"><span data-stu-id="634de-115">The limit on the processor clock frequency, in megahertz.</span></span> <span data-ttu-id="634de-116">Esse número é a frequência máxima de relógio do processador especificada multiplicada pelo limite de aceleração térmica do processador atual.</span><span class="sxs-lookup"><span data-stu-id="634de-116">This number is the maximum specified processor clock frequency multiplied by the current processor thermal throttle limit.</span></span>

</dd> <dt>

<span data-ttu-id="634de-117">**MaxIdleState**</span><span class="sxs-lookup"><span data-stu-id="634de-117">**MaxIdleState**</span></span>
</dt> <dd>

<span data-ttu-id="634de-118">O estado ocioso máximo deste processador.</span><span class="sxs-lookup"><span data-stu-id="634de-118">The maximum idle state of this processor.</span></span>

</dd> <dt>

<span data-ttu-id="634de-119">**CurrentIdleState**</span><span class="sxs-lookup"><span data-stu-id="634de-119">**CurrentIdleState**</span></span>
</dt> <dd>

<span data-ttu-id="634de-120">O estado ocioso atual deste processador.</span><span class="sxs-lookup"><span data-stu-id="634de-120">The current idle state of this processor.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="634de-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="634de-121">Remarks</span></span>

<span data-ttu-id="634de-122">Observe que essa definição de estrutura foi acidentalmente omitida de WinNT. h.</span><span class="sxs-lookup"><span data-stu-id="634de-122">Note that this structure definition was accidentally omitted from WinNT.h.</span></span> <span data-ttu-id="634de-123">Esse erro será corrigido no futuro.</span><span class="sxs-lookup"><span data-stu-id="634de-123">This error will be corrected in the future.</span></span> <span data-ttu-id="634de-124">Enquanto isso, para compilar seu aplicativo, inclua a definição de estrutura contida neste tópico em seu código-fonte.</span><span class="sxs-lookup"><span data-stu-id="634de-124">In the meantime, to compile your application, include the structure definition contained in this topic in your source code.</span></span>

## <a name="requirements"></a><span data-ttu-id="634de-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="634de-125">Requirements</span></span>



| <span data-ttu-id="634de-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="634de-126">Requirement</span></span> | <span data-ttu-id="634de-127">Valor</span><span class="sxs-lookup"><span data-stu-id="634de-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="634de-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="634de-128">Minimum supported client</span></span><br/> | <span data-ttu-id="634de-129">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="634de-129">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="634de-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="634de-130">Minimum supported server</span></span><br/> | <span data-ttu-id="634de-131">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="634de-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="634de-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="634de-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="634de-133">**CallNtPowerInformation**</span><span class="sxs-lookup"><span data-stu-id="634de-133">**CallNtPowerInformation**</span></span>](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation)
</dt> </dl>

 

 




