---
title: Mensagem de SB_GETUNICODEFORMAT (commctrl. h)
description: Mensagem de SB_GETUNICODEFORMAT-recupera o sinalizador de formato de caractere Unicode para o controle.
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
ms.openlocfilehash: 857af43911a01ffc58b1a878be6e1875a44c76cb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085894"
---
# <a name="sb_getunicodeformat-message"></a><span data-ttu-id="9008c-104">\_Mensagem de GETUNICODEFORMAT SB</span><span class="sxs-lookup"><span data-stu-id="9008c-104">SB\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="9008c-105">Recupera o sinalizador de formato de caractere Unicode para o controle.</span><span class="sxs-lookup"><span data-stu-id="9008c-105">Retrieves the Unicode character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="9008c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9008c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9008c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9008c-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9008c-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="9008c-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9008c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9008c-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9008c-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="9008c-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9008c-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="9008c-111">Return value</span></span>

<span data-ttu-id="9008c-112">Retorna o sinalizador de formato Unicode para o controle.</span><span class="sxs-lookup"><span data-stu-id="9008c-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="9008c-113">Se esse valor for diferente de zero, o controle estará usando caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="9008c-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="9008c-114">Se esse valor for zero, o controle estará usando caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="9008c-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="remarks"></a><span data-ttu-id="9008c-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="9008c-115">Remarks</span></span>

<span data-ttu-id="9008c-116">Consulte os comentários para [**CCM \_ GETUNICODEFORMAT**](ccm-getunicodeformat.md) para uma discussão sobre esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="9008c-116">See the remarks for [**CCM\_GETUNICODEFORMAT**](ccm-getunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="9008c-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9008c-117">Requirements</span></span>



| <span data-ttu-id="9008c-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9008c-118">Requirement</span></span> | <span data-ttu-id="9008c-119">Valor</span><span class="sxs-lookup"><span data-stu-id="9008c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9008c-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9008c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9008c-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9008c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9008c-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9008c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9008c-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9008c-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9008c-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9008c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9008c-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9008c-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9008c-126">Consulte também</span><span class="sxs-lookup"><span data-stu-id="9008c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9008c-127">**SB \_ SETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="9008c-127">**SB\_SETUNICODEFORMAT**</span></span>](sb-setunicodeformat.md)
</dt> </dl>

 

 





