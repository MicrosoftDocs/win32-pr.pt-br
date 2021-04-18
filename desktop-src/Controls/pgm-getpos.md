---
title: Mensagem de PGM_GETPOS (commctrl. h)
description: Recupera a posição de rolagem atual do controle de pager. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetPos do pager.
ms.assetid: 1e0f967a-3290-43b7-b812-8cf56abf2d32
keywords:
- Controles de PGM_GETPOS de mensagens do Windows
topic_type:
- apiref
api_name:
- PGM_GETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 611a27e9cb952c5be190fa041af3d238f0184b03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105755426"
---
# <a name="pgm_getpos-message"></a><span data-ttu-id="381e6-105">\_Mensagem GETPOS do PGM</span><span class="sxs-lookup"><span data-stu-id="381e6-105">PGM\_GETPOS message</span></span>

<span data-ttu-id="381e6-106">Recupera a posição de rolagem atual do controle de pager.</span><span class="sxs-lookup"><span data-stu-id="381e6-106">Retrieves the current scroll position of the pager control.</span></span> <span data-ttu-id="381e6-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetPos do pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getpos) .</span><span class="sxs-lookup"><span data-stu-id="381e6-107">You can send this message explicitly or use the [**Pager\_GetPos**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getpos) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="381e6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="381e6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="381e6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="381e6-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="381e6-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="381e6-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="381e6-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="381e6-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="381e6-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="381e6-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="381e6-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="381e6-113">Return value</span></span>

<span data-ttu-id="381e6-114">Retorna um valor INT que contém a posição de rolagem atual, em pixels.</span><span class="sxs-lookup"><span data-stu-id="381e6-114">Returns an INT value that contains the current scroll position, in pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="381e6-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="381e6-115">Requirements</span></span>



| <span data-ttu-id="381e6-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="381e6-116">Requirement</span></span> | <span data-ttu-id="381e6-117">Valor</span><span class="sxs-lookup"><span data-stu-id="381e6-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="381e6-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="381e6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="381e6-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="381e6-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="381e6-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="381e6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="381e6-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="381e6-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="381e6-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="381e6-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="381e6-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="381e6-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





