---
title: Listas
description: Listas
ms.assetid: 89fb4457-307a-4693-94d4-57f57c422d1e
keywords:
- mixers de áudio, controles
- mixers de áudio, listas
- mixers, controles
- mixers, listas
- controles de lista
- Estrutura de MIXERCONTROLDETAILS_BOOLEAN
- Estrutura de MIXERCONTROLDETAILS_LISTTEXT
- controle de seleção única
- controle de seleção múltipla
- controle do mixer
- Multiplexador (MUX)
- MUX (multiplexador)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d475816d7090ee241a1508cc054b12742c4ab27
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293941"
---
# <a name="lists"></a>Listas

Os controles de lista fornecem Estados de seleção única ou seleção múltipla para linhas de áudio complexas. Esses controles usam a [**estrutura \_ booliana MIXERCONTROLDETAILS**](/previous-versions//dd757295(v=vs.85)) para recuperar e definir propriedades de controle. A estrutura [**MIXERCONTROLDETAILS \_ LISTTEXT**](/previous-versions//dd757296(v=vs.85)) também é usada para recuperar todas as descrições de texto de um controle de vários itens. A tabela a seguir descreve os tipos de controles de lista.



| Control           | Descrição                                                                                                                                                                                                                                                                      |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Seleção única     | Restringe a seleção de controle para um item por vez. Ao contrário do controle Multiplexador, esse controle pode ser usado para controlar mais do que as linhas de origem de áudio. Por exemplo, você pode usar esse controle para selecionar um filtro de baixa passa de uma lista de filtros com suporte de um dispositivo de mixer. |
| Multiplexador (MUX) | Restringe a seleção de linha a uma linha de origem por vez.                                                                                                                                                                                                                       |
| Seleção múltipla   | Permite que o usuário Selecione vários itens de uma lista simultaneamente. Ao contrário do controle de mixer, o controle de seleção múltipla pode ser usado para controlar mais do que as linhas de origem de áudio.                                                                                                  |
| Mixagem             | Permite que o usuário Selecione linhas de origem de uma lista simultaneamente.                                                                                                                                                                                                               |



 

 

 