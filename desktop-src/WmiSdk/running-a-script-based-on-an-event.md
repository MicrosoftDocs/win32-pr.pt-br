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
# <a name="running-a-script-based-on-an-event"></a><span data-ttu-id="fc9ff-103">Executando um script com base em um evento</span><span class="sxs-lookup"><span data-stu-id="fc9ff-103">Running a Script Based on an Event</span></span>

<span data-ttu-id="fc9ff-104">O consumidor padrão implementado pela classe [**ActiveScriptEventConsumer**](activescripteventconsumer.md) permite que um computador execute um script e execute uma ação quando eventos importantes ocorrem para garantir que um computador possa detectar e resolver problemas automaticamente.</span><span class="sxs-lookup"><span data-stu-id="fc9ff-104">The standard consumer that is implemented by the [**ActiveScriptEventConsumer**](activescripteventconsumer.md) class allows a computer to run a script and take action when important events occur to ensure that a computer can detect and resolve problems automatically.</span></span>

<span data-ttu-id="fc9ff-105">Esse consumidor é carregado por padrão no namespace **da \\ assinatura raiz** .</span><span class="sxs-lookup"><span data-stu-id="fc9ff-105">This consumer is loaded by default in the **root\\subscription** namespace.</span></span>

<span data-ttu-id="fc9ff-106">Você pode configurar o desempenho de todas as instâncias do [**ActiveScriptEventConsumer**](activescripteventconsumer.md) em um sistema definindo os valores da propriedade **Timeout** ou **MaximumScripts** em uma única instância de [**ScriptingStandardConsumerSetting**](scriptingstandardconsumersetting.md).</span><span class="sxs-lookup"><span data-stu-id="fc9ff-106">You can configure the performance of all instances of [**ActiveScriptEventConsumer**](activescripteventconsumer.md) on a system by setting the values of the **Timeout** or **MaximumScripts** property in a single instance of [**ScriptingStandardConsumerSetting**](scriptingstandardconsumersetting.md).</span></span>

