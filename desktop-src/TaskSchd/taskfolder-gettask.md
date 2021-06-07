---
title: Propriedade TaskFolder.GetTask
description: Para scripts, obtém uma tarefa em um local especificado em uma pasta.
ms.assetid: c0ad4402-dd63-499f-964c-0eada5665d1b
keywords:
- Propriedade GetTask Agendador de Tarefas
- Propriedade GetTask Agendador de Tarefas objeto , TaskFolder
- Objeto TaskFolder Agendador de Tarefas propriedade , GetTask
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
ms.openlocfilehash: b697b8fa2d0715dcf0282c5f32490bfccec79fec
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387672"
---
# <a name="taskfoldergettask-property"></a><span data-ttu-id="762b0-106">Propriedade TaskFolder.GetTask</span><span class="sxs-lookup"><span data-stu-id="762b0-106">TaskFolder.GetTask property</span></span>

<span data-ttu-id="762b0-107">Para scripts, obtém uma tarefa em um local especificado em uma pasta.</span><span class="sxs-lookup"><span data-stu-id="762b0-107">For scripting, gets a task at a specified location in a folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="762b0-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="762b0-108">Syntax</span></span>


```VB
TaskFolder.GetTask( _
  ByVal path _
)
```



## <a name="property-value"></a><span data-ttu-id="762b0-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="762b0-109">Property value</span></span>

<span data-ttu-id="762b0-110">O caminho (local) para a tarefa em uma pasta.</span><span class="sxs-lookup"><span data-stu-id="762b0-110">The path (location) to the task in a folder.</span></span> <span data-ttu-id="762b0-111">A pasta da tarefa raiz é especificada com uma barra invertida ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="762b0-111">The root task folder is specified with a backslash (\\).</span></span> <span data-ttu-id="762b0-112">Um exemplo de um caminho de pasta de tarefa, na pasta de tarefas raiz, é \\ MyTaskFolder.</span><span class="sxs-lookup"><span data-stu-id="762b0-112">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="762b0-113">O caractere '.' não pode ser usado para especificar a pasta de tarefas atual e o '..'</span><span class="sxs-lookup"><span data-stu-id="762b0-113">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="762b0-114">Não é possível usar caracteres para especificar a pasta de tarefas pai no caminho.</span><span class="sxs-lookup"><span data-stu-id="762b0-114">characters cannot be used to specify the parent task folder in the path.</span></span>

## <a name="error-codes"></a><span data-ttu-id="762b0-115">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="762b0-115">Error codes</span></span>

<span data-ttu-id="762b0-116">A tarefa no local especificado.</span><span class="sxs-lookup"><span data-stu-id="762b0-116">The task at the specified location.</span></span> <span data-ttu-id="762b0-117">A tarefa é um [**objeto RegisteredTask.**](registeredtask.md)</span><span class="sxs-lookup"><span data-stu-id="762b0-117">The task is a [**RegisteredTask**](registeredtask.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="762b0-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="762b0-118">Requirements</span></span>



| <span data-ttu-id="762b0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="762b0-119">Requirement</span></span> | <span data-ttu-id="762b0-120">Valor</span><span class="sxs-lookup"><span data-stu-id="762b0-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="762b0-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="762b0-121">Minimum supported client</span></span><br/> | <span data-ttu-id="762b0-122">Somente \[ aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="762b0-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="762b0-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="762b0-123">Minimum supported server</span></span><br/> | <span data-ttu-id="762b0-124">Somente aplicativos da área de trabalho do Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="762b0-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="762b0-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="762b0-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="762b0-126"><dt>Taskschd.tlb</dt></span><span class="sxs-lookup"><span data-stu-id="762b0-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="762b0-127">DLL</span><span class="sxs-lookup"><span data-stu-id="762b0-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="762b0-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="762b0-128"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





