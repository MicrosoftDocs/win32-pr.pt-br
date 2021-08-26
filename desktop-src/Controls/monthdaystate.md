---
title: MONTHDAYSTATE
description: O tipo de dados MONTHDAYSTATE é um campo de bits que contém o estado de cada dia em um mês.
ms.assetid: eb3dd6cb-738e-424b-945b-1485798a444c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4e21eed1293a53bce8f38f5bd4db09b8cbe3fbf649fb07348a5dca65e908727
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079856"
---
# <a name="monthdaystate"></a>MONTHDAYSTATE

O tipo de dados MONTHDAYSTATE é um campo de bits que contém o estado de cada dia em um mês. O tipo de dados é definido em commctrl. h da seguinte maneira:


```
typedef DWORD MONTHDAYSTATE, *LPMONTHDAYSTATE;
```



Cada bit (0 a 30) representa o estado de um dia em um mês. Se um bit for on, o dia correspondente será exibido em negrito; caso contrário, ele será exibido sem ênfase.

Esse tipo de dados é usado com a mensagem [**MCM \_ SETDAYSTATE**](mcm-setdaystate.md) e a macro correspondente, [**calendário mensal \_ SETDAYSTATE**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate). Quando os valores de MONTHDAYSTATE são usados em referência a meses menores que 31 dias, somente os bits necessários serão acessados.

Esse tipo de dados foi definido pela primeira vez na [versão 4,70](common-control-versions.md) de Comctl32.dll.

 

 




