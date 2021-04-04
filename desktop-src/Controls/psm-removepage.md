---
title: Mensagem de PSM_REMOVEPAGE (Prsht. h)
description: Remove uma página de uma folha de propriedades. Você pode enviar essa mensagem explicitamente ou usando a macro PropSheet \_ RemovePage.
ms.assetid: 2f387e97-4db4-4ad5-8600-7325da674e33
keywords:
- Controles de PSM_REMOVEPAGE de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_REMOVEPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cae1611e1ed9540fce23d20681f44849903e5c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824634"
---
# <a name="psm_removepage-message"></a><span data-ttu-id="6fa64-105">Mensagem de PSM \_ REMOVEPAGE</span><span class="sxs-lookup"><span data-stu-id="6fa64-105">PSM\_REMOVEPAGE message</span></span>

<span data-ttu-id="6fa64-106">Remove uma página de uma folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="6fa64-106">Removes a page from a property sheet.</span></span> <span data-ttu-id="6fa64-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**PropSheet \_ RemovePage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_removepage) .</span><span class="sxs-lookup"><span data-stu-id="6fa64-107">You can send this message explicitly or by using the [**PropSheet\_RemovePage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_removepage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6fa64-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6fa64-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fa64-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6fa64-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6fa64-110">Índice de base zero da página a ser removida.</span><span class="sxs-lookup"><span data-stu-id="6fa64-110">Zero-based index of the page to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="6fa64-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6fa64-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6fa64-112">O identificador de HPROPSHEETPAGE da página a ser removida.</span><span class="sxs-lookup"><span data-stu-id="6fa64-112">The HPROPSHEETPAGE handle of the page to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fa64-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6fa64-113">Return value</span></span>

<span data-ttu-id="6fa64-114">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="6fa64-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6fa64-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="6fa64-115">Remarks</span></span>

<span data-ttu-id="6fa64-116">Um aplicativo pode especificar o índice ou o identificador, ou ambos.</span><span class="sxs-lookup"><span data-stu-id="6fa64-116">An application can specify the index or the handle, or both.</span></span> <span data-ttu-id="6fa64-117">Se ambos forem especificados, *lParam* terá precedência.</span><span class="sxs-lookup"><span data-stu-id="6fa64-117">If both are specified, *lParam* takes precedence.</span></span>

<span data-ttu-id="6fa64-118">O envio de **PSM \_ REMOVEPAGE** destrói a página da folha de propriedades que está sendo removida.</span><span class="sxs-lookup"><span data-stu-id="6fa64-118">Sending **PSM\_REMOVEPAGE** destroys the property sheet page that is being removed.</span></span>

<span data-ttu-id="6fa64-119">Várias mensagens e uma chamada de função ocorrem enquanto a folha de propriedades está manipulando a lista de páginas.</span><span class="sxs-lookup"><span data-stu-id="6fa64-119">A number of messages and one function call occur while the property sheet is manipulating the list of pages.</span></span> <span data-ttu-id="6fa64-120">Enquanto essa ação está ocorrendo, a tentativa de modificar a lista de páginas terá resultados imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="6fa64-120">While this action is taking place, attempting to modify the list of pages will have unpredictable results.</span></span> <span data-ttu-id="6fa64-121">De acordo, você não deve usar a mensagem de **PSM \_ REMOVEPAGE** em sua implementação do [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) ou ao manipular as notificações e mensagens do Windows a seguir.</span><span class="sxs-lookup"><span data-stu-id="6fa64-121">Accordingly, you should not use the **PSM\_REMOVEPAGE** message in your implementation of [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) or while handling the following notifications and Windows messages.</span></span>

