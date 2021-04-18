---
description: A classe CommandLineEventConsumer executa um programa executável especificado de uma linha de comando quando ocorre um evento especificado. Essa classe é um consumidor de eventos padrão que o WMI fornece.
ms.assetid: b912a4a1-7b1c-43a9-b098-fcfd62a2c2db
ms.tgt_platform: multiple
title: Executando um programa da linha de comando com base em um evento
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: de7f4fb5e679a6b5767635c70e2ffb5eda3ba800
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764377"
---
# <a name="running-a-program-from-the-command-line-based-on-an-event"></a>Executando um programa da linha de comando com base em um evento

A classe [**CommandLineEventConsumer**](commandlineeventconsumer.md) executa um programa executável especificado de uma linha de comando quando ocorre um evento especificado. Essa classe é um consumidor de eventos padrão que o WMI fornece.

Ao usar o [**CommandLineEventConsumer**](commandlineeventconsumer.md), você deve proteger o executável que deseja iniciar. Se o executável não estiver em um local seguro ou não estiver protegido com uma ACL (lista de controle de acesso) forte, um usuário sem privilégios de acesso poderá substituir o executável por um executável diferente. Você pode usar as classes [**Win32 \_ LogicalFileSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting) ou [**Win32 \_ LogicalShareSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalsharesecuritysetting) para alterar programaticamente a segurança de um arquivo ou compartilhamento. Para obter mais informações, consulte [criando um descritor de segurança para um novo objeto em C++](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).

O procedimento básico para usar consumidores padrão é sempre o mesmo e está localizado em [monitoramento e resposta a eventos com consumidores padrão](monitoring-and-responding-to-events-with-standard-consumers.md). O procedimento a seguir adiciona o procedimento básico, é específico à classe [**CommandLineEventConsumer**](commandlineeventconsumer.md) e descreve como criar um consumidor de eventos que executa um programa.

> [!Caution]
>
> A classe [**CommandLineEventConsumer**](commandlineeventconsumer.md) tem restrições de segurança especiais. Esse consumidor padrão deve ser configurado por um membro local do grupo Administradores no computador local. Se você usar uma conta de domínio para criar a assinatura, a conta LocalSystem deverá ter as permissões necessárias no domínio para verificar se o criador é membro do grupo local de administradores.
>
> [**CommandLineEventConsumer**](commandlineeventconsumer.md) não pode ser usado para iniciar um processo que é executado interativamente.

 

O procedimento a seguir descreve como criar um consumidor de eventos que executa um processo de uma linha de comando.

**Para criar um consumidor de eventos que executa um processo de uma linha de comando**

1.  No arquivo formato MOF (MOF), crie uma instância de [**CommandLineEventConsumer**](commandlineeventconsumer.md) para receber os eventos solicitados na consulta. Para obter mais informações, consulte [Designing formato MOF (MOF) classes](designing-managed-object-format--mof--classes.md).
2.  Crie uma instância de [**\_ \_ EventFilter**](--eventfilter.md) e dê um nome a ela.
3.  Crie uma consulta para especificar o tipo de evento. Para obter mais informações, consulte [consultando com WQL](querying-with-wql.md).
4.  Crie uma instância de [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) para associar o filtro à instância de [**CommandLineEventConsumer**](commandlineeventconsumer.md).
5.  Compile o arquivo MOF usando [**Mofcomp.exe**](mofcomp.md).

## <a name="example"></a>Exemplo

O exemplo de código a seguir cria uma nova classe chamada "MyCmdLineConsumer" para gerar eventos quando uma instância da nova classe é criada no final de um MOF. O exemplo está no código MOF, mas você pode criar as instâncias programaticamente usando a [API de script para WMI](scripting-api-for-wmi.md) ou a [API com para WMI](com-api-for-wmi.md).

O procedimento a seguir descreve como criar uma nova classe chamada MyCmdLineConsumer.

**Para criar uma nova classe chamada MyCmdLineConsumer**

1.  Crie o arquivo detest.bat do c: \\ cmdline \_ com um comando que execute um programa visível, como "calc.exe".
2.  Copie o MOF para um arquivo de texto e salve-o com uma extensão. mof.
3.  Em um janela Comando, compile o arquivo MOF usando o seguinte comando: **Mofcomp filename. mof**.

> [!Note]  
> O programa especificado em cmdline \_test.bat deve ser executado.

 

``` syntax
// Set the namespace as root\subscription.
// The CommandLineEventConsumer is already compiled
// in the root\subscription namespace. 
#pragma namespace ("\\\\.\\Root\\subscription")

class MyCmdLineConsumer
{
 [key]string Name;
};

// Create an instance of the command line consumer
// and give it the alias $CMDLINECONSUMER

instance of CommandLineEventConsumer as $CMDLINECONSUMER
{
 Name = "CmdLineConsumer_Example";
 CommandLineTemplate = "c:\\cmdline_test.bat";
 RunInteractively = True;
 WorkingDirectory = "c:\\";
};    

// Create an instance of the event filter
// and give it the alias $CMDLINEFILTER
// The filter queries for instance creation event
// for instances of the MyCmdLineConsumer class

instance of __EventFilter as $CMDLINEFILTER
{
    Name = "CmdLineFilter";
    Query = "SELECT * FROM __InstanceCreationEvent"
        " WHERE TargetInstance.__class = \"MyCmdLineConsumer\"";
    QueryLanguage = "WQL";
};

// Create an instance of the binding
// between filter and consumer instances.

instance of __FilterToConsumerBinding
{
     Consumer = $CMDLINECONSUMER;
     Filter = $CMDLINEFILTER;
};

// Create an instance of this class right now. 
// The commands in c:\\cmdline_test.bat execute
// as the result of creating the instance
// of MyCmdLineConsumer.
 
instance of MyCmdLineConsumer
{
     Name = "CmdLineEventConsumer test";
};
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Monitorando e respondendo a eventos com consumidores padrão](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 
