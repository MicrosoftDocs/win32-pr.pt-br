---
title: Método TaskFolder. CreateFolder
description: Para scripts, o cria uma pasta para tarefas relacionadas.
ms.assetid: 4fdc96bc-8c85-4b36-b3ea-bad7a46c3d35
keywords:
- Método CreateFolder Agendador de Tarefas
- Método CreateFolder Agendador de Tarefas, objeto TaskFolder
- Objeto TaskFolder Agendador de Tarefas, método CreateFolder
topic_type:
- apiref
api_name:
- TaskFolder.CreateFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ae66dadb0c943b1ca33be3e696ac1c8ca7d6234
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753335"
---
# <a name="taskfoldercreatefolder-method"></a><span data-ttu-id="dee35-106">Método TaskFolder. CreateFolder</span><span class="sxs-lookup"><span data-stu-id="dee35-106">TaskFolder.CreateFolder method</span></span>

<span data-ttu-id="dee35-107">Para scripts, o cria uma pasta para tarefas relacionadas.</span><span class="sxs-lookup"><span data-stu-id="dee35-107">For scripting, creates a folder for related tasks.</span></span>

## <a name="syntax"></a><span data-ttu-id="dee35-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dee35-108">Syntax</span></span>


```VB
ppFolder = .CreateFolder( _
  ByVal folderName, _
  ByVal sddl _
)
```



## <a name="parameters"></a><span data-ttu-id="dee35-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dee35-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dee35-110">*nome_da_pasta* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dee35-110">*folderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dee35-111">O nome usado para identificar a pasta.</span><span class="sxs-lookup"><span data-stu-id="dee35-111">The name that is used to identify the folder.</span></span> <span data-ttu-id="dee35-112">Se "nome_da_pasta \\ subpasta1 \\ SubFolder2" for especificado, toda a árvore de pastas será criada se as pastas não existirem.</span><span class="sxs-lookup"><span data-stu-id="dee35-112">If "FolderName\\SubFolder1\\SubFolder2" is specified, the entire folder tree will be created if the folders do not exist.</span></span> <span data-ttu-id="dee35-113">Esse parâmetro pode ser um caminho relativo para a instância de [**TaskFolder**](taskfolder.md) atual.</span><span class="sxs-lookup"><span data-stu-id="dee35-113">This parameter can be a relative path to the current [**TaskFolder**](taskfolder.md) instance.</span></span> <span data-ttu-id="dee35-114">A pasta de tarefas raiz é especificada com uma barra invertida ( \) .</span><span class="sxs-lookup"><span data-stu-id="dee35-114">The root task folder is specified with a backslash (\).</span></span> <span data-ttu-id="dee35-115">Um exemplo de um caminho de pasta de tarefas, sob a pasta da tarefa raiz, é \\ MyTaskFolder.</span><span class="sxs-lookup"><span data-stu-id="dee35-115">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="dee35-116">O caractere '. ' não pode ser usado para especificar a pasta de tarefas atual e o '.. '</span><span class="sxs-lookup"><span data-stu-id="dee35-116">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="dee35-117">os caracteres não podem ser usados para especificar a pasta pai da tarefa no caminho.</span><span class="sxs-lookup"><span data-stu-id="dee35-117">characters cannot be used to specify the parent task folder in the path.</span></span>

</dd> <dt>

<span data-ttu-id="dee35-118">*SDDL* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="dee35-118">*sddl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dee35-119">O descritor de segurança associado à pasta.</span><span class="sxs-lookup"><span data-stu-id="dee35-119">The security descriptor that is associated with the folder.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dee35-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dee35-120">Return value</span></span>

<span data-ttu-id="dee35-121">Um objeto [**TaskFolder**](taskfolder.md) que representa a nova subpasta.</span><span class="sxs-lookup"><span data-stu-id="dee35-121">A [**TaskFolder**](taskfolder.md) object that represents the new subfolder.</span></span>

## <a name="requirements"></a><span data-ttu-id="dee35-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dee35-122">Requirements</span></span>



| <span data-ttu-id="dee35-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="dee35-123">Requirement</span></span> | <span data-ttu-id="dee35-124">Valor</span><span class="sxs-lookup"><span data-stu-id="dee35-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dee35-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dee35-125">Minimum supported client</span></span><br/> | <span data-ttu-id="dee35-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dee35-126">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="dee35-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dee35-127">Minimum supported server</span></span><br/> | <span data-ttu-id="dee35-128">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dee35-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dee35-129">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="dee35-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="dee35-130"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="dee35-130"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="dee35-131">DLL</span><span class="sxs-lookup"><span data-stu-id="dee35-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dee35-132"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dee35-132"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dee35-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="dee35-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dee35-134">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="dee35-134">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





