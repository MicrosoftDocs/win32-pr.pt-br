---
title: Comutadores
description: Comutadores
ms.assetid: ab92d30d-97ab-4229-aed8-1080b6e6dc88
keywords:
- mixers de áudio, controles
- mixers de áudio, comutadores
- mixers, controles
- mixers, comutadores
- alternar controles
- Estrutura de MIXERCONTROLDETAILS_BOOLEAN
- Controle booliano
- controle de botão
- controle ativar/desativar
- controle mono
- controle de intensidade
- controle avançado de estéreo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1d65bb2a14a0e7dc527fab0e628035839855934
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823706"
---
# <a name="switches"></a>Comutadores

Os controles switch são opções de dois Estados. Esses controles usam a [**estrutura \_ booliana MIXERCONTROLDETAILS**](/previous-versions//dd757295(v=vs.85)) para recuperar e definir propriedades de controle. A tabela a seguir descreve os tipos de comutadores.



| Control         | Descrição                                                                                                                                                                                                                           |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Boolean         | A opção genérica. Ele pode ser definido como **true** ou **false**.                                                                                                                                                                           |
| Botão          | Defina como **verdadeiro** para todos os botões que o driver deve manipular, como se eles tivessem sido pressionados. Se o valor for **false**, nenhuma ação será executada.                                                                                         |
| Ativar/desativar          | Um comutador alternativo que é representado por um gráfico diferente daquele usado para a opção booliana. Ele pode ser definido como ON ou OFF.                                                                                                    |
| Mute            | Silencia uma linha de áudio (suprimindo o fluxo de dados da linha) ou permite que os dados de áudio sejam reproduzidos. Essa opção é usada frequentemente para ajudar a controlar as linhas que alimentam o mixer.                                                        |
| Mono            | Alterna entre a saída mono e estéreo para uma linha de áudio estéreo. Defina como desativado para reproduzir dados estéreo como canais separados. Defina como ON para combinar dados de ambos os canais em uma linha de áudio mono.                                            |
| Intensidade        | Aumenta baixo volume baixo para uma linha de áudio. Defina como ativado para impulsionar baixo volume baixo. Defina como desativado para definir os níveis de volume como normal. A quantidade de aumento é específica de hardware. Para obter mais informações, consulte a documentação do seu dispositivo MIXER. |
| Estéreo avançado | Aumenta a separação de estéreo. Defina como ativado para aumentar a separação de estéreo. Defina como desativado para nenhum aprimoramento.                                                                                                                                  |



 

 

 