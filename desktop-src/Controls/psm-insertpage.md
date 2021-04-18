---
title: Mensagem de PSM_INSERTPAGE (Prsht. h)
description: Insere uma nova página em uma folha de propriedades existente. A página pode ser inserida em um índice especificado ou após uma página especificada. Você pode enviar essa mensagem explicitamente ou usando a macro PropSheet \_ InsertPage.
ms.assetid: 69d55e68-510d-45f1-93d6-ce2bf5dfdb6d
keywords:
- Controles de PSM_INSERTPAGE de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_INSERTPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afdd58536a5cdd18d39a331df4b18c9bbae93842
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105749076"
---
# <a name="psm_insertpage-message"></a><span data-ttu-id="83d9a-106">Mensagem de PSM \_ INSERTPAGE</span><span class="sxs-lookup"><span data-stu-id="83d9a-106">PSM\_INSERTPAGE message</span></span>

<span data-ttu-id="83d9a-107">Insere uma nova página em uma folha de propriedades existente.</span><span class="sxs-lookup"><span data-stu-id="83d9a-107">Inserts a new page into an existing property sheet.</span></span> <span data-ttu-id="83d9a-108">A página pode ser inserida em um índice especificado ou após uma página especificada.</span><span class="sxs-lookup"><span data-stu-id="83d9a-108">The page can be inserted either at a specified index or after a specified page.</span></span> <span data-ttu-id="83d9a-109">Você pode enviar essa mensagem explicitamente ou usando a macro [**PropSheet \_ InsertPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_insertpage) .</span><span class="sxs-lookup"><span data-stu-id="83d9a-109">You can send this message explicitly or by using the [**PropSheet\_InsertPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_insertpage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="83d9a-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="83d9a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83d9a-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="83d9a-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="83d9a-112">Onde a página deve ser inserida.</span><span class="sxs-lookup"><span data-stu-id="83d9a-112">Where the page is to be inserted.</span></span> <span data-ttu-id="83d9a-113">Defina esse parâmetro como **NULL** para tornar a nova página a primeira página.</span><span class="sxs-lookup"><span data-stu-id="83d9a-113">Set this parameter to **NULL** to make the new page the first page.</span></span> <span data-ttu-id="83d9a-114">Para especificar onde a nova página deve ser inserida, você pode passar um índice ou um identificador HPROPSHEETPAGE da página existente.</span><span class="sxs-lookup"><span data-stu-id="83d9a-114">To specify where the new page is to be inserted, you can either pass an index or an existing page's HPROPSHEETPAGE handle.</span></span>



| <span data-ttu-id="83d9a-115">Valor</span><span class="sxs-lookup"><span data-stu-id="83d9a-115">Value</span></span>                                                                                                                                             | <span data-ttu-id="83d9a-116">Significado</span><span class="sxs-lookup"><span data-stu-id="83d9a-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="83d9a-117"><dt></dt><dt>índice</dt> do</span><span class="sxs-lookup"><span data-stu-id="83d9a-117"><dt></dt> <dt>index</dt></span></span> </dl>            | <span data-ttu-id="83d9a-118">Se o parâmetro *wParam* for menor que MAXUSHORT (o maior inteiro curto não atribuído), o *wParam* especificará o índice de base zero para a nova página.</span><span class="sxs-lookup"><span data-stu-id="83d9a-118">If the *wParam* parameter is less than MAXUSHORT (the largest unsigned short integer), the *wParam* specifies the zero-based index for the new page.</span></span> <span data-ttu-id="83d9a-119">Por exemplo, para transformar a página inserida na terceira página da folha de propriedades, defina *wParam* como 2.</span><span class="sxs-lookup"><span data-stu-id="83d9a-119">For example, to make the inserted page the third page on the property sheet, set *wParam* to 2.</span></span> <span data-ttu-id="83d9a-120">Para torná-la a primeira página, defina *wParam* como 0.</span><span class="sxs-lookup"><span data-stu-id="83d9a-120">To make it the first page, set *wParam* to 0.</span></span> <span data-ttu-id="83d9a-121">Se *wParam* tiver um valor maior que o número de páginas e menor que MAXUSHORT, a página será anexada.</span><span class="sxs-lookup"><span data-stu-id="83d9a-121">If *wParam* has a value greater than the number of pages and less than MAXUSHORT, the page will be appended.</span></span><br/> |
| <dl> <span data-ttu-id="83d9a-122"><dt></dt><dt>hpageInsertAfter</dt></span><span class="sxs-lookup"><span data-stu-id="83d9a-122"><dt></dt> <dt>hpageInsertAfter</dt></span></span> </dl> | <span data-ttu-id="83d9a-123">Se você definir o parâmetro *wParam* como um identificador HPROPSHEETPAGE da página existente, a nova página será inserida após ele.</span><span class="sxs-lookup"><span data-stu-id="83d9a-123">If you set the *wParam* parameter to an existing page's HPROPSHEETPAGE handle, the new page will be inserted after it.</span></span><br/>                                                                                                                                                                                                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="83d9a-124">*lParam*</span><span class="sxs-lookup"><span data-stu-id="83d9a-124">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="83d9a-125">Identificador para a página a ser inserida.</span><span class="sxs-lookup"><span data-stu-id="83d9a-125">Handle to the page to be inserted.</span></span> <span data-ttu-id="83d9a-126">A página deve ser criada primeiro por uma chamada para a função [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) .</span><span class="sxs-lookup"><span data-stu-id="83d9a-126">The page must first be created by a call to the [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83d9a-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="83d9a-127">Return value</span></span>

<span data-ttu-id="83d9a-128">Retorna um valor diferente de zero se a página tiver sido inserida com êxito ou zero caso contrário.</span><span class="sxs-lookup"><span data-stu-id="83d9a-128">Returns a nonzero value if the page was successfully inserted, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="83d9a-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="83d9a-129">Remarks</span></span>

<span data-ttu-id="83d9a-130">As páginas após o ponto de inserção são deslocadas para a direita para acomodar a nova página.</span><span class="sxs-lookup"><span data-stu-id="83d9a-130">The pages after the insertion point are shifted to the right to accommodate the new page.</span></span>

<span data-ttu-id="83d9a-131">A folha de propriedades não é redimensionada para se ajustar à nova página.</span><span class="sxs-lookup"><span data-stu-id="83d9a-131">The property sheet is not resized to fit the new page.</span></span> <span data-ttu-id="83d9a-132">Não torne a nova página maior do que a maior página da folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="83d9a-132">Do not make the new page larger than the property sheet's largest page.</span></span>

<span data-ttu-id="83d9a-133">Várias mensagens e uma chamada de função ocorrem enquanto a folha de propriedades está manipulando a lista de páginas.</span><span class="sxs-lookup"><span data-stu-id="83d9a-133">A number of messages and one function call occur while the property sheet is manipulating the list of pages.</span></span> <span data-ttu-id="83d9a-134">Enquanto essa ação está ocorrendo, a tentativa de modificar a lista de páginas terá resultados imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="83d9a-134">While this action is taking place, attempting to modify the list of pages will have unpredictable results.</span></span> <span data-ttu-id="83d9a-135">De acordo, você não deve usar a \_ mensagem de PSM INSERTPAGE em sua implementação do [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) ou ao manipular as notificações e mensagens do Windows a seguir.</span><span class="sxs-lookup"><span data-stu-id="83d9a-135">Accordingly, you should not use the PSM\_INSERTPAGE message in your implementation of [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) or while handling the following notifications and Windows messages.</span></span>

-   [<span data-ttu-id="83d9a-136">PSN \_ aplicar</span><span class="sxs-lookup"><span data-stu-id="83d9a-136">PSN\_APPLY</span></span>](psn-apply.md)
-   [<span data-ttu-id="83d9a-137">PSN \_ KILLACTIVE</span><span class="sxs-lookup"><span data-stu-id="83d9a-137">PSN\_KILLACTIVE</span></span>](psn-killactive.md)
-   [<span data-ttu-id="83d9a-138">redefinição de PSN \_</span><span class="sxs-lookup"><span data-stu-id="83d9a-138">PSN\_RESET</span></span>](psn-reset.md)
-   [<span data-ttu-id="83d9a-139">PSN \_ SETactive</span><span class="sxs-lookup"><span data-stu-id="83d9a-139">PSN\_SETACTIVE</span></span>](psn-setactive.md)
-   [<span data-ttu-id="83d9a-140">**destruição do WM \_**</span><span class="sxs-lookup"><span data-stu-id="83d9a-140">**WM\_DESTROY**</span></span>](/windows/desktop/winmsg/wm-destroy)
-   [<span data-ttu-id="83d9a-141">**INITDIALOG do WM \_**</span><span class="sxs-lookup"><span data-stu-id="83d9a-141">**WM\_INITDIALOG**</span></span>](/windows/desktop/dlgbox/wm-initdialog)

<span data-ttu-id="83d9a-142">Se você precisar modificar uma página de folha de propriedades enquanto estiver manipulando uma dessas mensagens ou enquanto [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) estiver em operação, poste uma mensagem privada do Windows.</span><span class="sxs-lookup"><span data-stu-id="83d9a-142">If you need to modify a property sheet page while you are handling one of these messages or while [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) is in operation, post yourself a private Windows message.</span></span> <span data-ttu-id="83d9a-143">Seu aplicativo não receberá essa mensagem até que o Gerenciador de folhas de propriedades tenha concluído suas tarefas.</span><span class="sxs-lookup"><span data-stu-id="83d9a-143">Your application will not receive that message until after the property sheet manager has finished its tasks.</span></span> <span data-ttu-id="83d9a-144">Em seguida, você pode modificar a lista de páginas.</span><span class="sxs-lookup"><span data-stu-id="83d9a-144">Then you can modify the list of pages.</span></span>

<span data-ttu-id="83d9a-145">As notificações a seguir também são afetadas pela modificação da folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="83d9a-145">The following notifications are also affected by property sheet modification.</span></span>

-   [<span data-ttu-id="83d9a-146">PSN \_ WIZBACK</span><span class="sxs-lookup"><span data-stu-id="83d9a-146">PSN\_WIZBACK</span></span>](psn-wizback.md)
-   [<span data-ttu-id="83d9a-147">PSN \_ WIZNEXT</span><span class="sxs-lookup"><span data-stu-id="83d9a-147">PSN\_WIZNEXT</span></span>](psn-wiznext.md)

<span data-ttu-id="83d9a-148">Você pode adicionar ou remover páginas em resposta a essas notificações, desde que você retorne (via DWL \_ MSGRESULT) um valor diferente de zero para especificar a página nova desejada.</span><span class="sxs-lookup"><span data-stu-id="83d9a-148">You can add or remove pages in response to these notifications, provided that you return (via DWL\_MSGRESULT) a nonzero value to specify the desired new page.</span></span> <span data-ttu-id="83d9a-149">No entanto, observe que, se você inserir uma página que está localizada antes da página atual (que tem um índice menor do que a página atual), [PSN \_ KILLACTIVE](psn-killactive.md) poderá ser enviada para a página errada.</span><span class="sxs-lookup"><span data-stu-id="83d9a-149">Note, however, that if you insert a page that is located before the current page (that has a smaller index than the current page), [PSN\_KILLACTIVE](psn-killactive.md) might be sent to the wrong page.</span></span>

> [!Note]  
> <span data-ttu-id="83d9a-150">Não há suporte para esta mensagem ao usar o estilo de assistente Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="83d9a-150">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="83d9a-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83d9a-151">Requirements</span></span>



| <span data-ttu-id="83d9a-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="83d9a-152">Requirement</span></span> | <span data-ttu-id="83d9a-153">Valor</span><span class="sxs-lookup"><span data-stu-id="83d9a-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="83d9a-154">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83d9a-154">Minimum supported client</span></span><br/> | <span data-ttu-id="83d9a-155">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="83d9a-155">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="83d9a-156">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83d9a-156">Minimum supported server</span></span><br/> | <span data-ttu-id="83d9a-157">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="83d9a-157">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="83d9a-158">parâmetro</span><span class="sxs-lookup"><span data-stu-id="83d9a-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="83d9a-159"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="83d9a-159"><dt>Prsht.h</dt></span></span> </dl> |



 

