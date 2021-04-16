---
description: O WMI fornece uma interface uniforme para quaisquer aplicativos ou scripts locais ou remotos que obtêm dados de gerenciamento de um sistema de computador, rede ou empresa.
ms.assetid: 41ba2a64-3322-48b8-a6ea-e468bfac06e2
ms.tgt_platform: multiple
title: Arquitetura do WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b90ee4f81c2afdfc222dd7d5d824f88bda122b73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104562275"
---
# <a name="wmi-architecture"></a><span data-ttu-id="66a7a-103">Arquitetura do WMI</span><span class="sxs-lookup"><span data-stu-id="66a7a-103">WMI Architecture</span></span>

<span data-ttu-id="66a7a-104">O WMI fornece uma interface uniforme para quaisquer aplicativos ou scripts locais ou remotos que obtêm dados de gerenciamento de um sistema de computador, rede ou empresa.</span><span class="sxs-lookup"><span data-stu-id="66a7a-104">WMI provides a uniform interface for any local or remote applications or scripts that obtain management data from a computer system, a network, or an enterprise.</span></span> <span data-ttu-id="66a7a-105">A interface uniforme foi projetada de modo que os scripts e aplicativos cliente WMI não precisem chamar uma ampla variedade de interfaces de programação de aplicativo (APIs) do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="66a7a-105">The uniform interface is designed such that WMI client applications and scripts do not have to call a wide variety of operating system application programming interfaces (APIs).</span></span> <span data-ttu-id="66a7a-106">Muitas APIs não podem ser chamadas por clientes de automação, como scripts ou aplicativos Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="66a7a-106">Many APIs cannot be called by automation clients like scripts or Visual Basic applications.</span></span> <span data-ttu-id="66a7a-107">Outras APIs não fazem chamadas para computadores remotos.</span><span class="sxs-lookup"><span data-stu-id="66a7a-107">Other APIs do not make calls to remote computers.</span></span>

