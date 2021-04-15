---
title: URIs do Recurso
description: Um URI de recurso é um identificador para um tipo distinto de operação de gerenciamento ou valor usado pelos serviços de gerenciamento que implementam o protocolo de WS-Management.
ms.assetid: 478a6e5d-0675-462e-b2fd-fd2b5379e298
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 665c73caf5cf636ab7f0a0162f488ff073917984
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104499052"
---
# <a name="resource-uris"></a><span data-ttu-id="71fe9-103">URIs do Recurso</span><span class="sxs-lookup"><span data-stu-id="71fe9-103">Resource URIs</span></span>

<span data-ttu-id="71fe9-104">Um [*URI de recurso*](windows-remote-management-glossary.md) é um identificador para um tipo distinto de operação de gerenciamento ou valor usado pelos serviços de gerenciamento que implementam o protocolo de WS-Management.</span><span class="sxs-lookup"><span data-stu-id="71fe9-104">A [*resource URI*](windows-remote-management-glossary.md) is an identifier for a distinct type of management operation or value used by management services that implement the WS-Management protocol.</span></span> <span data-ttu-id="71fe9-105">Um valor de gerenciamento pode ser a temperatura dentro de um computador.</span><span class="sxs-lookup"><span data-stu-id="71fe9-105">A management value could be the temperature inside a computer.</span></span> <span data-ttu-id="71fe9-106">Um exemplo de uma operação de gerenciamento é iniciar um serviço interrompido ou definir uma cota de usuário de volume de disco.</span><span class="sxs-lookup"><span data-stu-id="71fe9-106">An example of a management operation is starting a stopped service or setting a disk volume user quota.</span></span>

## <a name="resource-uri-format"></a><span data-ttu-id="71fe9-107">Formato do URI de recurso</span><span class="sxs-lookup"><span data-stu-id="71fe9-107">Resource URI Format</span></span>

<span data-ttu-id="71fe9-108">Um URI consiste em um prefixo e um caminho para um recurso, como é mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="71fe9-108">A URI consists of a prefix and a path to a resource as is shown in the following example:</span></span>

<span data-ttu-id="71fe9-109">"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_LogicalDisk"</span><span class="sxs-lookup"><span data-stu-id="71fe9-109">"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_LogicalDisk"</span></span>

