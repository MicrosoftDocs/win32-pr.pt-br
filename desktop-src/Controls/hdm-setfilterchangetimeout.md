---
title: Mensagem de HDM_SETFILTERCHANGETIMEOUT (commctrl. h)
description: Define o intervalo de tempo limite entre a hora em que uma alteração ocorre nos atributos de filtro e o lançamento de uma \_ notificação HDN FILTERCHANGE. Você pode enviar essa mensagem explicitamente ou usar a \_ macro SetFilterChangeTimeout do cabeçalho.
ms.assetid: 9bc8e0e7-d7c1-4dd6-9d39-6ae937f19d60
keywords:
- Controles de HDM_SETFILTERCHANGETIMEOUT de mensagens do Windows
topic_type:
- apiref
api_name:
- HDM_SETFILTERCHANGETIMEOUT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9876634d12cd15001c296151694cb755ed1b34e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009617"
---
# <a name="hdm_setfilterchangetimeout-message"></a><span data-ttu-id="76d3d-105">\_Mensagem HDM SETFILTERCHANGETIMEOUT</span><span class="sxs-lookup"><span data-stu-id="76d3d-105">HDM\_SETFILTERCHANGETIMEOUT message</span></span>

<span data-ttu-id="76d3d-106">Define o intervalo de tempo limite entre a hora em que uma alteração ocorre nos atributos de filtro e o lançamento de uma notificação [HDN \_ FILTERCHANGE](hdn-filterchange.md) .</span><span class="sxs-lookup"><span data-stu-id="76d3d-106">Sets the timeout interval between the time a change takes place in the filter attributes and the posting of an [HDN\_FILTERCHANGE](hdn-filterchange.md) notification.</span></span> <span data-ttu-id="76d3d-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetFilterChangeTimeout do cabeçalho**](/windows/desktop/api/Commctrl/nf-commctrl-header_setfilterchangetimeout) .</span><span class="sxs-lookup"><span data-stu-id="76d3d-107">You can send this message explicitly or use the [**Header\_SetFilterChangeTimeout**](/windows/desktop/api/Commctrl/nf-commctrl-header_setfilterchangetimeout) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="76d3d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="76d3d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76d3d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="76d3d-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="76d3d-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="76d3d-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="76d3d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="76d3d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="76d3d-112">O valor de tempo limite, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="76d3d-112">The timeout value, in milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76d3d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="76d3d-113">Return value</span></span>

<span data-ttu-id="76d3d-114">Retorna o índice do controle de filtro que está sendo modificado.</span><span class="sxs-lookup"><span data-stu-id="76d3d-114">Returns the index of the filter control being modified.</span></span>

## <a name="requirements"></a><span data-ttu-id="76d3d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76d3d-115">Requirements</span></span>



| <span data-ttu-id="76d3d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="76d3d-116">Requirement</span></span> | <span data-ttu-id="76d3d-117">Valor</span><span class="sxs-lookup"><span data-stu-id="76d3d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="76d3d-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="76d3d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="76d3d-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="76d3d-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="76d3d-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="76d3d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="76d3d-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="76d3d-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="76d3d-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="76d3d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="76d3d-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="76d3d-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76d3d-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="76d3d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76d3d-125">HDN \_ FILTERCHANGE</span><span class="sxs-lookup"><span data-stu-id="76d3d-125">HDN\_FILTERCHANGE</span></span>](hdn-filterchange.md)
</dt> </dl>

 

 





