---
description: A figura a seguir mostra a relação entre monitores e outros componentes da Monitor de Rede arquitetura.
ms.assetid: cbd6116c-1a95-4ac4-bc79-632ebe198197
title: Monitorar arquitetura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9cd0a099fc1474255b36f1f04d28899b25a527fee19ba1d29434b4692615ab8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119677117"
---
# <a name="monitor-architecture"></a>Monitorar arquitetura

A figura a seguir mostra a relação [*entre monitores*](m.md) e outros componentes da Monitor de Rede arquitetura.

![relação entre monitores e outros componentes do monitor de rede](images/nmarch2.png)

O tráfego de rede é coletado (como quadros individuais) do driver NDIS. O Monitor de Rede driver (Nmnt.sys) encaminha os quadros para um NPP (provedor de pacotes de rede), que, por sua vez, captura os dados no modo em tempo real. O NPP é uma coleção de interfaces COM usadas para capturar dados. Nesse caso, a interface [**IRTC**](irtc.md) é usada para executar uma captura em tempo real.

> [!Note]  
> O NPP é usado para capturas atrasadas e em tempo real. Para capturas atrasadas usadas por especialistas e analisadores, a interface [**IDelaydC**](idelaydc.md) é usada.

 

Em seguida, o monitor examina os dados capturados no modo em tempo real, detectando condições de rede específicas e gerando eventos conforme necessário.

Três outros componentes são usados por aplicativos de monitoramento: a Ferramenta de Controle do Monitor, o MCSVC (Monitor Control Service) e o Visualizador de Eventos:

-   A Ferramenta de Controle do Monitor é usada para gerenciar seus aplicativos de monitoramento. Isso inclui configurar e executar todos os seus aplicativos de monitor.
-   O MCSVC (Monitor Control Service) dispara eventos, fornece um link de comunicação ao WMI para exibição de eventos e coordena o processamento de operações de monitoramento.
-   O Visualizador de Eventos exibe os eventos acionados pelo Serviço de Controle do Monitor.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Imonitor**](imonitor.md)
</dt> <dt>

[**IMonitorEventer**](imonitoreventer.md)
</dt> <dt>

[**IRTC**](irtc.md)
</dt> </dl>

 

 



