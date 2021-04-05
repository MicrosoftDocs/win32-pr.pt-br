---
description: Contém informações sobre a inatividade do sistema.
ms.assetid: f6349b7c-1835-4492-95e3-9ce142628804
title: Estrutura de SYSTEM_POWER_INFORMATION
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SYSTEM_POWER_INFORMATION
api_type:
- NA
api_location: ''
ms.openlocfilehash: c32a8ad86b71ea680bd2961c9196a0896b055e5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921715"
---
# <a name="system_power_information-structure"></a><span data-ttu-id="b506d-103">Estrutura de informações de \_ energia do sistema \_</span><span class="sxs-lookup"><span data-stu-id="b506d-103">SYSTEM\_POWER\_INFORMATION structure</span></span>

<span data-ttu-id="b506d-104">Contém informações sobre a inatividade do sistema.</span><span class="sxs-lookup"><span data-stu-id="b506d-104">Contains information about the idleness of the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="b506d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b506d-105">Syntax</span></span>


```C++
typedef struct _SYSTEM_POWER_INFORMATION {
  ULONG MaxIdlenessAllowed;
  ULONG Idleness;
  ULONG TimeRemaining;
  UCHAR CoolingMode;
} SYSTEM_POWER_INFORMATION, *PSYSTEM_POWER_INFORMATION;
```



## <a name="members"></a><span data-ttu-id="b506d-106">Membros</span><span class="sxs-lookup"><span data-stu-id="b506d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b506d-107">**MaxIdlenessAllowed**</span><span class="sxs-lookup"><span data-stu-id="b506d-107">**MaxIdlenessAllowed**</span></span>
</dt> <dd>

<span data-ttu-id="b506d-108">A ociosidade na qual o sistema é considerado ocioso e o tempo limite ocioso começa a contar, expresso como uma porcentagem.</span><span class="sxs-lookup"><span data-stu-id="b506d-108">The idleness at which the system is considered idle and the idle time-out begins counting, expressed as a percentage.</span></span> <span data-ttu-id="b506d-109">Descartar abaixo desse número faz com que o temporizador seja cancelado.</span><span class="sxs-lookup"><span data-stu-id="b506d-109">Dropping below this number causes the timer to be canceled.</span></span>

</dd> <dt>

<span data-ttu-id="b506d-110">**Ociosidade**</span><span class="sxs-lookup"><span data-stu-id="b506d-110">**Idleness**</span></span>
</dt> <dd>

<span data-ttu-id="b506d-111">O nível ocioso atual, expresso como uma porcentagem.</span><span class="sxs-lookup"><span data-stu-id="b506d-111">The current idle level, expressed as a percentage.</span></span>

</dd> <dt>

<span data-ttu-id="b506d-112">**TimeRemaining**</span><span class="sxs-lookup"><span data-stu-id="b506d-112">**TimeRemaining**</span></span>
</dt> <dd>

<span data-ttu-id="b506d-113">O tempo restante no temporizador ocioso, em segundos.</span><span class="sxs-lookup"><span data-stu-id="b506d-113">The time remaining in the idle timer, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="b506d-114">**Coolmode**</span><span class="sxs-lookup"><span data-stu-id="b506d-114">**CoolingMode**</span></span>
</dt> <dd>

<span data-ttu-id="b506d-115">O modo de resfriamento do sistema atual.</span><span class="sxs-lookup"><span data-stu-id="b506d-115">The current system cooling mode.</span></span> <span data-ttu-id="b506d-116">Esse membro deve ter um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="b506d-116">This member must one of the following values.</span></span>



| <span data-ttu-id="b506d-117">Valor</span><span class="sxs-lookup"><span data-stu-id="b506d-117">Value</span></span>                                                                                                                                                                                                                                 | <span data-ttu-id="b506d-118">Significado</span><span class="sxs-lookup"><span data-stu-id="b506d-118">Meaning</span></span>                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span id="PO_TZ_ACTIVE"></span><span id="po_tz_active"></span><dl> <span data-ttu-id="b506d-119"><dt>**Po \_ TZ \_ ativo**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b506d-119"><dt>**PO\_TZ\_ACTIVE**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="b506d-120">O sistema está atualmente no modo de resfriamento ativo.</span><span class="sxs-lookup"><span data-stu-id="b506d-120">The system is currently in Active cooling mode.</span></span><br/>                                                |
| <span id="PO_TZ_INVALID_MODE"></span><span id="po_tz_invalid_mode"></span><dl> <span data-ttu-id="b506d-121"><dt>**Po \_ \_ \_ Modo inválido de TZ**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="b506d-121"><dt>**PO\_TZ\_INVALID\_MODE**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="b506d-122">O sistema não dá suporte à limitação da CPU ou não há zona termal definida no sistema.</span><span class="sxs-lookup"><span data-stu-id="b506d-122">The system does not support CPU throttling, or there is no thermal zone defined in the system.</span></span><br/> |
| <span id="PO_TZ_PASSIVE"></span><span id="po_tz_passive"></span><dl> <span data-ttu-id="b506d-123"><dt>**Po \_ TZ \_ passivo**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="b506d-123"><dt>**PO\_TZ\_PASSIVE**</dt> <dt>1</dt></span></span> </dl>                 | <span data-ttu-id="b506d-124">O sistema está atualmente no modo de resfriamento passivo.</span><span class="sxs-lookup"><span data-stu-id="b506d-124">The system is currently in Passive cooling mode.</span></span><br/>                                               |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b506d-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="b506d-125">Remarks</span></span>

<span data-ttu-id="b506d-126">Observe que essa definição de estrutura foi acidentalmente omitida de WinNT. h.</span><span class="sxs-lookup"><span data-stu-id="b506d-126">Note that this structure definition was accidentally omitted from WinNT.h.</span></span> <span data-ttu-id="b506d-127">Esse erro será corrigido no futuro.</span><span class="sxs-lookup"><span data-stu-id="b506d-127">This error will be corrected in the future.</span></span> <span data-ttu-id="b506d-128">Enquanto isso, para compilar seu aplicativo, inclua a definição de estrutura contida neste tópico em seu código-fonte.</span><span class="sxs-lookup"><span data-stu-id="b506d-128">In the meantime, to compile your application, include the structure definition contained in this topic in your source code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b506d-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b506d-129">Requirements</span></span>



| <span data-ttu-id="b506d-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="b506d-130">Requirement</span></span> | <span data-ttu-id="b506d-131">Valor</span><span class="sxs-lookup"><span data-stu-id="b506d-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b506d-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b506d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b506d-133">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b506d-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="b506d-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b506d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b506d-135">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b506d-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b506d-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="b506d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b506d-137">**CallNtPowerInformation**</span><span class="sxs-lookup"><span data-stu-id="b506d-137">**CallNtPowerInformation**</span></span>](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation)
</dt> </dl>

 

 




