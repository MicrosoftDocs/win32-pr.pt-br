---
title: Esmaecimentos
description: Esmaecimentos
ms.assetid: 2ca6be9f-9825-44d9-99c1-abcf6f0b42f7
keywords:
- mixers de áudio, controles
- mixers de áudio, esmaecimentos
- mixers, controles
- mixers, esmaecimentos
- esmaecimentos
- Estrutura de MIXERCONTROLDETAILS_UNSIGNED
- controle de esmaecimento de volume
- controle de esmaecimento de volume baixo
- controle de esmaecimento de volume de agudos
- controle de equalizador gráfico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd2b560b61a694089b947b0cfda7a54b486f1e3a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917200"
---
# <a name="faders"></a>Esmaecimentos

Os controles Fader geralmente são controles verticais que podem ser ajustados ou reduzidos. Esses controles têm uma escala linear e usam a estrutura não [**\_ assinada MIXERCONTROLDETAILS**](/previous-versions//dd757298(v=vs.85)) para recuperar e definir detalhes de controle. A tabela a seguir descreve os tipos de esmaecimentos.



| Control   | Descrição                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Fader     | Controle de esmaecimento geral. O intervalo de valores aceitáveis é de 0 a 65.535.                                                                                                                                                                                                                                                                                                                                       |
| Volume    | Controle de esmaecimento de volume geral. O intervalo de valores aceitáveis é de 0 a 65.535. Para obter informações sobre como alterar esse intervalo, consulte a documentação do seu dispositivo MIXER.                                                                                                                                                                                                                                        |
| Graves      | Controle de esmaecimento de volume baixo. O intervalo de valores aceitáveis é de 0 a 65.535. Os limites da banda de frequência de baixo são específicos de hardware. Para obter informações sobre limites de banda, consulte a documentação do seu dispositivo de mixer.                                                                                                                                                                                      |
| Agudo    | Controle de esmaecimento de volume de agudos. O intervalo de valores aceitáveis é de 0 a 65.535. Os limites da banda de frequência de agudo são específicos de hardware. Para obter informações sobre os limites de banda, consulte a documentação do seu dispositivo de mixer.                                                                                                                                                                              |
| Equalizer | Controle de equalizador gráfico. O intervalo de valores aceitáveis para uma banda do equalizador é de 0 a 65.535. O número de bandas do equalizador e seus limites são específicos de hardware. Para obter informações sobre o equalizador, consulte a documentação do seu dispositivo de mixer. Você pode usar a estrutura [**MIXERCONTROLDETAILS \_ LISTTEXT**](/previous-versions//dd757296(v=vs.85)) para recuperar rótulos de texto para o equalizador. |



 

 

 