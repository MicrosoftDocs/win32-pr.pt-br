---
title: Mensagem de EM_SETREADONLY (WinUser. h)
description: Define ou remove o estilo somente leitura (ES \_ ReadOnly) de um controle de edição. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: a10b3f57-0e67-4a0f-89f3-9c8ebd1514f8
keywords:
- Controles de EM_SETREADONLY de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETREADONLY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0b224e11212077703ab62ab6a180875672c879e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085500"
---
# <a name="em_setreadonly-message"></a><span data-ttu-id="13f1e-105">\_Mensagem em SETreadonly</span><span class="sxs-lookup"><span data-stu-id="13f1e-105">EM\_SETREADONLY message</span></span>

<span data-ttu-id="13f1e-106">Define ou remove o estilo somente leitura ([**es \_ ReadOnly**](edit-control-styles.md)) de um controle de edição.</span><span class="sxs-lookup"><span data-stu-id="13f1e-106">Sets or removes the read-only style ([**ES\_READONLY**](edit-control-styles.md)) of an edit control.</span></span> <span data-ttu-id="13f1e-107">Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="13f1e-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="13f1e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="13f1e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13f1e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="13f1e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="13f1e-110">Especifica se é para definir ou remover o estilo [**es \_ ReadOnly**](edit-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="13f1e-110">Specifies whether to set or remove the [**ES\_READONLY**](edit-control-styles.md) style.</span></span> <span data-ttu-id="13f1e-111">Um valor **true** define o estilo **es \_ ReadOnly** ; um valor **false** remove o estilo **es \_ ReadOnly** .</span><span class="sxs-lookup"><span data-stu-id="13f1e-111">A value of **TRUE** sets the **ES\_READONLY** style; a value of **FALSE** removes the **ES\_READONLY** style.</span></span>

</dd> <dt>

<span data-ttu-id="13f1e-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="13f1e-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="13f1e-113">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="13f1e-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13f1e-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="13f1e-114">Return value</span></span>

<span data-ttu-id="13f1e-115">Se a operação for concluída com sucesso, o valor de retorno será diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="13f1e-115">If the operation succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="13f1e-116">Se a operação falhar, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="13f1e-116">If the operation fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="13f1e-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="13f1e-117">Remarks</span></span>

<span data-ttu-id="13f1e-118">Quando um controle de edição tem o estilo [**es \_ ReadOnly**](edit-control-styles.md) , o usuário não pode alterar o texto dentro do controle de edição.</span><span class="sxs-lookup"><span data-stu-id="13f1e-118">When an edit control has the [**ES\_READONLY**](edit-control-styles.md) style, the user cannot change the text within the edit control.</span></span>

<span data-ttu-id="13f1e-119">Para determinar se um controle de edição tem o estilo [**es \_ ReadOnly**](edit-control-styles.md) , use a função [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) com o \_ sinalizador de estilo GWL.</span><span class="sxs-lookup"><span data-stu-id="13f1e-119">To determine whether an edit control has the [**ES\_READONLY**](edit-control-styles.md) style, use the [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga) function with the GWL\_STYLE flag.</span></span>

<span data-ttu-id="13f1e-120">**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="13f1e-120">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="13f1e-121">Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="13f1e-121">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="13f1e-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13f1e-122">Requirements</span></span>



| <span data-ttu-id="13f1e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="13f1e-123">Requirement</span></span> | <span data-ttu-id="13f1e-124">Valor</span><span class="sxs-lookup"><span data-stu-id="13f1e-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13f1e-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="13f1e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="13f1e-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="13f1e-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="13f1e-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="13f1e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="13f1e-128">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="13f1e-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="13f1e-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="13f1e-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="13f1e-130"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="13f1e-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13f1e-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="13f1e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13f1e-132">**GetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="13f1e-132">**GetWindowLong**</span></span>](/windows/desktop/api/winuser/nf-winuser-getwindowlonga)
</dt> </dl>

 

