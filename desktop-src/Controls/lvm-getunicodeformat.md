---
title: Mensagem de LVM_GETUNICODEFORMAT (commctrl. h)
description: Recupera o sinalizador de formato de caractere UNICODE para o controle. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetUnicodeFormat do ListView.
ms.assetid: b0598b60-4d0e-4c68-b63a-e614c6268129
keywords:
- Controles de LVM_GETUNICODEFORMAT de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 720a65baab8ec9c1ec3b311e49fe3672c97a0fba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824666"
---
# <a name="lvm_getunicodeformat-message"></a><span data-ttu-id="006d1-105">\_Mensagem GETUNICODEFORMAT LVM</span><span class="sxs-lookup"><span data-stu-id="006d1-105">LVM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="006d1-106">Recupera o sinalizador de formato de caractere UNICODE para o controle.</span><span class="sxs-lookup"><span data-stu-id="006d1-106">Retrieves the UNICODE character format flag for the control.</span></span> <span data-ttu-id="006d1-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetUnicodeFormat do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getunicodeformat) .</span><span class="sxs-lookup"><span data-stu-id="006d1-107">You can send this message explicitly or use the [**ListView\_GetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="006d1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="006d1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="006d1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="006d1-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="006d1-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="006d1-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="006d1-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="006d1-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="006d1-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="006d1-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="006d1-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="006d1-113">Return value</span></span>

<span data-ttu-id="006d1-114">Retorna o sinalizador de formato Unicode para o controle.</span><span class="sxs-lookup"><span data-stu-id="006d1-114">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="006d1-115">Se esse valor for diferente de zero, o controle estará usando caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="006d1-115">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="006d1-116">Se esse valor for zero, o controle estará usando caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="006d1-116">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="006d1-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="006d1-117">Remarks</span></span>

<span data-ttu-id="006d1-118">Consulte os comentários para [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) para uma discussão sobre esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="006d1-118">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="006d1-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="006d1-119">Requirements</span></span>



| <span data-ttu-id="006d1-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="006d1-120">Requirement</span></span> | <span data-ttu-id="006d1-121">Valor</span><span class="sxs-lookup"><span data-stu-id="006d1-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="006d1-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="006d1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="006d1-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="006d1-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="006d1-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="006d1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="006d1-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="006d1-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="006d1-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="006d1-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="006d1-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="006d1-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="006d1-128">Consulte também</span><span class="sxs-lookup"><span data-stu-id="006d1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="006d1-129">**\_SETUNICODEFORMAT LVM**</span><span class="sxs-lookup"><span data-stu-id="006d1-129">**LVM\_SETUNICODEFORMAT**</span></span>](lvm-setunicodeformat.md)
</dt> </dl>

 

 





