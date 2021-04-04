---
title: Mensagem de TBM_GETPTICS (commctrl. h)
description: Recupera o endereço de uma matriz que contém as posições das marcas de escala para um TrackBar.
ms.assetid: d15a4b4d-2ced-40a4-9351-ed7ecc5a5751
keywords:
- Controles de TBM_GETPTICS de mensagens do Windows
topic_type:
- apiref
api_name:
- TBM_GETPTICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d5d81e67156c0118310017413b8e73714246b7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918482"
---
# <a name="tbm_getptics-message"></a><span data-ttu-id="6edb4-104">\_Mensagem tbm GETPTICS</span><span class="sxs-lookup"><span data-stu-id="6edb4-104">TBM\_GETPTICS message</span></span>

<span data-ttu-id="6edb4-105">Recupera o endereço de uma matriz que contém as posições das marcas de escala para um TrackBar.</span><span class="sxs-lookup"><span data-stu-id="6edb4-105">Retrieves the address of an array that contains the positions of the tick marks for a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="6edb4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6edb4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6edb4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6edb4-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6edb4-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="6edb4-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6edb4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6edb4-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6edb4-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="6edb4-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6edb4-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6edb4-111">Return value</span></span>

<span data-ttu-id="6edb4-112">Retorna o endereço de uma matriz de valores **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="6edb4-112">Returns the address of an array of **DWORD** values.</span></span> <span data-ttu-id="6edb4-113">Os elementos da matriz especificam as posições lógicas das marcas de escala do TrackBar, sem incluir as primeiras e as últimas marcas de escala criadas pelo TrackBar.</span><span class="sxs-lookup"><span data-stu-id="6edb4-113">The elements of the array specify the logical positions of the trackbar's tick marks, not including the first and last tick marks created by the trackbar.</span></span> <span data-ttu-id="6edb4-114">As posições lógicas podem ser qualquer um dos valores inteiros na faixa de TrackBar de mínimo para máximo de posições do controle deslizante.</span><span class="sxs-lookup"><span data-stu-id="6edb4-114">The logical positions can be any of the integer values in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="remarks"></a><span data-ttu-id="6edb4-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="6edb4-115">Remarks</span></span>

<span data-ttu-id="6edb4-116">O número de elementos na matriz é dois menores que a contagem de tiques retornada pela mensagem [**tbm \_ GETNUMTICS**](tbm-getnumtics.md) .</span><span class="sxs-lookup"><span data-stu-id="6edb4-116">The number of elements in the array is two less than the tick count returned by the [**TBM\_GETNUMTICS**](tbm-getnumtics.md) message.</span></span> <span data-ttu-id="6edb4-117">Observe que os valores na matriz podem incluir posições duplicadas e podem não estar em ordem sequencial.</span><span class="sxs-lookup"><span data-stu-id="6edb4-117">Note that the values in the array may include duplicate positions and may not be in sequential order.</span></span> <span data-ttu-id="6edb4-118">O ponteiro retornado é válido até que você altere as marcas de escala do TrackBar.</span><span class="sxs-lookup"><span data-stu-id="6edb4-118">The returned pointer is valid until you change the trackbar's tick marks.</span></span>

## <a name="requirements"></a><span data-ttu-id="6edb4-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6edb4-119">Requirements</span></span>



| <span data-ttu-id="6edb4-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6edb4-120">Requirement</span></span> | <span data-ttu-id="6edb4-121">Valor</span><span class="sxs-lookup"><span data-stu-id="6edb4-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6edb4-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6edb4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6edb4-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6edb4-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6edb4-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6edb4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6edb4-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6edb4-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6edb4-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6edb4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6edb4-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6edb4-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





