---
title: Propriedade emailaction. HeaderFields
description: Para scripts, Obtém ou define as informações de cabeçalho no email que você deseja enviar.
ms.assetid: 492c1e7c-805a-4c58-82d3-45c82420c694
keywords:
- Agendador de Tarefas da propriedade HeaderFields
- Propriedade HeaderFields Agendador de Tarefas, objeto Emailaction
- Objeto emailaction Agendador de Tarefas, Propriedade HeaderFields
topic_type:
- apiref
api_name:
- EmailAction.HeaderFields
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96cfb963879e47e51e1096d2559fe4e72c6b2543
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824487"
---
# <a name="emailactionheaderfields-property"></a><span data-ttu-id="cd29c-106">Propriedade emailaction. HeaderFields</span><span class="sxs-lookup"><span data-stu-id="cd29c-106">EmailAction.HeaderFields property</span></span>

<span data-ttu-id="cd29c-107">\[Não há mais suporte para este objeto.</span><span class="sxs-lookup"><span data-stu-id="cd29c-107">\[This object is no longer supported.</span></span> <span data-ttu-id="cd29c-108">Use IExecAction com o cmdlet [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) do PowerShell como uma solução alternativa.\]</span><span class="sxs-lookup"><span data-stu-id="cd29c-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="cd29c-109">Para scripts, Obtém ou define as informações de cabeçalho no email que você deseja enviar.</span><span class="sxs-lookup"><span data-stu-id="cd29c-109">For scripting, gets or sets the header information in the email you want to send.</span></span>

<span data-ttu-id="cd29c-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="cd29c-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd29c-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cd29c-111">Syntax</span></span>


```VB
EmailAction.HeaderFields As TaskNamedValueCollection
```



## <a name="property-value"></a><span data-ttu-id="cd29c-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="cd29c-112">Property value</span></span>

<span data-ttu-id="cd29c-113">As informações de cabeçalho no email que você deseja enviar.</span><span class="sxs-lookup"><span data-stu-id="cd29c-113">The header information in the email you want to send.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd29c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd29c-114">Requirements</span></span>



| <span data-ttu-id="cd29c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd29c-115">Requirement</span></span> | <span data-ttu-id="cd29c-116">Valor</span><span class="sxs-lookup"><span data-stu-id="cd29c-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd29c-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cd29c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cd29c-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cd29c-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="cd29c-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cd29c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cd29c-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cd29c-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cd29c-121">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="cd29c-121">End of client support</span></span><br/>    | <span data-ttu-id="cd29c-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="cd29c-122">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="cd29c-123">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="cd29c-123">End of server support</span></span><br/>    | <span data-ttu-id="cd29c-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="cd29c-124">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="cd29c-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="cd29c-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="cd29c-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="cd29c-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="cd29c-127">DLL</span><span class="sxs-lookup"><span data-stu-id="cd29c-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd29c-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd29c-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd29c-129">Consulte também</span><span class="sxs-lookup"><span data-stu-id="cd29c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd29c-130">**Emailaction**</span><span class="sxs-lookup"><span data-stu-id="cd29c-130">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="cd29c-131">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="cd29c-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

