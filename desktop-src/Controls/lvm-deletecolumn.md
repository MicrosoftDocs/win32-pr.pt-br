---
title: Mensagem de LVM_DELETECOLUMN (commctrl. h)
description: Remove uma coluna de um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro DeleteColumn do ListView.
ms.assetid: 1748a70b-9a13-4753-ac23-55b5652164c2
keywords:
- Controles de LVM_DELETECOLUMN de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_DELETECOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: daa9005009ceaf42a01ede4f0f26334ae686c2df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644267"
---
# <a name="lvm_deletecolumn-message"></a><span data-ttu-id="7af96-105">\_Mensagem DELETECOLUMN LVM</span><span class="sxs-lookup"><span data-stu-id="7af96-105">LVM\_DELETECOLUMN message</span></span>

<span data-ttu-id="7af96-106">Remove uma coluna de um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="7af96-106">Removes a column from a list-view control.</span></span> <span data-ttu-id="7af96-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ DeleteColumn do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deletecolumn) .</span><span class="sxs-lookup"><span data-stu-id="7af96-107">You can send this message explicitly or by using the [**ListView\_DeleteColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deletecolumn) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7af96-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7af96-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7af96-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7af96-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7af96-110">O índice da coluna a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="7af96-110">The index of the column to delete.</span></span>

</dd> <dt>

<span data-ttu-id="7af96-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7af96-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="7af96-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="7af96-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7af96-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7af96-113">Return value</span></span>

<span data-ttu-id="7af96-114">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="7af96-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7af96-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="7af96-115">Remarks</span></span>

<span data-ttu-id="7af96-116">A exclusão de coluna zero de um controle de exibição de lista tem suporte apenas no ComCtl32.dll versão 6 e posterior.</span><span class="sxs-lookup"><span data-stu-id="7af96-116">Deleting column zero of a list-view control is supported only in ComCtl32.dll version 6 and later.</span></span> <span data-ttu-id="7af96-117">A versão 5 também dá suporte à exclusão de coluna zero, mas somente depois de usar [**CCM \_ SetVersion**](ccm-setversion.md) para definir a versão como 5 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="7af96-117">Version 5 also supports deleting column zero, but only after you use [**CCM\_SETVERSION**](ccm-setversion.md) to set the version to 5 or later.</span></span> <span data-ttu-id="7af96-118">Em versões anteriores à versão 5, se você precisar excluir a coluna zero, insira uma coluna fictícia de comprimento zero zero e exclua a coluna um e acima.</span><span class="sxs-lookup"><span data-stu-id="7af96-118">In versions prior to version 5, if you must delete column zero, insert a zero length dummy column zero and delete column one and above.</span></span>

## <a name="requirements"></a><span data-ttu-id="7af96-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7af96-119">Requirements</span></span>



| <span data-ttu-id="7af96-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7af96-120">Requirement</span></span> | <span data-ttu-id="7af96-121">Valor</span><span class="sxs-lookup"><span data-stu-id="7af96-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7af96-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7af96-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7af96-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7af96-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7af96-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7af96-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7af96-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7af96-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7af96-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7af96-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="7af96-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7af96-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





