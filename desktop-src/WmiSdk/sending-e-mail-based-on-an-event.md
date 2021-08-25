---
description: Usando a classe SMTPEventConsumer, você pode enviar um email para um usuário designado quando ocorre um evento especificado. Essa classe é um consumidor de eventos padrão que o WMI fornece.
ms.assetid: ed10e6f7-8e18-4cde-bd46-a7791547c7da
ms.tgt_platform: multiple
title: Enviar email com base em um evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68bcef0858f7022fcb36006f038b20dedc940da60ee6c61e0372f5a74663093a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860409"
---
# <a name="sending-email-based-on-an-event"></a>Enviar email com base em um evento

Usando a [classe SMTPEventConsumer,](smtpeventconsumer.md) você pode enviar um email para um usuário designado quando ocorre um evento especificado. Essa classe é um [consumidor de eventos padrão](standard-consumer-classes.md) que o WMI fornece.

A [classe SMTPEventConsumer](smtpeventconsumer.md) requer as seguintes condições para enviar uma mensagem de email em resposta a um evento:

-   A [classe SMTPEventConsumer](smtpeventconsumer.md) deve ser compilada no namespace correto. Para obter mais informações, [consulte Monitoramento e resposta a eventos com consumidores padrão.](monitoring-and-responding-to-events-with-standard-consumers.md)
-   Um servidor SMTP deve existir na rede.
-   A mensagem de email não pode ter um anexo.
-   A mensagem de email deve ser codificada em US-ASCII.

O procedimento básico para usar consumidores padrão é sempre o mesmo e está localizado em Monitoramento e resposta a [eventos com consumidores padrão.](monitoring-and-responding-to-events-with-standard-consumers.md) O procedimento a seguir adiciona ao procedimento básico; é específico para a [classe SMTPEventConsumer;](smtpeventconsumer.md) e descreve como criar um consumidor de eventos que envia email.

O procedimento a seguir descreve como criar um consumidor de eventos que envia email.

**Para criar um consumidor de eventos que envia email**

1.  Instale e registre a [classe SMTPEventConsumer,](smtpeventconsumer.md) se necessário.

    A [classe SMTPEventConsumer](smtpeventconsumer.md) é compilada no namespace da assinatura raiz \\ pelo programa de instalação do WMI.

2.  Identifique o evento que você deseja monitorar e criar a consulta de evento.

    Pode haver um evento intrínseco existente que use para monitorar seu evento. A maioria dos eventos intrínsecos está associada a alterações em instâncias de classe no \\ namespace "root cimv2". Analisando as classes na referência [classes WMI,](wmi-classes.md) você provavelmente pode encontrar uma classe que identifica o evento que deseja monitorar. Por exemplo, use a [**classe \_ LogicalDisk do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) para monitorar alterações em uma unidade de disco rígido.

    Se não houver eventos intrínsecos existentes que usem, poderá haver um provedor de eventos extrínsecos que possa funcionar. Por exemplo, use [**a classe RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) do provedor do Registro para monitorar as alterações no registro do sistema.

    Se não existir uma classe que identifique o evento que você deseja monitorar, você deverá criar seu próprio provedor de eventos e definir novas classes de evento extrísico. Para obter mais informações, consulte [Escrevendo um provedor de eventos](writing-an-event-provider.md).

3.  No arquivo Managed Object Format (MOF), crie uma instância do [SMTPEventConsumer](smtpeventconsumer.md) para receber eventos.

    Use as propriedades da instância para definir a mensagem de email a ser enviada quando um evento ocorrer. Por exemplo, a **propriedade ToLine** define o endereço de email e a propriedade **Message** define o texto da mensagem de email. Você deve definir o endereço de email, o assunto e o texto de uma mensagem, mas uma mensagem de email não pode ter um anexo. Para obter mais informações, consulte [Designando classes Managed Object Format (MOF).](designing-managed-object-format--mof--classes.md)

4.  Crie uma consulta de evento que especifica os eventos que você deseja monitorar.

    Para obter mais informações, [consulte Consultando com WQL](querying-with-wql.md).

5.  Crie uma instância de [**\_ \_ EventFilter**](--eventfilter.md) e armazene sua consulta na **propriedade** Consulta.

    Para obter mais informações, [consulte Consultando com WQL.](querying-with-wql.md)

6.  Crie uma instância de [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) para associar o filtro e o consumidor.
7.  Compile o arquivo MOF usando [**Mofcomp.exe**](mofcomp.md).


## <a name="example"></a>Exemplo

O exemplo nesta seção está no código MOF, mas você pode criar as instâncias programaticamente usando a API de Script para [WMI](scripting-api-for-wmi.md) ou a [API COM para WMI](com-api-for-wmi.md).

O procedimento a seguir descreve como usar o exemplo.

**Para usar o exemplo**

1.  Copie o MOF a seguir em um arquivo de texto e salve-o com uma extensão .mof.
2.  Em uma janela do prompt de comando, compile o arquivo MOF usando o seguinte comando:

    Nome do arquivo *Mofcomp***.mof* *

> [!Note]  
> Quando o código MOF é compilado no namespace da assinatura \\ raiz, [o SMTPEventConsumer](smtpeventconsumer.md) é compilado no mesmo namespace.

 

``` syntax
#pragma namespace ("\\\\.\\root\\subscription")

instance of __EventFilter as $FILTER
{
    Name = "LowDiskspaceFilter";
    
    EventNamespace = "\\\\.\\root\\cimv2";  

    Query = "SELECT * FROM __InstanceModificationEvent WITHIN 10 "
            "WHERE TargetInstance ISA \"Win32_LogicalDisk\" "
            "AND TargetInstance.FreeSpace < 846000000 "
            "AND PreviousInstance.FreeSpace >= 846000000 "
            "AND (TargetInstance.DeviceID = \"C:\" "
            "OR TargetInstance.DeviceID = \"D:\")";
    QueryLanguage = "WQL";
};


instance of SMTPEventConsumer as $CONSUMER
{
    Name = "LowDisk";
    ToLine = "SysAd@MyCompany.com, MyAlias@MyCompany.com";
    CcLine = "MyHome@MyISP.com";
    ReplyToLine = "MyAlias@MyCompany.com";
    SMTPServer = "SmartHost";
    Subject = "WARNING: Low disk space";
    Message = "WARNING: Your %TargetInstance.DeviceID% is"
        " getting dangerously low.";
};

instance of __FilterToConsumerBinding
{
    Consumer = $CONSUMER ;
    Filter = $FILTER ;
};
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Monitoramento e resposta a eventos com consumidores padrão](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 
