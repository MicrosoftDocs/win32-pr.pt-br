---
description: Usando a classe SMTPEventConsumer, você pode enviar um email para um usuário designado quando ocorrer um evento especificado. Essa classe é um consumidor de eventos padrão que o WMI fornece.
ms.assetid: ed10e6f7-8e18-4cde-bd46-a7791547c7da
ms.tgt_platform: multiple
title: Enviando email com base em um evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4929b7c8c29d514d73a6e4c9d14049a19f306233
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105797973"
---
# <a name="sending-email-based-on-an-event"></a><span data-ttu-id="5ee51-104">Enviando email com base em um evento</span><span class="sxs-lookup"><span data-stu-id="5ee51-104">Sending Email Based on an Event</span></span>

<span data-ttu-id="5ee51-105">Usando a classe [SMTPEventConsumer](smtpeventconsumer.md) , você pode enviar um email para um usuário designado quando ocorrer um evento especificado.</span><span class="sxs-lookup"><span data-stu-id="5ee51-105">By using the [SMTPEventConsumer](smtpeventconsumer.md) class, you can send email to a designated user when a specified event occurs.</span></span> <span data-ttu-id="5ee51-106">Essa classe é um [consumidor de eventos padrão](standard-consumer-classes.md) que o WMI fornece.</span><span class="sxs-lookup"><span data-stu-id="5ee51-106">This class is a [standard event consumer](standard-consumer-classes.md) that WMI provides.</span></span>

<span data-ttu-id="5ee51-107">A classe [SMTPEventConsumer](smtpeventconsumer.md) requer as seguintes condições para enviar uma mensagem de email em resposta a um evento:</span><span class="sxs-lookup"><span data-stu-id="5ee51-107">The [SMTPEventConsumer](smtpeventconsumer.md) class requires the following conditions to send an email message in response to an event:</span></span>

