---
title: Mensagem de CBEM_HASEDITCHANGED (commctrl. h)
description: Determina se o usuário alterou o texto de um controle de edição ComboBoxEx.
ms.assetid: 8bf8c40a-e1ab-4748-899b-a9ed27767884
keywords:
- Controles de CBEM_HASEDITCHANGED de mensagens do Windows
topic_type:
- apiref
api_name:
- CBEM_HASEDITCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5234b816a2ec080449ade072981b489968df8f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919173"
---
# <a name="cbem_haseditchanged-message"></a><span data-ttu-id="34855-104">\_Mensagem CBEM HASEDITCHANGED</span><span class="sxs-lookup"><span data-stu-id="34855-104">CBEM\_HASEDITCHANGED message</span></span>

<span data-ttu-id="34855-105">Determina se o usuário alterou o texto de um controle de edição ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="34855-105">Determines whether the user has changed the text of a ComboBoxEx edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="34855-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="34855-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34855-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="34855-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="34855-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="34855-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="34855-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="34855-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="34855-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="34855-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34855-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="34855-111">Return value</span></span>

<span data-ttu-id="34855-112">Retornará **true** se o texto na caixa de edição do controle tiver sido alterado ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="34855-112">Returns **TRUE** if the text in the control's edit box has been changed, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="34855-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="34855-113">Remarks</span></span>

<span data-ttu-id="34855-114">Um controle ComboBoxEx usa um controle de caixa de edição quando ele é definido como o estilo [**\_ suspenso CBS**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="34855-114">A ComboBoxEx control uses an edit box control when it is set to the [**CBS\_DROPDOWN**](combo-box-styles.md) style.</span></span> <span data-ttu-id="34855-115">Você pode recuperar o identificador de janela do controle caixa de edição enviando uma mensagem [**CBEM \_ GETEDITCONTROL**](cbem-geteditcontrol.md) .</span><span class="sxs-lookup"><span data-stu-id="34855-115">You can retrieve the edit box control's window handle by sending a [**CBEM\_GETEDITCONTROL**](cbem-geteditcontrol.md) message.</span></span>

<span data-ttu-id="34855-116">Quando o usuário começar a editar, você receberá uma notificação [CBEN \_ BEGINEDIT](cben-beginedit.md) .</span><span class="sxs-lookup"><span data-stu-id="34855-116">When the user begins editing, you will receive a [CBEN\_BEGINEDIT](cben-beginedit.md) notification.</span></span> <span data-ttu-id="34855-117">Quando a edição for concluída ou o foco for alterado, você receberá uma notificação [CBEN \_ ENDEDIT](cben-endedit.md) .</span><span class="sxs-lookup"><span data-stu-id="34855-117">When editing is complete, or the focus changes, you will receive a [CBEN\_ENDEDIT](cben-endedit.md) notification.</span></span> <span data-ttu-id="34855-118">A mensagem **CBEM \_ HASEDITCHANGED** só é útil para determinar se o texto foi alterado, caso seja enviado antes da notificação de CBEN \_ ENDEDIT.</span><span class="sxs-lookup"><span data-stu-id="34855-118">The **CBEM\_HASEDITCHANGED** message is only useful for determining whether the text has been changed if it is sent before the CBEN\_ENDEDIT notification.</span></span> <span data-ttu-id="34855-119">Se a mensagem for enviada posteriormente, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="34855-119">If the message is sent afterward, it will return **FALSE**.</span></span> <span data-ttu-id="34855-120">Por exemplo, suponha que o usuário comece a editar o texto na caixa de edição, mas altera o foco, gerando uma \_ notificação CBEN ENDEDIT.</span><span class="sxs-lookup"><span data-stu-id="34855-120">For example, suppose the user starts to edit the text in the edit box but changes focus, generating a CBEN\_ENDEDIT notification.</span></span> <span data-ttu-id="34855-121">Se você enviar uma mensagem **CBEM \_ HASEDITCHANGED** , ela retornará **false**, embora o texto tenha sido alterado.</span><span class="sxs-lookup"><span data-stu-id="34855-121">If you then send a **CBEM\_HASEDITCHANGED** message, it will return **FALSE**, even though the text has been changed.</span></span>

<span data-ttu-id="34855-122">O [**estilo \_ simples do CBS**](combo-box-styles.md) não funciona corretamente com **CBEM \_ HASEDITCHANGED**.</span><span class="sxs-lookup"><span data-stu-id="34855-122">The [**CBS\_SIMPLE**](combo-box-styles.md) style does not work correctly with **CBEM\_HASEDITCHANGED**.</span></span>

## <a name="requirements"></a><span data-ttu-id="34855-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34855-123">Requirements</span></span>



| <span data-ttu-id="34855-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="34855-124">Requirement</span></span> | <span data-ttu-id="34855-125">Valor</span><span class="sxs-lookup"><span data-stu-id="34855-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="34855-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="34855-126">Minimum supported client</span></span><br/> | <span data-ttu-id="34855-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="34855-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="34855-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="34855-128">Minimum supported server</span></span><br/> | <span data-ttu-id="34855-129">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="34855-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="34855-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="34855-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="34855-131"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="34855-131"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





