---
title: Recuperando o tipo de divisão de sequência
description: Recuperando o tipo de divisão de sequência
ms.assetid: 9c7e3482-93a3-4f9c-8b70-a9c733de14fe
keywords:
- MIDI (interface digital de instrumento musical), tipo de divisão de sequência
- MIDI (interface digital de instrumento musical), tipo de divisão de sequência
- Sequenciador MIDI MCI, tipo de divisão
- MCI_STATUS comando
- tipo de divisão de sequência
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81b28bb7e32097b888cdd3dec739eaccfc2a37dfe14060168fb11f0a7ca3d00e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117801800"
---
# <a name="retrieving-the-sequence-division-type"></a>Recuperando o tipo de divisão de sequência

O *tipo de divisão* de uma sequência MIDI determina a quantidade de tempo entre os eventos de Midi na sequência. Para determinar o tipo de divisão de uma sequência, use o comando [**\_ status do MCI**](mci-status.md) e defina o membro **dwItem** da estrutura de [**\_ \_ parâmetros do status do MCI**](mci-status-parms.md) como DIVTYPE do status do MCI \_ Seq \_ \_ .

Se o **comando \_ status do MCI** for bem-sucedido, o membro **dwReturn** da **estrutura \_ \_ parâmetros do status do MCI** conterá um dos valores a seguir para indicar o tipo de divisão.



| Valor                        | Tipo de divisão                     |
|------------------------------|-----------------------------------|
| MCI \_ Seq \_ div \_ PPQN          | PPQN (observação de partes por trimestre)     |
| MCI \_ Seq \_ div \_ SMPTE \_ 24     | SMPTE, 24 fps (quadros por segundo) |
| MCI \_ Seq \_ div \_ SMPTE \_ 25     | SMPTE, 25 fps                     |
| MCI \_ Seq \_ div \_ SMPTE \_ 30     | SMPTE, 30 fps                     |
| MCI \_ Seq \_ div \_ SMPTE \_ 30DROP | O quadro de soltar de SMPTE, 30 fps          |



 

Você deve saber o tipo de divisão de uma sequência para alterar ou consultar seu tempo. Você não pode alterar o tipo de divisão de uma sequência usando o sequenciador MCI.

 

 




