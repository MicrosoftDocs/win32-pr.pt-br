---
title: Propriedade emailaction. Attachments
description: Para scripts, Obtém ou define uma matriz de anexos que é enviada com a mensagem de email.
ms.assetid: 59bcb8c4-8b8c-4f09-94d6-3a65f1e8c0a8
keywords:
- Agendador de Tarefas da propriedade Attachments
- Propriedade Attachments Agendador de Tarefas, objeto Emailaction
- Objeto emailaction Agendador de Tarefas, Propriedade Attachments
topic_type:
- apiref
api_name:
- EmailAction.Attachments
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae620321f9dca7a5c38decf7de661d713989c88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644750"
---
# <a name="emailactionattachments-property"></a><span data-ttu-id="a2133-106">Propriedade emailaction. Attachments</span><span class="sxs-lookup"><span data-stu-id="a2133-106">EmailAction.Attachments property</span></span>

<span data-ttu-id="a2133-107">\[Não há mais suporte para este objeto.</span><span class="sxs-lookup"><span data-stu-id="a2133-107">\[This object is no longer supported.</span></span> <span data-ttu-id="a2133-108">Use IExecAction com o cmdlet [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) do PowerShell como uma solução alternativa.\]</span><span class="sxs-lookup"><span data-stu-id="a2133-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="a2133-109">Para scripts, Obtém ou define uma matriz de anexos que é enviada com a mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="a2133-109">For scripting, gets or sets an array of attachments that is sent with the email message.</span></span>

<span data-ttu-id="a2133-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="a2133-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2133-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a2133-111">Syntax</span></span>


```VB
EmailAction.Attachments As String
```



## <a name="property-value"></a><span data-ttu-id="a2133-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="a2133-112">Property value</span></span>

<span data-ttu-id="a2133-113">Uma matriz de anexos que é enviada com a mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="a2133-113">An array of attachments that is sent with the email message.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2133-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a2133-114">Remarks</span></span>

<span data-ttu-id="a2133-115">Um máximo de oito anexos pode estar na matriz de anexos.</span><span class="sxs-lookup"><span data-stu-id="a2133-115">A maximum of eight attachments can be in the array of attachments.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2133-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2133-116">Requirements</span></span>



| <span data-ttu-id="a2133-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2133-117">Requirement</span></span> | <span data-ttu-id="a2133-118">Valor</span><span class="sxs-lookup"><span data-stu-id="a2133-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a2133-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a2133-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a2133-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a2133-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="a2133-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a2133-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a2133-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a2133-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a2133-123">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="a2133-123">End of client support</span></span><br/>    | <span data-ttu-id="a2133-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a2133-124">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="a2133-125">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="a2133-125">End of server support</span></span><br/>    | <span data-ttu-id="a2133-126">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a2133-126">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="a2133-127">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="a2133-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="a2133-128"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a2133-128"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a2133-129">DLL</span><span class="sxs-lookup"><span data-stu-id="a2133-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2133-130"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2133-130"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2133-131">Consulte também</span><span class="sxs-lookup"><span data-stu-id="a2133-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2133-132">**Emailaction**</span><span class="sxs-lookup"><span data-stu-id="a2133-132">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="a2133-133">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="a2133-133">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

