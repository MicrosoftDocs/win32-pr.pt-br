---
description: O tipo de dados de tempo de referência \_ define as unidades para os tempos de referência no DirectShow. Cada unidade de tempo de referência é de 100 nanossegundos.
ms.assetid: 862c95bc-2e0a-42c0-b907-45f64f27bd41
title: REFERENCE_TIME (Strmif. h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab88576f611674f5b208c5c39d328c77dcf57aec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812972"
---
# <a name="reference_time"></a><span data-ttu-id="ccac1-104">hora de referência \_</span><span class="sxs-lookup"><span data-stu-id="ccac1-104">REFERENCE\_TIME</span></span>

<span data-ttu-id="ccac1-105">O tipo de dados de **\_ tempo de referência** define as unidades para os tempos de referência no DirectShow.</span><span class="sxs-lookup"><span data-stu-id="ccac1-105">The **REFERENCE\_TIME** data type defines the units for reference times in DirectShow.</span></span> <span data-ttu-id="ccac1-106">Cada unidade de tempo de referência é de 100 nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="ccac1-106">Each unit of reference time is 100 nanoseconds.</span></span>


```C++
typedef LONGLONG REFERENCE_TIME;
```



## <a name="remarks"></a><span data-ttu-id="ccac1-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="ccac1-107">Remarks</span></span>

<span data-ttu-id="ccac1-108">O tipo de dados de **\_ tempo de referência** é um inteiro de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="ccac1-108">The **REFERENCE\_TIME** data type is a 64-bit integer.</span></span>

<span data-ttu-id="ccac1-109">Os tempos de referência geralmente são medidos a partir de uma das seguintes linhas de base:</span><span class="sxs-lookup"><span data-stu-id="ccac1-109">Reference times are usually measured from one of the following baselines:</span></span>

-   <span data-ttu-id="ccac1-110">Um tempo de relógio absoluto.</span><span class="sxs-lookup"><span data-stu-id="ccac1-110">An absolute clock time.</span></span> <span data-ttu-id="ccac1-111">Nesse caso, a linha de base dependerá da implementação do relógio.</span><span class="sxs-lookup"><span data-stu-id="ccac1-111">In this case, the baseline will depend on the implementation of the clock.</span></span> <span data-ttu-id="ccac1-112">Para obter mais informações, consulte [relógios de referência](reference-clocks.md).</span><span class="sxs-lookup"><span data-stu-id="ccac1-112">For more information, see [Reference Clocks](reference-clocks.md).</span></span>
-   <span data-ttu-id="ccac1-113">Em relação ao início da reprodução.</span><span class="sxs-lookup"><span data-stu-id="ccac1-113">Relative to the start of playback.</span></span>

<span data-ttu-id="ccac1-114">Para obter mais informações sobre os tempos de referência, consulte [tempo e relógios no DirectShow](time-and-clocks-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="ccac1-114">For more information about reference times, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ccac1-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ccac1-115">Requirements</span></span>



| <span data-ttu-id="ccac1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccac1-116">Requirement</span></span> | <span data-ttu-id="ccac1-117">Valor</span><span class="sxs-lookup"><span data-stu-id="ccac1-117">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccac1-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ccac1-118">Header</span></span><br/> | <dl> <span data-ttu-id="ccac1-119"><dt>Strmif. h (incluir DShow. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ccac1-119"><dt>Strmif.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccac1-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="ccac1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccac1-121">Tipos de dados do DirectShow</span><span class="sxs-lookup"><span data-stu-id="ccac1-121">DirectShow Data Types</span></span>](directshow-data-types.md)
</dt> </dl>

 

 




