---
title: Mensagem de TCM_SETUNICODEFORMAT (commctrl. h)
description: TCM_SETUNICODEFORMAT mensagem – define o sinalizador de formato de caractere Unicode para o controle.
ms.assetid: 4a9bacfc-d1b7-432a-9b61-b0fe18576679
keywords:
- Controles de TCM_SETUNICODEFORMAT de mensagens do Windows
topic_type:
- apiref
api_name:
- TCM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2b84f944be9bd20897d25e4b111f55ced558a43
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085844"
---
# <a name="tcm_setunicodeformat-message"></a><span data-ttu-id="2ed8d-104">\_Mensagem SETUNICODEFORMAT de TCM</span><span class="sxs-lookup"><span data-stu-id="2ed8d-104">TCM\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="2ed8d-105">Define o sinalizador de formato de caractere Unicode para o controle.</span><span class="sxs-lookup"><span data-stu-id="2ed8d-105">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="2ed8d-106">Essa mensagem permite que você altere o conjunto de caracteres usado pelo controle em tempo de execução em vez de ter que recriar o controle.</span><span class="sxs-lookup"><span data-stu-id="2ed8d-106">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span> <span data-ttu-id="2ed8d-107">Você pode enviar essa mensagem explicitamente ou usar a macro [**TabCtrl \_ SetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setunicodeformat) .</span><span class="sxs-lookup"><span data-stu-id="2ed8d-107">You can send this message explicitly or use the [**TabCtrl\_SetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2ed8d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2ed8d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ed8d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2ed8d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2ed8d-110">Determina o conjunto de caracteres que é usado pelo controle.</span><span class="sxs-lookup"><span data-stu-id="2ed8d-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="2ed8d-111">Se esse valor for diferente de zero, o controle usará caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="2ed8d-111">If this value is nonzero, the control will use Unicode characters.</span></span> <span data-ttu-id="2ed8d-112">Se esse valor for zero, o controle usará caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="2ed8d-112">If this value is zero, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="2ed8d-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2ed8d-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2ed8d-114">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="2ed8d-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ed8d-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="2ed8d-115">Return value</span></span>

<span data-ttu-id="2ed8d-116">Retorna o sinalizador de formato Unicode anterior para o controle.</span><span class="sxs-lookup"><span data-stu-id="2ed8d-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ed8d-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="2ed8d-117">Remarks</span></span>

<span data-ttu-id="2ed8d-118">Consulte os comentários para [**CCM \_ SETUNICODEFORMAT**](ccm-setunicodeformat.md) para uma discussão sobre esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="2ed8d-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ed8d-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ed8d-119">Requirements</span></span>



| <span data-ttu-id="2ed8d-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ed8d-120">Requirement</span></span> | <span data-ttu-id="2ed8d-121">Valor</span><span class="sxs-lookup"><span data-stu-id="2ed8d-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2ed8d-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2ed8d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2ed8d-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2ed8d-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2ed8d-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2ed8d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2ed8d-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2ed8d-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2ed8d-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2ed8d-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ed8d-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ed8d-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ed8d-128">Consulte também</span><span class="sxs-lookup"><span data-stu-id="2ed8d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ed8d-129">**\_GETUNICODEFORMAT TCM**</span><span class="sxs-lookup"><span data-stu-id="2ed8d-129">**TCM\_GETUNICODEFORMAT**</span></span>](tcm-getunicodeformat.md)
</dt> </dl>

 

 





