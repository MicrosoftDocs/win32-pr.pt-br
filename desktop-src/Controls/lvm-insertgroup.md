---
title: Mensagem de LVM_INSERTGROUP (commctrl. h)
description: Insere um grupo em um controle de exibição de lista.
ms.assetid: d43e21bc-e212-42dd-af88-48813d40cd50
keywords:
- Controles de LVM_INSERTGROUP de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_INSERTGROUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94dbae780f7de26a5c791477e1a7321794054056
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755833"
---
# <a name="lvm_insertgroup-message"></a><span data-ttu-id="dff6c-104">Mensagem de inserção do LVM \_</span><span class="sxs-lookup"><span data-stu-id="dff6c-104">LVM\_INSERTGROUP message</span></span>

<span data-ttu-id="dff6c-105">Insere um grupo em um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="dff6c-105">Inserts a group into a list-view control.</span></span>

## <a name="parameters"></a><span data-ttu-id="dff6c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dff6c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dff6c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dff6c-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="dff6c-108">Índice em que o grupo deve ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="dff6c-108">Index where the group is to be added.</span></span> <span data-ttu-id="dff6c-109">Se for-1, o grupo será adicionado ao final da lista.</span><span class="sxs-lookup"><span data-stu-id="dff6c-109">If this is -1, the group is added at the end of the list.</span></span></dd> <dt>

<span data-ttu-id="dff6c-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dff6c-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="dff6c-111">Ponteiro para uma estrutura <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroup">**LVGROUP**</a> que contém o grupo a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="dff6c-111">Pointer to a <a href="/windows/win32/api/commctrl/ns-commctrl-lvgroup">**LVGROUP**</a> structure that contains the group to add.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dff6c-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="dff6c-112">Return value</span></span>

<span data-ttu-id="dff6c-113">Retorna o índice do item ao qual o grupo foi adicionado ou-1 se a operação falhou.</span><span class="sxs-lookup"><span data-stu-id="dff6c-113">Returns the index of the item that the group was added to, or -1 if the operation failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="dff6c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="dff6c-114">Remarks</span></span>

<span data-ttu-id="dff6c-115">Para ativar o modo de grupo, chame [**LVM \_ ENABLEGROUPVIEW**](lvm-enablegroupview.md) ou [**ListView \_ ENABLEGROUPVIEW**](/windows/desktop/api/Commctrl/nf-commctrl-listview_enablegroupview).</span><span class="sxs-lookup"><span data-stu-id="dff6c-115">To turn on group mode, call [**LVM\_ENABLEGROUPVIEW**](lvm-enablegroupview.md) or [**ListView\_EnableGroupView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_enablegroupview).</span></span>

<span data-ttu-id="dff6c-116">Um grupo não pode ser inserido em um controle de exibição de lista vazio.</span><span class="sxs-lookup"><span data-stu-id="dff6c-116">A group cannot be inserted into an empty list-view control.</span></span>

<span data-ttu-id="dff6c-117">Certifique-se de definir **iGroupId** no (s) item (ns) ao qual o grupo foi adicionado.</span><span class="sxs-lookup"><span data-stu-id="dff6c-117">Be sure to set the **iGroupId** in the item(s) the group was added to.</span></span> <span data-ttu-id="dff6c-118">Caso contrário, após o processamento de mensagens [**\_ ENABLEGROUPVIEW do LVM**](lvm-enablegroupview.md) com **verdadeiro** , o controle ListView não mostrará nenhum item.</span><span class="sxs-lookup"><span data-stu-id="dff6c-118">Otherwise after [**LVM\_ENABLEGROUPVIEW**](lvm-enablegroupview.md) message processing with **TRUE** the listview control will not show any items.</span></span>

> [!Note]  
> <span data-ttu-id="dff6c-119">Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32 versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="dff6c-119">To use this message, you must provide a manifest specifying Comclt32 version 6.0.</span></span> <span data-ttu-id="dff6c-120">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="dff6c-120">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="dff6c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dff6c-121">Requirements</span></span>



| <span data-ttu-id="dff6c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="dff6c-122">Requirement</span></span> | <span data-ttu-id="dff6c-123">Valor</span><span class="sxs-lookup"><span data-stu-id="dff6c-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dff6c-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dff6c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="dff6c-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dff6c-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="dff6c-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dff6c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="dff6c-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="dff6c-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dff6c-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dff6c-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="dff6c-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dff6c-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





