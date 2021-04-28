---
title: Mensagem de UDM_SETUNICODEFORMAT (commctrl. h)
description: UDM_SETUNICODEFORMAT mensagem – define o sinalizador de formato de caractere Unicode para o controle. Essa mensagem permite que você altere o conjunto de caracteres usado pelo controle em tempo de execução em vez de ter que recriar o controle.
ms.assetid: abe882db-bf32-40b0-a1c0-3e89cdc93fe7
keywords:
- Controles de UDM_SETUNICODEFORMAT de mensagens do Windows
topic_type:
- apiref
api_name:
- UDM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09eeb63d5c06a5e64c354c950cd84fc451568d36
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116534"
---
# <a name="udm_setunicodeformat-message"></a><span data-ttu-id="c7b27-105">\_Mensagem de SETUNICODEFORMAT UDM</span><span class="sxs-lookup"><span data-stu-id="c7b27-105">UDM\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="c7b27-106">Define o sinalizador de formato de caractere Unicode para o controle.</span><span class="sxs-lookup"><span data-stu-id="c7b27-106">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="c7b27-107">Essa mensagem permite que você altere o conjunto de caracteres usado pelo controle em tempo de execução em vez de ter que recriar o controle.</span><span class="sxs-lookup"><span data-stu-id="c7b27-107">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="c7b27-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c7b27-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7b27-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c7b27-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c7b27-110">Determina o conjunto de caracteres que é usado pelo controle.</span><span class="sxs-lookup"><span data-stu-id="c7b27-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="c7b27-111">Se esse valor for **true**, o controle usará caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="c7b27-111">If this value is **TRUE**, the control will use Unicode characters.</span></span> <span data-ttu-id="c7b27-112">Se esse valor for **false**, o controle usará caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="c7b27-112">If this value is **FALSE**, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="c7b27-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c7b27-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c7b27-114">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="c7b27-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7b27-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="c7b27-115">Return value</span></span>

<span data-ttu-id="c7b27-116">Retorna o sinalizador de formato Unicode anterior para o controle.</span><span class="sxs-lookup"><span data-stu-id="c7b27-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7b27-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="c7b27-117">Remarks</span></span>

<span data-ttu-id="c7b27-118">Consulte os comentários para [**CCM \_ SETUNICODEFORMAT**](ccm-setunicodeformat.md) para uma discussão sobre esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="c7b27-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7b27-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7b27-119">Requirements</span></span>



| <span data-ttu-id="c7b27-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7b27-120">Requirement</span></span> | <span data-ttu-id="c7b27-121">Valor</span><span class="sxs-lookup"><span data-stu-id="c7b27-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c7b27-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7b27-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c7b27-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c7b27-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c7b27-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7b27-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c7b27-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c7b27-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c7b27-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c7b27-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7b27-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7b27-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7b27-128">Consulte também</span><span class="sxs-lookup"><span data-stu-id="c7b27-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7b27-129">**\_GETUNICODEFORMAT UDM**</span><span class="sxs-lookup"><span data-stu-id="c7b27-129">**UDM\_GETUNICODEFORMAT**</span></span>](udm-getunicodeformat.md)
</dt> </dl>

 

 





