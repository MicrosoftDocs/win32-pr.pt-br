---
title: Mensagem de BCM_GETTEXTMARGIN (commctrl. h)
description: Obtém as margens usadas para desenhar texto em um controle de botão. Você pode enviar essa mensagem explicitamente ou usar o botão \_ GetTextMargin macro.
ms.assetid: 6c141752-e636-41c4-9d05-df8b320ff59f
keywords:
- Controles de BCM_GETTEXTMARGIN de mensagens do Windows
topic_type:
- apiref
api_name:
- BCM_GETTEXTMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6a7d809207c21c74a36c796a9035ed0e3772481
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918350"
---
# <a name="bcm_gettextmargin-message"></a><span data-ttu-id="049e3-105">\_Mensagem GETTEXTMARGIN do BCM</span><span class="sxs-lookup"><span data-stu-id="049e3-105">BCM\_GETTEXTMARGIN message</span></span>

<span data-ttu-id="049e3-106">Obtém as margens usadas para desenhar texto em um controle de botão.</span><span class="sxs-lookup"><span data-stu-id="049e3-106">Gets the margins used to draw text in a button control.</span></span> <span data-ttu-id="049e3-107">Você pode enviar essa mensagem explicitamente ou usar o [**botão \_ GetTextMargin**](/windows/desktop/api/Commctrl/nf-commctrl-button_gettextmargin) macro.</span><span class="sxs-lookup"><span data-stu-id="049e3-107">You can send this message explicitly or use the [**Button\_GetTextMargin**](/windows/desktop/api/Commctrl/nf-commctrl-button_gettextmargin) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="049e3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="049e3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="049e3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="049e3-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="049e3-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="049e3-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="049e3-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="049e3-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="049e3-112">Um ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que contém as margens a serem usadas para desenhar texto.</span><span class="sxs-lookup"><span data-stu-id="049e3-112">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that contains the margins to use for drawing text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="049e3-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="049e3-113">Return value</span></span>

<span data-ttu-id="049e3-114">Se a mensagem tiver sucesso, retornará **true**.</span><span class="sxs-lookup"><span data-stu-id="049e3-114">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="049e3-115">Caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="049e3-115">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="049e3-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="049e3-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="049e3-117">Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="049e3-117">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="049e3-118">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="049e3-118">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="049e3-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="049e3-119">Requirements</span></span>



| <span data-ttu-id="049e3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="049e3-120">Requirement</span></span> | <span data-ttu-id="049e3-121">Valor</span><span class="sxs-lookup"><span data-stu-id="049e3-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="049e3-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="049e3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="049e3-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="049e3-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="049e3-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="049e3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="049e3-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="049e3-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="049e3-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="049e3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="049e3-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="049e3-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

