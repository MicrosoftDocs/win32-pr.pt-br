---
title: Mensagem de RB_SETUNICODEFORMAT (commctrl. h)
description: RB_SETUNICODEFORMAT mensagem – define o sinalizador de formato de caractere Unicode para o controle. Essa mensagem permite que você altere o conjunto de caracteres usado pelo controle em tempo de execução em vez de ter que recriar o controle.
ms.assetid: 769b74e0-c1f0-4068-80c4-075f1db2058a
keywords:
- Controles de RB_SETUNICODEFORMAT de mensagens do Windows
topic_type:
- apiref
api_name:
- RB_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce9c168ee298d28d59010491031f7d94ebcaa650
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090964"
---
# <a name="rb_setunicodeformat-message"></a><span data-ttu-id="d2261-105">\_Mensagem SETUNICODEFORMAT RB</span><span class="sxs-lookup"><span data-stu-id="d2261-105">RB\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="d2261-106">Define o sinalizador de formato de caractere Unicode para o controle.</span><span class="sxs-lookup"><span data-stu-id="d2261-106">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="d2261-107">Essa mensagem permite que você altere o conjunto de caracteres usado pelo controle em tempo de execução em vez de ter que recriar o controle.</span><span class="sxs-lookup"><span data-stu-id="d2261-107">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="d2261-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d2261-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2261-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d2261-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d2261-110">Determina o conjunto de caracteres que é usado pelo controle.</span><span class="sxs-lookup"><span data-stu-id="d2261-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="d2261-111">Se esse valor for diferente de zero, o controle usará caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="d2261-111">If this value is nonzero, the control will use Unicode characters.</span></span> <span data-ttu-id="d2261-112">Se esse valor for zero, o controle usará caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="d2261-112">If this value is zero, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="d2261-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d2261-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d2261-114">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="d2261-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2261-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="d2261-115">Return value</span></span>

<span data-ttu-id="d2261-116">Retorna o sinalizador de formato Unicode anterior para o controle.</span><span class="sxs-lookup"><span data-stu-id="d2261-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2261-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="d2261-117">Remarks</span></span>

<span data-ttu-id="d2261-118">Consulte os comentários para [**CCM \_ SETUNICODEFORMAT**](ccm-setunicodeformat.md) para uma discussão sobre esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="d2261-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2261-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2261-119">Requirements</span></span>



| <span data-ttu-id="d2261-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2261-120">Requirement</span></span> | <span data-ttu-id="d2261-121">Valor</span><span class="sxs-lookup"><span data-stu-id="d2261-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d2261-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2261-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d2261-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d2261-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d2261-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d2261-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d2261-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d2261-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d2261-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d2261-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2261-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2261-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2261-128">Consulte também</span><span class="sxs-lookup"><span data-stu-id="d2261-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2261-129">**\_GETUNICODEFORMAT RB**</span><span class="sxs-lookup"><span data-stu-id="d2261-129">**RB\_GETUNICODEFORMAT**</span></span>](rb-getunicodeformat.md)
</dt> </dl>

 

 





