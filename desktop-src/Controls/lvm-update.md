---
title: Mensagem de LVM_UPDATE (commctrl. h)
description: Atualiza um item de exibição de lista. Se o controle de exibição de lista tiver o \_ estilo de AUTOORGANIZAR LVS, essa macro fará com que o controle de exibição de lista seja organizado. Você pode enviar essa mensagem explicitamente ou usando a macro de \_ atualização de ListView.
ms.assetid: 81b332e9-4bea-481e-a7c5-613371103550
keywords:
- Controles de LVM_UPDATE de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_UPDATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6cf2a4316e3ae3fc4dbab5e1afe780b03829b30
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824194"
---
# <a name="lvm_update-message"></a><span data-ttu-id="c3329-106">Mensagem de atualização do LVM \_</span><span class="sxs-lookup"><span data-stu-id="c3329-106">LVM\_UPDATE message</span></span>

<span data-ttu-id="c3329-107">Atualiza um item de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="c3329-107">Updates a list-view item.</span></span> <span data-ttu-id="c3329-108">Se o controle de exibição de lista tiver o estilo de [**\_ AutoOrganizar LVS**](list-view-window-styles.md) , essa macro fará com que o controle de exibição de lista seja organizado.</span><span class="sxs-lookup"><span data-stu-id="c3329-108">If the list-view control has the [**LVS\_AUTOARRANGE**](list-view-window-styles.md) style, this macro causes the list-view control to be arranged.</span></span> <span data-ttu-id="c3329-109">Você pode enviar essa mensagem explicitamente ou usando a macro [**de \_ atualização de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_update) .</span><span class="sxs-lookup"><span data-stu-id="c3329-109">You can send this message explicitly or by using the [**ListView\_Update**](/windows/desktop/api/Commctrl/nf-commctrl-listview_update) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c3329-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c3329-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3329-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c3329-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c3329-112">Índice do item a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="c3329-112">Index of the item to update.</span></span>

</dd> <dt>

<span data-ttu-id="c3329-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c3329-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c3329-114">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="c3329-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3329-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c3329-115">Return value</span></span>

<span data-ttu-id="c3329-116">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="c3329-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3329-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3329-117">Requirements</span></span>



| <span data-ttu-id="c3329-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3329-118">Requirement</span></span> | <span data-ttu-id="c3329-119">Valor</span><span class="sxs-lookup"><span data-stu-id="c3329-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c3329-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c3329-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c3329-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c3329-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c3329-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c3329-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c3329-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c3329-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c3329-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c3329-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3329-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3329-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





