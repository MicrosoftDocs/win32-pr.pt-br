---
title: Método TaskService. NewTask
description: Para scripts, retorna um objeto de definição de tarefa vazio a ser preenchido com configurações e propriedades e, em seguida, registrado usando o método TaskFolder. RegisterTaskDefinition.
ms.assetid: 696d57fc-100a-43e6-a8d9-9ec89be40367
keywords:
- Método NewTask Agendador de Tarefas
- Método NewTask Agendador de Tarefas, objeto TaskService
- Objeto TaskService Agendador de Tarefas, método NewTask
topic_type:
- apiref
api_name:
- TaskService.NewTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f5f10ce90861c76d0a751c54e8282269b7a8986
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105779284"
---
# <a name="taskservicenewtask-method"></a><span data-ttu-id="bb574-106">Método TaskService. NewTask</span><span class="sxs-lookup"><span data-stu-id="bb574-106">TaskService.NewTask method</span></span>

<span data-ttu-id="bb574-107">Para scripts, retorna um objeto de definição de tarefa vazio a ser preenchido com configurações e propriedades e, em seguida, registrado usando o método [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="bb574-107">For scripting, returns an empty task definition object to be filled in with settings and properties and then registered using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb574-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bb574-108">Syntax</span></span>


```VB
TaskService.NewTask( _
  ByVal flags _
)
```



## <a name="parameters"></a><span data-ttu-id="bb574-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bb574-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb574-110">*sinalizadores* \[ de no\]</span><span class="sxs-lookup"><span data-stu-id="bb574-110">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb574-111">Esse parâmetro é reservado para uso futuro e deve ser definido como 0.</span><span class="sxs-lookup"><span data-stu-id="bb574-111">This parameter is reserved for future use and must be set to 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb574-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bb574-112">Return value</span></span>

<span data-ttu-id="bb574-113">A definição de tarefa que especifica todas as informações necessárias para criar uma nova tarefa.</span><span class="sxs-lookup"><span data-stu-id="bb574-113">The task definition that specifies all the information required to create a new task.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb574-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb574-114">Requirements</span></span>



| <span data-ttu-id="bb574-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb574-115">Requirement</span></span> | <span data-ttu-id="bb574-116">Valor</span><span class="sxs-lookup"><span data-stu-id="bb574-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb574-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bb574-117">Minimum supported client</span></span><br/> | <span data-ttu-id="bb574-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bb574-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="bb574-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bb574-119">Minimum supported server</span></span><br/> | <span data-ttu-id="bb574-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bb574-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bb574-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="bb574-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="bb574-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bb574-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bb574-123">DLL</span><span class="sxs-lookup"><span data-stu-id="bb574-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb574-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb574-124"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





