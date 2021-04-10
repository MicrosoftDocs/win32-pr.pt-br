---
title: Tipo complexo de MetadataType
description: Define os tipos de metadados que você pode definir na seção de metadados do manifesto.
ms.assetid: 602bafe7-940e-4313-9da5-54c6aa7f60a2
keywords:
- Messagedatatype log de eventos de tipo complexo
topic_type:
- apiref
api_name:
- MetadataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 69b140a2b65d47d563fd88f49d6818efc13613f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009725"
---
# <a name="metadatatype-complex-type"></a><span data-ttu-id="90227-104">Tipo complexo de MetadataType</span><span class="sxs-lookup"><span data-stu-id="90227-104">MetadataType Complex Type</span></span>

<span data-ttu-id="90227-105">Define os tipos de metadados que você pode definir na seção de metadados do manifesto.</span><span class="sxs-lookup"><span data-stu-id="90227-105">Defines the metadata types that you can define in the metadata section of the manifest.</span></span>

``` syntax
<xs:complexType name="MetadataType">
    <xs:sequence>
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
            minOccurs="0"
         />
        <xs:element name="keywords"
            type="KeywordListType"
            minOccurs="0"
         />
        <xs:element name="types"
            type="TypeListType"
            minOccurs="0"
         />
        <xs:element name="namedQueries"
            type="NamedQueryType"
            minOccurs="0"
         />
        <xs:element name="messageTable"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:sequence>
                    <xs:element name="message"
                        minOccurs="0"
                        maxOccurs="unbounded"
                    >
                        <xs:complexType>
                            <xs:attribute name="value"
                                type="UInt32Type"
                                use="required"
                             />
                            <xs:attribute name="mid"
                                type="xs:string"
                                use="optional"
                             />
                            <xs:attribute name="message"
                                type="strTableRef"
                                use="required"
                             />
                            <xs:attribute name="symbol"
                                type="CSymbolType"
                                use="optional"
                             />
                        </xs:complexType>
                    </xs:element>
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="anyURI"
        use="required"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="90227-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="90227-106">Child elements</span></span>



| <span data-ttu-id="90227-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="90227-107">Element</span></span>                                                                       | <span data-ttu-id="90227-108">Type</span><span class="sxs-lookup"><span data-stu-id="90227-108">Type</span></span>                                                                       | <span data-ttu-id="90227-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="90227-109">Description</span></span>                                                                                                                                                      |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="90227-110">**meios**</span><span class="sxs-lookup"><span data-stu-id="90227-110">**channels**</span></span>](eventmanifestschema-channels-metadatatype-element.md)         | [<span data-ttu-id="90227-111">**ChannelListType**</span><span class="sxs-lookup"><span data-stu-id="90227-111">**ChannelListType**</span></span>](eventmanifestschema-channellisttype-complextype.md) | <span data-ttu-id="90227-112">Define uma lista de canais para os quais os provedores podem registrar eventos.</span><span class="sxs-lookup"><span data-stu-id="90227-112">Defines a list of channels to which providers can log events.</span></span> <span data-ttu-id="90227-113">Um provedor pode, então, importar um ou mais dos canais em seu manifesto.</span><span class="sxs-lookup"><span data-stu-id="90227-113">A provider can then import one or more of the channels in their manifest.</span></span><br/>               |
| [<span data-ttu-id="90227-114">**palavras-chave**</span><span class="sxs-lookup"><span data-stu-id="90227-114">**keywords**</span></span>](eventmanifestschema-keywords-metadatatype-element.md)         | [<span data-ttu-id="90227-115"></span><span class="sxs-lookup"><span data-stu-id="90227-115">**KeywordListType**</span></span>](eventmanifestschema-keywordlisttype-complextype.md) | <span data-ttu-id="90227-116">Define uma lista de palavras-chave que determinam a categoria de eventos que o provedor grava.</span><span class="sxs-lookup"><span data-stu-id="90227-116">Defines a list of keywords that determine the category of events that the provider writes.</span></span><br/>                                                            |
| [<span data-ttu-id="90227-117">**alcançar**</span><span class="sxs-lookup"><span data-stu-id="90227-117">**levels**</span></span>](eventmanifestschema-levels-metadatatype-element.md)             | [<span data-ttu-id="90227-118">**LevelListType**</span><span class="sxs-lookup"><span data-stu-id="90227-118">**LevelListType**</span></span>](eventmanifestschema-levellisttype-complextype.md)     | <span data-ttu-id="90227-119">Define uma lista de níveis que especificam a severidade de um evento.</span><span class="sxs-lookup"><span data-stu-id="90227-119">Defines a list of levels that specify the severity of an event.</span></span><br/>                                                                                       |
| <span data-ttu-id="90227-120">**message**</span><span class="sxs-lookup"><span data-stu-id="90227-120">**message**</span></span>                                                                   |                                                                            | <span data-ttu-id="90227-121">Define uma cadeia de caracteres de mensagem.</span><span class="sxs-lookup"><span data-stu-id="90227-121">Defines a message string.</span></span><br/>                                                                                                                             |
| <span data-ttu-id="90227-122">**mensagem de**</span><span class="sxs-lookup"><span data-stu-id="90227-122">**messageTable**</span></span>                                                              |                                                                            | <span data-ttu-id="90227-123">Define uma lista de cadeias de caracteres de mensagem.</span><span class="sxs-lookup"><span data-stu-id="90227-123">Defines a list of message strings.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="90227-124">**namedQueries**</span><span class="sxs-lookup"><span data-stu-id="90227-124">**namedQueries**</span></span>](eventmanifestschema-namedqueries-metadatatype-element.md) | [<span data-ttu-id="90227-125">**NamedQueryType**</span><span class="sxs-lookup"><span data-stu-id="90227-125">**NamedQueryType**</span></span>](eventmanifestschema-namedquerytype-complextype.md)   | <span data-ttu-id="90227-126">Define uma lista de consultas nomeadas que usam expressões regulares para executar ações de localizar e substituir na cadeia de caracteres de mensagem de um evento.</span><span class="sxs-lookup"><span data-stu-id="90227-126">Defines a list of named queries that use regular expressions to perform find and replace actions on an event's message string.</span></span><br/>                        |
| [<span data-ttu-id="90227-127">**opcodes**</span><span class="sxs-lookup"><span data-stu-id="90227-127">**opcodes**</span></span>](eventmanifestschema-opcodes-metadatatype-element.md)           | [<span data-ttu-id="90227-128">**OpcodeListType**</span><span class="sxs-lookup"><span data-stu-id="90227-128">**OpcodeListType**</span></span>](eventmanifestschema-opcodelisttype-complextype.md)   | <span data-ttu-id="90227-129">Define uma lista de opcodes que você pode usar para agrupar eventos dentro de uma tarefa.</span><span class="sxs-lookup"><span data-stu-id="90227-129">Defines a list of opcodes that you can use to group events within a task.</span></span><br/>                                                                             |
| <span data-ttu-id="90227-130">**tarefa**</span><span class="sxs-lookup"><span data-stu-id="90227-130">**tasks**</span></span>                                                                     | [<span data-ttu-id="90227-131">**TaskListtype**</span><span class="sxs-lookup"><span data-stu-id="90227-131">**TaskListType**</span></span>](eventmanifestschema-tasklisttype-complextype.md)       | <span data-ttu-id="90227-132">Define uma lista de tarefas que um provedor pode usar para agrupar eventos.</span><span class="sxs-lookup"><span data-stu-id="90227-132">Defines a list of tasks that a provider can use to group events.</span></span> <span data-ttu-id="90227-133">Normalmente, você usa tarefas para agrupar eventos para um recurso ou componente do provedor.</span><span class="sxs-lookup"><span data-stu-id="90227-133">Typically, you use tasks to group events for a feature or component of the provider.</span></span><br/> |
| [<span data-ttu-id="90227-134">**digita**</span><span class="sxs-lookup"><span data-stu-id="90227-134">**types**</span></span>](eventmanifestschema-types-metadatatype-element.md)               | [<span data-ttu-id="90227-135">**TypeListType**</span><span class="sxs-lookup"><span data-stu-id="90227-135">**TypeListType**</span></span>](eventmanifestschema-typelisttype-complextype.md)       | <span data-ttu-id="90227-136">Define uma lista de tipos XML.</span><span class="sxs-lookup"><span data-stu-id="90227-136">Defines a list of XML types.</span></span><br/>                                                                                                                          |



## <a name="attributes"></a><span data-ttu-id="90227-137">Atributos</span><span class="sxs-lookup"><span data-stu-id="90227-137">Attributes</span></span>



| <span data-ttu-id="90227-138">Nome</span><span class="sxs-lookup"><span data-stu-id="90227-138">Name</span></span>    | <span data-ttu-id="90227-139">Tipo</span><span class="sxs-lookup"><span data-stu-id="90227-139">Type</span></span>                                                              | <span data-ttu-id="90227-140">Descrição</span><span class="sxs-lookup"><span data-stu-id="90227-140">Description</span></span>                                                                                        |
|---------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90227-141">message</span><span class="sxs-lookup"><span data-stu-id="90227-141">message</span></span> | [<span data-ttu-id="90227-142">**strTableRef**</span><span class="sxs-lookup"><span data-stu-id="90227-142">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="90227-143">Uma referência à cadeia de caracteres localizada na tabela de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="90227-143">A reference to the localized string in the string table.</span></span><br/>                                |
| <span data-ttu-id="90227-144">mid</span><span class="sxs-lookup"><span data-stu-id="90227-144">mid</span></span>     | <span data-ttu-id="90227-145">xs:string</span><span class="sxs-lookup"><span data-stu-id="90227-145">xs:string</span></span>                                                         | <span data-ttu-id="90227-146">Não usado.</span><span class="sxs-lookup"><span data-stu-id="90227-146">Not used.</span></span><br/>                                                                               |
| <span data-ttu-id="90227-147">name</span><span class="sxs-lookup"><span data-stu-id="90227-147">name</span></span>    | <span data-ttu-id="90227-148">anyURI</span><span class="sxs-lookup"><span data-stu-id="90227-148">anyURI</span></span>                                                            | <span data-ttu-id="90227-149">O URI do arquivo meta.</span><span class="sxs-lookup"><span data-stu-id="90227-149">The URI of the meta file.</span></span> <br/>                                                              |
| <span data-ttu-id="90227-150">símbolo</span><span class="sxs-lookup"><span data-stu-id="90227-150">symbol</span></span>  | [<span data-ttu-id="90227-151">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="90227-151">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="90227-152">O nome simbólico que você deseja que o compilador de mensagem crie para essa cadeia de caracteres de mensagem.</span><span class="sxs-lookup"><span data-stu-id="90227-152">The symbolic name that you want the message compiler to create for this message string.</span></span><br/> |
| <span data-ttu-id="90227-153">value</span><span class="sxs-lookup"><span data-stu-id="90227-153">value</span></span>   | [<span data-ttu-id="90227-154">**UInt32type**</span><span class="sxs-lookup"><span data-stu-id="90227-154">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="90227-155">O número a ser usado como o identificador da mensagem para esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="90227-155">The number to use as the message identifier for this message.</span></span><br/>                           |



## <a name="remarks"></a><span data-ttu-id="90227-156">Comentários</span><span class="sxs-lookup"><span data-stu-id="90227-156">Remarks</span></span>

<span data-ttu-id="90227-157">Embora você possa criar um manifesto que contenha uma seção de metadados, o serviço não o usará; os únicos metadados que o serviço reconhece são os metadados encontrados no arquivo de Winmeta.xml.</span><span class="sxs-lookup"><span data-stu-id="90227-157">Although you can create a manifest that contains a metadata section, the service will not use it; the only metadata that the service recognizes is the metadata found in the Winmeta.xml file.</span></span>

## <a name="requirements"></a><span data-ttu-id="90227-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90227-158">Requirements</span></span>



| <span data-ttu-id="90227-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="90227-159">Requirement</span></span> | <span data-ttu-id="90227-160">Valor</span><span class="sxs-lookup"><span data-stu-id="90227-160">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="90227-161">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90227-161">Minimum supported client</span></span><br/> | <span data-ttu-id="90227-162">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="90227-162">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="90227-163">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="90227-163">Minimum supported server</span></span><br/> | <span data-ttu-id="90227-164">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="90227-164">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





