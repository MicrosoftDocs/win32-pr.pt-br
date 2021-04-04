---
title: Mensagem de LVM_ARRANGE (commctrl. h)
description: Organiza os itens na exibição de ícones. Você pode enviar essa mensagem explicitamente ou usando a macro de \_ organização de ListView.
ms.assetid: f7dbcdd2-3cc9-4bae-827e-8bac3b49486c
keywords:
- Controles de LVM_ARRANGE de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_ARRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a1b6a081cf963a649329951358ea4c972f200f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085178"
---
# <a name="lvm_arrange-message"></a><span data-ttu-id="0844a-105">Mensagem de organização do LVM \_</span><span class="sxs-lookup"><span data-stu-id="0844a-105">LVM\_ARRANGE message</span></span>

<span data-ttu-id="0844a-106">Organiza os itens na exibição de ícones.</span><span class="sxs-lookup"><span data-stu-id="0844a-106">Arranges items in icon view.</span></span> <span data-ttu-id="0844a-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**de \_ organização de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_arrange) .</span><span class="sxs-lookup"><span data-stu-id="0844a-107">You can send this message explicitly or by using the [**ListView\_Arrange**](/windows/desktop/api/Commctrl/nf-commctrl-listview_arrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0844a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0844a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0844a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0844a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0844a-110">Um dos seguintes valores que especifica o alinhamento:</span><span class="sxs-lookup"><span data-stu-id="0844a-110">One of the following values that specifies alignment:</span></span>



| <span data-ttu-id="0844a-111">Valor</span><span class="sxs-lookup"><span data-stu-id="0844a-111">Value</span></span>                                                                                                                                                            | <span data-ttu-id="0844a-112">Significado</span><span class="sxs-lookup"><span data-stu-id="0844a-112">Meaning</span></span>                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| <span id="LVA_ALIGNLEFT"></span><span id="lva_alignleft"></span><dl> <span data-ttu-id="0844a-113"><dt>**LVA \_ ALIGNLEFT**</dt></span><span class="sxs-lookup"><span data-stu-id="0844a-113"><dt>**LVA\_ALIGNLEFT**</dt></span></span> </dl>    | <span data-ttu-id="0844a-114">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="0844a-114">Not implemented.</span></span> <span data-ttu-id="0844a-115">Em vez disso, aplique o estilo [**LVS \_ ALIGNLEFT**](list-view-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="0844a-115">Apply the [**LVS\_ALIGNLEFT**](list-view-window-styles.md) style instead.</span></span><br/> |
| <span id="LVA_ALIGNTOP"></span><span id="lva_aligntop"></span><dl> <span data-ttu-id="0844a-116"><dt>**LVA \_ ALIGNTOP**</dt></span><span class="sxs-lookup"><span data-stu-id="0844a-116"><dt>**LVA\_ALIGNTOP**</dt></span></span> </dl>       | <span data-ttu-id="0844a-117">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="0844a-117">Not implemented.</span></span> <span data-ttu-id="0844a-118">Em vez disso, aplique o estilo [**LVS \_ ALIGNTOP**](list-view-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="0844a-118">Apply the [**LVS\_ALIGNTOP**](list-view-window-styles.md) style instead.</span></span><br/>   |
| <span id="LVA_DEFAULT"></span><span id="lva_default"></span><dl> <span data-ttu-id="0844a-119"><dt>**LVA \_ padrão**</dt></span><span class="sxs-lookup"><span data-stu-id="0844a-119"><dt>**LVA\_DEFAULT**</dt></span></span> </dl>          | <span data-ttu-id="0844a-120">Alinha os itens de acordo com os estilos de alinhamento atuais do controle de exibição de lista (o valor padrão).</span><span class="sxs-lookup"><span data-stu-id="0844a-120">Aligns items according to the list-view control's current alignment styles (the default value).</span></span><br/>           |
| <span id="LVA_SNAPTOGRID"></span><span id="lva_snaptogrid"></span><dl> <span data-ttu-id="0844a-121"><dt>**LVA \_ SNAPTOGRID**</dt></span><span class="sxs-lookup"><span data-stu-id="0844a-121"><dt>**LVA\_SNAPTOGRID**</dt></span></span> </dl> | <span data-ttu-id="0844a-122">Ajusta todos os ícones para a posição da grade mais próxima.</span><span class="sxs-lookup"><span data-stu-id="0844a-122">Snaps all icons to the nearest grid position.</span></span><br/>                                                             |



 

</dd> <dt>

<span data-ttu-id="0844a-123">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0844a-123">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0844a-124">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="0844a-124">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0844a-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0844a-125">Return value</span></span>

<span data-ttu-id="0844a-126">Retornará **true** se for bem-sucedido; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="0844a-126">Returns **TRUE** if successful; otherwise, **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0844a-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0844a-127">Requirements</span></span>



| <span data-ttu-id="0844a-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="0844a-128">Requirement</span></span> | <span data-ttu-id="0844a-129">Valor</span><span class="sxs-lookup"><span data-stu-id="0844a-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0844a-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0844a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="0844a-131">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0844a-131">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0844a-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0844a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="0844a-133">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0844a-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0844a-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0844a-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="0844a-135"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0844a-135"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





