---
description: Depois que um driver de dispositivo converteu um arquivo de diário inteiro em comandos de dispositivo bruto, o arquivo dos comandos convertidos é passado de volta para o spooler.
ms.assetid: 149e44d0-052a-48ba-8f65-59eab193c785
title: Monitores de porta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8334da48fb147a41924be2cf090f55d7955cb1d7913c43b302a312fd4447602f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118470926"
---
# <a name="port-monitors"></a>Monitores de porta

Depois que um driver de dispositivo converteu um arquivo de diário inteiro em comandos de dispositivo bruto, o arquivo dos comandos convertidos é passado de volta para o spooler. O spooler envia esses comandos de baixo nível para um monitor. Um monitor de porta é um .dll que passa os comandos de dispositivo brutos pela rede, por meio de uma porta paralela, ou por meio de uma porta serial para o dispositivo de impressora. Monitores de porta personalizados podem ser instalados para dar suporte à passagem de dados de dispositivo por meio de outras portas de comunicação.

Use as funções a seguir para trabalhar com monitores de porta.



| Função                               | Descrição                                                                         |
|----------------------------------------|-------------------------------------------------------------------------------------|
| [**Addmonitor**](addmonitor.md)       | Instala um monitor de porta local e vincula a configuração, os dados e os arquivos de monitoramento. |
| [**DeleteMonitor**](deletemonitor.md) | Remove um monitor de porta adicionado pela função [**addmonitor**](addmonitor.md) .      |
| [**EnumMonitors**](enummonitors.md)   | Enumera os monitores de porta instalados em um servidor especificado.                       |



 

 

 



