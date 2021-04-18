---
title: Mensagem de PSM_GETCURRENTPAGEHWND (Prsht. h)
description: Recupera um identificador para a janela da página atual de uma folha de propriedades. Você pode enviar essa mensagem explicitamente ou usando a macro PropSheet \_ GetCurrentPageHwnd.
ms.assetid: 1f2d0af9-5853-48e7-b827-483be032b6ca
keywords:
- Controles de PSM_GETCURRENTPAGEHWND de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_GETCURRENTPAGEHWND
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae9ac89e6bc60317f2caf31ea92754d10983e11a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755831"
---
# <a name="psm_getcurrentpagehwnd-message"></a><span data-ttu-id="8e582-105">Mensagem de PSM \_ GETCURRENTPAGEHWND</span><span class="sxs-lookup"><span data-stu-id="8e582-105">PSM\_GETCURRENTPAGEHWND message</span></span>

<span data-ttu-id="8e582-106">Recupera um identificador para a janela da página atual de uma folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="8e582-106">Retrieves a handle to the window of the current page of a property sheet.</span></span> <span data-ttu-id="8e582-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**PropSheet \_ GetCurrentPageHwnd**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getcurrentpagehwnd) .</span><span class="sxs-lookup"><span data-stu-id="8e582-107">You can send this message explicitly or by using the [**PropSheet\_GetCurrentPageHwnd**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getcurrentpagehwnd) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8e582-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8e582-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e582-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8e582-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8e582-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="8e582-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="8e582-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8e582-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8e582-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="8e582-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e582-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8e582-113">Return value</span></span>

<span data-ttu-id="8e582-114">Retorna um identificador para a janela da página da folha de propriedades atual.</span><span class="sxs-lookup"><span data-stu-id="8e582-114">Returns a handle to the window of the current property sheet page.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e582-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="8e582-115">Remarks</span></span>

<span data-ttu-id="8e582-116">Use a **mensagem \_ GETCURRENTPAGEHWND de PSM** com folhas de propriedades sem janela restrita para determinar quando destruir a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="8e582-116">Use the **PSM\_GETCURRENTPAGEHWND** message with modeless property sheets to determine when to destroy the dialog box.</span></span> <span data-ttu-id="8e582-117">Quando o usuário clica no botão **OK** ou **Cancelar** , o **PSM \_ GETCURRENTPAGEHWND** retorna **NULL** e, em seguida, você pode usar a função [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) para destruir a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="8e582-117">When the user clicks the **OK** or **Cancel** button, **PSM\_GETCURRENTPAGEHWND** returns **NULL**, and you can then use the [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) function to destroy the dialog box.</span></span>

> [!Note]  
> <span data-ttu-id="8e582-118">Não há suporte para esta mensagem ao usar o estilo de assistente Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="8e582-118">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8e582-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e582-119">Requirements</span></span>



| <span data-ttu-id="8e582-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e582-120">Requirement</span></span> | <span data-ttu-id="8e582-121">Valor</span><span class="sxs-lookup"><span data-stu-id="8e582-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8e582-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8e582-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8e582-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8e582-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8e582-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8e582-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8e582-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8e582-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8e582-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8e582-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e582-127"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e582-127"><dt>Prsht.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e582-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="8e582-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e582-129">**Folha**</span><span class="sxs-lookup"><span data-stu-id="8e582-129">**PropertySheet**</span></span>](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)
</dt> </dl>

 

