---
title: TDN_HELP código de notificação (commctrl. h)
description: Enviado por uma caixa de diálogo de tarefa quando o usuário pressiona F1 no teclado enquanto a caixa de diálogo tem foco. Esse código de notificação é recebido somente por meio da função de retorno de chamada da caixa de diálogo de tarefa, que pode ser registrada usando o método TaskDialogIndirect.
ms.assetid: 207ba231-639d-4906-b5dc-1592f2717f1c
keywords:
- TDN_HELP de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TDN_HELP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64d5e08342094aec5adc3da42621307d1577cd68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086408"
---
# <a name="tdn_help-notification-code"></a><span data-ttu-id="cac39-105">Código de notificação da ajuda do TDN \_</span><span class="sxs-lookup"><span data-stu-id="cac39-105">TDN\_HELP notification code</span></span>

<span data-ttu-id="cac39-106">Enviado por uma caixa de diálogo de tarefa quando o usuário pressiona F1 no teclado enquanto a caixa de diálogo tem foco.</span><span class="sxs-lookup"><span data-stu-id="cac39-106">Sent by a task dialog when the user presses F1 on the keyboard while the dialog has focus.</span></span> <span data-ttu-id="cac39-107">Esse código de notificação é recebido somente por meio da função de retorno de chamada da caixa de diálogo de tarefa, que pode ser registrada usando o método [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="cac39-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_HELP
        
   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="cac39-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cac39-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cac39-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cac39-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cac39-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="cac39-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="cac39-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cac39-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cac39-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="cac39-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cac39-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cac39-113">Return value</span></span>

<span data-ttu-id="cac39-114">O valor de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="cac39-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="cac39-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cac39-115">Requirements</span></span>



| <span data-ttu-id="cac39-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="cac39-116">Requirement</span></span> | <span data-ttu-id="cac39-117">Valor</span><span class="sxs-lookup"><span data-stu-id="cac39-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cac39-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cac39-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cac39-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cac39-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cac39-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cac39-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cac39-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cac39-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cac39-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cac39-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="cac39-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="cac39-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





