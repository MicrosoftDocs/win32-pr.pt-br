---
title: Mensagem de LVM_GETTEXTCOLOR (commctrl. h)
description: Recupera a cor do texto de um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetTextColor do ListView.
ms.assetid: 51685e61-dd0a-4c21-8c66-31cf72c2b3e4
keywords:
- Controles de LVM_GETTEXTCOLOR de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7686e8f06f49dbfc14899f47ba52017daaf23c07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753575"
---
# <a name="lvm_gettextcolor-message"></a><span data-ttu-id="89266-105">\_Mensagem GETTEXTCOLOR LVM</span><span class="sxs-lookup"><span data-stu-id="89266-105">LVM\_GETTEXTCOLOR message</span></span>

<span data-ttu-id="89266-106">Recupera a cor do texto de um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="89266-106">Retrieves the text color of a list-view control.</span></span> <span data-ttu-id="89266-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetTextColor do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettextcolor) .</span><span class="sxs-lookup"><span data-stu-id="89266-107">You can send this message explicitly or by using the [**ListView\_GetTextColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettextcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="89266-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="89266-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89266-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="89266-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="89266-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="89266-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="89266-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="89266-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="89266-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="89266-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89266-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="89266-113">Return value</span></span>

<span data-ttu-id="89266-114">Retorna a cor do texto.</span><span class="sxs-lookup"><span data-stu-id="89266-114">Returns the text color.</span></span>

## <a name="requirements"></a><span data-ttu-id="89266-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89266-115">Requirements</span></span>



| <span data-ttu-id="89266-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="89266-116">Requirement</span></span> | <span data-ttu-id="89266-117">Valor</span><span class="sxs-lookup"><span data-stu-id="89266-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="89266-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89266-118">Minimum supported client</span></span><br/> | <span data-ttu-id="89266-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="89266-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="89266-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89266-120">Minimum supported server</span></span><br/> | <span data-ttu-id="89266-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="89266-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="89266-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="89266-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="89266-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="89266-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





