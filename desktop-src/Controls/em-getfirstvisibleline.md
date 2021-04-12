---
title: Mensagem de EM_GETFIRSTVISIBLELINE (WinUser. h)
description: Obtém o índice de base zero da linha visível superior em um controle de edição de várias linhas. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: 022838d2-7948-4c5a-92ca-655822c4f672
keywords:
- Controles de EM_GETFIRSTVISIBLELINE de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETFIRSTVISIBLELINE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bb759be166b69b3cfa488e9e23d61d9e0ec42d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499549"
---
# <a name="em_getfirstvisibleline-message"></a><span data-ttu-id="798ca-105">\_Mensagem em GETFIRSTVISIBLELINE</span><span class="sxs-lookup"><span data-stu-id="798ca-105">EM\_GETFIRSTVISIBLELINE message</span></span>

<span data-ttu-id="798ca-106">Obtém o índice de base zero da linha visível superior em um controle de edição de várias linhas.</span><span class="sxs-lookup"><span data-stu-id="798ca-106">Gets the zero-based index of the uppermost visible line in a multiline edit control.</span></span> <span data-ttu-id="798ca-107">Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="798ca-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="798ca-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="798ca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="798ca-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="798ca-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="798ca-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="798ca-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="798ca-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="798ca-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="798ca-112">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="798ca-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="798ca-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="798ca-113">Return value</span></span>

<span data-ttu-id="798ca-114">O valor de retorno é o índice de base zero da linha visível superior em um controle de edição de várias linhas.</span><span class="sxs-lookup"><span data-stu-id="798ca-114">The return value is the zero-based index of the uppermost visible line in a multiline edit control.</span></span>

<span data-ttu-id="798ca-115">**Controles de edição:** Para controles de edição de linha única, o valor de retorno é o índice de base zero do primeiro caractere visível.</span><span class="sxs-lookup"><span data-stu-id="798ca-115">**Edit controls:** For single-line edit controls, the return value is the zero-based index of the first visible character.</span></span>

<span data-ttu-id="798ca-116">**Controles de edição avançados:** Para controles de edição Rich de linha única, o valor de retorno é zero.</span><span class="sxs-lookup"><span data-stu-id="798ca-116">**Rich edit controls:** For single-line rich edit controls, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="798ca-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="798ca-117">Remarks</span></span>

<span data-ttu-id="798ca-118">O número de linhas e o comprimento das linhas em um controle de edição dependem da largura do controle e da configuração de WordWrap atual.</span><span class="sxs-lookup"><span data-stu-id="798ca-118">The number of lines and the length of the lines in an edit control depend on the width of the control and the current Wordwrap setting.</span></span>

<span data-ttu-id="798ca-119">**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="798ca-119">**Rich Edit:** Supported in Microsoft Rich Edit 1.0 and later.</span></span> <span data-ttu-id="798ca-120">Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="798ca-120">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="798ca-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="798ca-121">Requirements</span></span>



| <span data-ttu-id="798ca-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="798ca-122">Requirement</span></span> | <span data-ttu-id="798ca-123">Valor</span><span class="sxs-lookup"><span data-stu-id="798ca-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="798ca-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="798ca-124">Minimum supported client</span></span><br/> | <span data-ttu-id="798ca-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="798ca-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="798ca-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="798ca-126">Minimum supported server</span></span><br/> | <span data-ttu-id="798ca-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="798ca-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="798ca-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="798ca-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="798ca-129"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="798ca-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 





