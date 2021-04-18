---
title: TDN_EXPANDO_BUTTON_CLICKED código de notificação (commctrl. h)
description: Enviado pela caixa de diálogo de tarefa quando o usuário clica no botão expando da caixa de diálogo. Essa notificação é recebida somente por meio da função de retorno de chamada da caixa de diálogo de tarefa, que pode ser registrada usando o método TaskDialogIndirect.
ms.assetid: 15e2a9d0-9986-4fb1-a15e-dd4839e45146
keywords:
- TDN_EXPANDO_BUTTON_CLICKED de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TDN_EXPANDO_BUTTON_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f3c36379a8efc40c7873d817b832705b3c1e084
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105748854"
---
# <a name="tdn_expando_button_clicked-notification-code"></a><span data-ttu-id="4f57a-105">O \_ botão expanda TDN \_ \_ clicou no código de notificação</span><span class="sxs-lookup"><span data-stu-id="4f57a-105">TDN\_EXPANDO\_BUTTON\_CLICKED notification code</span></span>

<span data-ttu-id="4f57a-106">Enviado pela caixa de diálogo de tarefa quando o usuário clica no botão expando da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="4f57a-106">Sent by the task dialog when the user clicks on the dialog's expando button.</span></span> <span data-ttu-id="4f57a-107">Essa notificação é recebida somente por meio da função de retorno de chamada da caixa de diálogo de tarefa, que pode ser registrada usando o método [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="4f57a-107">This notification is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_EXPANDO_BUTTON_CLICKED
        
   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="4f57a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4f57a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f57a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4f57a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4f57a-110">Um **bool** que será **verdadeiro** se a caixa de diálogo for expandida ou **false** se não.</span><span class="sxs-lookup"><span data-stu-id="4f57a-110">A **BOOL** that is **TRUE** if the dialog is expanded, or **FALSE** if not.</span></span>

</dd> <dt>

<span data-ttu-id="4f57a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4f57a-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4f57a-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="4f57a-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f57a-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4f57a-113">Return value</span></span>

<span data-ttu-id="4f57a-114">O valor de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="4f57a-114">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f57a-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="4f57a-115">Remarks</span></span>

<span data-ttu-id="4f57a-116">O exemplo na seção sintaxe mostra a conversão para wParam antes de enviar a notificação.</span><span class="sxs-lookup"><span data-stu-id="4f57a-116">The example in the Syntax section shows the cast to wParam before sending the notification.</span></span> <span data-ttu-id="4f57a-117">**LParam** não é usado e deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="4f57a-117">**LPARAM** is not used and must be zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f57a-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f57a-118">Requirements</span></span>



| <span data-ttu-id="4f57a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f57a-119">Requirement</span></span> | <span data-ttu-id="4f57a-120">Valor</span><span class="sxs-lookup"><span data-stu-id="4f57a-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4f57a-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4f57a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4f57a-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4f57a-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4f57a-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4f57a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4f57a-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4f57a-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4f57a-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4f57a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f57a-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f57a-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





