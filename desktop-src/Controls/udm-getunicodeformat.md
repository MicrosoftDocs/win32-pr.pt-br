---
title: Mensagem de UDM_GETUNICODEFORMAT (commctrl. h)
description: Recupera o sinalizador de formato de caractere Unicode para o controle.
ms.assetid: 8c09d37b-95a2-49cd-b578-919f9c39fa8b
keywords:
- Controles de UDM_GETUNICODEFORMAT de mensagens do Windows
topic_type:
- apiref
api_name:
- UDM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b2f9eef604af6cf5dfcefbf1e3e03dec561ac21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919193"
---
# <a name="udm_getunicodeformat-message"></a><span data-ttu-id="f60ad-104">\_Mensagem de GETUNICODEFORMAT UDM</span><span class="sxs-lookup"><span data-stu-id="f60ad-104">UDM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="f60ad-105">Recupera o sinalizador de formato de caractere Unicode para o controle.</span><span class="sxs-lookup"><span data-stu-id="f60ad-105">Retrieves the Unicode character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="f60ad-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f60ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f60ad-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f60ad-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f60ad-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="f60ad-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f60ad-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f60ad-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f60ad-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="f60ad-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f60ad-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f60ad-111">Return value</span></span>

<span data-ttu-id="f60ad-112">Retorna o sinalizador de formato Unicode para o controle.</span><span class="sxs-lookup"><span data-stu-id="f60ad-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="f60ad-113">Se esse valor for diferente de zero, o controle estará usando caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="f60ad-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="f60ad-114">Se esse valor for zero, o controle estará usando caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="f60ad-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="f60ad-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="f60ad-115">Remarks</span></span>

<span data-ttu-id="f60ad-116">Consulte os comentários para [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) para uma discussão sobre esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="f60ad-116">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="f60ad-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f60ad-117">Requirements</span></span>



| <span data-ttu-id="f60ad-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f60ad-118">Requirement</span></span> | <span data-ttu-id="f60ad-119">Valor</span><span class="sxs-lookup"><span data-stu-id="f60ad-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f60ad-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f60ad-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f60ad-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f60ad-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f60ad-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f60ad-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f60ad-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f60ad-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f60ad-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f60ad-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f60ad-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f60ad-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f60ad-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="f60ad-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f60ad-127">**\_SETUNICODEFORMAT UDM**</span><span class="sxs-lookup"><span data-stu-id="f60ad-127">**UDM\_SETUNICODEFORMAT**</span></span>](udm-setunicodeformat.md)
</dt> </dl>

 

 





