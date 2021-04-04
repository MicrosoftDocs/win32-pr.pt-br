---
title: Mensagem de LVM_GETITEMCOUNT (commctrl. h)
description: Recupera o número de itens em um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetItemCount de ListView.
ms.assetid: 7c639d69-e42c-41b5-9fdd-4943166752a2
keywords:
- Controles de LVM_GETITEMCOUNT de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETITEMCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff2791440c7285d054eca0d2945086d06e3c35a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645022"
---
# <a name="lvm_getitemcount-message"></a><span data-ttu-id="f2ea5-105">Mensagem do LVM \_ GETitemcount</span><span class="sxs-lookup"><span data-stu-id="f2ea5-105">LVM\_GETITEMCOUNT message</span></span>

<span data-ttu-id="f2ea5-106">Recupera o número de itens em um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="f2ea5-106">Retrieves the number of items in a list-view control.</span></span> <span data-ttu-id="f2ea5-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetItemCount de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemcount) .</span><span class="sxs-lookup"><span data-stu-id="f2ea5-107">You can send this message explicitly or by using the [**ListView\_GetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f2ea5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f2ea5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2ea5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f2ea5-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f2ea5-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="f2ea5-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f2ea5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f2ea5-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="f2ea5-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="f2ea5-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2ea5-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f2ea5-113">Return value</span></span>

<span data-ttu-id="f2ea5-114">Retorna o número de itens.</span><span class="sxs-lookup"><span data-stu-id="f2ea5-114">Returns the number of items.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2ea5-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2ea5-115">Requirements</span></span>



| <span data-ttu-id="f2ea5-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2ea5-116">Requirement</span></span> | <span data-ttu-id="f2ea5-117">Valor</span><span class="sxs-lookup"><span data-stu-id="f2ea5-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f2ea5-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2ea5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f2ea5-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f2ea5-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f2ea5-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2ea5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f2ea5-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f2ea5-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f2ea5-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f2ea5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2ea5-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2ea5-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





