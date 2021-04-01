---
title: Mensagem de EM_GETMARGINS (WinUser. h)
description: Obtém as larguras das margens esquerda e direita de um controle de edição.
ms.assetid: 2482354b-aae0-4abd-8287-65c423f30abb
keywords:
- Controles de EM_GETMARGINS de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETMARGINS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 239ad7e7888f5bceef60bf2719c3b67798b56220
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644349"
---
# <a name="em_getmargins-message"></a><span data-ttu-id="5d797-104">\_Mensagem em GETmargins</span><span class="sxs-lookup"><span data-stu-id="5d797-104">EM\_GETMARGINS message</span></span>

<span data-ttu-id="5d797-105">Obtém as larguras das margens esquerda e direita de um controle de edição.</span><span class="sxs-lookup"><span data-stu-id="5d797-105">Gets the widths of the left and right margins for an edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="5d797-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5d797-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d797-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5d797-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5d797-108">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="5d797-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="5d797-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5d797-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5d797-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="5d797-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d797-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5d797-111">Return value</span></span>

<span data-ttu-id="5d797-112">Retorna a largura da margem esquerda no LOWORD e a largura da margem direita no HIWORD.</span><span class="sxs-lookup"><span data-stu-id="5d797-112">Returns the width of the left margin in the LOWORD, and the width of the right margin in the HIWORD.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d797-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="5d797-113">Remarks</span></span>

<span data-ttu-id="5d797-114">**Edição avançada:** Não há suporte para a mensagem em **\_ GetMargins** .</span><span class="sxs-lookup"><span data-stu-id="5d797-114">**Rich Edit:** The **EM\_GETMARGINS** message is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d797-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d797-115">Requirements</span></span>



| <span data-ttu-id="5d797-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d797-116">Requirement</span></span> | <span data-ttu-id="5d797-117">Valor</span><span class="sxs-lookup"><span data-stu-id="5d797-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d797-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d797-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5d797-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5d797-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5d797-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d797-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5d797-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5d797-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5d797-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5d797-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d797-123"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5d797-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d797-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="5d797-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d797-125">**\_SETmargins**</span><span class="sxs-lookup"><span data-stu-id="5d797-125">**EM\_SETMARGINS**</span></span>](em-setmargins.md)
</dt> </dl>

 

 





