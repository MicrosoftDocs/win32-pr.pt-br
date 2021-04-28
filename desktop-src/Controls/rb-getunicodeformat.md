---
title: Mensagem de RB_GETUNICODEFORMAT (commctrl. h)
description: Mensagem de RB_GETUNICODEFORMAT-recupera o sinalizador de formato de caractere Unicode para o controle.
ms.assetid: 48a4472b-dda4-41a2-b5bc-6f74b1cdc70b
keywords:
- Controles de RB_GETUNICODEFORMAT de mensagens do Windows
topic_type:
- apiref
api_name:
- RB_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45e1a4546c9c33e87943d305c85939ab280fa122
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085974"
---
# <a name="rb_getunicodeformat-message"></a><span data-ttu-id="2b12e-104">\_Mensagem GETUNICODEFORMAT RB</span><span class="sxs-lookup"><span data-stu-id="2b12e-104">RB\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="2b12e-105">Recupera o sinalizador de formato de caractere Unicode para o controle.</span><span class="sxs-lookup"><span data-stu-id="2b12e-105">Retrieves the Unicode character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="2b12e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2b12e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b12e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2b12e-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="2b12e-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="2b12e-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="2b12e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2b12e-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2b12e-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="2b12e-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b12e-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="2b12e-111">Return value</span></span>

<span data-ttu-id="2b12e-112">Retorna o sinalizador de formato Unicode para o controle.</span><span class="sxs-lookup"><span data-stu-id="2b12e-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="2b12e-113">Se esse valor for diferente de zero, o controle estará usando caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="2b12e-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="2b12e-114">Se esse valor for zero, o controle estará usando caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="2b12e-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b12e-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="2b12e-115">Remarks</span></span>

<span data-ttu-id="2b12e-116">Consulte os comentários para [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) para uma discussão sobre esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="2b12e-116">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b12e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b12e-117">Requirements</span></span>



| <span data-ttu-id="2b12e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b12e-118">Requirement</span></span> | <span data-ttu-id="2b12e-119">Valor</span><span class="sxs-lookup"><span data-stu-id="2b12e-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2b12e-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b12e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2b12e-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2b12e-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2b12e-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b12e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2b12e-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2b12e-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2b12e-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2b12e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b12e-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b12e-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b12e-126">Consulte também</span><span class="sxs-lookup"><span data-stu-id="2b12e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b12e-127">**\_SETUNICODEFORMAT RB**</span><span class="sxs-lookup"><span data-stu-id="2b12e-127">**RB\_SETUNICODEFORMAT**</span></span>](rb-setunicodeformat.md)
</dt> </dl>

 

 





