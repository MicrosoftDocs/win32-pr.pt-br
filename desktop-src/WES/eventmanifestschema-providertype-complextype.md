---
title: Tipo complexo ProviderType
description: Define um provedor e os metadados que ele usa para definir seus eventos. | Tipo complexo ProviderType
ms.assetid: 70199cf5-a6d0-4780-9ff1-ed083a5b49ac
keywords:
- Log de eventos do tipo complexo ProviderType
topic_type:
- apiref
api_name:
- ProviderType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c258b3ff48cdd2f00f632fdce770b58182a531c7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298323"
---
# <a name="providertype-complex-type"></a><span data-ttu-id="97262-105">Tipo complexo ProviderType</span><span class="sxs-lookup"><span data-stu-id="97262-105">ProviderType Complex Type</span></span>

<span data-ttu-id="97262-106">Define um provedor e os metadados que ele usa para definir seus eventos.</span><span class="sxs-lookup"><span data-stu-id="97262-106">Defines a provider and the metadata that it uses to define its events.</span></span>

``` syntax
<xs:complexType name="ProviderType">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="channels"
            type="ChannelListType"
         />
        <xs:element name="levels"
            type="LevelListType"
         />
        <xs:element name="tasks"
            type="TaskListType"
         />
        <xs:element name="opcodes"
            type="OpcodeListType"
         />
        <xs:element name="keywords"
            type="KeywordListType"
         />
        <xs:element name="maps"
            type="MapType"
         />
        <xs:element name="namedQueries"
            type="NamedQueryType"
         />
        <xs:element name="templates"
            type="TemplateListType"
         />
        <xs:element name="events"
            type="DefinitionType"
         />
        <xs:element name="filters"
            type="FilterListType"
         />
        <xs:any
            processContents="lax"
            namespace="##other"
         />
    </xs:choice>
    <xs:attribute name="name"
        type="anyURI"
        use="required"
     />
    <xs:attribute name="guid"
        type="GUIDType"
        use="required"
     />
    <xs:attribute name="resourceFileName"
        type="filePath"
        use="optional"
     />
    <xs:attribute name="messageFileName"
        type="filePath"
        use="optional"
     />
    <xs:attribute name="parameterFileName"
        type="filePath"
        use="optional"
     />
    <xs:attribute name="helpLink"
        type="anyURI"
        use="optional"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="required"
     />
    <xs:attribute name="message"
        type="strTableRef"
        use="optional"
     />
    <xs:attribute name="source"
        use="optional"
        default="Xml"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="Xml"
                 />
                <xs:enumeration
                    value="Wbem"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="warnOnApplicationCompatibilityError"
        type="xs:boolean"
        use="optional"
        default="false"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="97262-107">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="97262-107">Child elements</span></span>



| <span data-ttu-id="97262-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="97262-108">Element</span></span>                                                                       | <span data-ttu-id="97262-109">Type</span><span class="sxs-lookup"><span data-stu-id="97262-109">Type</span></span>                                                                         | <span data-ttu-id="97262-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="97262-110">Description</span></span>                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="97262-111">**meios**</span><span class="sxs-lookup"><span data-stu-id="97262-111">**channels**</span></span>](eventmanifestschema-channels-providertype-element.md)         | [<span data-ttu-id="97262-112">**ChannelListType**</span><span class="sxs-lookup"><span data-stu-id="97262-112">**ChannelListType**</span></span>](eventmanifestschema-channellisttype-complextype.md)   | <span data-ttu-id="97262-113">Define uma lista de canais para os quais os provedores podem registrar eventos.</span><span class="sxs-lookup"><span data-stu-id="97262-113">Defines a list of channels to which providers can log events.</span></span><br/>                                                                                                                                                                                      |
| [<span data-ttu-id="97262-114">**LostFocus**</span><span class="sxs-lookup"><span data-stu-id="97262-114">**events**</span></span>](eventmanifestschema-events-providertype-element.md)             | [<span data-ttu-id="97262-115">**Definitiontype**</span><span class="sxs-lookup"><span data-stu-id="97262-115">**DefinitionType**</span></span>](eventmanifestschema-definitiontype-complextype.md)     | <span data-ttu-id="97262-116">Define uma lista de definições de eventos dos eventos que o provedor pode registrar.</span><span class="sxs-lookup"><span data-stu-id="97262-116">Defines a list of event definitions of the events that the provider can log.</span></span><br/>                                                                                                                                                                       |
| <span data-ttu-id="97262-117">**Filter**</span><span class="sxs-lookup"><span data-stu-id="97262-117">**filters**</span></span>                                                                   | [<span data-ttu-id="97262-118">**FilterListType**</span><span class="sxs-lookup"><span data-stu-id="97262-118">**FilterListType**</span></span>](eventmanifestschema-filterlisttype-complextype.md)     | <span data-ttu-id="97262-119">Define uma lista de filtros aos quais seu provedor dá suporte.</span><span class="sxs-lookup"><span data-stu-id="97262-119">Defines a list of filters that your provider supports.</span></span> <span data-ttu-id="97262-120">Você pode usar os filtros, como faria em nível e palavras-chave, para determinar se deseja escrever um evento.</span><span class="sxs-lookup"><span data-stu-id="97262-120">You can use the filters, as you would level and keywords, to determine if you want to write an event.</span></span> <br/> <span data-ttu-id="97262-121">**Windows Server 2008 e Windows Vista:** Sem suporte até o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="97262-121">**Windows Server 2008 and Windows Vista:** Not supported until Windows 7.</span></span><br/> |
| [<span data-ttu-id="97262-122">**palavras-chave**</span><span class="sxs-lookup"><span data-stu-id="97262-122">**keywords**</span></span>](eventmanifestschema-keywords-providertype-element.md)         | [<span data-ttu-id="97262-123"></span><span class="sxs-lookup"><span data-stu-id="97262-123">**KeywordListType**</span></span>](eventmanifestschema-keywordlisttype-complextype.md)   | <span data-ttu-id="97262-124">Define uma lista de palavras-chave que categorizam eventos.</span><span class="sxs-lookup"><span data-stu-id="97262-124">Defines a list of keywords that categorize events.</span></span><br/>                                                                                                                                                                                                 |
| [<span data-ttu-id="97262-125">**alcançar**</span><span class="sxs-lookup"><span data-stu-id="97262-125">**levels**</span></span>](eventmanifestschema-levels-providertype-element.md)             | [<span data-ttu-id="97262-126">**LevelListType**</span><span class="sxs-lookup"><span data-stu-id="97262-126">**LevelListType**</span></span>](eventmanifestschema-levellisttype-complextype.md)       | <span data-ttu-id="97262-127">Define uma lista de níveis que especificam a severidade de um evento.</span><span class="sxs-lookup"><span data-stu-id="97262-127">Defines a list of levels that specify the severity of an event.</span></span><br/>                                                                                                                                                                                    |
| [<span data-ttu-id="97262-128">**los**</span><span class="sxs-lookup"><span data-stu-id="97262-128">**maps**</span></span>](eventmanifestschema-maps-providertype-element.md)                 | [<span data-ttu-id="97262-129">**MapType**</span><span class="sxs-lookup"><span data-stu-id="97262-129">**MapType**</span></span>](eventmanifestschema-maptype-complextype.md)                   | <span data-ttu-id="97262-130">Define uma lista de pares de nome/valor que você pode referenciar na seção de modelo do manifesto.</span><span class="sxs-lookup"><span data-stu-id="97262-130">Defines a list of name/value pairs that you can reference in the template section of the manifest.</span></span><br/>                                                                                                                                                 |
| [<span data-ttu-id="97262-131">**namedQueries**</span><span class="sxs-lookup"><span data-stu-id="97262-131">**namedQueries**</span></span>](eventmanifestschema-namedqueries-providertype-element.md) | [<span data-ttu-id="97262-132">**NamedQueryType**</span><span class="sxs-lookup"><span data-stu-id="97262-132">**NamedQueryType**</span></span>](eventmanifestschema-namedquerytype-complextype.md)     | <span data-ttu-id="97262-133">Não usado.</span><span class="sxs-lookup"><span data-stu-id="97262-133">Not used.</span></span> <span data-ttu-id="97262-134">Define uma lista de consultas nomeadas que consultam a cadeia de caracteres de mensagem de evento para um valor e executam uma ação especificada, se encontradas.</span><span class="sxs-lookup"><span data-stu-id="97262-134">Defines a list of named queries that query the event message string for a value and perform a specified action if found.</span></span><br/>                                                                                                                 |
| [<span data-ttu-id="97262-135">**opcodes**</span><span class="sxs-lookup"><span data-stu-id="97262-135">**opcodes**</span></span>](eventmanifestschema-opcodes-providertype-element.md)           | [<span data-ttu-id="97262-136">**OpcodeListType**</span><span class="sxs-lookup"><span data-stu-id="97262-136">**OpcodeListType**</span></span>](eventmanifestschema-opcodelisttype-complextype.md)     | <span data-ttu-id="97262-137">Define uma lista de opcodes que você pode usar para agrupar eventos dentro de uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="97262-137">Defines a list of opcodes that you can use to group events within a task.</span></span><br/>                                                                                                                                                                          |
| [<span data-ttu-id="97262-138">**tarefa**</span><span class="sxs-lookup"><span data-stu-id="97262-138">**tasks**</span></span>](eventmanifestschema-tasks-providertype-element.md)               | [<span data-ttu-id="97262-139">**TaskListtype**</span><span class="sxs-lookup"><span data-stu-id="97262-139">**TaskListType**</span></span>](eventmanifestschema-tasklisttype-complextype.md)         | <span data-ttu-id="97262-140">Define uma lista de tarefas que um provedor pode usar para agrupar eventos.</span><span class="sxs-lookup"><span data-stu-id="97262-140">Defines a list of tasks that a provider can use to group events.</span></span> <span data-ttu-id="97262-141">Normalmente, você usa tarefas para agrupar eventos para um recurso ou componente do provedor.</span><span class="sxs-lookup"><span data-stu-id="97262-141">Typically, you use tasks to group events for a feature or component of the provider.</span></span><br/>                                                                                              |
| [<span data-ttu-id="97262-142">**modelo**</span><span class="sxs-lookup"><span data-stu-id="97262-142">**templates**</span></span>](eventmanifestschema-templates-providertype-element.md)       | [<span data-ttu-id="97262-143">**TemplateListType**</span><span class="sxs-lookup"><span data-stu-id="97262-143">**TemplateListType**</span></span>](eventmanifestschema-templatelisttype-complextype.md) | <span data-ttu-id="97262-144">Define uma lista de modelos que especificam os dados a serem incluídos com os eventos.</span><span class="sxs-lookup"><span data-stu-id="97262-144">Defines a list of templates that specify the data to include with the events.</span></span><br/>                                                                                                                                                                      |



## <a name="attributes"></a><span data-ttu-id="97262-145">Atributos</span><span class="sxs-lookup"><span data-stu-id="97262-145">Attributes</span></span>



| <span data-ttu-id="97262-146">Nome</span><span class="sxs-lookup"><span data-stu-id="97262-146">Name</span></span>                                | <span data-ttu-id="97262-147">Tipo</span><span class="sxs-lookup"><span data-stu-id="97262-147">Type</span></span>                                                              | <span data-ttu-id="97262-148">Descrição</span><span class="sxs-lookup"><span data-stu-id="97262-148">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97262-149">guid</span><span class="sxs-lookup"><span data-stu-id="97262-149">guid</span></span>                                | [<span data-ttu-id="97262-150">**GUIDtype**</span><span class="sxs-lookup"><span data-stu-id="97262-150">**GUIDType**</span></span>](eventmanifestschema-guidtype-simpletype.md)       | <span data-ttu-id="97262-151">Um GUID que identifica exclusivamente o provedor.</span><span class="sxs-lookup"><span data-stu-id="97262-151">A GUID that uniquely identifies the provider.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="97262-152">helpLink</span><span class="sxs-lookup"><span data-stu-id="97262-152">helpLink</span></span>                            | <span data-ttu-id="97262-153">anyURI</span><span class="sxs-lookup"><span data-stu-id="97262-153">anyURI</span></span>                                                            | <span data-ttu-id="97262-154">A URL ou o link da ajuda MS para o conteúdo que fornece informações sobre os eventos que o provedor gera.</span><span class="sxs-lookup"><span data-stu-id="97262-154">The URL or MS help link to content that provides information about the events that the provider raises.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="97262-155">message</span><span class="sxs-lookup"><span data-stu-id="97262-155">message</span></span>                             | [<span data-ttu-id="97262-156">**strTableRef**</span><span class="sxs-lookup"><span data-stu-id="97262-156">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="97262-157">O nome de exibição localizado para o provedor.</span><span class="sxs-lookup"><span data-stu-id="97262-157">The localized display name for the provider.</span></span> <span data-ttu-id="97262-158">A cadeia de caracteres de mensagem faz referência a uma cadeia de caracteres localizada na seção [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) do manifesto.</span><span class="sxs-lookup"><span data-stu-id="97262-158">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span> <br/>                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="97262-159">messageFileName</span><span class="sxs-lookup"><span data-stu-id="97262-159">messageFileName</span></span>                     | [<span data-ttu-id="97262-160">**filePath**</span><span class="sxs-lookup"><span data-stu-id="97262-160">**filePath**</span></span>](eventmanifestschema-filepath-simpletype.md)       | <span data-ttu-id="97262-161">O caminho completo para o arquivo que contém os recursos de mensagem localizados do provedor.</span><span class="sxs-lookup"><span data-stu-id="97262-161">The full path to the file that contains the provider's localized message resources.</span></span> <span data-ttu-id="97262-162">O arquivo pode ser um arquivo executável ou um arquivo DLL.</span><span class="sxs-lookup"><span data-stu-id="97262-162">The file can be an executable file or DLL file.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="97262-163">name</span><span class="sxs-lookup"><span data-stu-id="97262-163">name</span></span>                                | <span data-ttu-id="97262-164">anyURI</span><span class="sxs-lookup"><span data-stu-id="97262-164">anyURI</span></span>                                                            | <span data-ttu-id="97262-165">O nome do provedor.</span><span class="sxs-lookup"><span data-stu-id="97262-165">The name of the provider.</span></span> <span data-ttu-id="97262-166">O nome deve estar no formato, componente de produto *da empresa* -  - .</span><span class="sxs-lookup"><span data-stu-id="97262-166">The name should be of the form, *Company*-*Product*-*Component*.</span></span><br/> <span data-ttu-id="97262-167">O nome não pode ter mais de 255 caracteres e não pode conter os caracteres: ' > ', ' < ', ' & ', ' "', ' ', ' ', ' \| \\ : ', ' ', '? ', ' \* ', ou caracteres com códigos inferiores a 31.</span><span class="sxs-lookup"><span data-stu-id="97262-167">The name cannot be longer than 255 characters, and cannot contain the characters: '>', '<', '&', '"', '\|', '\\', ':', '', '?', '\*', or characters with codes less than 31.</span></span> <span data-ttu-id="97262-168">Além disso, o nome deve seguir as restrições gerais nos nomes de chave do registro e arquivo.</span><span class="sxs-lookup"><span data-stu-id="97262-168">In addition, the name must follow the general constraints on file and registry key names.</span></span> <span data-ttu-id="97262-169">Essas restrições podem ser encontradas no [nomear um arquivo](/windows/desktop/FileIO/naming-a-file)e nos [limites de tamanho do elemento do registro](/windows/desktop/SysInfo/registry-element-size-limits).</span><span class="sxs-lookup"><span data-stu-id="97262-169">These constraints can be found at [Naming a File](/windows/desktop/FileIO/naming-a-file), and [Registry Element Size Limits](/windows/desktop/SysInfo/registry-element-size-limits).</span></span><br/> |
| <span data-ttu-id="97262-170">parameterFileName</span><span class="sxs-lookup"><span data-stu-id="97262-170">parameterFileName</span></span>                   | [<span data-ttu-id="97262-171">**filePath**</span><span class="sxs-lookup"><span data-stu-id="97262-171">**filePath**</span></span>](eventmanifestschema-filepath-simpletype.md)       | <span data-ttu-id="97262-172">O caminho completo para o arquivo que contém os recursos de cadeia de caracteres do parâmetro do provedor.</span><span class="sxs-lookup"><span data-stu-id="97262-172">The full path to the file that contain the provider's parameter string resources.</span></span> <span data-ttu-id="97262-173">O arquivo pode ser um arquivo executável ou um arquivo DLL.</span><span class="sxs-lookup"><span data-stu-id="97262-173">The file can be an executable file or DLL file.</span></span> <span data-ttu-id="97262-174">Você pode especificar mais de um arquivo de parâmetro separado por um ponto-e-vírgula.</span><span class="sxs-lookup"><span data-stu-id="97262-174">You can specify more than one parameter file separated by a semicolon.</span></span> <span data-ttu-id="97262-175">O arquivo é pesquisado quando a cadeia de caracteres de mensagem de um evento contém uma cadeia de caracteres de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="97262-175">The file is searched when an event's message string contains a parameter string.</span></span> <span data-ttu-id="97262-176">Os parâmetros permitem que você forneça cadeias de caracteres de inserção localizáveis.</span><span class="sxs-lookup"><span data-stu-id="97262-176">Parameters let you provide localizable insert strings.</span></span> <span data-ttu-id="97262-177">Consulte comentários para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="97262-177">See Remarks for more information.</span></span><br/>                                                                                                                                                |
| <span data-ttu-id="97262-178">resourceFileName</span><span class="sxs-lookup"><span data-stu-id="97262-178">resourceFileName</span></span>                    | [<span data-ttu-id="97262-179">**filePath**</span><span class="sxs-lookup"><span data-stu-id="97262-179">**filePath**</span></span>](eventmanifestschema-filepath-simpletype.md)       | <span data-ttu-id="97262-180">O caminho completo para o arquivo que contém os recursos de metadados do provedor.</span><span class="sxs-lookup"><span data-stu-id="97262-180">The full path to the file that contains the provider's metadata resources.</span></span> <span data-ttu-id="97262-181">O arquivo pode ser um arquivo executável ou um arquivo DLL.</span><span class="sxs-lookup"><span data-stu-id="97262-181">The file can be an executable file or DLL file.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="97262-182">source</span><span class="sxs-lookup"><span data-stu-id="97262-182">source</span></span>                              |                                                                   | <span data-ttu-id="97262-183">Somente para uso interno.</span><span class="sxs-lookup"><span data-stu-id="97262-183">For internal use only.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="97262-184">símbolo</span><span class="sxs-lookup"><span data-stu-id="97262-184">symbol</span></span>                              | [<span data-ttu-id="97262-185">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="97262-185">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="97262-186">O símbolo a ser usado para fazer referência ao GUID do provedor em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="97262-186">The symbol to use to reference the provider's GUID in your application.</span></span> <span data-ttu-id="97262-187">O [**compilador de mensagem (MC.exe)**](message-compiler--mc-exe-.md) usa o símbolo para criar uma constante para o GUID do provedor no arquivo de cabeçalho que o compilador gera.</span><span class="sxs-lookup"><span data-stu-id="97262-187">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the provider's GUID in the header file that the compiler generates.</span></span><br/>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="97262-188">warnOnApplicationCompatibilityError</span><span class="sxs-lookup"><span data-stu-id="97262-188">warnOnApplicationCompatibilityError</span></span> | <span data-ttu-id="97262-189">**xs:boolean**</span><span class="sxs-lookup"><span data-stu-id="97262-189">**xs:boolean**</span></span>                                                    | <span data-ttu-id="97262-190">Somente para uso interno.</span><span class="sxs-lookup"><span data-stu-id="97262-190">For internal use only.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



## <a name="remarks"></a><span data-ttu-id="97262-191">Comentários</span><span class="sxs-lookup"><span data-stu-id="97262-191">Remarks</span></span>

<span data-ttu-id="97262-192">O Windows Visualizador de Eventos (Eventvwr.exe) usará a cadeia de caracteres de mensagem localizada, se disponível; caso contrário, ele usa a cadeia de caracteres do atributo Name.</span><span class="sxs-lookup"><span data-stu-id="97262-192">The Windows Event Viewer (Eventvwr.exe) will use the localized message string if available; otherwise, it uses the string from the name attribute.</span></span>

<span data-ttu-id="97262-193">Os caminhos para resourceFileName, messageFileName e parameterFileName podem conter variáveis de ambiente.</span><span class="sxs-lookup"><span data-stu-id="97262-193">The paths for resourceFileName, messageFileName, and parameterFileName can contain environment variables.</span></span> <span data-ttu-id="97262-194">Se você definir uma nova variável de ambiente para usar no caminho, deverá reiniciar o computador para que o serviço de log de eventos possa selecionar a nova variável; caso contrário, o serviço não será capaz de localizar os recursos do provedor.</span><span class="sxs-lookup"><span data-stu-id="97262-194">If you define a new environment variable to use in the path, you must restart the computer so that the event log service can pick up the new variable; otherwise, the service will not be able to find your provider's resources.</span></span>

<span data-ttu-id="97262-195">A cadeia de caracteres de mensagem do evento pode conter cadeias de caracteres de inserção e de parâmetros.</span><span class="sxs-lookup"><span data-stu-id="97262-195">An event's message string can contain insertion strings and parameter strings.</span></span> <span data-ttu-id="97262-196">Uma cadeia de caracteres de inserção é do formato%*n*, em que *n* é um índice baseado em um que identifica um item de dados do modelo de dados do evento que você deseja inserir na mensagem.</span><span class="sxs-lookup"><span data-stu-id="97262-196">An insertion string is of the form %*n*, where *n* is a one-based index that identifies a data item from the event's data template that you want to insert into the message.</span></span> <span data-ttu-id="97262-197">Uma cadeia de caracteres de parâmetro (consulte o atributo **parameterFileName** ) é do formato%%*n*, em que n é o identificador de uma mensagem na tabela de mensagens.</span><span class="sxs-lookup"><span data-stu-id="97262-197">A parameter string (see the **parameterFileName** attribute) is of the form %%*n*, where n is the identifier of a message in the message table.</span></span> <span data-ttu-id="97262-198">Se a cadeia de caracteres de mensagem do evento contiver "%1% %11 = %2% %12" e os valores de item de dados para %1 e %2 eram 8 e 2, respectivamente, e as cadeias de caracteres de parâmetro para% %11 e% %12 eram "quartos" e "galões", respectivamente, a cadeia de formatação formatada seria "8 quartos</span><span class="sxs-lookup"><span data-stu-id="97262-198">If the event's message string contained "%1 %%11 = %2 %%12" and the data item values for %1 and %2 were 8 and 2, respectively, and the parameter strings for %%11 and %%12 were "quarts" and "gallons", respectively, the formatted string would be "8 quarts = 2 gallons".</span></span>

## <a name="requirements"></a><span data-ttu-id="97262-199">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97262-199">Requirements</span></span>



| <span data-ttu-id="97262-200">Requisito</span><span class="sxs-lookup"><span data-stu-id="97262-200">Requirement</span></span> | <span data-ttu-id="97262-201">Valor</span><span class="sxs-lookup"><span data-stu-id="97262-201">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="97262-202">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="97262-202">Minimum supported client</span></span><br/> | <span data-ttu-id="97262-203">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="97262-203">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="97262-204">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="97262-204">Minimum supported server</span></span><br/> | <span data-ttu-id="97262-205">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="97262-205">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

