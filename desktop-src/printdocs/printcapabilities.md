---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: f503b62f-02e1-4621-8799-a8b6ad12f489
title: PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e10c6dd8ce98b071f1eb239762544a9b72160035
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105762215"
---
# <a name="printcapabilities"></a><span data-ttu-id="5caf7-104">PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="5caf7-104">PrintCapabilities</span></span>

<span data-ttu-id="5caf7-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="5caf7-105">This topic is not current.</span></span> <span data-ttu-id="5caf7-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5caf7-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5caf7-107">Um elemento PrintCapabilities representa a raiz do documento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="5caf7-107">A PrintCapabilities element represents the root of the PrintCapabilities document.</span></span> <span data-ttu-id="5caf7-108">O documento PrintCapabilities contém todas as informações necessárias para descrever os atributos de dispositivo com suporte, considerando uma configuração de dispositivo específica.</span><span class="sxs-lookup"><span data-stu-id="5caf7-108">The PrintCapabilities document contains all of the information needed to describe the supported device attributes, given a particular device configuration.</span></span>

## <a name="element-tag"></a><span data-ttu-id="5caf7-109">Marca do elemento</span><span class="sxs-lookup"><span data-stu-id="5caf7-109">Element Tag</span></span>

<PrintCapabilities>

## <a name="xml-attributes"></a><span data-ttu-id="5caf7-110">Atributos XML</span><span class="sxs-lookup"><span data-stu-id="5caf7-110">XML Attributes</span></span>

<span data-ttu-id="5caf7-111">A tabela a seguir lista os atributos XML que podem ser relativos a esse elemento.</span><span class="sxs-lookup"><span data-stu-id="5caf7-111">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="5caf7-112">Atributo XML</span><span class="sxs-lookup"><span data-stu-id="5caf7-112">XML Attribute</span></span>      | <span data-ttu-id="5caf7-113">Detalhes</span><span class="sxs-lookup"><span data-stu-id="5caf7-113">Details</span></span>                                                                                                                                                                                                             |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5caf7-114">version</span><span class="sxs-lookup"><span data-stu-id="5caf7-114">version</span></span><br/> | <span data-ttu-id="5caf7-115">Especifica a versão do esquema que define os tipos de elemento e sua estrutura.</span><span class="sxs-lookup"><span data-stu-id="5caf7-115">Specifies the version of the schema that defines element types and their structure.</span></span> <span data-ttu-id="5caf7-116">O atributo Version é do tipo inteiro.</span><span class="sxs-lookup"><span data-stu-id="5caf7-116">The version attribute is of type integer.</span></span> <span data-ttu-id="5caf7-117">A versão do esquema atual é designada como "1".</span><span class="sxs-lookup"><span data-stu-id="5caf7-117">The current schema version is designated "1".</span></span> <span data-ttu-id="5caf7-118">Esse atributo é necessário.</span><span class="sxs-lookup"><span data-stu-id="5caf7-118">This attribute is required.</span></span> <br/> |



 

<span data-ttu-id="5caf7-119">Para obter mais informações, consulte a seção [atributos XML](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="5caf7-119">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="5caf7-120">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="5caf7-120">Element Information</span></span>

<span data-ttu-id="5caf7-121">A tabela a seguir lista os elementos que podem ser pais deste elemento, os elementos que podem ser filhos desse elemento e quaisquer restrições no próprio elemento.</span><span class="sxs-lookup"><span data-stu-id="5caf7-121">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="5caf7-122">Category</span><span class="sxs-lookup"><span data-stu-id="5caf7-122">Category</span></span>                   | <span data-ttu-id="5caf7-123">Detalhes</span><span class="sxs-lookup"><span data-stu-id="5caf7-123">Details</span></span>                                                                                                           |
|----------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5caf7-124">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="5caf7-124">Parent elements</span></span><br/> | <span data-ttu-id="5caf7-125">Somente raiz do documento.</span><span class="sxs-lookup"><span data-stu-id="5caf7-125">Document root only.</span></span><br/>                                                                                    |
| <span data-ttu-id="5caf7-126">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="5caf7-126">Child elements</span></span><br/>  | <span data-ttu-id="5caf7-127">*Recurso* (zero ou mais)</span><span class="sxs-lookup"><span data-stu-id="5caf7-127">*Feature* (zero or more)</span></span><br/> <span data-ttu-id="5caf7-128">*ParameterDef* (zero ou mais)</span><span class="sxs-lookup"><span data-stu-id="5caf7-128">*ParameterDef* (zero or more)</span></span><br/> <span data-ttu-id="5caf7-129">*Propriedade* (zero ou mais)</span><span class="sxs-lookup"><span data-stu-id="5caf7-129">*Property* (zero or more)</span></span><br/> |
| <span data-ttu-id="5caf7-130">Este elemento</span><span class="sxs-lookup"><span data-stu-id="5caf7-130">This element</span></span><br/>    | <span data-ttu-id="5caf7-131">Nenhum dado de caractere é permitido.</span><span class="sxs-lookup"><span data-stu-id="5caf7-131">No character data is permitted.</span></span><br/> <span data-ttu-id="5caf7-132">Irmãos filho duplicados não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="5caf7-132">Duplicate child siblings are not permitted.</span></span><br/>                 |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="5caf7-133">Dependências de configuração</span><span class="sxs-lookup"><span data-stu-id="5caf7-133">Configuration Dependencies</span></span>

<span data-ttu-id="5caf7-134">O elemento raiz pode não ter nenhuma dependência de configuração.</span><span class="sxs-lookup"><span data-stu-id="5caf7-134">The root element may not have any configuration dependencies.</span></span>

## <a name="example"></a><span data-ttu-id="5caf7-135">Exemplo</span><span class="sxs-lookup"><span data-stu-id="5caf7-135">Example</span></span>

<span data-ttu-id="5caf7-136">Consulte o [exemplo de documento PrintCapabilities](printcapabilities-document-example.md).</span><span class="sxs-lookup"><span data-stu-id="5caf7-136">See [PrintCapabilities Document Example](printcapabilities-document-example.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5caf7-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5caf7-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5caf7-138">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="5caf7-138">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




