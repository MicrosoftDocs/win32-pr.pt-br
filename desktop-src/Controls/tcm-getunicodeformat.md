---
title: Mensagem de TCM_GETUNICODEFORMAT (commctrl. h)
description: Recupera o sinalizador de formato de caractere Unicode para o controle. Você pode enviar essa mensagem explicitamente ou usar a \_ macro TabCtrl GetUnicodeFormat.
ms.assetid: 720e0325-500b-436c-8713-38ed780735bf
keywords:
- Controles de TCM_GETUNICODEFORMAT de mensagens do Windows
topic_type:
- apiref
api_name:
- TCM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b497f1b2c2b5ac55ee949b498602b50b267fef3b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824709"
---
# <a name="tcm_getunicodeformat-message"></a><span data-ttu-id="5e65f-105">\_Mensagem GETUNICODEFORMAT de TCM</span><span class="sxs-lookup"><span data-stu-id="5e65f-105">TCM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="5e65f-106">Recupera o sinalizador de formato de caractere Unicode para o controle.</span><span class="sxs-lookup"><span data-stu-id="5e65f-106">Retrieves the Unicode character format flag for the control.</span></span> <span data-ttu-id="5e65f-107">Você pode enviar essa mensagem explicitamente ou usar a macro [**TabCtrl \_ GetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getunicodeformat) .</span><span class="sxs-lookup"><span data-stu-id="5e65f-107">You can send this message explicitly or use the [**TabCtrl\_GetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5e65f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5e65f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e65f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5e65f-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5e65f-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="5e65f-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="5e65f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5e65f-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="5e65f-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="5e65f-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e65f-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5e65f-113">Return value</span></span>

<span data-ttu-id="5e65f-114">Retorna o sinalizador de formato Unicode para o controle.</span><span class="sxs-lookup"><span data-stu-id="5e65f-114">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="5e65f-115">Se esse valor for diferente de zero, o controle estará usando caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="5e65f-115">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="5e65f-116">Se esse valor for zero, o controle estará usando caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="5e65f-116">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e65f-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="5e65f-117">Remarks</span></span>

<span data-ttu-id="5e65f-118">Consulte os comentários para [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) para uma discussão sobre esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="5e65f-118">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e65f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e65f-119">Requirements</span></span>



| <span data-ttu-id="5e65f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e65f-120">Requirement</span></span> | <span data-ttu-id="5e65f-121">Valor</span><span class="sxs-lookup"><span data-stu-id="5e65f-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5e65f-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e65f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5e65f-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5e65f-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5e65f-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5e65f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5e65f-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5e65f-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5e65f-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5e65f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e65f-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e65f-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e65f-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="5e65f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e65f-129">**\_SETUNICODEFORMAT TCM**</span><span class="sxs-lookup"><span data-stu-id="5e65f-129">**TCM\_SETUNICODEFORMAT**</span></span>](tcm-setunicodeformat.md)
</dt> </dl>

 

 





