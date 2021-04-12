---
title: Elemento instrumentationManifest
description: O nó raiz do manifesto.
ms.assetid: cb7b5201-be11-48f9-bcca-4606904f0c1d
keywords:
- EventLog do elemento instrumentationManifest
topic_type:
- apiref
api_name:
- instrumentationManifest
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c15092d7a7eafd625e9c2026965af053d38fe4b9
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2021
ms.locfileid: "104172575"
---
# <a name="instrumentationmanifest-element"></a><span data-ttu-id="8c910-104">Elemento instrumentationManifest</span><span class="sxs-lookup"><span data-stu-id="8c910-104">instrumentationManifest Element</span></span>

<span data-ttu-id="8c910-105">O nó raiz do manifesto.</span><span class="sxs-lookup"><span data-stu-id="8c910-105">The root node of the manifest.</span></span>

``` syntax
<xs:element name="instrumentationManifest">
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="InstrumentationManifestType"
            >
                <xs:choice
                    maxOccurs="3"
                >
                    <xs:choice>
                        <xs:element name="metadata"
                            type="MetadataType"
                         />
                        <xs:element name="instrumentation"
                            type="InstrumentationType"
                         />
                    </xs:choice>
                    <xs:element name="localization"
                        type="LocalizationType"
                     />
                    <xs:any
                        processContents="lax"
                        minOccurs="0"
                        maxOccurs="unbounded"
                        namespace="##other"
                     />
                </xs:choice>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="8c910-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="8c910-106">Child elements</span></span>



| <span data-ttu-id="8c910-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="8c910-107">Element</span></span>                                                                                        | <span data-ttu-id="8c910-108">Type</span><span class="sxs-lookup"><span data-stu-id="8c910-108">Type</span></span>                                                                               | <span data-ttu-id="8c910-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="8c910-109">Description</span></span>                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8c910-110">**Instrumentação**</span><span class="sxs-lookup"><span data-stu-id="8c910-110">**instrumentation**</span></span>](eventmanifestschema-instrumentation-instrumentationmanifest-element.md) | [<span data-ttu-id="8c910-111">**InstrumentationType**</span><span class="sxs-lookup"><span data-stu-id="8c910-111">**InstrumentationType**</span></span>](eventmanifestschema-instrumentationtype-complextype.md) | <span data-ttu-id="8c910-112">Esta seção define um ou mais provedores de eventos e os eventos que eles registram.</span><span class="sxs-lookup"><span data-stu-id="8c910-112">This section defines one or more event providers and the events that they log.</span></span><br/>                                                                                                                                                                                                                     |
| [<span data-ttu-id="8c910-113">**Localizar**</span><span class="sxs-lookup"><span data-stu-id="8c910-113">**localization**</span></span>](eventmanifestschema-localization-instrumentationmanifest-element.md)       | [<span data-ttu-id="8c910-114">**Localizaçãotype**</span><span class="sxs-lookup"><span data-stu-id="8c910-114">**LocalizationType**</span></span>](eventmanifestschema-localizationtype-complextype.md)       | <span data-ttu-id="8c910-115">Esta seção define as cadeias de caracteres de mensagem localizadas que os consumidores usam para exibição.</span><span class="sxs-lookup"><span data-stu-id="8c910-115">This section defines the localized message strings that consumers use for display.</span></span> <span data-ttu-id="8c910-116">Por exemplo, esta seção conteria a cadeia de caracteres de mensagem localizada para o nome do seu provedor, os eventos que você definir e quaisquer atributos de evento que você definir, como canais, tarefas e OpCodes.</span><span class="sxs-lookup"><span data-stu-id="8c910-116">For example, this section would contain the localized message string for the name of your provider, the events that you define, and any event attributes that you define, such as channels, tasks, and opcodes.</span></span><br/> |
| [<span data-ttu-id="8c910-117">**los**</span><span class="sxs-lookup"><span data-stu-id="8c910-117">**metadata**</span></span>](eventmanifestschema-metadata-instrumentationmanifest-element.md)               | [<span data-ttu-id="8c910-118">**MetadataType**</span><span class="sxs-lookup"><span data-stu-id="8c910-118">**MetadataType**</span></span>](eventmanifestschema-metadatatype-complextype.md)               | <span data-ttu-id="8c910-119">Esta seção define os tipos de metadados que outros manifestos podem usar.</span><span class="sxs-lookup"><span data-stu-id="8c910-119">This section defines metadata types that other manifests can use.</span></span> <span data-ttu-id="8c910-120">Para obter um exemplo, consulte o arquivo Winmeta.xml incluído na \\ pasta include do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="8c910-120">For an example, see the Winmeta.xml file included in the \\Include folder of the Windows SDK.</span></span><br/>                                                                                                                                    |



## <a name="remarks"></a><span data-ttu-id="8c910-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="8c910-121">Remarks</span></span>

<span data-ttu-id="8c910-122">O elemento **instrumentationManifest** deve conter os seguintes namespaces:</span><span class="sxs-lookup"><span data-stu-id="8c910-122">The **instrumentationManifest** element must contain the following namespaces:</span></span>

<dl> <span data-ttu-id="8c910-123">xmlns = " https://schemas.microsoft.com/win/2004/08/events "</span><span class="sxs-lookup"><span data-stu-id="8c910-123">xmlns="https://schemas.microsoft.com/win/2004/08/events"</span></span>  
<span data-ttu-id="8c910-124">xmlns: Win = " https://manifests.microsoft.com/win/2004/08/windows/events "</span><span class="sxs-lookup"><span data-stu-id="8c910-124">xmlns:win="https://manifests.microsoft.com/win/2004/08/windows/events"</span></span>  
<span data-ttu-id="8c910-125">xmlns: XS = " https://www.w3.org/2001/XMLSchema "</span><span class="sxs-lookup"><span data-stu-id="8c910-125">xmlns:xs="https://www.w3.org/2001/XMLSchema"</span></span>  
</dl>

<span data-ttu-id="8c910-126">Um manifesto deve conter uma seção de instrumentação e uma seção de localização.</span><span class="sxs-lookup"><span data-stu-id="8c910-126">A manifest must contain an instrumentation section and a localization section.</span></span> <span data-ttu-id="8c910-127">A seção de instrumentação e a seção de metadados são mutuamente exclusivas (você não pode definir ambos no mesmo manifesto).</span><span class="sxs-lookup"><span data-stu-id="8c910-127">The instrumentation section and metadata section are mutually exclusive (you cannot define both in the same manifest).</span></span> <span data-ttu-id="8c910-128">Embora você possa criar um manifesto que contenha uma seção de metadados, o serviço não o usará; os únicos metadados que o serviço reconhece são os metadados encontrados no arquivo de Winmeta.xml.</span><span class="sxs-lookup"><span data-stu-id="8c910-128">Although you can create a manifest that contains a metadata section, the service will not use it; the only metadata that the service recognizes is the metadata found in the Winmeta.xml file.</span></span>

## <a name="examples"></a><span data-ttu-id="8c910-129">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8c910-129">Examples</span></span>

<span data-ttu-id="8c910-130">O exemplo a seguir mostra o esqueleto de um manifesto de instrumentação totalmente definido.</span><span class="sxs-lookup"><span data-stu-id="8c910-130">The following example shows the skeleton of a fully defined instrumentation manifest.</span></span>


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="https://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="https://www.w3.org/2001/XMLSchema"    
    >

    <instrumentation>
        <events>
            <provider ...>
                <channels>
                    <importChanel .../>
                    <channel .../>
                </channels>
                <levels>
                <level .../>
                </levels>
                <tasks>
                    <task .../>
                </tasks>
                <opcodes>
                    <opcode .../>
                </opcodes>
                <keywords>
                    <keyword .../>
                </keywords>
                <filters>
                    <filter .../>
                </filters>
                <maps>
                    <valueMap ...>
                        <map .../>
                    </valueMap>
                    <bitMap ...>
                        <map .../>
                    </bitMap>
                </maps>
                <namedQueries>
                    <patternMap ...>
                        <map .../>
                    </patternMap>  
                </namedQueries>
                <templates>
                    <template ...>
                        <data .../>
                        <UserData>
                            <!-- valid XML fragment -->
                        </UserData>
                    </template>
                </templates>
                <events>
                    <event .../>
                </events>
            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources ...>
            <stringTable>
                <string .../>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```



## <a name="requirements"></a><span data-ttu-id="8c910-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c910-131">Requirements</span></span>



| <span data-ttu-id="8c910-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c910-132">Requirement</span></span> | <span data-ttu-id="8c910-133">Valor</span><span class="sxs-lookup"><span data-stu-id="8c910-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8c910-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8c910-134">Minimum supported client</span></span><br/> | <span data-ttu-id="8c910-135">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8c910-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8c910-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8c910-136">Minimum supported server</span></span><br/> | <span data-ttu-id="8c910-137">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8c910-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





