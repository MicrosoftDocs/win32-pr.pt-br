---
title: Propriedade TaskService. HighestVersion
description: Para scripts, indica a versão mais recente do Agendador de Tarefas a que um computador dá suporte.
ms.assetid: b4e55e46-6f33-4224-811b-06bf218dd1ac
keywords:
- Agendador de Tarefas da propriedade HighestVersion
- Propriedade HighestVersion Agendador de Tarefas, objeto TaskService
- Objeto TaskService Agendador de Tarefas, Propriedade HighestVersion
topic_type:
- apiref
api_name:
- TaskService.HighestVersion
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b4e381326ab901fcaf8657975ce3f8401facd44
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645208"
---
# <a name="taskservicehighestversion-property"></a><span data-ttu-id="c7c55-106">Propriedade TaskService. HighestVersion</span><span class="sxs-lookup"><span data-stu-id="c7c55-106">TaskService.HighestVersion property</span></span>

<span data-ttu-id="c7c55-107">Para scripts, indica a versão mais recente do Agendador de Tarefas a que um computador dá suporte.</span><span class="sxs-lookup"><span data-stu-id="c7c55-107">For scripting, indicates the highest version of Task Scheduler that a computer supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7c55-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7c55-108">Syntax</span></span>


```VB
TaskService.HighestVersion As Integer
```



## <a name="property-value"></a><span data-ttu-id="c7c55-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="c7c55-109">Property value</span></span>

<span data-ttu-id="c7c55-110">A versão mais recente do Agendador de Tarefas a que um computador dá suporte.</span><span class="sxs-lookup"><span data-stu-id="c7c55-110">The highest version of Task Scheduler that a computer supports.</span></span> <span data-ttu-id="c7c55-111">A versão mais alta é um valor que é dividido em MajorVersion/MinorVersion no limite de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="c7c55-111">The highest version is a value that is split into MajorVersion/MinorVersion on the 16-bit boundary.</span></span> <span data-ttu-id="c7c55-112">O serviço de Agendador de Tarefas retorna 1 para a versão principal e 2 para a versão secundária.</span><span class="sxs-lookup"><span data-stu-id="c7c55-112">The Task Scheduler service returns 1 for the major version and 2 for the minor version.</span></span> <span data-ttu-id="c7c55-113">Use a função [CLng](/previous-versions//ck4c5842(v=vs.85)) para obter o valor inteiro da propriedade.</span><span class="sxs-lookup"><span data-stu-id="c7c55-113">Use the [CLng](/previous-versions//ck4c5842(v=vs.85)) function to get the integer value of the property.</span></span>

## <a name="examples"></a><span data-ttu-id="c7c55-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c7c55-114">Examples</span></span>

<span data-ttu-id="c7c55-115">O código a seguir mostra como usar a função [CLng](/previous-versions//ck4c5842(v=vs.85)) para obter o valor da propriedade **HighestVersion** .</span><span class="sxs-lookup"><span data-stu-id="c7c55-115">The following code shows how to use the [CLng](/previous-versions//ck4c5842(v=vs.85)) function to get the value of the **HighestVersion** property.</span></span>


```VB
wscript.echo service.HighestVersion
Test = clng( service.HighestVersion )
If Test <> 65538  Then
    wscript.echo "Fail"

Else
    wscript.echo "Pass"
End If
```



## <a name="requirements"></a><span data-ttu-id="c7c55-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7c55-116">Requirements</span></span>



| <span data-ttu-id="c7c55-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7c55-117">Requirement</span></span> | <span data-ttu-id="c7c55-118">Valor</span><span class="sxs-lookup"><span data-stu-id="c7c55-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7c55-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7c55-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c7c55-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c7c55-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c7c55-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7c55-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c7c55-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c7c55-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c7c55-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="c7c55-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="c7c55-124"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c7c55-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c7c55-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c7c55-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7c55-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7c55-126"><dt>Taskschd.dll</dt></span></span> </dl> |



 

