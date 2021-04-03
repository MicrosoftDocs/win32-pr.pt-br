---
title: Propriedade EmailAction.Cc
description: Para scripts, Obtém ou define o endereço de email ou endereços que você deseja CC na mensagem de email.
ms.assetid: 4ad67064-3e6b-4666-a3ce-66e4dcc3f873
keywords:
- Agendador de Tarefas de propriedade CC
- Propriedade CC Agendador de Tarefas, objeto Emailaction
- Objeto emailaction Agendador de Tarefas, Propriedade CC
topic_type:
- apiref
api_name:
- EmailAction.Cc
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00f05d7fbd1883aa38ba972eba1eb14767349357
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644749"
---
# <a name="emailactioncc-property"></a><span data-ttu-id="36cf2-106">Propriedade EmailAction.Cc</span><span class="sxs-lookup"><span data-stu-id="36cf2-106">EmailAction.Cc property</span></span>

<span data-ttu-id="36cf2-107">\[Não há mais suporte para este objeto.</span><span class="sxs-lookup"><span data-stu-id="36cf2-107">\[This object is no longer supported.</span></span> <span data-ttu-id="36cf2-108">Use IExecAction com o cmdlet [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) do PowerShell como uma solução alternativa.\]</span><span class="sxs-lookup"><span data-stu-id="36cf2-108">Please use IExecAction with the powershell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) cmdlet as a workaround.\]</span></span>

<span data-ttu-id="36cf2-109">Para scripts, Obtém ou define o endereço de email ou endereços que você deseja CC na mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="36cf2-109">For scripting, gets or sets the email address or addresses that you want to Cc in the email message.</span></span>

<span data-ttu-id="36cf2-110">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="36cf2-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="36cf2-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="36cf2-111">Syntax</span></span>


```VB
EmailAction.Cc As String
```



## <a name="property-value"></a><span data-ttu-id="36cf2-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="36cf2-112">Property value</span></span>

<span data-ttu-id="36cf2-113">O endereço de email ou endereços que você deseja CC na mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="36cf2-113">The email address or addresses that you want to Cc in the email message.</span></span>

## <a name="requirements"></a><span data-ttu-id="36cf2-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36cf2-114">Requirements</span></span>



| <span data-ttu-id="36cf2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="36cf2-115">Requirement</span></span> | <span data-ttu-id="36cf2-116">Valor</span><span class="sxs-lookup"><span data-stu-id="36cf2-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="36cf2-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="36cf2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="36cf2-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="36cf2-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="36cf2-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="36cf2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="36cf2-120">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="36cf2-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="36cf2-121">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="36cf2-121">End of client support</span></span><br/>    | <span data-ttu-id="36cf2-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="36cf2-122">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="36cf2-123">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="36cf2-123">End of server support</span></span><br/>    | <span data-ttu-id="36cf2-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="36cf2-124">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="36cf2-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="36cf2-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="36cf2-126"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="36cf2-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="36cf2-127">DLL</span><span class="sxs-lookup"><span data-stu-id="36cf2-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36cf2-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36cf2-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36cf2-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="36cf2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36cf2-130">**Emailaction**</span><span class="sxs-lookup"><span data-stu-id="36cf2-130">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="36cf2-131">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="36cf2-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

