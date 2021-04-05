---
title: TDN_VERIFICATION_CLICKED código de notificação (commctrl. h)
description: Enviado por um diálogo de tarefa quando o usuário clica na caixa de seleção de verificação da tarefa. Esse código de notificação é recebido somente por meio da função de retorno de chamada da caixa de diálogo de tarefa, que pode ser registrada usando o método TaskDialogIndirect.
ms.assetid: cd7bc07a-9a70-4361-abfa-986a5a2e13e0
keywords:
- TDN_VERIFICATION_CLICKED de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TDN_VERIFICATION_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7887a4d696f5294ebffc6fc6cc7183ff2c0aed8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919158"
---
# <a name="tdn_verification_clicked-notification-code"></a><span data-ttu-id="0ed19-105">A \_ verificação de TDN \_ clicou no código de notificação</span><span class="sxs-lookup"><span data-stu-id="0ed19-105">TDN\_VERIFICATION\_CLICKED notification code</span></span>

<span data-ttu-id="0ed19-106">Enviado por um diálogo de tarefa quando o usuário clica na caixa de seleção de verificação da tarefa.</span><span class="sxs-lookup"><span data-stu-id="0ed19-106">Sent by a task dialog when the user clicks the task dialog verification check box.</span></span> <span data-ttu-id="0ed19-107">Esse código de notificação é recebido somente por meio da função de retorno de chamada da caixa de diálogo de tarefa, que pode ser registrada usando o método [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="0ed19-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_VERIFICATION_CLICKED

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="0ed19-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0ed19-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ed19-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0ed19-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0ed19-110">Um **bool** que especifica o status da caixa de seleção de verificação.</span><span class="sxs-lookup"><span data-stu-id="0ed19-110">A **BOOL** that specifies the status of the verification checkbox.</span></span> <span data-ttu-id="0ed19-111">Será **true** se a caixa de seleção de verificação estiver marcada ou **false** se estiver desmarcada.</span><span class="sxs-lookup"><span data-stu-id="0ed19-111">It is **TRUE** if the verification checkbox is checked, or **FALSE** if it is unchecked.</span></span>

</dd> <dt>

<span data-ttu-id="0ed19-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0ed19-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0ed19-113">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="0ed19-113">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ed19-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0ed19-114">Return value</span></span>

<span data-ttu-id="0ed19-115">O valor de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="0ed19-115">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ed19-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ed19-116">Requirements</span></span>



| <span data-ttu-id="0ed19-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ed19-117">Requirement</span></span> | <span data-ttu-id="0ed19-118">Valor</span><span class="sxs-lookup"><span data-stu-id="0ed19-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0ed19-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0ed19-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0ed19-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0ed19-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0ed19-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0ed19-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0ed19-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0ed19-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0ed19-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0ed19-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ed19-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ed19-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ed19-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="0ed19-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="0ed19-126">**Referência**</span><span class="sxs-lookup"><span data-stu-id="0ed19-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0ed19-127">*TaskDialogCallbackProc*</span><span class="sxs-lookup"><span data-stu-id="0ed19-127">*TaskDialogCallbackProc*</span></span>](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback)
</dt> </dl>

 

