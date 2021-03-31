---
description: O consumidor padrão implementado pela classe ActiveScriptEventConsumer permite que um computador execute um script e execute uma ação quando eventos importantes ocorrem para garantir que um computador possa detectar e resolver problemas automaticamente.
ms.assetid: 0d2ac139-3e2b-4089-ae9c-289d376e27a2
ms.tgt_platform: multiple
title: Executando um script com base em um evento
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4dbb1e55c7828a79d6541182eff5ce20147a82c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103836946"
---
# <a name="running-a-script-based-on-an-event"></a>Executando um script com base em um evento

O consumidor padrão implementado pela classe [**ActiveScriptEventConsumer**](activescripteventconsumer.md) permite que um computador execute um script e execute uma ação quando eventos importantes ocorrem para garantir que um computador possa detectar e resolver problemas automaticamente.

Esse consumidor é carregado por padrão no namespace **da \\ assinatura raiz** .

Você pode configurar o desempenho de todas as instâncias do [**ActiveScriptEventConsumer**](activescripteventconsumer.md) em um sistema definindo os valores da propriedade **Timeout** ou **MaximumScripts** em uma única instância de [**ScriptingStandardConsumerSetting**](scriptingstandardconsumersetting.md).

O procedimento básico para usar consumidores padrão é sempre o mesmo e está localizado em [monitoramento e resposta a eventos com consumidores padrão](monitoring-and-responding-to-events-with-standard-consumers.md). O procedimento a seguir que adiciona ao procedimento básico é específico à classe [**ActiveScriptEventConsumer**](activescripteventconsumer.md) e descreve como criar um consumidor de evento que executa um script.

> [!Caution]  
> A classe [**ActiveScriptEventConsumer**](activescripteventconsumer.md) tem restrições de segurança especiais. Esse consumidor padrão deve ser configurado por um membro local do grupo Administradores no computador local. Se você usar uma conta de domínio para criar a assinatura, a conta LocalSystem deverá ter as permissões necessárias no domínio para verificar se o criador é membro do grupo local de administradores.

 

O procedimento a seguir descreve como criar um consumidor de eventos que executa um script.

**Para criar um consumidor de eventos que executa um script**

1.  Escreva o script para ser executado quando ocorrer um evento.

    Você pode escrever o script em qualquer idioma, mas certifique-se de que um mecanismo de script para o idioma escolhido esteja instalado em seu computador. O script não precisa usar objetos de script WMI.

    Somente um administrador pode configurar um consumidor de script, e o script é executado em credenciais LocalSystem, o que fornece recursos amplos para o consumidor, exceto para acesso à rede. No entanto, o script não tem acesso a dados de logon de usuário específicos, por exemplo, variáveis de ambiente e compartilhamentos de rede.

2.  No arquivo formato MOF (MOF), crie uma instância de [**ActiveScriptEventConsumer**](activescripteventconsumer.md) para receber os eventos solicitados na consulta.

    Você pode colocar o texto do script em **ScriptText** ou pode especificar o caminho e o nome de arquivo do script em **ScriptFileName**. Para obter mais informações, consulte [Designing formato MOF (MOF) classes](designing-managed-object-format--mof--classes.md).

3.  Crie uma instância de [**\_ \_ EventFilter**](--eventfilter.md), nomeie-a e, em seguida, crie uma consulta para especificar o tipo de evento, que dispara a execução do script.

    Para obter mais informações, consulte [consultando com WQL](querying-with-wql.md).

4.  Crie uma instância de [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) para associar o filtro à instância de [**ActiveScriptEventConsumer**](activescripteventconsumer.md).
5.  Compile o arquivo MOF usando [**Mofcomp.exe**](mofcomp.md).

Os exemplos na seção a seguir mostram duas maneiras de implementar um script controlado por evento. O primeiro exemplo usa um script que é definido em um arquivo externo e o segundo exemplo usa um script que é criado no código MOF. Os exemplos estão no código MOF, mas você pode criar as instâncias programaticamente usando a [API de script para WMI](scripting-api-for-wmi.md) ou a [API com para WMI](com-api-for-wmi.md).

## <a name="example-using-an-external-script"></a>Exemplo usando um script externo

O procedimento a seguir descreve como usar o exemplo de script externo.

**Para usar o exemplo de script externo**

1.  Crie um arquivo chamado c: \\Asec.vbs e, em seguida, copie o script neste exemplo para ele.
2.  Copie a lista MOF em um arquivo de texto e salve-a com uma extensão. mof.
3.  Em uma janela de prompt de comando, compile o arquivo MOF usando o comando a seguir.

     *Nome do arquivo Mofcomp * * *. mof**

