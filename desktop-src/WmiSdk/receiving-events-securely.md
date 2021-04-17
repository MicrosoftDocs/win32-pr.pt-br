---
description: Consumidores temporários e permanentes têm métodos diferentes para proteger a entrega de eventos.
ms.assetid: cd02e5db-f9e2-438b-9632-0a1387a6d4e3
ms.tgt_platform: multiple
title: Recebendo eventos com segurança
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f27d156213553ee17a346d780cbea0ff82beca83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755024"
---
# <a name="receiving-events-securely"></a>Recebendo eventos com segurança

Consumidores temporários e permanentes têm métodos diferentes para proteger a entrega de eventos.

As seções a seguir são discutidas neste tópico:

-   [Protegendo consumidores temporários](#securing-temporary-consumers)
-   [Protegendo consumidores permanentes](#securing-permanent-consumers)
-   [Protegendo a assinatura permanente](#securing-the-permanent-subscription)
-   [Definindo um Administrator-Only SD](#setting-an-administrator-only-sd)
-   [Representando a identidade do provedor de eventos](#impersonating-the-event-provider-identity)
-   [SIDs e assinaturas permanentes](#sids-and-permanent-subscriptions)
-   [Criando assinaturas permanentes usando contas de domínio](#creating-permanent-subscriptions-using-domain-accounts)
-   [Tópicos relacionados](#related-topics)

## <a name="securing-temporary-consumers"></a>Protegendo consumidores temporários

Um [*consumidor temporário*](gloss-t.md) é executado até que o sistema seja reinicializado ou o WMI seja interrompido, mas não poderá ser iniciado se um evento específico for gerado. Por exemplo, uma chamada para [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) cria um consumidor temporário.

As chamadas [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) ou [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) criam consumidores de eventos temporários. Os consumidores temporários não podem controlar quem fornece eventos para o [*coletor*](gloss-s.md) de eventos que eles criam.

Chamadas para métodos [**ExecNotificationQuery**](swbemservices-execnotificationquery.md) podem ser feitas de forma síncrona, [*semisynchronously*](gloss-s.md)ou assíncrona. Por exemplo, [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) é um método síncrono que pode ser chamado de semisynchronously, dependendo de como o parâmetro *iFlags* é definido. [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) é uma chamada assíncrona.

Lembre-se de que o retorno de chamada para o coletor das versões assíncronas dessas chamadas pode não ser retornado no mesmo nível de autenticação que a chamada que o script fez. Portanto, é recomendável que você use semisynchronous em vez de chamadas assíncronas. Se você precisar de comunicação assíncrona, consulte [chamar um método](calling-a-method.md) e [definir a segurança em uma chamada assíncrona](setting-security-on-an-asynchronous-call.md).

Os assinantes de script não podem verificar os direitos de acesso de um provedor de eventos para fornecer eventos ao coletor criado pelo script. Portanto, é recomendável que as chamadas para [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) usem o formulário semisynchronous da chamada e usem configurações de segurança específicas. Para obter mais informações, consulte [fazendo uma chamada de Semisynchronous com o VBScript](making-a-semisynchronous-call-with-vbscript.md).

## <a name="securing-permanent-consumers"></a>Protegendo consumidores permanentes

Um [*consumidor permanente*](gloss-p.md) tem uma assinatura permanente para eventos de um provedor de eventos que persistirá depois que o sistema operacional for reiniciado. Um provedor de eventos que dá suporte a consumidores permanentes é um [*provedor de consumidor de eventos*](gloss-e.md). Se o provedor de eventos não estiver em execução quando um evento ocorrer, o WMI iniciará o provedor quando precisar entregar eventos. O WMI identifica a qual provedor de consumidor os eventos devem ser entregues, com base na instância [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) , que associa a instância [**\_ \_ Win32Provider**](--win32provider.md) do provedor de consumidor a uma [*classe de consumidor lógica*](gloss-l.md) definida pelo provedor de consumidor. Para obter mais informações sobre a função de provedores de consumidor, consulte [escrevendo um provedor de consumidor de eventos](writing-an-event-consumer-provider.md).

Os consumidores permanentes podem controlar quem envia eventos e provedores de eventos podem controlar quem acessa seus eventos.

Scripts e aplicativos de cliente criam instâncias da classe de consumidor lógica como parte de uma assinatura. A classe consumidor lógico define quais informações o evento contém, o que o cliente pode fazer com o evento e como o evento é entregue.

As [classes de consumidor padrão](standard-consumer-classes.md) do WMI fornecem exemplos da função de classes de consumidor lógicas. Para obter mais informações, consulte [monitorando e respondendo a eventos com consumidores padrão](monitoring-and-responding-to-events-with-standard-consumers.md).

## <a name="securing-the-permanent-subscription"></a>Protegendo a assinatura permanente

As assinaturas permanentes têm maior potencial para causar problemas de segurança no WMI e, portanto, têm os seguintes requisitos de segurança:

-   A instância de consumidor lógico, [**\_ \_ EventFilter**](--eventfilter.md), e as instâncias de [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) devem ter o mesmo SID (identificador de segurança individual) na propriedade **CreatorSID** . Para obter mais informações, consulte [mantendo o mesmo SID em todas as instâncias de uma assinatura permanente](#sids-and-permanent-subscriptions).
-   A conta que cria a assinatura deve ser uma conta de domínio com privilégios de administrador local ou a conta de grupo de administradores locais. Usar o SID do grupo Administradores permite que a assinatura continue a funcionar no computador local, mesmo se ela estiver desconectada da rede. O uso de uma conta de domínio permite a identificação exata do usuário.

    No entanto, se o computador não estiver conectado e a criação da conta for uma conta de domínio, o consumidor falhará porque o WMI não pode verificar a identidade da conta. Para evitar a falha de assinatura se o computador estiver desconectado da rede, use o SID do grupo Administradores para uma assinatura. Nesse caso, você deve garantir que a conta LocalSystem possa acessar os dados de associação de grupo no domínio. Alguns provedores de consumidor de eventos têm requisitos de segurança particularmente altos, uma vez que uma assinatura não autorizada pode causar grandes danos. Os exemplos são os consumidores padrão, [**ActiveScriptEventConsumer**](activescripteventconsumer.md) e [**CommandLineEventConsumer**](commandlineeventconsumer.md).

-   Você pode configurar a assinatura permanente para aceitar apenas eventos de identidades específicas do provedor de eventos. Defina o descritor de segurança na propriedade **EventAccess** da instância [**\_ \_ EventFilter**](--eventfilter.md) para as identidades do provedor de eventos. O WMI compara a identidade do provedor de eventos com o descritor de segurança para determinar se o provedor tem acesso de **\_ \_ publicação de WBEM direito** . Para obter mais informações, consulte [constantes de segurança do WMI](wmi-security-constants.md).

    Se o filtro permitir acesso à identidade do provedor de eventos, ele também confiará no evento. Isso permite que o consumidor que recebeu o evento gere um evento delegado.

    **Observação**  O padrão para o descritor de segurança em **EventAccess** é **nulo**, o que permite o acesso a todos. É recomendável limitar o acesso na instância de assinatura do [**\_ \_ EventFilter**](--eventfilter.md) para melhorar a segurança do evento.

## <a name="setting-an-administrator-only-sd"></a>Definindo um Administrator-Only SD

O exemplo de código C++ a seguir cria um descritor de segurança somente de administrador na instância [**\_ \_ EventFilter**](--eventfilter.md) . Este exemplo cria o descritor de segurança usando SDDL ( [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) ). Para obter mais informações sobre a **\_ \_ assinatura do WBEM direito**, consulte [constantes de segurança do WMI](wmi-security-constants.md).


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



O exemplo de código anterior requer a seguinte referência e as \# instruções include.


```C++
#define _WIN32_DCOM
#include <wbemidl.h>
#include <comdef.h>

#pragma comment(lib, "wbemuuid.lib")
```



## <a name="impersonating-the-event-provider-identity"></a>Representando a identidade do provedor de eventos

Um consumidor permanente pode precisar representar o provedor de eventos para processar o evento. Os consumidores permanentes só podem representar o provedor de eventos quando existem as seguintes condições:

-   A instância de [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) tem a propriedade **MaintainSecurityContext** definida como **true**.
-   Um evento é entregue no mesmo contexto de segurança em que o provedor estava quando gerou o evento. Apenas um consumidor implementado como uma DLL, um consumidor em processo, pode receber eventos no contexto de segurança do provedor. Para obter mais informações sobre segurança de provedores em processo e consumidores, consulte [hospedagem e segurança do provedor](provider-hosting-and-security.md).
-   O provedor de eventos está sendo executado em um processo que permite a representação.

A conta que executa o processo do consumidor deve ter acesso de **\_ gravação total** ao repositório do WMI (também conhecido como repositório CIM). Na assinatura, as instâncias [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md), [**\_ \_ EventConsumer**](--eventconsumer.md)e [**\_ \_ EventFilter**](--eventfilter.md) devem ter o mesmo valor de Sid (identificador de segurança individual) na propriedade **CreatorSID** . O WMI armazena o SID no **CreatorSID** para cada instância.

## <a name="sids-and-permanent-subscriptions"></a>SIDs e assinaturas permanentes

Uma assinatura permanente não funciona quando a associação, o consumidor e o filtro não são criados pelo mesmo usuário, o que significa que [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md), [**\_ \_ EventConsumer**](--eventconsumer.md)e [**\_ \_ EventFilter**](--eventfilter.md) devem ter o mesmo valor de Sid (identificador de segurança individual) na propriedade **CreatorSID** . Instrumentação de Gerenciamento do Windows (WMI) armazena esse valor.

## <a name="creating-permanent-subscriptions-using-domain-accounts"></a>Criando assinaturas permanentes usando contas de domínio

Vários problemas devem ser considerados ao usar contas de domínio para criar assinaturas permanentes. Cada assinatura permanente ainda deve funcionar quando nenhum usuário está conectado, o que significa que elas funcionam sob a conta LocalSystem interna.

Se um usuário de domínio for o criador de uma assinatura permanente para consumidores sensíveis à segurança ([**ActiveScriptEventConsumer**](activescripteventconsumer.md), [**CommandLineEventConsumer**](commandlineeventconsumer.md)), o WMI verificará se a propriedade **CreatorSID** da classe [**\_ \_ EventFilter**](--eventfilter.md) , a classe [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) e as instâncias do consumidor pertencem a um usuário que é membro do grupo Administradores local.

O exemplo de código a seguir mostra como você pode especificar a propriedade **CreatorSID** .

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

Para situações entre domínios, adicione usuários autenticados ao "grupo de acesso de autorização do Windows".

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Protegendo eventos WMI](securing-wmi-events.md)
</dt> <dt>

[Recebendo um evento WMI](receiving-a-wmi-event.md)
</dt> </dl>

 

 