<span data-ttu-id="66a7a-108">Para obter dados do WMI, grave um script de cliente ou aplicativo que acesse as [classes WMI](wmi-classes.md) ou forneça dados para o WMI escrevendo um [*provedor WMI*](gloss-p.md).</span><span class="sxs-lookup"><span data-stu-id="66a7a-108">To obtain data from WMI, write a client script or application that accesses [WMI Classes](wmi-classes.md) or provide data to WMI by writing a [*WMI provider*](gloss-p.md).</span></span> <span data-ttu-id="66a7a-109">Para obter mais informações, consulte [usando o WMI](using-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="66a7a-109">For more information, see [Using WMI](using-wmi.md).</span></span>

## <a name="objects-consumers-and-infrastructure-of-wmi"></a><span data-ttu-id="66a7a-110">Objetos, consumidores e infraestrutura do WMI</span><span class="sxs-lookup"><span data-stu-id="66a7a-110">Objects, Consumers, and Infrastructure of WMI</span></span>

<span data-ttu-id="66a7a-111">O diagrama a seguir mostra a relação entre a infraestrutura do WMI e os provedores do WMI e os objetos gerenciados e também mostra a relação entre a infraestrutura do WMI e os consumidores do WMI.</span><span class="sxs-lookup"><span data-stu-id="66a7a-111">The following diagram shows the relationship between the WMI infrastructure and the WMI providers and managed objects, and it also shows the relationship between the WMI infrastructure and the WMI consumers.</span></span>

![relação entre a infraestrutura do WMI, os provedores de WMI e os objetos gerenciados](images/wmi-architecture.png)

## <a name="wmi-components"></a><span data-ttu-id="66a7a-113">Componentes WMI</span><span class="sxs-lookup"><span data-stu-id="66a7a-113">WMI Components</span></span>

<span data-ttu-id="66a7a-114">A lista a seguir descreve os principais componentes WMI:</span><span class="sxs-lookup"><span data-stu-id="66a7a-114">The following list describes the key WMI components:</span></span>

-   <span data-ttu-id="66a7a-115">Objetos gerenciados e provedores de WMI</span><span class="sxs-lookup"><span data-stu-id="66a7a-115">Managed objects and WMI providers</span></span>

    <span data-ttu-id="66a7a-116">Um provedor WMI é um objeto COM que monitora um ou mais [*objetos gerenciados*](gloss-m.md) para o WMI.</span><span class="sxs-lookup"><span data-stu-id="66a7a-116">A WMI provider is a COM object that monitors one or more [*managed objects*](gloss-m.md) for WMI.</span></span> <span data-ttu-id="66a7a-117">Um objeto gerenciado é um componente corporativo lógico ou físico, como uma unidade de disco rígido, adaptador de rede, sistema de banco de dados, sistema operacional, processo ou serviço.</span><span class="sxs-lookup"><span data-stu-id="66a7a-117">A managed object is a logical or physical enterprise component, such as a hard disk drive, network adapter, database system, operating system, process, or service.</span></span>

    <span data-ttu-id="66a7a-118">Semelhante a um driver, um provedor fornece o WMI com dados de um objeto gerenciado e manipula mensagens do WMI para o objeto gerenciado.</span><span class="sxs-lookup"><span data-stu-id="66a7a-118">Similar to a driver, a provider supplies WMI with data from a managed object and handles messages from WMI to the managed object.</span></span> <span data-ttu-id="66a7a-119">Os provedores WMI consistem em um arquivo DLL e um arquivo [*MOF (formato MOF)*](gloss-m.md) que define as classes para as quais o provedor retorna dados e executa operações.</span><span class="sxs-lookup"><span data-stu-id="66a7a-119">WMI providers consist of a DLL file and a [*Managed Object Format (MOF)*](gloss-m.md) file that defines the classes for which the provider returns data and performs operations.</span></span> <span data-ttu-id="66a7a-120">Provedores, como aplicativos WMI C++, usam a [API com para o WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="66a7a-120">Providers, like WMI C++ applications, use the [COM API for WMI](com-api-for-wmi.md).</span></span> <span data-ttu-id="66a7a-121">Para obter mais informações, consulte [fornecendo dados ao WMI](providing-data-to-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="66a7a-121">For more information, see [Providing Data to WMI](providing-data-to-wmi.md).</span></span>

    <span data-ttu-id="66a7a-122">Um exemplo de provedor é o [provedor de registro](/previous-versions/windows/desktop/regprov/system-registry-provider)pré-instalado, que acessa os dados no registro do sistema.</span><span class="sxs-lookup"><span data-stu-id="66a7a-122">An example of a provider is the preinstalled [Registry provider](/previous-versions/windows/desktop/regprov/system-registry-provider), which accesses data in the system registry.</span></span> <span data-ttu-id="66a7a-123">O provedor de registro tem uma [*classe WMI*](gloss-w.md), [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov), com muitos métodos, mas sem propriedades.</span><span class="sxs-lookup"><span data-stu-id="66a7a-123">The Registry provider has one [*WMI class*](gloss-w.md), [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov), with many methods but no properties.</span></span> <span data-ttu-id="66a7a-124">Outros provedores pré-instalados, como o [Provedor Win32](/windows/desktop/CIMWin32Prov/win32-provider), normalmente têm classes com muitas propriedades, mas poucos métodos, como o [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) ou o disco [**\_ lógico do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span><span class="sxs-lookup"><span data-stu-id="66a7a-124">Other preinstalled providers, such as the [Win32 provider](/windows/desktop/CIMWin32Prov/win32-provider), usually have classes with many properties but few methods, such as [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) or [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span></span> <span data-ttu-id="66a7a-125">O arquivo DLL do provedor de registro, Stdprov.dll, contém o código que retorna dados dinamicamente quando solicitado por scripts ou aplicativos cliente.</span><span class="sxs-lookup"><span data-stu-id="66a7a-125">The Registry provider DLL file, Stdprov.dll, contains the code that dynamically returns data when requested by client scripts or applications.</span></span>

    <span data-ttu-id="66a7a-126">Os arquivos MOF e DLL WMI estão localizados em% WINDIR% \\ System32 \\ WBEM, juntamente com as [ferramentas de Command-Line WMI](wmi-command-line-tools.md), como [**Winmgmt.exe**](winmgmt.md) e [**Mofcomp.exe**](mofcomp.md).</span><span class="sxs-lookup"><span data-stu-id="66a7a-126">WMI MOF and DLL files are located in %WINDIR%\\System32\\Wbem, along with the [WMI Command-Line Tools](wmi-command-line-tools.md), such as [**Winmgmt.exe**](winmgmt.md) and [**Mofcomp.exe**](mofcomp.md).</span></span> <span data-ttu-id="66a7a-127">As classes de provedor, como o [**\_ LogicalDisk do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), são definidas em arquivos MOF e, em seguida, compiladas no repositório WMI na inicialização do sistema.</span><span class="sxs-lookup"><span data-stu-id="66a7a-127">Provider classes, such as [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), are defined in MOF files, and then compiled into the WMI repository at system startup.</span></span>

-   [<span data-ttu-id="66a7a-128">Infraestrutura WMI</span><span class="sxs-lookup"><span data-stu-id="66a7a-128">WMI infrastructure</span></span>](wmi-infrastructure.md)

    <span data-ttu-id="66a7a-129">A infraestrutura do WMI é um componente do sistema operacional Microsoft Windows conhecido como o serviço WMI (Winmgmt).</span><span class="sxs-lookup"><span data-stu-id="66a7a-129">The WMI infrastructure is a Microsoft Windows operating system component know as the WMI service(winmgmt).</span></span> <span data-ttu-id="66a7a-130">A infraestrutura do WMI tem dois componentes: o núcleo do WMI e o [*repositório do WMI*](gloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="66a7a-130">The WMI infrastructure has two components: the WMI Core, and the [*WMI repository*](gloss-w.md).</span></span>

    <span data-ttu-id="66a7a-131">O repositório WMI é organizado por [*namespaces*](gloss-n.md)WMI.</span><span class="sxs-lookup"><span data-stu-id="66a7a-131">The WMI repository is organized by WMI [*namespaces*](gloss-n.md).</span></span> <span data-ttu-id="66a7a-132">O serviço WMI cria alguns namespaces como raiz \\ padrão, cimv2 raiz \\ e \\ assinatura raiz na inicialização do sistema e desinstala um conjunto padrão de definições de classe, incluindo as [classes Win32](/windows/desktop/CIMWin32Prov/win32-provider), as classes de [sistema WMI](wmi-system-classes.md)e outras.</span><span class="sxs-lookup"><span data-stu-id="66a7a-132">The WMI service creates some namespaces such as root\\default, root\\cimv2, and root\\subscription at system startup and preinstalls a default set of class definitions, including the [Win32 Classes](/windows/desktop/CIMWin32Prov/win32-provider), the [WMI System Classes](wmi-system-classes.md), and others.</span></span> <span data-ttu-id="66a7a-133">Os namespaces restantes encontrados no sistema são criados por provedores para outras partes do sistema operacional ou produtos.</span><span class="sxs-lookup"><span data-stu-id="66a7a-133">The remaining namespaces found on your system are created by providers for other parts of the operating system or products.</span></span> <span data-ttu-id="66a7a-134">Para obter mais informações e uma lista de provedores de WMI encontrados na maioria das versões do sistema operacional, consulte [provedores WMI](wmi-providers.md).</span><span class="sxs-lookup"><span data-stu-id="66a7a-134">For more information and a list of WMI providers found in most operating system versions, see [WMI Providers](wmi-providers.md).</span></span>

    <span data-ttu-id="66a7a-135">O serviço WMI atua como um intermediário entre os provedores, os aplicativos de gerenciamento e o repositório do WMI.</span><span class="sxs-lookup"><span data-stu-id="66a7a-135">The WMI service acts as an intermediary between the providers, management applications, and the WMI repository.</span></span> <span data-ttu-id="66a7a-136">Somente dados estáticos sobre objetos são armazenados no repositório, como as classes definidas pelos provedores.</span><span class="sxs-lookup"><span data-stu-id="66a7a-136">Only static data about objects is stored in the repository, such as the classes defined by providers.</span></span> <span data-ttu-id="66a7a-137">O WMI Obtém a maioria dos dados dinamicamente do provedor quando um cliente o solicita.</span><span class="sxs-lookup"><span data-stu-id="66a7a-137">WMI obtains most data dynamically from the provider when a client requests it.</span></span> <span data-ttu-id="66a7a-138">Você também pode configurar assinaturas para receber notificações de eventos de um provedor.</span><span class="sxs-lookup"><span data-stu-id="66a7a-138">You also can set up subscriptions to receive event notifications from a provider.</span></span> <span data-ttu-id="66a7a-139">Para obter mais informações, consulte [monitorando eventos](monitoring-events.md).</span><span class="sxs-lookup"><span data-stu-id="66a7a-139">For more information, see [Monitoring Events](monitoring-events.md).</span></span>

-   <span data-ttu-id="66a7a-140">Consumidores do WMI</span><span class="sxs-lookup"><span data-stu-id="66a7a-140">WMI consumers</span></span>

    <span data-ttu-id="66a7a-141">Um consumidor do WMI é um aplicativo de gerenciamento ou script que interage com a infraestrutura do WMI.</span><span class="sxs-lookup"><span data-stu-id="66a7a-141">A WMI consumer is a management application or script that interacts with the WMI infrastructure.</span></span> <span data-ttu-id="66a7a-142">Um aplicativo de gerenciamento pode consultar, enumerar dados, executar métodos de provedor ou assinar eventos chamando a [API com para WMI](com-api-for-wmi.md) ou a [API de script para WMI](scripting-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="66a7a-142">A management application can query, enumerate data, run provider methods, or subscribe to events by calling either the [COM API for WMI](com-api-for-wmi.md) or the [Scripting API for WMI](scripting-api-for-wmi.md).</span></span> <span data-ttu-id="66a7a-143">Os únicos dados ou ações disponíveis para um objeto gerenciado, como uma unidade de disco ou um serviço, são aqueles que um provedor fornece.</span><span class="sxs-lookup"><span data-stu-id="66a7a-143">The only data or actions available for a managed object, such as a disk drive or a service, are those that a provider supplies.</span></span>

## <a name="related-topics"></a><span data-ttu-id="66a7a-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="66a7a-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66a7a-145">Usando o WMI</span><span class="sxs-lookup"><span data-stu-id="66a7a-145">Using WMI</span></span>](using-wmi.md)
</dt> <dt>

[<span data-ttu-id="66a7a-146">Provedores de WMI</span><span class="sxs-lookup"><span data-stu-id="66a7a-146">WMI Providers</span></span>](wmi-providers.md)
</dt> <dt>

[<span data-ttu-id="66a7a-147">Criando um script ou aplicativo WMI</span><span class="sxs-lookup"><span data-stu-id="66a7a-147">Creating a WMI Application or Script</span></span>](creating-a-wmi-application-or-script.md)
</dt> <dt>

[<span data-ttu-id="66a7a-148">Tarefas do WMI para scripts e aplicativos</span><span class="sxs-lookup"><span data-stu-id="66a7a-148">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="66a7a-149">Fornecendo dados ao WMI</span><span class="sxs-lookup"><span data-stu-id="66a7a-149">Providing Data to WMI</span></span>](providing-data-to-wmi.md)
</dt> <dt>

[<span data-ttu-id="66a7a-150">Classes WMI</span><span class="sxs-lookup"><span data-stu-id="66a7a-150">WMI Classes</span></span>](wmi-classes.md)
</dt> <dt>

[<span data-ttu-id="66a7a-151">Eventos de monitoramento</span><span class="sxs-lookup"><span data-stu-id="66a7a-151">Monitoring Events</span></span>](monitoring-events.md)
</dt> <dt>

[<span data-ttu-id="66a7a-152">Chamando um método</span><span class="sxs-lookup"><span data-stu-id="66a7a-152">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 
