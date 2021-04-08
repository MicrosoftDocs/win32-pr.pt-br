---
title: TDN_BUTTON_CLICKED código de notificação (commctrl. h)
description: Enviado por uma caixa de diálogo de tarefa quando o usuário seleciona um botão ou link de comando na caixa de diálogo de tarefa. Esse código de notificação é recebido somente por meio da função de retorno de chamada da caixa de diálogo de tarefa, que pode ser registrada usando o método TaskDialogIndirect.
ms.assetid: eefe48f8-8a80-4280-8a7e-244d9b699ec7
keywords:
- TDN_BUTTON_CLICKED de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TDN_BUTTON_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a7a0b799f4163633194306edaa1703e068e93c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919163"
---
# <a name="tdn_button_clicked-notification-code"></a><span data-ttu-id="758b1-105">O \_ botão TDN \_ clicou em código de notificação</span><span class="sxs-lookup"><span data-stu-id="758b1-105">TDN\_BUTTON\_CLICKED notification code</span></span>

<span data-ttu-id="758b1-106">Enviado por uma caixa de diálogo de tarefa quando o usuário seleciona um botão ou link de comando na caixa de diálogo de tarefa.</span><span class="sxs-lookup"><span data-stu-id="758b1-106">Sent by a task dialog when the user selects a button or command link in the task dialog.</span></span> <span data-ttu-id="758b1-107">Esse código de notificação é recebido somente por meio da função de retorno de chamada da caixa de diálogo de tarefa, que pode ser registrada usando o método [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="758b1-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_BUTTON_CLICKED  

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="758b1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="758b1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="758b1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="758b1-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="758b1-110">Um **int** que especifica a ID do botão ou link o que foi selecionado.</span><span class="sxs-lookup"><span data-stu-id="758b1-110">An **int** that specifies the ID of the button or comand link that was selected.</span></span>

</dd> <dt>

<span data-ttu-id="758b1-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="758b1-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="758b1-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="758b1-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="758b1-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="758b1-113">Return value</span></span>

<span data-ttu-id="758b1-114">Para impedir que a caixa de diálogo de tarefa seja fechada, o aplicativo deve retornar **S \_ false**, caso contrário, a caixa de diálogo de tarefa será fechada e a ID do botão será retornada por meio da chamada de aplicativo original.</span><span class="sxs-lookup"><span data-stu-id="758b1-114">To prevent the task dialog from closing, the application must return **S\_FALSE**, otherwise the task dialog is closed and the button ID is returned via the original application call.</span></span>

## <a name="requirements"></a><span data-ttu-id="758b1-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="758b1-115">Requirements</span></span>



| <span data-ttu-id="758b1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="758b1-116">Requirement</span></span> | <span data-ttu-id="758b1-117">Valor</span><span class="sxs-lookup"><span data-stu-id="758b1-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="758b1-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="758b1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="758b1-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="758b1-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="758b1-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="758b1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="758b1-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="758b1-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="758b1-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="758b1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="758b1-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="758b1-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





