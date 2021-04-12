---
title: Controles deslizantes (multimídia do Windows)
description: Controles deslizantes
ms.assetid: cfd82672-5b22-4b59-82b5-15ca68a451fc
keywords:
- mixers de áudio, controles
- mixers de áudio, controles deslizantes
- mixers, controles
- mixers, controles deslizantes
- controles deslizantes
- Estrutura de MIXERCONTROLDETAILS_SIGNED
- controle panorâmico
- Controle de Pan QSound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d1d7644255e2fa9ee6384cbb5102df81c2a1eb0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104369102"
---
# <a name="sliders-windows-multimedia"></a>Controles deslizantes (multimídia do Windows)

Os controles deslizantes geralmente são controles horizontais que podem ser ajustados para a esquerda ou para a direita. Esses controles usam a [**estrutura \_ assinada MIXERCONTROLDETAILS**](/previous-versions//dd757297(v=vs.85)) para recuperar e definir propriedades de controle. A tabela a seguir descreve os tipos de controles deslizantes.



| Control    | Descrição                                                                                                               |
|------------|---------------------------------------------------------------------------------------------------------------------------|
| Controle deslizante     | Tem um intervalo de – 32.768 a 32.767. O driver do mixer define os limites deste controle.                               |
| Panorâmica        | Tem um intervalo de – 32.768 a 32.767. O driver do mixer define os limites desse controle, com 0 como o valor de midrange. |
| Pan QSound | Fornece controle de som expandido por meio de QSound. Esse controle tem um intervalo de – 15 a 15.                               |



 

 

 
