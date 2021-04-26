---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: ab26850e-554a-4a1b-9250-edb0b4e17fe2
title: PageDeviceColorSpaceProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20a1b4cf607ddf880311659e562647ba583a2951
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995673"
---
# <a name="pagedevicecolorspaceprofileuri"></a><span data-ttu-id="cdb3a-104">PageDeviceColorSpaceProfileURI</span><span class="sxs-lookup"><span data-stu-id="cdb3a-104">PageDeviceColorSpaceProfileURI</span></span>

<span data-ttu-id="cdb3a-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="cdb3a-105">This topic is not current.</span></span> <span data-ttu-id="cdb3a-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="cdb3a-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="cdb3a-107">Especifica um URI relativo para a raiz do pacote para um perfil ICC contido em um documento XPS.</span><span class="sxs-lookup"><span data-stu-id="cdb3a-107">Specifies a relative URI to the package root to an ICC profile contained in an XPS Document.</span></span> <span data-ttu-id="cdb3a-108">O processamento dessa opção depende da configuração do recurso PageDeviceColorSpaceUsage.</span><span class="sxs-lookup"><span data-stu-id="cdb3a-108">The processing of this option depends of the setting of the PageDeviceColorSpaceUsage feature.</span></span> <span data-ttu-id="cdb3a-109">Todos os elementos que usam esse perfil já estão no espaço de cores do dispositivo apropriado e não serão gerenciados por cores no driver ou no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cdb3a-109">All elements using that profile are assumed to be already in the appropriate device color space, and will not be color managed in the driver or device.</span></span>

