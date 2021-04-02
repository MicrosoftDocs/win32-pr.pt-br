---
description: A classe LogFileEventConsumer pode gravar texto predefinido em um arquivo de log quando ocorrer um evento especificado. Essa classe é um consumidor de eventos padrão que o WMI fornece.
ms.assetid: c337e9f7-f40c-4d7d-a180-c053e24c882b
ms.tgt_platform: multiple
title: Gravando em um arquivo de log baseado em um evento
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 33cc82925b6afc1690f2cd87607f21e9ea02fdbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165314"
---
# <a name="writing-to-a-log-file-based-on-an-event"></a><span data-ttu-id="94c51-104">Gravando em um arquivo de log baseado em um evento</span><span class="sxs-lookup"><span data-stu-id="94c51-104">Writing to a Log File Based on an Event</span></span>

<span data-ttu-id="94c51-105">A classe [**LogFileEventConsumer**](logfileeventconsumer.md) pode gravar texto predefinido em um arquivo de log quando ocorrer um evento especificado.</span><span class="sxs-lookup"><span data-stu-id="94c51-105">The [**LogFileEventConsumer**](logfileeventconsumer.md) class can write predefined text to a log file when a specified event occurs.</span></span> <span data-ttu-id="94c51-106">Essa classe é um consumidor de eventos padrão que o WMI fornece.</span><span class="sxs-lookup"><span data-stu-id="94c51-106">This class is a standard event consumer that WMI provides.</span></span>

