---
title: Medidores
description: Medidores
ms.assetid: 11a98d2a-7cdd-4249-bba9-7edc51d7f8b0
keywords:
- mixers de áudio, controles
- mixers de áudio, medidores
- mixers, controles
- mixers, medidores
- controles de medidor
- Estrutura de MIXERCONTROLDETAILS_BOOLEAN
- Estrutura de MIXERCONTROLDETAILS_SIGNED
- Estrutura de MIXERCONTROLDETAILS_UNSIGNED
- Controle booliano
- controle de pico
- controle assinado
- controle não assinado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36f1bebfca22b963e5c1eb6fede3f2786b35199
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104454064"
---
# <a name="meters"></a>Medidores

Os controles de medição medem os dados que passam por uma linha de áudio. Esses controles usam o [**MIXERCONTROLDETAILS \_ booliano**](/previous-versions//dd757295(v=vs.85)), o [**MIXERCONTROLDETAILS \_ assinado**](/previous-versions//dd757297(v=vs.85))e o [**MIXERCONTROLDETAILS estruturas \_ não assinadas**](/previous-versions//dd757298(v=vs.85)) para recuperar e definir propriedades de controle. A tabela a seguir descreve os tipos de medidores.



| Control  | Descrição                                                                                                                                            |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| Boolean  | Mede se um valor inteiro é FALSE/desligado (zero) ou TRUE/ON (diferente de zero).                                                                            |
| Peak     | Mede a deflexão de 0 nas direções positiva e negativa. O intervalo de valores inteiros para o medidor de pico é de – 32.768 a 32.767. |
| Com sinal   | Mede valores inteiros no intervalo de – 231 a (231 – 1). O driver do mixer define os limites desse medidor.                                     |
| Não assinado | Mede valores inteiros no intervalo de 0 a (232 – 1). O driver do mixer define os limites desse medidor.                                        |



 

 

 