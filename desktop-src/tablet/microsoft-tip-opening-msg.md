---
description: Notifica a janela quando o painel de entrada de texto está sendo aberto.
ms.assetid: 6eadd648-bffb-4227-bdcd-cd733f692734
title: Mensagem de MICROSOFT_TIP_OPENING_MSG (PenInputPanel. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f0938b8a00e39f54817b8ec52e86e00aae52111
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105815549"
---
# <a name="microsoft_tip_opening_msg-message"></a><span data-ttu-id="4a932-103">\_Mensagem do \_ msg de abertura do Microsoft Tip \_</span><span class="sxs-lookup"><span data-stu-id="4a932-103">MICROSOFT\_TIP\_OPENING\_MSG message</span></span>

<span data-ttu-id="4a932-104">Notifica a janela quando o painel de entrada de texto está sendo aberto.</span><span class="sxs-lookup"><span data-stu-id="4a932-104">Notifies the window when the Text Input Panel is opening.</span></span>

## <a name="parameters"></a><span data-ttu-id="4a932-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4a932-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a932-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4a932-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4a932-107">Atualmente não usado, deve ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="4a932-107">Currently not used, should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4a932-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4a932-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4a932-109">Atualmente não usado, deve ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="4a932-109">Currently not used, should be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a932-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4a932-110">Return value</span></span>

<span data-ttu-id="4a932-111">Os aplicativos devem chamar [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) depois de manipular essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="4a932-111">Applications should call [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) after handling this message.</span></span> <span data-ttu-id="4a932-112">Consulte **DefWindowProc** para obter informações sobre seus valores de retorno.</span><span class="sxs-lookup"><span data-stu-id="4a932-112">See **DefWindowProc** for information about its return values.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a932-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="4a932-113">Remarks</span></span>

<span data-ttu-id="4a932-114">Essa notificação permite que você saiba quando o painel de entrada está abrindo.</span><span class="sxs-lookup"><span data-stu-id="4a932-114">This notification lets you know when the input panel is opening.</span></span> <span data-ttu-id="4a932-115">Se você quiser executar uma ação quando isso acontecer, manipule a mensagem, execute a operação no manipulador e, em seguida, passe a mensagem para [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="4a932-115">If you want to perform an action when this happens, handle the message, perform your operation in the handler, and then pass on the message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span>

> [!Note]  
> <span data-ttu-id="4a932-116">Essa mensagem também é enviada quando o painel de entrada de texto já está visível e o usuário alterna do teclado para a capa de manuscrito.</span><span class="sxs-lookup"><span data-stu-id="4a932-116">This message is also sent when the Text Input Panel is already visible and the user switches from the keyboard to the handwriting skin.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4a932-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a932-117">Requirements</span></span>



| <span data-ttu-id="4a932-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a932-118">Requirement</span></span> | <span data-ttu-id="4a932-119">Valor</span><span class="sxs-lookup"><span data-stu-id="4a932-119">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a932-120">Cliente</span><span class="sxs-lookup"><span data-stu-id="4a932-120">Client</span></span><br/> | <span data-ttu-id="4a932-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4a932-121">Windows Vista</span></span><br/>                                                                   |
| <span data-ttu-id="4a932-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4a932-122">Header</span></span><br/> | <dl> <span data-ttu-id="4a932-123"><dt>PenInputPanel. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a932-123"><dt>Peninputpanel.h</dt></span></span> </dl> |



 

