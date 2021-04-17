---
description: A classe CSystemClock implementa um relógio que retorna a hora do sistema.
ms.assetid: 22f8b641-6472-433f-bff4-4e62eae25c9b
title: Classe CSystemClock
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock
api_type:
- COM
api_location: ''
ms.openlocfilehash: e9cc5e0bde8983cfd8c544d3898d4af628e10f87
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104558531"
---
# <a name="csystemclock-class"></a><span data-ttu-id="09636-103">Classe CSystemClock</span><span class="sxs-lookup"><span data-stu-id="09636-103">CSystemClock class</span></span>

![hierarquia de classe CSystemClock](images/sclock01.png)

<span data-ttu-id="09636-105">A `CSystemClock` classe implementa um relógio que retorna a hora do sistema.</span><span class="sxs-lookup"><span data-stu-id="09636-105">The `CSystemClock` class implements a clock that returns the system time.</span></span>

<span data-ttu-id="09636-106">Essa classe deriva da classe [**CBaseReferenceClock**](cbasereferenceclock.md) e adiciona suporte para as interfaces **IPersist** e [**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust) .</span><span class="sxs-lookup"><span data-stu-id="09636-106">This class derives from the [**CBaseReferenceClock**](cbasereferenceclock.md) class, and adds support for the **IPersist** and [**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust) interfaces.</span></span>



| <span data-ttu-id="09636-107">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="09636-107">Public Methods</span></span>                                        | <span data-ttu-id="09636-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="09636-108">Description</span></span>                                         |
|-------------------------------------------------------|-----------------------------------------------------|
| [<span data-ttu-id="09636-109">**CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="09636-109">**CreateInstance**</span></span>](csystemclock-createinstance.md) | <span data-ttu-id="09636-110">Cria uma nova instância desse objeto.</span><span class="sxs-lookup"><span data-stu-id="09636-110">Creates a new instance of this object.</span></span>              |
| [<span data-ttu-id="09636-111">**CSystemClock**</span><span class="sxs-lookup"><span data-stu-id="09636-111">**CSystemClock**</span></span>](csystemclock-csystemclock.md)     | <span data-ttu-id="09636-112">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="09636-112">Constructor method.</span></span>                                 |
| <span data-ttu-id="09636-113">Métodos IAMClockAdjust</span><span class="sxs-lookup"><span data-stu-id="09636-113">IAMClockAdjust Methods</span></span>                                | <span data-ttu-id="09636-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="09636-114">Description</span></span>                                         |
| [<span data-ttu-id="09636-115">**SetClockDelta**</span><span class="sxs-lookup"><span data-stu-id="09636-115">**SetClockDelta**</span></span>](csystemclock-setclockdelta.md)   | <span data-ttu-id="09636-116">Ajusta a hora do relógio.</span><span class="sxs-lookup"><span data-stu-id="09636-116">Adjusts the clock time.</span></span>                             |
| <span data-ttu-id="09636-117">Métodos IPersist</span><span class="sxs-lookup"><span data-stu-id="09636-117">IPersist Methods</span></span>                                      | <span data-ttu-id="09636-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="09636-118">Description</span></span>                                         |
| [<span data-ttu-id="09636-119">**GetClassID**</span><span class="sxs-lookup"><span data-stu-id="09636-119">**GetClassID**</span></span>](csystemclock-getclassid.md)         | <span data-ttu-id="09636-120">Retorna o identificador de classe (CLSID) do objeto.</span><span class="sxs-lookup"><span data-stu-id="09636-120">Returns the class identifier (CLSID) of the object.</span></span> |



 

 

 



