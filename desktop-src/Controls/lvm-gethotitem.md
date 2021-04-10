---
title: Mensagem de LVM_GETHOTITEM (commctrl. h)
description: Recupera o índice do item ativo. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetHotItem do ListView.
ms.assetid: f80189da-6c8b-4faf-925a-0c33fedf8c4e
keywords:
- Controles de LVM_GETHOTITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56c7bbfb845518eb40b55556df5294d59cff3d7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086167"
---
# <a name="lvm_gethotitem-message"></a><span data-ttu-id="79444-105">\_Mensagem GETHOTITEM LVM</span><span class="sxs-lookup"><span data-stu-id="79444-105">LVM\_GETHOTITEM message</span></span>

<span data-ttu-id="79444-106">Recupera o índice do item ativo.</span><span class="sxs-lookup"><span data-stu-id="79444-106">Retrieves the index of the hot item.</span></span> <span data-ttu-id="79444-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetHotItem do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethotitem) .</span><span class="sxs-lookup"><span data-stu-id="79444-107">You can send this message explicitly or use the [**ListView\_GetHotItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethotitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="79444-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="79444-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79444-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="79444-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="79444-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="79444-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="79444-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="79444-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="79444-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="79444-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79444-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="79444-113">Return value</span></span>

<span data-ttu-id="79444-114">Retorna o índice do item que está quente.</span><span class="sxs-lookup"><span data-stu-id="79444-114">Returns the index of the item that is hot.</span></span>

## <a name="requirements"></a><span data-ttu-id="79444-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79444-115">Requirements</span></span>



| <span data-ttu-id="79444-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="79444-116">Requirement</span></span> | <span data-ttu-id="79444-117">Valor</span><span class="sxs-lookup"><span data-stu-id="79444-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="79444-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79444-118">Minimum supported client</span></span><br/> | <span data-ttu-id="79444-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="79444-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="79444-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79444-120">Minimum supported server</span></span><br/> | <span data-ttu-id="79444-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="79444-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="79444-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="79444-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="79444-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="79444-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





