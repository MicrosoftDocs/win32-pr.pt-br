---
title: Objeto TaskVariables
description: Objeto de script que define as variáveis de tarefa que podem ser passadas como parâmetros para manipuladores de tarefas e executáveis externos que são iniciados por tarefas.
ms.assetid: 194babe0-16bd-4a78-af45-139c9c7eacbe
keywords:
- Agendador de Tarefas de objeto TaskVariables
- Agendador de Tarefas de objeto TaskVariables, descrito
topic_type:
- apiref
api_name:
- TaskVariables
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00fe20153b0d6d66ca6c7f263a8e76d5a4d480b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455691"
---
# <a name="taskvariables-object"></a><span data-ttu-id="ef1e8-105">Objeto TaskVariables</span><span class="sxs-lookup"><span data-stu-id="ef1e8-105">TaskVariables object</span></span>

<span data-ttu-id="ef1e8-106">Objeto de script que define as variáveis de tarefa que podem ser passadas como parâmetros para manipuladores de tarefas e executáveis externos que são iniciados por tarefas.</span><span class="sxs-lookup"><span data-stu-id="ef1e8-106">Scripting object that defines task variables that can be passed as parameters to task handlers and external executables that are launched by tasks.</span></span>

## <a name="members"></a><span data-ttu-id="ef1e8-107">Membros</span><span class="sxs-lookup"><span data-stu-id="ef1e8-107">Members</span></span>

<span data-ttu-id="ef1e8-108">O objeto **TaskVariables** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ef1e8-108">The **TaskVariables** object has these types of members:</span></span>

-   [<span data-ttu-id="ef1e8-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="ef1e8-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ef1e8-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="ef1e8-110">Methods</span></span>

<span data-ttu-id="ef1e8-111">O objeto **TaskVariables** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="ef1e8-111">The **TaskVariables** object has these methods.</span></span>



| <span data-ttu-id="ef1e8-112">Método</span><span class="sxs-lookup"><span data-stu-id="ef1e8-112">Method</span></span>                                         | <span data-ttu-id="ef1e8-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="ef1e8-113">Description</span></span>                                                                                               |
|:-----------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ef1e8-114">**GetContext**</span><span class="sxs-lookup"><span data-stu-id="ef1e8-114">**GetContext**</span></span>](taskvariables-getcontext.md) | <span data-ttu-id="ef1e8-115">Usado para compartilhar o contexto entre etapas e tarefas diferentes que estão na mesma instância de trabalho.</span><span class="sxs-lookup"><span data-stu-id="ef1e8-115">Used to share the context between different steps and tasks that are in the same job instance.</span></span><br/> |
| [<span data-ttu-id="ef1e8-116">**GetInput**</span><span class="sxs-lookup"><span data-stu-id="ef1e8-116">**GetInput**</span></span>](taskvariables-getinput.md)     | <span data-ttu-id="ef1e8-117">Obtém as variáveis de entrada para uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="ef1e8-117">Gets the input variables for a task.</span></span><br/>                                                           |
| [<span data-ttu-id="ef1e8-118">**SetOutput**</span><span class="sxs-lookup"><span data-stu-id="ef1e8-118">**SetOutput**</span></span>](taskvariables-setoutput.md)   | <span data-ttu-id="ef1e8-119">Define as variáveis de saída para uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="ef1e8-119">Sets the output variables for a task.</span></span><br/>                                                          |



 

## <a name="requirements"></a><span data-ttu-id="ef1e8-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef1e8-120">Requirements</span></span>



| <span data-ttu-id="ef1e8-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef1e8-121">Requirement</span></span> | <span data-ttu-id="ef1e8-122">Valor</span><span class="sxs-lookup"><span data-stu-id="ef1e8-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef1e8-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ef1e8-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ef1e8-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ef1e8-124">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ef1e8-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ef1e8-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ef1e8-126">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ef1e8-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ef1e8-127">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ef1e8-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="ef1e8-128"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ef1e8-128"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ef1e8-129">DLL</span><span class="sxs-lookup"><span data-stu-id="ef1e8-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef1e8-130"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef1e8-130"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





