---
title: Sobre a configuração do Monitor
description: Sobre a configuração do Monitor
ms.assetid: 66345021-41e8-429a-bbf7-a4aa72a57337
keywords:
- monitor,about
- monitor, calibragem de cores
- monitor, ajustando a área de exibição do monitor
- monitorar, salvar configurações do monitor
- monitorar, restaurar as configurações do monitor
- monitor, recursos do fornecedor
- calibragem de cores
- ajustando a área de exibição do monitor
- salvando configurações do monitor
- restaurando configurações do monitor
- recursos do fornecedor
- monitorar configuração, calibragem de cores
- monitorar a configuração, sobre
- monitorar a configuração, ajustar a área de exibição do monitor
- monitorar a configuração, salvar as configurações do monitor
- monitorar a configuração, restaurar as configurações do monitor
- monitorar a configuração, recursos do fornecedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f5f3d8c56521c07d704fe586f486298d0e679d1bfc33e25a29d943aa92dd66e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146179"
---
# <a name="about-monitor-configuration"></a>Sobre a configuração do Monitor

Os usos para as funções de configuração do monitor incluem:

-   Calibragem de cores. Um monitor calibrado corretamente reproduz cores corretamente. Normalmente, um aplicativo de calibragem de cores exibe um padrão de teste e tem controles para alterar uma configuração de monitor. O usuário altera a configuração até que uma condição seja atendida e repete esse processo para cada configuração de monitor até que o monitor seja calibrado.
-   Ajustando a área de exibição do monitor. As funções de configuração do monitor podem ser usadas para alterar o tamanho e a posição da área de exibição de um monitor. Por exemplo, quando um monitor de LCD está conectado a um computador usando um conector análogo, a melhor qualidade de imagem é obtida quando há um mapeamento de um para um entre pixels no buffer de quadros da placa gráfica e pixels no monitor do LCD.
-   Salvando e restaurando as configurações do monitor. Alguns usuários precisam de vários conjuntos de configurações de monitor, pois diferentes cenários exigem configurações de monitor diferentes. Por exemplo, monitorar as configurações ideais para aplicativos da área de trabalho não são ideais para assistir à tv.
-   Usando recursos de monitor específicos do fornecedor. Usando as funções de configuração do monitor, os fabricantes podem criar aplicativos que usam os recursos específicos do fornecedor do monitor.

As funções de configuração do monitor são divididas em funções de alto nível e de baixo nível. As funções de alto nível são mais fáceis de usar do que as funções de baixo nível. Para usar as funções de alto nível, você não precisa saber nada sobre a DDC/CI (Interface de Comando do Canal de Dados de Exibição). No entanto, as funções de alto nível não dão acesso a recursos específicos do fornecedor do monitor.

As funções de baixo nível são um wrapper fino em torno dos comandos DDC/CI. Para usar as funções de baixo nível, você deve estar familiarizado com o padrão DDC/CI e também com o padrão MCCS (Conjunto de Comandos de Controle) do VESA Monitor. Em geral, você deve usar as funções de alto nível, a menos que precise usar recursos que estão disponíveis apenas nas funções de baixo nível.

As funções de configuração do monitor de alto nível são projetadas para que um aplicativo não possa colocar um monitor em um estado inutilizável. As funções de baixo nível podem ser usadas para enviar códigos VCP para o monitor. No entanto, esteja ciente de que alguns códigos VCP podem desabilitar a funcionalidade importante ou colocar o monitor em um estado em que o usuário não possa ver a imagem de exibição. Para obter mais informações, consulte o padrão MCCS (Conjunto de Comandos de Controle) do VESA Monitor.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Monitorar configuração](monitor-configuration.md)
</dt> </dl>

 

 




