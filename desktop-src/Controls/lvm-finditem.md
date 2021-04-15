---
title: Mensagem de LVM_FINDITEM (commctrl. h)
description: Procura um item de exibição de lista com as características especificadas. Você pode enviar essa mensagem explicitamente ou usando a \_ macro FindItem do ListView.
ms.assetid: 3b18c8ad-97e6-4f4d-bf89-afb95f925ed1
keywords:
- Controles de LVM_FINDITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_FINDITEM
- LVM_FINDITEMA
- LVM_FINDITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1f7dfc19e263a6ab7ad29b5e514fa4e52c1a9ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454636"
---
# <a name="lvm_finditem-message"></a><span data-ttu-id="c4365-105">\_Mensagem FINDITEM LVM</span><span class="sxs-lookup"><span data-stu-id="c4365-105">LVM\_FINDITEM message</span></span>

<span data-ttu-id="c4365-106">Procura um item de exibição de lista com as características especificadas.</span><span class="sxs-lookup"><span data-stu-id="c4365-106">Searches for a list-view item with the specified characteristics.</span></span> <span data-ttu-id="c4365-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ FindItem do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_finditem) .</span><span class="sxs-lookup"><span data-stu-id="c4365-107">You can send this message explicitly or by using the [**ListView\_FindItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_finditem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c4365-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c4365-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4365-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c4365-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c4365-110">O índice do item para iniciar a pesquisa com ou-1 para iniciar desde o início.</span><span class="sxs-lookup"><span data-stu-id="c4365-110">The index of the item to begin the search with or -1 to start from the beginning.</span></span> <span data-ttu-id="c4365-111">O item especificado é excluído da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="c4365-111">The specified item is itself excluded from the search.</span></span>

</dd> <dt>

<span data-ttu-id="c4365-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c4365-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c4365-113">Um ponteiro para uma estrutura [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) que contém informações sobre o que Pesquisar.</span><span class="sxs-lookup"><span data-stu-id="c4365-113">A pointer to an [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) structure that contains information about what to search for.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4365-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c4365-114">Return value</span></span>

<span data-ttu-id="c4365-115">Retorna o índice do item se for bem-sucedido ou-1 caso contrário.</span><span class="sxs-lookup"><span data-stu-id="c4365-115">Returns the index of the item if successful, or -1 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4365-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4365-116">Requirements</span></span>



| <span data-ttu-id="c4365-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4365-117">Requirement</span></span> | <span data-ttu-id="c4365-118">Valor</span><span class="sxs-lookup"><span data-stu-id="c4365-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c4365-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c4365-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c4365-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c4365-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c4365-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c4365-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c4365-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c4365-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c4365-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c4365-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4365-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4365-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="c4365-125">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="c4365-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c4365-126">**LVM \_ FINDITEMW** (Unicode) e **LVM \_ FINDITEMA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c4365-126">**LVM\_FINDITEMW** (Unicode) and **LVM\_FINDITEMA** (ANSI)</span></span><br/>                 |



 

 





