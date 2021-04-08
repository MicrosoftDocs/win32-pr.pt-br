---
title: Mensagem de EM_GETPASSWORDCHAR (WinUser. h)
description: Obtém o caractere de senha que um controle de edição exibe quando o usuário digita o texto. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: 874336f6-701b-466a-afa6-0cb3e787ba4c
keywords:
- Controles de EM_GETPASSWORDCHAR de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETPASSWORDCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6285f002554e22c89896711d3d1d355a95c6bb7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824689"
---
# <a name="em_getpasswordchar-message"></a><span data-ttu-id="cf851-105">\_Mensagem em GETpasswordchar</span><span class="sxs-lookup"><span data-stu-id="cf851-105">EM\_GETPASSWORDCHAR message</span></span>

<span data-ttu-id="cf851-106">Obtém o caractere de senha que um controle de edição exibe quando o usuário digita o texto.</span><span class="sxs-lookup"><span data-stu-id="cf851-106">Gets the password character that an edit control displays when the user enters text.</span></span> <span data-ttu-id="cf851-107">Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="cf851-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="cf851-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cf851-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf851-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cf851-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cf851-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="cf851-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="cf851-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cf851-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cf851-112">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="cf851-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf851-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cf851-113">Return value</span></span>

<span data-ttu-id="cf851-114">O valor de retorno especifica o caractere a ser exibido no lugar de quaisquer caracteres digitados pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="cf851-114">The return value specifies the character to be displayed in place of any characters typed by the user.</span></span> <span data-ttu-id="cf851-115">Se o valor de retorno for **nulo**, não haverá nenhum caractere de senha e o controle exibirá os caracteres digitados pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="cf851-115">If the return value is **NULL**, there is no password character, and the control displays the characters typed by the user.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf851-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="cf851-116">Remarks</span></span>

<span data-ttu-id="cf851-117">Se um controle de edição for criado com o estilo de [**\_ senha es**](edit-control-styles.md) , o caractere de senha padrão será definido como um asterisco ( \* ).</span><span class="sxs-lookup"><span data-stu-id="cf851-117">If an edit control is created with the [**ES\_PASSWORD**](edit-control-styles.md) style, the default password character is set to an asterisk (\*).</span></span> <span data-ttu-id="cf851-118">Se um controle de edição for criado sem o estilo de **\_ senha es** , não haverá nenhum caractere de senha.</span><span class="sxs-lookup"><span data-stu-id="cf851-118">If an edit control is created without the **ES\_PASSWORD** style, there is no password character.</span></span> <span data-ttu-id="cf851-119">Para alterar o caractere da senha, envie a mensagem em [**\_ SetPasswordChar**](em-setpasswordchar.md) .</span><span class="sxs-lookup"><span data-stu-id="cf851-119">To change the password character, send the [**EM\_SETPASSWORDCHAR**](em-setpasswordchar.md) message.</span></span>

<span data-ttu-id="cf851-120">**Controles de edição:** Os controles de edição de várias linhas não dão suporte ao estilo de senha ou às mensagens.</span><span class="sxs-lookup"><span data-stu-id="cf851-120">**Edit controls:** Multiline edit controls do not support the password style or messages.</span></span>

<span data-ttu-id="cf851-121">**Edição avançada:** Com suporte no Microsoft rich edit 2,0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="cf851-121">**Rich edit:** Supported in Microsoft Rich Edit 2.0 and later.</span></span> <span data-ttu-id="cf851-122">Os controles de linha única e de edição de várias linhas dão suporte ao estilo e às mensagens da senha.</span><span class="sxs-lookup"><span data-stu-id="cf851-122">Both single-line and multiline edit controls support the password style and messages.</span></span> <span data-ttu-id="cf851-123">Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="cf851-123">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cf851-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf851-124">Requirements</span></span>



| <span data-ttu-id="cf851-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf851-125">Requirement</span></span> | <span data-ttu-id="cf851-126">Valor</span><span class="sxs-lookup"><span data-stu-id="cf851-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf851-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cf851-127">Minimum supported client</span></span><br/> | <span data-ttu-id="cf851-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cf851-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cf851-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cf851-129">Minimum supported server</span></span><br/> | <span data-ttu-id="cf851-130">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cf851-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cf851-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cf851-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf851-132"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cf851-132"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf851-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="cf851-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf851-134">**em \_ SETpasswordchar**</span><span class="sxs-lookup"><span data-stu-id="cf851-134">**EM\_SETPASSWORDCHAR**</span></span>](em-setpasswordchar.md)
</dt> </dl>

 

 