-   [<span data-ttu-id="6fa64-122">PSN \_ aplicar</span><span class="sxs-lookup"><span data-stu-id="6fa64-122">PSN\_APPLY</span></span>](psn-apply.md)
-   [<span data-ttu-id="6fa64-123">PSN \_ KILLACTIVE</span><span class="sxs-lookup"><span data-stu-id="6fa64-123">PSN\_KILLACTIVE</span></span>](psn-killactive.md)
-   [<span data-ttu-id="6fa64-124">redefinição de PSN \_</span><span class="sxs-lookup"><span data-stu-id="6fa64-124">PSN\_RESET</span></span>](psn-reset.md)
-   [<span data-ttu-id="6fa64-125">PSN \_ SETactive</span><span class="sxs-lookup"><span data-stu-id="6fa64-125">PSN\_SETACTIVE</span></span>](psn-setactive.md)
-   [<span data-ttu-id="6fa64-126">**destruição do WM \_**</span><span class="sxs-lookup"><span data-stu-id="6fa64-126">**WM\_DESTROY**</span></span>](/windows/desktop/winmsg/wm-destroy)
-   [<span data-ttu-id="6fa64-127">**INITDIALOG do WM \_**</span><span class="sxs-lookup"><span data-stu-id="6fa64-127">**WM\_INITDIALOG**</span></span>](/windows/desktop/dlgbox/wm-initdialog)

<span data-ttu-id="6fa64-128">Se você precisar modificar uma página de folha de propriedades enquanto estiver manipulando uma dessas mensagens ou enquanto [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) estiver em operação, poste uma mensagem privada do Windows.</span><span class="sxs-lookup"><span data-stu-id="6fa64-128">If you need to modify a property sheet page while you are handling one of these messages or while [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) is in operation, post yourself a private Windows message.</span></span> <span data-ttu-id="6fa64-129">Seu aplicativo não receberá essa mensagem até que o Gerenciador de folhas de propriedades tenha concluído suas tarefas.</span><span class="sxs-lookup"><span data-stu-id="6fa64-129">Your application will not receive that message until after the property sheet manager has finished its tasks.</span></span> <span data-ttu-id="6fa64-130">Em seguida, você pode modificar a lista de páginas.</span><span class="sxs-lookup"><span data-stu-id="6fa64-130">Then you can modify the list of pages.</span></span>

<span data-ttu-id="6fa64-131">As notificações a seguir também são afetadas pela modificação da folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="6fa64-131">The following notifications are also affected by property sheet modification.</span></span>

-   [<span data-ttu-id="6fa64-132">PSN \_ WIZBACK</span><span class="sxs-lookup"><span data-stu-id="6fa64-132">PSN\_WIZBACK</span></span>](psn-wizback.md)
-   [<span data-ttu-id="6fa64-133">PSN \_ WIZNEXT</span><span class="sxs-lookup"><span data-stu-id="6fa64-133">PSN\_WIZNEXT</span></span>](psn-wiznext.md)

<span data-ttu-id="6fa64-134">Você pode adicionar ou remover páginas em resposta a essas notificações, desde que você retorne (via DWL \_ MSGRESULT) um valor diferente de zero para especificar a página nova desejada.</span><span class="sxs-lookup"><span data-stu-id="6fa64-134">You can add or remove pages in response to these notifications, provided that you return (via DWL\_MSGRESULT) a nonzero value to specify the desired new page.</span></span> <span data-ttu-id="6fa64-135">No entanto, observe que se você remover uma página que está localizada antes da página atual (que tem um índice menor do que a página atual), [PSN \_ KILLACTIVE](psn-killactive.md) poderá ser enviada para a página errada.</span><span class="sxs-lookup"><span data-stu-id="6fa64-135">Note, however, that if you remove a page that is located before the current page (that has a smaller index than the current page), [PSN\_KILLACTIVE](psn-killactive.md) might be sent to the wrong page.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fa64-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6fa64-136">Requirements</span></span>



| <span data-ttu-id="6fa64-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fa64-137">Requirement</span></span> | <span data-ttu-id="6fa64-138">Valor</span><span class="sxs-lookup"><span data-stu-id="6fa64-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6fa64-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6fa64-139">Minimum supported client</span></span><br/> | <span data-ttu-id="6fa64-140">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6fa64-140">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6fa64-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6fa64-141">Minimum supported server</span></span><br/> | <span data-ttu-id="6fa64-142">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6fa64-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6fa64-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6fa64-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fa64-144"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="6fa64-144"><dt>Prsht.h</dt></span></span> </dl> |



 

