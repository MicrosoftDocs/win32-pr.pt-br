---
title: Método TaskFolder. DeleteTask
description: Para scripts, exclui uma tarefa da pasta.
ms.assetid: c030b2bf-fbde-4b8b-b38b-763938855d12
keywords:
- Agendador de Tarefas do método DeleteTask
- Método DeleteTask Agendador de Tarefas, objeto TaskFolder
- Objeto TaskFolder Agendador de Tarefas, método DeleteTask
topic_type:
- apiref
api_name:
- TaskFolder.DeleteTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aad4cf0a881a62cf5e9c1600653e5df58f3000f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644818"
---
# <a name="taskfolderdeletetask-method"></a><span data-ttu-id="d655b-106">Método TaskFolder. DeleteTask</span><span class="sxs-lookup"><span data-stu-id="d655b-106">TaskFolder.DeleteTask method</span></span>

<span data-ttu-id="d655b-107">Para scripts, exclui uma tarefa da pasta.</span><span class="sxs-lookup"><span data-stu-id="d655b-107">For scripting, deletes a task from the folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="d655b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d655b-108">Syntax</span></span>


```VB
TaskFolder.DeleteTask( _
  ByVal Name, _
  ByVal flags _
)
```



## <a name="parameters"></a><span data-ttu-id="d655b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d655b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d655b-110">*Nome* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="d655b-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d655b-111">O nome da tarefa que é especificada quando a tarefa foi registrada.</span><span class="sxs-lookup"><span data-stu-id="d655b-111">The name of the task that is specified when the task was registered.</span></span> <span data-ttu-id="d655b-112">O caractere '. ' não pode ser usado para especificar a pasta de tarefas atual e o '.. '</span><span class="sxs-lookup"><span data-stu-id="d655b-112">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="d655b-113">os caracteres não podem ser usados para especificar a pasta pai da tarefa no caminho.</span><span class="sxs-lookup"><span data-stu-id="d655b-113">characters cannot be used to specify the parent task folder in the path.</span></span>

</dd> <dt>

<span data-ttu-id="d655b-114">*sinalizadores* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="d655b-114">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d655b-115">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="d655b-115">Not supported.</span></span> <span data-ttu-id="d655b-116">O valor é 0</span><span class="sxs-lookup"><span data-stu-id="d655b-116">Value is 0</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d655b-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d655b-117">Return value</span></span>

<span data-ttu-id="d655b-118">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="d655b-118">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d655b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d655b-119">Requirements</span></span>



| <span data-ttu-id="d655b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d655b-120">Requirement</span></span> | <span data-ttu-id="d655b-121">Valor</span><span class="sxs-lookup"><span data-stu-id="d655b-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d655b-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d655b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d655b-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d655b-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d655b-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d655b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d655b-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d655b-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d655b-126">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d655b-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="d655b-127"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d655b-127"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d655b-128">DLL</span><span class="sxs-lookup"><span data-stu-id="d655b-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d655b-129"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d655b-129"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d655b-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="d655b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d655b-131">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="d655b-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





