---
title: Mensagem de HDM_GETUNICODEFORMAT (commctrl. h)
description: Obtém o sinalizador de formato de caractere Unicode para o controle. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetUnicodeFormat do cabeçalho.
ms.assetid: 2b36265a-023c-4083-a755-769461f3804b
keywords:
- Controles de HDM_GETUNICODEFORMAT de mensagens do Windows
topic_type:
- apiref
api_name:
- HDM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce625cc9d4c0ede0c4ce9b54dc852025b22d4870
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085585"
---
# <a name="hdm_getunicodeformat-message"></a><span data-ttu-id="38ad9-105">\_Mensagem HDM GETUNICODEFORMAT</span><span class="sxs-lookup"><span data-stu-id="38ad9-105">HDM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="38ad9-106">Obtém o sinalizador de formato de caractere Unicode para o controle.</span><span class="sxs-lookup"><span data-stu-id="38ad9-106">Gets the Unicode character format flag for the control.</span></span> <span data-ttu-id="38ad9-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetUnicodeFormat do cabeçalho**](/windows/desktop/api/Commctrl/nf-commctrl-header_getunicodeformat) .</span><span class="sxs-lookup"><span data-stu-id="38ad9-107">You can send this message explicitly or use the [**Header\_GetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-header_getunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="38ad9-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="38ad9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38ad9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="38ad9-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="38ad9-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="38ad9-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="38ad9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="38ad9-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="38ad9-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="38ad9-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38ad9-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="38ad9-113">Return value</span></span>

<span data-ttu-id="38ad9-114">Retorna o sinalizador de formato Unicode para o controle.</span><span class="sxs-lookup"><span data-stu-id="38ad9-114">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="38ad9-115">Se esse valor for diferente de zero, o controle estará usando caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="38ad9-115">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="38ad9-116">Se esse valor for zero, o controle estará usando caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="38ad9-116">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="38ad9-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="38ad9-117">Remarks</span></span>

<span data-ttu-id="38ad9-118">Consulte os comentários para [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) para uma discussão sobre esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="38ad9-118">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="38ad9-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38ad9-119">Requirements</span></span>



| <span data-ttu-id="38ad9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="38ad9-120">Requirement</span></span> | <span data-ttu-id="38ad9-121">Valor</span><span class="sxs-lookup"><span data-stu-id="38ad9-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="38ad9-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="38ad9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="38ad9-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="38ad9-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="38ad9-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="38ad9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="38ad9-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="38ad9-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="38ad9-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="38ad9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="38ad9-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="38ad9-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38ad9-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="38ad9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38ad9-129">**HDM \_ SETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="38ad9-129">**HDM\_SETUNICODEFORMAT**</span></span>](hdm-setunicodeformat.md)
</dt> </dl>

 

 





