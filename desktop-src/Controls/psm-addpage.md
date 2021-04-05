---
title: Mensagem de PSM_ADDPAGE (Prsht. h)
description: Adiciona uma nova página ao final de uma folha de propriedades existente. Você pode enviar essa mensagem explicitamente ou usando a macro PropSheet do \_ AddPage.
ms.assetid: 41f9a09e-6de6-466b-bdfa-c8c4e8f193e4
keywords:
- Controles de PSM_ADDPAGE de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_ADDPAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c4d09e07dfa2be86e11fa33863f091732955714
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824637"
---
# <a name="psm_addpage-message"></a><span data-ttu-id="7dada-105">Mensagem de PSM \_ ADDPAGE</span><span class="sxs-lookup"><span data-stu-id="7dada-105">PSM\_ADDPAGE message</span></span>

<span data-ttu-id="7dada-106">Adiciona uma nova página ao final de uma folha de propriedades existente.</span><span class="sxs-lookup"><span data-stu-id="7dada-106">Adds a new page to the end of an existing property sheet.</span></span> <span data-ttu-id="7dada-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**PropSheet do \_ AddPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_addpage) .</span><span class="sxs-lookup"><span data-stu-id="7dada-107">You can send this message explicitly or by using the [**PropSheet\_AddPage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_addpage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7dada-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7dada-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7dada-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7dada-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7dada-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="7dada-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="7dada-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7dada-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7dada-112">Identificador para a página a ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="7dada-112">Handle to the page to add.</span></span> <span data-ttu-id="7dada-113">A página deve ter sido criada por uma chamada anterior para a função [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) .</span><span class="sxs-lookup"><span data-stu-id="7dada-113">The page must have been created by a previous call to the [**CreatePropertySheetPage**](/windows/desktop/api/Prsht/nf-prsht-createpropertysheetpagea) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7dada-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7dada-114">Return value</span></span>

<span data-ttu-id="7dada-115">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="7dada-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7dada-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="7dada-116">Remarks</span></span>

<span data-ttu-id="7dada-117">A nova página não deve ser maior do que a maior página atualmente na folha de propriedades porque a folha de propriedades não é redimensionada para se ajustar à nova página.</span><span class="sxs-lookup"><span data-stu-id="7dada-117">The new page should be no larger than the largest page currently in the property sheet because the property sheet is not resized to fit the new page.</span></span>

<span data-ttu-id="7dada-118">Várias mensagens e uma chamada de função ocorrem enquanto a folha de propriedades está manipulando a lista de páginas.</span><span class="sxs-lookup"><span data-stu-id="7dada-118">A number of messages and one function call occur while the property sheet is manipulating the list of pages.</span></span> <span data-ttu-id="7dada-119">Enquanto essa ação está ocorrendo, a tentativa de modificar a lista de páginas terá resultados imprevisíveis.</span><span class="sxs-lookup"><span data-stu-id="7dada-119">While this action is taking place, attempting to modify the list of pages will have unpredictable results.</span></span> <span data-ttu-id="7dada-120">De acordo, você não deve usar a \_ mensagem de PSM ADDPAGE em sua implementação do [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) ou ao manipular as notificações e mensagens do Windows a seguir.</span><span class="sxs-lookup"><span data-stu-id="7dada-120">Accordingly, you should not use the PSM\_ADDPAGE message in your implementation of [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) or while handling the following notifications and Windows messages.</span></span>

-   [<span data-ttu-id="7dada-121">PSN \_ aplicar</span><span class="sxs-lookup"><span data-stu-id="7dada-121">PSN\_APPLY</span></span>](psn-apply.md)
-   [<span data-ttu-id="7dada-122">PSN \_ KILLACTIVE</span><span class="sxs-lookup"><span data-stu-id="7dada-122">PSN\_KILLACTIVE</span></span>](psn-killactive.md)
-   [<span data-ttu-id="7dada-123">redefinição de PSN \_</span><span class="sxs-lookup"><span data-stu-id="7dada-123">PSN\_RESET</span></span>](psn-reset.md)
-   [<span data-ttu-id="7dada-124">PSN \_ SETactive</span><span class="sxs-lookup"><span data-stu-id="7dada-124">PSN\_SETACTIVE</span></span>](psn-setactive.md)
-   [<span data-ttu-id="7dada-125">**destruição do WM \_**</span><span class="sxs-lookup"><span data-stu-id="7dada-125">**WM\_DESTROY**</span></span>](/windows/desktop/winmsg/wm-destroy)
-   [<span data-ttu-id="7dada-126">**INITDIALOG do WM \_**</span><span class="sxs-lookup"><span data-stu-id="7dada-126">**WM\_INITDIALOG**</span></span>](/windows/desktop/dlgbox/wm-initdialog)

<span data-ttu-id="7dada-127">Se você precisar modificar uma página de folha de propriedades enquanto estiver manipulando uma dessas mensagens ou enquanto [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) estiver em operação, poste uma mensagem privada do Windows.</span><span class="sxs-lookup"><span data-stu-id="7dada-127">If you need to modify a property sheet page while you are handling one of these messages or while [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) is in operation, post yourself a private Windows message.</span></span> <span data-ttu-id="7dada-128">Seu aplicativo não receberá essa mensagem até que o Gerenciador de folhas de propriedades tenha concluído suas tarefas.</span><span class="sxs-lookup"><span data-stu-id="7dada-128">Your application will not receive that message until after the property sheet manager has finished its tasks.</span></span> <span data-ttu-id="7dada-129">Em seguida, você pode modificar a lista de páginas.</span><span class="sxs-lookup"><span data-stu-id="7dada-129">Then you can modify the list of pages.</span></span>

## <a name="requirements"></a><span data-ttu-id="7dada-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7dada-130">Requirements</span></span>



| <span data-ttu-id="7dada-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="7dada-131">Requirement</span></span> | <span data-ttu-id="7dada-132">Valor</span><span class="sxs-lookup"><span data-stu-id="7dada-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7dada-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7dada-133">Minimum supported client</span></span><br/> | <span data-ttu-id="7dada-134">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7dada-134">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7dada-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7dada-135">Minimum supported server</span></span><br/> | <span data-ttu-id="7dada-136">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7dada-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7dada-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7dada-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="7dada-138"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="7dada-138"><dt>Prsht.h</dt></span></span> </dl> |



 