-   [<span data-ttu-id="cdb3a-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="cdb3a-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="cdb3a-111">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="cdb3a-111">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="cdb3a-112">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="cdb3a-112">Element Information</span></span>



| <span data-ttu-id="cdb3a-113">Nome</span><span class="sxs-lookup"><span data-stu-id="cdb3a-113">Name</span></span> | <span data-ttu-id="cdb3a-114">Valor</span><span class="sxs-lookup"><span data-stu-id="cdb3a-114">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdb3a-115">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="cdb3a-115">Element Type</span></span> <br/>   | <span data-ttu-id="cdb3a-116">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="cdb3a-116">ParameterDef</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="cdb3a-117">Prefixo de escopo</span><span class="sxs-lookup"><span data-stu-id="cdb3a-117">Scoping Prefix</span></span> <br/> | <span data-ttu-id="cdb3a-118">?</span><span class="sxs-lookup"><span data-stu-id="cdb3a-118">Page</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="cdb3a-119">Observações</span><span class="sxs-lookup"><span data-stu-id="cdb3a-119">Notes</span></span> <br/>          | <span data-ttu-id="cdb3a-120">Isso se aplica somente a documentos XPS e não deve ser usado em PrintTickets arbitrários.</span><span class="sxs-lookup"><span data-stu-id="cdb3a-120">This applies to XPS Documents only and should not be used in arbitrary PrintTickets.</span></span><br/> <span data-ttu-id="cdb3a-121">Os consumidores em conformidade com XPS devem impor que uma referência de URI a um recurso como uma imagem ou um perfil de cor em um documento de recursos de impressão ou PrintTicket deve se referir a um nome de parte (um URI relativo para a raiz do pacote) dentro do mesmo pacote de documento XPS que contém o PrintTicket resultante.</span><span class="sxs-lookup"><span data-stu-id="cdb3a-121">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="cdb3a-122">Um consumidor XPS compatível não deve usar um URI que não seja compatível com a sintaxe do nome da parte.</span><span class="sxs-lookup"><span data-stu-id="cdb3a-122">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="cdb3a-123">Essas configurações são específicas do XPS.</span><span class="sxs-lookup"><span data-stu-id="cdb3a-123">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="cdb3a-124">Os URIs que são referenciados em um documento de recursos de impressão ou PrintTicket não devem ser resolvidos como URLs.</span><span class="sxs-lookup"><span data-stu-id="cdb3a-124">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="cdb3a-125">Isso não é seguro, pois eles podem não ser resolvidos como pretendidos e podem criar riscos de segurança prejudiciais para o driver e o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="cdb3a-125">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="cdb3a-126">Conteúdo da estrutura</span><span class="sxs-lookup"><span data-stu-id="cdb3a-126">Structure Content</span></span>

<span data-ttu-id="cdb3a-127">A estrutura XML desse elemento é:</span><span class="sxs-lookup"><span data-stu-id="cdb3a-127">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="cdb3a-128">Propriedades da estrutura</span><span class="sxs-lookup"><span data-stu-id="cdb3a-128">Structure Properties</span></span>

<span data-ttu-id="cdb3a-129">A tabela a seguir descreve as características das variáveis definidas na estrutura XML.</span><span class="sxs-lookup"><span data-stu-id="cdb3a-129">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="cdb3a-130">Propriedade</span><span class="sxs-lookup"><span data-stu-id="cdb3a-130">Property</span></span>                | <span data-ttu-id="cdb3a-131">xsi:type</span><span class="sxs-lookup"><span data-stu-id="cdb3a-131">xsi:type</span></span>           | <span data-ttu-id="cdb3a-132">Valor</span><span class="sxs-lookup"><span data-stu-id="cdb3a-132">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="cdb3a-133">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="cdb3a-133">DataType</span></span><br/>     | <span data-ttu-id="cdb3a-134">string</span><span class="sxs-lookup"><span data-stu-id="cdb3a-134">string</span></span><br/>  | <span data-ttu-id="cdb3a-135">xs:string</span><span class="sxs-lookup"><span data-stu-id="cdb3a-135">xs:string</span></span><br/>       |
| <span data-ttu-id="cdb3a-136">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="cdb3a-136">DefaultValue</span></span><br/> | <span data-ttu-id="cdb3a-137">string</span><span class="sxs-lookup"><span data-stu-id="cdb3a-137">string</span></span><br/>  | <span data-ttu-id="cdb3a-138">não definido</span><span class="sxs-lookup"><span data-stu-id="cdb3a-138">undefined</span></span><br/>       |
| <span data-ttu-id="cdb3a-139">MaxLength</span><span class="sxs-lookup"><span data-stu-id="cdb3a-139">MaxLength</span></span><br/>    | <span data-ttu-id="cdb3a-140">Número inteiro</span><span class="sxs-lookup"><span data-stu-id="cdb3a-140">integer</span></span><br/> | <span data-ttu-id="cdb3a-141">não definido</span><span class="sxs-lookup"><span data-stu-id="cdb3a-141">undefined</span></span><br/>       |
| <span data-ttu-id="cdb3a-142">MinLength</span><span class="sxs-lookup"><span data-stu-id="cdb3a-142">MinLength</span></span><br/>    | <span data-ttu-id="cdb3a-143">integer</span><span class="sxs-lookup"><span data-stu-id="cdb3a-143">integer</span></span><br/> | <span data-ttu-id="cdb3a-144">1</span><span class="sxs-lookup"><span data-stu-id="cdb3a-144">1</span></span><br/>               |
| <span data-ttu-id="cdb3a-145">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="cdb3a-145">Mandatory</span></span><br/>    | <span data-ttu-id="cdb3a-146">string</span><span class="sxs-lookup"><span data-stu-id="cdb3a-146">string</span></span><br/>  | <span data-ttu-id="cdb3a-147">PSK: condicional</span><span class="sxs-lookup"><span data-stu-id="cdb3a-147">psk:Conditional</span></span><br/> |
| <span data-ttu-id="cdb3a-148">UnitType</span><span class="sxs-lookup"><span data-stu-id="cdb3a-148">UnitType</span></span><br/>     | <span data-ttu-id="cdb3a-149">string</span><span class="sxs-lookup"><span data-stu-id="cdb3a-149">string</span></span><br/>  | <span data-ttu-id="cdb3a-150">characters</span><span class="sxs-lookup"><span data-stu-id="cdb3a-150">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="cdb3a-151">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cdb3a-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cdb3a-152">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="cdb3a-152">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




