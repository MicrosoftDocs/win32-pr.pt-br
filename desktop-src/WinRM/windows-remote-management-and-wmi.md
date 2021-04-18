---
title: Gerenciamento Remoto do Windows e WMI
description: Gerenciamento Remoto do Windows pode ser usado para recuperar dados expostos por Instrumentação de Gerenciamento do Windows.
ms.assetid: a625440b-a839-487d-b862-e35934f24e1f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6942e89ea2e63ef809f3452e6ce55a493662c938
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "105763986"
---
# <a name="windows-remote-management-and-wmi"></a><span data-ttu-id="50701-103">Gerenciamento Remoto do Windows e WMI</span><span class="sxs-lookup"><span data-stu-id="50701-103">Windows Remote Management and WMI</span></span>

<span data-ttu-id="50701-104">Gerenciamento Remoto do Windows pode ser usado para recuperar dados expostos por Instrumentação de Gerenciamento do Windows ([WMI](/windows/desktop/WmiSdk/wmi-start-page) e [mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)).</span><span class="sxs-lookup"><span data-stu-id="50701-104">Windows Remote Management can be used to retrieve data exposed by Windows Management Instrumentation ([WMI](/windows/desktop/WmiSdk/wmi-start-page) and [MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)).</span></span> <span data-ttu-id="50701-105">Você pode obter dados do WMI com scripts ou aplicativos que usam a [API de script do WinRM](winrm-scripting-api.md) ou por meio da ferramenta de linha de comando **WinRM** .</span><span class="sxs-lookup"><span data-stu-id="50701-105">You can obtain WMI data with scripts or applications that use the [WinRM Scripting API](winrm-scripting-api.md) or through the **Winrm** command-line tool.</span></span>

<span data-ttu-id="50701-106">O WinRM oferece suporte à maioria das classes e operações WMI familiares, incluindo objetos incorporados.</span><span class="sxs-lookup"><span data-stu-id="50701-106">WinRM supports most of the familiar WMI classes and operations, including embedded objects.</span></span> <span data-ttu-id="50701-107">O WinRM pode aproveitar o WMI para coletar dados sobre [*recursos*](windows-remote-management-glossary.md) ou para gerenciar recursos em um sistema operacional baseado no Windows.</span><span class="sxs-lookup"><span data-stu-id="50701-107">WinRM can leverage WMI to collect data about [*resources*](windows-remote-management-glossary.md) or to manage resources on a Windows-based operating system.</span></span> <span data-ttu-id="50701-108">Isso significa que você pode obter dados sobre objetos como discos, adaptadores de rede, serviços ou processos em sua empresa por meio do conjunto existente de [classes WMI](/windows/desktop/WmiSdk/wmi-classes).</span><span class="sxs-lookup"><span data-stu-id="50701-108">That means that you can obtain data about objects such as disks, network adapters, services, or processes in your enterprise through the existing set of [WMI classes](/windows/desktop/WmiSdk/wmi-classes).</span></span> <span data-ttu-id="50701-109">Você também pode acessar os dados de hardware que estão disponíveis no provedor padrão de [IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)do WMI.</span><span class="sxs-lookup"><span data-stu-id="50701-109">You can also access the hardware data that is available from the standard WMI [IPMI provider](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).</span></span>

## <a name="identifying-a-wmi-resource"></a><span data-ttu-id="50701-110">Identificando um recurso WMI</span><span class="sxs-lookup"><span data-stu-id="50701-110">Identifying a WMI Resource</span></span>

<span data-ttu-id="50701-111">Você pode fazer referência a uma classe WMI como um [*recurso*](windows-remote-management-glossary.md) no WinRM e no protocolo WS-Management: um tipo de entidade gerenciada, como um serviço ou um disco.</span><span class="sxs-lookup"><span data-stu-id="50701-111">You can reference a WMI class as a [*resource*](windows-remote-management-glossary.md) in WinRM and in the WS-Management protocol: a type of managed entity, like a service or a disk.</span></span>

