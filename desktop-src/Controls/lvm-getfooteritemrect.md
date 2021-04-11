---
title: Mensagem de LVM_GETFOOTERITEMRECT (commctrl. h)
description: Obtém as coordenadas de um rodapé para um item especificado em um controle de exibição de lista. Envie essa mensagem explicitamente ou usando a \_ macro GetFooterItemRect do ListView.
ms.assetid: 4a6055d3-1cc1-4c3d-a5f6-006617ff3bce
keywords:
- Controles de LVM_GETFOOTERITEMRECT de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETFOOTERITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 142cb92806fa1d58faa0414c10c41bd2815d5b6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104163579"
---
# <a name="lvm_getfooteritemrect-message"></a><span data-ttu-id="34b01-105">\_Mensagem GETFOOTERITEMRECT LVM</span><span class="sxs-lookup"><span data-stu-id="34b01-105">LVM\_GETFOOTERITEMRECT message</span></span>

<span data-ttu-id="34b01-106">Obtém as coordenadas de um rodapé para um item especificado em um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="34b01-106">Gets the coordinates of a footer for a specified item in a list-view control.</span></span> <span data-ttu-id="34b01-107">Envie essa mensagem explicitamente ou usando a macro [**\_ GetFooterItemRect do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooteritemrect) .</span><span class="sxs-lookup"><span data-stu-id="34b01-107">Send this message explicitly or by using the [**ListView\_GetFooterItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooteritemrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="34b01-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="34b01-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34b01-109">*wParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="34b01-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34b01-110">O índice do item no controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="34b01-110">The index of the item in the list-view control.</span></span>

</dd> <dt>

<span data-ttu-id="34b01-111">*lParam* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="34b01-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="34b01-112">Um ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) para receber as coordenadas.</span><span class="sxs-lookup"><span data-stu-id="34b01-112">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to receive the coordinates.</span></span> <span data-ttu-id="34b01-113">O aplicativo de chamada é responsável por alocar essa estrutura.</span><span class="sxs-lookup"><span data-stu-id="34b01-113">The calling application is responsible for allocating this structure.</span></span> <span data-ttu-id="34b01-114">As coordenadas recebidas são expressas como coordenadas do cliente.</span><span class="sxs-lookup"><span data-stu-id="34b01-114">The coordinates received are expressed as client coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34b01-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="34b01-115">Return value</span></span>

<span data-ttu-id="34b01-116">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="34b01-116">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="34b01-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34b01-117">Requirements</span></span>



| <span data-ttu-id="34b01-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="34b01-118">Requirement</span></span> | <span data-ttu-id="34b01-119">Valor</span><span class="sxs-lookup"><span data-stu-id="34b01-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="34b01-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="34b01-120">Minimum supported client</span></span><br/> | <span data-ttu-id="34b01-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="34b01-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="34b01-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="34b01-122">Minimum supported server</span></span><br/> | <span data-ttu-id="34b01-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="34b01-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="34b01-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="34b01-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="34b01-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="34b01-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

