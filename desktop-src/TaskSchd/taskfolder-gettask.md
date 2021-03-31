---
title: Propriedade TaskFolder. getTask
description: Para scripts, obtém uma tarefa em um local especificado em uma pasta.
ms.assetid: c0ad4402-dd63-499f-964c-0eada5665d1b
keywords:
- Agendador de Tarefas de propriedade getTask
- Propriedade getTask Agendador de Tarefas, objeto TaskFolder
- Objeto TaskFolder Agendador de Tarefas, Propriedade getTask
topic_type:
- apiref
api_name:
- TaskFolder.GetTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e813538cfcb995949cbe1fb8ec6a3b0d7772061c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644424"
---
# <a name="taskfoldergettask-property"></a><span data-ttu-id="1912c-106">Propriedade TaskFolder. getTask</span><span class="sxs-lookup"><span data-stu-id="1912c-106">TaskFolder.GetTask property</span></span>

<span data-ttu-id="1912c-107">Para scripts, obtém uma tarefa em um local especificado em uma pasta.</span><span class="sxs-lookup"><span data-stu-id="1912c-107">For scripting, gets a task at a specified location in a folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="1912c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1912c-108">Syntax</span></span>


```VB
TaskFolder.GetTask( _
  ByVal path _
)
```



## <a name="property-value"></a><span data-ttu-id="1912c-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="1912c-109">Property value</span></span>

<span data-ttu-id="1912c-110">O caminho (local) para a tarefa em uma pasta.</span><span class="sxs-lookup"><span data-stu-id="1912c-110">The path (location) to the task in a folder.</span></span> <span data-ttu-id="1912c-111">A pasta de tarefas raiz é especificada com uma barra invertida ( \) .</span><span class="sxs-lookup"><span data-stu-id="1912c-111">The root task folder is specified with a backslash (\).</span></span> <span data-ttu-id="1912c-112">Um exemplo de um caminho de pasta de tarefas, sob a pasta da tarefa raiz, é \\ MyTaskFolder.</span><span class="sxs-lookup"><span data-stu-id="1912c-112">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="1912c-113">O caractere '. ' não pode ser usado para especificar a pasta de tarefas atual e o '.. '</span><span class="sxs-lookup"><span data-stu-id="1912c-113">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="1912c-114">os caracteres não podem ser usados para especificar a pasta pai da tarefa no caminho.</span><span class="sxs-lookup"><span data-stu-id="1912c-114">characters cannot be used to specify the parent task folder in the path.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1912c-115">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="1912c-115">Error codes</span></span>

<span data-ttu-id="1912c-116">A tarefa no local especificado.</span><span class="sxs-lookup"><span data-stu-id="1912c-116">The task at the specified location.</span></span> <span data-ttu-id="1912c-117">A tarefa é um objeto [**RegisteredTask**](registeredtask.md) .</span><span class="sxs-lookup"><span data-stu-id="1912c-117">The task is a [**RegisteredTask**](registeredtask.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="1912c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1912c-118">Requirements</span></span>



| <span data-ttu-id="1912c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1912c-119">Requirement</span></span> | <span data-ttu-id="1912c-120">Valor</span><span class="sxs-lookup"><span data-stu-id="1912c-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1912c-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1912c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1912c-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1912c-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="1912c-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1912c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1912c-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1912c-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1912c-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="1912c-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="1912c-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1912c-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1912c-127">DLL</span><span class="sxs-lookup"><span data-stu-id="1912c-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1912c-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1912c-128"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





