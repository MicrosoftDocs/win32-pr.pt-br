---
title: Mensagem de TVM_SORTCHILDRENCB (commctrl. h)
description: Classifica os itens de exibição em árvore usando uma função de retorno de chamada definida pelo aplicativo que compara os itens. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ SortChildrenCB.
ms.assetid: 1669e576-5e57-49f6-8097-7d6547306014
keywords:
- Controles de TVM_SORTCHILDRENCB de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_SORTCHILDRENCB
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b1dab4abbbc019a81d7a066c81dbb3537a0d80d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455889"
---
# <a name="tvm_sortchildrencb-message"></a><span data-ttu-id="77ee8-105">\_Mensagem TVM SORTCHILDRENCB</span><span class="sxs-lookup"><span data-stu-id="77ee8-105">TVM\_SORTCHILDRENCB message</span></span>

<span data-ttu-id="77ee8-106">Classifica os itens de exibição em árvore usando uma função de retorno de chamada definida pelo aplicativo que compara os itens.</span><span class="sxs-lookup"><span data-stu-id="77ee8-106">Sorts tree-view items using an application-defined callback function that compares the items.</span></span> <span data-ttu-id="77ee8-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ SortChildrenCB**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildrencb) .</span><span class="sxs-lookup"><span data-stu-id="77ee8-107">You can send this message explicitly or by using the [**TreeView\_SortChildrenCB**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildrencb) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="77ee8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="77ee8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77ee8-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="77ee8-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="77ee8-110">Reservado.</span><span class="sxs-lookup"><span data-stu-id="77ee8-110">Reserved.</span></span> <span data-ttu-id="77ee8-111">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="77ee8-111">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="77ee8-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="77ee8-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="77ee8-113">Ponteiro para uma estrutura [**TVSORTCB**](/windows/win32/api/commctrl/ns-commctrl-tvsortcb) .</span><span class="sxs-lookup"><span data-stu-id="77ee8-113">Pointer to a [**TVSORTCB**](/windows/win32/api/commctrl/ns-commctrl-tvsortcb) structure.</span></span> <span data-ttu-id="77ee8-114">O membro **lpfnCompare** é o endereço da função de retorno de chamada definida pelo aplicativo, que é chamada durante a operação de classificação cada vez que a ordem relativa de dois itens de lista precisa ser comparada.</span><span class="sxs-lookup"><span data-stu-id="77ee8-114">The **lpfnCompare** member is the address of the application-defined callback function, which is called during the sort operation each time the relative order of two list items needs to be compared.</span></span> <span data-ttu-id="77ee8-115">Para obter mais informações sobre a função de retorno de chamada, consulte a descrição de **TVSORTCB**.</span><span class="sxs-lookup"><span data-stu-id="77ee8-115">For more information about the callback function, see the description of **TVSORTCB**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77ee8-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="77ee8-116">Return value</span></span>

<span data-ttu-id="77ee8-117">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="77ee8-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="77ee8-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77ee8-118">Requirements</span></span>



| <span data-ttu-id="77ee8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="77ee8-119">Requirement</span></span> | <span data-ttu-id="77ee8-120">Valor</span><span class="sxs-lookup"><span data-stu-id="77ee8-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="77ee8-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77ee8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="77ee8-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="77ee8-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="77ee8-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77ee8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="77ee8-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="77ee8-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="77ee8-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="77ee8-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="77ee8-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="77ee8-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





