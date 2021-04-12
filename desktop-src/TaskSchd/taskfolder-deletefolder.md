---
title: Método TaskFolder. DeleteFolder
description: Para scripts, exclui uma subpasta da pasta pai.
ms.assetid: 0d6a9a60-7909-4945-8186-3495e6fe9bc4
keywords:
- Agendador de Tarefas do método DeleteFolder
- Método DeleteFolder Agendador de Tarefas, objeto TaskFolder
- Objeto TaskFolder Agendador de Tarefas, método DeleteFolder
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
ms.openlocfilehash: 6ea9b8aaa7da7710cedc49e10d6be2a203f62b34
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455401"
---
# <a name="taskfolderdeletefolder-method"></a><span data-ttu-id="23308-106">Método TaskFolder. DeleteFolder</span><span class="sxs-lookup"><span data-stu-id="23308-106">TaskFolder.DeleteFolder method</span></span>

<span data-ttu-id="23308-107">Para scripts, exclui uma subpasta da pasta pai.</span><span class="sxs-lookup"><span data-stu-id="23308-107">For scripting, deletes a subfolder from the parent folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="23308-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="23308-108">Syntax</span></span>


```VB
TaskFolder.DeleteFolder( _
  ByVal folderName, _
  ByVal flags _
)
```



## <a name="parameters"></a><span data-ttu-id="23308-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="23308-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23308-110">*nome_da_pasta* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="23308-110">*folderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23308-111">O nome da subpasta a ser removida.</span><span class="sxs-lookup"><span data-stu-id="23308-111">The name of the subfolder to be removed.</span></span> <span data-ttu-id="23308-112">A pasta de tarefas raiz é especificada com uma barra invertida ( \) .</span><span class="sxs-lookup"><span data-stu-id="23308-112">The root task folder is specified with a backslash (\).</span></span> <span data-ttu-id="23308-113">Esse parâmetro pode ser um caminho relativo para a pasta que você deseja excluir.</span><span class="sxs-lookup"><span data-stu-id="23308-113">This parameter can be a relative path to the folder you want to delete.</span></span> <span data-ttu-id="23308-114">Um exemplo de um caminho de pasta de tarefas, sob a pasta da tarefa raiz, é \\ MyTaskFolder.</span><span class="sxs-lookup"><span data-stu-id="23308-114">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="23308-115">O caractere '. ' não pode ser usado para especificar a pasta de tarefas atual e o '.. '</span><span class="sxs-lookup"><span data-stu-id="23308-115">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="23308-116">os caracteres não podem ser usados para especificar a pasta pai da tarefa no caminho.</span><span class="sxs-lookup"><span data-stu-id="23308-116">characters cannot be used to specify the parent task folder in the path.</span></span>

</dd> <dt>

<span data-ttu-id="23308-117">*sinalizadores* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="23308-117">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23308-118">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="23308-118">Not supported.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23308-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="23308-119">Return value</span></span>

<span data-ttu-id="23308-120">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="23308-120">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="23308-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23308-121">Requirements</span></span>



| <span data-ttu-id="23308-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="23308-122">Requirement</span></span> | <span data-ttu-id="23308-123">Valor</span><span class="sxs-lookup"><span data-stu-id="23308-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="23308-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="23308-124">Minimum supported client</span></span><br/> | <span data-ttu-id="23308-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="23308-125">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="23308-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="23308-126">Minimum supported server</span></span><br/> | <span data-ttu-id="23308-127">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="23308-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="23308-128">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="23308-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="23308-129"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="23308-129"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="23308-130">DLL</span><span class="sxs-lookup"><span data-stu-id="23308-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23308-131"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23308-131"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23308-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="23308-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23308-133">**TaskFolder**</span><span class="sxs-lookup"><span data-stu-id="23308-133">**TaskFolder**</span></span>](taskfolder.md)
</dt> <dt>

[<span data-ttu-id="23308-134">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="23308-134">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





