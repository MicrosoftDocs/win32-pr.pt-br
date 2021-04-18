---
title: Mensagem de TCM_GETITEM (commctrl. h)
description: Recupera informações sobre uma guia em um controle guia. Você pode enviar essa mensagem explicitamente ou usando a macro TabCtrl \_ GetItem.
ms.assetid: 41774f14-c4e9-4c98-bc25-3522b2125ed5
keywords:
- Controles de TCM_GETITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- TCM_GETITEM
- TCM_GETITEMA
- TCM_GETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6f94f26a0893416847df052ff47731391a86f5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105749669"
---
# <a name="tcm_getitem-message"></a><span data-ttu-id="7d454-105">\_Mensagem GETITEM de TCM</span><span class="sxs-lookup"><span data-stu-id="7d454-105">TCM\_GETITEM message</span></span>

<span data-ttu-id="7d454-106">Recupera informações sobre uma guia em um controle guia.</span><span class="sxs-lookup"><span data-stu-id="7d454-106">Retrieves information about a tab in a tab control.</span></span> <span data-ttu-id="7d454-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**TabCtrl \_ GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitem) .</span><span class="sxs-lookup"><span data-stu-id="7d454-107">You can send this message explicitly or by using the [**TabCtrl\_GetItem**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7d454-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7d454-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d454-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7d454-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7d454-110">Índice da guia.</span><span class="sxs-lookup"><span data-stu-id="7d454-110">Index of the tab.</span></span>

</dd> <dt>

<span data-ttu-id="7d454-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7d454-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7d454-112">Ponteiro para uma estrutura [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) que especifica as informações para recuperar e receber informações sobre a guia. Quando a mensagem é enviada, o membro de **máscara** especifica quais atributos retornar.</span><span class="sxs-lookup"><span data-stu-id="7d454-112">Pointer to a [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) structure that specifies the information to retrieve and receives information about the tab. When the message is sent, the **mask** member specifies which attributes to return.</span></span> <span data-ttu-id="7d454-113">Se o membro de **máscara** especificar o \_ valor de texto TCIF, o membro **pszText** deverá conter o endereço do buffer que receberá o texto do item e o membro **cchTextMax** deverá especificar o tamanho do buffer.</span><span class="sxs-lookup"><span data-stu-id="7d454-113">If the **mask** member specifies the TCIF\_TEXT value, the **pszText** member must contain the address of the buffer that receives the item text, and the **cchTextMax** member must specify the size of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d454-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7d454-114">Return value</span></span>

<span data-ttu-id="7d454-115">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="7d454-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d454-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="7d454-116">Remarks</span></span>

<span data-ttu-id="7d454-117">Se o \_ sinalizador de texto TCIF for definido no membro **Mask** da estrutura [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) , o controle poderá alterar o membro **pszText** da estrutura para apontar para o novo texto em vez de preencher o buffer com o texto solicitado.</span><span class="sxs-lookup"><span data-stu-id="7d454-117">If the TCIF\_TEXT flag is set in the **mask** member of the [**TCITEM**](/windows/win32/api/commctrl/ns-commctrl-tcitema) structure, the control may change the **pszText** member of the structure to point to the new text instead of filling the buffer with the requested text.</span></span> <span data-ttu-id="7d454-118">O controle pode definir o membro **pszText** como **nulo** para indicar que nenhum texto está associado ao item.</span><span class="sxs-lookup"><span data-stu-id="7d454-118">The control may set the **pszText** member to **NULL** to indicate that no text is associated with the item.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d454-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d454-119">Requirements</span></span>



| <span data-ttu-id="7d454-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d454-120">Requirement</span></span> | <span data-ttu-id="7d454-121">Valor</span><span class="sxs-lookup"><span data-stu-id="7d454-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7d454-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7d454-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7d454-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7d454-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7d454-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7d454-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7d454-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7d454-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7d454-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7d454-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d454-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d454-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="7d454-128">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="7d454-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="7d454-129">**TCM \_ GETITEMW** (Unicode) e **TCM \_ getitema** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="7d454-129">**TCM\_GETITEMW** (Unicode) and **TCM\_GETITEMA** (ANSI)</span></span><br/>                   |



 

 