<span data-ttu-id="50701-112">Uma classe ou um método WMI é identificado por um [*URI*](windows-remote-management-glossary.md), assim como qualquer outro recurso é ao usar o protocolo WS-Management.</span><span class="sxs-lookup"><span data-stu-id="50701-112">A WMI class or method is identified by a [*URI*](windows-remote-management-glossary.md), just as any other resource is when using the WS-Management protocol.</span></span> <span data-ttu-id="50701-113">O URI pode especificar um recurso de WMI (classe), uma ação de WMI (método) ou identificar uma instância específica de uma classe em [*mensagens*](windows-remote-management-glossary.md) enviadas por uma rede.</span><span class="sxs-lookup"><span data-stu-id="50701-113">The URI can specify a WMI resource (class), a WMI action (method), or identify a specific instance of a class in [*messages*](windows-remote-management-glossary.md) sent over a network.</span></span> <span data-ttu-id="50701-114">Para obter mais informações, consulte [URIs de recurso](resource-uris.md).</span><span class="sxs-lookup"><span data-stu-id="50701-114">For more information, see [Resource URIs](resource-uris.md).</span></span>

## <a name="constructing-the-uri-prefix-for-wmi-classes"></a><span data-ttu-id="50701-115">Construindo o prefixo URI para classes WMI</span><span class="sxs-lookup"><span data-stu-id="50701-115">Constructing the URI Prefix for WMI Classes</span></span>

<span data-ttu-id="50701-116">O prefixo URI contém uma parte fixa e o namespace WMI.</span><span class="sxs-lookup"><span data-stu-id="50701-116">The URI prefix contains a fixed part and the WMI namespace.</span></span> <span data-ttu-id="50701-117">Por exemplo, o prefixo URI no Windows Server que contém a parte fixa do prefixo é: `http://schemas.microsoft.com/wbem/wsman/1/wmi/<WmiNamespace>` .</span><span class="sxs-lookup"><span data-stu-id="50701-117">For example, the URI prefix in Windows Server that contains the fixed part of the prefix is: `http://schemas.microsoft.com/wbem/wsman/1/wmi/<WmiNamespace>`.</span></span> <span data-ttu-id="50701-118">Isso permite que o prefixo de URI seja gerado para qualquer namespace WMI.</span><span class="sxs-lookup"><span data-stu-id="50701-118">This allows the URI prefix to be generated for any WMI namespace.</span></span> <span data-ttu-id="50701-119">Por exemplo, para acessar o namespace WMI **\\ padrão raiz** , use o seguinte prefixo de URI: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/default/` .</span><span class="sxs-lookup"><span data-stu-id="50701-119">For example, to access the **root\\default** WMI namespace, use the following URI prefix: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/default/`.</span></span>

<span data-ttu-id="50701-120">A maioria das classes WMI para gerenciamento está no namespace **raiz \\ cimv2** .</span><span class="sxs-lookup"><span data-stu-id="50701-120">The majority of the WMI classes for management are in the **root\\cimv2** namespace.</span></span> <span data-ttu-id="50701-121">Para acessar classes e instâncias no namespace **raiz \\ cimv2** , use o prefixo URI: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/` .</span><span class="sxs-lookup"><span data-stu-id="50701-121">To access classes and instances in **root\\cimv2** namespace, use the URI prefix: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/`.</span></span> <span data-ttu-id="50701-122">Para obter mais informações, consulte [URIs de recurso](resource-uris.md).</span><span class="sxs-lookup"><span data-stu-id="50701-122">For more information, see [Resource URIs](resource-uris.md).</span></span>

## <a name="generating-a-complete-uri-for-wmi-classes"></a><span data-ttu-id="50701-123">Gerando um URI completo para classes WMI</span><span class="sxs-lookup"><span data-stu-id="50701-123">Generating a Complete URI for WMI Classes</span></span>

<span data-ttu-id="50701-124">O URI que você fornece, seja para a ferramenta de linha de comando **WinRM** ou para um script, consiste no prefixo mais a especificação de recurso.</span><span class="sxs-lookup"><span data-stu-id="50701-124">The URI that you supply, either to the **Winrm** command-line tool or to a script, consists of the prefix plus the resource specification.</span></span>

<span data-ttu-id="50701-125">O procedimento a seguir descreve como gerar um URI de recurso para obter uma classe WMI ou para usar em uma operação enumerar.</span><span class="sxs-lookup"><span data-stu-id="50701-125">The following procedure describes how to generate a resource URI either to get a WMI class or to use in an enumerate operation.</span></span>

<span data-ttu-id="50701-126">**Para gerar um URI de recurso para uma classe WMI**</span><span class="sxs-lookup"><span data-stu-id="50701-126">**To generate a resource URI for a WMI class**</span></span>

