---
title: Mensagem de TDM_NAVIGATE_PAGE (commctrl. h)
description: Recria uma caixa de diálogo de tarefa com novo conteúdo, simulando a funcionalidade de um assistente de várias páginas.
ms.assetid: e0eefd08-e279-47db-97e9-7ca86b41e22f
keywords:
- Controles de TDM_NAVIGATE_PAGE de mensagens do Windows
topic_type:
- apiref
api_name:
- TDM_NAVIGATE_PAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56fc86e0e4fe457a43e035ed5d568e91303c7fcd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919078"
---
# <a name="tdm_navigate_page-message"></a><span data-ttu-id="f5193-104">\_ \_ Mensagem da página de navegação TDM</span><span class="sxs-lookup"><span data-stu-id="f5193-104">TDM\_NAVIGATE\_PAGE message</span></span>

<span data-ttu-id="f5193-105">Recria uma caixa de diálogo de tarefa com novo conteúdo, simulando a funcionalidade de um assistente de várias páginas.</span><span class="sxs-lookup"><span data-stu-id="f5193-105">Recreates a task dialog with new contents, simulating the functionality of a multi-page wizard.</span></span>

## <a name="parameters"></a><span data-ttu-id="f5193-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f5193-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5193-107">*wParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f5193-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5193-108">Não usado.</span><span class="sxs-lookup"><span data-stu-id="f5193-108">Not used.</span></span> <span data-ttu-id="f5193-109">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="f5193-109">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f5193-110">*lParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f5193-110">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5193-111">Um ponteiro para uma estrutura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) que descreve a caixa de diálogo de tarefa a ser criada.</span><span class="sxs-lookup"><span data-stu-id="f5193-111">A pointer to a [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) structure that describes the task dialog to create.</span></span> <span data-ttu-id="f5193-112">O aplicativo de chamada deve alocar essa estrutura e definir seus membros.</span><span class="sxs-lookup"><span data-stu-id="f5193-112">The calling application must allocate this structure and set its members.</span></span> <span data-ttu-id="f5193-113">Os valores dos membros variam dependendo do tipo de página para a qual o usuário navega.</span><span class="sxs-lookup"><span data-stu-id="f5193-113">The values of the members vary depending on the kind of page the user navigates to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5193-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f5193-114">Return value</span></span>

<span data-ttu-id="f5193-115">O valor de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="f5193-115">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5193-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="f5193-116">Remarks</span></span>

<span data-ttu-id="f5193-117">Para iniciar uma caixa de diálogo de tarefa do assistente, use a função [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="f5193-117">To launch a wizard task dialog, use the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) function.</span></span> <span data-ttu-id="f5193-118">À medida que o usuário navega usando o assistente, envie essa mensagem para a caixa de diálogo de tarefa para exibir a próxima página.</span><span class="sxs-lookup"><span data-stu-id="f5193-118">As the user navigates using the wizard, send this message to the task dialog to display the next page.</span></span> <span data-ttu-id="f5193-119">Uma caixa de diálogo Nova tarefa (semelhante a uma nova página) é criada com os elementos especificados na estrutura apontada por *lParam*.</span><span class="sxs-lookup"><span data-stu-id="f5193-119">A new task dialog (looks like a new page) is created with the elements specified in the structure pointed to by *lParam*.</span></span> <span data-ttu-id="f5193-120">Na criação, todo o conteúdo do quadro da caixa de diálogo é destruído e reconstruído.</span><span class="sxs-lookup"><span data-stu-id="f5193-120">At creation, the entire contents of the dialog frame are destroyed and reconstructed.</span></span> <span data-ttu-id="f5193-121">Como resultado, todas as informações de estado mantidas pelos controles (por exemplo, uma barra de progresso, um botão expando ou uma caixa de seleção de verificação) na caixa de diálogo são perdidas.</span><span class="sxs-lookup"><span data-stu-id="f5193-121">As a result, any state information held by controls (for example, a progress bar, expando button, or verification checkbox) in the dialog is lost.</span></span>

<span data-ttu-id="f5193-122">O layout da caixa de diálogo de tarefa pode falhar e isso pode não ser refletido no valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="f5193-122">The layout of the task dialog may fail and this may not be reflected in the return value.</span></span> <span data-ttu-id="f5193-123">Um valor de retorno de S \_ OK reflete apenas que a caixa de diálogo de tarefa recebeu a mensagem e tentou processá-la.</span><span class="sxs-lookup"><span data-stu-id="f5193-123">A return value of S\_OK reflects only that the task dialog received the message and attempted to process it.</span></span> <span data-ttu-id="f5193-124">Se o layout da caixa de diálogo de tarefa falhar (a caixa de diálogo de tarefa não pode ser exibida), a caixa de diálogo será fechada e um código **HRESULT** será retornado na função de retorno de chamada registrada.</span><span class="sxs-lookup"><span data-stu-id="f5193-124">If the layout of the task dialog fails (the task dialog cannot be displayed), the dialog will close and an **HRESULT** code is returned at the registered callback function.</span></span> <span data-ttu-id="f5193-125">Para obter mais informações sobre a sintaxe da função de retorno de chamada, consulte [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback).</span><span class="sxs-lookup"><span data-stu-id="f5193-125">For more information on the callback function syntax, see [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback).</span></span>

## <a name="requirements"></a><span data-ttu-id="f5193-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5193-126">Requirements</span></span>



| <span data-ttu-id="f5193-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5193-127">Requirement</span></span> | <span data-ttu-id="f5193-128">Valor</span><span class="sxs-lookup"><span data-stu-id="f5193-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f5193-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5193-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f5193-130">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f5193-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f5193-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5193-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f5193-132">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f5193-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f5193-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f5193-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5193-134"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5193-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

