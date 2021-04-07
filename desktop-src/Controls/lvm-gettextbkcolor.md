---
title: Mensagem de LVM_GETTEXTBKCOLOR (commctrl. h)
description: Recupera a cor da tela de fundo do texto de um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetTextBkColor do ListView.
ms.assetid: 3d2c8be8-d7f9-4aa7-b358-f7effc6dbb25
keywords:
- Controles de LVM_GETTEXTBKCOLOR de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETTEXTBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36bf5b6700904c5af47ef47e749dfa753c5ff8cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918966"
---
# <a name="lvm_gettextbkcolor-message"></a><span data-ttu-id="7f57b-105">\_Mensagem GETTEXTBKCOLOR LVM</span><span class="sxs-lookup"><span data-stu-id="7f57b-105">LVM\_GETTEXTBKCOLOR message</span></span>

<span data-ttu-id="7f57b-106">Recupera a cor da tela de fundo do texto de um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="7f57b-106">Retrieves the text background color of a list-view control.</span></span> <span data-ttu-id="7f57b-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetTextBkColor do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettextbkcolor) .</span><span class="sxs-lookup"><span data-stu-id="7f57b-107">You can send this message explicitly or by using the [**ListView\_GetTextBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettextbkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7f57b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7f57b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f57b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7f57b-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7f57b-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="7f57b-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="7f57b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7f57b-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="7f57b-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="7f57b-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f57b-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7f57b-113">Return value</span></span>

<span data-ttu-id="7f57b-114">Retorna a cor do plano de fundo do texto.</span><span class="sxs-lookup"><span data-stu-id="7f57b-114">Returns the background color of the text.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f57b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f57b-115">Requirements</span></span>



| <span data-ttu-id="7f57b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f57b-116">Requirement</span></span> | <span data-ttu-id="7f57b-117">Valor</span><span class="sxs-lookup"><span data-stu-id="7f57b-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7f57b-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7f57b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7f57b-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7f57b-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7f57b-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7f57b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7f57b-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7f57b-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7f57b-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7f57b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f57b-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f57b-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





