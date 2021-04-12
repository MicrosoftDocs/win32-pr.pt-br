---
title: Mensagem de EM_POSFROMCHAR (WinUser. h)
description: Recupera as coordenadas da área do cliente de um caractere especificado em um controle de edição. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: a32532fa-976f-4c19-ac6e-29e5614fc410
keywords:
- Controles de EM_POSFROMCHAR de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_POSFROMCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d98968873ad006b2e91cf3add2429bf7630fae1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499442"
---
# <a name="em_posfromchar-message"></a><span data-ttu-id="33e8d-105">\_Mensagem em POSFROMCHAR</span><span class="sxs-lookup"><span data-stu-id="33e8d-105">EM\_POSFROMCHAR message</span></span>

<span data-ttu-id="33e8d-106">Recupera as coordenadas da área do cliente de um caractere especificado em um controle de edição.</span><span class="sxs-lookup"><span data-stu-id="33e8d-106">Retrieves the client area coordinates of a specified character in an edit control.</span></span> <span data-ttu-id="33e8d-107">Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="33e8d-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="33e8d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="33e8d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33e8d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="33e8d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="33e8d-110">**Edição avançada 1,0 e 3,0:** Um ponteiro para uma estrutura [**pontual**](/previous-versions//dd162807(v=vs.85)) que recebe as coordenadas da área de cliente do caractere.</span><span class="sxs-lookup"><span data-stu-id="33e8d-110">**Rich Edit 1.0 and 3.0:** A pointer to a [**POINTL**](/previous-versions//dd162807(v=vs.85)) structure that receives the client area coordinates of the character.</span></span> <span data-ttu-id="33e8d-111">As coordenadas estão em unidades de tela e são relativas ao canto superior esquerdo da área do cliente do controle.</span><span class="sxs-lookup"><span data-stu-id="33e8d-111">The coordinates are in screen units and are relative to the upper-left corner of the control's client area.</span></span>

<span data-ttu-id="33e8d-112">**Editar controles e edição avançada 2,0:** O índice de base zero do caractere.</span><span class="sxs-lookup"><span data-stu-id="33e8d-112">**Edit controls and Rich Edit 2.0:** The zero-based index of the character.</span></span>

</dd> <dt>

<span data-ttu-id="33e8d-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="33e8d-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="33e8d-114">**Edição avançada 1,0 e 3,0:** O índice de base zero do caractere.</span><span class="sxs-lookup"><span data-stu-id="33e8d-114">**Rich Edit 1.0 and 3.0:** The zero-based index of the character.</span></span>

<span data-ttu-id="33e8d-115">**Editar controles e edição avançada 2,0:** Esse parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="33e8d-115">**Edit controls and Rich Edit 2.0:** This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33e8d-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="33e8d-116">Return value</span></span>

<span data-ttu-id="33e8d-117">**Edição avançada 1,0 e 3,0:** O valor de retorno não é usado.</span><span class="sxs-lookup"><span data-stu-id="33e8d-117">**Rich Edit 1.0 and 3.0:** The return value is not used.</span></span>

<span data-ttu-id="33e8d-118">**Editar controles e edição avançada 2,0:** O valor de retorno contém as coordenadas da área do cliente do caractere.</span><span class="sxs-lookup"><span data-stu-id="33e8d-118">**Edit controls and Rich Edit 2.0:** The return value contains the client area coordinates of the character.</span></span> <span data-ttu-id="33e8d-119">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém a coordenada horizontal e o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contém a coordenada vertical.</span><span class="sxs-lookup"><span data-stu-id="33e8d-119">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the horizontal coordinate and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) contains the vertical coordinate.</span></span>

## <a name="remarks"></a><span data-ttu-id="33e8d-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="33e8d-120">Remarks</span></span>

