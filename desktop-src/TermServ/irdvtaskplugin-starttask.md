---
title: Método IRDVTaskPlugin StartTask
description: Chamado para iniciar a tarefa de atualização na máquina virtual.
ms.assetid: c1e9f18b-1e83-4a29-8646-8adde94e8c14
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método StartTask
- Método StartTask Serviços de Área de Trabalho Remota, interface IRDVTaskPlugin
- Serviços de Área de Trabalho Remota de interface IRDVTaskPlugin, método StartTask
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.StartTask
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 51c499549378700a90d8fc78d075bc07c1f874cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455383"
---
# <a name="irdvtaskpluginstarttask-method"></a><span data-ttu-id="88b2d-106">Método IRDVTaskPlugin:: StartTask</span><span class="sxs-lookup"><span data-stu-id="88b2d-106">IRDVTaskPlugin::StartTask method</span></span>

<span data-ttu-id="88b2d-107">Chamado para iniciar a tarefa de atualização na máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="88b2d-107">Called to start the update task on the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="88b2d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="88b2d-108">Syntax</span></span>


```C++
HRESULT StartTask(
  [in] BSTR            Label,
  [in] BSTR            Identifier,
  [in] SAFEARRAY(BYTE) *Context
);
```



## <a name="parameters"></a><span data-ttu-id="88b2d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="88b2d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88b2d-110">*Rótulo* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="88b2d-110">*Label* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88b2d-111">O rótulo da tarefa.</span><span class="sxs-lookup"><span data-stu-id="88b2d-111">The label for the task.</span></span> <span data-ttu-id="88b2d-112">Esse é o rótulo que foi passado para o agente de gatilho no método [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) .</span><span class="sxs-lookup"><span data-stu-id="88b2d-112">This is the label that was passed to the trigger agent in the [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="88b2d-113">*Identificador* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="88b2d-113">*Identifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88b2d-114">O identificador da tarefa.</span><span class="sxs-lookup"><span data-stu-id="88b2d-114">The identifier of the task.</span></span> <span data-ttu-id="88b2d-115">Esse é o identificador que foi passado para o agente de gatilho no método [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) .</span><span class="sxs-lookup"><span data-stu-id="88b2d-115">This is the identifier that was passed to the trigger agent in the [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="88b2d-116">*Contexto* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="88b2d-116">*Context* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88b2d-117">Dados opcionais para a tarefa.</span><span class="sxs-lookup"><span data-stu-id="88b2d-117">Optional data for the task.</span></span> <span data-ttu-id="88b2d-118">Esses são os dados que foram passados para o agente de gatilho no método [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) .</span><span class="sxs-lookup"><span data-stu-id="88b2d-118">This is the data that was passed to the trigger agent in the [**ScheduleTask**](irdvtaskpluginnotifysink-scheduletask.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88b2d-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="88b2d-119">Return value</span></span>

<span data-ttu-id="88b2d-120">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="88b2d-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="88b2d-121">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="88b2d-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="88b2d-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88b2d-122">Requirements</span></span>



| <span data-ttu-id="88b2d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="88b2d-123">Requirement</span></span> | <span data-ttu-id="88b2d-124">Valor</span><span class="sxs-lookup"><span data-stu-id="88b2d-124">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="88b2d-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="88b2d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="88b2d-126">Windows 7 Enterprise</span><span class="sxs-lookup"><span data-stu-id="88b2d-126">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="88b2d-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="88b2d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="88b2d-128">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="88b2d-128">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="88b2d-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="88b2d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88b2d-130">**IRDVTaskPlugin**</span><span class="sxs-lookup"><span data-stu-id="88b2d-130">**IRDVTaskPlugin**</span></span>](irdvtaskplugin.md)
</dt> </dl>

 

 





