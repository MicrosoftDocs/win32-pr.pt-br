---
title: Mensagem de LVM_GETTOPINDEX (commctrl. h)
description: Recupera o índice do item visível superior no modo de exibição de lista ou de relatório. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetTopIndex do ListView.
ms.assetid: vs|controls|~\controls\listview\messages\lvm_gettopindex.htm
keywords:
- Controles de LVM_GETTOPINDEX de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETTOPINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb1cb080588d1825fcbd9e6c5e7b1b573fd7ad2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105811143"
---
# <a name="lvm_gettopindex-message"></a><span data-ttu-id="913fa-105">\_Mensagem GETTOPINDEX LVM</span><span class="sxs-lookup"><span data-stu-id="913fa-105">LVM\_GETTOPINDEX message</span></span>

<span data-ttu-id="913fa-106">Recupera o índice do item visível superior no modo de exibição de lista ou de relatório.</span><span class="sxs-lookup"><span data-stu-id="913fa-106">Retrieves the index of the topmost visible item when in list or report view.</span></span> <span data-ttu-id="913fa-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetTopIndex do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettopindex) .</span><span class="sxs-lookup"><span data-stu-id="913fa-107">You can send this message explicitly or by using the [**ListView\_GetTopIndex**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettopindex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="913fa-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="913fa-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="913fa-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="913fa-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="913fa-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="913fa-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="913fa-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="913fa-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="913fa-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="913fa-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="913fa-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="913fa-113">Return value</span></span>

<span data-ttu-id="913fa-114">Retorna o índice do item se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="913fa-114">Returns the index of the item if successful.</span></span> <span data-ttu-id="913fa-115">Retornará zero se o controle de exibição de lista estiver em um modo de exibição de ícone ou pequeno, ou se o controle de exibição de lista estiver no modo de exibição de detalhes com grupos habilitados.</span><span class="sxs-lookup"><span data-stu-id="913fa-115">Returns zero if the list-view control is in icon or small icon view, or if the list-view control is in details view with groups enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="913fa-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="913fa-116">Requirements</span></span>



| <span data-ttu-id="913fa-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="913fa-117">Requirement</span></span> | <span data-ttu-id="913fa-118">Valor</span><span class="sxs-lookup"><span data-stu-id="913fa-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="913fa-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="913fa-119">Minimum supported client</span></span><br/> | <span data-ttu-id="913fa-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="913fa-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="913fa-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="913fa-121">Minimum supported server</span></span><br/> | <span data-ttu-id="913fa-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="913fa-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="913fa-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="913fa-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="913fa-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="913fa-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





