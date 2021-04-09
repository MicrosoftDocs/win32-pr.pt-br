---
title: Mensagem de UDM_SETACCEL (commctrl. h)
description: Define a aceleração para um controle de cima para baixo.
ms.assetid: af1d0a34-13ba-4bda-82f5-d7afab6bb1ed
keywords:
- Controles de UDM_SETACCEL de mensagens do Windows
topic_type:
- apiref
api_name:
- UDM_SETACCEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b43ed290ce1668ffcaa9fb086a99ad52e5129ad6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009765"
---
# <a name="udm_setaccel-message"></a><span data-ttu-id="6db00-104">\_Mensagem de SETACCEL UDM</span><span class="sxs-lookup"><span data-stu-id="6db00-104">UDM\_SETACCEL message</span></span>

<span data-ttu-id="6db00-105">Define a aceleração para um controle de cima para baixo.</span><span class="sxs-lookup"><span data-stu-id="6db00-105">Sets the acceleration for an up-down control.</span></span>

## <a name="parameters"></a><span data-ttu-id="6db00-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6db00-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6db00-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6db00-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6db00-108">Número de estruturas [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) especificadas por *aAccels*.</span><span class="sxs-lookup"><span data-stu-id="6db00-108">Number of [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) structures specified by *aAccels*.</span></span>

</dd> <dt>

<span data-ttu-id="6db00-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6db00-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6db00-110">Ponteiro para uma matriz de estruturas [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) que contêm informações de aceleração.</span><span class="sxs-lookup"><span data-stu-id="6db00-110">Pointer to an array of [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) structures that contain acceleration information.</span></span> <span data-ttu-id="6db00-111">Os elementos devem ser classificados em ordem crescente com base no membro **NSEC** .</span><span class="sxs-lookup"><span data-stu-id="6db00-111">Elements should be sorted in ascending order based on the **nSec** member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6db00-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6db00-112">Return value</span></span>

<span data-ttu-id="6db00-113">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="6db00-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="6db00-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6db00-114">Requirements</span></span>



| <span data-ttu-id="6db00-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6db00-115">Requirement</span></span> | <span data-ttu-id="6db00-116">Valor</span><span class="sxs-lookup"><span data-stu-id="6db00-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6db00-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6db00-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6db00-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6db00-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6db00-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6db00-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6db00-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6db00-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6db00-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6db00-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6db00-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6db00-122"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6db00-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="6db00-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6db00-124">**\_GETACCEL UDM**</span><span class="sxs-lookup"><span data-stu-id="6db00-124">**UDM\_GETACCEL**</span></span>](udm-getaccel.md)
</dt> </dl>

 

 





