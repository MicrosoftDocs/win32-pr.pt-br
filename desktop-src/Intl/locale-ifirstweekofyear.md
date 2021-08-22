---
description: LOCALE \_ IFIRSTWEEKOFYEAR
ms.assetid: 866a28b7-e0b8-4b99-96df-345791a24833
title: LOCALE_IFIRSTWEEKOFYEAR
ms.topic: article
ms.date: 03/04/2020
ms.openlocfilehash: da0d8697e8a02bb6943f4a4154a1ea89c4e01cbaed7576631e3a61d161e80503
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147419"
---
# <a name="locale_ifirstweekofyear"></a>LOCALE \_ IFIRSTWEEKOFYEAR

A primeira semana do ano.



| Valor | Significado                                                                                                                          |
|-------|----------------------------------------------------------------------------------------------------------------------------------|
| 0     | A semana que contém 1/1 é a primeira semana do ano. Observe que isso pode ser um único dia, se 1/1 cair no último dia da semana. |
| 1     | A primeira semana inteira após 1/1 é a primeira semana do ano.                                                                     |
| 2     | A primeira semana que contém pelo menos quatro dias é a primeira semana do ano. Compatível com ISO 8601.                                     |

Se LOCALE_IFIRSTWEEKOFYEAR for 2, LOCALE_IFIRSTDAYOFWEEK será 0 (segunda-feira) e LOCALE_ICALENDARTYPE será gregoriano, a primeira semana seguirá a definição ISO 8601, em que a primeira semana é a semana com a primeira quinta-feira do ano gregoriano.


 

 

 



