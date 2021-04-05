---
title: TDN_RADIO_BUTTON_CLICKED código de notificação (commctrl. h)
description: Enviado por uma caixa de diálogo de tarefa quando o usuário seleciona um botão de opção ou um link de comando na caixa de diálogo de tarefa. Esse código de notificação é recebido somente por meio da função de retorno de chamada da caixa de diálogo de tarefa, que pode ser registrada usando o método TaskDialogIndirect.
ms.assetid: d9a29874-6755-4754-bcaf-94746b218b47
keywords:
- TDN_RADIO_BUTTON_CLICKED de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TDN_RADIO_BUTTON_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0c8b16f738e4807c94a060b41b3932d0f3e07ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919159"
---
# <a name="tdn_radio_button_clicked-notification-code"></a><span data-ttu-id="3bca5-105">O \_ botão de opção TDN \_ \_ clicou no código de notificação</span><span class="sxs-lookup"><span data-stu-id="3bca5-105">TDN\_RADIO\_BUTTON\_CLICKED notification code</span></span>

<span data-ttu-id="3bca5-106">Enviado por uma caixa de diálogo de tarefa quando o usuário seleciona um botão de opção ou um link de comando na caixa de diálogo de tarefa.</span><span class="sxs-lookup"><span data-stu-id="3bca5-106">Sent by a task dialog when the user selects a radio button or command link in the task dialog.</span></span> <span data-ttu-id="3bca5-107">Esse código de notificação é recebido somente por meio da função de retorno de chamada da caixa de diálogo de tarefa, que pode ser registrada usando o método [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="3bca5-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_RADIO_BUTTON_CLICKED

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="3bca5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3bca5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bca5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3bca5-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3bca5-110">Um **int** que especifica a ID correspondente ao botão de opção que foi clicado.</span><span class="sxs-lookup"><span data-stu-id="3bca5-110">An **int** that specifies the ID corresponding to the radio button that was clicked.</span></span>

</dd> <dt>

<span data-ttu-id="3bca5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3bca5-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3bca5-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="3bca5-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bca5-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3bca5-113">Return value</span></span>

<span data-ttu-id="3bca5-114">O valor de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="3bca5-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bca5-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3bca5-115">Requirements</span></span>



| <span data-ttu-id="3bca5-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3bca5-116">Requirement</span></span> | <span data-ttu-id="3bca5-117">Valor</span><span class="sxs-lookup"><span data-stu-id="3bca5-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3bca5-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3bca5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3bca5-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3bca5-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3bca5-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3bca5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3bca5-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3bca5-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3bca5-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3bca5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3bca5-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3bca5-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