<span data-ttu-id="33e8d-121">Uma coordenada retornada pode ser um valor negativo se o caractere especificado não for exibido na área do cliente do controle de edição.</span><span class="sxs-lookup"><span data-stu-id="33e8d-121">A returned coordinate can be a negative value if the specified character is not displayed in the edit control's client area.</span></span> <span data-ttu-id="33e8d-122">As coordenadas são truncadas para valores inteiros.</span><span class="sxs-lookup"><span data-stu-id="33e8d-122">The coordinates are truncated to integer values.</span></span>

<span data-ttu-id="33e8d-123">Se o caractere for um delimitador de linha, as coordenadas retornadas indicarão um ponto apenas além do último caractere visível na linha.</span><span class="sxs-lookup"><span data-stu-id="33e8d-123">If the character is a line delimiter, the returned coordinates indicate a point just beyond the last visible character in the line.</span></span> <span data-ttu-id="33e8d-124">Se o índice especificado for maior que o índice do último caractere no controle, o controle retornará-1.</span><span class="sxs-lookup"><span data-stu-id="33e8d-124">If the specified index is greater than the index of the last character in the control, the control returns -1.</span></span>

<span data-ttu-id="33e8d-125">**Edição avançada 3,0 e posterior:** Para compatibilidade com versões anteriores, o Microsoft Rich Edit 3,0 dá suporte à sintaxe usada pelo Microsoft rich edit 2,0.</span><span class="sxs-lookup"><span data-stu-id="33e8d-125">**Rich Edit 3.0 and later:** For backward compatibility, Microsoft Rich Edit 3.0 supports the syntax used by Microsoft Rich Edit 2.0.</span></span> <span data-ttu-id="33e8d-126">Se o Microsoft Rich Edit 3,0 detectar que *wParam* não é um ponteiro [**pointal**](/previous-versions//dd162807(v=vs.85)) válido, ele assumirá que a mensagem foi enviada usando a sintaxe Microsoft rich edit 2,0.</span><span class="sxs-lookup"><span data-stu-id="33e8d-126">If Microsoft Rich Edit 3.0 detects that *wParam* is not a valid [**POINTL**](/previous-versions//dd162807(v=vs.85)) pointer, it assumes the message was sent using the Microsoft Rich Edit 2.0 syntax.</span></span> <span data-ttu-id="33e8d-127">Nesse caso, ele usa o valor de retorno para retornar as coordenadas.</span><span class="sxs-lookup"><span data-stu-id="33e8d-127">In this case, it uses the return value to return the coordinates.</span></span>

<span data-ttu-id="33e8d-128">**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="33e8d-128">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="33e8d-129">Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="33e8d-129">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="33e8d-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33e8d-130">Requirements</span></span>



| <span data-ttu-id="33e8d-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="33e8d-131">Requirement</span></span> | <span data-ttu-id="33e8d-132">Valor</span><span class="sxs-lookup"><span data-stu-id="33e8d-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33e8d-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33e8d-133">Minimum supported client</span></span><br/> | <span data-ttu-id="33e8d-134">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="33e8d-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="33e8d-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33e8d-135">Minimum supported server</span></span><br/> | <span data-ttu-id="33e8d-136">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="33e8d-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="33e8d-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="33e8d-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="33e8d-138"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="33e8d-138"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33e8d-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="33e8d-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="33e8d-140">**Referência**</span><span class="sxs-lookup"><span data-stu-id="33e8d-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="33e8d-141">**em \_ CHARFROMPOS**</span><span class="sxs-lookup"><span data-stu-id="33e8d-141">**EM\_CHARFROMPOS**</span></span>](em-charfrompos.md)
</dt> <dt>

<span data-ttu-id="33e8d-142">**Outros recursos**</span><span class="sxs-lookup"><span data-stu-id="33e8d-142">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="33e8d-143">[**PONTO**](/previous-versions//dd162807(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="33e8d-143">[**POINTL**](/previous-versions//dd162807(v=vs.85))</span></span>
</dt> </dl>

 

