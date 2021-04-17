---
title: SystemMonitor.Batmétodo chingLock
description: Bloqueia o monitor do sistema para impedi-lo de amostragem de dados do contador do contador ou arquivo de log recém-adicionado.
ms.assetid: 6b9d683a-7a97-44a4-9eb6-6caaafe2abdd
keywords:
- Método BatchingLock SysMon
- Método BatchingLock SysMon, objeto SystemMonitor
- Objeto SystemMonitor SysMon, método BatchingLock
topic_type:
- apiref
api_name:
- SystemMonitor.BatchingLock
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b858a6920b039d911ae571d81744eb99dea4ef4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105762878"
---
# <a name="systemmonitorbatchinglock-method"></a><span data-ttu-id="1b781-106">SystemMonitor.Batmétodo chingLock</span><span class="sxs-lookup"><span data-stu-id="1b781-106">SystemMonitor.BatchingLock method</span></span>

<span data-ttu-id="1b781-107">Bloqueia o monitor do sistema para impedi-lo de amostragem de dados do contador do contador ou arquivo de log recém-adicionado.</span><span class="sxs-lookup"><span data-stu-id="1b781-107">Locks the System Monitor to prevent it from sampling counter data from the newly added counter or log file.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b781-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1b781-108">Syntax</span></span>


```VB
SystemMonitor.BatchingLock( _
  ByVal lock As Boolean, _
  ByVal batchReason As SysmonBatchReason _
)
```



## <a name="parameters"></a><span data-ttu-id="1b781-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1b781-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b781-110">*Bloquear* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1b781-110">*lock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b781-111">Defina como true para bloquear o monitor do sistema para impedir que ele faça amostragem de dados do contador do contador ou arquivo de log recém-adicionado.</span><span class="sxs-lookup"><span data-stu-id="1b781-111">Set to True to lock the System Monitor to prevent it from sampling counter data from the newly added counter or log file.</span></span> <span data-ttu-id="1b781-112">Defina como false para remover o bloqueio.</span><span class="sxs-lookup"><span data-stu-id="1b781-112">Set to False to remove the lock.</span></span>

</dd> <dt>

<span data-ttu-id="1b781-113">*batchReason* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1b781-113">*batchReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b781-114">Identifica a origem dos dados que você está bloqueando.</span><span class="sxs-lookup"><span data-stu-id="1b781-114">Identifies the source of the data that you are locking.</span></span> <span data-ttu-id="1b781-115">Use o mesmo valor de motivo ao bloquear e desbloquear o recurso.</span><span class="sxs-lookup"><span data-stu-id="1b781-115">Use the same reason value when locking and unlocking the resource.</span></span> <span data-ttu-id="1b781-116">Para obter os valores possíveis, consulte a enumeração [**SysmonBatchReason**](/windows/win32/api/isysmon/ne-isysmon-sysmonbatchreason) .</span><span class="sxs-lookup"><span data-stu-id="1b781-116">For possible values, see the [**SysmonBatchReason**](/windows/win32/api/isysmon/ne-isysmon-sysmonbatchreason) enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b781-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1b781-117">Return value</span></span>

<span data-ttu-id="1b781-118">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="1b781-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b781-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="1b781-119">Remarks</span></span>

<span data-ttu-id="1b781-120">Você deve chamar esse método duas vezes, uma vez para bloquear a origem (true) e uma vez para desbloquear a origem (false).</span><span class="sxs-lookup"><span data-stu-id="1b781-120">You must call this method twice, once to lock the source (True) and once to unlock the source (False).</span></span>

<span data-ttu-id="1b781-121">Você pode posicionar apenas um bloqueio.</span><span class="sxs-lookup"><span data-stu-id="1b781-121">You can place only one lock.</span></span> <span data-ttu-id="1b781-122">Por exemplo, se você definir o bloqueio para SysmonBatchAddFiles e, em seguida, fizer uma segunda chamada usando SysmonBatchAddCounters como o motivo, a segunda chamada removerá o bloqueio colocado pela primeira chamada.</span><span class="sxs-lookup"><span data-stu-id="1b781-122">For example, if you set the lock for SysmonBatchAddFiles and then make a second call using SysmonBatchAddCounters as the reason, the second call removes the lock placed by the first call.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b781-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b781-123">Requirements</span></span>



| <span data-ttu-id="1b781-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b781-124">Requirement</span></span> | <span data-ttu-id="1b781-125">Valor</span><span class="sxs-lookup"><span data-stu-id="1b781-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1b781-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1b781-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1b781-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1b781-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1b781-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1b781-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1b781-129">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1b781-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1b781-130">DLL</span><span class="sxs-lookup"><span data-stu-id="1b781-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b781-131"><dt>Sysmon. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="1b781-131"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b781-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="1b781-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b781-133">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="1b781-133">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





