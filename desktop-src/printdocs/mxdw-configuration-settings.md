---
description: O Microsoft XPS Document Writer (MXDW) permite que os usuários criem arquivos de documento XPS Imprimindo de qualquer aplicativo do Windows.
ms.assetid: 1fa50337-2df7-48d3-a179-0ca5ae3dfda3
title: Definições de configuração do MXDW
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4026a99baa33ec50bc3ad129ef6610a428f83ab
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105810958"
---
# <a name="mxdw-configuration-settings"></a><span data-ttu-id="b1f8d-103">Definições de configuração do MXDW</span><span class="sxs-lookup"><span data-stu-id="b1f8d-103">MXDW Configuration Settings</span></span>

<span data-ttu-id="b1f8d-104">O Microsoft XPS Document Writer (MXDW) permite que os usuários criem arquivos de documento XPS Imprimindo de qualquer aplicativo do Windows.</span><span class="sxs-lookup"><span data-stu-id="b1f8d-104">The Microsoft XPS Document Writer (MXDW) enables users to create XPS document files by printing from any Windows application.</span></span> <span data-ttu-id="b1f8d-105">Os desenvolvedores de aplicativos podem controlar as seguintes configurações de saída do MXDW usando as partes PrintTicket e PrintCapabilities do [esquema de impressão](./printschema.md).</span><span class="sxs-lookup"><span data-stu-id="b1f8d-105">Applications developers can control the following output settings of the MXDW using the PrintTicket and PrintCapabilities parts of the [Print Schema](./printschema.md).</span></span>

## <a name="jobinterleaving"></a><span data-ttu-id="b1f8d-106">JobInterleaving</span><span class="sxs-lookup"><span data-stu-id="b1f8d-106">JobInterleaving</span></span>

<span data-ttu-id="b1f8d-107">A configuração JobInterleaving controla a ordem de intercalação de conteúdo para os documentos XPS.</span><span class="sxs-lookup"><span data-stu-id="b1f8d-107">The JobInterleaving setting controls the content interleaving order for the XPS Documents.</span></span> <span data-ttu-id="b1f8d-108">Para obter informações sobre intercalação de trabalhos, consulte a [especificação de papel XML](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf).</span><span class="sxs-lookup"><span data-stu-id="b1f8d-108">For information about job interleaving, see the [XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf).</span></span> <span data-ttu-id="b1f8d-109">O MXDW dá suporte às duas opções a seguir para essa configuração:</span><span class="sxs-lookup"><span data-stu-id="b1f8d-109">MXDW supports the following two options for this setting:</span></span>

-   <span data-ttu-id="b1f8d-110">**Off** -esta opção desabilita a intercalação para que todos os dados de cada elemento de conteúdo no documento sejam contíguos, o que melhora a eficiência do acesso aleatório.</span><span class="sxs-lookup"><span data-stu-id="b1f8d-110">**Off** - This option disables interleaving so that all data for each content element in the document is contiguous, which improves the efficiency of random access.</span></span> <span data-ttu-id="b1f8d-111">Essa opção é melhor para exibir um documento XPS.</span><span class="sxs-lookup"><span data-stu-id="b1f8d-111">This option is best for viewing an XPS document.</span></span>
-   <span data-ttu-id="b1f8d-112">A opção **on** -this permite a intercalação para que os dados de cada elemento de conteúdo sejam divididos e reordenados para um processamento sequencial mais eficiente.</span><span class="sxs-lookup"><span data-stu-id="b1f8d-112">**On** - This option enables interleaving so that data for each content element is broken up and reordered for more efficient sequential processing.</span></span> <span data-ttu-id="b1f8d-113">Essa opção é melhor para download e impressão na Web.</span><span class="sxs-lookup"><span data-stu-id="b1f8d-113">This option is best for web download and printing.</span></span>

<span data-ttu-id="b1f8d-114">O exemplo a seguir é um exemplo do XML de PrintCapabilities que inclui a configuração JobInterleaving.</span><span class="sxs-lookup"><span data-stu-id="b1f8d-114">The following example is an example of the PrintCapabilities XML that includes the JobInterleaving setting.</span></span>


