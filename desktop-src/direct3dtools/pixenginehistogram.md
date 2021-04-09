---
description: Representa um histograma de uma textura.
MS-HAID: vspixengine.PixEngineHistogram
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estrutura PixEngineHistogram
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: FC720568-6C8E-4B14-BCB1-5FA14D32C785
api_name:
- PixEngineHistogram
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c19b77c962121949cc2495170061fee3adcecfc7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087660"
---
# <a name="span-idvspixenginepixenginehistogramspanpixenginehistogram-structure"></a><span data-ttu-id="fef9d-103"><span id="vspixengine.pixenginehistogram"></span>Estrutura PixEngineHistogram</span><span class="sxs-lookup"><span data-stu-id="fef9d-103"><span id="vspixengine.pixenginehistogram"></span>PixEngineHistogram structure</span></span>

<span data-ttu-id="fef9d-104">Representa um histograma de uma textura.</span><span class="sxs-lookup"><span data-stu-id="fef9d-104">Represents a histogram of a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="fef9d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fef9d-105">Syntax</span></span>


```C++
} PixEngineHistogram;
```

## <a name="members"></a><span data-ttu-id="fef9d-106">Membros</span><span class="sxs-lookup"><span data-stu-id="fef9d-106">Members</span></span>

<span data-ttu-id="fef9d-107">**horizontalMin**</span><span class="sxs-lookup"><span data-stu-id="fef9d-107">**horizontalMin**</span></span>  
<span data-ttu-id="fef9d-108">Os valores mínimos para cada um dos componentes X, Y, Z e W no eixo horizontal (domínio) do histograma.</span><span class="sxs-lookup"><span data-stu-id="fef9d-108">The minimum values for each of the X, Y, Z, and W components in the horizontal axis (domain) of the histogram.</span></span>

<span data-ttu-id="fef9d-109">**horizontalMax**</span><span class="sxs-lookup"><span data-stu-id="fef9d-109">**horizontalMax**</span></span>  
<span data-ttu-id="fef9d-110">Os valores máximos para cada um dos componentes X, Y, Z e W no eixo horizontal (domínio) do histograma.</span><span class="sxs-lookup"><span data-stu-id="fef9d-110">The maximum values for each of the X, Y, Z, and W components in the horizontal axis (domain) of the histogram.</span></span>

<span data-ttu-id="fef9d-111">**verticalMin**</span><span class="sxs-lookup"><span data-stu-id="fef9d-111">**verticalMin**</span></span>  
<span data-ttu-id="fef9d-112">Os valores mínimos para cada um dos componentes X, Y, Z e W no eixo vertical (intervalo) do histograma.</span><span class="sxs-lookup"><span data-stu-id="fef9d-112">The minimum values for each of the X, Y, Z, and W components in the vertical axis (range) of the histogram.</span></span>

<span data-ttu-id="fef9d-113">**verticalMax**</span><span class="sxs-lookup"><span data-stu-id="fef9d-113">**verticalMax**</span></span>  
<span data-ttu-id="fef9d-114">Os valores máximos para cada um dos componentes X, Y, Z e W no eixo vertical (intervalo) do histograma.</span><span class="sxs-lookup"><span data-stu-id="fef9d-114">The maximum values for each of the X, Y, Z, and W components in the vertical axis (range) of the histogram.</span></span>

<span data-ttu-id="fef9d-115">**dataLength**</span><span class="sxs-lookup"><span data-stu-id="fef9d-115">**dataLength**</span></span>  
<span data-ttu-id="fef9d-116">O número de amostras consideradas no histograma.</span><span class="sxs-lookup"><span data-stu-id="fef9d-116">The number of samples considered in the histogram.</span></span>

## <a name="requirements"></a><span data-ttu-id="fef9d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fef9d-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="fef9d-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fef9d-118">Header</span></span></p></td><td><span data-ttu-id="fef9d-119">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="fef9d-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



