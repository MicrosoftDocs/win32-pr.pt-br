---
title: Mensagem de HDM_GETITEMRECT (commctrl. h)
description: Obtém o retângulo delimitador para um determinado item em um controle de cabeçalho. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetItemRect do cabeçalho.
ms.assetid: b483ef97-3700-425b-8160-81c673850f68
keywords:
- Controles de HDM_GETITEMRECT de mensagens do Windows
topic_type:
- apiref
api_name:
- HDM_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4baec72bd914a9d2dad72556a5444c0059452cf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455435"
---
# <a name="hdm_getitemrect-message"></a><span data-ttu-id="ae30a-105">\_Mensagem HDM GETITEMRECT</span><span class="sxs-lookup"><span data-stu-id="ae30a-105">HDM\_GETITEMRECT message</span></span>

<span data-ttu-id="ae30a-106">Obtém o retângulo delimitador para um determinado item em um controle de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="ae30a-106">Gets the bounding rectangle for a given item in a header control.</span></span> <span data-ttu-id="ae30a-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetItemRect do cabeçalho**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemrect) .</span><span class="sxs-lookup"><span data-stu-id="ae30a-107">You can send this message explicitly or use the [**Header\_GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ae30a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ae30a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae30a-109">*wParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ae30a-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae30a-110">O índice de base zero do item de controle de cabeçalho para o qual recuperar o retângulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="ae30a-110">The zero-based index of the header control item for which to retrieve the bounding rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="ae30a-111">*lParam* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="ae30a-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae30a-112">Um ponteiro para uma estrutura [**Rect**](/windows/win32/api/windef/ns-windef-rect) que recebe as informações do retângulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="ae30a-112">A pointer to a [**RECT**](/windows/win32/api/windef/ns-windef-rect) structure that receives the bounding rectangle information.</span></span> <span data-ttu-id="ae30a-113">O remetente da mensagem é responsável por alocar essa estrutura.</span><span class="sxs-lookup"><span data-stu-id="ae30a-113">The message sender is responsible for allocating this structure.</span></span> <span data-ttu-id="ae30a-114">As coordenadas retornadas na estrutura RECT são expressas em relação ao pai do controle de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="ae30a-114">The coordinates returned in the RECT structure are expressed relative to the header control parent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae30a-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ae30a-115">Return value</span></span>

<span data-ttu-id="ae30a-116">Retornará zero se for bem-sucedido ou nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="ae30a-116">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae30a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae30a-117">Requirements</span></span>



| <span data-ttu-id="ae30a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae30a-118">Requirement</span></span> | <span data-ttu-id="ae30a-119">Valor</span><span class="sxs-lookup"><span data-stu-id="ae30a-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ae30a-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ae30a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ae30a-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ae30a-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ae30a-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ae30a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ae30a-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ae30a-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ae30a-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ae30a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae30a-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae30a-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





