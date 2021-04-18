---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: fe6bd921-cbf3-4cca-afae-82d3822206ba
title: PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3d2e225eb38584e290db55c33594be80d0d7999
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105760297"
---
# <a name="printticket"></a><span data-ttu-id="32b4c-104">PrintTicket</span><span class="sxs-lookup"><span data-stu-id="32b4c-104">PrintTicket</span></span>

<span data-ttu-id="32b4c-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="32b4c-105">This topic is not current.</span></span> <span data-ttu-id="32b4c-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="32b4c-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="32b4c-107">Um elemento PrintTicket é o elemento raiz do documento PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="32b4c-107">A PrintTicket element is the root element of the PrintTicket document.</span></span> <span data-ttu-id="32b4c-108">Um elemento PrintTicket contém todas as informações de formatação de trabalho necessárias para gerar um trabalho.</span><span class="sxs-lookup"><span data-stu-id="32b4c-108">A PrintTicket element contains all job formatting information required to output a job.</span></span>

## <a name="element-tag"></a><span data-ttu-id="32b4c-109">Marca do elemento</span><span class="sxs-lookup"><span data-stu-id="32b4c-109">Element Tag</span></span>

<PrintTicket>

## <a name="xml-attributes"></a><span data-ttu-id="32b4c-110">Atributos XML</span><span class="sxs-lookup"><span data-stu-id="32b4c-110">XML Attributes</span></span>

<span data-ttu-id="32b4c-111">A tabela a seguir lista os atributos XML que podem ser relativos a esse elemento.</span><span class="sxs-lookup"><span data-stu-id="32b4c-111">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="32b4c-112">Atributo XML</span><span class="sxs-lookup"><span data-stu-id="32b4c-112">XML Attribute</span></span>      | <span data-ttu-id="32b4c-113">Detalhes</span><span class="sxs-lookup"><span data-stu-id="32b4c-113">Details</span></span>                                                                                                                                                                                   |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32b4c-114">version</span><span class="sxs-lookup"><span data-stu-id="32b4c-114">version</span></span><br/> | <span data-ttu-id="32b4c-115">Especifica a versão do esquema que define os tipos de elemento e sua estrutura, um literal do tipo inteiro.</span><span class="sxs-lookup"><span data-stu-id="32b4c-115">Specifies the version of the schema that defines element types and their structure, a literal of type integer.</span></span> <span data-ttu-id="32b4c-116">A versão atual do esquema é "1".</span><span class="sxs-lookup"><span data-stu-id="32b4c-116">The current schema version is "1".</span></span> <span data-ttu-id="32b4c-117">Esse atributo é necessário.</span><span class="sxs-lookup"><span data-stu-id="32b4c-117">This attribute is required.</span></span> <br/> |



 

<span data-ttu-id="32b4c-118">Para obter mais informações, consulte a seção [atributos XML](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="32b4c-118">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="32b4c-119">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="32b4c-119">Element Information</span></span>

<span data-ttu-id="32b4c-120">A tabela a seguir lista os elementos que podem ser pais deste elemento, os elementos que podem ser filhos desse elemento e quaisquer restrições no próprio elemento.</span><span class="sxs-lookup"><span data-stu-id="32b4c-120">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="32b4c-121">Category</span><span class="sxs-lookup"><span data-stu-id="32b4c-121">Category</span></span>                   | <span data-ttu-id="32b4c-122">Detalhes</span><span class="sxs-lookup"><span data-stu-id="32b4c-122">Details</span></span>                                                                                                            |
|----------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32b4c-123">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="32b4c-123">Parent elements</span></span><br/> | <span data-ttu-id="32b4c-124">Somente raiz do documento.</span><span class="sxs-lookup"><span data-stu-id="32b4c-124">Document root only.</span></span><br/>                                                                                     |
| <span data-ttu-id="32b4c-125">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="32b4c-125">Child elements</span></span><br/>  | <span data-ttu-id="32b4c-126">*Recurso* (zero ou mais)</span><span class="sxs-lookup"><span data-stu-id="32b4c-126">*Feature* (zero or more)</span></span><br/> <span data-ttu-id="32b4c-127">*ParameterInit* (zero ou mais)</span><span class="sxs-lookup"><span data-stu-id="32b4c-127">*ParameterInit* (zero or more)</span></span><br/> <span data-ttu-id="32b4c-128">*Propriedade* (zero ou mais)</span><span class="sxs-lookup"><span data-stu-id="32b4c-128">*Property* (zero or more)</span></span><br/> |
| <span data-ttu-id="32b4c-129">Este elemento</span><span class="sxs-lookup"><span data-stu-id="32b4c-129">This element</span></span><br/>    | <span data-ttu-id="32b4c-130">Nenhum dado de caractere é permitido.</span><span class="sxs-lookup"><span data-stu-id="32b4c-130">No character data is permitted.</span></span><br/> <span data-ttu-id="32b4c-131">Irmãos filho duplicados não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="32b4c-131">Duplicate child siblings are not permitted.</span></span><br/>                  |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="32b4c-132">Dependências de configuração</span><span class="sxs-lookup"><span data-stu-id="32b4c-132">Configuration Dependencies</span></span>

<span data-ttu-id="32b4c-133">As dependências de configuração são aplicáveis somente a elementos em um documento de PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="32b4c-133">Configuration dependencies are applicable only to elements in a PrintCapabilities document.</span></span>

## <a name="example"></a><span data-ttu-id="32b4c-134">Exemplo</span><span class="sxs-lookup"><span data-stu-id="32b4c-134">Example</span></span>

<span data-ttu-id="32b4c-135">Consulte o [exemplo de PrintTicket](printticket-example.md).</span><span class="sxs-lookup"><span data-stu-id="32b4c-135">See [PrintTicket Example](printticket-example.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="32b4c-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="32b4c-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32b4c-137">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="32b4c-137">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




