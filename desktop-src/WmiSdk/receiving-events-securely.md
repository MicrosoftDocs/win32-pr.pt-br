---
description: Os consumidores temporários e permanentes têm diferentes métodos de proteção da entrega de eventos.
ms.assetid: cd02e5db-f9e2-438b-9632-0a1387a6d4e3
ms.tgt_platform: multiple
title: Recebendo eventos com segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d64db5b0289abd9a43caee6ddb3b68da94a9560b0ea8f591d95ee472cf900b4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118316523"
---
# <a name="receiving-events-securely"></a>Recebendo eventos com segurança

Os consumidores temporários e permanentes têm diferentes métodos de proteção da entrega de eventos.

As seções a seguir são discutidas neste tópico:

-   [Proteger consumidores temporários](#securing-temporary-consumers)
-   [Proteger consumidores permanentes](#securing-permanent-consumers)
-   [Proteger a assinatura permanente](#securing-the-permanent-subscription)
-   [Definindo um SD Administrator-Only aplicativo](#setting-an-administrator-only-sd)
-   [Representando a identidade do provedor de eventos](#impersonating-the-event-provider-identity)
-   [SIDs e assinaturas permanentes](#sids-and-permanent-subscriptions)
-   [Criando assinaturas permanentes usando contas de domínio](#creating-permanent-subscriptions-using-domain-accounts)
-   [Tópicos relacionados](#related-topics)

## <a name="securing-temporary-consumers"></a>Proteger consumidores temporários

Um [*consumidor temporário é*](gloss-t.md) executado até que o sistema seja reinicializado ou o WMI seja interrompido, mas não pode ser iniciado se um evento específico for gerado. Por exemplo, uma chamada para [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) cria um consumidor temporário.

As chamadas [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) ou [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) criam consumidores de eventos temporários. Os consumidores temporários não podem controlar quem fornece eventos para o sink [*de eventos*](gloss-s.md) que eles criam.

Chamadas para [**métodos ExecNotificationQuery**](swbemservices-execnotificationquery.md) podem ser feitas de forma síncrona, [*semissíncrona*](gloss-s.md)ou assíncrona. Por exemplo, [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) é um método síncrono que pode ser chamado de forma síncrona, dependendo de como o parâmetro *iflags* é definido. [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) é uma chamada assíncrona.

Esteja ciente de que o retorno de chamada para o sink para as versões assíncronas dessas chamadas pode não ser retornado no mesmo nível de autenticação que a chamada feita pelo script. Portanto, é recomendável usar chamadas síncronas em vez de assíncronas. Se você precisar de comunicação assíncrona, consulte Chamando um método e Definindo [a](calling-a-method.md) segurança [em uma chamada assíncrona](setting-security-on-an-asynchronous-call.md).

Os assinantes de script não podem verificar os direitos de acesso de um provedor de eventos para fornecer eventos ao sink criado pelo script. Portanto, é recomendável que as chamadas [**paraSWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) usem a forma semisíncrona da chamada e usem configurações de segurança específicas. Para obter mais informações, [consulte Fazendo uma chamada semisíncrona com o VBScript.](making-a-semisynchronous-call-with-vbscript.md)

## <a name="securing-permanent-consumers"></a>Proteger consumidores permanentes

Um [*consumidor permanente tem*](gloss-p.md) uma assinatura permanente para eventos de um provedor de eventos que persistirão depois que o sistema operacional for reiniciado. Um provedor de eventos que dá suporte a consumidores permanentes é um [*provedor de consumidor de eventos*](gloss-e.md). Se o provedor de eventos não estiver em execução quando ocorrer um evento, o WMI iniciará o provedor quando precisar entregar eventos. O WMI identifica a qual provedor de consumidor os eventos devem ser entregues, com base na instância [**\_ \_ EventConsumerProviderRegistration,**](--eventconsumerproviderregistration.md) que associa [*a*](gloss-l.md) instância do provedor de consumidor [**\_ \_ Win32Provider**](--win32provider.md) a uma classe de consumidor lógica definida pelo provedor de consumidor. Para obter mais informações sobre a função de provedores de consumidor, consulte [Escrevendo um provedor de consumidor de eventos](writing-an-event-consumer-provider.md).

Os consumidores permanentes podem controlar quem envia eventos e provedores de eventos podem controlar quem acessa seus eventos.

Scripts de cliente e aplicativos criam instâncias da classe de consumidor lógico como parte de uma assinatura. A classe de consumidor lógica define quais informações o evento contém, o que o cliente pode fazer com o evento e como o evento é entregue.

As Classes de Consumidor [Padrão WMI](standard-consumer-classes.md) fornecem exemplos da função de classes de consumidor lógicas. Para obter mais informações, [consulte Monitoramento e resposta a eventos com consumidores padrão.](monitoring-and-responding-to-events-with-standard-consumers.md)

## <a name="securing-the-permanent-subscription"></a>Proteger a assinatura permanente

As assinaturas permanentes têm maior potencial para causar problemas de segurança no WMI e, portanto, têm os seguintes requisitos de segurança:

-   A instância de consumidor lógico, [**\_ \_ o EventFilter**](--eventfilter.md)e as instâncias [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) devem ter o mesmo SID (identificador de segurança) individual na propriedade **CreatorSID.** Para obter mais informações, [consulte Mantendo o mesmo SID em todas as instâncias de uma assinatura permanente](#sids-and-permanent-subscriptions).
-   A conta que cria a assinatura deve ser uma conta de domínio com privilégios de administrador local ou a conta do grupo administradores local. O uso do SID do grupo Administradores permite que a assinatura continue a funcionar no computador local, mesmo que ela seja desconectada da rede. O uso de uma conta de domínio permite a identificação exata do usuário.

    No entanto, se o computador não estiver conectado e a conta de criação for uma conta de domínio, o consumidor falhará porque o WMI não pode verificar a identidade da conta. Para evitar a falha de assinatura se o computador estiver desconectado da rede, use o SID do grupo Administradores para uma assinatura. Nesse caso, você deve garantir que a conta LocalSystem possa acessar dados de associação de grupo no domínio. Alguns provedores de consumidores de eventos têm requisitos de segurança particularmente altos, pois uma assinatura não mal-estruturada pode causar grandes danos. Exemplos são os consumidores padrão, [**ActiveScriptEventConsumer**](activescripteventconsumer.md) e [**CommandLineEventConsumer.**](commandlineeventconsumer.md)

-   Você pode configurar a assinatura permanente para aceitar apenas eventos de identidades específicas do provedor de eventos. Definir o descritor de segurança na **propriedade EventAccess** da [**\_ \_ instância eventFilter**](--eventfilter.md) para as identidades do provedor de eventos. O WMI compara a identidade do provedor de eventos com o descritor de segurança para determinar se o provedor tem **acesso WBEM \_ RIGHT \_ PUBLISH.** Para obter mais informações, consulte [Constantes de segurança WMI](wmi-security-constants.md).

    Se o filtro permitir acesso à identidade do provedor de eventos, ele também confiará no evento. Isso permite que o consumidor que recebeu o evento aumente um evento delegado.

    **Observação**  O padrão para o descritor de segurança **em EventAccess** é **NULL,** que permite acesso a todos. A limitação do acesso na instância de assinatura do [**\_ \_ EventFilter**](--eventfilter.md) é recomendada para melhorar a segurança do evento.

## <a name="setting-an-administrator-only-sd"></a>Definindo um SD Administrator-Only aplicativo

O exemplo de código C++ a seguir cria um descritor de segurança somente de administrador na [**\_ \_ instância eventFilter.**](--eventfilter.md) Este exemplo cria o descritor de segurança [usando](/windows/desktop/SecAuthZ/security-descriptor-definition-language) a SDDL (Linguagem de Definição do Descritor de Segurança). Para obter mais informações sobre **o WBEM \_ RIGHT \_ SUBSCRIBE,** consulte [Constantes de segurança WMI](wmi-security-constants.md).


```C++
// Create SD that allows only administrators 
//    to send events to this filter. 
// The SDDL settings are O:BAG:BAD:(A;;0x80;;;BA)
// Set the EventAccess property in the 
//    IWbemClassObject of the __EventFilter instance. 
   long lMask = WBEM_RIGHT_PUBLISH;
     WCHAR wBuf[MAX_PATH];
     _ltow( lMask, wBuf, 16 );
 
HRESULT hRes = pEventFilterInstance->Put( L"EventAccess", 0,
    &_variant_t( L"O:BAG:BAD:(A;;0x80;;;BA)" ), NULL );
```



O exemplo de código anterior requer as instruções de referência e \# inclusão a seguir.


```C++
#define _WIN32_DCOM
#include <wbemidl.h>
#include <comdef.h>

#pragma comment(lib, "wbemuuid.lib")
```



## <a name="impersonating-the-event-provider-identity"></a>Representando a identidade do provedor de eventos

Um consumidor permanente pode precisar representar o provedor de eventos para processar o evento. Os consumidores permanentes só poderão representar o provedor de eventos quando existirem as seguintes condições:

-   A instância de [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) tem a **propriedade MaintainSecurityContext** definida como **True.**
-   Um evento é entregue no mesmo contexto de segurança em que o provedor estava quando gerou o evento. Somente um consumidor implementado como uma DLL, um consumidor em processo, pode receber eventos no contexto de segurança do provedor. Para obter mais informações sobre a segurança de provedores e consumidores em processo, consulte [Hospedagem e segurança do provedor.](provider-hosting-and-security.md)
-   O provedor de eventos está em execução em um processo que permite a representação.

A conta que executa o processo do consumidor deve ter **acesso FULL \_ WRITE** ao repositório WMI (também conhecido como repositório CIM). Na assinatura, as instâncias [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md), [**\_ \_ EventConsumer**](--eventconsumer.md)e [**\_ \_ EventFilter**](--eventfilter.md) devem ter o mesmo valor de SID (identificador de segurança individual) na propriedade **CreatorSID.** O WMI armazena o SID no **CreatorSID** para cada instância.

## <a name="sids-and-permanent-subscriptions"></a>SIDs e assinaturas permanentes

Uma assinatura permanente não funciona quando a associação, o consumidor e o filtro não são criados pelo mesmo usuário, o que significa que [**\_ \_ o FilterToConsumerBinding,**](--filtertoconsumerbinding.md) [**\_ \_ EventConsumer**](--eventconsumer.md)e [**\_ \_ EventFilter**](--eventfilter.md) devem ter o mesmo valor de SID (identificador de segurança) individual na propriedade **CreatorSID.** Windows A Instrumentação de Gerenciamento (WMI) armazena esse valor.

## <a name="creating-permanent-subscriptions-using-domain-accounts"></a>Criando assinaturas permanentes usando contas de domínio

Vários problemas devem ser considerados ao usar contas de domínio para criar assinaturas permanentes. Cada assinatura permanente ainda deve funcionar quando nenhum usuário estiver conectado, o que significa que eles funcionam na conta interna localSystem.

Se um usuário de domínio for o criador de uma assinatura permanente para consumidores sensíveis à segurança [**(ActiveScriptEventConsumer,**](activescripteventconsumer.md) [**CommandLineEventConsumer),**](commandlineeventconsumer.md)o WMI verificará se a propriedade **CreatorSID** da classe [**\_ \_ EventFilter,**](--eventfilter.md) [**\_ \_ a classe FilterToConsumerBinding**](--filtertoconsumerbinding.md) e as instâncias de consumidor pertencem a um usuário que é membro do grupo Administradores local.

O exemplo de código a seguir mostra como você pode especificar a **propriedade CreatorSID.**

``` syntax
 instance of __EventFilter as $FILTER
    {
        // this is the Administrators SID in array of bytes format
        CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0};    
        // Add filter code here ...
    }

    instance of ActiveScriptEventConsumer as $CONSUMER
    {
       CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0};
       // Add consumer code here ...
    }

    instance of __FilterToConsumerBinding
    {
       CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0};
       Consumer = $CONSUMER;
       Filter = $FILTER;
       // Add binding code here ...
    }
```

Para situações entre domínios, adicione Usuários Autenticados ao "Grupo de Acesso Windows Autorização".

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Proteger eventos WMI](securing-wmi-events.md)
</dt> <dt>

[Recebendo um evento WMI](receiving-a-wmi-event.md)
</dt> </dl>

 

 
