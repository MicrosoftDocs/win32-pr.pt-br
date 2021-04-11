---
title: Propriedade emailaction. Server
description: Para scripts, Obtém ou define o nome do servidor SMTP que você usa para enviar email do.
ms.assetid: a6e03144-ae3e-4c4c-aad8-884be5ab324f
keywords:
- Agendador de Tarefas de Propriedade do servidor
- Propriedade do servidor Agendador de Tarefas, objeto Emailaction
- Agendador de Tarefas de objeto de emailaction, propriedade de servidor
topic_type:
- apiref
api_name:
- EmailAction.Server
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fefcc5e33727d6b4ad0bcd60e48432c68422105
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295802"
---
# <a name="emailactionserver-property"></a><span data-ttu-id="85367-106">Propriedade emailaction. Server</span><span class="sxs-lookup"><span data-stu-id="85367-106">EmailAction.Server property</span></span>

<span data-ttu-id="85367-107">\[Não há mais suporte para este objeto.</span><span class="sxs-lookup"><span data-stu-id="85367-107">\[This object is no longer supported.</span></span> <span data-ttu-id="85367-108">Use IExecAction com o cmdlet [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) do PowerShell como uma solução alternativa.\]</span><span class="sxs-lookup"><span data-stu-id="85367-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="85367-109">Para scripts, Obtém ou define o nome do servidor SMTP que você usa para enviar email do.</span><span class="sxs-lookup"><span data-stu-id="85367-109">For scripting, gets or sets the name of the SMTP server that you use to send email from.</span></span>

<span data-ttu-id="85367-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="85367-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="85367-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="85367-111">Syntax</span></span>


```VB
EmailAction.Server As String
```



## <a name="property-value"></a><span data-ttu-id="85367-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="85367-112">Property value</span></span>

<span data-ttu-id="85367-113">O nome do servidor que você usa para enviar email.</span><span class="sxs-lookup"><span data-stu-id="85367-113">The name of the server that you use to send email from.</span></span>

## <a name="remarks"></a><span data-ttu-id="85367-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="85367-114">Remarks</span></span>

<span data-ttu-id="85367-115">Verifique se o servidor SMTP que envia o email está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="85367-115">Make sure the SMTP server that sends the email is setup correctly.</span></span> <span data-ttu-id="85367-116">O email é enviado usando a autenticação NTLM para servidores SMTP do Windows, o que significa que as credenciais de segurança usadas para executar a tarefa também devem ter privilégios no servidor SMTP para enviar mensagens de email.</span><span class="sxs-lookup"><span data-stu-id="85367-116">E-mail is sent using NTLM authentication for Windows SMTP servers, which means that the security credentials used for running the task must also have privileges on the SMTP server to send email message.</span></span> <span data-ttu-id="85367-117">Se o servidor SMTP for um servidor não baseado em Windows, o email será enviado se o servidor permitir acesso anônimo.</span><span class="sxs-lookup"><span data-stu-id="85367-117">If the SMTP server is a non-Windows based server, then the email will be sent if the server allows anonymous access.</span></span> <span data-ttu-id="85367-118">Para obter informações sobre como configurar o servidor SMTP, consulte [configuração do servidor SMTP](https://www.microsoft.com/technet/prodtechnol/WindowsServer2003/Library/IIS/e4cf06f5-9a36-474b-ba78-3f287a2b88f2.mspx?mfr=true)e para obter informações sobre como gerenciar as configurações do servidor SMTP, consulte [Administração de SMTP](/previous-versions/windows/it-pro/windows-server-2003/cc758258(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="85367-118">For information about setting up the SMTP server, see [SMTP Server Setup](https://www.microsoft.com/technet/prodtechnol/WindowsServer2003/Library/IIS/e4cf06f5-9a36-474b-ba78-3f287a2b88f2.mspx?mfr=true), and for information about managing SMTP server settings, see [SMTP Administration](/previous-versions/windows/it-pro/windows-server-2003/cc758258(v=ws.10)).</span></span>

## <a name="requirements"></a><span data-ttu-id="85367-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85367-119">Requirements</span></span>



| <span data-ttu-id="85367-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="85367-120">Requirement</span></span> | <span data-ttu-id="85367-121">Valor</span><span class="sxs-lookup"><span data-stu-id="85367-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="85367-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="85367-122">Minimum supported client</span></span><br/> | <span data-ttu-id="85367-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="85367-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="85367-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="85367-124">Minimum supported server</span></span><br/> | <span data-ttu-id="85367-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="85367-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="85367-126">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="85367-126">End of client support</span></span><br/>    | <span data-ttu-id="85367-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="85367-127">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="85367-128">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="85367-128">End of server support</span></span><br/>    | <span data-ttu-id="85367-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="85367-129">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="85367-130">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="85367-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="85367-131"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="85367-131"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="85367-132">DLL</span><span class="sxs-lookup"><span data-stu-id="85367-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85367-133"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85367-133"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85367-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="85367-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85367-135">**Emailaction**</span><span class="sxs-lookup"><span data-stu-id="85367-135">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="85367-136">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="85367-136">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

