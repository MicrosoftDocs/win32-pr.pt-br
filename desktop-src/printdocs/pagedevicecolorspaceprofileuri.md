---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: ab26850e-554a-4a1b-9250-edb0b4e17fe2
title: PageDeviceColorSpaceProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4536251150851ad02abf41ca26ffaa36699281db
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105786195"
---
# <a name="pagedevicecolorspaceprofileuri"></a><span data-ttu-id="02300-104">PageDeviceColorSpaceProfileURI</span><span class="sxs-lookup"><span data-stu-id="02300-104">PageDeviceColorSpaceProfileURI</span></span>

<span data-ttu-id="02300-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="02300-105">This topic is not current.</span></span> <span data-ttu-id="02300-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="02300-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="02300-107">Especifica um URI relativo para a raiz do pacote para um perfil ICC contido em um documento XPS.</span><span class="sxs-lookup"><span data-stu-id="02300-107">Specifies a relative URI to the package root to an ICC profile contained in an XPS Document.</span></span> <span data-ttu-id="02300-108">O processamento dessa opção depende da configuração do recurso PageDeviceColorSpaceUsage.</span><span class="sxs-lookup"><span data-stu-id="02300-108">The processing of this option depends of the setting of the PageDeviceColorSpaceUsage feature.</span></span> <span data-ttu-id="02300-109">Todos os elementos que usam esse perfil já estão no espaço de cores do dispositivo apropriado e não serão gerenciados por cores no driver ou no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="02300-109">All elements using that profile are assumed to be already in the appropriate device color space, and will not be color managed in the driver or device.</span></span>

-   [<span data-ttu-id="02300-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="02300-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="02300-111">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="02300-111">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="02300-112">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="02300-112">Element Information</span></span>



| <span data-ttu-id="02300-113">Nome</span><span class="sxs-lookup"><span data-stu-id="02300-113">Name</span></span>                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02300-114">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="02300-114">Element Type</span></span> <br/>   | <span data-ttu-id="02300-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="02300-115">ParameterDef</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="02300-116">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="02300-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="02300-117">?</span><span class="sxs-lookup"><span data-stu-id="02300-117">Page</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="02300-118">Observações</span><span class="sxs-lookup"><span data-stu-id="02300-118">Notes</span></span> <br/>          | <span data-ttu-id="02300-119">Isso se aplica somente a documentos XPS e não deve ser usado em PrintTickets arbitrários.</span><span class="sxs-lookup"><span data-stu-id="02300-119">This applies to XPS Documents only and should not be used in arbitrary PrintTickets.</span></span><br/> <span data-ttu-id="02300-120">Os consumidores em conformidade com XPS devem impor que uma referência de URI a um recurso como uma imagem ou um perfil de cor em um documento de recursos de impressão ou PrintTicket deve se referir a um nome de parte (um URI relativo para a raiz do pacote) dentro do mesmo pacote de documento XPS que contém o PrintTicket resultante.</span><span class="sxs-lookup"><span data-stu-id="02300-120">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="02300-121">Um consumidor XPS compatível não deve usar um URI que não seja compatível com a sintaxe do nome da parte.</span><span class="sxs-lookup"><span data-stu-id="02300-121">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="02300-122">Essas configurações são específicas do XPS.</span><span class="sxs-lookup"><span data-stu-id="02300-122">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="02300-123">Os URIs que são referenciados em um documento de recursos de impressão ou PrintTicket não devem ser resolvidos como URLs.</span><span class="sxs-lookup"><span data-stu-id="02300-123">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="02300-124">Isso não é seguro, pois eles podem não ser resolvidos como pretendidos e podem criar riscos de segurança prejudiciais para o driver e o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="02300-124">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="02300-125">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="02300-125">Structure Content</span></span>

<span data-ttu-id="02300-126">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="02300-126">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="02300-127">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="02300-127">Structure Properties</span></span>

<span data-ttu-id="02300-128">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="02300-128">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="02300-129">Propriedade</span><span class="sxs-lookup"><span data-stu-id="02300-129">Property</span></span>                | <span data-ttu-id="02300-130">xsi:type</span><span class="sxs-lookup"><span data-stu-id="02300-130">xsi:type</span></span>           | <span data-ttu-id="02300-131">Valor</span><span class="sxs-lookup"><span data-stu-id="02300-131">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="02300-132">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="02300-132">DataType</span></span><br/>     | <span data-ttu-id="02300-133">string</span><span class="sxs-lookup"><span data-stu-id="02300-133">string</span></span><br/>  | <span data-ttu-id="02300-134">xs:string</span><span class="sxs-lookup"><span data-stu-id="02300-134">xs:string</span></span><br/>       |
| <span data-ttu-id="02300-135">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="02300-135">DefaultValue</span></span><br/> | <span data-ttu-id="02300-136">string</span><span class="sxs-lookup"><span data-stu-id="02300-136">string</span></span><br/>  | <span data-ttu-id="02300-137">não definido</span><span class="sxs-lookup"><span data-stu-id="02300-137">undefined</span></span><br/>       |
| <span data-ttu-id="02300-138">MaxLength</span><span class="sxs-lookup"><span data-stu-id="02300-138">MaxLength</span></span><br/>    | <span data-ttu-id="02300-139">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="02300-139">integer</span></span><br/> | <span data-ttu-id="02300-140">não definido</span><span class="sxs-lookup"><span data-stu-id="02300-140">undefined</span></span><br/>       |
| <span data-ttu-id="02300-141">MinLength</span><span class="sxs-lookup"><span data-stu-id="02300-141">MinLength</span></span><br/>    | <span data-ttu-id="02300-142">integer</span><span class="sxs-lookup"><span data-stu-id="02300-142">integer</span></span><br/> | <span data-ttu-id="02300-143">1</span><span class="sxs-lookup"><span data-stu-id="02300-143">1</span></span><br/>               |
| <span data-ttu-id="02300-144">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="02300-144">Mandatory</span></span><br/>    | <span data-ttu-id="02300-145">string</span><span class="sxs-lookup"><span data-stu-id="02300-145">string</span></span><br/>  | <span data-ttu-id="02300-146">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="02300-146">psk:Conditional</span></span><br/> |
| <span data-ttu-id="02300-147">UnitType</span><span class="sxs-lookup"><span data-stu-id="02300-147">UnitType</span></span><br/>     | <span data-ttu-id="02300-148">string</span><span class="sxs-lookup"><span data-stu-id="02300-148">string</span></span><br/>  | <span data-ttu-id="02300-149">characters</span><span class="sxs-lookup"><span data-stu-id="02300-149">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="02300-150">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="02300-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02300-151">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="02300-151">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