1.  <span data-ttu-id="50701-127">Comece com o prefixo que indica que o esquema de protocolo de WS-Management deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="50701-127">Start with the prefix that indicates the WS-Management protocol schema should be used.</span></span>

    https://schemas.microsoft.com/wbem/wsman/1

    <span data-ttu-id="50701-128">O prefixo do URI de recurso para classes WMI é sempre o mesmo.</span><span class="sxs-lookup"><span data-stu-id="50701-128">The resource URI prefix for WMI classes is always the same.</span></span> <span data-ttu-id="50701-129">Para obter mais informações, consulte [prefixos de URI](uri-prefixes.md).</span><span class="sxs-lookup"><span data-stu-id="50701-129">For more information, see [URI Prefixes](uri-prefixes.md).</span></span>

2.  <span data-ttu-id="50701-130">Adicione o namespace WMI ao prefixo.</span><span class="sxs-lookup"><span data-stu-id="50701-130">Add the WMI namespace to the prefix.</span></span>

    `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/`

3.  <span data-ttu-id="50701-131">Adicione o nome da classe.</span><span class="sxs-lookup"><span data-stu-id="50701-131">Add the class name.</span></span>

    `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service`

4.  <span data-ttu-id="50701-132">Para definir o valor de uma propriedade ou para invocar um método específico, adicione o valor de chave ou os valores necessários para a classe.</span><span class="sxs-lookup"><span data-stu-id="50701-132">To set the value of a property, or to invoke a specific method, add the required key value or values for the class.</span></span>

    `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service?Name=Winmgmt`

    <span data-ttu-id="50701-133">Se você deixar o valor da chave em branco, não será alterado o valor da propriedade original.</span><span class="sxs-lookup"><span data-stu-id="50701-133">If you leave the key value blank, you will not alter the original property value.</span></span>

    > [!Note]  
    > <span data-ttu-id="50701-134">Deixar o valor da chave em branco define o valor da propriedade como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="50701-134">Leaving the key value blank sets the property value to **NULL**.</span></span>

     

## <a name="locating-a-wmi-resource-with-winrm"></a><span data-ttu-id="50701-135">Localizando um recurso WMI com o WinRM</span><span class="sxs-lookup"><span data-stu-id="50701-135">Locating a WMI Resource with WinRM</span></span>

