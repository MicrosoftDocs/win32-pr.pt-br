---
title: Criando assinaturas de evento de hardware
description: Em computadores que têm um BMC (Baseboard Management Controller) instalado, os eventos de hardware são gerados e registrados no SEL (log de eventos do sistema), que é o armazenamento de eventos do BMC armazenado na memória não volátil.
ms.assetid: 646ab546-500e-44ee-8b08-2f835e57e3e6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc5f904e74d1f29b0666c9cb02b13689a0633bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294320"
---
# <a name="creating-hardware-event-subscriptions"></a>Criando assinaturas de evento de hardware

Em computadores que têm um BMC (Baseboard Management Controller) instalado, os eventos de hardware são gerados e registrados no SEL (log de eventos do sistema), que é o armazenamento de eventos do BMC armazenado na memória não volátil. Para ler esses eventos de hardware no Windows Server 2008 usando o Visualizador de Eventos, você deve criar uma assinatura para os eventos. As assinaturas de evento de hardware só funcionarão no Windows Server 2008.

O procedimento a seguir define como criar a assinatura de evento do SEL para recuperar os eventos de hardware:

1.  Salve o XML a seguir em um arquivo. XML (neste exemplo, o arquivo é denominado Wsmanselrg.xml). Esse XML define a assinatura.

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

    

2.  Crie uma assinatura de evento executando o seguinte comando em uma janela de prompt de comando (o programa Wecutil.exe está localizado no diretório% SYSTEMROOT% \\ System32):

    **Wecutil cs** *<path> \\wsmanselrg.xml*

3.  Verifique se a assinatura está ativa executando o seguinte comando em uma janela de prompt de comando:

    **Wecutil gr** *wsmanselrg*

O BMC é um microcontrolador conectado localmente a um servidor. BMCs têm sensores que monitoram o estado físico do servidor e uma conexão de rede separada que pode se comunicar pela rede, mesmo que o servidor esteja offline. Você tem acesso aos dados do BMC por meio do provedor WMI da IPMI (interface de gerenciamento de plataforma inteligente). Para obter mais informações sobre o provedor IPMI, consulte [provedor IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).

O computador deve ter o BMC e o provedor IPMI instalados para que a assinatura de evento funcione. Para computadores em execução no Windows Server 2008, o provedor IPMI é instalado por padrão. Se o BMC não estiver disponível, o driver IPMI não poderá ser instalado e o status do tempo de execução da assinatura sempre exibirá um erro (falha genérica 0x8004001-WMI).

 

 