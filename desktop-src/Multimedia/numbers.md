---
title: Números (multimídia do Windows)
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
ms.openlocfilehash: f02c4ffd40f1058fae51af3798135840394be918
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104085059"
---
# <a name="numbers-windows-multimedia"></a>Números (multimídia do Windows)

O número de controles permite que o usuário insira dados numéricos associados a uma linha. Os dados numéricos são expressos como inteiros assinados, inteiros não assinados ou valores de número inteiro de decibéis. Esses controles usam as estruturas [**\_ não**](/previous-versions//dd757298(v=vs.85)) [**\_ assinadas MIXERCONTROLDETAILS**](/previous-versions//dd757297(v=vs.85)) e MIXERCONTROLDETAILS para recuperar e definir propriedades de controle. A tabela a seguir descreve os tipos de controles de número.



| Control  | Descrição                                                                                                                         |
|----------|-------------------------------------------------------------------------------------------------------------------------------------|
| Com sinal   | Permite valores inteiros inseridos no intervalo de – 231 a (231 – 1).                                                               |
| Não assinado | Permite valores inteiros inseridos no intervalo de 0 a (232 – 1).                                                                   |
| Decibéi  | Permite que valores de um inteiro decibéi sejam inseridos, em décimos de decibéis. O intervalo de valores para esse controle é de – 32.768 a 32.767. |
| Porcentagem  | Permite que os valores sejam inseridos como porcentagens.                                                                                         |



 

 

 
