---
title: Mensagem de LVM_GETSELECTEDCOUNT (commctrl. h)
description: Determina o número de itens selecionados em um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetSelectedCount do ListView.
ms.assetid: 38916227-e6ca-4efa-9821-13f0fdb29834
keywords:
- Controles de LVM_GETSELECTEDCOUNT de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETSELECTEDCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b23f0e8d1d87e2cc7dd60d32ac3dd4943611a36f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824668"
---
# <a name="lvm_getselectedcount-message"></a><span data-ttu-id="27649-105">\_Mensagem GETSELECTEDCOUNT LVM</span><span class="sxs-lookup"><span data-stu-id="27649-105">LVM\_GETSELECTEDCOUNT message</span></span>

<span data-ttu-id="27649-106">Determina o número de itens selecionados em um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="27649-106">Determines the number of selected items in a list-view control.</span></span> <span data-ttu-id="27649-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetSelectedCount do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getselectedcount) .</span><span class="sxs-lookup"><span data-stu-id="27649-107">You can send this message explicitly or by using the [**ListView\_GetSelectedCount**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getselectedcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="27649-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="27649-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27649-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="27649-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="27649-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="27649-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="27649-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="27649-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="27649-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="27649-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27649-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="27649-113">Return value</span></span>

<span data-ttu-id="27649-114">Retorna o número de itens selecionados.</span><span class="sxs-lookup"><span data-stu-id="27649-114">Returns the number of selected items.</span></span>

## <a name="requirements"></a><span data-ttu-id="27649-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27649-115">Requirements</span></span>



| <span data-ttu-id="27649-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="27649-116">Requirement</span></span> | <span data-ttu-id="27649-117">Valor</span><span class="sxs-lookup"><span data-stu-id="27649-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="27649-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="27649-118">Minimum supported client</span></span><br/> | <span data-ttu-id="27649-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="27649-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="27649-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="27649-120">Minimum supported server</span></span><br/> | <span data-ttu-id="27649-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="27649-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="27649-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="27649-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="27649-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="27649-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





