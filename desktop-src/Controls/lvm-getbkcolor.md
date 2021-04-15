---
title: Mensagem de LVM_GETBKCOLOR (commctrl. h)
description: Obtém a cor da tela de fundo de um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetBkColor do ListView.
ms.assetid: 077d3b2e-f6d1-4acc-b002-e9e707ad274c
keywords:
- Controles de LVM_GETBKCOLOR de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4329adda75677d1cc0126eaa0196fadf143cd0b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454635"
---
# <a name="lvm_getbkcolor-message"></a><span data-ttu-id="e6b48-105">\_Mensagem GETBKCOLOR LVM</span><span class="sxs-lookup"><span data-stu-id="e6b48-105">LVM\_GETBKCOLOR message</span></span>

<span data-ttu-id="e6b48-106">Obtém a cor da tela de fundo de um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="e6b48-106">Gets the background color of a list-view control.</span></span> <span data-ttu-id="e6b48-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetBkColor do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getbkcolor) .</span><span class="sxs-lookup"><span data-stu-id="e6b48-107">You can send this message explicitly or by using the [**ListView\_GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getbkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e6b48-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e6b48-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6b48-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e6b48-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e6b48-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="e6b48-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e6b48-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e6b48-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="e6b48-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="e6b48-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6b48-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e6b48-113">Return value</span></span>

<span data-ttu-id="e6b48-114">Retorna a cor da tela de fundo do controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="e6b48-114">Returns the background color of the list-view control.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6b48-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6b48-115">Requirements</span></span>



| <span data-ttu-id="e6b48-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6b48-116">Requirement</span></span> | <span data-ttu-id="e6b48-117">Valor</span><span class="sxs-lookup"><span data-stu-id="e6b48-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e6b48-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e6b48-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e6b48-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e6b48-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e6b48-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e6b48-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e6b48-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e6b48-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e6b48-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e6b48-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6b48-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6b48-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





