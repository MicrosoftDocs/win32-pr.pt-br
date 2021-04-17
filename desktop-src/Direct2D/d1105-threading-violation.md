---
title: Violação de Threading D1105
ms.assetid: 2c6cf90b-ce9e-4ea9-849d-22170f65ffb0
description: Uma interface segmentada de aluguel foi acessada simultaneamente de vários threads.
keywords:
- D1105 de violação de Threading Direct2D
topic_type:
- apiref
api_name:
- D1105 Threading Violation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: fe83baa32be8ae18948ae5a80e3e0b218cd4fa4a
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/27/2021
ms.locfileid: "105749171"
---
# <a name="d1105-threading-violation"></a><span data-ttu-id="b217b-104">D1105: violação de Threading</span><span class="sxs-lookup"><span data-stu-id="b217b-104">D1105: Threading Violation</span></span>

<span data-ttu-id="b217b-105">Uma interface de interface threadada \[  \] de aluguel foi acessada simultaneamente de vários threads.</span><span class="sxs-lookup"><span data-stu-id="b217b-105">A rental threaded interface \[*interface*\] was simultaneously accessed from multiple threads.</span></span>

## <a name="placeholders"></a><span data-ttu-id="b217b-106">Espaços reservados</span><span class="sxs-lookup"><span data-stu-id="b217b-106">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="b217b-107"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span><span class="sxs-lookup"><span data-stu-id="b217b-107"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span></span>
</dt> <dd>

<span data-ttu-id="b217b-108">O endereço da interface que foi acessada por vários threads.</span><span class="sxs-lookup"><span data-stu-id="b217b-108">The address of the interface that was accessed by multiple threads.</span></span>

</dd> </dl> 




 

## <a name="possible-causes"></a><span data-ttu-id="b217b-109">Possíveis causas</span><span class="sxs-lookup"><span data-stu-id="b217b-109">Possible Causes</span></span>

<span data-ttu-id="b217b-110">Usando uma instância de objeto da mesma fábrica de thread único de dois threads diferentes.</span><span class="sxs-lookup"><span data-stu-id="b217b-110">Using an object instance from the same single-threaded factory from two different threads.</span></span>

 

 




