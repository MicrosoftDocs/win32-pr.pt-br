---
title: Consultando e definindo o tempo
description: Consultando e definindo o tempo
ms.assetid: 84eba230-88b6-4cba-9e90-ba0b4bcfc691
keywords:
- MIDI (interface digital de instrumento musical), tempo
- MIDI (interface digital de instrumentos musicais), tempo
- Sequenciador MIDI MCI, tempo
- MCI_STATUS comando
- tempo de sequência
- golpe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3927d2f04e1b073b25c262437620325dc5cd040
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637261"
---
# <a name="querying-and-setting-the-tempo"></a>Consultando e definindo o tempo

Para recuperar o tempo de uma sequência, use o [**comando \_ status do MCI**](mci-status.md) e defina o membro **dwItem** da estrutura de [**parâmetros do \_ status \_ do MCI**](mci-status-parms.md) para o \_ tempo de status de Seq MCI \_ \_ . Se o **comando \_ status do MCI** for bem-sucedido, o membro **dwReturn** da **estrutura \_ \_ parâmetros do status do MCI** conterá o tempo atual.

Para alterar o tempo, use o comando [**MCI \_ set**](mci-set.md) com a estrutura [**MCI \_ Seq \_ set \_ parms**](mci-seq-set-parms.md) , especificando o \_ sinalizador MCI Seq \_ set \_ tempo e definindo o membro **dwTempo** da estrutura para o tempo desejado.

A maneira como o tempo é representado depende do tipo de divisão da sequência. Se o tipo de divisão for PPQN, o tempo será representado em batidas por minuto. Se o tipo de divisão for um dos tipos de divisão SMPTE, o tempo será representado em quadros por segundo. Para obter informações sobre como determinar o tipo de divisão de uma sequência, consulte [recuperando o tipo de divisão de sequência](retrieving-the-sequence-division-type.md).

 

 




