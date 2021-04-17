---
title: Mensagem de TVM_SETAUTOSCROLLINFO (commctrl. h)
description: Define informações usadas para determinar as características de rolagem automática. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ SetAutoScrollInfo.
ms.assetid: de55933f-1caa-4193-84de-0486c41e8f1f
keywords:
- Controles de TVM_SETAUTOSCROLLINFO de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_SETAUTOSCROLLINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faa1f7920d2ec8c443b2ec5f1ff9189c22c5f21e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105754369"
---
# <a name="tvm_setautoscrollinfo-message"></a><span data-ttu-id="96904-105">\_Mensagem TVM SETAUTOSCROLLINFO</span><span class="sxs-lookup"><span data-stu-id="96904-105">TVM\_SETAUTOSCROLLINFO message</span></span>

<span data-ttu-id="96904-106">Define informações usadas para determinar as características de rolagem automática.</span><span class="sxs-lookup"><span data-stu-id="96904-106">Sets information used to determine auto-scroll characteristics.</span></span> <span data-ttu-id="96904-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ SetAutoScrollInfo**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setautoscrollinfo) .</span><span class="sxs-lookup"><span data-stu-id="96904-107">You can send this message explicitly or by using the [**TreeView\_SetAutoScrollInfo**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setautoscrollinfo) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="96904-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="96904-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96904-109">*wParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="96904-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96904-110">Especifica pixels por segundo.</span><span class="sxs-lookup"><span data-stu-id="96904-110">Specifies pixels per second.</span></span> <span data-ttu-id="96904-111">O deslocamento para a rolagem é dividido pelo *wParam* para determinar a duração total da rolagem automática.</span><span class="sxs-lookup"><span data-stu-id="96904-111">The offset to scroll is divided by the *wParam* to determine the total duration of the auto-scroll.</span></span>

</dd> <dt>

<span data-ttu-id="96904-112">*lParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="96904-112">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96904-113">Especifica o intervalo de tempo de redesenho.</span><span class="sxs-lookup"><span data-stu-id="96904-113">Specifies the redraw time interval.</span></span> <span data-ttu-id="96904-114">Redesenhe a cada intervalo de ELASPED até que o item seja rolado para a exibição.</span><span class="sxs-lookup"><span data-stu-id="96904-114">Redraw at every elasped interval, until the item is scrolled into view.</span></span> <span data-ttu-id="96904-115">Determinado *wParam*, o local do item é calculado e um redesenho ocorre.</span><span class="sxs-lookup"><span data-stu-id="96904-115">Given *wParam*, the location of the item is calculated and a repaint occurs.</span></span> <span data-ttu-id="96904-116">Defina esse valor para criar uma rolagem suave.</span><span class="sxs-lookup"><span data-stu-id="96904-116">Set this value to create smooth scrolling.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96904-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="96904-117">Return value</span></span>

<span data-ttu-id="96904-118">Retorna **true**.</span><span class="sxs-lookup"><span data-stu-id="96904-118">Returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="96904-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="96904-119">Remarks</span></span>

<span data-ttu-id="96904-120">As informações de AutoScroll são usadas para rolar um item não visível para a exibição.</span><span class="sxs-lookup"><span data-stu-id="96904-120">Autoscroll information is used to scroll a nonvisible item into view.</span></span> <span data-ttu-id="96904-121">O controle deve ter o estilo estendido de [**TVs \_ ex \_ AUTOHSCROLL**](tree-view-control-window-extended-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="96904-121">The control must have the [**TVS\_EX\_AUTOHSCROLL**](tree-view-control-window-extended-styles.md) extended style.</span></span> <span data-ttu-id="96904-122">Para obter informações sobre estilos estendidos, consulte Tree-View estilos estendidos de controle.</span><span class="sxs-lookup"><span data-stu-id="96904-122">For information on extended styles, see Tree-View Control Extended Styles.</span></span>

## <a name="requirements"></a><span data-ttu-id="96904-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96904-123">Requirements</span></span>



| <span data-ttu-id="96904-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="96904-124">Requirement</span></span> | <span data-ttu-id="96904-125">Valor</span><span class="sxs-lookup"><span data-stu-id="96904-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="96904-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96904-126">Minimum supported client</span></span><br/> | <span data-ttu-id="96904-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="96904-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="96904-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96904-128">Minimum supported server</span></span><br/> | <span data-ttu-id="96904-129">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="96904-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="96904-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="96904-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="96904-131"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="96904-131"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





