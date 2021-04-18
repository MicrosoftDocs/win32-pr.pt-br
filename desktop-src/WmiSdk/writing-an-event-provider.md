---
description: Um provedor de eventos é um objeto COM que fornece ao WMI notificações de eventos intrínsecos e extrínsecos.
ms.assetid: 075bdc65-4ea3-4f91-9823-1d2d0dc13423
ms.tgt_platform: multiple
title: Escrevendo um provedor de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb118d89f214e9fc651c1c9d93abfcfe43f49fc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812060"
---
# <a name="writing-an-event-provider"></a>Escrevendo um provedor de eventos

Um provedor de eventos é um objeto COM que fornece ao WMI notificações de eventos intrínsecos e extrínsecos. Um evento intrínseco relata uma alteração de dados interna ao WMI, enquanto um evento extrínsecos relata um evento definido pelo usuário não descrito por um evento intrínseco. Por exemplo, um evento em resposta a alterações, criação ou exclusão da classe do [**disco \_ lógico do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) seria classificado como um evento intrínseco. Um evento que é gerado com base em algo diferente da modificação, criação ou exclusão de um objeto WMI existente é um evento extrínsecos. Independentemente da classe com suporte, você pode implementar todos os provedores de eventos da mesma maneira.

O procedimento a seguir descreve como implementar um provedor de eventos.

**Para implementar um provedor de eventos**

1.  Projete e Registre seu provedor de classes com o WMI.

    Provedores de classe se registram com WMI criando uma instância do [**\_ \_ Win32Provider**](--win32provider.md) e uma classe [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) . Para obter mais informações, consulte [registrando um provedor de eventos](registering-an-event-provider.md).

2.  Implemente a interface [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para seu provedor.

    A interface [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) é usada por um WMI de interface comum para carregar e inicializar todos os provedores. Para obter mais informações, consulte [inicializando um provedor](initializing-a-provider.md).

3.  Implemente o [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) como a interface principal para seu provedor.

    A interface [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) usa o método **ProviderEvents** para fornecer eventos ao WMI. Para obter mais informações, consulte [implementando a interface primária para um provedor de eventos](implementing-the-primary-interface-for-an-event-provider.md).

    > [!Note]  
    > Os provedores de eventos devem usar o modelo multi-threaded "both".

     

4.  Opcionalmente, você também pode implementar a interface [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink) para aumentar o desempenho do seu provedor de eventos.

    A interface [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink) permite que o provedor Otimize consultas antes de enviar uma resposta para o WMI e é mais útil para um provedor que fornece eventos de vários tipos e que precisa executar o máximo possível de otimizações internas. Para obter mais informações, consulte [Otimizando um provedor de eventos](optimizing-an-event-provider.md).

5.  Implemente a interface [**IWbemEventProviderSecurity**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovidersecurity) para limitar os consumidores a determinados identificadores de segurança (SIDs) ou implemente [**IWbemEventSink:: SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) para proteger o próprio coletor. O provedor também pode definir a **propriedade \_ descritor de segurança** na classe de evento para proteger eventos individuais no código MOF. Para obter mais informações, consulte [SECURING WMI Events](securing-wmi-events.md).
6.  Adicione qualquer código adicional necessário para seu provedor.

    Ao projetar seu provedor, você provavelmente precisará chamar as interfaces WMI. Para obter mais informações, consulte [chamando um método](calling-a-method.md).

    Ao recuperar informações de um cliente, talvez seja necessário acessar os níveis de segurança para esse cliente. Para obter mais informações, consulte [representando um cliente](impersonating-a-client.md).

7.  Substitua o provedor preexistente pelo seu novo código.

    Você não precisará executar esta etapa se não tiver um provedor preexistente para copiar. Para obter mais informações, consulte [atualizando um provedor](updating-a-provider.md).

Um aplicativo cliente pode solicitar um evento registrando-se com o WMI como um consumidor de eventos. Para obter mais informações, consulte [recebendo um evento WMI](receiving-a-wmi-event.md).

 

 
