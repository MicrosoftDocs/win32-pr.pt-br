---
description: Leia sobre o parâmetro PageDeviceColorSpaceProfileURI. Este tópico não é atual. Para obter as informações mais atuais, consulte a Especificação de Esquema de Impressão.
ms.assetid: ab26850e-554a-4a1b-9250-edb0b4e17fe2
title: PageDeviceColorSpaceProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21420dec2e3057de903b1e04c55a7c6d234343b0
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396641"
---
# <a name="pagedevicecolorspaceprofileuri"></a><span data-ttu-id="d5522-105">PageDeviceColorSpaceProfileURI</span><span class="sxs-lookup"><span data-stu-id="d5522-105">PageDeviceColorSpaceProfileURI</span></span>

<span data-ttu-id="d5522-106">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="d5522-106">This topic is not current.</span></span> <span data-ttu-id="d5522-107">Para obter as informações mais atuais, consulte a [Especificação de Esquema de Impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="d5522-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d5522-108">Especifica um URI relativo para a raiz do pacote para um perfil ICC contido em um documento XPS.</span><span class="sxs-lookup"><span data-stu-id="d5522-108">Specifies a relative URI to the package root to an ICC profile contained in an XPS Document.</span></span> <span data-ttu-id="d5522-109">O processamento dessa opção depende da configuração do recurso PageDeviceColorSpaceUsage.</span><span class="sxs-lookup"><span data-stu-id="d5522-109">The processing of this option depends of the setting of the PageDeviceColorSpaceUsage feature.</span></span> <span data-ttu-id="d5522-110">Presume-se que todos os elementos que usam esse perfil já estão no espaço de cores do dispositivo apropriado e não serão gerenciados por cores no driver ou no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d5522-110">All elements using that profile are assumed to be already in the appropriate device color space, and will not be color managed in the driver or device.</span></span>

-   [<span data-ttu-id="d5522-111">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="d5522-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="d5522-112">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="d5522-112">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="d5522-113">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="d5522-113">Element Information</span></span>



| <span data-ttu-id="d5522-114">Name</span><span class="sxs-lookup"><span data-stu-id="d5522-114">Name</span></span> | <span data-ttu-id="d5522-115">Valor</span><span class="sxs-lookup"><span data-stu-id="d5522-115">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5522-116">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="d5522-116">Element Type</span></span> <br/>   | <span data-ttu-id="d5522-117">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="d5522-117">ParameterDef</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="d5522-118">Prefixo de definição de scoping</span><span class="sxs-lookup"><span data-stu-id="d5522-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="d5522-119">?</span><span class="sxs-lookup"><span data-stu-id="d5522-119">Page</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="d5522-120">Observações</span><span class="sxs-lookup"><span data-stu-id="d5522-120">Notes</span></span> <br/>          | <span data-ttu-id="d5522-121">Isso se aplica somente a documentos XPS e não deve ser usado em PrintTickets arbitrários.</span><span class="sxs-lookup"><span data-stu-id="d5522-121">This applies to XPS Documents only and should not be used in arbitrary PrintTickets.</span></span><br/> <span data-ttu-id="d5522-122">Os consumidores compatíveis com XPS DEVEM impor que uma referência de URI a um recurso, como uma imagem ou perfil de cor em um documento Recursos de Impressão ou PrintTicket, DEVE se referir a um nome de parte (um URI relativo para a raiz do pacote) dentro do mesmo pacote do Documento XPS que contém o PrintTicket resultante.</span><span class="sxs-lookup"><span data-stu-id="d5522-122">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="d5522-123">Um consumidor XPS compatível NÃO DEVE usar um URI que não está em conformidade com a sintaxe de nome da parte.</span><span class="sxs-lookup"><span data-stu-id="d5522-123">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="d5522-124">Essas configurações são específicas do XPS.</span><span class="sxs-lookup"><span data-stu-id="d5522-124">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="d5522-125">URIs que são referenciados em um documento Funcionalidades de Impressão ou PrintTicket NÃO DEVEM ser resolvidos como URLs.</span><span class="sxs-lookup"><span data-stu-id="d5522-125">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="d5522-126">Isso não é seguro, pois eles podem não ser resolvidos conforme o esperado e podem criar riscos de segurança prejudiciais para o driver e o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="d5522-126">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="d5522-127">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="d5522-127">Structure Content</span></span>

<span data-ttu-id="d5522-128">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="d5522-128">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageDeviceColorSpaceProfileURI">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">characters</psf:Value>
  </psf:Property>
</psf:ParameterDef>
```

## <a name="structure-properties"></a><span data-ttu-id="d5522-129">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="d5522-129">Structure Properties</span></span>

<span data-ttu-id="d5522-130">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="d5522-130">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="d5522-131">Propriedade</span><span class="sxs-lookup"><span data-stu-id="d5522-131">Property</span></span>                | <span data-ttu-id="d5522-132">xsi:type</span><span class="sxs-lookup"><span data-stu-id="d5522-132">xsi:type</span></span>           | <span data-ttu-id="d5522-133">Valor</span><span class="sxs-lookup"><span data-stu-id="d5522-133">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="d5522-134">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d5522-134">DataType</span></span><br/>     | <span data-ttu-id="d5522-135">string</span><span class="sxs-lookup"><span data-stu-id="d5522-135">string</span></span><br/>  | <span data-ttu-id="d5522-136">xs:string</span><span class="sxs-lookup"><span data-stu-id="d5522-136">xs:string</span></span><br/>       |
| <span data-ttu-id="d5522-137">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="d5522-137">DefaultValue</span></span><br/> | <span data-ttu-id="d5522-138">string</span><span class="sxs-lookup"><span data-stu-id="d5522-138">string</span></span><br/>  | <span data-ttu-id="d5522-139">não definido</span><span class="sxs-lookup"><span data-stu-id="d5522-139">undefined</span></span><br/>       |
| <span data-ttu-id="d5522-140">MaxLength</span><span class="sxs-lookup"><span data-stu-id="d5522-140">MaxLength</span></span><br/>    | <span data-ttu-id="d5522-141">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="d5522-141">integer</span></span><br/> | <span data-ttu-id="d5522-142">não definido</span><span class="sxs-lookup"><span data-stu-id="d5522-142">undefined</span></span><br/>       |
| <span data-ttu-id="d5522-143">Minlength</span><span class="sxs-lookup"><span data-stu-id="d5522-143">MinLength</span></span><br/>    | <span data-ttu-id="d5522-144">integer</span><span class="sxs-lookup"><span data-stu-id="d5522-144">integer</span></span><br/> | <span data-ttu-id="d5522-145">1</span><span class="sxs-lookup"><span data-stu-id="d5522-145">1</span></span><br/>               |
| <span data-ttu-id="d5522-146">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="d5522-146">Mandatory</span></span><br/>    | <span data-ttu-id="d5522-147">string</span><span class="sxs-lookup"><span data-stu-id="d5522-147">string</span></span><br/>  | <span data-ttu-id="d5522-148">psk:Conditional</span><span class="sxs-lookup"><span data-stu-id="d5522-148">psk:Conditional</span></span><br/> |
| <span data-ttu-id="d5522-149">Unittype</span><span class="sxs-lookup"><span data-stu-id="d5522-149">UnitType</span></span><br/>     | <span data-ttu-id="d5522-150">string</span><span class="sxs-lookup"><span data-stu-id="d5522-150">string</span></span><br/>  | <span data-ttu-id="d5522-151">characters</span><span class="sxs-lookup"><span data-stu-id="d5522-151">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="d5522-152">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d5522-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5522-153">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="d5522-153">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




