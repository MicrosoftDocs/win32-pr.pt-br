---
title: Propriedade emailaction. Subject
description: Para scripts, Obtém ou define o assunto da mensagem de email.
ms.assetid: ea398af1-9ae6-4bcf-9618-bb840b15127e
keywords:
- Agendador de Tarefas da propriedade Subject
- Propriedade Subject Agendador de Tarefas, objeto Emailaction
- Agendador de Tarefas do objeto emailaction, propriedade Subject
topic_type:
- apiref
api_name:
- EmailAction.Subject
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6236ded39993c4cb2499e64ba2e31959df91449e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766205"
---
# <a name="emailactionsubject-property"></a><span data-ttu-id="43546-106">Propriedade emailaction. Subject</span><span class="sxs-lookup"><span data-stu-id="43546-106">EmailAction.Subject property</span></span>

<span data-ttu-id="43546-107">\[Não há mais suporte para este objeto.</span><span class="sxs-lookup"><span data-stu-id="43546-107">\[This object is no longer supported.</span></span> <span data-ttu-id="43546-108">Use IExecAction com o cmdlet [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage?view=powershell-7&preserve-view=true) do PowerShell como uma solução alternativa.\]</span><span class="sxs-lookup"><span data-stu-id="43546-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage?view=powershell-7&preserve-view=true) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="43546-109">Para scripts, Obtém ou define o assunto da mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="43546-109">For scripting, gets or sets the subject of the email message.</span></span>

<span data-ttu-id="43546-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="43546-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="43546-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="43546-111">Syntax</span></span>


```VB
EmailAction.Subject As String
```



## <a name="property-value"></a><span data-ttu-id="43546-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="43546-112">Property value</span></span>

<span data-ttu-id="43546-113">O assunto da mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="43546-113">The subject of the email message.</span></span>

## <a name="remarks"></a><span data-ttu-id="43546-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="43546-114">Remarks</span></span>

<span data-ttu-id="43546-115">Ao definir esse valor de propriedade, o valor pode ser um texto que é recuperado de um arquivo Resource. dll.</span><span class="sxs-lookup"><span data-stu-id="43546-115">When setting this property value, the value can be text that is retrieved from a resource .dll file.</span></span> <span data-ttu-id="43546-116">Uma cadeia de caracteres especializada é usada para fazer referência ao texto do arquivo de recurso.</span><span class="sxs-lookup"><span data-stu-id="43546-116">A specialized string is used to reference the text from the resource file.</span></span> <span data-ttu-id="43546-117">O formato da cadeia de caracteres é $ (@ \[ dll \] , \[ ResourceId \] ), em que \[ dll \] é o caminho para o arquivo. dll que contém o recurso e \[ ResourceId \] é o identificador do texto do recurso.</span><span class="sxs-lookup"><span data-stu-id="43546-117">The format of the string is $(@ \[Dll\], \[ResourceID\]) where \[Dll\] is the path to the .dll file that contains the resource and \[ResourceID\] is the identifier for the resource text.</span></span> <span data-ttu-id="43546-118">Por exemplo, a configuração desse valor de propriedade como $ (@% SystemRoot% \\ System32 \\ResourceName.dll,-101) definirá a propriedade como o valor do texto do recurso com um identificador igual a-101 no arquivo% SystemRoot% \\ System32 \\ResourceName.dll.</span><span class="sxs-lookup"><span data-stu-id="43546-118">For example, the setting this property value to $(@ %SystemRoot%\\System32\\ResourceName.dll, -101) will set the property to the value of the resource text with an identifier equal to -101 in the %SystemRoot%\\System32\\ResourceName.dll file.</span></span>

## <a name="requirements"></a><span data-ttu-id="43546-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43546-119">Requirements</span></span>



| <span data-ttu-id="43546-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="43546-120">Requirement</span></span> | <span data-ttu-id="43546-121">Valor</span><span class="sxs-lookup"><span data-stu-id="43546-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="43546-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43546-122">Minimum supported client</span></span><br/> | <span data-ttu-id="43546-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="43546-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="43546-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43546-124">Minimum supported server</span></span><br/> | <span data-ttu-id="43546-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="43546-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="43546-126">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="43546-126">End of client support</span></span><br/>    | <span data-ttu-id="43546-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="43546-127">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="43546-128">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="43546-128">End of server support</span></span><br/>    | <span data-ttu-id="43546-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="43546-129">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="43546-130">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="43546-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="43546-131"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="43546-131"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="43546-132">DLL</span><span class="sxs-lookup"><span data-stu-id="43546-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43546-133"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43546-133"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43546-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="43546-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43546-135">**Emailaction**</span><span class="sxs-lookup"><span data-stu-id="43546-135">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="43546-136">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="43546-136">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

