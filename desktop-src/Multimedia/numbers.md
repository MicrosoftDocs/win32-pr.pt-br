---
title: números (Windows multimídia)
description: Números
ms.assetid: d416c4c2-a3e1-45a2-9ae1-82050a5e471b
keywords:
- mixers de áudio, controles
- mixers de áudio, números
- mixers, controles
- mixers, números
- controles de número
- Estrutura de MIXERCONTROLDETAILS_SIGNED
- Estrutura de MIXERCONTROLDETAILS_UNSIGNED
- controle decibéi
- controle de porcentagem
- controle assinado
- controle não assinado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21c9e1bacdea3f52129d78eea2f0bc7134df08b7077c83510bd8de824777e524
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806616"
---
# <a name="numbers-windows-multimedia"></a>números (Windows multimídia)

O número de controles permite que o usuário insira dados numéricos associados a uma linha. Os dados numéricos são expressos como inteiros assinados, inteiros não assinados ou valores de número inteiro de decibéis. Esses controles usam as estruturas [**\_ não**](/previous-versions//dd757298(v=vs.85)) [**\_ assinadas MIXERCONTROLDETAILS**](/previous-versions//dd757297(v=vs.85)) e MIXERCONTROLDETAILS para recuperar e definir propriedades de controle. A tabela a seguir descreve os tipos de controles de número.



| Control  | Descrição                                                                                                                         |
|----------|-------------------------------------------------------------------------------------------------------------------------------------|
| Com sinal   | Permite valores inteiros inseridos no intervalo de – 231 a (231 – 1).                                                               |
| Não assinado | Permite valores inteiros inseridos no intervalo de 0 a (232 – 1).                                                                   |
| Decibéi  | Permite que valores de um inteiro decibéi sejam inseridos, em décimos de decibéis. O intervalo de valores para esse controle é de – 32.768 a 32.767. |
| Porcentagem  | Permite que os valores sejam inseridos como porcentagens.                                                                                         |



 

 

 
