---
title: Mensagem de HDM_SETUNICODEFORMAT (commctrl. h)
description: HDM_SETUNICODEFORMAT mensagem – define o sinalizador de formato de caractere UNICODE para o controle.
ms.assetid: 18161fe5-c779-4be0-9e7a-1b5948e42b80
keywords:
- Controles de HDM_SETUNICODEFORMAT de mensagens do Windows
topic_type:
- apiref
api_name:
- HDM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d32ffa5f7f90ab266c52c67899dbff3be0d51123
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085954"
---
# <a name="hdm_setunicodeformat-message"></a><span data-ttu-id="7cd4f-104">\_Mensagem HDM SETUNICODEFORMAT</span><span class="sxs-lookup"><span data-stu-id="7cd4f-104">HDM\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="7cd4f-105">Define o sinalizador de formato de caractere UNICODE para o controle.</span><span class="sxs-lookup"><span data-stu-id="7cd4f-105">Sets the UNICODE character format flag for the control.</span></span> <span data-ttu-id="7cd4f-106">Essa mensagem permite que você altere o conjunto de caracteres usado pelo controle em tempo de execução em vez de ter que recriar o controle.</span><span class="sxs-lookup"><span data-stu-id="7cd4f-106">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span> <span data-ttu-id="7cd4f-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetUnicodeFormat do cabeçalho**](/windows/desktop/api/Commctrl/nf-commctrl-header_setunicodeformat) .</span><span class="sxs-lookup"><span data-stu-id="7cd4f-107">You can send this message explicitly or use the [**Header\_SetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-header_setunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7cd4f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7cd4f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cd4f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7cd4f-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7cd4f-110">O conjunto de caracteres que é usado pelo controle.</span><span class="sxs-lookup"><span data-stu-id="7cd4f-110">The character set that is used by the control.</span></span> <span data-ttu-id="7cd4f-111">Se esse valor for diferente de zero, o controle usará caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="7cd4f-111">If this value is nonzero, the control will use Unicode characters.</span></span> <span data-ttu-id="7cd4f-112">Se esse valor for zero, o controle usará caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="7cd4f-112">If this value is zero, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="7cd4f-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7cd4f-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="7cd4f-114">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="7cd4f-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cd4f-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="7cd4f-115">Return value</span></span>

<span data-ttu-id="7cd4f-116">Retorna o sinalizador de formato Unicode anterior para o controle.</span><span class="sxs-lookup"><span data-stu-id="7cd4f-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cd4f-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="7cd4f-117">Remarks</span></span>

<span data-ttu-id="7cd4f-118">Consulte os comentários para [**CCM \_ SETUNICODEFORMAT**](ccm-setunicodeformat.md) para uma discussão sobre esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="7cd4f-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="7cd4f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7cd4f-119">Requirements</span></span>



| <span data-ttu-id="7cd4f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7cd4f-120">Requirement</span></span> | <span data-ttu-id="7cd4f-121">Valor</span><span class="sxs-lookup"><span data-stu-id="7cd4f-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7cd4f-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7cd4f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7cd4f-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7cd4f-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7cd4f-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7cd4f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7cd4f-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7cd4f-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7cd4f-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7cd4f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="7cd4f-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7cd4f-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7cd4f-128">Consulte também</span><span class="sxs-lookup"><span data-stu-id="7cd4f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cd4f-129">**HDM \_ GETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="7cd4f-129">**HDM\_GETUNICODEFORMAT**</span></span>](hdm-getunicodeformat.md)
</dt> </dl>

 

 





