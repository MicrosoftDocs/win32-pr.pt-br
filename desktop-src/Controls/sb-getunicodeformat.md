---
title: Mensagem de SB_GETUNICODEFORMAT (commctrl. h)
description: Recupera o sinalizador de formato de caractere Unicode para o controle.
ms.assetid: 0b2b543a-b1ef-452c-9b34-c5fbbac4aaa9
keywords:
- Controles de SB_GETUNICODEFORMAT de mensagens do Windows
topic_type:
- apiref
api_name:
- SB_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9dbb639a04f0a40d9d5e11b938aaadbcc8b4c730
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499596"
---
# <a name="sb_getunicodeformat-message"></a><span data-ttu-id="228d0-104">\_Mensagem de GETUNICODEFORMAT SB</span><span class="sxs-lookup"><span data-stu-id="228d0-104">SB\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="228d0-105">Recupera o sinalizador de formato de caractere Unicode para o controle.</span><span class="sxs-lookup"><span data-stu-id="228d0-105">Retrieves the Unicode character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="228d0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="228d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="228d0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="228d0-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="228d0-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="228d0-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="228d0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="228d0-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="228d0-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="228d0-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="228d0-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="228d0-111">Return value</span></span>

<span data-ttu-id="228d0-112">Retorna o sinalizador de formato Unicode para o controle.</span><span class="sxs-lookup"><span data-stu-id="228d0-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="228d0-113">Se esse valor for diferente de zero, o controle estará usando caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="228d0-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="228d0-114">Se esse valor for zero, o controle estará usando caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="228d0-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="228d0-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="228d0-115">Remarks</span></span>

<span data-ttu-id="228d0-116">Consulte os comentários para [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) para uma discussão sobre esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="228d0-116">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="228d0-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="228d0-117">Requirements</span></span>



| <span data-ttu-id="228d0-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="228d0-118">Requirement</span></span> | <span data-ttu-id="228d0-119">Valor</span><span class="sxs-lookup"><span data-stu-id="228d0-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="228d0-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="228d0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="228d0-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="228d0-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="228d0-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="228d0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="228d0-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="228d0-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="228d0-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="228d0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="228d0-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="228d0-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="228d0-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="228d0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="228d0-127">**SB \_ SETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="228d0-127">**SB\_SETUNICODEFORMAT**</span></span>](sb-setunicodeformat.md)
</dt> </dl>

 

 





