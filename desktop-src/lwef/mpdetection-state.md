---
title: Enumeração de MPDETECTION_STATE (MpClient. h)
description: O estado da ameaça detectada no momento.
ms.assetid: 293771FF-A210-41D0-88A5-3B52ACAA9295
keywords:
- Recursos do ambiente Windows herdado de enumeração de MPDETECTION_STATE
- PMPDETECTION_STATE recursos de ambiente herdados do ponteiro de enumeração do Windows
topic_type:
- apiref
api_name:
- MPDETECTION_STATE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9265a15641d2072d87b33af2782f17974bf07be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454945"
---
# <a name="mpdetection_state-enumeration"></a><span data-ttu-id="012e5-105">\_Enumeração de estado MPDETECTION</span><span class="sxs-lookup"><span data-stu-id="012e5-105">MPDETECTION\_STATE enumeration</span></span>

<span data-ttu-id="012e5-106">O estado da ameaça detectada no momento.</span><span class="sxs-lookup"><span data-stu-id="012e5-106">The state of the currently detected threat.</span></span>

## <a name="syntax"></a><span data-ttu-id="012e5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="012e5-107">Syntax</span></span>


```C++
typedef enum tagMPDETECTION_STATE { 
  MPDETECTION_STATE_UNKNOWN             = 0,
  MPDETECTION_STATE_ACTIVE              = 1,
  MPDETECTION_STATE_FINISHED            = 2,
  MPDETECTION_STATE_ADDITIONAL_ACTIONS  = 3,
  MPDETECTION_STATE_FAILED              = 4,
  MPDETECTION_STATE_CRITICALLY_FAILED   = 5,
  MPDETECTION_STATE_CLEARED             = 6
} MPDETECTION_STATE, *PMPDETECTION_STATE;
```



## <a name="constants"></a><span data-ttu-id="012e5-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="012e5-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="012e5-109"><span id="MPDETECTION_STATE_UNKNOWN"></span><span id="mpdetection_state_unknown"></span>**Estado de MPDETECTION \_ \_ desconhecido**</span><span class="sxs-lookup"><span data-stu-id="012e5-109"><span id="MPDETECTION_STATE_UNKNOWN"></span><span id="mpdetection_state_unknown"></span>**MPDETECTION\_STATE\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="012e5-110">Em um estado de erro.</span><span class="sxs-lookup"><span data-stu-id="012e5-110">In an error state.</span></span>

</dd> <dt>

<span data-ttu-id="012e5-111"><span id="MPDETECTION_STATE_ACTIVE"></span><span id="mpdetection_state_active"></span>**\_estado \_ ativo do MPDETECTION**</span><span class="sxs-lookup"><span data-stu-id="012e5-111"><span id="MPDETECTION_STATE_ACTIVE"></span><span id="mpdetection_state_active"></span>**MPDETECTION\_STATE\_ACTIVE**</span></span>
</dt> <dd>

<span data-ttu-id="012e5-112">Ameaça ativa.</span><span class="sxs-lookup"><span data-stu-id="012e5-112">Active threat.</span></span>

</dd> <dt>

<span data-ttu-id="012e5-113"><span id="MPDETECTION_STATE_FINISHED"></span><span id="mpdetection_state_finished"></span>**\_estado MPDETECTION \_ concluído**</span><span class="sxs-lookup"><span data-stu-id="012e5-113"><span id="MPDETECTION_STATE_FINISHED"></span><span id="mpdetection_state_finished"></span>**MPDETECTION\_STATE\_FINISHED**</span></span>
</dt> <dd>

<span data-ttu-id="012e5-114">24 horas pendentes para mover para limpo.</span><span class="sxs-lookup"><span data-stu-id="012e5-114">Pending 24 hours to a move to cleared.</span></span>

</dd> <dt>

<span data-ttu-id="012e5-115"><span id="MPDETECTION_STATE_ADDITIONAL_ACTIONS"></span><span id="mpdetection_state_additional_actions"></span>**\_ \_ ações adicionais de estado MPDETECTION \_**</span><span class="sxs-lookup"><span data-stu-id="012e5-115"><span id="MPDETECTION_STATE_ADDITIONAL_ACTIONS"></span><span id="mpdetection_state_additional_actions"></span>**MPDETECTION\_STATE\_ADDITIONAL\_ACTIONS**</span></span>
</dt> <dd>

<span data-ttu-id="012e5-116">Ações adicionais necessárias.</span><span class="sxs-lookup"><span data-stu-id="012e5-116">Additional actions required.</span></span>

</dd> <dt>

<span data-ttu-id="012e5-117"><span id="MPDETECTION_STATE_FAILED"></span><span id="mpdetection_state_failed"></span>**\_ \_ falha no estado MPDETECTION**</span><span class="sxs-lookup"><span data-stu-id="012e5-117"><span id="MPDETECTION_STATE_FAILED"></span><span id="mpdetection_state_failed"></span>**MPDETECTION\_STATE\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="012e5-118">Falha de correção não crítica.</span><span class="sxs-lookup"><span data-stu-id="012e5-118">Non-critical remediation failure.</span></span>

</dd> <dt>

<span data-ttu-id="012e5-119"><span id="MPDETECTION_STATE_CRITICALLY_FAILED"></span><span id="mpdetection_state_critically_failed"></span>**o \_ estado MPDETECTION \_ falhou criticamente \_**</span><span class="sxs-lookup"><span data-stu-id="012e5-119"><span id="MPDETECTION_STATE_CRITICALLY_FAILED"></span><span id="mpdetection_state_critically_failed"></span>**MPDETECTION\_STATE\_CRITICALLY\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="012e5-120">Falha de correção crítica.</span><span class="sxs-lookup"><span data-stu-id="012e5-120">Critical remediation failure.</span></span>

</dd> <dt>

<span data-ttu-id="012e5-121"><span id="MPDETECTION_STATE_CLEARED"></span><span id="mpdetection_state_cleared"></span>**\_estado MPDETECTION \_ limpo**</span><span class="sxs-lookup"><span data-stu-id="012e5-121"><span id="MPDETECTION_STATE_CLEARED"></span><span id="mpdetection_state_cleared"></span>**MPDETECTION\_STATE\_CLEARED**</span></span>
</dt> <dd>

<span data-ttu-id="012e5-122">A ameaça não aparece na consulta de estado, somente no histórico.</span><span class="sxs-lookup"><span data-stu-id="012e5-122">Threat does not show up in the state query, only in history.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="012e5-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="012e5-123">Requirements</span></span>



| <span data-ttu-id="012e5-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="012e5-124">Requirement</span></span> | <span data-ttu-id="012e5-125">Valor</span><span class="sxs-lookup"><span data-stu-id="012e5-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="012e5-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="012e5-126">Minimum supported client</span></span><br/> | <span data-ttu-id="012e5-127">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="012e5-127">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="012e5-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="012e5-128">Minimum supported server</span></span><br/> | <span data-ttu-id="012e5-129">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="012e5-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="012e5-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="012e5-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="012e5-131"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="012e5-131"><dt>MpClient.h</dt></span></span> </dl> |



 

 





