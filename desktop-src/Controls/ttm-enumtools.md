---
title: Mensagem de TTM_ENUMTOOLS (commctrl. h)
description: Recupera as informações que um controle ToolTip mantém sobre a ferramenta atual \ 8212; ou seja, a ferramenta para a qual ToolTip está atualmente exibindo texto.
ms.assetid: c470db71-c24c-45f4-b497-e59811017eee
keywords:
- Controles de TTM_ENUMTOOLS de mensagens do Windows
topic_type:
- apiref
api_name:
- TTM_ENUMTOOLS
- TTM_ENUMTOOLSA
- TTM_ENUMTOOLSW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad1679f9740539507a57c4cba93319569add0af3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455171"
---
# <a name="ttm_enumtools-message"></a><span data-ttu-id="dff34-104">\_Mensagem TTM ENUMTOOLS</span><span class="sxs-lookup"><span data-stu-id="dff34-104">TTM\_ENUMTOOLS message</span></span>

<span data-ttu-id="dff34-105">Recupera as informações que um controle ToolTip mantém sobre a ferramenta atual, que é a ferramenta para a qual a dica de ferramentas está exibindo texto no momento.</span><span class="sxs-lookup"><span data-stu-id="dff34-105">Retrieves the information that a tooltip control maintains about the current tool that is, the tool for which the tooltip is currently displaying text.</span></span>

## <a name="parameters"></a><span data-ttu-id="dff34-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dff34-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dff34-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dff34-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dff34-108">Índice de base zero da ferramenta para a qual recuperar informações.</span><span class="sxs-lookup"><span data-stu-id="dff34-108">Zero-based index of the tool for which to retrieve information.</span></span>

</dd> <dt>

<span data-ttu-id="dff34-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dff34-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dff34-110">Ponteiro para uma estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) que recebe informações sobre a ferramenta.</span><span class="sxs-lookup"><span data-stu-id="dff34-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure that receives information about the tool.</span></span> <span data-ttu-id="dff34-111">Defina o membro **cbSize** dessa estrutura como sizeof (TOOLINFO) antes de enviar esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="dff34-111">Set the **cbSize** member of this structure to sizeof(TOOLINFO) before sending this message.</span></span> <span data-ttu-id="dff34-112">Aloque um buffer.</span><span class="sxs-lookup"><span data-stu-id="dff34-112">Allocate a buffer.</span></span> <span data-ttu-id="dff34-113">Defina o membro **lpszText** para apontar para o buffer para receber o texto da ferramenta.</span><span class="sxs-lookup"><span data-stu-id="dff34-113">Set the **lpszText** member to point to the buffer to receive the tool text.</span></span> <span data-ttu-id="dff34-114">Não é possível determinar o tamanho do buffer necessário.</span><span class="sxs-lookup"><span data-stu-id="dff34-114">There is no way to determine the required buffer size.</span></span> <span data-ttu-id="dff34-115">No entanto, o texto da ferramenta, como retornado no membro **lpszText** da estrutura **TOOLINFO** , tem um comprimento máximo de 80 **TCHARs**, incluindo o **nulo** de terminação.</span><span class="sxs-lookup"><span data-stu-id="dff34-115">However, tool text, as returned at the **lpszText** member of the **TOOLINFO** structure, has a maximum length of 80 **TCHARs**, including the terminating **NULL**.</span></span> <span data-ttu-id="dff34-116">Se o texto exceder esse comprimento, ele será truncado.</span><span class="sxs-lookup"><span data-stu-id="dff34-116">If the text exceeds this length, it is truncated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dff34-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dff34-117">Return value</span></span>

<span data-ttu-id="dff34-118">Retornará **true** se qualquer ferramenta for enumerada ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="dff34-118">Returns **TRUE** if any tools are enumerated, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="dff34-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="dff34-119">Remarks</span></span>

<span data-ttu-id="dff34-120">**Aviso de segurança:** O uso dessa mensagem pode comprometer a segurança do seu programa.</span><span class="sxs-lookup"><span data-stu-id="dff34-120">**Security Warning:** Using this message might compromise the security of your program.</span></span> <span data-ttu-id="dff34-121">Essa mensagem não fornece uma maneira para o destinatário da mensagem saber o tamanho do buffer ou para especificar o tamanho do buffer.</span><span class="sxs-lookup"><span data-stu-id="dff34-121">This message does not provide a way for the message receiver to know the size of the buffer or to specify the size of the buffer.</span></span> <span data-ttu-id="dff34-122">Você deve examinar as [considerações de segurança: controles do Microsoft Windows](sec-comctls.md) antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="dff34-122">You should review the [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>

## <a name="requirements"></a><span data-ttu-id="dff34-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dff34-123">Requirements</span></span>



| <span data-ttu-id="dff34-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="dff34-124">Requirement</span></span> | <span data-ttu-id="dff34-125">Valor</span><span class="sxs-lookup"><span data-stu-id="dff34-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dff34-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dff34-126">Minimum supported client</span></span><br/> | <span data-ttu-id="dff34-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dff34-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dff34-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dff34-128">Minimum supported server</span></span><br/> | <span data-ttu-id="dff34-129">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="dff34-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dff34-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dff34-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="dff34-131"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dff34-131"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="dff34-132">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="dff34-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="dff34-133">**TTM \_ ENUMTOOLSW** (Unicode) e **TTM \_ ENUMTOOLSA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="dff34-133">**TTM\_ENUMTOOLSW** (Unicode) and **TTM\_ENUMTOOLSA** (ANSI)</span></span><br/>               |



 

 





