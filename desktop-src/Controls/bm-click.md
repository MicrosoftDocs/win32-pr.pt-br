---
title: Mensagem de BM_CLICK (WinUser. h)
description: Simula o usuário clicando em um botão. Essa mensagem faz com que o botão receba as \_ mensagens do WM LBUTTONDOWN e do WM \_ LBUTTONUP, e a janela pai do botão receba um \_ código de notificação clicado em bilhão.
ms.assetid: f76ca5eb-170c-43fc-a239-67af15497f08
keywords:
- Controles de BM_CLICK de mensagens do Windows
topic_type:
- apiref
api_name:
- BM_CLICK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b86c4809ac1ded3a9b7c57d1b73b70ab1cebc3b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009074"
---
# <a name="bm_click-message"></a><span data-ttu-id="95616-105">BM \_ clique em mensagem</span><span class="sxs-lookup"><span data-stu-id="95616-105">BM\_CLICK message</span></span>

<span data-ttu-id="95616-106">Simula o usuário clicando em um botão.</span><span class="sxs-lookup"><span data-stu-id="95616-106">Simulates the user clicking a button.</span></span> <span data-ttu-id="95616-107">Essa mensagem faz com que o botão receba as mensagens do [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) e do [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) , e a janela pai do botão receba um código de notificação [ \_ clicado em bilhão](bn-clicked.md) .</span><span class="sxs-lookup"><span data-stu-id="95616-107">This message causes the button to receive the [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) and [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) messages, and the button's parent window to receive a [BN\_CLICKED](bn-clicked.md) notification code.</span></span>

## <a name="parameters"></a><span data-ttu-id="95616-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="95616-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95616-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="95616-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="95616-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="95616-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="95616-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="95616-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="95616-112">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="95616-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95616-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="95616-113">Return value</span></span>

<span data-ttu-id="95616-114">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="95616-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="95616-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="95616-115">Remarks</span></span>

<span data-ttu-id="95616-116">Se o botão estiver em uma caixa de diálogo e a caixa de diálogo não estiver ativa, a mensagem de **\_ clique BM** poderá falhar.</span><span class="sxs-lookup"><span data-stu-id="95616-116">If the button is in a dialog box and the dialog box is not active, the **BM\_CLICK** message might fail.</span></span> <span data-ttu-id="95616-117">Para garantir o sucesso nessa situação, chame a função [**SetActiveWindow**](/windows/desktop/api/winuser/nf-winuser-setactivewindow) para ativar a caixa de diálogo antes de enviar a mensagem de **\_ clique BM** para o botão.</span><span class="sxs-lookup"><span data-stu-id="95616-117">To ensure success in this situation, call the [**SetActiveWindow**](/windows/desktop/api/winuser/nf-winuser-setactivewindow) function to activate the dialog box before sending the **BM\_CLICK** message to the button.</span></span>

## <a name="requirements"></a><span data-ttu-id="95616-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95616-118">Requirements</span></span>



| <span data-ttu-id="95616-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="95616-119">Requirement</span></span> | <span data-ttu-id="95616-120">Valor</span><span class="sxs-lookup"><span data-stu-id="95616-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95616-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95616-121">Minimum supported client</span></span><br/> | <span data-ttu-id="95616-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="95616-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="95616-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95616-123">Minimum supported server</span></span><br/> | <span data-ttu-id="95616-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="95616-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="95616-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="95616-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="95616-126"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="95616-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