<span data-ttu-id="71fe9-110">Essa especificação de esquema indica que o URI é baseado na versão 1 do protocolo WS-Management oficial e que o recurso é um [**\_ LogicalDisk Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) no namespace "raiz \\ cimv2" do repositório do WMI.</span><span class="sxs-lookup"><span data-stu-id="71fe9-110">This schema specification indicates that the URI is based on version 1 of the official WS-Management protocol and that the resource is a [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) in the "root\\cimv2" namespace of the WMI repository.</span></span> <span data-ttu-id="71fe9-111">Os prefixos de URI contêm uma especificação de esquema, como "schemas.microsoft.com/wbem/wsman/1/wmi" e um tipo específico de recurso, como o **\_ LogicalDisk do Win32**.</span><span class="sxs-lookup"><span data-stu-id="71fe9-111">URI prefixes contain a schema specification, such as "schemas.microsoft.com/wbem/wsman/1/wmi" and a specific type of resource, such as **Win32\_LogicalDisk**.</span></span> <span data-ttu-id="71fe9-112">Para obter mais informações sobre como identificar uma instância específica de uma classe WMI, consulte [gerenciamento remoto do Windows e WMI](windows-remote-management-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="71fe9-112">For more information about identifying a specific instance of a WMI class, see [Windows Remote Management and WMI](windows-remote-management-and-wmi.md).</span></span>

<span data-ttu-id="71fe9-113">Para obter mais informações, consulte [prefixos de URI](uri-prefixes.md).</span><span class="sxs-lookup"><span data-stu-id="71fe9-113">For more information, see [URI Prefixes](uri-prefixes.md).</span></span>

## <a name="types-of-resource-uris"></a><span data-ttu-id="71fe9-114">Tipos de URIs de recurso</span><span class="sxs-lookup"><span data-stu-id="71fe9-114">Types of Resource URIs</span></span>

<span data-ttu-id="71fe9-115">Embora [*Instrumentação de gerenciamento do Windows (WMI)*](windows-remote-management-glossary.md) seja a principal fonte de dados de gerenciamento para sistemas operacionais baseados no Windows, também existem outras fontes de esquema de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="71fe9-115">While [*Windows Management Instrumentation (WMI)*](windows-remote-management-glossary.md) is the primary source of management data for Windows-based operating systems, other sources of management schema also exist.</span></span>

<span data-ttu-id="71fe9-116">A lista a seguir descreve vários tipos de URIs de recursos usados pelo Gerenciamento Remoto do Windows:</span><span class="sxs-lookup"><span data-stu-id="71fe9-116">The following list describes several types of resource URIs used by Windows Remote Management:</span></span>

-   <span data-ttu-id="71fe9-117">URIs de WMI</span><span class="sxs-lookup"><span data-stu-id="71fe9-117">WMI URIs</span></span>

    <span data-ttu-id="71fe9-118">Esse grupo de URIs representa um [*modelo CIM*](/windows/desktop/WmiSdk/gloss-c) caminho de classe que inclui o namespace e a classe.</span><span class="sxs-lookup"><span data-stu-id="71fe9-118">This group of URIs represent a [*Common Information Model*](/windows/desktop/WmiSdk/gloss-c) class path which includes namespace and class.</span></span>

    <span data-ttu-id="71fe9-119">Os URIs do WMI podem ser usados em:</span><span class="sxs-lookup"><span data-stu-id="71fe9-119">WMI URIs can be used in:</span></span>

    -   <span data-ttu-id="71fe9-120">Métodos de [**sessão**](session.md)</span><span class="sxs-lookup"><span data-stu-id="71fe9-120">[**Session**](session.md) methods</span></span>
    -   <span data-ttu-id="71fe9-121">Métodos [**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)</span><span class="sxs-lookup"><span data-stu-id="71fe9-121">[**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession) methods</span></span>
    -   <span data-ttu-id="71fe9-122">Métodos [**WSMan. CreateResourceLocator**](wsman-createresourcelocator.md) ou [**IWSMan. CreateResourceLocator**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-createresourcelocator)</span><span class="sxs-lookup"><span data-stu-id="71fe9-122">[**WSMan.CreateResourceLocator**](wsman-createresourcelocator.md) or [**IWSMan.CreateResourceLocator**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-createresourcelocator) methods</span></span>
    -   <span data-ttu-id="71fe9-123">Métodos [**ResourceLocator**](resourcelocator.md) ou [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator)</span><span class="sxs-lookup"><span data-stu-id="71fe9-123">[**ResourceLocator**](resourcelocator.md) or [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) methods</span></span>

-   <span data-ttu-id="71fe9-124">URIs IPMI</span><span class="sxs-lookup"><span data-stu-id="71fe9-124">IPMI URIs</span></span>

    <span data-ttu-id="71fe9-125">Esse grupo de URIs representa URIs padrão do setor baseados na versão 2,9 do CIM.</span><span class="sxs-lookup"><span data-stu-id="71fe9-125">This group of URIs represent industry standard URIs based upon CIM version 2.9.</span></span> <span data-ttu-id="71fe9-126">URIs IPMI podem ser usados em métodos de [**sessão**](session.md) [**Get**](session-get.md), [**Put**](session-put.md), [**Enumerate**](session-enumerate.md) e [**Invoke**](session-invoke.md).</span><span class="sxs-lookup"><span data-stu-id="71fe9-126">IPMI URIs can be used in [**Session**](session.md) methods [**Get**](session-get.md), [**Put**](session-put.md), [**Enumerate**](session-enumerate.md) , and [**Invoke**](session-invoke.md).</span></span>

    <span data-ttu-id="71fe9-127">Um exemplo é https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2/CIM_NumericSensor.xsd.</span><span class="sxs-lookup"><span data-stu-id="71fe9-127">An example is https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2/CIM_NumericSensor.xsd.</span></span> <span data-ttu-id="71fe9-128">Esse recurso é definido de acordo com o esquema CIM [DMTF.org](https://www.dmtf.org/home) .</span><span class="sxs-lookup"><span data-stu-id="71fe9-128">This resource is defined according to the [DMTF.org](https://www.dmtf.org/home) CIM schema.</span></span>

-   <span data-ttu-id="71fe9-129">URIs de configuração do WinRM</span><span class="sxs-lookup"><span data-stu-id="71fe9-129">WinRM configuration URIs</span></span>

    <span data-ttu-id="71fe9-130">Esse grupo de URIs são operações de configuração para a configuração do [*ouvinte*](windows-remote-management-glossary.md) do WinRM.</span><span class="sxs-lookup"><span data-stu-id="71fe9-130">This group of URIs are configuration operations for the WinRM [*listener*](windows-remote-management-glossary.md) configuration.</span></span>

    <span data-ttu-id="71fe9-131"> https://schemas.microsoft.com/wbem/wsman/1/config/listener pode ser usado em métodos de [**sessão**](session.md) [**Get**](session-get.md), [**Put**](session-put.md), [**Create**](session-create.md), [**delete**](session-delete.md)e [**Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="71fe9-131">https://schemas.microsoft.com/wbem/wsman/1/config/listener can be used in [**Session**](session.md) methods [**Get**](session-get.md), [**Put**](session-put.md), [**Create**](session-create.md), [**Delete**](session-delete.md), and [**Enumerate**](session-enumerate.md).</span></span>

-   <span data-ttu-id="71fe9-132">URIs de SEL ( [*log de eventos do sistema*](windows-remote-management-glossary.md) )</span><span class="sxs-lookup"><span data-stu-id="71fe9-132">[*System Event Log*](windows-remote-management-glossary.md) (SEL) URIs</span></span>

    <span data-ttu-id="71fe9-133">Esse grupo de URIs assina eventos do coletor de eventos do BMC.</span><span class="sxs-lookup"><span data-stu-id="71fe9-133">This group of URIs subscribes to Event Collector events from the BMC.</span></span> <span data-ttu-id="71fe9-134">Você pode assinar esses eventos usando a ferramenta de linha de comando **wevtutil** .</span><span class="sxs-lookup"><span data-stu-id="71fe9-134">You can subscribe to these events using the **Wevtutil** command-line tool.</span></span> <span data-ttu-id="71fe9-135">Para obter mais informações, consulte https://schemas.microsoft.com/wbem/wsman/1/logrecord/sel.</span><span class="sxs-lookup"><span data-stu-id="71fe9-135">For more information, see https://schemas.microsoft.com/wbem/wsman/1/logrecord/sel.</span></span>

## <a name="case-sensitivity"></a><span data-ttu-id="71fe9-136">Diferenciação de maiúsculas e minúsculas</span><span class="sxs-lookup"><span data-stu-id="71fe9-136">Case Sensitivity</span></span>

<span data-ttu-id="71fe9-137">O [*plug-in WMI*](windows-remote-management-glossary.md) preserva o caso do URI de recurso recebido em uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="71fe9-137">The [*WMI plug-in*](windows-remote-management-glossary.md) preserves the case of the resource URI received in a request.</span></span> <span data-ttu-id="71fe9-138">No entanto, para garantir a interoperabilidade com outras implementações do protocolo WS-Management, use o caso correto para o recurso solicitado no URI de recurso.</span><span class="sxs-lookup"><span data-stu-id="71fe9-138">However, to ensure interoperability with other implementations of WS-Management protocol, use the correct case for the requested resource in resource URI.</span></span> <span data-ttu-id="71fe9-139">O caso correto é a ortografia definida pelo provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="71fe9-139">The correct case is the spelling defined by the resource provider.</span></span>

<span data-ttu-id="71fe9-140">Enquanto os URIs de recurso não exigem diferenciação de maiúsculas e minúsculas, o [*fragmento*](windows-remote-management-glossary.md) XML faz.</span><span class="sxs-lookup"><span data-stu-id="71fe9-140">While resource URIs do not require case-sensitivity, [*fragment*](windows-remote-management-glossary.md) XML does.</span></span> <span data-ttu-id="71fe9-141">Um fragmento especifica apenas uma propriedade, em vez de todo o conjunto de propriedades de um recurso.</span><span class="sxs-lookup"><span data-stu-id="71fe9-141">A fragment specifies just one property, rather than the entire set of properties for a resource.</span></span> <span data-ttu-id="71fe9-142">No caso de recursos do WMI, a sintaxe do fragmento Obtém uma propriedade de uma instância de recurso.</span><span class="sxs-lookup"><span data-stu-id="71fe9-142">In the case of WMI resources, fragment syntax gets one property from a resource instance.</span></span> <span data-ttu-id="71fe9-143">Por exemplo, obter apenas a propriedade **version** de [**\_ OperatingSystem do Win32**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) requer o uso de um fragmento.</span><span class="sxs-lookup"><span data-stu-id="71fe9-143">For example, getting only the **Version** property from [**Win32\_OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem) requires using a fragment.</span></span> <span data-ttu-id="71fe9-144">Para obter mais informações sobre fragmentos, consulte "adicionando um seletor a um objeto ResourceLocator ou IWSManResourceLocator" em [gerenciamento remoto do Windows e WMI](windows-remote-management-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="71fe9-144">For more information about fragments, see "Adding a selector to a ResourceLocator or IWSManResourceLocator object" in [Windows Remote Management and WMI](windows-remote-management-and-wmi.md).</span></span>

<span data-ttu-id="71fe9-145">Seguindo os padrões de XML e [*XPath*](windows-remote-management-glossary.md) , o [*plug-in do WMI*](windows-remote-management-glossary.md) impõe a diferenciação de maiúsculas e minúsculas para fragmentos e XML que definem os parâmetros de entrada para um método.</span><span class="sxs-lookup"><span data-stu-id="71fe9-145">Following XML and [*XPath*](windows-remote-management-glossary.md) standards, the [*WMI plug-in*](windows-remote-management-glossary.md) enforces case-sensitivity for fragments and XML that defines the input parameters for a method.</span></span> <span data-ttu-id="71fe9-146">Diferenciar maiúsculas de minúsculas é necessário para dar suporte ao padrão XPath 1.0/nível 1.</span><span class="sxs-lookup"><span data-stu-id="71fe9-146">Case-sensitivity is required to support the XPath 1.0/Level 1 standard.</span></span> <span data-ttu-id="71fe9-147">Para obter dados WMI por meio do WinRM, a diferenciação de maiúsculas e minúsculas significa que os nomes de classes, propriedades e métodos WMI devem corresponder ao caso do nome encontrado no repositório WMI.</span><span class="sxs-lookup"><span data-stu-id="71fe9-147">To get WMI data through WinRM, case-sensitivity means that the names of WMI classes, properties, and methods must match the case of the name found in the WMI repository.</span></span>

<span data-ttu-id="71fe9-148">Para obter mais informações, consulte [Sintaxe XPath](/previous-versions/dotnet/netframework-4.0/ms256471(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="71fe9-148">For more information, see [XPath Syntax](/previous-versions/dotnet/netframework-4.0/ms256471(v=vs.100)).</span></span>

## <a name="case-sensitivity-examples"></a><span data-ttu-id="71fe9-149">Exemplos de sensibilidade de caso</span><span class="sxs-lookup"><span data-stu-id="71fe9-149">Case Sensitivity Examples</span></span>

<span data-ttu-id="71fe9-150">Por exemplo, um script que obtém a propriedade **de \_ descritor de segurança** de uma instância da classe de [**\_ serviço WMI Win32**](/windows/desktop/CIMWin32Prov/win32-service) não pode usar maiúsculas para os nomes no caminho do fragmento, somente o URI.</span><span class="sxs-lookup"><span data-stu-id="71fe9-150">For example, a script that obtains the **SECURITY\_DESCRIPTOR** property from an instance of the WMI [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) class cannot use upper-case for the names in the fragment path, only the URI.</span></span> <span data-ttu-id="71fe9-151">O [*plug-in do WMI*](windows-remote-management-glossary.md) do WinRM retorna um erro para o seguinte exemplo de VBScript porque o XML do XPath fornecido para o **FragmentPath** não usa o caso correto.</span><span class="sxs-lookup"><span data-stu-id="71fe9-151">The WinRM [*WMI plug-in*](windows-remote-management-glossary.md) returns an error for the following VBScript example because the XPath XML supplied for the **FragmentPath** does not use the correct case.</span></span> <span data-ttu-id="71fe9-152">No repositório WMI, a classe é escrita "serviço Win32 \_ ".</span><span class="sxs-lookup"><span data-stu-id="71fe9-152">In the WMI repository, the class is spelled "Win32\_Service".</span></span>


```VB
RResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/"_& "wmi/root/cimv2/Win32_Service?Name=winrm"
Set WSMan = CreateObject("WSMan.Automation")
Set Locator = WSMan.CreateResourceLocator(Resourceuri)
Locator.FragmentPath = "/Win32_SERVICE/Name"
Set Session = WSMan.Createsession
xml = Session.Get(Locator)
WScript.Echo xml
```



<span data-ttu-id="71fe9-153">A seguinte versão do mesmo exemplo mostra o uso correto do caso para a classe [**de \_ serviço do Win32**](/windows/desktop/CIMWin32Prov/win32-service) e a propriedade do **\_ descritor de segurança** .</span><span class="sxs-lookup"><span data-stu-id="71fe9-153">The following version of the same example shows the correct use of case for the [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) class and **SECURITY\_DESCRIPTOR** property.</span></span>


```VB
ResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/"_
    & "wmi/root/cimv2/Win32_Service?Name=winrm"
Set WSMan = CreateObject("WSMan.Automation")
Set Locator = WSMan.CreateResourceLocator(Resourceuri)
Locator.FragmentPath = "/Win32_Service/Name"
Set Session = WSMan.Createsession
xml = Session.Get(Locator)
WScript.Echo xml
```



## <a name="related-topics"></a><span data-ttu-id="71fe9-154">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="71fe9-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71fe9-155">Sobre Gerenciamento Remoto do Windows</span><span class="sxs-lookup"><span data-stu-id="71fe9-155">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="71fe9-156">Gerenciamento de hardware remoto</span><span class="sxs-lookup"><span data-stu-id="71fe9-156">Remote Hardware Management</span></span>](remote-hardware-management.md)
</dt> <dt>

[<span data-ttu-id="71fe9-157">**ResourceLocator**</span><span class="sxs-lookup"><span data-stu-id="71fe9-157">**ResourceLocator**</span></span>](resourcelocator.md)
</dt> </dl>

 

 