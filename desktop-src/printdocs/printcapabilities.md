---
description: Saiba mais sobre o elemento PrintCapabilities, que representa a raiz do documento PrintCapabilities.
ms.assetid: f503b62f-02e1-4621-8799-a8b6ad12f489
title: PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2158fd651849df2e4ea24c640065f1041569741a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407019"
---
# <a name="printcapabilities"></a><span data-ttu-id="5424f-103">PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="5424f-103">PrintCapabilities</span></span>

<span data-ttu-id="5424f-104">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="5424f-104">This topic is not current.</span></span> <span data-ttu-id="5424f-105">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="5424f-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="5424f-106">Um elemento PrintCapabilities representa a raiz do documento PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="5424f-106">A PrintCapabilities element represents the root of the PrintCapabilities document.</span></span> <span data-ttu-id="5424f-107">O documento PrintCapabilities contém todas as informações necessárias para descrever os atributos de dispositivo com suporte, considerando uma configuração de dispositivo específica.</span><span class="sxs-lookup"><span data-stu-id="5424f-107">The PrintCapabilities document contains all of the information needed to describe the supported device attributes, given a particular device configuration.</span></span>

## <a name="element-tag"></a><span data-ttu-id="5424f-108">Marca do elemento</span><span class="sxs-lookup"><span data-stu-id="5424f-108">Element Tag</span></span>

<PrintCapabilities>

## <a name="xml-attributes"></a><span data-ttu-id="5424f-109">Atributos XML</span><span class="sxs-lookup"><span data-stu-id="5424f-109">XML Attributes</span></span>

<span data-ttu-id="5424f-110">A tabela a seguir lista os atributos XML que podem ser relativos a esse elemento.</span><span class="sxs-lookup"><span data-stu-id="5424f-110">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="5424f-111">Atributo XML</span><span class="sxs-lookup"><span data-stu-id="5424f-111">XML Attribute</span></span>      | <span data-ttu-id="5424f-112">Detalhes</span><span class="sxs-lookup"><span data-stu-id="5424f-112">Details</span></span>                                                                                                                                                                                                             |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5424f-113">version</span><span class="sxs-lookup"><span data-stu-id="5424f-113">version</span></span><br/> | <span data-ttu-id="5424f-114">Especifica a versão do esquema que define os tipos de elemento e sua estrutura.</span><span class="sxs-lookup"><span data-stu-id="5424f-114">Specifies the version of the schema that defines element types and their structure.</span></span> <span data-ttu-id="5424f-115">O atributo Version é do tipo inteiro.</span><span class="sxs-lookup"><span data-stu-id="5424f-115">The version attribute is of type integer.</span></span> <span data-ttu-id="5424f-116">A versão do esquema atual é designada como "1".</span><span class="sxs-lookup"><span data-stu-id="5424f-116">The current schema version is designated "1".</span></span> <span data-ttu-id="5424f-117">Esse atributo é necessário.</span><span class="sxs-lookup"><span data-stu-id="5424f-117">This attribute is required.</span></span> <br/> |



 

<span data-ttu-id="5424f-118">Para obter mais informações, consulte a seção [atributos XML](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="5424f-118">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="5424f-119">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="5424f-119">Element Information</span></span>

<span data-ttu-id="5424f-120">A tabela a seguir lista os elementos que podem ser pais deste elemento, os elementos que podem ser filhos desse elemento e quaisquer restrições no próprio elemento.</span><span class="sxs-lookup"><span data-stu-id="5424f-120">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="5424f-121">Categoria</span><span class="sxs-lookup"><span data-stu-id="5424f-121">Category</span></span>                   | <span data-ttu-id="5424f-122">Detalhes</span><span class="sxs-lookup"><span data-stu-id="5424f-122">Details</span></span>                                                                                                           |
|----------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5424f-123">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="5424f-123">Parent elements</span></span><br/> | <span data-ttu-id="5424f-124">Somente raiz do documento.</span><span class="sxs-lookup"><span data-stu-id="5424f-124">Document root only.</span></span><br/>                                                                                    |
| <span data-ttu-id="5424f-125">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="5424f-125">Child elements</span></span><br/>  | <span data-ttu-id="5424f-126">*Recurso* (zero ou mais)</span><span class="sxs-lookup"><span data-stu-id="5424f-126">*Feature* (zero or more)</span></span><br/> <span data-ttu-id="5424f-127">*ParameterDef* (zero ou mais)</span><span class="sxs-lookup"><span data-stu-id="5424f-127">*ParameterDef* (zero or more)</span></span><br/> <span data-ttu-id="5424f-128">*Propriedade* (zero ou mais)</span><span class="sxs-lookup"><span data-stu-id="5424f-128">*Property* (zero or more)</span></span><br/> |
| <span data-ttu-id="5424f-129">Este elemento</span><span class="sxs-lookup"><span data-stu-id="5424f-129">This element</span></span><br/>    | <span data-ttu-id="5424f-130">Nenhum dado de caractere é permitido.</span><span class="sxs-lookup"><span data-stu-id="5424f-130">No character data is permitted.</span></span><br/> <span data-ttu-id="5424f-131">Irmãos filho duplicados não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="5424f-131">Duplicate child siblings are not permitted.</span></span><br/>                 |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="5424f-132">Dependências de configuração</span><span class="sxs-lookup"><span data-stu-id="5424f-132">Configuration Dependencies</span></span>

<span data-ttu-id="5424f-133">O elemento raiz pode não ter nenhuma dependência de configuração.</span><span class="sxs-lookup"><span data-stu-id="5424f-133">The root element may not have any configuration dependencies.</span></span>

## <a name="example"></a><span data-ttu-id="5424f-134">Exemplo</span><span class="sxs-lookup"><span data-stu-id="5424f-134">Example</span></span>

<span data-ttu-id="5424f-135">Consulte o [exemplo de documento PrintCapabilities](printcapabilities-document-example.md).</span><span class="sxs-lookup"><span data-stu-id="5424f-135">See [PrintCapabilities Document Example](printcapabilities-document-example.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5424f-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5424f-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5424f-137">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="5424f-137">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




