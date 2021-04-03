---
title: Mensagem de CBEM_GETUNICODEFORMAT (commctrl. h)
description: Obtém o sinalizador de formato de caractere UNICODE para o controle.
ms.assetid: 854ff8d5-6e2f-4918-a6c5-91356a4454af
keywords:
- Controles de CBEM_GETUNICODEFORMAT de mensagens do Windows
topic_type:
- apiref
api_name:
- CBEM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b77bb0daabe6ef14d4be1b5e2de6bb1dd63248d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824797"
---
# <a name="cbem_getunicodeformat-message"></a><span data-ttu-id="8dcb4-104">\_Mensagem CBEM GETUNICODEFORMAT</span><span class="sxs-lookup"><span data-stu-id="8dcb4-104">CBEM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="8dcb4-105">Obtém o sinalizador de formato de caractere UNICODE para o controle.</span><span class="sxs-lookup"><span data-stu-id="8dcb4-105">Gets the UNICODE character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="8dcb4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8dcb4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8dcb4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8dcb4-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8dcb4-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="8dcb4-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8dcb4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8dcb4-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="8dcb4-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="8dcb4-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8dcb4-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8dcb4-111">Return value</span></span>

<span data-ttu-id="8dcb4-112">Retorna o sinalizador de formato Unicode para o controle.</span><span class="sxs-lookup"><span data-stu-id="8dcb4-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="8dcb4-113">Se esse valor for diferente de zero, o controle estará usando caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="8dcb4-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="8dcb4-114">Se esse valor for zero, o controle estará usando caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="8dcb4-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="8dcb4-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="8dcb4-115">Remarks</span></span>

<span data-ttu-id="8dcb4-116">Consulte os comentários para [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) para uma discussão sobre esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="8dcb4-116">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="8dcb4-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8dcb4-117">Requirements</span></span>



| <span data-ttu-id="8dcb4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8dcb4-118">Requirement</span></span> | <span data-ttu-id="8dcb4-119">Valor</span><span class="sxs-lookup"><span data-stu-id="8dcb4-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8dcb4-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8dcb4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8dcb4-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8dcb4-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8dcb4-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8dcb4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8dcb4-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8dcb4-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8dcb4-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8dcb4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8dcb4-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8dcb4-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8dcb4-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="8dcb4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8dcb4-127">**CBEM \_ SETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="8dcb4-127">**CBEM\_SETUNICODEFORMAT**</span></span>](cbem-setunicodeformat.md)
</dt> </dl>

 

 