<span data-ttu-id="fc9ff-107">O procedimento básico para usar consumidores padrão é sempre o mesmo e está localizado em [monitoramento e resposta a eventos com consumidores padrão](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="fc9ff-107">The basic procedure for using standard consumers is always the same, and is located in [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span> <span data-ttu-id="fc9ff-108">O procedimento a seguir que adiciona ao procedimento básico é específico à classe [**ActiveScriptEventConsumer**](activescripteventconsumer.md) e descreve como criar um consumidor de evento que executa um script.</span><span class="sxs-lookup"><span data-stu-id="fc9ff-108">The following procedure that adds to the basic procedure, is specific to the [**ActiveScriptEventConsumer**](activescripteventconsumer.md) class, and describes how to create an event consumer that runs a script.</span></span>

> [!Caution]  
> <span data-ttu-id="fc9ff-109">A classe [**ActiveScriptEventConsumer**](activescripteventconsumer.md) tem restrições de segurança especiais.</span><span class="sxs-lookup"><span data-stu-id="fc9ff-109">The [**ActiveScriptEventConsumer**](activescripteventconsumer.md) class has special security constraints.</span></span> <span data-ttu-id="fc9ff-110">Esse consumidor padrão deve ser configurado por um membro local do grupo Administradores no computador local.</span><span class="sxs-lookup"><span data-stu-id="fc9ff-110">This standard consumer must be configured by a local member of the Administrators group on the local computer.</span></span> <span data-ttu-id="fc9ff-111">Se você usar uma conta de domínio para criar a assinatura, a conta LocalSystem deverá ter as permissões necessárias no domínio para verificar se o criador é membro do grupo local de administradores.</span><span class="sxs-lookup"><span data-stu-id="fc9ff-111">If you use a domain account to create the subscription, the LocalSystem account must have the necessary permissions on the domain to verify that the creator is a member of the local Administrators group.</span></span>

 

<span data-ttu-id="fc9ff-112">O procedimento a seguir descreve como criar um consumidor de eventos que executa um script.</span><span class="sxs-lookup"><span data-stu-id="fc9ff-112">The following procedure describes how to create an event consumer that executes a script.</span></span>

<span data-ttu-id="fc9ff-113">**Para criar um consumidor de eventos que executa um script**</span><span class="sxs-lookup"><span data-stu-id="fc9ff-113">**To create an event consumer that executes a script**</span></span>

1.  <span data-ttu-id="fc9ff-114">Escreva o script para ser executado quando ocorrer um evento.</span><span class="sxs-lookup"><span data-stu-id="fc9ff-114">Write the script to run when an event takes place.</span></span>

    <span data-ttu-id="fc9ff-115">Você pode escrever o script em qualquer idioma, mas certifique-se de que um mecanismo de script para o idioma escolhido esteja instalado em seu computador.</span><span class="sxs-lookup"><span data-stu-id="fc9ff-115">You can write the script in any language, but ensure that a scripting engine for the language that you choose is installed on your machine.</span></span> <span data-ttu-id="fc9ff-116">O script não precisa usar objetos de script WMI.</span><span class="sxs-lookup"><span data-stu-id="fc9ff-116">The script does not have to use WMI scripting objects.</span></span>

    <span data-ttu-id="fc9ff-117">Somente um administrador pode configurar um consumidor de script, e o script é executado em credenciais LocalSystem, o que fornece recursos amplos para o consumidor, exceto para acesso à rede.</span><span class="sxs-lookup"><span data-stu-id="fc9ff-117">Only an administrator can set up a script consumer, and the script runs under LocalSystem credentials, which gives broad capabilities to the consumer except for network access.</span></span> <span data-ttu-id="fc9ff-118">No entanto, o script não tem acesso a dados de logon de usuário específicos, por exemplo, variáveis de ambiente e compartilhamentos de rede.</span><span class="sxs-lookup"><span data-stu-id="fc9ff-118">However, the script does not have access to specific user logon data, for example, environment variables and network shares.</span></span>

2.  <span data-ttu-id="fc9ff-119">No arquivo formato MOF (MOF), crie uma instância de [**ActiveScriptEventConsumer**](activescripteventconsumer.md) para receber os eventos solicitados na consulta.</span><span class="sxs-lookup"><span data-stu-id="fc9ff-119">In the Managed Object Format (MOF) file, create an instance of [**ActiveScriptEventConsumer**](activescripteventconsumer.md) to receive the events you request in the query.</span></span>

    <span data-ttu-id="fc9ff-120">Você pode colocar o texto do script em **ScriptText** ou pode especificar o caminho e o nome de arquivo do script em **ScriptFileName**.</span><span class="sxs-lookup"><span data-stu-id="fc9ff-120">You can put the text of the script in **ScriptText**, or you can specify the path and filename of the script in **ScriptFileName**.</span></span> <span data-ttu-id="fc9ff-121">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="fc9ff-121">For more information, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>

3.  <span data-ttu-id="fc9ff-122">Crie uma instância de [**\_ \_ EventFilter**](--eventfilter.md), nomeie-a e, em seguida, crie uma consulta para especificar o tipo de evento, que dispara a execução do script.</span><span class="sxs-lookup"><span data-stu-id="fc9ff-122">Create an instance of [**\_\_EventFilter**](--eventfilter.md), name it, and then create a query to specify the type of event, which triggers executing the script.</span></span>

    <span data-ttu-id="fc9ff-123">Para obter mais informações, consulte [consultando com WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="fc9ff-123">For more information see, [Querying with WQL](querying-with-wql.md).</span></span>

4.  <span data-ttu-id="fc9ff-124">Crie uma instância de [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) para associar o filtro à instância de [**ActiveScriptEventConsumer**](activescripteventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="fc9ff-124">Create an instance of [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) to associate the filter with the instance of [**ActiveScriptEventConsumer**](activescripteventconsumer.md).</span></span>
5.  <span data-ttu-id="fc9ff-125">Compile o arquivo MOF usando [**Mofcomp.exe**](mofcomp.md).</span><span class="sxs-lookup"><span data-stu-id="fc9ff-125">Compile the MOF file by using [**Mofcomp.exe**](mofcomp.md).</span></span>

<span data-ttu-id="fc9ff-126">Os exemplos na seção a seguir mostram duas maneiras de implementar um script controlado por evento.</span><span class="sxs-lookup"><span data-stu-id="fc9ff-126">The examples in the following section show two ways to implement an event-driven script.</span></span> <span data-ttu-id="fc9ff-127">O primeiro exemplo usa um script que é definido em um arquivo externo e o segundo exemplo usa um script que é criado no código MOF.</span><span class="sxs-lookup"><span data-stu-id="fc9ff-127">The first example uses a script that is defined in an external file, and the second example uses a script that is built into the MOF code.</span></span> <span data-ttu-id="fc9ff-128">Os exemplos estão no código MOF, mas você pode criar as instâncias programaticamente usando a [API de script para WMI](scripting-api-for-wmi.md) ou a [API com para WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="fc9ff-128">The examples are in MOF code, but you can create the instances programmatically by using either the [Scripting API for WMI](scripting-api-for-wmi.md) or the [COM API for WMI](com-api-for-wmi.md).</span></span>

## <a name="example-using-an-external-script"></a><span data-ttu-id="fc9ff-129">Exemplo usando um script externo</span><span class="sxs-lookup"><span data-stu-id="fc9ff-129">Example Using an External Script</span></span>

<span data-ttu-id="fc9ff-130">O procedimento a seguir descreve como usar o exemplo de script externo.</span><span class="sxs-lookup"><span data-stu-id="fc9ff-130">The following procedure describes how to use the external script example.</span></span>

<span data-ttu-id="fc9ff-131">**Para usar o exemplo de script externo**</span><span class="sxs-lookup"><span data-stu-id="fc9ff-131">**To use the external script example**</span></span>

1.  <span data-ttu-id="fc9ff-132">Crie um arquivo chamado c: \\Asec.vbs e, em seguida, copie o script neste exemplo para ele.</span><span class="sxs-lookup"><span data-stu-id="fc9ff-132">Create a file named c:\\Asec.vbs, and then copy the script in this example into it.</span></span>
2.  <span data-ttu-id="fc9ff-133">Copie a lista MOF em um arquivo de texto e salve-a com uma extensão. mof.</span><span class="sxs-lookup"><span data-stu-id="fc9ff-133">Copy the MOF list into a text file and save it with a .mof extension.</span></span>
3.  <span data-ttu-id="fc9ff-134">Em uma janela de prompt de comando, compile o arquivo MOF usando o comando a seguir.</span><span class="sxs-lookup"><span data-stu-id="fc9ff-134">In a command prompt window, compile the MOF file by using the following command.</span></span>

    <span data-ttu-id="fc9ff-135"> *Nome do arquivo Mofcomp\ *\ * *. mof**</span><span class="sxs-lookup"><span data-stu-id="fc9ff-135">**Mofcomp** *filename\*\*\*.mof*\*</span></span>

4.  <span data-ttu-id="fc9ff-136">Execute a calculadora, que cria um processo de calc.exe.</span><span class="sxs-lookup"><span data-stu-id="fc9ff-136">Run the Calculator, which creates a calc.exe process.</span></span> <span data-ttu-id="fc9ff-137">Aguarde mais de cinco segundos, feche a janela da calculadora e, em seguida, examine o diretório C: \\ para obter um arquivo chamado ASEC. log.</span><span class="sxs-lookup"><span data-stu-id="fc9ff-137">Wait for more than five seconds, close the Calculator window, and then look in the C:\\ directory for a file named ASEC.log.</span></span>

    <span data-ttu-id="fc9ff-138">O texto a seguir é semelhante ao texto que estará contido no arquivo ASEC. log.</span><span class="sxs-lookup"><span data-stu-id="fc9ff-138">The following text is similar to the text that will be contained in the ASEC.log file.</span></span>

    ``` syntax
    Time: 12/31/2002 2:56:33 PM; Entry made by: ASEC
    Application closed. UserModeTime:  1562500; 
    KernelModeTime: 3125000 [hundreds of nanoseconds]
    ```

<span data-ttu-id="fc9ff-139">O exemplo de código VBScript a seguir mostra o script que é chamado quando um evento é recebido pelo consumidor permanente.</span><span class="sxs-lookup"><span data-stu-id="fc9ff-139">The following VBScript code example shows the script that is called when an event is received by the permanent consumer.</span></span> <span data-ttu-id="fc9ff-140">O objeto **TargetEvent** é uma instância [**\_ \_ InstanceDeletionEvent**](--instancedeletionevent.md) , de modo que tem uma propriedade chamada **TargetInstance**, que é uma instância de [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) usada para acionar o evento.</span><span class="sxs-lookup"><span data-stu-id="fc9ff-140">The **TargetEvent** object is an [**\_\_InstanceDeletionEvent**](--instancedeletionevent.md) instance so it has a property named **TargetInstance**, which is a [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) instance used to fire the event.</span></span> <span data-ttu-id="fc9ff-141">A **classe \_ process do Win32** tem as propriedades **usermodetime** e **KernelModeTime** que são colocadas no arquivo de log criado pelo script.</span><span class="sxs-lookup"><span data-stu-id="fc9ff-141">The **Win32\_Process** class has the **UserModeTime** and **KernelModeTime** properties that are put into the log file created by the script.</span></span>


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



<span data-ttu-id="fc9ff-142">O exemplo de código MOF a seguir chama o script quando um evento é recebido.</span><span class="sxs-lookup"><span data-stu-id="fc9ff-142">The following MOF code example calls the script when an event is received.</span></span> <span data-ttu-id="fc9ff-143">Ele cria o filtro, o consumidor e a associação entre eles no namespace **de \\ assinatura raiz** .</span><span class="sxs-lookup"><span data-stu-id="fc9ff-143">It creates the filter, consumer, and the binding between them in the **root\\subscription** namespace.</span></span>

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

## <a name="example-using-inline-script"></a><span data-ttu-id="fc9ff-144">Exemplo usando script embutido</span><span class="sxs-lookup"><span data-stu-id="fc9ff-144">Example Using Inline Script</span></span>

<span data-ttu-id="fc9ff-145">O procedimento a seguir descreve como usar o exemplo de script embutido.</span><span class="sxs-lookup"><span data-stu-id="fc9ff-145">The following procedure describes how to use the inline script example.</span></span>

<span data-ttu-id="fc9ff-146">**Para usar o exemplo de script embutido**</span><span class="sxs-lookup"><span data-stu-id="fc9ff-146">**To use the inline script example**</span></span>

1.  <span data-ttu-id="fc9ff-147">Copie a lista MOF nesta seção em um arquivo de texto e salve-a com uma extensão. mof.</span><span class="sxs-lookup"><span data-stu-id="fc9ff-147">Copy the MOF list in this section into a text file, and save it with a .mof extension.</span></span>
2.  <span data-ttu-id="fc9ff-148">Em uma janela de prompt de comando, compile o arquivo MOF usando o comando a seguir.</span><span class="sxs-lookup"><span data-stu-id="fc9ff-148">In a command prompt window, compile the MOF file by using the following command.</span></span>

    <span data-ttu-id="fc9ff-149"> *Nome do arquivo Mofcomp\ *\ * *. mof**</span><span class="sxs-lookup"><span data-stu-id="fc9ff-149">**Mofcomp** *filename\*\*\*.mof*\*</span></span>

<span data-ttu-id="fc9ff-150">O exemplo de código MOF a seguir cria o filtro, o consumidor e a associação entre eles e também contém o script embutido.</span><span class="sxs-lookup"><span data-stu-id="fc9ff-150">The following MOF code example creates the filter, consumer, and the binding between them and also contains the script inline.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="fc9ff-151">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fc9ff-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc9ff-152">Monitorando e respondendo a eventos com consumidores padrão</span><span class="sxs-lookup"><span data-stu-id="fc9ff-152">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 
