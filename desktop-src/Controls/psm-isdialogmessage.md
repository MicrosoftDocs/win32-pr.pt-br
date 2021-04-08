---
title: Mensagem de PSM_ISDIALOGMESSAGE (Prsht. h)
description: Passa uma mensagem para uma caixa de diálogo de folha de propriedades e indica se a caixa de diálogo processou a mensagem. Você pode enviar essa mensagem explicitamente ou usando a macro PropSheet \_ IsDialogMessage.
ms.assetid: 7629c3f8-0b10-4585-8a95-9309c75b3ebb
keywords:
- Controles de PSM_ISDIALOGMESSAGE de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_ISDIALOGMESSAGE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b753fc849d76e3ac5071dd85bdd94950460fbb10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824452"
---
# <a name="psm_isdialogmessage-message"></a><span data-ttu-id="1ab83-105">Mensagem de PSM \_ ISDIALOGMESSAGE</span><span class="sxs-lookup"><span data-stu-id="1ab83-105">PSM\_ISDIALOGMESSAGE message</span></span>

<span data-ttu-id="1ab83-106">Passa uma mensagem para uma caixa de diálogo de folha de propriedades e indica se a caixa de diálogo processou a mensagem.</span><span class="sxs-lookup"><span data-stu-id="1ab83-106">Passes a message to a property sheet dialog box and indicates whether the dialog box processed the message.</span></span> <span data-ttu-id="1ab83-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**PropSheet \_ IsDialogMessage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_isdialogmessage) .</span><span class="sxs-lookup"><span data-stu-id="1ab83-107">You can send this message explicitly or by using the [**PropSheet\_IsDialogMessage**](/windows/desktop/api/Prsht/nf-prsht-propsheet_isdialogmessage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="1ab83-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1ab83-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ab83-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1ab83-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1ab83-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="1ab83-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1ab83-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1ab83-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1ab83-112">Ponteiro para uma estrutura de [**msg**](/windows/win32/api/winuser/ns-winuser-msg) que contém a mensagem a ser verificada.</span><span class="sxs-lookup"><span data-stu-id="1ab83-112">Pointer to an [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) structure that contains the message to be checked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ab83-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1ab83-113">Return value</span></span>

<span data-ttu-id="1ab83-114">Retornará **true** se a mensagem tiver sido processada ou **false** se a mensagem não tiver sido processada.</span><span class="sxs-lookup"><span data-stu-id="1ab83-114">Returns **TRUE** if the message has been processed, or **FALSE** if the message has not been processed.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ab83-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="1ab83-115">Remarks</span></span>

<span data-ttu-id="1ab83-116">Seu loop de mensagem deve usar a mensagem de **PSM \_ ISDIALOGMESSAGE** com folhas de propriedades sem janela restrita para passar mensagens para a caixa de diálogo folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="1ab83-116">Your message loop should use the **PSM\_ISDIALOGMESSAGE** message with modeless property sheets to pass messages to the property sheet dialog box.</span></span> <span data-ttu-id="1ab83-117">Em sistemas que dão suporte a Unicode, use as versões Unicode das funções [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) e [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea) (**GetMessageW** e **PeekMessageW**) para recuperar mensagens.</span><span class="sxs-lookup"><span data-stu-id="1ab83-117">On systems that support Unicode, use the Unicode versions of the [**GetMessage**](/windows/desktop/api/winuser/nf-winuser-getmessage) and [**PeekMessage**](/windows/desktop/api/winuser/nf-winuser-peekmessagea) functions (**GetMessageW** and **PeekMessageW**) to retrieve messages.</span></span>

<span data-ttu-id="1ab83-118">Se o valor de retorno indicar que a mensagem foi processada, ela não deverá ser passada para a função [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) ou [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) .</span><span class="sxs-lookup"><span data-stu-id="1ab83-118">If the return value indicates that the message was processed, it must not be passed to the [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) or [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage) function.</span></span>

> [!Note]  
> <span data-ttu-id="1ab83-119">Não há suporte para esta mensagem ao usar o estilo de assistente Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="1ab83-119">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1ab83-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ab83-120">Requirements</span></span>



| <span data-ttu-id="1ab83-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ab83-121">Requirement</span></span> | <span data-ttu-id="1ab83-122">Valor</span><span class="sxs-lookup"><span data-stu-id="1ab83-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1ab83-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ab83-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1ab83-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1ab83-124">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1ab83-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1ab83-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1ab83-126">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1ab83-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1ab83-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1ab83-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ab83-128"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ab83-128"><dt>Prsht.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ab83-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="1ab83-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ab83-130">**Folha**</span><span class="sxs-lookup"><span data-stu-id="1ab83-130">**PropertySheet**</span></span>](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)
</dt> </dl>

 

