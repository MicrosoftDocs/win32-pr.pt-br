---
title: Mensagem de EM_GETCUEBANNER (commctrl. h)
description: Obtém o texto que é exibido como a indicação textual, ou Tip, em um controle de edição.
ms.assetid: 311b783a-cd78-440f-bfc2-f5108ae7d1f8
keywords:
- Controles de EM_GETCUEBANNER de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETCUEBANNER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d28d4aeea5a206c74f2e6b41cee27b5073448ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919128"
---
# <a name="em_getcuebanner-message"></a><span data-ttu-id="6ca77-104">\_Mensagem em GETCUEBANNER</span><span class="sxs-lookup"><span data-stu-id="6ca77-104">EM\_GETCUEBANNER message</span></span>

<span data-ttu-id="6ca77-105">Obtém o texto que é exibido como a indicação textual, ou Tip, em um controle de edição.</span><span class="sxs-lookup"><span data-stu-id="6ca77-105">Gets the text that is displayed as the textual cue, or tip, in an edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="6ca77-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6ca77-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ca77-107">*wParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6ca77-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ca77-108">Um ponteiro para um buffer Unicode que recebe o texto definido como a indicação textual.</span><span class="sxs-lookup"><span data-stu-id="6ca77-108">A pointer to a Unicode buffer that receives the text set as the textual cue.</span></span> <span data-ttu-id="6ca77-109">O chamador é responsável por alocar o buffer.</span><span class="sxs-lookup"><span data-stu-id="6ca77-109">The caller is responsible for allocating the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="6ca77-110">*lParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6ca77-110">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ca77-111">O tamanho do buffer apontado por *wParam* em **WCHAR**, incluindo o **nulo** de terminação.</span><span class="sxs-lookup"><span data-stu-id="6ca77-111">The size of the buffer pointed to by *wParam* in **WCHARs**, including the terminating **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ca77-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6ca77-112">Return value</span></span>

<span data-ttu-id="6ca77-113">Retornará **true** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="6ca77-113">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ca77-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="6ca77-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6ca77-115">Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="6ca77-115">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="6ca77-116">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6ca77-116">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6ca77-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ca77-117">Requirements</span></span>



| <span data-ttu-id="6ca77-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ca77-118">Requirement</span></span> | <span data-ttu-id="6ca77-119">Valor</span><span class="sxs-lookup"><span data-stu-id="6ca77-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6ca77-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ca77-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6ca77-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6ca77-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6ca77-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ca77-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6ca77-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6ca77-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6ca77-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6ca77-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ca77-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ca77-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ca77-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="6ca77-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ca77-127">**Editar \_ GetCueBannerText**</span><span class="sxs-lookup"><span data-stu-id="6ca77-127">**Edit\_GetCueBannerText**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_getcuebannertext)
</dt> </dl>

 

 





