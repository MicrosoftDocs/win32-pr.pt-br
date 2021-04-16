---
description: A figura a seguir mostra a relação entre monitores e outros componentes da arquitetura de Monitor de Rede.
ms.assetid: cbd6116c-1a95-4ac4-bc79-632ebe198197
title: Arquitetura do monitor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38c1a36ef19933d888f27079d8d94ddba16bde79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104567852"
---
# <a name="monitor-architecture"></a>Arquitetura do monitor

A figura a seguir mostra a relação entre [*monitores*](m.md) e outros componentes da arquitetura de monitor de rede.

![relação entre monitores e outros componentes do monitor de rede](images/nmarch2.png)

O tráfego de rede é coletado (como quadros individuais) do driver NDIS. O driver de Monitor de Rede (Nmnt.sys), em seguida, roteia os quadros para um NPP (provedor de pacotes de rede) que, por sua vez, captura os dados em modo em tempo real. O NPP é uma coleção de interfaces COM usadas para capturar dados. Nesse caso, a interface [**IRTC**](irtc.md) é usada para executar uma captura em tempo real.

> [!Note]  
> O NPP é usado para capturas atrasadas e em tempo real. Para capturas atrasadas usadas por especialistas e analisadores, a interface [**IDelaydC**](idelaydc.md) é usada.

 

Em seguida, o monitor examina os dados capturados no modo em tempo real, detectando condições de rede específicas e gerando eventos conforme necessário.

Três outros componentes são usados por aplicativos de monitor: a ferramenta de controle de monitor, o serviço de controle de monitor (MCSVC) e o Visualizador de Eventos:

-   A ferramenta de controle de monitor é usada para gerenciar seus aplicativos de monitor. Isso inclui a configuração e a execução de todos os seus aplicativos de monitor.
-   O serviço de controle de monitor (MCSVC) dispara eventos, fornece um link de comunicações para o WMI para exibição de eventos e coordena o processamento de operações de monitor.
-   O Visualizador de Eventos exibe os eventos acionados pelo serviço de controle de monitor.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IMonitor**](imonitor.md)
</dt> <dt>

[**IMonitorEventer**](imonitoreventer.md)
</dt> <dt>

[**IRTC**](irtc.md)
</dt> </dl>

 

 



