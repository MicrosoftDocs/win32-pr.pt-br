---
title: Método TaskFolder.DeleteFolder
description: Para scripts, exclui uma subpasta da pasta pai.
ms.assetid: 0d6a9a60-7909-4945-8186-3495e6fe9bc4
keywords:
- Método DeleteFolder Agendador de Tarefas
- Método DeleteFolder Agendador de Tarefas , objeto TaskFolder
- Objeto TaskFolder Agendador de Tarefas , método DeleteFolder
topic_type:
- apiref
api_name:
- TaskFolder.DeleteFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31080f017329cde376b646befd4b7e12ba02926b
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387035"
---
# <a name="taskfolderdeletefolder-method"></a><span data-ttu-id="f0865-106">Método TaskFolder.DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="f0865-106">TaskFolder.DeleteFolder method</span></span>

<span data-ttu-id="f0865-107">Para scripts, exclui uma subpasta da pasta pai.</span><span class="sxs-lookup"><span data-stu-id="f0865-107">For scripting, deletes a subfolder from the parent folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0865-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f0865-108">Syntax</span></span>


```VB
TaskFolder.DeleteFolder( _
  ByVal folderName, _
  ByVal flags _
)
```



## <a name="parameters"></a><span data-ttu-id="f0865-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f0865-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0865-110">*folderName* \[ Em\]</span><span class="sxs-lookup"><span data-stu-id="f0865-110">*folderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0865-111">O nome da subpasta a ser removida.</span><span class="sxs-lookup"><span data-stu-id="f0865-111">The name of the subfolder to be removed.</span></span> <span data-ttu-id="f0865-112">A pasta da tarefa raiz é especificada com uma barra invertida ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="f0865-112">The root task folder is specified with a backslash (\\).</span></span> <span data-ttu-id="f0865-113">Esse parâmetro pode ser um caminho relativo para a pasta que você deseja excluir.</span><span class="sxs-lookup"><span data-stu-id="f0865-113">This parameter can be a relative path to the folder you want to delete.</span></span> <span data-ttu-id="f0865-114">Um exemplo de um caminho de pasta de tarefa, na pasta de tarefas raiz, é \\ MyTaskFolder.</span><span class="sxs-lookup"><span data-stu-id="f0865-114">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="f0865-115">O caractere '.' não pode ser usado para especificar a pasta de tarefas atual e o '..'</span><span class="sxs-lookup"><span data-stu-id="f0865-115">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="f0865-116">Não é possível usar caracteres para especificar a pasta de tarefas pai no caminho.</span><span class="sxs-lookup"><span data-stu-id="f0865-116">characters cannot be used to specify the parent task folder in the path.</span></span>

</dd> <dt>

<span data-ttu-id="f0865-117">*sinalizadores* \[ Em\]</span><span class="sxs-lookup"><span data-stu-id="f0865-117">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0865-118">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="f0865-118">Not supported.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0865-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f0865-119">Return value</span></span>

<span data-ttu-id="f0865-120">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f0865-120">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0865-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0865-121">Requirements</span></span>



| <span data-ttu-id="f0865-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0865-122">Requirement</span></span> | <span data-ttu-id="f0865-123">Valor</span><span class="sxs-lookup"><span data-stu-id="f0865-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0865-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f0865-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f0865-125">Somente \[ aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f0865-125">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f0865-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f0865-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f0865-127">Somente aplicativos da área de trabalho do Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f0865-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f0865-128">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f0865-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="f0865-129"><dt>Taskschd.tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f0865-129"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f0865-130">DLL</span><span class="sxs-lookup"><span data-stu-id="f0865-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0865-131"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0865-131"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0865-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="f0865-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0865-133">**TaskFolder**</span><span class="sxs-lookup"><span data-stu-id="f0865-133">**TaskFolder**</span></span>](taskfolder.md)
</dt> <dt>

[<span data-ttu-id="f0865-134">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="f0865-134">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





