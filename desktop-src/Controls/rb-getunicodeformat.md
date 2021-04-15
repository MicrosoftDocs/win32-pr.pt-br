---
title: Mensagem de RB_GETUNICODEFORMAT (commctrl. h)
description: Recupera o sinalizador de formato de caractere Unicode para o controle.
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
ms.openlocfilehash: 1a6ef31c409ddc0570b03a3bcd8bb0dd81e9c722
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454692"
---
# <a name="rb_getunicodeformat-message"></a><span data-ttu-id="c2e64-104">\_Mensagem GETUNICODEFORMAT RB</span><span class="sxs-lookup"><span data-stu-id="c2e64-104">RB\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="c2e64-105">Recupera o sinalizador de formato de caractere Unicode para o controle.</span><span class="sxs-lookup"><span data-stu-id="c2e64-105">Retrieves the Unicode character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="c2e64-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c2e64-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2e64-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c2e64-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c2e64-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="c2e64-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="c2e64-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c2e64-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c2e64-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="c2e64-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2e64-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c2e64-111">Return value</span></span>

<span data-ttu-id="c2e64-112">Retorna o sinalizador de formato Unicode para o controle.</span><span class="sxs-lookup"><span data-stu-id="c2e64-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="c2e64-113">Se esse valor for diferente de zero, o controle estará usando caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="c2e64-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="c2e64-114">Se esse valor for zero, o controle estará usando caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="c2e64-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2e64-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="c2e64-115">Remarks</span></span>

<span data-ttu-id="c2e64-116">Consulte os comentários para [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) para uma discussão sobre esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="c2e64-116">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2e64-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2e64-117">Requirements</span></span>



| <span data-ttu-id="c2e64-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2e64-118">Requirement</span></span> | <span data-ttu-id="c2e64-119">Valor</span><span class="sxs-lookup"><span data-stu-id="c2e64-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c2e64-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2e64-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c2e64-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c2e64-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c2e64-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c2e64-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c2e64-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c2e64-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c2e64-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c2e64-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2e64-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2e64-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2e64-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="c2e64-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2e64-127">**\_SETUNICODEFORMAT RB**</span><span class="sxs-lookup"><span data-stu-id="c2e64-127">**RB\_SETUNICODEFORMAT**</span></span>](rb-setunicodeformat.md)
</dt> </dl>

 

 





