---
title: Estrutura de BG_JOB_TIMES (Deliveryoptimization. h)
description: A estrutura de BG_JOB_TIMES fornece carimbos de data/hora relacionados ao trabalho.
ms.assetid: 0147478F-C850-4B66-AB15-042C1A81D6B5
keywords:
- Estrutura de BG_JOB_TIMES
topic_type:
- apiref
api_name:
- BG_JOB_TIMES
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0a2d4e56bb616254537e26fc1ba0fdf5b9e251a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644355"
---
# <a name="bg_job_times-structure"></a><span data-ttu-id="fc835-104">Estrutura de BG_JOB_TIMES</span><span class="sxs-lookup"><span data-stu-id="fc835-104">BG_JOB_TIMES structure</span></span>

<span data-ttu-id="fc835-105">A estrutura de **BG_JOB_TIMES** fornece carimbos de data/hora relacionados ao trabalho.</span><span class="sxs-lookup"><span data-stu-id="fc835-105">The **BG_JOB_TIMES** structure provides job-related time stamps.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc835-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fc835-106">Syntax</span></span>


```C++
typedef struct _BG_JOB_TIMES {
  FILETIME CreationTime;
  FILETIME ModificationTime;
  FILETIME TransferCompletionTime;
} BG_JOB_TIMES;
```



## <a name="members"></a><span data-ttu-id="fc835-107">Membros</span><span class="sxs-lookup"><span data-stu-id="fc835-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="fc835-108">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="fc835-108">**CreationTime**</span></span>
</dt> <dd>

<span data-ttu-id="fc835-109">Hora em que o trabalho foi criado.</span><span class="sxs-lookup"><span data-stu-id="fc835-109">Time the job was created.</span></span> <span data-ttu-id="fc835-110">A hora é especificada como [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="fc835-110">The time is specified as [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="fc835-111">**Modificatime**</span><span class="sxs-lookup"><span data-stu-id="fc835-111">**ModificationTime**</span></span>
</dt> <dd>

<span data-ttu-id="fc835-112">Hora em que o trabalho foi modificado pela última vez ou os bytes foram transferidos.</span><span class="sxs-lookup"><span data-stu-id="fc835-112">Time the job was last modified or bytes were transferred.</span></span> <span data-ttu-id="fc835-113">Adicionar arquivos ou chamar qualquer um dos métodos set nas interfaces [ \* *método ibackgroundcopyjob \** _](/previous-versions//mt811348(v=vs.85)) altera esse valor.</span><span class="sxs-lookup"><span data-stu-id="fc835-113">Adding files or calling any of the set methods in the [\**IBackgroundCopyJob\** _](/previous-versions//mt811348(v=vs.85)) interfaces changes this value.</span></span> <span data-ttu-id="fc835-114">Além disso, as alterações no estado do trabalho e na chamada dos [métodos *_ suspender* \*](ibackgroundcopyjob-suspend.md), [**retomar**](ibackgroundcopyjob-resume.md), [**Cancelar**](ibackgroundcopyjob-cancel.md)e [**concluir**](ibackgroundcopyjob-complete.md) alteram esse valor.</span><span class="sxs-lookup"><span data-stu-id="fc835-114">In addition, changes to the state of the job and calling the [_ *Suspend*\*](ibackgroundcopyjob-suspend.md), [**Resume**](ibackgroundcopyjob-resume.md), [**Cancel**](ibackgroundcopyjob-cancel.md), and [**Complete**](ibackgroundcopyjob-complete.md) methods change this value.</span></span> <span data-ttu-id="fc835-115">A hora é especificada como [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="fc835-115">The time is specified as [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="fc835-116">**TransferCompletionTime**</span><span class="sxs-lookup"><span data-stu-id="fc835-116">**TransferCompletionTime**</span></span>
</dt> <dd>

<span data-ttu-id="fc835-117">Hora em que o trabalho entrou no estado de BG_JOB_STATE_TRANSFERRED.</span><span class="sxs-lookup"><span data-stu-id="fc835-117">Time the job entered the BG_JOB_STATE_TRANSFERRED state.</span></span> <span data-ttu-id="fc835-118">A hora é especificada como [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime).</span><span class="sxs-lookup"><span data-stu-id="fc835-118">The time is specified as [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fc835-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc835-119">Requirements</span></span>



| <span data-ttu-id="fc835-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc835-120">Requirement</span></span> | <span data-ttu-id="fc835-121">Valor</span><span class="sxs-lookup"><span data-stu-id="fc835-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc835-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fc835-122">Minimum supported client</span></span><br/> | <span data-ttu-id="fc835-123">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="fc835-123">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="fc835-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fc835-124">Minimum supported server</span></span><br/> | <span data-ttu-id="fc835-125">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="fc835-125">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="fc835-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fc835-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc835-127"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc835-127"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc835-128">Consulte também</span><span class="sxs-lookup"><span data-stu-id="fc835-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc835-129">**Método ibackgroundcopyjob:: gettimes**</span><span class="sxs-lookup"><span data-stu-id="fc835-129">**IBackgroundCopyJob::GetTimes**</span></span>](ibackgroundcopyjob-gettimes.md)
</dt> </dl>

 

