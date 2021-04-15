---
title: Sobre a configuração do monitor
description: Sobre a configuração do monitor
ms.assetid: 66345021-41e8-429a-bbf7-a4aa72a57337
keywords:
- monitorar, sobre
- monitor, calibração de cor
- monitor, ajuste da área de exibição do monitor
- monitorar, salvar configurações do monitor
- monitorar, restaurar configurações do monitor
- monitorar, recursos do fornecedor
- calibragem de cores
- ajustando a área de exibição do monitor
- Salvando configurações do monitor
- Restaurando configurações do monitor
- recursos do fornecedor
- configuração do monitor, calibragem de cores
- monitorar a configuração, sobre
- configuração do monitor, ajuste da área de exibição do monitor
- configuração do monitor, salvando configurações do monitor
- configuração do monitor, Restaurando configurações do monitor
- configuração do monitor, recursos do fornecedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60d8e2f3d463bc84acaf8b48f493f5a0118976ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498675"
---
# <a name="about-monitor-configuration"></a>Sobre a configuração do monitor

Os usos para as funções de configuração do monitor incluem:

-   Calibragem de cor. Um monitor calibrado corretamente reproduz cores corretamente. Normalmente, um aplicativo de calibragem de cor exibe um padrão de teste e tem controles para alterar uma configuração de monitor. O usuário altera a configuração até que uma condição seja atendida e repete esse processo para cada configuração de monitor até que o monitor seja calibrado.
-   Ajustando a área de exibição do monitor. As funções de configuração do monitor podem ser usadas para alterar o tamanho e a posição da área de exibição de um monitor. Por exemplo, quando um monitor de LCD está conectado a um computador usando um conector analógico, a melhor qualidade de imagem é obtida quando há um mapeamento de um para um entre pixels no buffer de quadro da placa gráfica e pixels no monitor LCD.
-   Salvando e restaurando configurações do monitor. Alguns usuários precisam de vários conjuntos de configurações de monitor, pois diferentes cenários exigem configurações de monitor diferentes. Por exemplo, as configurações de monitor ideais para aplicativos de área de trabalho não são ideais para assistir à televisão.
-   Usando recursos de monitor específicos do fornecedor. Usando as funções de configuração do monitor, os fabricantes podem criar aplicativos que usam os recursos específicos do fornecedor do monitor.

As funções de configuração do monitor são divididas em funções de alto nível e de nível baixo. As funções de alto nível são mais fáceis de usar do que as funções de nível inferior. Para usar as funções de alto nível, você não precisa saber nada sobre a interface de comando de canal de dados de exibição (DDC/CI). No entanto, as funções de alto nível não oferecem acesso a recursos específicos do fornecedor do monitor.

As funções de nível baixo são um wrapper fino em volta dos comandos DDC/CI. Para usar as funções de nível inferior, você deve estar familiarizado com o padrão DDC/CI e também com o padrão MCCS (VESA monitor Control Set). Em geral, você deve usar as funções de alto nível, a menos que precise usar recursos que estão disponíveis apenas nas funções de nível baixo.

As funções de configuração de monitor de alto nível são projetadas para que um aplicativo não possa colocar um monitor em um estado inutilizável. As funções de nível baixo podem ser usadas para enviar códigos VCP ao monitor. No entanto, lembre-se de que alguns códigos de VCP podem desabilitar a funcionalidade importante ou colocar o monitor em um estado em que o usuário não consegue ver a imagem de exibição. Para obter mais informações, consulte o padrão do conjunto de comandos do controle de monitor VESA (MCCS).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configuração do monitor](monitor-configuration.md)
</dt> </dl>

 

 




