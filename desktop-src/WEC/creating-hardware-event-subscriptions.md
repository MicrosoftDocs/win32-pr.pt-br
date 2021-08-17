---
title: Criando assinaturas de evento de hardware
description: Em computadores que têm um BMC (Controlador de Gerenciamento do Baseboard) instalado, os eventos de hardware são gerados e registrados no SEL (log de eventos do sistema), que é o armazenamento de eventos do BMC armazenado na memória não complicada.
ms.assetid: 646ab546-500e-44ee-8b08-2f835e57e3e6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54ee32d590143ed8a1ffacec6f59ad3b3094c2d2a22d0df66b0cb0d3521f83e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117751108"
---
# <a name="creating-hardware-event-subscriptions"></a>Criando assinaturas de evento de hardware

Em computadores que têm um BMC (Controlador de Gerenciamento do Baseboard) instalado, os eventos de hardware são gerados e registrados no SEL (log de eventos do sistema), que é o armazenamento de eventos do BMC armazenado na memória não complicada. Para ler esses eventos de hardware no Windows Server 2008 usando o Visualizador de Eventos, você deve criar uma assinatura para os eventos. As assinaturas de evento de hardware só funcionarão no Windows Server 2008.

O procedimento a seguir define como criar a assinatura de evento SEL para recuperar os eventos de hardware:

1.  Salve o XML a seguir em um .xml arquivo (neste exemplo, o arquivo é chamado Wsmanselrg.xml). Esse XML define a assinatura.

    ```XML
    <Subscription xmlns="http://schemas.microsoft.com/2006/03/windows/events/subscription">
        <Description>A subscription for the HardwareEvents</Description>
        <SubscriptionId>WSManSelRg</SubscriptionId>
        <Uri>http://schemas.microsoft.com/wbem/wsman/1/logrecord/sel</Uri>
        <EventSources>
            <EventSource>
                <Address>LOCALHOST</Address>
            </EventSource>
        </EventSources>
        <LogFile>HardwareEvents</LogFile>
        <Delivery Mode="pull">
            <PushSettings>
                <Heartbeat Interval="10000"/>
            </PushSettings>
        </Delivery>
    </Subscription>
    ```

    

2.  Crie uma assinatura de evento executando o seguinte comando em uma janela de prompt de comando (o programa Wecutil.exe está localizado no diretório %SYSTEMROOT% \\ System32.):

    **Wecutil cs** *<path> \\wsmanselrg.xml*

3.  Verifique se a assinatura está ativa executando o seguinte comando em uma janela de prompt de comando:

    **Wecutil gr** *wsmanselrg*

O BMC é um microcontrolador anexado localmente a um servidor. Os BMCs têm sensores que monitoram o estado físico do servidor e uma conexão de rede separada que pode se comunicar pela rede, mesmo se o servidor estiver offline. Você tem acesso aos dados do BMC por meio do provedor WMI da INTERFACE de Gerenciamento de Plataforma Inteligente (IPMI). Para obter mais informações sobre o provedor IPMI, consulte [Provedor IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).

O computador deve ter o BMC e o provedor IPMI instalados para que a assinatura de evento funcione. Para computadores em execução Windows Server 2008, o provedor IPMI é instalado por padrão. Se o BMC não estiver disponível, o driver IPMI não poderá ser instalado e o status do runtime da assinatura sempre exibirá um erro (0x8004001 – Falha Genérica do WMI).

 

 