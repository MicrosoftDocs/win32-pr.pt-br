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
# <a name="running-a-program-from-the-command-line-based-on-an-event"></a><span data-ttu-id="43933-104">Executando um programa da linha de comando com base em um evento</span><span class="sxs-lookup"><span data-stu-id="43933-104">Running a Program from the Command Line Based on an Event</span></span>

<span data-ttu-id="43933-105">A classe [**CommandLineEventConsumer**](commandlineeventconsumer.md) executa um programa executável especificado de uma linha de comando quando ocorre um evento especificado.</span><span class="sxs-lookup"><span data-stu-id="43933-105">The [**CommandLineEventConsumer**](commandlineeventconsumer.md) class runs a specified executable program from a command line when a specified event occurs.</span></span> <span data-ttu-id="43933-106">Essa classe é um consumidor de eventos padrão que o WMI fornece.</span><span class="sxs-lookup"><span data-stu-id="43933-106">This class is a standard event consumer that WMI provides.</span></span>

<span data-ttu-id="43933-107">Ao usar o [**CommandLineEventConsumer**](commandlineeventconsumer.md), você deve proteger o executável que deseja iniciar.</span><span class="sxs-lookup"><span data-stu-id="43933-107">When you use [**CommandLineEventConsumer**](commandlineeventconsumer.md), you should secure the executable that you want to start.</span></span> <span data-ttu-id="43933-108">Se o executável não estiver em um local seguro ou não estiver protegido com uma ACL (lista de controle de acesso) forte, um usuário sem privilégios de acesso poderá substituir o executável por um executável diferente.</span><span class="sxs-lookup"><span data-stu-id="43933-108">If the executable is not in a secure location or not secured with a strong access control list (ACL), a user without access privileges can replace your executable with a different executable.</span></span> <span data-ttu-id="43933-109">Você pode usar as classes [**Win32 \_ LogicalFileSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting) ou [**Win32 \_ LogicalShareSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalsharesecuritysetting) para alterar programaticamente a segurança de um arquivo ou compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="43933-109">You can use the [**Win32\_LogicalFileSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting) or [**Win32\_LogicalShareSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalsharesecuritysetting) classes to change programmatically the security of a file or share.</span></span> <span data-ttu-id="43933-110">Para obter mais informações, consulte [criando um descritor de segurança para um novo objeto em C++](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span><span class="sxs-lookup"><span data-stu-id="43933-110">For more information, see [Creating a Security Descriptor for a New Object in C++](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span></span>

<span data-ttu-id="43933-111">O procedimento básico para usar consumidores padrão é sempre o mesmo e está localizado em [monitoramento e resposta a eventos com consumidores padrão](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="43933-111">The basic procedure to use standard consumers is always the same, and is located in [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span> <span data-ttu-id="43933-112">O procedimento a seguir adiciona o procedimento básico, é específico à classe [**CommandLineEventConsumer**](commandlineeventconsumer.md) e descreve como criar um consumidor de eventos que executa um programa.</span><span class="sxs-lookup"><span data-stu-id="43933-112">The following procedure adds to the basic procedure, is specific to the [**CommandLineEventConsumer**](commandlineeventconsumer.md) class, and describes how to create an event consumer that runs a program.</span></span>

> [!Caution]
>
> <span data-ttu-id="43933-113">A classe [**CommandLineEventConsumer**](commandlineeventconsumer.md) tem restrições de segurança especiais.</span><span class="sxs-lookup"><span data-stu-id="43933-113">The [**CommandLineEventConsumer**](commandlineeventconsumer.md) class has special security constraints.</span></span> <span data-ttu-id="43933-114">Esse consumidor padrão deve ser configurado por um membro local do grupo Administradores no computador local.</span><span class="sxs-lookup"><span data-stu-id="43933-114">This standard consumer must be configured by a local member of the Administrators group on the local computer.</span></span> <span data-ttu-id="43933-115">Se você usar uma conta de domínio para criar a assinatura, a conta LocalSystem deverá ter as permissões necessárias no domínio para verificar se o criador é membro do grupo local de administradores.</span><span class="sxs-lookup"><span data-stu-id="43933-115">If you use a domain account to create the subscription, the LocalSystem account must have the necessary permissions on the domain to verify that the creator is a member of the local Administrators group.</span></span>
>
> <span data-ttu-id="43933-116">[**CommandLineEventConsumer**](commandlineeventconsumer.md) não pode ser usado para iniciar um processo que é executado interativamente.</span><span class="sxs-lookup"><span data-stu-id="43933-116">[**CommandLineEventConsumer**](commandlineeventconsumer.md) cannot be used to start a process that runs interactively.</span></span>

 

<span data-ttu-id="43933-117">O procedimento a seguir descreve como criar um consumidor de eventos que executa um processo de uma linha de comando.</span><span class="sxs-lookup"><span data-stu-id="43933-117">The following procedure describes how to create an event consumer that runs a process from a command line.</span></span>

<span data-ttu-id="43933-118">**Para criar um consumidor de eventos que executa um processo de uma linha de comando**</span><span class="sxs-lookup"><span data-stu-id="43933-118">**To create an event consumer that runs a process from a command line**</span></span>

1.  <span data-ttu-id="43933-119">No arquivo formato MOF (MOF), crie uma instância de [**CommandLineEventConsumer**](commandlineeventconsumer.md) para receber os eventos solicitados na consulta.</span><span class="sxs-lookup"><span data-stu-id="43933-119">In the Managed Object Format (MOF) file, create an instance of [**CommandLineEventConsumer**](commandlineeventconsumer.md) to receive the events you request in the query.</span></span> <span data-ttu-id="43933-120">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="43933-120">For more information, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>
2.  <span data-ttu-id="43933-121">Crie uma instância de [**\_ \_ EventFilter**](--eventfilter.md) e dê um nome a ela.</span><span class="sxs-lookup"><span data-stu-id="43933-121">Create an instance of [**\_\_EventFilter**](--eventfilter.md) and give it a name.</span></span>
3.  <span data-ttu-id="43933-122">Crie uma consulta para especificar o tipo de evento.</span><span class="sxs-lookup"><span data-stu-id="43933-122">Create a query to specify the type of event.</span></span> <span data-ttu-id="43933-123">Para obter mais informações, consulte [consultando com WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="43933-123">For more information, see [Querying with WQL](querying-with-wql.md).</span></span>
4.  <span data-ttu-id="43933-124">Crie uma instância de [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) para associar o filtro à instância de [**CommandLineEventConsumer**](commandlineeventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="43933-124">Create an instance of [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) to associate the filter with the instance of [**CommandLineEventConsumer**](commandlineeventconsumer.md).</span></span>
5.  <span data-ttu-id="43933-125">Compile o arquivo MOF usando [**Mofcomp.exe**](mofcomp.md).</span><span class="sxs-lookup"><span data-stu-id="43933-125">Compile your MOF file by using [**Mofcomp.exe**](mofcomp.md).</span></span>

## <a name="example"></a><span data-ttu-id="43933-126">Exemplo</span><span class="sxs-lookup"><span data-stu-id="43933-126">Example</span></span>

<span data-ttu-id="43933-127">O exemplo de código a seguir cria uma nova classe chamada "MyCmdLineConsumer" para gerar eventos quando uma instância da nova classe é criada no final de um MOF.</span><span class="sxs-lookup"><span data-stu-id="43933-127">The following code example creates a new class called "MyCmdLineConsumer" to generate events when an instance of the new class is created at the end of a MOF.</span></span> <span data-ttu-id="43933-128">O exemplo está no código MOF, mas você pode criar as instâncias programaticamente usando a [API de script para WMI](scripting-api-for-wmi.md) ou a [API com para WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="43933-128">The example is in MOF code, but you can create the instances programmatically by using the [Scripting API for WMI](scripting-api-for-wmi.md) or the [COM API for WMI](com-api-for-wmi.md).</span></span>

<span data-ttu-id="43933-129">O procedimento a seguir descreve como criar uma nova classe chamada MyCmdLineConsumer.</span><span class="sxs-lookup"><span data-stu-id="43933-129">The following procedure describes how to create a new class called MyCmdLineConsumer.</span></span>

<span data-ttu-id="43933-130">**Para criar uma nova classe chamada MyCmdLineConsumer**</span><span class="sxs-lookup"><span data-stu-id="43933-130">**To create a new class called MyCmdLineConsumer**</span></span>

1.  <span data-ttu-id="43933-131">Crie o arquivo detest.bat do c: \\ cmdline \_ com um comando que execute um programa visível, como "calc.exe".</span><span class="sxs-lookup"><span data-stu-id="43933-131">Create the c:\\cmdline\_test.bat file with a command that executes a visible program, such as "calc.exe" .</span></span>
2.  <span data-ttu-id="43933-132">Copie o MOF para um arquivo de texto e salve-o com uma extensão. mof.</span><span class="sxs-lookup"><span data-stu-id="43933-132">Copy the MOF to a text file and save it with a .mof extension.</span></span>
3.  <span data-ttu-id="43933-133">Em um janela Comando, compile o arquivo MOF usando o seguinte comando: **Mofcomp filename. mof**.</span><span class="sxs-lookup"><span data-stu-id="43933-133">In a Command window, compile the MOF file by using the following command: **Mofcomp filename.mof**.</span></span>

> [!Note]  
> <span data-ttu-id="43933-134">O programa especificado em cmdline \_test.bat deve ser executado.</span><span class="sxs-lookup"><span data-stu-id="43933-134">The program specified in cmdline\_test.bat should execute.</span></span>

 

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

## <a name="related-topics"></a><span data-ttu-id="43933-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="43933-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43933-136">Monitorando e respondendo a eventos com consumidores padrão</span><span class="sxs-lookup"><span data-stu-id="43933-136">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 
