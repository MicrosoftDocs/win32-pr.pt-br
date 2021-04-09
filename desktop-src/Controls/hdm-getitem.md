---
title: Mensagem de HDM_GETITEM (commctrl. h)
description: Obtém informações sobre um item em um controle de cabeçalho. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetItem do cabeçalho.
ms.assetid: fb1330d3-fd28-490c-9caa-4b2b5ff86ba0
keywords:
- Controles de HDM_GETITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- HDM_GETITEM
- HDM_GETITEMA
- HDM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2073602121480930e0f7d9d2e5a904c0dea77ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085588"
---
# <a name="hdm_getitem-message"></a><span data-ttu-id="14fd9-105">\_Mensagem HDM GETITEM</span><span class="sxs-lookup"><span data-stu-id="14fd9-105">HDM\_GETITEM message</span></span>

<span data-ttu-id="14fd9-106">Obtém informações sobre um item em um controle de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="14fd9-106">Gets information about an item in a header control.</span></span> <span data-ttu-id="14fd9-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetItem do cabeçalho**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitem) .</span><span class="sxs-lookup"><span data-stu-id="14fd9-107">You can send this message explicitly or use the [**Header\_GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="14fd9-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="14fd9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14fd9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="14fd9-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="14fd9-110">O índice do item para o qual as informações serão recuperadas.</span><span class="sxs-lookup"><span data-stu-id="14fd9-110">The index of the item for which information is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="14fd9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="14fd9-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="14fd9-112">Um ponteiro para uma estrutura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) .</span><span class="sxs-lookup"><span data-stu-id="14fd9-112">A pointer to an [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure.</span></span> <span data-ttu-id="14fd9-113">Quando a mensagem é enviada, o membro de **máscara** indica o tipo de informação que está sendo solicitada.</span><span class="sxs-lookup"><span data-stu-id="14fd9-113">When the message is sent, the **mask** member indicates the type of information being requested.</span></span> <span data-ttu-id="14fd9-114">Quando a mensagem retorna, os outros membros recebem as informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="14fd9-114">When the message returns, the other members receive the requested information.</span></span> <span data-ttu-id="14fd9-115">Se o membro de **máscara** especificar zero, a mensagem retornará **true** , mas não copiará nenhuma informação para a estrutura.</span><span class="sxs-lookup"><span data-stu-id="14fd9-115">If the **mask** member specifies zero, the message returns **TRUE** but copies no information to the structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14fd9-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="14fd9-116">Return value</span></span>

<span data-ttu-id="14fd9-117">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="14fd9-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="14fd9-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="14fd9-118">Remarks</span></span>

<span data-ttu-id="14fd9-119">Se o \_ sinalizador de texto HDI for definido no membro **Mask** da estrutura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) , o controle poderá alterar o membro **pszText** da estrutura para apontar para o novo texto em vez de preencher o buffer com o texto solicitado.</span><span class="sxs-lookup"><span data-stu-id="14fd9-119">If the HDI\_TEXT flag is set in the **mask** member of the [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure, the control may change the **pszText** member of the structure to point to the new text instead of filling the buffer with the requested text.</span></span> <span data-ttu-id="14fd9-120">Os aplicativos não devem pressupor que o texto sempre será colocado no buffer solicitado.</span><span class="sxs-lookup"><span data-stu-id="14fd9-120">Applications should not assume that the text will always be placed in the requested buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="14fd9-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14fd9-121">Requirements</span></span>



| <span data-ttu-id="14fd9-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="14fd9-122">Requirement</span></span> | <span data-ttu-id="14fd9-123">Valor</span><span class="sxs-lookup"><span data-stu-id="14fd9-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="14fd9-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="14fd9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="14fd9-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="14fd9-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="14fd9-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="14fd9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="14fd9-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="14fd9-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="14fd9-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="14fd9-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="14fd9-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="14fd9-129"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="14fd9-130">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="14fd9-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="14fd9-131">**HDM \_ GETITEMW** (Unicode) e **HDM \_ getitema** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="14fd9-131">**HDM\_GETITEMW** (Unicode) and **HDM\_GETITEMA** (ANSI)</span></span><br/>                   |



 

 