-   <span data-ttu-id="5ee51-108">A classe [SMTPEventConsumer](smtpeventconsumer.md) deve ser compilada no namespace correto.</span><span class="sxs-lookup"><span data-stu-id="5ee51-108">The [SMTPEventConsumer](smtpeventconsumer.md) class must be compiled into the correct namespace.</span></span> <span data-ttu-id="5ee51-109">Para obter mais informações, consulte [monitorando e respondendo a eventos com consumidores padrão](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="5ee51-109">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>
-   <span data-ttu-id="5ee51-110">Um servidor SMTP deve existir na rede.</span><span class="sxs-lookup"><span data-stu-id="5ee51-110">An SMTP server must exist on the network.</span></span>
-   <span data-ttu-id="5ee51-111">A mensagem de email não pode ter um anexo.</span><span class="sxs-lookup"><span data-stu-id="5ee51-111">The email message cannot have an attachment.</span></span>
-   <span data-ttu-id="5ee51-112">A mensagem de email deve ser codificada em US-ASCII.</span><span class="sxs-lookup"><span data-stu-id="5ee51-112">The email message must be encoded in US-ASCII.</span></span>

<span data-ttu-id="5ee51-113">O procedimento básico para usar consumidores padrão é sempre o mesmo e está localizado em [monitoramento e resposta a eventos com consumidores padrão](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="5ee51-113">The basic procedure for using standard consumers is always the same, and is located in [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span> <span data-ttu-id="5ee51-114">O procedimento a seguir adiciona ao procedimento básico; é específico para a classe [SMTPEventConsumer](smtpeventconsumer.md) ; e descreve como criar um consumidor de eventos que envia email.</span><span class="sxs-lookup"><span data-stu-id="5ee51-114">The following procedure adds to the basic procedure; is specific to the [SMTPEventConsumer](smtpeventconsumer.md) class; and describes how to create an event consumer that sends email.</span></span>

<span data-ttu-id="5ee51-115">O procedimento a seguir descreve como criar um consumidor de eventos que envia email.</span><span class="sxs-lookup"><span data-stu-id="5ee51-115">The following procedure describes how to create an event consumer that sends email.</span></span>

<span data-ttu-id="5ee51-116">**Para criar um consumidor de eventos que envia email**</span><span class="sxs-lookup"><span data-stu-id="5ee51-116">**To create an event consumer that sends email**</span></span>

1.  <span data-ttu-id="5ee51-117">Instale e registre a classe [SMTPEventConsumer](smtpeventconsumer.md) , se necessário.</span><span class="sxs-lookup"><span data-stu-id="5ee51-117">Install and register the [SMTPEventConsumer](smtpeventconsumer.md) class, if necessary.</span></span>

    <span data-ttu-id="5ee51-118">A classe [SMTPEventConsumer](smtpeventconsumer.md) é compilada no \\ namespace da assinatura raiz pelo programa de instalação do WMI.</span><span class="sxs-lookup"><span data-stu-id="5ee51-118">The [SMTPEventConsumer](smtpeventconsumer.md) class is compiled into the root\\subscription namespace by the WMI setup program.</span></span>

2.  <span data-ttu-id="5ee51-119">Identifique o evento que você deseja monitorar e crie a consulta de evento.</span><span class="sxs-lookup"><span data-stu-id="5ee51-119">Identify the event that you want to monitor and create the event query.</span></span>

    <span data-ttu-id="5ee51-120">Pode haver um evento intrínseco existente que use para monitorar seu evento.</span><span class="sxs-lookup"><span data-stu-id="5ee51-120">There might be an existing intrinsic event that use to monitor your event.</span></span> <span data-ttu-id="5ee51-121">A maioria dos eventos intrínsecos está associada às alterações nas instâncias de classe no namespace "raiz \\ cimv2".</span><span class="sxs-lookup"><span data-stu-id="5ee51-121">Most intrinsic events are associated with changes to class instances in the "root\\cimv2" namespace.</span></span> <span data-ttu-id="5ee51-122">Ao analisar as classes na referência de [classes WMI](wmi-classes.md) , você provavelmente encontrará uma classe que identifica o evento que deseja monitorar.</span><span class="sxs-lookup"><span data-stu-id="5ee51-122">By analyzing the classes in the [WMI Classes](wmi-classes.md) reference, you can probably find a class that identifies the event you want to monitor.</span></span> <span data-ttu-id="5ee51-123">Por exemplo, use a classe do [**\_ LogicalDisk do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) para monitorar alterações em uma unidade de disco rígido.</span><span class="sxs-lookup"><span data-stu-id="5ee51-123">For example, use the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class to monitor changes to a hard disk drive.</span></span>

    <span data-ttu-id="5ee51-124">Se não houver nenhum evento intrínseco existente que use, pode haver um provedor de eventos extrínsecos que pode funcionar.</span><span class="sxs-lookup"><span data-stu-id="5ee51-124">If there are no existing intrinsic events that use, there might be an extrinsic event provider that can work.</span></span> <span data-ttu-id="5ee51-125">Por exemplo, use a classe [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) do provedor de registro para monitorar alterações no registro do sistema.</span><span class="sxs-lookup"><span data-stu-id="5ee51-125">For example, use the [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) class of the Registry provider to monitor changes to the system registry.</span></span>

    <span data-ttu-id="5ee51-126">Se não existir uma classe que identifique o evento que você deseja monitorar, você deverá criar seu próprio provedor de eventos e definir novas classes de evento extrínsecos.</span><span class="sxs-lookup"><span data-stu-id="5ee51-126">If a class does not exist that identifies the event you want to monitor, you must create your own event provider and define new extrinsic event classes.</span></span> <span data-ttu-id="5ee51-127">Para obter mais informações, consulte [escrevendo um provedor de eventos](writing-an-event-provider.md).</span><span class="sxs-lookup"><span data-stu-id="5ee51-127">For more information, see [Writing an Event Provider](writing-an-event-provider.md).</span></span>

3.  <span data-ttu-id="5ee51-128">No arquivo formato MOF (MOF), crie uma instância do [SMTPEventConsumer](smtpeventconsumer.md) para receber eventos.</span><span class="sxs-lookup"><span data-stu-id="5ee51-128">In the Managed Object Format (MOF) file, create an instance of the [SMTPEventConsumer](smtpeventconsumer.md) to receive events.</span></span>

    <span data-ttu-id="5ee51-129">Use as propriedades da instância do para definir a mensagem de email a ser enviada quando um evento ocorrer.</span><span class="sxs-lookup"><span data-stu-id="5ee51-129">Use the properties of the instance to define the email message to send when an event occurs.</span></span> <span data-ttu-id="5ee51-130">Por exemplo, a propriedade **ToLine** define o endereço de email e a propriedade **Message** define o texto da mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="5ee51-130">For example, the **ToLine** property defines the email address, and the **Message** property defines the text of the email message.</span></span> <span data-ttu-id="5ee51-131">Você deve definir o endereço de email, o assunto e o texto de uma mensagem, mas uma mensagem de email não pode ter um anexo.</span><span class="sxs-lookup"><span data-stu-id="5ee51-131">You must define the email address, subject, and text of a message, but an email message cannot have an attachment.</span></span> <span data-ttu-id="5ee51-132">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="5ee51-132">For more information, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>

4.  <span data-ttu-id="5ee51-133">Crie uma consulta de evento que especifique os eventos que você deseja monitorar.</span><span class="sxs-lookup"><span data-stu-id="5ee51-133">Create an event query that specifies the events you want to monitor.</span></span>

    <span data-ttu-id="5ee51-134">Para obter mais informações, consulte [consultando com WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="5ee51-134">For more information, see [Querying with WQL](querying-with-wql.md).</span></span>

5.  <span data-ttu-id="5ee51-135">Crie uma instância de [**\_ \_ EventFilter**](--eventfilter.md) e armazene sua consulta na propriedade de **consulta** .</span><span class="sxs-lookup"><span data-stu-id="5ee51-135">Create an instance of [**\_\_EventFilter**](--eventfilter.md) and store your query in the **Query** property.</span></span>

    <span data-ttu-id="5ee51-136">Para obter mais informações, consulte [consultando com WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="5ee51-136">For more information see, [Querying with WQL](querying-with-wql.md).</span></span>

6.  <span data-ttu-id="5ee51-137">Crie uma instância de [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) para associar o filtro e o consumidor.</span><span class="sxs-lookup"><span data-stu-id="5ee51-137">Create an instance of [**\_\_FilterToConsumerBinding**](--filtertoconsumerbinding.md) to associate the filter and the consumer.</span></span>
7.  <span data-ttu-id="5ee51-138">Compile o arquivo MOF usando [**Mofcomp.exe**](mofcomp.md).</span><span class="sxs-lookup"><span data-stu-id="5ee51-138">Compile the MOF file by using [**Mofcomp.exe**](mofcomp.md).</span></span>


## <a name="example"></a><span data-ttu-id="5ee51-139">Exemplo</span><span class="sxs-lookup"><span data-stu-id="5ee51-139">Example</span></span>

<span data-ttu-id="5ee51-140">O exemplo nesta seção está no código MOF, mas você pode criar as instâncias programaticamente usando a [API de script para WMI](scripting-api-for-wmi.md) ou a [API com para WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="5ee51-140">The example in this section is in MOF code, but you can create the instances programmatically by using the [Scripting API for WMI](scripting-api-for-wmi.md) or the [COM API for WMI](com-api-for-wmi.md).</span></span>

<span data-ttu-id="5ee51-141">O procedimento a seguir descreve como usar o exemplo.</span><span class="sxs-lookup"><span data-stu-id="5ee51-141">The following procedure describes how to use the example.</span></span>

<span data-ttu-id="5ee51-142">**Para usar o exemplo**</span><span class="sxs-lookup"><span data-stu-id="5ee51-142">**To use the example**</span></span>

1.  <span data-ttu-id="5ee51-143">Copie o MOF a seguir para um arquivo de texto e salve-o com uma extensão. mof.</span><span class="sxs-lookup"><span data-stu-id="5ee51-143">Copy the following MOF to a text file and save it with a .mof extension.</span></span>
2.  <span data-ttu-id="5ee51-144">Em uma janela de prompt de comando, compile o arquivo MOF usando o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="5ee51-144">In a command prompt window, compile the MOF file by using the following command:</span></span>

    <span data-ttu-id="5ee51-145"> *Nome do arquivo Mofcomp\ *\ * *. mof**</span><span class="sxs-lookup"><span data-stu-id="5ee51-145">**Mofcomp** *filename\*\*\*.mof*\*</span></span>

> [!Note]  
> <span data-ttu-id="5ee51-146">Quando o código MOF é compilado no \\ namespace de assinatura raiz, o [SMTPEventConsumer](smtpeventconsumer.md) é compilado no mesmo namespace.</span><span class="sxs-lookup"><span data-stu-id="5ee51-146">When MOF code is compiled into the root\\subscription namespace, the [SMTPEventConsumer](smtpeventconsumer.md) is compiled into the same namespace.</span></span>

 

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

## <a name="related-topics"></a><span data-ttu-id="5ee51-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5ee51-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ee51-148">Monitorando e respondendo a eventos com consumidores padrão</span><span class="sxs-lookup"><span data-stu-id="5ee51-148">Monitoring and Responding to Events with Standard Consumers</span></span>](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 
