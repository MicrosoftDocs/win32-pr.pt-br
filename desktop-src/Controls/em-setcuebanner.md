---
title: Mensagem de EM_SETCUEBANNER (commctrl. h)
description: Define a indicação textual ou Tip, que é exibida pelo controle de edição para solicitar informações ao usuário.
ms.assetid: 1b1ff5e7-e0b8-40c1-8b7e-7003e9ef959b
keywords:
- Controles de EM_SETCUEBANNER de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETCUEBANNER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d740bf0a3a055f45c6d104d44349f078d3bf9ad2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455766"
---
# <a name="em_setcuebanner-message"></a><span data-ttu-id="1a72c-104">\_Mensagem em SETCUEBANNER</span><span class="sxs-lookup"><span data-stu-id="1a72c-104">EM\_SETCUEBANNER message</span></span>

<span data-ttu-id="1a72c-105">Define a indicação textual ou Tip, que é exibida pelo controle de edição para solicitar informações ao usuário.</span><span class="sxs-lookup"><span data-stu-id="1a72c-105">Sets the textual cue, or tip, that is displayed by the edit control to prompt the user for information.</span></span>

## <a name="parameters"></a><span data-ttu-id="1a72c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1a72c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a72c-107">*wParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1a72c-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a72c-108">**True** se a faixa de indicação deve ser mostrada mesmo quando o controle de edição tem foco; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="1a72c-108">**TRUE** if the cue banner should show even when the edit control has focus; otherwise, **FALSE**.</span></span> <span data-ttu-id="1a72c-109">**False** é o comportamento padrão que a faixa de indicação desaparece quando o usuário clica no controle.</span><span class="sxs-lookup"><span data-stu-id="1a72c-109">**FALSE** is the default behavior the cue banner disappears when the user clicks in the control.</span></span>

</dd> <dt>

<span data-ttu-id="1a72c-110">*lParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1a72c-110">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a72c-111">Um ponteiro para uma cadeia de caracteres Unicode que contém o texto a ser exibido como a indicação textual.</span><span class="sxs-lookup"><span data-stu-id="1a72c-111">A pointer to a Unicode string that contains the text to display as the textual cue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a72c-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1a72c-112">Return value</span></span>

<span data-ttu-id="1a72c-113">Se a mensagem tiver sucesso, retornará **true**.</span><span class="sxs-lookup"><span data-stu-id="1a72c-113">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="1a72c-114">Caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="1a72c-114">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a72c-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="1a72c-115">Remarks</span></span>

<span data-ttu-id="1a72c-116">Um controle de edição que é usado para iniciar uma pesquisa pode exibir "Insira a pesquisa aqui" em texto cinza como uma indicação textual.</span><span class="sxs-lookup"><span data-stu-id="1a72c-116">An edit control that is used to begin a search may display "Enter search here" in gray text as a textual cue.</span></span> <span data-ttu-id="1a72c-117">Quando o usuário clica no texto, o texto desaparece e o usuário pode digitar.</span><span class="sxs-lookup"><span data-stu-id="1a72c-117">When the user clicks the text, the text goes away and the user can type.</span></span>

<span data-ttu-id="1a72c-118">Não é possível definir uma faixa de indicação em um controle de edição de várias linhas ou em um controle de edição com formatação.</span><span class="sxs-lookup"><span data-stu-id="1a72c-118">You cannot set a cue banner on a multiline edit control or on a rich edit control.</span></span>

> [!Note]  
> <span data-ttu-id="1a72c-119">Para usar essa API, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="1a72c-119">To use this API, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="1a72c-120">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1a72c-120">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="1a72c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a72c-121">Requirements</span></span>



| <span data-ttu-id="1a72c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a72c-122">Requirement</span></span> | <span data-ttu-id="1a72c-123">Valor</span><span class="sxs-lookup"><span data-stu-id="1a72c-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1a72c-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a72c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1a72c-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1a72c-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1a72c-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a72c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1a72c-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1a72c-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1a72c-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1a72c-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a72c-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a72c-129"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a72c-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="1a72c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a72c-131">**Editar \_ SetCueBannerText**</span><span class="sxs-lookup"><span data-stu-id="1a72c-131">**Edit\_SetCueBannerText**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-edit_setcuebannertext)
</dt> </dl>

 

 