```XML
<psf:Feature name="ns0000:JobInterleaving">
   <psf:Property name="psf:SelectionType">
      <psf:Value xsi:type="xsd:QName">psk:PickOne</psf:Value> 
   </psf:Property>
   <psf:Property name="psk:DisplayName">
      <psf:Value xsi:type="xsd:string">Interleaving</psf:Value> 
   </psf:Property>
   <psf:Option name="ns0000:OFF" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">Off - Best for viewing</psf:Value> 
      </psf:Property>
   </psf:Option>
   <psf:Option name="ns0000:ON" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">On - Best for the web/printing</psf:Value> 
      </psf:Property>
   </psf:Option>
</psf:Feature>
```



<span data-ttu-id="b1f8d-115">O XML PrintTicket é semelhante, exceto que ele especifica uma opção específica.</span><span class="sxs-lookup"><span data-stu-id="b1f8d-115">The PrintTicket XML is similar, except that it specifies a particular option.</span></span> <span data-ttu-id="b1f8d-116">Consulte o [esquema de impressão](./printschema.md) para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="b1f8d-116">See the [Print Schema](./printschema.md) for details.</span></span>

<span data-ttu-id="b1f8d-117">Como JobInterleaving não é uma das [palavras-chave públicas do esquema de impressão](./print-schema-public-keywords.md), você deve incluir uma declaração do namespace (neste caso, "ns0000" na marca **PrintCapabilities** (ou **PrintTicket**) no início do documento PrintCapabilities (ou PrintTicket), conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="b1f8d-117">Since JobInterleaving is not one of the [Print Schema Public Keywords](./print-schema-public-keywords.md), you must include a declaration of the namespace (in this case "ns0000" in the **PrintCapabilities** (or **PrintTicket**) tag at the beginning of the PrintCapabilities (or PrintTicket) document, as shown in the following example:</span></span>


```XML
<psf:PrintCapabilities 
xmlns:psf="http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework" 
xmlns:xsi="https://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="https://www.w3.org/2001/XMLSchema"  
version="1" 
xmlns:ns0000=http://schemas.microsoft.com/windows/2006/06/printing/printschemakeywords/microsoftxpsdocumentwriter>
```



## <a name="jobimagetype"></a><span data-ttu-id="b1f8d-118">JobImageType</span><span class="sxs-lookup"><span data-stu-id="b1f8d-118">JobImageType</span></span>

<span data-ttu-id="b1f8d-119">JobImageType controla o formato de saída dos formatos de bitmap inseridos.</span><span class="sxs-lookup"><span data-stu-id="b1f8d-119">JobImageType controls the output format of embedded bitmap formats.</span></span> <span data-ttu-id="b1f8d-120">O MXDW dá suporte às quatro opções a seguir para essa configuração:</span><span class="sxs-lookup"><span data-stu-id="b1f8d-120">MXDW supports the following four options for this setting:</span></span>

-   <span data-ttu-id="b1f8d-121">**JPEGHigh** -essa opção especifica a imagem JPEG com um alto nível de compactação.</span><span class="sxs-lookup"><span data-stu-id="b1f8d-121">**JPEGHigh** - This option specifies the JPEG image with a high level of compression.</span></span> <span data-ttu-id="b1f8d-122">Essa opção produz o menor tamanho de arquivo, mas a qualidade de imagem mais baixa.</span><span class="sxs-lookup"><span data-stu-id="b1f8d-122">This option produces the smallest file size, but the lowest image quality.</span></span>
-   <span data-ttu-id="b1f8d-123">**JPEGMed** -essa opção especifica a imagem JPEG com um nível médio de compactação.</span><span class="sxs-lookup"><span data-stu-id="b1f8d-123">**JPEGMed** - This option specifies the JPEG image with a medium level of compression.</span></span> <span data-ttu-id="b1f8d-124">Essa opção fornece o melhor equilíbrio entre o tamanho do arquivo e a qualidade da imagem.</span><span class="sxs-lookup"><span data-stu-id="b1f8d-124">This option provides the best balance of file size and image quality.</span></span>
-   <span data-ttu-id="b1f8d-125">**JPEGLow** -essa opção especifica a imagem JPEG com um baixo nível de compactação.</span><span class="sxs-lookup"><span data-stu-id="b1f8d-125">**JPEGLow** - This option specifies the JPEG image with a low level of compression.</span></span> <span data-ttu-id="b1f8d-126">Essa opção produz a redução mínima no tamanho do arquivo e a alta qualidade da imagem.</span><span class="sxs-lookup"><span data-stu-id="b1f8d-126">This option produces the least reduction in file size and high image quality.</span></span>
-   <span data-ttu-id="b1f8d-127">**Png** -essa opção especifica o formato de imagem png com compactação sem perdas.</span><span class="sxs-lookup"><span data-stu-id="b1f8d-127">**PNG** - This option specifies the PNG image format with lossless compression.</span></span> <span data-ttu-id="b1f8d-128">Essa opção produz o maior tamanho de arquivo e a qualidade de imagem mais alta.</span><span class="sxs-lookup"><span data-stu-id="b1f8d-128">This option produces the largest file size and the highest image quality.</span></span>

<span data-ttu-id="b1f8d-129">O XML de PrintCapabilities da configuração JobImageType aparece abaixo:</span><span class="sxs-lookup"><span data-stu-id="b1f8d-129">The PrintCapabilities XML of the JobImageType setting appears below:</span></span>


```XML
<psf:Feature name="ns0000:JobImageType">
   <psf:Property name="psf:SelectionType">
      <psf:Value xsi:type="xsd:QName">psk:PickOne</psf:Value> 
   </psf:Property>
   <psf:Property name="psk:DisplayName">
      <psf:Value xsi:type="xsd:string">Images</psf:Value> 
   </psf:Property>
   <psf:Option name="ns0000:JPEGHigh" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">JPG - Maximum compression</psf:Value> 
      </psf:Property>
   </psf:Option>
   <psf:Option name="ns0000:JPEGMed" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
        <psf:Value xsi:type="xsd:string">JPG - Medium compression</psf:Value> 
      </psf:Property>
   </psf:Option>
   <psf:Option name="ns0000:JPEGLow" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">JPG - Minimum compression</psf:Value> 
      </psf:Property>
   </psf:Option>
   <psf:Option name="ns0000:PNG" constrained="psk:None">
      <psf:Property name="psk:DisplayName">
         <psf:Value xsi:type="xsd:string">PNG - Lossless compression</psf:Value> 
      </psf:Property>
   </psf:Option>
</psf:Feature>
```



<span data-ttu-id="b1f8d-130">O XML PrintTicket é semelhante, exceto que ele especifica uma opção específica.</span><span class="sxs-lookup"><span data-stu-id="b1f8d-130">The PrintTicket XML is similar, except that it specifies a particular option.</span></span> <span data-ttu-id="b1f8d-131">Consulte o [esquema de impressão](./printschema.md) para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="b1f8d-131">See the [Print Schema](./printschema.md) for details.</span></span>

<span data-ttu-id="b1f8d-132">Como JobImageType não é uma das [palavras-chave públicas do esquema de impressão](./print-schema-public-keywords.md), você deve incluir uma declaração do namespace (neste caso, "ns0000" na marca **PrintCapabilities** (ou **PrintTicket**) no início do documento PrintCapabilities (ou PrintTicket), conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="b1f8d-132">Since JobImageType is not one of the [Print Schema Public Keywords](./print-schema-public-keywords.md), you must include a declaration of the namespace (in this case "ns0000" in the **PrintCapabilities** (or **PrintTicket**) tag at the beginning of the PrintCapabilities (or PrintTicket) document, as shown in the following example:</span></span>


```XML
<psf:PrintTicket 
xmlns:psf="http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework" 
xmlns:xsi="https://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="https://www.w3.org/2001/XMLSchema"  
version="1" 
xmlns:ns0000=http://schemas.microsoft.com/windows/2006/06/printing/printschemakeywords/microsoftxpsdocumentwriter>
```



## <a name="related-topics"></a><span data-ttu-id="b1f8d-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b1f8d-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1f8d-134">Especificação de Papel XML</span><span class="sxs-lookup"><span data-stu-id="b1f8d-134">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> <dt>

[<span data-ttu-id="b1f8d-135">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="b1f8d-135">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> <dt>

[<span data-ttu-id="b1f8d-136">Imprimir esquema</span><span class="sxs-lookup"><span data-stu-id="b1f8d-136">Print Schema</span></span>](./printschema.md)
</dt> <dt>

[<span data-ttu-id="b1f8d-137">Downloads de licença e de especificação XPS</span><span class="sxs-lookup"><span data-stu-id="b1f8d-137">XPS Specification and License Downloads</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
