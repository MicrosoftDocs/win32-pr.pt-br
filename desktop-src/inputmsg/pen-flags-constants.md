---
title: Sinalizadores de caneta
description: Os valores que podem aparecer no campo penFlags da estrutura de POINTER_PEN_INFO.
ms.assetid: BC3CE568-4090-4451-B780-18530C988305
topic_type:
- apiref
api_name:
- PEN_FLAG_NONE
- PEN_FLAG_BARREL
- PEN_FLAG_INVERTED
- PEN_FLAG_ERASER
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: d7c28beaf58b6fa96bb8dd82b2dd650b2a7d6950
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455557"
---
# <a name="pen-flags"></a><span data-ttu-id="44dfa-103">Sinalizadores de caneta</span><span class="sxs-lookup"><span data-stu-id="44dfa-103">Pen Flags</span></span>

<span data-ttu-id="44dfa-104">Os valores que podem aparecer no campo **penFlags** da estrutura de [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="44dfa-104">Values that can appear in the **penFlags** field of the [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) structure.</span></span>

<dl> <dt>

<span data-ttu-id="44dfa-105"><span id="PEN_FLAG_NONE"></span><span id="pen_flag_none"></span>**PEN_FLAG_NONE**</span><span class="sxs-lookup"><span data-stu-id="44dfa-105"><span id="PEN_FLAG_NONE"></span><span id="pen_flag_none"></span>**PEN_FLAG_NONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44dfa-106">0x00000000</span><span class="sxs-lookup"><span data-stu-id="44dfa-106">0x00000000</span></span>
</dt> <dt>



<span data-ttu-id="44dfa-107">Não há nenhum sinalizador de caneta.</span><span class="sxs-lookup"><span data-stu-id="44dfa-107">There is no pen flag.</span></span> <span data-ttu-id="44dfa-108">Esse é o padrão.</span><span class="sxs-lookup"><span data-stu-id="44dfa-108">This is the default.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44dfa-109"><span id="PEN_FLAG_BARREL"></span><span id="pen_flag_barrel"></span>**PEN_FLAG_BARREL**</span><span class="sxs-lookup"><span data-stu-id="44dfa-109"><span id="PEN_FLAG_BARREL"></span><span id="pen_flag_barrel"></span>**PEN_FLAG_BARREL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44dfa-110">0x00000001</span><span class="sxs-lookup"><span data-stu-id="44dfa-110">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="44dfa-111">O botão de cilindro é pressionado.</span><span class="sxs-lookup"><span data-stu-id="44dfa-111">The barrel button is pressed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44dfa-112"><span id="PEN_FLAG_INVERTED"></span><span id="pen_flag_inverted"></span>**PEN_FLAG_INVERTED**</span><span class="sxs-lookup"><span data-stu-id="44dfa-112"><span id="PEN_FLAG_INVERTED"></span><span id="pen_flag_inverted"></span>**PEN_FLAG_INVERTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44dfa-113">0x00000002</span><span class="sxs-lookup"><span data-stu-id="44dfa-113">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="44dfa-114">A caneta está invertida.</span><span class="sxs-lookup"><span data-stu-id="44dfa-114">The pen is inverted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="44dfa-115"><span id="PEN_FLAG_ERASER"></span><span id="pen_flag_eraser"></span>**PEN_FLAG_ERASER**</span><span class="sxs-lookup"><span data-stu-id="44dfa-115"><span id="PEN_FLAG_ERASER"></span><span id="pen_flag_eraser"></span>**PEN_FLAG_ERASER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44dfa-116">0x00000004</span><span class="sxs-lookup"><span data-stu-id="44dfa-116">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="44dfa-117">O botão de borracha é pressionado.</span><span class="sxs-lookup"><span data-stu-id="44dfa-117">The eraser button is pressed.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="44dfa-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44dfa-118">Requirements</span></span>



| <span data-ttu-id="44dfa-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="44dfa-119">Requirement</span></span> | <span data-ttu-id="44dfa-120">Valor</span><span class="sxs-lookup"><span data-stu-id="44dfa-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="44dfa-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44dfa-121">Minimum supported client</span></span><br/> | <span data-ttu-id="44dfa-122">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="44dfa-122">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="44dfa-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44dfa-123">Minimum supported server</span></span><br/> | <span data-ttu-id="44dfa-124">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="44dfa-124">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="44dfa-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="44dfa-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="44dfa-126"><dt>WinUser. h</dt></span><span class="sxs-lookup"><span data-stu-id="44dfa-126"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44dfa-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="44dfa-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44dfa-128">Constantes</span><span class="sxs-lookup"><span data-stu-id="44dfa-128">Constants</span></span>](constants.md)
</dt> <dt>

[<span data-ttu-id="44dfa-129">**POINTER_INFO**</span><span class="sxs-lookup"><span data-stu-id="44dfa-129">**POINTER_INFO**</span></span>](/previous-versions/windows/desktop/api)
</dt> </dl>

 

 





