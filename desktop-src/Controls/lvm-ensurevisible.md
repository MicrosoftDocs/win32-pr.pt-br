---
title: Mensagem de LVM_ENSUREVISIBLE (commctrl. h)
description: Garante que um item de exibição de lista seja totalmente ou parcialmente visível, rolando o controle de exibição de lista, se necessário. Você pode enviar essa mensagem explicitamente ou usando a \_ macro EnsureVisible do ListView.
ms.assetid: 3564b6e6-b8b6-401b-85bc-8bd6261fc054
keywords:
- Controles de LVM_ENSUREVISIBLE de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_ENSUREVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d0ff4009399988f20f3e162114f91e4cff02820
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103917998"
---
# <a name="lvm_ensurevisible-message"></a><span data-ttu-id="8309d-105">\_Mensagem ENSUREVISIBLE LVM</span><span class="sxs-lookup"><span data-stu-id="8309d-105">LVM\_ENSUREVISIBLE message</span></span>

<span data-ttu-id="8309d-106">Garante que um item de exibição de lista seja totalmente ou parcialmente visível, rolando o controle de exibição de lista, se necessário.</span><span class="sxs-lookup"><span data-stu-id="8309d-106">Ensures that a list-view item is either entirely or partially visible, scrolling the list-view control if necessary.</span></span> <span data-ttu-id="8309d-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ EnsureVisible do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_ensurevisible) .</span><span class="sxs-lookup"><span data-stu-id="8309d-107">You can send this message explicitly or by using the [**ListView\_EnsureVisible**](/windows/desktop/api/Commctrl/nf-commctrl-listview_ensurevisible) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8309d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8309d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8309d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8309d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8309d-110">O índice do item de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="8309d-110">The index of the list-view item.</span></span>

</dd> <dt>

<span data-ttu-id="8309d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8309d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8309d-112">Um valor que especifica se o item deve estar totalmente visível.</span><span class="sxs-lookup"><span data-stu-id="8309d-112">A value specifying whether the item must be entirely visible.</span></span> <span data-ttu-id="8309d-113">Se esse parâmetro for **true**, nenhuma rolagem ocorrerá se o item estiver pelo menos parcialmente visível.</span><span class="sxs-lookup"><span data-stu-id="8309d-113">If this parameter is **TRUE**, no scrolling occurs if the item is at least partially visible.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8309d-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8309d-114">Return value</span></span>

<span data-ttu-id="8309d-115">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="8309d-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8309d-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="8309d-116">Remarks</span></span>

<span data-ttu-id="8309d-117">A mensagem falhará se o estilo da janela incluir [**LVS \_ NoScroll**](list-view-window-styles.md).</span><span class="sxs-lookup"><span data-stu-id="8309d-117">The message fails if the window style includes [**LVS\_NOSCROLL**](list-view-window-styles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8309d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8309d-118">Requirements</span></span>



| <span data-ttu-id="8309d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8309d-119">Requirement</span></span> | <span data-ttu-id="8309d-120">Valor</span><span class="sxs-lookup"><span data-stu-id="8309d-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8309d-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8309d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8309d-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8309d-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8309d-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8309d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8309d-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8309d-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8309d-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8309d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8309d-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8309d-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





