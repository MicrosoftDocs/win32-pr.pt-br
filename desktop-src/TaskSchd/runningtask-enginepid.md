---
title: Propriedade RunningTask. EnginePID
description: Para scripts, obtém a ID do processo para o mecanismo (processo) que está executando a tarefa.
ms.assetid: cb8a0f2f-ebe3-4f52-8fbd-b0cebb539728
keywords:
- Agendador de Tarefas da propriedade EnginePID
- Propriedade EnginePID Agendador de Tarefas, objeto RunningTask
- Objeto RunningTask Agendador de Tarefas, Propriedade EnginePID
topic_type:
- apiref
api_name:
- RunningTask.EnginePID
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bd725c44fc85e82d3693d9467956d3040aad2bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105759038"
---
# <a name="runningtaskenginepid-property"></a><span data-ttu-id="e6cc0-106">Propriedade RunningTask. EnginePID</span><span class="sxs-lookup"><span data-stu-id="e6cc0-106">RunningTask.EnginePID property</span></span>

<span data-ttu-id="e6cc0-107">Para scripts, obtém a ID do processo para o mecanismo (processo) que está executando a tarefa.</span><span class="sxs-lookup"><span data-stu-id="e6cc0-107">For scripting, gets the process ID for the engine (process) which is running the task.</span></span>

<span data-ttu-id="e6cc0-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="e6cc0-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6cc0-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e6cc0-109">Syntax</span></span>


```VB
RunningTask.EnginePID As Integer
```



## <a name="property-value"></a><span data-ttu-id="e6cc0-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="e6cc0-110">Property value</span></span>

<span data-ttu-id="e6cc0-111">A ID do processo para o mecanismo que está executando a tarefa.</span><span class="sxs-lookup"><span data-stu-id="e6cc0-111">The process ID for the engine which is running the task.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6cc0-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="e6cc0-112">Remarks</span></span>

<span data-ttu-id="e6cc0-113">A ID de processo retornada por essa propriedade não pode ser acrescentada diretamente a uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="e6cc0-113">The process ID returned by this property cannot be appended directly to a string.</span></span> <span data-ttu-id="e6cc0-114">O valor retornado precisa ser convertido em um valor inteiro primeiro chamando a função [CInt](/previous-versions//fctcwhw9(v=vs.85)) no valor retornado.</span><span class="sxs-lookup"><span data-stu-id="e6cc0-114">The returned value needs to be converted to an integer value first by calling the [CInt](/previous-versions//fctcwhw9(v=vs.85)) function on the returned value.</span></span>


```VB
ProcessId = cint(RunningTask.EnginePID)
wscript.echo "Process Id of Engine is " & "ProcessId
```



## <a name="requirements"></a><span data-ttu-id="e6cc0-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6cc0-115">Requirements</span></span>



| <span data-ttu-id="e6cc0-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6cc0-116">Requirement</span></span> | <span data-ttu-id="e6cc0-117">Valor</span><span class="sxs-lookup"><span data-stu-id="e6cc0-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6cc0-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e6cc0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e6cc0-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e6cc0-119">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e6cc0-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e6cc0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e6cc0-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e6cc0-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e6cc0-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e6cc0-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="e6cc0-123"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e6cc0-123"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e6cc0-124">DLL</span><span class="sxs-lookup"><span data-stu-id="e6cc0-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6cc0-125"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6cc0-125"><dt>Taskschd.dll</dt></span></span> </dl> |



 

