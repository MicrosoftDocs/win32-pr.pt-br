---
title: Propriedade execaction. Path
description: Para scripts, Obtém ou define o caminho para um arquivo executável.
ms.assetid: 00fea05f-4f57-47ac-9812-8cd352fe02a8
keywords:
- Agendador de Tarefas de propriedade de caminho
- Propriedade Path Agendador de Tarefas, objeto Execaction
- Agendador de Tarefas de objeto execaction, propriedade Path
topic_type:
- apiref
api_name:
- ExecAction.Path
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b20e1dcd8cd9700f961eb944c7be3168582b8c55
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644489"
---
# <a name="execactionpath-property"></a><span data-ttu-id="c76e8-106">Propriedade execaction. Path</span><span class="sxs-lookup"><span data-stu-id="c76e8-106">ExecAction.Path property</span></span>

<span data-ttu-id="c76e8-107">Para scripts, Obtém ou define o caminho para um arquivo executável.</span><span class="sxs-lookup"><span data-stu-id="c76e8-107">For scripting, gets or sets the path to an executable file.</span></span>

## <a name="syntax"></a><span data-ttu-id="c76e8-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c76e8-108">Syntax</span></span>


```VB
ExecAction.Path As String
```



## <a name="property-value"></a><span data-ttu-id="c76e8-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="c76e8-109">Property value</span></span>

<span data-ttu-id="c76e8-110">O caminho para o arquivo executável a ser executado pela ação.</span><span class="sxs-lookup"><span data-stu-id="c76e8-110">The path to the executable file to be run by the action.</span></span>

## <a name="remarks"></a><span data-ttu-id="c76e8-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="c76e8-111">Remarks</span></span>

<span data-ttu-id="c76e8-112">Essa ação executa uma operação de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="c76e8-112">This action performs a command-line operation.</span></span> <span data-ttu-id="c76e8-113">Por exemplo, a ação pode executar um script ou iniciar um executável.</span><span class="sxs-lookup"><span data-stu-id="c76e8-113">For example, the action could run a script or launch an executable.</span></span>

<span data-ttu-id="c76e8-114">Ao ler ou gravar XML, o caminho da operação de linha de comando é especificado no elemento [**Command**](taskschedulerschema-command-exectype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="c76e8-114">When reading or writing XML, the command-line operation path is specified in the [**Command**](taskschedulerschema-command-exectype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="c76e8-115">O caminho é verificado para certificar-se de que ele é válido quando a tarefa é registrada, não quando essa propriedade é definida.</span><span class="sxs-lookup"><span data-stu-id="c76e8-115">The path is checked to make sure it is valid when the task is registered, not when this property is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="c76e8-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c76e8-116">Requirements</span></span>



| <span data-ttu-id="c76e8-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c76e8-117">Requirement</span></span> | <span data-ttu-id="c76e8-118">Valor</span><span class="sxs-lookup"><span data-stu-id="c76e8-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c76e8-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c76e8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c76e8-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c76e8-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c76e8-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c76e8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c76e8-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c76e8-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c76e8-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="c76e8-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="c76e8-124"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c76e8-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c76e8-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c76e8-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c76e8-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c76e8-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c76e8-127">Consulte também</span><span class="sxs-lookup"><span data-stu-id="c76e8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c76e8-128">**Execaction**</span><span class="sxs-lookup"><span data-stu-id="c76e8-128">**ExecAction**</span></span>](execaction.md)
</dt> <dt>

[<span data-ttu-id="c76e8-129">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="c76e8-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





