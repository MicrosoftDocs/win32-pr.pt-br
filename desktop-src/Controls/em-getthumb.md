---
title: Mensagem de EM_GETTHUMB (WinUser. h)
description: Obtém a posição da caixa de rolagem (Thumb) na barra de rolagem vertical de um controle de edição de várias linhas. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: 04bd0102-1652-405b-8c42-50e138abaf75
keywords:
- Controles de EM_GETTHUMB de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETTHUMB
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e6689c530794e11897f1f88a7d5864058d53aa8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086033"
---
# <a name="em_getthumb-message"></a><span data-ttu-id="ce07c-105">\_Mensagem em GETthumb</span><span class="sxs-lookup"><span data-stu-id="ce07c-105">EM\_GETTHUMB message</span></span>

<span data-ttu-id="ce07c-106">Obtém a posição da caixa de rolagem (Thumb) na barra de rolagem vertical de um controle de edição de várias linhas.</span><span class="sxs-lookup"><span data-stu-id="ce07c-106">Gets the position of the scroll box (thumb) in the vertical scroll bar of a multiline edit control.</span></span> <span data-ttu-id="ce07c-107">Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="ce07c-107">You can send this message to either an edit control or a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="ce07c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ce07c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce07c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ce07c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ce07c-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="ce07c-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ce07c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ce07c-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ce07c-112">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="ce07c-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce07c-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ce07c-113">Return value</span></span>

<span data-ttu-id="ce07c-114">O valor de retorno é a posição da caixa de rolagem.</span><span class="sxs-lookup"><span data-stu-id="ce07c-114">The return value is the position of the scroll box.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce07c-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="ce07c-115">Remarks</span></span>

<span data-ttu-id="ce07c-116">**Edição avançada:** Com suporte no Microsoft rich edit 2,0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="ce07c-116">**Rich Edit:** Supported in Microsoft Rich Edit 2.0 and later.</span></span> <span data-ttu-id="ce07c-117">Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).</span><span class="sxs-lookup"><span data-stu-id="ce07c-117">For information about the compatibility of rich edit versions with the various system versions, see [About Rich Edit Controls](about-rich-edit-controls.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ce07c-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce07c-118">Requirements</span></span>



| <span data-ttu-id="ce07c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce07c-119">Requirement</span></span> | <span data-ttu-id="ce07c-120">Valor</span><span class="sxs-lookup"><span data-stu-id="ce07c-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce07c-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ce07c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ce07c-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ce07c-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ce07c-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ce07c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ce07c-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ce07c-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ce07c-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ce07c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce07c-126"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ce07c-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 





