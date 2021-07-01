---
description: Encontre informações sobre o elemento PrintTicket. Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: fe6bd921-cbf3-4cca-afae-82d3822206ba
title: PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b279ff681704a63f6547738c73fb9192d6f8a65d
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120071"
---
# <a name="printticket"></a><span data-ttu-id="020a2-105">PrintTicket</span><span class="sxs-lookup"><span data-stu-id="020a2-105">PrintTicket</span></span>

<span data-ttu-id="020a2-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="020a2-106">This topic is not current.</span></span> <span data-ttu-id="020a2-107">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="020a2-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="020a2-108">Um elemento PrintTicket é o elemento raiz do documento PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="020a2-108">A PrintTicket element is the root element of the PrintTicket document.</span></span> <span data-ttu-id="020a2-109">Um elemento PrintTicket contém todas as informações de formatação de trabalho necessárias para gerar um trabalho.</span><span class="sxs-lookup"><span data-stu-id="020a2-109">A PrintTicket element contains all job formatting information required to output a job.</span></span>

## <a name="element-tag"></a><span data-ttu-id="020a2-110">Marca do elemento</span><span class="sxs-lookup"><span data-stu-id="020a2-110">Element Tag</span></span>

<PrintTicket>

## <a name="xml-attributes"></a><span data-ttu-id="020a2-111">Atributos XML</span><span class="sxs-lookup"><span data-stu-id="020a2-111">XML Attributes</span></span>

<span data-ttu-id="020a2-112">A tabela a seguir lista os atributos XML que podem ser relativos a esse elemento.</span><span class="sxs-lookup"><span data-stu-id="020a2-112">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="020a2-113">Atributo XML</span><span class="sxs-lookup"><span data-stu-id="020a2-113">XML Attribute</span></span>      | <span data-ttu-id="020a2-114">Detalhes</span><span class="sxs-lookup"><span data-stu-id="020a2-114">Details</span></span>                                                                                                                                                                                   |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="020a2-115">version</span><span class="sxs-lookup"><span data-stu-id="020a2-115">version</span></span><br/> | <span data-ttu-id="020a2-116">Especifica a versão do esquema que define os tipos de elemento e sua estrutura, um literal do tipo inteiro.</span><span class="sxs-lookup"><span data-stu-id="020a2-116">Specifies the version of the schema that defines element types and their structure, a literal of type integer.</span></span> <span data-ttu-id="020a2-117">A versão atual do esquema é "1".</span><span class="sxs-lookup"><span data-stu-id="020a2-117">The current schema version is "1".</span></span> <span data-ttu-id="020a2-118">Esse atributo é necessário.</span><span class="sxs-lookup"><span data-stu-id="020a2-118">This attribute is required.</span></span> <br/> |



 

<span data-ttu-id="020a2-119">Para obter mais informações, consulte a seção [atributos XML](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="020a2-119">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="020a2-120">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="020a2-120">Element Information</span></span>

<span data-ttu-id="020a2-121">A tabela a seguir lista os elementos que podem ser pais deste elemento, os elementos que podem ser filhos desse elemento e quaisquer restrições no próprio elemento.</span><span class="sxs-lookup"><span data-stu-id="020a2-121">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="020a2-122">Categoria</span><span class="sxs-lookup"><span data-stu-id="020a2-122">Category</span></span>                   | <span data-ttu-id="020a2-123">Detalhes</span><span class="sxs-lookup"><span data-stu-id="020a2-123">Details</span></span>                                                                                                            |
|----------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="020a2-124">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="020a2-124">Parent elements</span></span><br/> | <span data-ttu-id="020a2-125">Somente raiz do documento.</span><span class="sxs-lookup"><span data-stu-id="020a2-125">Document root only.</span></span><br/>                                                                                     |
| <span data-ttu-id="020a2-126">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="020a2-126">Child elements</span></span><br/>  | <span data-ttu-id="020a2-127">*Recurso* (zero ou mais)</span><span class="sxs-lookup"><span data-stu-id="020a2-127">*Feature* (zero or more)</span></span><br/> <span data-ttu-id="020a2-128">*ParameterInit* (zero ou mais)</span><span class="sxs-lookup"><span data-stu-id="020a2-128">*ParameterInit* (zero or more)</span></span><br/> <span data-ttu-id="020a2-129">*Propriedade* (zero ou mais)</span><span class="sxs-lookup"><span data-stu-id="020a2-129">*Property* (zero or more)</span></span><br/> |
| <span data-ttu-id="020a2-130">Este elemento</span><span class="sxs-lookup"><span data-stu-id="020a2-130">This element</span></span><br/>    | <span data-ttu-id="020a2-131">Nenhum dado de caractere é permitido.</span><span class="sxs-lookup"><span data-stu-id="020a2-131">No character data is permitted.</span></span><br/> <span data-ttu-id="020a2-132">Irmãos filho duplicados não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="020a2-132">Duplicate child siblings are not permitted.</span></span><br/>                  |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="020a2-133">Dependências de configuração</span><span class="sxs-lookup"><span data-stu-id="020a2-133">Configuration Dependencies</span></span>

<span data-ttu-id="020a2-134">As dependências de configuração são aplicáveis somente a elementos em um documento de PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="020a2-134">Configuration dependencies are applicable only to elements in a PrintCapabilities document.</span></span>

## <a name="example"></a><span data-ttu-id="020a2-135">Exemplo</span><span class="sxs-lookup"><span data-stu-id="020a2-135">Example</span></span>

<span data-ttu-id="020a2-136">Consulte o [exemplo de PrintTicket](printticket-example.md).</span><span class="sxs-lookup"><span data-stu-id="020a2-136">See [PrintTicket Example](printticket-example.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="020a2-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="020a2-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="020a2-138">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="020a2-138">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




