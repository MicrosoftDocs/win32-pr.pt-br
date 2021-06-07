---
title: Método TaskService. GetFolder
description: Para scripts, obtém uma pasta de tarefas registradas.
ms.assetid: 57e5b411-1fb6-4ee1-9802-ed2adbb4fdf8
keywords:
- Método GetFolder Agendador de Tarefas
- Método GetFolder Agendador de Tarefas, objeto TaskService
- Objeto TaskService Agendador de Tarefas, método GetFolder
topic_type:
- apiref
api_name:
- TaskService.GetFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e58f2d930a0577b6f1be620891b7ba631f18d77
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387095"
---
# <a name="taskservicegetfolder-method"></a><span data-ttu-id="9703f-106">Método TaskService. GetFolder</span><span class="sxs-lookup"><span data-stu-id="9703f-106">TaskService.GetFolder method</span></span>

<span data-ttu-id="9703f-107">Para scripts, obtém uma pasta de tarefas registradas.</span><span class="sxs-lookup"><span data-stu-id="9703f-107">For scripting, gets a folder of registered tasks.</span></span>

## <a name="syntax"></a><span data-ttu-id="9703f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9703f-108">Syntax</span></span>


```VB
TaskService.GetFolder( _
  ByVal path _
)
```



## <a name="parameters"></a><span data-ttu-id="9703f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9703f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9703f-110">*caminho* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="9703f-110">*path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9703f-111">O caminho para a pasta a ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="9703f-111">The path to the folder to be retrieved.</span></span> <span data-ttu-id="9703f-112">Não use uma barra invertida após o nome da última pasta no caminho.</span><span class="sxs-lookup"><span data-stu-id="9703f-112">Do not use a backslash following the last folder name in the path.</span></span> <span data-ttu-id="9703f-113">A pasta de tarefas raiz é especificada com uma barra invertida ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="9703f-113">The root task folder is specified with a backslash (\\).</span></span> <span data-ttu-id="9703f-114">Um exemplo de um caminho de pasta de tarefas, sob a pasta da tarefa raiz, é \\ MyTaskFolder.</span><span class="sxs-lookup"><span data-stu-id="9703f-114">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="9703f-115">O caractere '. ' não pode ser usado para especificar a pasta de tarefas atual e o '.. '</span><span class="sxs-lookup"><span data-stu-id="9703f-115">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="9703f-116">os caracteres não podem ser usados para especificar a pasta pai da tarefa no caminho.</span><span class="sxs-lookup"><span data-stu-id="9703f-116">characters cannot be used to specify the parent task folder in the path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9703f-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9703f-117">Return value</span></span>

<span data-ttu-id="9703f-118">Um objeto [**TaskFolder**](taskfolder.md) para a pasta solicitada.</span><span class="sxs-lookup"><span data-stu-id="9703f-118">A [**TaskFolder**](taskfolder.md) object for the requested folder.</span></span>

## <a name="requirements"></a><span data-ttu-id="9703f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9703f-119">Requirements</span></span>



| <span data-ttu-id="9703f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9703f-120">Requirement</span></span> | <span data-ttu-id="9703f-121">Valor</span><span class="sxs-lookup"><span data-stu-id="9703f-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9703f-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9703f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9703f-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9703f-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="9703f-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9703f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9703f-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9703f-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9703f-126">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="9703f-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="9703f-127"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9703f-127"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9703f-128">DLL</span><span class="sxs-lookup"><span data-stu-id="9703f-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9703f-129"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9703f-129"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9703f-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="9703f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9703f-131">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="9703f-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





