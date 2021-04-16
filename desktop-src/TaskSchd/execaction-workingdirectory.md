---
title: Propriedade execaction. WorkingDirectory
description: Para scripts, Obtém ou define o diretório que contém o arquivo executável ou os arquivos que são usados pelo arquivo executável.
ms.assetid: 7b1e3c9d-ba08-4812-b50e-f97b6c12f8bd
keywords:
- Agendador de Tarefas da propriedade WorkingDirectory
- Propriedade WorkingDirectory Agendador de Tarefas, objeto Execaction
- Agendador de Tarefas de objeto execaction, Propriedade WorkingDirectory
topic_type:
- apiref
api_name:
- ExecAction.WorkingDirectory
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28d4755b6f760ed1af75c676ecb70074c3ea7c92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105758392"
---
# <a name="execactionworkingdirectory-property"></a><span data-ttu-id="bb0ef-106">Propriedade execaction. WorkingDirectory</span><span class="sxs-lookup"><span data-stu-id="bb0ef-106">ExecAction.WorkingDirectory property</span></span>

<span data-ttu-id="bb0ef-107">Para scripts, Obtém ou define o diretório que contém o arquivo executável ou os arquivos que são usados pelo arquivo executável.</span><span class="sxs-lookup"><span data-stu-id="bb0ef-107">For scripting, gets or sets the directory that contains either the executable file or the files that are used by the executable file.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb0ef-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb0ef-108">Syntax</span></span>


```VB
ExecAction.WorkingDirectory As String
```



## <a name="property-value"></a><span data-ttu-id="bb0ef-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="bb0ef-109">Property value</span></span>

<span data-ttu-id="bb0ef-110">O diretório que contém o arquivo executável ou os arquivos que são usados pelo arquivo executável.</span><span class="sxs-lookup"><span data-stu-id="bb0ef-110">The directory that contains either the executable file or the files that are used by the executable file.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb0ef-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="bb0ef-111">Remarks</span></span>

<span data-ttu-id="bb0ef-112">Ao ler ou gravar XML, o diretório de trabalho do aplicativo é especificado no elemento [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="bb0ef-112">When reading or writing XML, the working directory of the application is specified in the [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="bb0ef-113">O caminho é verificado para certificar-se de que ele é válido quando a tarefa é registrada, não quando essa propriedade é definida.</span><span class="sxs-lookup"><span data-stu-id="bb0ef-113">The path is checked to make sure it is valid when the task is registered, not when this property is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb0ef-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb0ef-114">Requirements</span></span>



| <span data-ttu-id="bb0ef-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb0ef-115">Requirement</span></span> | <span data-ttu-id="bb0ef-116">Valor</span><span class="sxs-lookup"><span data-stu-id="bb0ef-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb0ef-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bb0ef-117">Minimum supported client</span></span><br/> | <span data-ttu-id="bb0ef-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bb0ef-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="bb0ef-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bb0ef-119">Minimum supported server</span></span><br/> | <span data-ttu-id="bb0ef-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bb0ef-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bb0ef-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="bb0ef-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="bb0ef-122"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bb0ef-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bb0ef-123">DLL</span><span class="sxs-lookup"><span data-stu-id="bb0ef-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb0ef-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb0ef-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb0ef-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="bb0ef-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb0ef-126">**Execaction**</span><span class="sxs-lookup"><span data-stu-id="bb0ef-126">**ExecAction**</span></span>](execaction.md)
</dt> <dt>

[<span data-ttu-id="bb0ef-127">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="bb0ef-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





