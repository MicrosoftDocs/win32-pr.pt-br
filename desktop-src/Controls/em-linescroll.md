---
title: Mensagem de EM_LINESCROLL (WinUser. h)
description: Rola o texto em um controle de edição de várias linhas.
ms.assetid: 5398082d-f1ef-4a3a-9e5a-83cf286adbf1
keywords:
- Controles de EM_LINESCROLL de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_LINESCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 646e225ef269ccddca2cdc29caf635d94c1671e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009563"
---
# <a name="em_linescroll-message"></a><span data-ttu-id="fc882-104">\_Mensagem em LINESCROLL</span><span class="sxs-lookup"><span data-stu-id="fc882-104">EM\_LINESCROLL message</span></span>

<span data-ttu-id="fc882-105">Rola o texto em um controle de edição de várias linhas.</span><span class="sxs-lookup"><span data-stu-id="fc882-105">Scrolls the text in a multiline edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="fc882-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fc882-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc882-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fc882-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fc882-108">**Controles de edição:** O número de caracteres a rolar horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="fc882-108">**Edit controls:** The number of characters to scroll horizontally.</span></span>

<span data-ttu-id="fc882-109">**Controles de edição avançados:** Esse parâmetro não é usado; Ele deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="fc882-109">**Rich edit controls:** This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="fc882-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fc882-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fc882-111">O número de linhas a rolar verticalmente.</span><span class="sxs-lookup"><span data-stu-id="fc882-111">The number of lines to scroll vertically.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc882-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fc882-112">Return value</span></span>

<span data-ttu-id="fc882-113">Se a mensagem for enviada para um controle de edição de várias linhas, o valor de retorno será **true**.</span><span class="sxs-lookup"><span data-stu-id="fc882-113">If the message is sent to a multiline edit control, the return value is **TRUE**.</span></span>

<span data-ttu-id="fc882-114">Se a mensagem for enviada para um controle de edição de linha única, o valor de retorno será **false**.</span><span class="sxs-lookup"><span data-stu-id="fc882-114">If the message is sent to a single-line edit control, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc882-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="fc882-115">Remarks</span></span>

<span data-ttu-id="fc882-116">O controle não rola verticalmente além da última linha de texto no controle de edição.</span><span class="sxs-lookup"><span data-stu-id="fc882-116">The control does not scroll vertically past the last line of text in the edit control.</span></span> <span data-ttu-id="fc882-117">Se a linha atual mais o número de linhas especificado pelo parâmetro *lParam* exceder o número total de linhas no controle de edição, o valor será ajustado de forma que a última linha do controle de edição seja rolada para a parte superior da janela de controle de edição.</span><span class="sxs-lookup"><span data-stu-id="fc882-117">If the current line plus the number of lines specified by the *lParam* parameter exceeds the total number of lines in the edit control, the value is adjusted so that the last line of the edit control is scrolled to the top of the edit-control window.</span></span>

<span data-ttu-id="fc882-118">**Controles de edição:** A mensagem em **\_ LINESCROLL** rola o texto vertical ou horizontalmente em um controle de edição de várias linhas.</span><span class="sxs-lookup"><span data-stu-id="fc882-118">**Edit controls:** The **EM\_LINESCROLL** message scrolls the text vertically or horizontally in a multiline edit control.</span></span> <span data-ttu-id="fc882-119">A mensagem em **\_ LINESCROLL** pode ser usada para rolar horizontalmente além do último caractere de qualquer linha.</span><span class="sxs-lookup"><span data-stu-id="fc882-119">The **EM\_LINESCROLL** message can be used to scroll horizontally past the last character of any line.</span></span>

<span data-ttu-id="fc882-120">**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="fc882-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="fc882-121">A mensagem em **\_ LINESCROLL** rola o texto verticalmente em um controle de edição de várias linhas.</span><span class="sxs-lookup"><span data-stu-id="fc882-121">The **EM\_LINESCROLL** message scrolls the text vertically in a multiline edit control.</span></span> <span data-ttu-id="fc882-122">Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="fc882-122">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fc882-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc882-123">Requirements</span></span>



| <span data-ttu-id="fc882-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc882-124">Requirement</span></span> | <span data-ttu-id="fc882-125">Valor</span><span class="sxs-lookup"><span data-stu-id="fc882-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc882-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fc882-126">Minimum supported client</span></span><br/> | <span data-ttu-id="fc882-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fc882-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fc882-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fc882-128">Minimum supported server</span></span><br/> | <span data-ttu-id="fc882-129">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fc882-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fc882-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fc882-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc882-131"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fc882-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 





