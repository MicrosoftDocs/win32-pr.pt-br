---
title: Tipo complexo DebugDataType
description: Define os dados que podem ser registrados para eventos de pré-processamento (pré-processador de rastreamento de software) do Windows.
ms.assetid: 75638e0f-7a26-473e-a0c4-bd8972ac171f
keywords:
- Log de eventos do tipo complexo DebugDataType
topic_type:
- apiref
api_name:
- DebugDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c190d3b2b0e870ac249fed03485828685d5dc770
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008793"
---
# <a name="debugdatatype-complex-type"></a><span data-ttu-id="ff5de-104">Tipo complexo DebugDataType</span><span class="sxs-lookup"><span data-stu-id="ff5de-104">DebugDataType Complex Type</span></span>

<span data-ttu-id="ff5de-105">Define os dados que podem ser registrados para eventos de pré-processamento (pré-processador de rastreamento de software) do Windows.</span><span class="sxs-lookup"><span data-stu-id="ff5de-105">Defines the data that can be logged for Windows software trace preprocessor (WPP) events.</span></span>

``` syntax
<xs:complexType name="DebugDataType">
    <xs:sequence>
        <xs:element name="SequenceNumber"
            type="unsignedInt"
            minOccurs="0"
         />
        <xs:element name="FlagsName"
            type="string"
            minOccurs="0"
         />
        <xs:element name="LevelName"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Component"
            type="string"
         />
        <xs:element name="SubComponent"
            type="string"
            minOccurs="0"
         />
        <xs:element name="FileLine"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Function"
            type="unsignedInt"
            minOccurs="0"
         />
        <xs:element name="Message"
            type="string"
         />
        <xs:any
            minOccurs="0"
            maxOccurs="unbounded"
            processContents="lax"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="ff5de-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="ff5de-106">Child elements</span></span>



| <span data-ttu-id="ff5de-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="ff5de-107">Element</span></span>                                                                    | <span data-ttu-id="ff5de-108">Type</span><span class="sxs-lookup"><span data-stu-id="ff5de-108">Type</span></span>        | <span data-ttu-id="ff5de-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="ff5de-109">Description</span></span>                                                                                                        |
|----------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ff5de-110">**Componente**</span><span class="sxs-lookup"><span data-stu-id="ff5de-110">**Component**</span></span>](eventschema-component-debugdatatype-element.md)           | <span data-ttu-id="ff5de-111">string</span><span class="sxs-lookup"><span data-stu-id="ff5de-111">string</span></span>      | <span data-ttu-id="ff5de-112">O nome do componente que registrou a mensagem de rastreamento.</span><span class="sxs-lookup"><span data-stu-id="ff5de-112">The name of the component that logged the trace message.</span></span><br/>                                                |
| [<span data-ttu-id="ff5de-113">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="ff5de-113">**FileLine**</span></span>](eventschema-fileline-debugdatatype-element.md)             | <span data-ttu-id="ff5de-114">string</span><span class="sxs-lookup"><span data-stu-id="ff5de-114">string</span></span>      | <span data-ttu-id="ff5de-115">O nome do arquivo de origem e a linha dentro do arquivo de origem que registrou a mensagem de rastreamento.</span><span class="sxs-lookup"><span data-stu-id="ff5de-115">The name of the source file and the line within the source file that logged the trace message.</span></span><br/>          |
| [<span data-ttu-id="ff5de-116">**FlagName**</span><span class="sxs-lookup"><span data-stu-id="ff5de-116">**FlagsName**</span></span>](eventschema-flagname-debugdatatype-element.md)            | <span data-ttu-id="ff5de-117">string</span><span class="sxs-lookup"><span data-stu-id="ff5de-117">string</span></span>      | <span data-ttu-id="ff5de-118">O valor do sinalizador passado ao provedor quando ele foi habilitado.</span><span class="sxs-lookup"><span data-stu-id="ff5de-118">The flag value passed to the provider when it was enabled.</span></span><br/>                                              |
| [<span data-ttu-id="ff5de-119">**Função**</span><span class="sxs-lookup"><span data-stu-id="ff5de-119">**Function**</span></span>](eventschema-function-debugdatatype-element.md)             | <span data-ttu-id="ff5de-120">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ff5de-120">unsignedInt</span></span> | <span data-ttu-id="ff5de-121">O nome da função que registrou a mensagem de rastreamento.</span><span class="sxs-lookup"><span data-stu-id="ff5de-121">The name of the function that logged the trace message.</span></span><br/>                                                 |
| [<span data-ttu-id="ff5de-122">**LevelName**</span><span class="sxs-lookup"><span data-stu-id="ff5de-122">**LevelName**</span></span>](eventschema-levelname-debugdatatype-element.md)           | <span data-ttu-id="ff5de-123">string</span><span class="sxs-lookup"><span data-stu-id="ff5de-123">string</span></span>      | <span data-ttu-id="ff5de-124">O valor de nível passado ao provedor quando ele foi habilitado.</span><span class="sxs-lookup"><span data-stu-id="ff5de-124">The level value passed to the provider when it was enabled.</span></span><br/>                                             |
| [<span data-ttu-id="ff5de-125">**Mensagem**</span><span class="sxs-lookup"><span data-stu-id="ff5de-125">**Message**</span></span>](eventschema-message-debugdatatype-element.md)               | <span data-ttu-id="ff5de-126">string</span><span class="sxs-lookup"><span data-stu-id="ff5de-126">string</span></span>      | <span data-ttu-id="ff5de-127">A cadeia de caracteres da mensagem.</span><span class="sxs-lookup"><span data-stu-id="ff5de-127">The message string.</span></span> <span data-ttu-id="ff5de-128">O XML contém esse elemento se o evento WPP especificou o campo FormatString.</span><span class="sxs-lookup"><span data-stu-id="ff5de-128">The XML contains this element if the WPP event specified the FormattedString field.</span></span><br/> |
| [<span data-ttu-id="ff5de-129">**SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="ff5de-129">**SequenceNumber**</span></span>](eventschema-sequencenumber-debugdatatype-element.md) | <span data-ttu-id="ff5de-130">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ff5de-130">unsignedInt</span></span> | <span data-ttu-id="ff5de-131">O número de sequência local ou global da mensagem de rastreamento.</span><span class="sxs-lookup"><span data-stu-id="ff5de-131">The local or global sequence number of the trace message.</span></span><br/>                                               |
| [<span data-ttu-id="ff5de-132">**Subcomponente**</span><span class="sxs-lookup"><span data-stu-id="ff5de-132">**SubComponent**</span></span>](eventschema-subcomponent-debugdatatype-element.md)     | <span data-ttu-id="ff5de-133">string</span><span class="sxs-lookup"><span data-stu-id="ff5de-133">string</span></span>      | <span data-ttu-id="ff5de-134">O nome do subcomponente que registrou a mensagem de rastreamento.</span><span class="sxs-lookup"><span data-stu-id="ff5de-134">The name of the subcomponent that logged the trace message.</span></span><br/>                                             |



## <a name="remarks"></a><span data-ttu-id="ff5de-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="ff5de-135">Remarks</span></span>

<span data-ttu-id="ff5de-136">Os elementos serão incluídos somente se o provedor definir a variável de \_ ambiente% Trace Format% \_ prefix para incluí-los.</span><span class="sxs-lookup"><span data-stu-id="ff5de-136">The elements are included only if the provider set the %TRACE\_FORMAT\_PREFIX% environment variable to include them.</span></span> <span data-ttu-id="ff5de-137">Para obter detalhes sobre esses elementos, consulte rastrear mensagem prefixo.</span><span class="sxs-lookup"><span data-stu-id="ff5de-137">For details on these elements, see Trace Message Prefix.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff5de-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff5de-138">Requirements</span></span>



| <span data-ttu-id="ff5de-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff5de-139">Requirement</span></span> | <span data-ttu-id="ff5de-140">Valor</span><span class="sxs-lookup"><span data-stu-id="ff5de-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ff5de-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ff5de-141">Minimum supported client</span></span><br/> | <span data-ttu-id="ff5de-142">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ff5de-142">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ff5de-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ff5de-143">Minimum supported server</span></span><br/> | <span data-ttu-id="ff5de-144">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ff5de-144">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





