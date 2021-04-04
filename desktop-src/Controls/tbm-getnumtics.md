---
title: Mensagem de TBM_GETNUMTICS (commctrl. h)
description: Recupera o número de marcas de escala em um TrackBar.
ms.assetid: 3c3f7ebb-a544-474c-ba14-68eae543ee38
keywords:
- Controles de TBM_GETNUMTICS de mensagens do Windows
topic_type:
- apiref
api_name:
- TBM_GETNUMTICS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 712e1a0190334ec279f28a68959f3e3d5d5ffd1d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918162"
---
# <a name="tbm_getnumtics-message"></a><span data-ttu-id="26abf-104">\_Mensagem tbm GETNUMTICS</span><span class="sxs-lookup"><span data-stu-id="26abf-104">TBM\_GETNUMTICS message</span></span>

<span data-ttu-id="26abf-105">Recupera o número de marcas de escala em um TrackBar.</span><span class="sxs-lookup"><span data-stu-id="26abf-105">Retrieves the number of tick marks in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="26abf-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="26abf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26abf-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="26abf-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="26abf-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="26abf-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="26abf-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="26abf-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="26abf-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="26abf-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26abf-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="26abf-111">Return value</span></span>

<span data-ttu-id="26abf-112">Se nenhum [sinalizador de tique](trackbar-control-styles.md) for definido, ele retornará 2 para os tiques inicial e final.</span><span class="sxs-lookup"><span data-stu-id="26abf-112">If no [tick flag](trackbar-control-styles.md) is set, it returns 2 for the beginning and ending ticks.</span></span> <span data-ttu-id="26abf-113">Se o [**TBS \_ notiques**](trackbar-control-styles.md) for definido, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="26abf-113">If [**TBS\_NOTICKS**](trackbar-control-styles.md) is set, it returns zero.</span></span> <span data-ttu-id="26abf-114">Caso contrário, ele usa a diferença entre o intervalo mínimo e o máximo, divide pela frequência de tique e adiciona 2.</span><span class="sxs-lookup"><span data-stu-id="26abf-114">Otherwise, it takes the difference between the range minimum and maximum, divides by the tick frequency, and adds 2.</span></span>

## <a name="remarks"></a><span data-ttu-id="26abf-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="26abf-115">Remarks</span></span>

<span data-ttu-id="26abf-116">A mensagem **tbm \_ GETNUMTICS** conta todas as marcas de escala, incluindo as primeiras e as últimas marcas de escala criadas pelo TrackBar.</span><span class="sxs-lookup"><span data-stu-id="26abf-116">The **TBM\_GETNUMTICS** message counts all of the tick marks, including the first and last tick marks created by the trackbar.</span></span>

## <a name="requirements"></a><span data-ttu-id="26abf-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26abf-117">Requirements</span></span>



| <span data-ttu-id="26abf-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="26abf-118">Requirement</span></span> | <span data-ttu-id="26abf-119">Valor</span><span class="sxs-lookup"><span data-stu-id="26abf-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="26abf-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="26abf-120">Minimum supported client</span></span><br/> | <span data-ttu-id="26abf-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="26abf-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="26abf-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="26abf-122">Minimum supported server</span></span><br/> | <span data-ttu-id="26abf-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="26abf-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="26abf-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="26abf-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="26abf-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="26abf-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





