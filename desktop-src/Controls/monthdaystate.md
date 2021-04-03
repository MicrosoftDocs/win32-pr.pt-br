---
title: MONTHDAYSTATE
description: O tipo de dados MONTHDAYSTATE é um campo de bits que contém o estado de cada dia em um mês.
ms.assetid: eb3dd6cb-738e-424b-945b-1485798a444c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2286482460ec87982c46a564e8441edd9bf7bb43
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822309"
---
# <a name="monthdaystate"></a><span data-ttu-id="2ecfc-103">MONTHDAYSTATE</span><span class="sxs-lookup"><span data-stu-id="2ecfc-103">MONTHDAYSTATE</span></span>

<span data-ttu-id="2ecfc-104">O tipo de dados MONTHDAYSTATE é um campo de bits que contém o estado de cada dia em um mês.</span><span class="sxs-lookup"><span data-stu-id="2ecfc-104">The MONTHDAYSTATE data type is a bitfield that holds the state of each day in a month.</span></span> <span data-ttu-id="2ecfc-105">O tipo de dados é definido em commctrl. h da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="2ecfc-105">The data type is defined in Commctrl.h as follows:</span></span>


```
typedef DWORD MONTHDAYSTATE, *LPMONTHDAYSTATE;
```



<span data-ttu-id="2ecfc-106">Cada bit (0 a 30) representa o estado de um dia em um mês.</span><span class="sxs-lookup"><span data-stu-id="2ecfc-106">Each bit (0 through 30) represents the state of a day in a month.</span></span> <span data-ttu-id="2ecfc-107">Se um bit for on, o dia correspondente será exibido em negrito; caso contrário, ele será exibido sem ênfase.</span><span class="sxs-lookup"><span data-stu-id="2ecfc-107">If a bit is on, the corresponding day will be displayed in bold; otherwise it will be displayed with no emphasis.</span></span>

<span data-ttu-id="2ecfc-108">Esse tipo de dados é usado com a mensagem [**MCM \_ SETDAYSTATE**](mcm-setdaystate.md) e a macro correspondente, [**calendário mensal \_ SETDAYSTATE**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate).</span><span class="sxs-lookup"><span data-stu-id="2ecfc-108">This data type is used with the [**MCM\_SETDAYSTATE**](mcm-setdaystate.md) message and the corresponding macro, [**MonthCal\_SetDayState**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate).</span></span> <span data-ttu-id="2ecfc-109">Quando os valores de MONTHDAYSTATE são usados em referência a meses menores que 31 dias, somente os bits necessários serão acessados.</span><span class="sxs-lookup"><span data-stu-id="2ecfc-109">When MONTHDAYSTATE values are used in reference to months shorter than 31 days, only the needed bits will be accessed.</span></span>

<span data-ttu-id="2ecfc-110">Esse tipo de dados foi definido pela primeira vez na [versão 4,70](common-control-versions.md) de Comctl32.dll.</span><span class="sxs-lookup"><span data-stu-id="2ecfc-110">This data type was first defined in [Version 4.70](common-control-versions.md) of Comctl32.dll.</span></span>

 

 