4.  Execute a calculadora, que cria um processo de calc.exe. Aguarde mais de cinco segundos, feche a janela da calculadora e, em seguida, examine o diretório C: \\ para obter um arquivo chamado ASEC. log.

    O texto a seguir é semelhante ao texto que estará contido no arquivo ASEC. log.

    ``` syntax
    Time: 12/31/2002 2:56:33 PM; Entry made by: ASEC
    Application closed. UserModeTime:  1562500; 
    KernelModeTime: 3125000 [hundreds of nanoseconds]
    ```

O exemplo de código VBScript a seguir mostra o script que é chamado quando um evento é recebido pelo consumidor permanente. O objeto **TargetEvent** é uma instância [**\_ \_ InstanceDeletionEvent**](--instancedeletionevent.md) , de modo que tem uma propriedade chamada **TargetInstance**, que é uma instância de [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) usada para acionar o evento. A **classe \_ process do Win32** tem as propriedades **usermodetime** e **KernelModeTime** que são colocadas no arquivo de log criado pelo script.


```VB
' asec.vbs script
Dim objFS, objFile
Set objFS = CreateObject("Scripting.FileSystemObject")
Set objFile = objFS.OpenTextFile("C:\ASEC.log", 8, true)
objFile.WriteLine "Time: " & Now & "; Entry made by: ASEC"

objFile.WriteLine "Application closed. UserModeTime:  " & _
    TargetEvent.TargetInstance.UserModeTime & _
    "; KernelModeTime: " & _
    TargetEvent.TargetInstance.KernelModeTime & _
    " [hundreds of nanoseconds]"
objFile.Close
```



O exemplo de código MOF a seguir chama o script quando um evento é recebido. Ele cria o filtro, o consumidor e a associação entre eles no namespace **de \\ assinatura raiz** .

``` syntax
#pragma namespace ("\\\\.\\root\\subscription")

instance of ActiveScriptEventConsumer as $Cons
{
    Name = "ASEC";
    ScriptingEngine = "VBScript";
    ScriptFileName = "c:\\asec2.vbs";
};

instance of __EventFilter as $Filt
{
    Name = "EF";
    Query = "SELECT * FROM __InstanceDeletionEvent WITHIN 5 "
        "WHERE TargetInstance ISA \"Win32_Process\" "
        "AND TargetInstance.Name = \"calc.exe\"";
    QueryLanguage = "WQL";
    EventNamespace = "root\\cimv2";
};

instance of __FilterToConsumerBinding
{
    Filter = $Filt;
    Consumer = $Cons;
};
```

## <a name="example-using-inline-script"></a>Exemplo usando script embutido

O procedimento a seguir descreve como usar o exemplo de script embutido.

**Para usar o exemplo de script embutido**

1.  Copie a lista MOF nesta seção em um arquivo de texto e salve-a com uma extensão. mof.
2.  Em uma janela de prompt de comando, compile o arquivo MOF usando o comando a seguir.

     *Nome do arquivo Mofcomp * * *. mof**

O exemplo de código MOF a seguir cria o filtro, o consumidor e a associação entre eles e também contém o script embutido.

``` syntax
#pragma namespace ("\\\\.\\root\\subscription")

instance of ActiveScriptEventConsumer as $Cons
{
    Name = "ASEC";
    ScriptingEngine = "VBScript";
    
    ScriptText =
        "Dim objFS, objFile\n"
        "Set objFS = CreateObject(\"Scripting.FileSystemObject\")\n"
        "Set objFile = objFS.OpenTextFile(\"C:\\ASEC.log\","
        " 8, true)\nobjFile.WriteLine \"Time: \" & Now & \";"
        " Entry made by: ASEC\"\nobjFile.WriteLine"
        " \"Application closed. UserModeTime:  \" & "
        "TargetEvent.TargetInstance.UserModeTime &_\n"
        "\"; KernelModeTime: \" & "
        "TargetEvent.TargetInstance.KernelModeTime "
        "& \" [hundreds of nanoseconds]\"\n"
        "objFile.Close\n";
};

instance of __EventFilter as $Filt
{
    Name = "EF";
    Query = "SELECT * FROM __InstanceDeletionEvent WITHIN 5 "
        "WHERE TargetInstance ISA \"Win32_Process\" "
        "AND TargetInstance.Name = \"calc.exe\"";
    QueryLanguage = "WQL";
    EventNamespace = "root\\cimv2";
};

instance of __FilterToConsumerBinding
{
    Filter = $Filt;
    Consumer = $Cons;
};
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Monitorando e respondendo a eventos com consumidores padrão](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 
