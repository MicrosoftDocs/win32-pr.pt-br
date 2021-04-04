---
title: Mensagem de LVM_DELETEITEM (commctrl. h)
description: Remove um item de um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro DeleteItem do ListView.
ms.assetid: 0eddd4c1-7786-4a8c-a16d-9fd83cce98b3
keywords:
- Controles de LVM_DELETEITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19fce5afbbaa6702f296df12acf7dad4edac16fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085175"
---
# <a name="lvm_deleteitem-message"></a><span data-ttu-id="0fec7-105">\_Mensagem DELETEITEM LVM</span><span class="sxs-lookup"><span data-stu-id="0fec7-105">LVM\_DELETEITEM message</span></span>

<span data-ttu-id="0fec7-106">Remove um item de um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="0fec7-106">Removes an item from a list-view control.</span></span> <span data-ttu-id="0fec7-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ DeleteItem do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deleteitem) .</span><span class="sxs-lookup"><span data-stu-id="0fec7-107">You can send this message explicitly or by using the [**ListView\_DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deleteitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0fec7-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0fec7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fec7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0fec7-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0fec7-110">O índice do item de exibição de lista a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="0fec7-110">The index of the list-view item to delete.</span></span>

</dd> <dt>

<span data-ttu-id="0fec7-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0fec7-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="0fec7-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="0fec7-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fec7-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0fec7-113">Return value</span></span>

<span data-ttu-id="0fec7-114">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="0fec7-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fec7-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0fec7-115">Requirements</span></span>



| <span data-ttu-id="0fec7-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0fec7-116">Requirement</span></span> | <span data-ttu-id="0fec7-117">Valor</span><span class="sxs-lookup"><span data-stu-id="0fec7-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0fec7-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0fec7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0fec7-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0fec7-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0fec7-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0fec7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0fec7-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0fec7-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0fec7-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0fec7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0fec7-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0fec7-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





