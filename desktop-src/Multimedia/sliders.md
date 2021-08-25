---
title: controles deslizantes (Windows multimídia)
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
ms.openlocfilehash: 6e902e3ead0416cb4b2a7d56d289f91779563109cb9494784635affc75069dfe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805346"
---
# <a name="sliders-windows-multimedia"></a>controles deslizantes (Windows multimídia)

Os controles deslizantes geralmente são controles horizontais que podem ser ajustados para a esquerda ou para a direita. Esses controles usam a [**estrutura \_ assinada MIXERCONTROLDETAILS**](/previous-versions//dd757297(v=vs.85)) para recuperar e definir propriedades de controle. A tabela a seguir descreve os tipos de controles deslizantes.



| Control    | Descrição                                                                                                               |
|------------|---------------------------------------------------------------------------------------------------------------------------|
| Controle deslizante     | Tem um intervalo de – 32.768 a 32.767. O driver do mixer define os limites deste controle.                               |
| Panorâmica        | Tem um intervalo de – 32.768 a 32.767. O driver do mixer define os limites desse controle, com 0 como o valor de midrange. |
| Pan QSound | Fornece controle de som expandido por meio de QSound. Esse controle tem um intervalo de – 15 a 15.                               |



 

 

 
