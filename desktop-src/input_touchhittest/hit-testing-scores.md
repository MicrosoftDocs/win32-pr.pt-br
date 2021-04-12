---
title: Pontuações de teste de colisão de toque
description: As constantes a seguir identificam as possíveis pontuações de teste de clique para um objeto, em relação a outros objetos que interseccionam a área de contato de toque.
ms.assetid: EACDE6DB-ADBD-4F0C-8C31-7321AB6A73EA
topic_type:
- apiref
api_name:
- TOUCH_HIT_TESTING_PROXIMITY_CLOSEST
- TOUCH_HIT_TESTING_PROXIMITY_FARTHEST
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: f6590e7d56c1c9d92f0ff20524b6e4222d8655b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499321"
---
# <a name="touch-hit-testing-scores"></a><span data-ttu-id="1f98f-103">Pontuações de teste de colisão de toque</span><span class="sxs-lookup"><span data-stu-id="1f98f-103">Touch Hit Testing Scores</span></span>

<span data-ttu-id="1f98f-104">As constantes a seguir identificam as possíveis pontuações de teste de clique para um objeto, em relação a outros objetos que interseccionam a área de contato de toque.</span><span class="sxs-lookup"><span data-stu-id="1f98f-104">The following constants identify the possible hit test scores for an object, relative to other objects that intersect the touch contact area.</span></span>

| <span data-ttu-id="1f98f-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="1f98f-105">Constant/value</span></span> | <span data-ttu-id="1f98f-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="1f98f-106">Description</span></span> |
|---|---|
| <span data-ttu-id="1f98f-107">**TOUCH_HIT_TESTING_PROXIMITY_CLOSEST** 0x0</span><span class="sxs-lookup"><span data-stu-id="1f98f-107">**TOUCH_HIT_TESTING_PROXIMITY_CLOSEST** 0x0</span></span>      | <span data-ttu-id="1f98f-108">O objeto é o destino mais provável.</span><span class="sxs-lookup"><span data-stu-id="1f98f-108">The object is the most probable target.</span></span><br/>  |
| <span data-ttu-id="1f98f-109">**TOUCH_HIT_TESTING_PROXIMITY_FARTHEST** 0xFFF</span><span class="sxs-lookup"><span data-stu-id="1f98f-109">**TOUCH_HIT_TESTING_PROXIMITY_FARTHEST** 0xFFF</span></span> | <span data-ttu-id="1f98f-110">O objeto é o destino menos provável.</span><span class="sxs-lookup"><span data-stu-id="1f98f-110">The object is the least probable target.</span></span><br/> |

## <a name="requirements"></a><span data-ttu-id="1f98f-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f98f-111">Requirements</span></span>

| <span data-ttu-id="1f98f-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f98f-112">Requirement</span></span> | <span data-ttu-id="1f98f-113">Valor</span><span class="sxs-lookup"><span data-stu-id="1f98f-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1f98f-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f98f-114">Minimum supported client</span></span><br/> | <span data-ttu-id="1f98f-115">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="1f98f-115">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="1f98f-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f98f-116">Minimum supported server</span></span><br/> | <span data-ttu-id="1f98f-117">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="1f98f-117">None supported</span></span><br/>                                                            |
| <span data-ttu-id="1f98f-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1f98f-118">Header</span></span><br/>                   | <span data-ttu-id="1f98f-119">WinUser. h</span><span class="sxs-lookup"><span data-stu-id="1f98f-119">Winuser.h</span></span> |
