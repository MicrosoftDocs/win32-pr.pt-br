---
description: Depois que um driver de dispositivo converteu um arquivo de diário inteiro em comandos de dispositivo bruto, o arquivo dos comandos convertidos é passado de volta para o spooler.
ms.assetid: 149e44d0-052a-48ba-8f65-59eab193c785
title: Monitores de porta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa4b00e4171b3fd6e366a66deae8f5e70578ca92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811555"
---
# <a name="port-monitors"></a>Monitores de porta

Depois que um driver de dispositivo converteu um arquivo de diário inteiro em comandos de dispositivo bruto, o arquivo dos comandos convertidos é passado de volta para o spooler. O spooler envia esses comandos de baixo nível para um monitor. Um monitor de porta é um. dll que passa os comandos de dispositivo brutos pela rede, por meio de uma porta paralela, ou por meio de uma porta serial para o dispositivo de impressora. Monitores de porta personalizados podem ser instalados para dar suporte à passagem de dados de dispositivo por meio de outras portas de comunicação.

Use as funções a seguir para trabalhar com monitores de porta.



| Função                               | Descrição                                                                         |
|----------------------------------------|-------------------------------------------------------------------------------------|
| [**Addmonitor**](addmonitor.md)       | Instala um monitor de porta local e vincula a configuração, os dados e os arquivos de monitoramento. |
| [**DeleteMonitor**](deletemonitor.md) | Remove um monitor de porta adicionado pela função [**addmonitor**](addmonitor.md) .      |
| [**EnumMonitors**](enummonitors.md)   | Enumera os monitores de porta instalados em um servidor especificado.                       |



 

 

 



