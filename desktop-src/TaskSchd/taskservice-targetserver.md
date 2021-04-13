---
title: Propriedade TaskService. TargetServer
description: Para scripts, obtém o nome do computador que está executando o serviço de Agendador de Tarefas ao qual o usuário está conectado.
ms.assetid: 8b0edf18-2a79-46f2-9b90-2c4726db881e
keywords:
- Agendador de Tarefas da Propriedade TargetServer
- Propriedade TargetServer Agendador de Tarefas, objeto TaskService
- Objeto TaskService Agendador de Tarefas, Propriedade TargetServer
topic_type:
- apiref
api_name:
- TaskService.TargetServer
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4347915fae57585716a64a6a4ca549ccc1c299
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499810"
---
# <a name="taskservicetargetserver-property"></a><span data-ttu-id="6ad37-106">Propriedade TaskService. TargetServer</span><span class="sxs-lookup"><span data-stu-id="6ad37-106">TaskService.TargetServer property</span></span>

<span data-ttu-id="6ad37-107">Para scripts, obtém o nome do computador que está executando o serviço de Agendador de Tarefas ao qual o usuário está conectado.</span><span class="sxs-lookup"><span data-stu-id="6ad37-107">For scripting, gets the name of the computer that is running the Task Scheduler service that the user is connected to.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ad37-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ad37-108">Syntax</span></span>


```VB
TaskService.TargetServer As String
```



## <a name="property-value"></a><span data-ttu-id="6ad37-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="6ad37-109">Property value</span></span>

<span data-ttu-id="6ad37-110">O nome do computador que está executando o serviço de Agendador de Tarefas ao qual o usuário está conectado.</span><span class="sxs-lookup"><span data-stu-id="6ad37-110">The name of the computer that is running the Task Scheduler service that the user is connected to.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ad37-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="6ad37-111">Remarks</span></span>

<span data-ttu-id="6ad37-112">Essa propriedade retorna uma cadeia de caracteres vazia quando o usuário passa um endereço IP, localhost ou '. ' como um parâmetro e retorna o nome do computador que está executando o serviço de Agendador de Tarefas quando o usuário não passa nenhum valor de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="6ad37-112">This property returns an empty string when the user passes an IP address, Localhost, or '.' as a parameter, and it returns the name of the computer that is running the Task Scheduler service when the user does not pass any parameter value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ad37-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ad37-113">Requirements</span></span>



| <span data-ttu-id="6ad37-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ad37-114">Requirement</span></span> | <span data-ttu-id="6ad37-115">Valor</span><span class="sxs-lookup"><span data-stu-id="6ad37-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ad37-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ad37-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6ad37-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6ad37-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="6ad37-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ad37-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6ad37-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6ad37-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6ad37-120">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6ad37-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="6ad37-121"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6ad37-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6ad37-122">DLL</span><span class="sxs-lookup"><span data-stu-id="6ad37-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ad37-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ad37-123"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





