---
title: Mensagem de LVM_ENABLEGROUPVIEW (commctrl. h)
description: Habilita ou desabilita se os itens em um controle de exibição de lista são exibidos como um grupo.
ms.assetid: 783a5e23-d1cb-4523-a6d2-b2cf93fa7f62
keywords:
- Controles de LVM_ENABLEGROUPVIEW de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_ENABLEGROUPVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1d546e1236fa4f0800c0353810beb5b427ba4fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008872"
---
# <a name="lvm_enablegroupview-message"></a><span data-ttu-id="6d81d-104">\_Mensagem ENABLEGROUPVIEW LVM</span><span class="sxs-lookup"><span data-stu-id="6d81d-104">LVM\_ENABLEGROUPVIEW message</span></span>

<span data-ttu-id="6d81d-105">Habilita ou desabilita se os itens em um controle de exibição de lista são exibidos como um grupo.</span><span class="sxs-lookup"><span data-stu-id="6d81d-105">Enables or disables whether the items in a list-view control display as a group.</span></span>

## <a name="parameters"></a><span data-ttu-id="6d81d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6d81d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d81d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6d81d-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6d81d-108">Um **bool** que indica se um controle de exibição de lista deve ser habilitado para agrupar itens exibidos.</span><span class="sxs-lookup"><span data-stu-id="6d81d-108">A **BOOL** that indicates whether to enable a list-view control to group displayed items.</span></span> <span data-ttu-id="6d81d-109">Use **true** para habilitar o agrupamento, **false** para desabilitá-lo.</span><span class="sxs-lookup"><span data-stu-id="6d81d-109">Use **TRUE** to enable grouping, **FALSE** to disable it.</span></span> </dd> <dt>

<span data-ttu-id="6d81d-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6d81d-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6d81d-111">Deve ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="6d81d-111">Must be **NULL**.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d81d-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6d81d-112">Return value</span></span>

<span data-ttu-id="6d81d-113">Retorna um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="6d81d-113">Returns one of the following values.</span></span>



| <span data-ttu-id="6d81d-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="6d81d-114">Return code</span></span>                                                                       | <span data-ttu-id="6d81d-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="6d81d-115">Description</span></span>                                                                                  |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6d81d-116"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="6d81d-116"><dt>**0**</dt></span></span> </dl>  | <span data-ttu-id="6d81d-117">A capacidade de exibir itens de exibição de lista como um grupo já está habilitada ou desabilitada.</span><span class="sxs-lookup"><span data-stu-id="6d81d-117">The ability to display list-view items as a group is already enabled or disabled.</span></span><br/> |
| <dl> <span data-ttu-id="6d81d-118"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="6d81d-118"><dt>**1**</dt></span></span> </dl>  | <span data-ttu-id="6d81d-119">O estado do controle foi alterado com êxito.</span><span class="sxs-lookup"><span data-stu-id="6d81d-119">The state of the control was successfully changed.</span></span><br/>                                |
| <dl> <span data-ttu-id="6d81d-120"><dt>**-1**</dt></span><span class="sxs-lookup"><span data-stu-id="6d81d-120"><dt>**-1**</dt></span></span> </dl> | <span data-ttu-id="6d81d-121">Falha na operação.</span><span class="sxs-lookup"><span data-stu-id="6d81d-121">The operation failed.</span></span><br/>                                                             |



 

## <a name="remarks"></a><span data-ttu-id="6d81d-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="6d81d-122">Remarks</span></span>

<span data-ttu-id="6d81d-123">**LVM \_** Não há suporte para ENABLEGROUPVIEW no estilo [**LVS \_ OWNERDATA**](list-view-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="6d81d-123">**LVM\_ENABLEGROUPVIEW** is not supported under the [**LVS\_OWNERDATA**](list-view-window-styles.md) style.</span></span>

> [!Note]  
> <span data-ttu-id="6d81d-124">Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="6d81d-124">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="6d81d-125">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6d81d-125">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6d81d-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d81d-126">Requirements</span></span>



| <span data-ttu-id="6d81d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d81d-127">Requirement</span></span> | <span data-ttu-id="6d81d-128">Valor</span><span class="sxs-lookup"><span data-stu-id="6d81d-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6d81d-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d81d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6d81d-130">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6d81d-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6d81d-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d81d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6d81d-132">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6d81d-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6d81d-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6d81d-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d81d-134"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d81d-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





