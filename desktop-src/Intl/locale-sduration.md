---
description: SDURATION de localidade \_
ms.assetid: 45ffd7ed-f964-4948-8679-cf960b5c1e0e
title: LOCALE_SDURATION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acb7031c5e9ddc3173fe7f10117eaad8c72820b1d3b81a82da33f6541901a933
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147359"
---
# <a name="locale_sduration"></a>SDURATION de localidade \_

**Windows Vista e posterior:** Formato de duração de tempo composto por imagens de formato listadas na tabela a seguir. O formato é semelhante ao formato para [ \_ STIMEFORMAT de localidade](locale-stime-constants.md). Como para STIMEFORMAT de localidade \_ , esse formato também pode incluir qualquer cadeia de caracteres entre aspas simples. Os formatos podem incluir, por exemplo, "h:mm: SS" ou "d ' s h'h ' s'. FFF '". Em comparação com a localidade \_ STIMEFORMAT, há imagens de formato adicionais para frações de um segundo. Como esse formato é para duração, não para tempo, ele não especifica um sistema de relógio de 12 ou 24 horas, ou inclui um indicador AM/PM. Essa constante pode ser usada, por exemplo, para um aplicativo de várias mídias que exibe a hora do arquivo ou um aplicativo de evento esportivo que exibe horários de término.



| Valor | Significado                                                                                                                                                                                                                             |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| h     | Horas sem zeros à esquerda para horas de dígito único                                                                                                                                                                                  |
| hh    | Horas com zeros à esquerda para horas de dígito único                                                                                                                                                                                     |
| m     | Minutos sem zeros à esquerda para minutos de dígito único                                                                                                                                                                              |
| MM    | Minutos com zeros à esquerda para minutos de dígito único                                                                                                                                                                                 |
| s     | Segundos sem zeros à esquerda para segundos de dígito único                                                                                                                                                                              |
| ss    | Segundos com zeros à esquerda para segundos de dígito único                                                                                                                                                                                 |
| f     | Décimos de segundo                                                                                                                                                                                                                  |
| ff    | Centésimos de segundo                                                                                                                                                                                                              |
| fff   | Milésimos de segundo; o caractere "f" pode ocorrer até nove horários consecutivos (fffffffff), embora o suporte para temporizadores de frequência seja limitado a 100 nanossegundos; Se houver nove caracteres, os dois últimos dígitos serão sempre zero |



 

 

 



