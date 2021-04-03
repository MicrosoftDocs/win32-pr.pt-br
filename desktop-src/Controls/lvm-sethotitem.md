---
title: Mensagem de LVM_SETHOTITEM (commctrl. h)
description: Define o item ativo para um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usar a \_ macro SetHotItem do ListView.
ms.assetid: 0aa2b15d-4983-4234-9863-f1fdee09f913
keywords:
- Controles de LVM_SETHOTITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82c17bc67c530581b79a87030b31b655f856dd0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644260"
---
# <a name="lvm_sethotitem-message"></a><span data-ttu-id="939c2-105">\_Mensagem SETHOTITEM LVM</span><span class="sxs-lookup"><span data-stu-id="939c2-105">LVM\_SETHOTITEM message</span></span>

<span data-ttu-id="939c2-106">Define o item ativo para um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="939c2-106">Sets the hot item for a list-view control.</span></span> <span data-ttu-id="939c2-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetHotItem do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethotitem) .</span><span class="sxs-lookup"><span data-stu-id="939c2-107">You can send this message explicitly or use the [**ListView\_SetHotItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethotitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="939c2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="939c2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="939c2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="939c2-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="939c2-110">Índice de base zero do item a ser definido como o item ativo.</span><span class="sxs-lookup"><span data-stu-id="939c2-110">Zero-based index of the item to be set as the hot item.</span></span>

</dd> <dt>

<span data-ttu-id="939c2-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="939c2-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="939c2-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="939c2-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="939c2-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="939c2-113">Return value</span></span>

<span data-ttu-id="939c2-114">Retorna o índice do item que estava anteriormente quente.</span><span class="sxs-lookup"><span data-stu-id="939c2-114">Returns the index of the item that was previously hot.</span></span>

## <a name="requirements"></a><span data-ttu-id="939c2-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="939c2-115">Requirements</span></span>



| <span data-ttu-id="939c2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="939c2-116">Requirement</span></span> | <span data-ttu-id="939c2-117">Valor</span><span class="sxs-lookup"><span data-stu-id="939c2-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="939c2-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="939c2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="939c2-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="939c2-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="939c2-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="939c2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="939c2-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="939c2-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="939c2-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="939c2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="939c2-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="939c2-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





