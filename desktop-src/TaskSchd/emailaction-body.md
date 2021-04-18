---
title: Propriedade emailaction. Body
description: Para scripts, Obtém ou define o corpo do email que contém a mensagem de email.
ms.assetid: 0015c2b9-9278-407b-b3cf-492f2d95bcb6
keywords:
- Agendador de Tarefas de Propriedade do corpo
- Propriedade do corpo Agendador de Tarefas, objeto Emailaction
- Objeto emailaction Agendador de Tarefas, Propriedade Body
topic_type:
- apiref
api_name:
- EmailAction.Body
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84be176fcf63c7a5191588dc0a68ccaf06c69f94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105766962"
---
# <a name="emailactionbody-property"></a><span data-ttu-id="d01a6-106">Propriedade emailaction. Body</span><span class="sxs-lookup"><span data-stu-id="d01a6-106">EmailAction.Body property</span></span>

<span data-ttu-id="d01a6-107">\[Não há mais suporte para este objeto.</span><span class="sxs-lookup"><span data-stu-id="d01a6-107">\[This object is no longer supported.</span></span> <span data-ttu-id="d01a6-108">Use IExecAction com o cmdlet [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) do PowerShell como uma solução alternativa.\]</span><span class="sxs-lookup"><span data-stu-id="d01a6-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="d01a6-109">Para scripts, Obtém ou define o corpo do email que contém a mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="d01a6-109">For scripting, gets or sets the body of the email that contains the email message.</span></span>

<span data-ttu-id="d01a6-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="d01a6-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d01a6-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="d01a6-111">Syntax</span></span>


```VB
EmailAction.Body As String
```



## <a name="property-value"></a><span data-ttu-id="d01a6-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="d01a6-112">Property value</span></span>

<span data-ttu-id="d01a6-113">O corpo do email que contém a mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="d01a6-113">The body of the email that contains the email message.</span></span>

## <a name="remarks"></a><span data-ttu-id="d01a6-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d01a6-114">Remarks</span></span>

<span data-ttu-id="d01a6-115">Ao definir esse valor de propriedade, o valor pode ser um texto que é recuperado de um arquivo Resource. dll.</span><span class="sxs-lookup"><span data-stu-id="d01a6-115">When setting this property value, the value can be text that is retrieved from a resource .dll file.</span></span> <span data-ttu-id="d01a6-116">Uma cadeia de caracteres especializada é usada para fazer referência ao texto do arquivo de recurso.</span><span class="sxs-lookup"><span data-stu-id="d01a6-116">A specialized string is used to reference the text from the resource file.</span></span> <span data-ttu-id="d01a6-117">O formato da cadeia de caracteres é $ (@ \[ dll \] , \[ ResourceId \] ), em que \[ dll \] é o caminho para o arquivo. dll que contém o recurso e \[ ResourceId \] é o identificador do texto do recurso.</span><span class="sxs-lookup"><span data-stu-id="d01a6-117">The format of the string is $(@ \[Dll\], \[ResourceID\]) where \[Dll\] is the path to the .dll file that contains the resource and \[ResourceID\] is the identifier for the resource text.</span></span> <span data-ttu-id="d01a6-118">Por exemplo, a configuração desse valor de propriedade como $ (@% SystemRoot% \\ System32 \\ResourceName.dll,-101) definirá a propriedade como o valor do texto do recurso com um identificador igual a-101 no arquivo% SystemRoot% \\ System32 \\ResourceName.dll.</span><span class="sxs-lookup"><span data-stu-id="d01a6-118">For example, the setting this property value to $(@ %SystemRoot%\\System32\\ResourceName.dll, -101) will set the property to the value of the resource text with an identifier equal to -101 in the %SystemRoot%\\System32\\ResourceName.dll file.</span></span>

## <a name="requirements"></a><span data-ttu-id="d01a6-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d01a6-119">Requirements</span></span>



| <span data-ttu-id="d01a6-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d01a6-120">Requirement</span></span> | <span data-ttu-id="d01a6-121">Valor</span><span class="sxs-lookup"><span data-stu-id="d01a6-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d01a6-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d01a6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d01a6-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d01a6-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d01a6-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d01a6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d01a6-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d01a6-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d01a6-126">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="d01a6-126">End of client support</span></span><br/>    | <span data-ttu-id="d01a6-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d01a6-127">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="d01a6-128">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="d01a6-128">End of server support</span></span><br/>    | <span data-ttu-id="d01a6-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d01a6-129">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="d01a6-130">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d01a6-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="d01a6-131"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d01a6-131"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d01a6-132">DLL</span><span class="sxs-lookup"><span data-stu-id="d01a6-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d01a6-133"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d01a6-133"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d01a6-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="d01a6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d01a6-135">**Emailaction**</span><span class="sxs-lookup"><span data-stu-id="d01a6-135">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="d01a6-136">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="d01a6-136">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