<span data-ttu-id="50701-136">Você pode obter dados WMI por meio da ferramenta de linha de comando, **WinRM** ou por meio de um script de Visual Basic que usa a [API de script do WinRM](winrm-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="50701-136">You can obtain WMI data either through the command-line tool, **Winrm**, or through a Visual Basic script that uses the [WinRM Scripting API](winrm-scripting-api.md).</span></span> <span data-ttu-id="50701-137">Você não usa um [caminho WMI](/windows/desktop/WmiSdk/describing-the-location-of-a-wmi-object) para localizar um recurso.</span><span class="sxs-lookup"><span data-stu-id="50701-137">You do not use a [WMI path](/windows/desktop/WmiSdk/describing-the-location-of-a-wmi-object) to locate a resource.</span></span> <span data-ttu-id="50701-138">Em vez disso, você converte o namespace e a hierarquia do WMI em um [*URI*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="50701-138">Instead, you convert the WMI namespace and hierarchy to a [*URI*](windows-remote-management-glossary.md).</span></span>

<span data-ttu-id="50701-139">O URI do WinRM para uma classe WMI contém duas partes: o [prefixo do URI](uri-prefixes.md) e a classe que você deseja acessar.</span><span class="sxs-lookup"><span data-stu-id="50701-139">The WinRM URI for a WMI class contains two parts: the [URI prefix](uri-prefixes.md) and the class that you want to access.</span></span>

<span data-ttu-id="50701-140">Por exemplo, o URI a seguir pode ser fornecido para o método [**Session. Enumerate**](session-enumerate.md) para listar todos os serviços em um computador.</span><span class="sxs-lookup"><span data-stu-id="50701-140">For example, the following URI can be supplied to the [**Session.Enumerate**](session-enumerate.md) method to list all the services on a computer.</span></span> <span data-ttu-id="50701-141">O prefixo do URI é `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/` , e a classe é o [**\_ serviço Win32**](/windows/desktop/CIMWin32Prov/win32-service).</span><span class="sxs-lookup"><span data-stu-id="50701-141">The URI prefix is `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/`, and the class is [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>

`strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_CurrentTime"`

<span data-ttu-id="50701-142">No WMI, liste os dados de todas as instâncias de um recurso ou classe de várias maneiras:</span><span class="sxs-lookup"><span data-stu-id="50701-142">In WMI, list the data for all of the instances of a resource or class in several ways:</span></span>

-   <span data-ttu-id="50701-143">Uma consulta para todas as instâncias desse recurso.</span><span class="sxs-lookup"><span data-stu-id="50701-143">A query for all the instances of that resource.</span></span>

    `Set colServices = objWMIService.ExecQuery("Select * from Win32_Service")`

-   <span data-ttu-id="50701-144">Uma chamada para [**SWbemServices. InstancesOf**](/windows/desktop/WmiSdk/swbemservices-instancesof) ou [**SWbemObject. Instances \_**](/windows/desktop/WmiSdk/swbemobject-instances-).</span><span class="sxs-lookup"><span data-stu-id="50701-144">A call to [**SWbemServices.InstancesOf**](/windows/desktop/WmiSdk/swbemservices-instancesof) or [**SWbemObject.Instances\_**](/windows/desktop/WmiSdk/swbemobject-instances-).</span></span>

    `Set colServices = InstancesOf("Win32_Service")`

<span data-ttu-id="50701-145">No WinRM, há uma maneira de listar todas as instâncias de um recurso: [**Session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="50701-145">In WinRM, there is one way to list all of the instances of a resource: [**Session.Enumerate**](session-enumerate.md).</span></span>


```VB
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service"
Set colServices = objSession.Enumerate( strResource )
```



## <a name="locating-a-specific-instance-of-a-wmi-resource"></a><span data-ttu-id="50701-146">Localizando uma instância específica de um recurso WMI</span><span class="sxs-lookup"><span data-stu-id="50701-146">Locating a Specific Instance of a WMI Resource</span></span>

<span data-ttu-id="50701-147">No WMI, você pode designar uma instância específica de uma classe especificando valores para as propriedades de chave ou consultando uma instância que corresponda a uma lista de valores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="50701-147">In WMI, you can designate a particular instance of a class either by specifying values for the key properties or by querying for an instance that matches a list of property values.</span></span> <span data-ttu-id="50701-148">As propriedades de chave têm o [**qualificador de chave**](/windows/desktop/WmiSdk/key-qualifier)WMI.</span><span class="sxs-lookup"><span data-stu-id="50701-148">Key properties have the WMI [**Key qualifier**](/windows/desktop/WmiSdk/key-qualifier).</span></span>

<span data-ttu-id="50701-149">Você pode obter uma instância específica de uma classe de várias maneiras:</span><span class="sxs-lookup"><span data-stu-id="50701-149">You can obtain a specific instance of a class in several ways:</span></span>

-   <span data-ttu-id="50701-150">Uma chamada para [**Session. enumerar**](session-enumerate.md) com os parâmetros *Filter* e *Dialect* para criar uma consulta.</span><span class="sxs-lookup"><span data-stu-id="50701-150">A call to [**Session.Enumerate**](session-enumerate.md) with the *filter* and *dialect* parameters to create a query.</span></span>

    ```VB
    RemoteComputer = "servername.domain.com"
    strDialect = "http://schemas.microsoft.com/wbem/wsman/1/WQL"
    strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/*"
    Set objWsman = CreateObject("Wsman.Automation")
    Set objSession = objWsman.CreateSession("https://" & RemoteComputer)

    strFilter = "SELECT * FROM Win32_Share WHERE Name='Admin$'"
    Set objResultSet = objSession.Enumerate(strResource, strFilter, strDialect)
    ```

    

-   <span data-ttu-id="50701-151">Uma chamada para [**SWbemServices. Get**](/windows/desktop/WmiSdk/swbemservices-get).</span><span class="sxs-lookup"><span data-stu-id="50701-151">A call to [**SWbemServices.Get**](/windows/desktop/WmiSdk/swbemservices-get).</span></span> <span data-ttu-id="50701-152">Para [**Session. Get**](session-get.md), você deve fornecer um ou mais valores de chave específicos, precedidos por um ponto de interrogação (?).</span><span class="sxs-lookup"><span data-stu-id="50701-152">For [**Session.Get**](session-get.md), you must supply one or more specific key values, preceded by a question mark (?).</span></span>

    <span data-ttu-id="50701-153">O formato do URI para uma instância específica é `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/WMI\_Class?Key1=Value` .</span><span class="sxs-lookup"><span data-stu-id="50701-153">The format of the URI for a specific instance is `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/WMI\_Class?Key1=Value`.</span></span>

    ```VB
    strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service?Name=winmgmt"
    ```

    

    <span data-ttu-id="50701-154">Uma classe WMI pode ter mais de uma chave.</span><span class="sxs-lookup"><span data-stu-id="50701-154">A WMI class may have more than one key.</span></span> <span data-ttu-id="50701-155">Os pares nome-valor da chave são separados por um sinal "+".</span><span class="sxs-lookup"><span data-stu-id="50701-155">Key name-value pairs are separated by a "+" sign.</span></span> <span data-ttu-id="50701-156">Nesse caso, o formato é: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service?Key1=Value1+Key2=Value2` .</span><span class="sxs-lookup"><span data-stu-id="50701-156">In that case, the format is: `http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_Service?Key1=Value1+Key2=Value2`.</span></span>

    <span data-ttu-id="50701-157">A sintaxe do WinRM para obter um objeto WMI singleton é diferente do WMI.</span><span class="sxs-lookup"><span data-stu-id="50701-157">The WinRM syntax to obtain a singleton WMI object is different from WMI.</span></span> <span data-ttu-id="50701-158">Um singleton é uma classe WMI definida para que apenas uma instância seja permitida.</span><span class="sxs-lookup"><span data-stu-id="50701-158">A singleton is a WMI class defined so that only one instance is allowed.</span></span> <span data-ttu-id="50701-159">[**Win32 \_**](/previous-versions/windows/desktop/wmitimepprov/win32-currenttime) Os [**\_ WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting) atuais ou Win32 são exemplos de uma classe singleton WMI.</span><span class="sxs-lookup"><span data-stu-id="50701-159">[**Win32\_CurrentTime**](/previous-versions/windows/desktop/wmitimepprov/win32-currenttime) or [**Win32\_WMISetting**](/windows/desktop/CIMWin32Prov/win32-wmisetting) are examples of a WMI singleton class.</span></span>

    <span data-ttu-id="50701-160">A sintaxe de WMI para singletons é mostrada no exemplo de código VBScript a seguir.</span><span class="sxs-lookup"><span data-stu-id="50701-160">The WMI syntax for singletons is shown in the following VBScript code example.</span></span>

    ```VB
    Set TimeObject = objWMIService.Get("Win32_CurrentTime=@")
    ```

    

    <span data-ttu-id="50701-161">O exemplo a seguir mostra a sintaxe de singleton do WinRM que não usa "@".</span><span class="sxs-lookup"><span data-stu-id="50701-161">The following example shows the WinRM singleton syntax which does not use "@".</span></span>

    ```VB
    strResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_CurrentTime"
    ```

    

-   <span data-ttu-id="50701-162">Adicionando um [*seletor*](windows-remote-management-glossary.md) a um objeto [**ResourceLocator**](resourcelocator.md) ou [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) .</span><span class="sxs-lookup"><span data-stu-id="50701-162">Adding a [*selector*](windows-remote-management-glossary.md) to a [**ResourceLocator**](resourcelocator.md) or [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) object.</span></span>

    <span data-ttu-id="50701-163">O exemplo de código VBScript a seguir mostra como usar um seletor para obter uma instância específica do [**\_ processador Win32**](/windows/desktop/CIMWin32Prov/win32-processor).</span><span class="sxs-lookup"><span data-stu-id="50701-163">The following VBScript code example shows how to use a selector to get a specific instance of [**Win32\_Processor**](/windows/desktop/CIMWin32Prov/win32-processor).</span></span>

    ```VB
    strUri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Processor"
    Set objWsman = CreateObject("Wsman.Automation")
    Set Session = objWsman.CreateSession
    Set Locator = objWsman.CreateResourceLocator(strUri)
    Locator.AddSelector "DeviceID", "CPU0"
    ```

    

## <a name="related-topics"></a><span data-ttu-id="50701-164">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="50701-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50701-165">Sobre Gerenciamento Remoto do Windows</span><span class="sxs-lookup"><span data-stu-id="50701-165">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="50701-166">Prefixos de URI</span><span class="sxs-lookup"><span data-stu-id="50701-166">URI Prefixes</span></span>](uri-prefixes.md)
</dt> <dt>

[<span data-ttu-id="50701-167">URIs do Recurso</span><span class="sxs-lookup"><span data-stu-id="50701-167">Resource URIs</span></span>](resource-uris.md)
</dt> <dt>

[<span data-ttu-id="50701-168">Criando scripts no Gerenciamento Remoto do Windows</span><span class="sxs-lookup"><span data-stu-id="50701-168">Scripting in Windows Remote Management</span></span>](scripting-in-windows-remote-management.md)
</dt> </dl>
