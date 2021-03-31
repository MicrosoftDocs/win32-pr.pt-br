---
title: Mensagem de HDM_GETITEMCOUNT (commctrl. h)
description: Obtém uma contagem dos itens em um controle de cabeçalho. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetItemCount do cabeçalho.
ms.assetid: 0e6d2131-53b4-4927-bd0f-577b8eaf237a
keywords:
- Controles de HDM_GETITEMCOUNT de mensagens do Windows
topic_type:
- apiref
api_name:
- HDM_GETITEMCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52ac0e647a675adf2bf29b9ff1f204bbd8b040d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085824"
---
# <a name="hdm_getitemcount-message"></a><span data-ttu-id="d4b56-105">\_Mensagem HDM GETitemcount</span><span class="sxs-lookup"><span data-stu-id="d4b56-105">HDM\_GETITEMCOUNT message</span></span>

<span data-ttu-id="d4b56-106">Obtém uma contagem dos itens em um controle de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="d4b56-106">Gets a count of the items in a header control.</span></span> <span data-ttu-id="d4b56-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetItemCount do cabeçalho**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemcount) .</span><span class="sxs-lookup"><span data-stu-id="d4b56-107">You can send this message explicitly or use the [**Header\_GetItemCount**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d4b56-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d4b56-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4b56-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d4b56-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d4b56-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="d4b56-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d4b56-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d4b56-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d4b56-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="d4b56-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4b56-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d4b56-113">Return value</span></span>

<span data-ttu-id="d4b56-114">Retorna o número de itens, se for bem-sucedido, ou-1 caso contrário.</span><span class="sxs-lookup"><span data-stu-id="d4b56-114">Returns the number of items if successful, or -1 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4b56-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4b56-115">Requirements</span></span>



| <span data-ttu-id="d4b56-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4b56-116">Requirement</span></span> | <span data-ttu-id="d4b56-117">Valor</span><span class="sxs-lookup"><span data-stu-id="d4b56-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d4b56-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d4b56-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d4b56-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d4b56-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d4b56-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d4b56-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d4b56-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d4b56-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d4b56-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d4b56-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4b56-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4b56-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