<span data-ttu-id="94c51-107">O procedimento básico para usar consumidores padrão é sempre o mesmo e está localizado em [monitoramento e resposta a eventos com consumidores padrão](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="94c51-107">The basic procedure for using standard consumers is always the same, and is located in [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="94c51-108">O procedimento a seguir adiciona o procedimento básico, é específico à classe [**LogFileEventConsumer**](logfileeventconsumer.md) e descreve como criar um consumidor de eventos que executa um programa.</span><span class="sxs-lookup"><span data-stu-id="94c51-108">The following procedure adds to the basic procedure, is specific to the [**LogFileEventConsumer**](logfileeventconsumer.md) class, and describes how to create an event consumer that runs a program.</span></span>

<span data-ttu-id="94c51-109">**Para criar um consumidor de eventos que grava em um arquivo de log**</span><span class="sxs-lookup"><span data-stu-id="94c51-109">**To create an event consumer that writes to a log file**</span></span>

1.  <span data-ttu-id="94c51-110">No arquivo formato MOF (MOF), crie uma instância de [**LogFileEventConsumer**](logfileeventconsumer.md) para receber os eventos solicitados na consulta, nomeie a instância na propriedade **Name** e coloque o caminho para o arquivo de log na propriedade **filename** .</span><span class="sxs-lookup"><span data-stu-id="94c51-110">In the Managed Object Format (MOF) file, create an instance of [**LogFileEventConsumer**](logfileeventconsumer.md) to receive the events you request in the query, name the instance in the **Name** property, and then place the path to the log file in the **Filename** property.</span></span>

    <span data-ttu-id="94c51-111">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="94c51-111">For more information, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>

2.  <span data-ttu-id="94c51-112">Forneça o modelo de texto para gravar no arquivo de log na propriedade Text.</span><span class="sxs-lookup"><span data-stu-id="94c51-112">Provide the text template to write to the log file in the Text property.</span></span>

    <span data-ttu-id="94c51-113">Para obter mais informações, consulte [usando modelos de cadeia de caracteres padrão](using-standard-string-templates.md).</span><span class="sxs-lookup"><span data-stu-id="94c51-113">For more information, see [Using Standard String Templates](using-standard-string-templates.md).</span></span>

3.  <span data-ttu-id="94c51-114">Crie uma instância de [**\_ \_ EventFilter**](--eventfilter.md) e defina uma consulta para especificar os eventos que ativarão o consumidor.</span><span class="sxs-lookup"><span data-stu-id="94c51-114">Create an instance of [**\_\_EventFilter**](--eventfilter.md) and define a query to specify the events that will activate the consumer.</span></span>

    <span data-ttu-id="94c51-115">Para obter mais informações, consulte [consultando com WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="94c51-115">For more information, see [Querying with WQL](querying-with-wql.md).</span></span>

4.  <span data-ttu-id="94c51-116">Crie uma instância de [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) para associar o filtro à instância de [**LogFileEventConsumer**](logfileeventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="94c51-116">Create an instance of [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) to associate the filter with the instance of [**LogFileEventConsumer**](logfileeventconsumer.md).</span></span>
5.  <span data-ttu-id="94c51-117">Para controlar quem lê ou grava em seu arquivo de log, defina a segurança no diretório em que o log está localizado no nível necessário.</span><span class="sxs-lookup"><span data-stu-id="94c51-117">To control who reads or writes to your log file, set the security on the directory where the log is located to the required level.</span></span>
6.  <span data-ttu-id="94c51-118">Compile o arquivo MOF usando [**Mofcomp.exe**](mofcomp.md).</span><span class="sxs-lookup"><span data-stu-id="94c51-118">Compile your MOF file using [**Mofcomp.exe**](mofcomp.md).</span></span>

## <a name="example"></a><span data-ttu-id="94c51-119">Exemplo</span><span class="sxs-lookup"><span data-stu-id="94c51-119">Example</span></span>

<span data-ttu-id="94c51-120">O exemplo nesta seção está no código MOF, mas você pode criar as instâncias programaticamente usando a [API de script para WMI](scripting-api-for-wmi.md) ou a [API com para WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="94c51-120">The example in this section is in MOF code, but you can create the instances programmatically by using the [Scripting API for WMI](scripting-api-for-wmi.md) or the [COM API for WMI](com-api-for-wmi.md).</span></span> <span data-ttu-id="94c51-121">O exemplo usa o LogFileEventConsumer padrão para criar uma classe de consumidor denominada LogFileEvent que grava uma linha no arquivo c: \\ logfile. log quando uma instância da classe LogFileEvent é criada.</span><span class="sxs-lookup"><span data-stu-id="94c51-121">The example uses the standard LogFileEventConsumer to create a consumer class named LogFileEvent that writes a line to the file c:\\Logfile.log when an instance of the class LogFileEvent is created.</span></span>

<span data-ttu-id="94c51-122">O procedimento a seguir descreve como usar o exemplo.</span><span class="sxs-lookup"><span data-stu-id="94c51-122">The following procedure describes how to use the example.</span></span>

<span data-ttu-id="94c51-123">**Para usar o exemplo**</span><span class="sxs-lookup"><span data-stu-id="94c51-123">**To use the example**</span></span>

1.  <span data-ttu-id="94c51-124">Copie a listagem MOF abaixo em um arquivo de texto e salve-a com uma extensão. mof.</span><span class="sxs-lookup"><span data-stu-id="94c51-124">Copy the MOF listing below into a text file and save it with a .mof extension.</span></span>
2.  <span data-ttu-id="94c51-125">Em uma janela de comando, compile o arquivo MOF usando o comando a seguir.</span><span class="sxs-lookup"><span data-stu-id="94c51-125">In a command window, compile the MOF file by using the following command.</span></span>

    <span data-ttu-id="94c51-126"> *Nome do arquivo Mofcomp\ *\ * *. mof**</span><span class="sxs-lookup"><span data-stu-id="94c51-126">**Mofcomp** *filename\*\*\*.mof*\*</span></span>

3.  <span data-ttu-id="94c51-127">Abra o arquivo logfile. log para ver a linha especificada por LogFileEvent.Name: "evento de consumidor de evento de logfile".</span><span class="sxs-lookup"><span data-stu-id="94c51-127">Open Logfile.log to see the line specified by LogFileEvent.Name: "Logfile Event Consumer event".</span></span>

``` syntax
// Set the namespace as root\subscription.
// The LogFileEventConsumer is already compiled 
//     in the root\subscription namespace. 

#pragma namespace ("\\\\.\\Root\\subscription")

class LogFileEvent
{
    [key]string Name;
};

// Create an instance of the standard log
// file consumer and give it the alias $CONSUMER

instance of LogFileEventConsumer as $CONSUMER
{
    // If the file does not already exist, it is created.
    Filename = "c:\\Logfile.log";  
    IsUnicode = FALSE;
    // Name of this instance of LogFileEventConsumer
    Name = "LogfileEventConsumer_Example";  
    // See "Using Standard String Templates"; 
    Text = "%TargetInstance.Name%"; 
    // TargetInstance is the instance of LogFileEvent 
    //    requested in the filter        
                                         
};

// Create an instance of the event filter 
// and give it the alias $FILTER
// Query for any instance operation type,
// such as instance creation, for LogFileEvent class

instance of __EventFilter as $FILTER
{
    Name = "LogFileFilter";
    Query = "SELECT * FROM __InstanceOperationEvent "
        "WHERE TargetInstance.__class = \"LogFileEvent\"";
    QueryLanguage = "WQL";
};

// Create an instance of the binding.

instance of __FilterToConsumerBinding
{
    Consumer=$CONSUMER;
    Filter=$FILTER;
 DeliverSynchronously=FALSE;
};

// Create an instance of this class right now
// Look at the file c:\Logfile.log to see
// that a line has been written.

instance of LogFileEvent
{
 Name = "Logfile Event Consumer event";  
};
```

## <a name="related-topics"></a><span data-ttu-id="94c51-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="94c51-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94c51-129">Monitorando e respondendo a eventos com consumidores padrão</span><span class="sxs-lookup"><span data-stu-id="94c51-129">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 



