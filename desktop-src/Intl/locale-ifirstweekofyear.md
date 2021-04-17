---
description: IFIRSTWEEKOFYEAR de localidade \_
ms.assetid: 866a28b7-e0b8-4b99-96df-345791a24833
title: LOCALE_IFIRSTWEEKOFYEAR
ms.topic: article
ms.date: 03/04/2020
ms.openlocfilehash: 7f391fb167a9362fc8770bbcc5a495170148b489
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "105751464"
---
# <a name="locale_ifirstweekofyear"></a>IFIRSTWEEKOFYEAR de localidade \_

A primeira semana do ano.



| Valor | Significado                                                                                                                          |
|-------|----------------------------------------------------------------------------------------------------------------------------------|
| 0     | A semana que contém 1/1 é a primeira semana do ano. Observe que isso pode ser um único dia, se 1/1 estiver no último dia da semana. |
| 1     | A primeira semana completa após 1/1 é a primeira semana do ano.                                                                     |
| 2     | A primeira semana que contém pelo menos quatro dias é a primeira semana do ano. ISO 8601 compatível.                                     |

Se LOCALE_IFIRSTWEEKOFYEAR for 2, LOCALE_IFIRSTDAYOFWEEK for 0 (segunda-feira) e LOCALE_ICALENDARTYPE for Gregoriano, a primeira semana seguirá a definição de ISO 8601, na qual a primeira semana é a semana com a primeira quinta-feira do ano gregoriano.


 

 

 



