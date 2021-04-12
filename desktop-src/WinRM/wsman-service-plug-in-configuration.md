---
title: Configuração de plug-in do serviço WinRM
description: Um plug-in Gerenciamento Remoto do Windows (WinRM) deve ser registrado no catálogo do WinRM para permitir que a infraestrutura determine dinamicamente o conjunto de plug-ins disponíveis e os URIs de recursos aos quais eles dão suporte.
ms.assetid: d71cd244-3f10-40e3-a756-36cdf41b9cad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60bf618d71e55c6afd28de918198725895088559
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104294593"
---
# <a name="winrm-service-plug-in-configuration"></a><span data-ttu-id="45e12-103">Configuração de plug-in do serviço WinRM</span><span class="sxs-lookup"><span data-stu-id="45e12-103">WinRM Service Plug-in Configuration</span></span>

<span data-ttu-id="45e12-104">Um plug-in Gerenciamento Remoto do Windows (WinRM) deve ser registrado no catálogo do WinRM para permitir que a infraestrutura determine dinamicamente o conjunto de plug-ins disponíveis e os [*URIs de recursos*](windows-remote-management-glossary.md) aos quais eles dão suporte.</span><span class="sxs-lookup"><span data-stu-id="45e12-104">A Windows Remote Management (WinRM) plug-in must be registered in the WinRM catalog to enable the infrastructure to dynamically determine the set of available plug-ins and the [*resource URIs*](windows-remote-management-glossary.md) that they support.</span></span> <span data-ttu-id="45e12-105">Todos os [*URIs de recurso*](windows-remote-management-glossary.md) para plug-ins WinRM devem estar em conformidade com o formato definido no RFC 3986 ( [https://www.ietf.org/rfc/rfc3986.txt](https://www.ietf.org/rfc/rfc3986.txt) ).</span><span class="sxs-lookup"><span data-stu-id="45e12-105">All [*resource URIs*](windows-remote-management-glossary.md) for WinRM plug-ins should conform to the format that is defined in RFC 3986 ([https://www.ietf.org/rfc/rfc3986.txt](https://www.ietf.org/rfc/rfc3986.txt)).</span></span> <span data-ttu-id="45e12-106">A configuração é feita por meio do serviço WinRM principal.</span><span class="sxs-lookup"><span data-stu-id="45e12-106">Configuration is done through the main WinRM service.</span></span>

<span data-ttu-id="45e12-107">O comando a seguir registra uma configuração de plug-in com o serviço WinRM:</span><span class="sxs-lookup"><span data-stu-id="45e12-107">The following command registers a plug-in configuration with the WinRM service:</span></span>

```console
winrm create http://schemas.microsoft.com/wbem/wsman/1/config/plugin?name=MyPlugIn -file:myplugin.xml
```

> [!NOTE]
> <span data-ttu-id="45e12-108">O serviço WinRM precisa ser reiniciado para expor os plug-ins registrados recentemente.</span><span class="sxs-lookup"><span data-stu-id="45e12-108">The WinRM service needs to be restarted to expose the newly registered plug-ins.</span></span>

<span data-ttu-id="45e12-109">A configuração de plug-in é especificada em XML.</span><span class="sxs-lookup"><span data-stu-id="45e12-109">Plug-in configuration is specified in XML.</span></span> <span data-ttu-id="45e12-110">A seguir, é mostrado um exemplo.</span><span class="sxs-lookup"><span data-stu-id="45e12-110">The following is an example.</span></span>

```XML
<PlugInConfiguration xmlns="http://schemas.microsoft.com/wbem/wsman/1/config/PluginConfiguration" 
                     Name="MyPlugIn"
                     Filename="%systemroot%\system32\myplugin.dll" 
                     SDKVersion="1"
                     XmlRenderingType="text"
                     Architecture="64"
                     Enabled="true">

 <InitializationParameters>
  <Param Name="myParam1" Value="myValue1"/>
  <Param Name="myParam2" Value="myValue2"/>
 </InitializationParameters>

 <Resources>
  <Resource ResourceUri="https://schemas.MyCompany.com/MyUri1" SupportsOptions="true" ExactMatch="false">
   <Capability Type="Get" SupportsFragment="true"/>
   <Capability Type="Put" SupportsFragment="true"/>
   <Capability Type="Create"/>
   <Capability Type="Delete"/>
   <Capability Type="Invoke"/>
   <Capability Type="Enumerate" SupportsFiltering="true"/>
  </Resource>

  <Resource ResourceUri="https://schemas.MyCompany.com/MyUri2" SupportsOptions="false" ExactMatch="true">
   <Security Uri="https://schemas.MyCompany.com/MyUri2" Sddl="O:NSG:BAD:P(A;;GA;;;BA)"/>
   <Security Uri="https://schemas.MyCompany.com/MyUri2/MoreSpecific" Sddl="O:NSG:BAD:P(A;;GR;;;BA)" ExactMatch="true"/>
   <Capability Type="Shell"/>
  </Resource>
 </Resources>
</PlugInConfiguration>
```



<span data-ttu-id="45e12-111">A lista a seguir descreve os elementos XML em mais detalhes e é seguida pelo esquema de configuração especificado como um XSD.</span><span class="sxs-lookup"><span data-stu-id="45e12-111">The following list describes the XML elements in more detail and is followed by the configuration schema specified as an XSD.</span></span>

<dl> <dt>

<span data-ttu-id="45e12-112"><span id="PlugInConfiguration_OperationsConfiguration"></span><span id="pluginconfiguration_operationsconfiguration"></span><span id="PLUGINCONFIGURATION_OPERATIONSCONFIGURATION"></span>**PlugInConfiguration** / **OperationsConfiguration**</span><span class="sxs-lookup"><span data-stu-id="45e12-112"><span id="PlugInConfiguration_OperationsConfiguration"></span><span id="pluginconfiguration_operationsconfiguration"></span><span id="PLUGINCONFIGURATION_OPERATIONSCONFIGURATION"></span>**PlugInConfiguration**/**OperationsConfiguration**</span></span>
</dt> <dd>

<span data-ttu-id="45e12-113">Especifica o nome do arquivo do plug-in de operações.</span><span class="sxs-lookup"><span data-stu-id="45e12-113">Specifies the file name of the operations plug-in.</span></span> <span data-ttu-id="45e12-114">Todas as variáveis de ambiente colocadas nessa entrada serão expandidas no contexto dos usuários quando uma solicitação chegar.</span><span class="sxs-lookup"><span data-stu-id="45e12-114">Any environment variables that are put in this entry will be expanded in the users' context when a request comes in.</span></span> <span data-ttu-id="45e12-115">Cada usuário pode ter uma versão diferente da mesma variável de ambiente, de modo que cada usuário poderia acabar com um plug-in diferente.</span><span class="sxs-lookup"><span data-stu-id="45e12-115">Each user could have a different version of the same environment variable, so each user could end up with a different plug-in.</span></span> <span data-ttu-id="45e12-116">Essa entrada não pode ficar em branco e deve apontar para um plug-in válido.</span><span class="sxs-lookup"><span data-stu-id="45e12-116">This entry cannot be blank and must point to a valid plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="45e12-117"><span id="PlugInConfiguration_Name"></span><span id="pluginconfiguration_name"></span><span id="PLUGINCONFIGURATION_NAME"></span>**PlugInConfiguration** / **Nome** do</span><span class="sxs-lookup"><span data-stu-id="45e12-117"><span id="PlugInConfiguration_Name"></span><span id="pluginconfiguration_name"></span><span id="PLUGINCONFIGURATION_NAME"></span>**PlugInConfiguration**/**Name**</span></span>
</dt> <dd>

<span data-ttu-id="45e12-118">Especifica o nome de exibição a ser usado para o plug-in.</span><span class="sxs-lookup"><span data-stu-id="45e12-118">Specifies the display name to use for the plug-in.</span></span> <span data-ttu-id="45e12-119">Se um erro for retornado do plug-in, esse nome será colocado no XML de erro que é retornado para o aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="45e12-119">If an error is returned from the plug-in, this name will be put into the error XML that is returned to the client application.</span></span> <span data-ttu-id="45e12-120">O nome não é específico da localidade.</span><span class="sxs-lookup"><span data-stu-id="45e12-120">The name is not locale specific.</span></span>

</dd> <dt>

<span data-ttu-id="45e12-121"><span id="PlugInConfiguration_Architecture"></span><span id="pluginconfiguration_architecture"></span><span id="PLUGINCONFIGURATION_ARCHITECTURE"></span>**PlugInConfiguration** / **Arquitetura** do</span><span class="sxs-lookup"><span data-stu-id="45e12-121"><span id="PlugInConfiguration_Architecture"></span><span id="pluginconfiguration_architecture"></span><span id="PLUGINCONFIGURATION_ARCHITECTURE"></span>**PlugInConfiguration**/**Architecture**</span></span>
</dt> <dd>

<span data-ttu-id="45e12-122">Especifica se o plug-in de operações é de 32 bits ou 64 bits.</span><span class="sxs-lookup"><span data-stu-id="45e12-122">Specifies whether the operations plug-in is 32-bit or 64-bit.</span></span> <span data-ttu-id="45e12-123">Se esse elemento não for especificado, o valor padrão será "32" em sistemas x86 e "64" nos sistemas de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="45e12-123">If this element is not specified, the value will default to "32" on x86 systems and to "64" on 64-bit systems.</span></span> <span data-ttu-id="45e12-124">Para sistemas x86, o único valor válido é "32".</span><span class="sxs-lookup"><span data-stu-id="45e12-124">For x86 systems, the only valid value is "32".</span></span> <span data-ttu-id="45e12-125">Se o valor for "32" em um sistema de 64 bits, o redirecionamento do WOW64 precisará ser levado em conta ao inserir as informações de **nome de arquivo** .</span><span class="sxs-lookup"><span data-stu-id="45e12-125">If the value is "32" on an 64-bit system, wow64 redirection needs to be taken into account when entering the **Filename** information.</span></span> <span data-ttu-id="45e12-126">O sistema de arquivos subjacente usará o redirecionamento de WOW64 para converter system32 em SysWOW64.</span><span class="sxs-lookup"><span data-stu-id="45e12-126">The underlying file system will use wow64 redirection to translate system32 to syswow64.</span></span> <span data-ttu-id="45e12-127">Por exemplo, se **filename** for "% windir% \\ System32 \\myplugin.dll" e a **arquitetura** for "32", o arquivo de plug-in real estará localizado em "% windir% \\ SysWOW64 \\myplugin.dll".</span><span class="sxs-lookup"><span data-stu-id="45e12-127">For example, if **Filename** is "%windir%\\system32\\myplugin.dll" and **Architecture** is "32", the actual plug-in file is located at "%windir%\\syswow64\\myplugin.dll".</span></span>

</dd> <dt>

<span data-ttu-id="45e12-128"><span id="PlugInConfiguration_XmlRenderingType"></span><span id="pluginconfiguration_xmlrenderingtype"></span><span id="PLUGINCONFIGURATION_XMLRENDERINGTYPE"></span>**PlugInConfiguration** / **Xmlrenderizatype**</span><span class="sxs-lookup"><span data-stu-id="45e12-128"><span id="PlugInConfiguration_XmlRenderingType"></span><span id="pluginconfiguration_xmlrenderingtype"></span><span id="PLUGINCONFIGURATION_XMLRENDERINGTYPE"></span>**PlugInConfiguration**/**XmlRenderingType**</span></span>
</dt> <dd>

<span data-ttu-id="45e12-129">Configura o formato em que o XML é passado para plug-ins por meio do objeto de [**\_ dados WSMan**](/windows/desktop/api/Wsman/ns-wsman-wsman_data) .</span><span class="sxs-lookup"><span data-stu-id="45e12-129">Configures the format in which XML is passed to plug-ins through the [**WSMAN\_DATA**](/windows/desktop/api/Wsman/ns-wsman-wsman_data) object.</span></span> <span data-ttu-id="45e12-130">Os seguintes tipos estão disponíveis:</span><span class="sxs-lookup"><span data-stu-id="45e12-130">The following types are available:</span></span>

<dl> <dt>

<span data-ttu-id="45e12-131"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Texto</span><span class="sxs-lookup"><span data-stu-id="45e12-131"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Text</span></span>
</dt> <dd>

<span data-ttu-id="45e12-132">Os dados XML de entrada estão contidos em uma \_ estrutura de texto de tipo de dados WSMan \_ \_ , que representa o XML como um buffer de memória **PCWSTR** .</span><span class="sxs-lookup"><span data-stu-id="45e12-132">Incoming XML data is contained in a WSMAN\_DATA\_TYPE\_TEXT structure, which represents the XML as a **PCWSTR** memory buffer.</span></span>

</dd> <dt>

<span data-ttu-id="45e12-133"><span id="XMLReader"></span><span id="xmlreader"></span><span id="XMLREADER"></span>XMLReader</span><span class="sxs-lookup"><span data-stu-id="45e12-133"><span id="XMLReader"></span><span id="xmlreader"></span><span id="XMLREADER"></span>XMLReader</span></span>
</dt> <dd>

<span data-ttu-id="45e12-134">Os dados XML de entrada estão contidos em \_ uma \_ estrutura de leitor XML do WS tipo de dados \_ do WSMan \_ \_ , que representa o XML como um objeto **XmlReader** , que é definido no arquivo de cabeçalho WebServices. h.</span><span class="sxs-lookup"><span data-stu-id="45e12-134">Incoming XML data is contained in a WSMAN\_DATA\_TYPE\_WS\_XML\_READER structure, which represents the XML as an **XmlReader** object, which is defined in the WebServices.h header file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="45e12-135"><span id="PlugInConfiguration_InitializationXml"></span><span id="pluginconfiguration_initializationxml"></span><span id="PLUGINCONFIGURATION_INITIALIZATIONXML"></span>**PlugInConfiguration** / **InitializationXml**</span><span class="sxs-lookup"><span data-stu-id="45e12-135"><span id="PlugInConfiguration_InitializationXml"></span><span id="pluginconfiguration_initializationxml"></span><span id="PLUGINCONFIGURATION_INITIALIZATIONXML"></span>**PlugInConfiguration**/**InitializationXml**</span></span>
</dt> <dd>

<span data-ttu-id="45e12-136">Esse nó é opcional e permite que um plug-in configure o XML extra que será passado para o método [**WSManPluginStartup**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_startup).</span><span class="sxs-lookup"><span data-stu-id="45e12-136">This node is optional and allows a plug-in to configure extra XML that will be passed in to the [**WSManPluginStartup**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_startup)method.</span></span> <span data-ttu-id="45e12-137">A maioria dos plug-ins não precisará dessas informações adicionais, mas se um plug-in precisar ser usado em mais de um cenário que requer semântica de tempo de execução diferente, esse XML dará ao plug-in a flexibilidade para fazer isso.</span><span class="sxs-lookup"><span data-stu-id="45e12-137">Most plug-ins will not need this extra information, but if a plug-in needs to be used under more than one scenario that requires different run-time semantics, this XML will give the plug-in the flexibility to do this.</span></span>

</dd> <dt>

<span data-ttu-id="45e12-138"><span id="PlugInConfiguration_Resources"></span><span id="pluginconfiguration_resources"></span><span id="PLUGINCONFIGURATION_RESOURCES"></span>**PlugInConfiguration** / **Recursos** do</span><span class="sxs-lookup"><span data-stu-id="45e12-138"><span id="PlugInConfiguration_Resources"></span><span id="pluginconfiguration_resources"></span><span id="PLUGINCONFIGURATION_RESOURCES"></span>**PlugInConfiguration**/**Resources**</span></span>
</dt> <dd>

<span data-ttu-id="45e12-139">Especifica uma lista de [*URIs de recursos*](windows-remote-management-glossary.md)aos quais esse plug-in dá suporte.</span><span class="sxs-lookup"><span data-stu-id="45e12-139">Specifies a list of [*resource URIs*](windows-remote-management-glossary.md)that this plug-in supports.</span></span> <span data-ttu-id="45e12-140">Pelo menos uma entrada **ResourceURI** deve ser especificada; caso contrário, o XML será rejeitado.</span><span class="sxs-lookup"><span data-stu-id="45e12-140">At least one **ResourceUri** entry must be specified; otherwise, the XML will be rejected.</span></span>

</dd> <dt>

<span data-ttu-id="45e12-141"><span id="PlugInConfiguration_Resources_Resource"></span><span id="pluginconfiguration_resources_resource"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE"></span>**PlugInConfiguration** / **Recursos** / do **Recurso** do</span><span class="sxs-lookup"><span data-stu-id="45e12-141"><span id="PlugInConfiguration_Resources_Resource"></span><span id="pluginconfiguration_resources_resource"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE"></span>**PlugInConfiguration**/**Resources**/**Resource**</span></span>
</dt> <dd>

<span data-ttu-id="45e12-142">Representa uma configuração de [*URI de recurso*](windows-remote-management-glossary.md)único.</span><span class="sxs-lookup"><span data-stu-id="45e12-142">Represents a single [*resource URI*](windows-remote-management-glossary.md)configuration.</span></span>

> [!Note]  
> <span data-ttu-id="45e12-143">O atributo de **suporteoptions** pode ser definido como false.</span><span class="sxs-lookup"><span data-stu-id="45e12-143">The **SupportsOptions** attribute can be set to false.</span></span> <span data-ttu-id="45e12-144">Se o **suporteoptions** for definido como false, esse atributo não será listado quando o recurso for enumerado.</span><span class="sxs-lookup"><span data-stu-id="45e12-144">If **SupportsOptions** is set to false, this attribute is not listed when the resource is enumerated.</span></span>

 

</dd> <dt>

<span data-ttu-id="45e12-145"><span id="PlugInConfiguration_Resources_Resource_ResourceUri"></span><span id="pluginconfiguration_resources_resource_resourceuri"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_RESOURCEURI"></span>**PlugInConfiguration** / **Recursos** / do **Recurso** / do **ResourceURI**</span><span class="sxs-lookup"><span data-stu-id="45e12-145"><span id="PlugInConfiguration_Resources_Resource_ResourceUri"></span><span id="pluginconfiguration_resources_resource_resourceuri"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_RESOURCEURI"></span>**PlugInConfiguration**/**Resources**/**Resource**/**ResourceUri**</span></span>
</dt> <dd>

<span data-ttu-id="45e12-146">Especifica um único [*URI de recurso*](windows-remote-management-glossary.md) em completo ou como uma cadeia de caracteres de correspondência parcial com base no atributo **ExactMatch** .</span><span class="sxs-lookup"><span data-stu-id="45e12-146">Specifies a single [*resource URI*](windows-remote-management-glossary.md) either in full or as a partial match string based on the **ExactMatch** attribute.</span></span> <span data-ttu-id="45e12-147">Se **ExactMatch** não estiver presente, o padrão será **false**, o que significa que o processador SOAP do WinRM fará uma correspondência parcial com o início do *URI do recurso* e, se houver uma correspondência, passá-lo para o plug-in.</span><span class="sxs-lookup"><span data-stu-id="45e12-147">If **ExactMatch** is not present, it defaults to **False**, which means the WinRM SOAP processor will do a partial match to the start of the *resource URI* and, if there is a match, pass it to the plug-in.</span></span> <span data-ttu-id="45e12-148">O atributo de **suporteoptions** poderá ser especificado se esse *URI de recurso* tiver permissão para ter qualquer opção passada.</span><span class="sxs-lookup"><span data-stu-id="45e12-148">The **SupportsOptions** attribute can be specified if this *resource URI* is allowed to have any options passed in.</span></span> <span data-ttu-id="45e12-149">Por padrão, não há suporte para nenhuma opção e, se houver alguma presente na solicitação do cliente, será retornado um erro.</span><span class="sxs-lookup"><span data-stu-id="45e12-149">By default, no options are supported, and if any are present in the client request, an error will be returned.</span></span> <span data-ttu-id="45e12-150">Se houver suporte para as opções do plug-in, é importante que o plug-in retorne o erro correto se uma opção estiver presente de que o plug-in não entende quando o sinalizador **MustUnderstand** está definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="45e12-150">If options are supported by the plug-in, it is important that the plug-in returns the correct error if an option is present that the plug-in does not understand when the **mustUnderstand** flag is set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="45e12-151"><span id="PlugInConfiguration_Resources_Resource_Capability"></span><span id="pluginconfiguration_resources_resource_capability"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_CAPABILITY"></span>**PlugInConfiguration** / **Recursos** / do **Recurso** / do **Funcionalidade** do</span><span class="sxs-lookup"><span data-stu-id="45e12-151"><span id="PlugInConfiguration_Resources_Resource_Capability"></span><span id="pluginconfiguration_resources_resource_capability"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_CAPABILITY"></span>**PlugInConfiguration**/**Resources**/**Resource**/**Capability**</span></span>
</dt> <dd>

<span data-ttu-id="45e12-152">Especifica um recurso que está disponível neste [*URI de recurso*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="45e12-152">Specifies a capability that is available on this [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="45e12-153">Haverá uma entrada para cada tipo de operação que ele suporta.</span><span class="sxs-lookup"><span data-stu-id="45e12-153">There will be one entry for each type of operation that it supports.</span></span> <span data-ttu-id="45e12-154">As seguintes opções estão disponíveis:</span><span class="sxs-lookup"><span data-stu-id="45e12-154">The following options are available:</span></span>

<dl> <dt>

<span data-ttu-id="45e12-155"><span id="Get"></span><span id="get"></span><span id="GET"></span>Obter</span><span class="sxs-lookup"><span data-stu-id="45e12-155"><span id="Get"></span><span id="get"></span><span id="GET"></span>Get</span></span>
</dt> <dd>

<span data-ttu-id="45e12-156">Há suporte para operações Get no [*URI do recurso*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="45e12-156">Get operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="45e12-157">O atributo **SupportFragment** será usado se a operação get der suporte ao conceito.</span><span class="sxs-lookup"><span data-stu-id="45e12-157">The **SupportFragment** attribute is used if the get operation supports the concept.</span></span> <span data-ttu-id="45e12-158">O atributo **SupportFiltering** não é válido e deve ser definido como false.</span><span class="sxs-lookup"><span data-stu-id="45e12-158">The **SupportFiltering** attribute is not valid and should be set to false.</span></span> <span data-ttu-id="45e12-159">Esse recurso não será válido para um *URI de recurso* se também houver suporte para operações de Shell.</span><span class="sxs-lookup"><span data-stu-id="45e12-159">This capability is not valid for a *resource URI* if shell operations are also supported.</span></span>

</dd> <dt>

<span data-ttu-id="45e12-160"><span id="Put"></span><span id="put"></span><span id="PUT"></span>Posicione</span><span class="sxs-lookup"><span data-stu-id="45e12-160"><span id="Put"></span><span id="put"></span><span id="PUT"></span>Put</span></span>
</dt> <dd>

<span data-ttu-id="45e12-161">As operações Put têm suporte no [*URI de recurso*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="45e12-161">Put operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="45e12-162">O atributo **SupportFragment** será usado se a operação Put der suporte ao conceito.</span><span class="sxs-lookup"><span data-stu-id="45e12-162">The **SupportFragment** attribute is used if the put operation supports the concept.</span></span> <span data-ttu-id="45e12-163">O atributo **SupportFiltering** não é válido e deve ser definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="45e12-163">The **SupportFiltering** attribute is not valid and should be set to **False**.</span></span> <span data-ttu-id="45e12-164">Esse recurso não será válido para um *URI de recurso* se também houver suporte para operações de Shell.</span><span class="sxs-lookup"><span data-stu-id="45e12-164">This capability is not valid for a *resource URI* if shell operations are also supported.</span></span>

</dd> <dt>

<span data-ttu-id="45e12-165"><span id="Create"></span><span id="create"></span><span id="CREATE"></span>Criada</span><span class="sxs-lookup"><span data-stu-id="45e12-165"><span id="Create"></span><span id="create"></span><span id="CREATE"></span>Create</span></span>
</dt> <dd>

<span data-ttu-id="45e12-166">Há suporte para operações de criação no [*URI de recurso*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="45e12-166">Create operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="45e12-167">O atributo **SupportFragment** será usado se a operação de criação der suporte ao conceito.</span><span class="sxs-lookup"><span data-stu-id="45e12-167">The **SupportFragment** attribute is used if the create operation supports the concept.</span></span> <span data-ttu-id="45e12-168">O atributo **SupportFiltering** não é válido e deve ser definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="45e12-168">The **SupportFiltering** attribute is not valid and should be set to **False**.</span></span> <span data-ttu-id="45e12-169">Esse recurso não será válido para um *URI de recurso* se também houver suporte para operações de Shell.</span><span class="sxs-lookup"><span data-stu-id="45e12-169">This capability is not valid for a *resource URI* if shell operations are also supported.</span></span>

</dd> <dt>

<span data-ttu-id="45e12-170"><span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>Apagar</span><span class="sxs-lookup"><span data-stu-id="45e12-170"><span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>Delete</span></span>
</dt> <dd>

<span data-ttu-id="45e12-171">As operações de exclusão têm suporte no [*URI de recurso*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="45e12-171">Delete operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="45e12-172">O atributo **SupportFragment** será usado se a operação de exclusão der suporte ao conceito.</span><span class="sxs-lookup"><span data-stu-id="45e12-172">The **SupportFragment** attribute is used if the delete operation supports the concept.</span></span> <span data-ttu-id="45e12-173">O atributo **SupportFiltering** não é válido e deve ser definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="45e12-173">The **SupportFiltering** attribute is not valid and should be set to **False**.</span></span> <span data-ttu-id="45e12-174">Esse recurso não será válido para um *URI de recurso* se também houver suporte para operações de Shell.</span><span class="sxs-lookup"><span data-stu-id="45e12-174">This capability is not valid for a *resource URI* if shell operations are also supported.</span></span>

</dd> <dt>

<span data-ttu-id="45e12-175"><span id="Invoke"></span><span id="invoke"></span><span id="INVOKE"></span>Chame</span><span class="sxs-lookup"><span data-stu-id="45e12-175"><span id="Invoke"></span><span id="invoke"></span><span id="INVOKE"></span>Invoke</span></span>
</dt> <dd>

<span data-ttu-id="45e12-176">As operações Invoke têm suporte no [*URI de recurso*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="45e12-176">Invoke operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="45e12-177">O atributo **SupportFragment** não tem suporte para operações Invoke e deve ser definido como false.</span><span class="sxs-lookup"><span data-stu-id="45e12-177">The **SupportFragment** attribute is not supported for invoke operations and should be set to false.</span></span> <span data-ttu-id="45e12-178">O atributo **SupportFiltering** não é válido e deve ser definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="45e12-178">The **SupportFiltering** attribute is not valid and should be set to **False**.</span></span> <span data-ttu-id="45e12-179">Esse recurso não será válido para um *URI de recurso* se também houver suporte para operações de Shell.</span><span class="sxs-lookup"><span data-stu-id="45e12-179">This capability is not valid for a *resource URI* if shell operations are also supported.</span></span>

</dd> <dt>

<span data-ttu-id="45e12-180"><span id="Enumerate"></span><span id="enumerate"></span><span id="ENUMERATE"></span>Enumera</span><span class="sxs-lookup"><span data-stu-id="45e12-180"><span id="Enumerate"></span><span id="enumerate"></span><span id="ENUMERATE"></span>Enumerate</span></span>
</dt> <dd>

<span data-ttu-id="45e12-181">As operações de enumeração têm suporte no [*URI de recurso*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="45e12-181">Enumerate operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="45e12-182">O atributo **SupportFragment** não tem suporte para operações de enumeração e deve ser definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="45e12-182">The **SupportFragment** attribute is not supported for enumerate operations and should be set to **False**.</span></span> <span data-ttu-id="45e12-183">O atributo **SupportFiltering** é válido e, se o plug-in der suporte à filtragem, esse atributo deverá ser definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="45e12-183">The **SupportFiltering** attribute is valid, and if the plug-in supports filtering this attribute should be set to **True**.</span></span> <span data-ttu-id="45e12-184">Esse recurso não será válido para um *URI de recurso* se também houver suporte para operações de Shell.</span><span class="sxs-lookup"><span data-stu-id="45e12-184">This capability is not valid for a *resource URI* if shell operations are also supported.</span></span>

</dd> <dt>

<span data-ttu-id="45e12-185"><span id="Subscribe"></span><span id="subscribe"></span><span id="SUBSCRIBE"></span>Faça</span><span class="sxs-lookup"><span data-stu-id="45e12-185"><span id="Subscribe"></span><span id="subscribe"></span><span id="SUBSCRIBE"></span>Subscribe</span></span>
</dt> <dd>

<span data-ttu-id="45e12-186">As operações de assinatura têm suporte no [*URI de recurso*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="45e12-186">Subscribe operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="45e12-187">O atributo **SupportFragment** não tem suporte para operações de assinatura e deve ser definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="45e12-187">The **SupportFragment** attribute is not supported for subscribe operations and should be set to **False**.</span></span> <span data-ttu-id="45e12-188">O atributo **SupportFiltering** não é válido e deve ser definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="45e12-188">The **SupportFiltering** attribute is not valid and should be set to **False**.</span></span> <span data-ttu-id="45e12-189">Esse recurso não será válido para um *URI de recurso* se também houver suporte para operações de Shell.</span><span class="sxs-lookup"><span data-stu-id="45e12-189">This capability is not valid for a *resource URI* if shell operations are also supported.</span></span>

</dd> <dt>

<span data-ttu-id="45e12-190"><span id="Shell"></span><span id="shell"></span><span id="SHELL"></span>Shell</span><span class="sxs-lookup"><span data-stu-id="45e12-190"><span id="Shell"></span><span id="shell"></span><span id="SHELL"></span>Shell</span></span>
</dt> <dd>

<span data-ttu-id="45e12-191">Há suporte para operações de Shell no [*URI de recurso*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="45e12-191">Shell operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="45e12-192">O atributo **SupportFragment** não tem suporte para operações de shell e deve ser definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="45e12-192">The **SupportFragment** attribute is not supported for shell operations and should be set to **False**.</span></span> <span data-ttu-id="45e12-193">O atributo **SupportFiltering** não é válido e deve ser definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="45e12-193">The **SupportFiltering** attribute is not valid and should be set to **False**.</span></span> <span data-ttu-id="45e12-194">Esse recurso não será válido para um *URI de recurso* se qualquer outra funcionalidade de operação também tiver suporte.</span><span class="sxs-lookup"><span data-stu-id="45e12-194">This capability is not valid for a *resource URI* if any other operation capability is also supported.</span></span> <span data-ttu-id="45e12-195">Se uma funcionalidade de operação do Shell estiver configurada para um *URI de recurso*, as operações obter, colocar, criar, excluir, invocar e enumerar serão processadas internamente no serviço WinRM para gerenciar shells.</span><span class="sxs-lookup"><span data-stu-id="45e12-195">If a shell operation capability is configured for a *resource URI*, then get, put, create, delete, invoke, and enumerate operations are processed internally within the WinRm service to manage shells.</span></span> <span data-ttu-id="45e12-196">Como resultado, o plug-in não pode lidar com as operações em si.</span><span class="sxs-lookup"><span data-stu-id="45e12-196">As a result, the plug-in cannot deal with the operations itself.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="45e12-197"><span id="PlugInConfiguration_Resources_Resource_Security"></span><span id="pluginconfiguration_resources_resource_security"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_SECURITY"></span>**PlugInConfiguration** / **Recursos** / do **Recurso** / do **Segurança** do</span><span class="sxs-lookup"><span data-stu-id="45e12-197"><span id="PlugInConfiguration_Resources_Resource_Security"></span><span id="pluginconfiguration_resources_resource_security"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_SECURITY"></span>**PlugInConfiguration**/**Resources**/**Resource**/**Security**</span></span>
</dt> <dd>

<span data-ttu-id="45e12-198">Esse elemento define o descritor de segurança (por meio do atributo **SDDL** ) que deve ser aplicado para determinar o acesso a um [*URI de recurso*](windows-remote-management-glossary.md) específico (por meio do atributo **URI** ).</span><span class="sxs-lookup"><span data-stu-id="45e12-198">This element defines the security descriptor (via the **Sddl** attribute) that should be applied to determine access to a particular [*resource URI*](windows-remote-management-glossary.md) (via the **Uri** attribute).</span></span> <span data-ttu-id="45e12-199">Se **ExactMatch** não estiver presente, o elemento de **segurança** assume como padrão **false**, o que significa que o **SDDL** se aplica a todos os *URIs de recurso* que compartilham o **URI** como um prefixo.</span><span class="sxs-lookup"><span data-stu-id="45e12-199">If **ExactMatch** is not present, the **Security** element defaults to **False**, which means that the **Sddl** applies to all *resource URIs* that share **Uri** as a prefix.</span></span> <span data-ttu-id="45e12-200">Se **ExactMatch** for definido como true, o **SDDL** se aplicará somente ao **URI** exato especificado.</span><span class="sxs-lookup"><span data-stu-id="45e12-200">If **ExactMatch** is set to true, the **Sddl** applies only to the exact **Uri** specified.</span></span> <span data-ttu-id="45e12-201">Se houver várias entradas de **segurança** que possam se aplicar a *URIs de recursos* específicos, a correspondência de prefixo mais longo será usada para determinar a **SDDL** apropriada.</span><span class="sxs-lookup"><span data-stu-id="45e12-201">If there are multiple **Security** entries that could apply to a particular *resource URIs*, the longest-prefix match is used to determine the appropriate **Sddl**.</span></span> <span data-ttu-id="45e12-202">Como resultado da correspondência de prefixo mais longo, se existir uma entrada de **URI** de correspondência exata, ela será sempre escolhida como o elemento de segurança apropriado.</span><span class="sxs-lookup"><span data-stu-id="45e12-202">As a result of the longest-prefix match, if an exact-match **Uri** entry exists, it will always be chosen as the appropriate Security element.</span></span>

</dd> </dl>

<span data-ttu-id="45e12-203">Este é o esquema de configuração de plug-in especificado como um XSD.</span><span class="sxs-lookup"><span data-stu-id="45e12-203">The following is the plug-in configuration schema specified as an XSD.</span></span>

``` syntax
<?xml version="1.0" encoding="utf-8"?>
<xs:schema attributeFormDefault="unqualified" 
           elementFormDefault="qualified" 
           targetNamespace="http://schemas.microsoft.com/wbem/wsman/1/config/PluginConfiguration" 
           xmlns="http://schemas.microsoft.com/wbem/wsman/1/config/PluginConfiguration" 
           xmlns:xs="https://www.w3.org/2001/XMLSchema">
 <xs:element name="PlugInConfiguration">
  <xs:complexType>
   <xs:sequence>
    <xs:element name="InitializationParameters" minOccurs="0" maxOccurs="1">
     <xs:complexType>
      <xs:sequence>
       <xs:element name="Param">
        <xs:complexType>
         <xs:sequence></xs:sequence>
         <xs:attribute name="Name" type="xs:string"/>
         <xs:attribute name="Value" type="xs:string"/>
        </xs:complexType>
       </xs:element>
      </xs:sequence>
     </xs:complexType>
    </xs:element>
    <xs:element name="Resources">
     <xs:complexType>
      <xs:sequence>
       <xs:element minOccurs="1" maxOccurs="unbounded" name="Resource">
        <xs:complexType>
         <xs:sequence>
          <xs:element name="Capability" minOccurs="1" maxOccurs="unbounded">
           <xs:complexType>
            <xs:simpleContent>
             <xs:extension base="ResourceCapabilityType">
              <xs:attribute name="SupportsFragment" type="xs:boolean" use="optional" default="false"/>
              <xs:attribute name="SupportsFiltering" type="xs:boolean" use="optional" default="false"/>
              <xs:attribute name="Type" type="ResourceCapabilityType"/>
             </xs:extension>
            </xs:simpleContent>
           </xs:complexType>
          </xs:element>
          <xs:element name="Security" minOccurs="0" maxOccurs="unbounded">
           <xs:complexType>
            <xs:sequence></xs:sequence>
            <xs:attribute name="Uri" type="xs:string"/>
            <xs:attribute name="Sddl" type="xs:string"/>
            <xs:attribute name="ExactMatch" type="xs:boolean" use="optional" default="false"/>
           </xs:complexType>
          </xs:element>
         </xs:sequence>
         <xs:attribute name="ResourceUri" type="xs:string"/>
         <xs:attribute name="ExactMatch" type="xs:boolean" use="optional" default="false"/>
         <xs:attribute name="SupportOptions" type="xs:boolean" use="optional" default="false"/>
        </xs:complexType>
       </xs:element>
      </xs:sequence>
     </xs:complexType>
    </xs:element>
   </xs:sequence>
   <xs:attribute name="Filename" type="xs:token"/>
   <xs:attribute name="SDKVersion" type="xs:unsignedInt"/>
   <xs:attribute name="Name" type="xs:string"/>
   <xs:attribute name="XmlRenderingType" type="XmlRenderingTypeType" use="optional" default="text"/>
   <!--Architecture will default to 32 on x86 systems; 64 on 64-bit systems.-->
   <xs:attribute name="Architecture" type="ArchitectureType" use="optional" default="32"/>
  </xs:complexType>
 </xs:element>
 <xs:simpleType name="ResourceCapabilityType">
  <xs:restriction base="xs:token">
   <xs:enumeration value="Get"/>
   <xs:enumeration value="Put"/>
   <xs:enumeration value="Create"/>
   <xs:enumeration value="Delete"/>
   <xs:enumeration value="Invoke"/>
   <xs:enumeration value="Enumerate"/>
   <xs:enumeration value="Subscribe"/>
   <xs:enumeration value="Shell"/>
  </xs:restriction>
 </xs:simpleType>
 <xs:simpleType name="XmlRenderingTypeType">
  <xs:restriction base="xs:token">
   <xs:enumeration value="text"/>
   <xs:enumeration value="XmlReader"/>
  </xs:restriction>
 </xs:simpleType>
 <xs:simpleType name="ArchitectureType">
  <xs:restriction base="xs:token">
   <xs:enumeration value="32"/>
   <xs:enumeration value="64"/>
  </xs:restriction>
 </xs:simpleType>
</xs:schema>
```

 

 




