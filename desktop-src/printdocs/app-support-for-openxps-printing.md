---
description: OpenXPS é o formato de especificação de papel XML aberto para documentos e é baseado na especificação padrão da ECMA (Associação de Makeers da Europa).
ms.assetid: 52FB5B3F-BEBF-4851-8BE9-5DC7AE535313
title: Suporte de aplicativo para impressão OpenXPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 914d8c365209ea3486bedd5e0352e63a8e31086f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105784510"
---
# <a name="app-support-for-openxps-printing"></a><span data-ttu-id="7ee30-103">Suporte de aplicativo para impressão OpenXPS</span><span class="sxs-lookup"><span data-stu-id="7ee30-103">App Support for OpenXPS Printing</span></span>

<span data-ttu-id="7ee30-104">OpenXPS é o formato de especificação de papel XML aberto para documentos e é baseado na especificação padrão da ECMA (Associação de fabricantes de computadores Europeu).</span><span class="sxs-lookup"><span data-stu-id="7ee30-104">OpenXPS is the Open XML Paper Specification format for documents, and it’s based on the European Computer Manufacturers Association (ECMA) standard specification.</span></span>

<span data-ttu-id="7ee30-105">O Windows 8 fornece suporte completo para a impressão OpenXPS por meio do modelo de driver de impressão v4, lado a lado com suporte contínuo para o formato XPS da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7ee30-105">Windows 8 provides full support for OpenXPS printing via the v4 print driver model, side-by-side with continued support for the Microsoft XPS format.</span></span> <span data-ttu-id="7ee30-106">E este tópico se concentra na parte desse suporte que é relevante para os desenvolvedores de aplicativos do Windows.</span><span class="sxs-lookup"><span data-stu-id="7ee30-106">And this topic focuses on the portion of this support that is relevant to Windows application developers.</span></span> <span data-ttu-id="7ee30-107">Para obter informações sobre os requisitos de driver para o suporte do OpenXPS, consulte [suporte de driver para OpenXPS](/windows-hardware/drivers/print/printer-driver-overview).</span><span class="sxs-lookup"><span data-stu-id="7ee30-107">For information about driver requirements for OpenXPS support, see [Driver Support for OpenXPS](/windows-hardware/drivers/print/printer-driver-overview).</span></span>

## <a name="sending-xps-data-to-the-print-system"></a><span data-ttu-id="7ee30-108">Enviando dados XPS para o sistema de impressão</span><span class="sxs-lookup"><span data-stu-id="7ee30-108">Sending XPS data to the Print System</span></span>

<span data-ttu-id="7ee30-109">Recomendamos que você use [**IPrintDocumentPackageTarget**](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget) para enviar todos os trabalhos de impressão XPS para o sistema de impressão.</span><span class="sxs-lookup"><span data-stu-id="7ee30-109">We recommend that you use [**IPrintDocumentPackageTarget**](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget) for sending all XPS print jobs to the print system.</span></span> <span data-ttu-id="7ee30-110">O **IPrintDocumentPackageTarget** aceita o OM (modelo de objeto XPS) sem serialização, e isso ajuda a melhorar o desempenho geral.</span><span class="sxs-lookup"><span data-stu-id="7ee30-110">**IPrintDocumentPackageTarget** accepts the XPS object model (OM) without serialization, and that helps to improve the overall performance.</span></span>

<span data-ttu-id="7ee30-111">Aqui está um breve resumo da interface **IPrintDocumentPackageTarget** :</span><span class="sxs-lookup"><span data-stu-id="7ee30-111">Here's a brief summary of the **IPrintDocumentPackageTarget** interface:</span></span>

-   <span data-ttu-id="7ee30-112">Essa interface oferece suporte à impressão de soluções personalizadas, bem como a aplicativos de área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="7ee30-112">This interface supports printing from tailored solutions as well as desktop applications.</span></span>

-   <span data-ttu-id="7ee30-113">Para aplicativos de desktops, isso pode ser usado no lugar de [**StartXpsPrintJob1**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob1).</span><span class="sxs-lookup"><span data-stu-id="7ee30-113">For desktops apps, this can be used in place of [**StartXpsPrintJob1**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob1).</span></span>

-   <span data-ttu-id="7ee30-114">Disponível no Windows 7 com Service Pack 1 (SP1) + atualização de plataforma e Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7ee30-114">Available on Windows 7 with Service Pack 1 (SP1) + Platform Update, and Windows 8.</span></span>

-   <span data-ttu-id="7ee30-115">Inclua *DocumentTarget. h* em projetos para usar essas APIs.</span><span class="sxs-lookup"><span data-stu-id="7ee30-115">Include *DocumentTarget.h* in projects to use these APIs.</span></span>

<span data-ttu-id="7ee30-116">Os aplicativos que consomem documentos OpenXPS devem observar que o tipo MIME para OpenXPS é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="7ee30-116">Applications that consume OpenXPS documents should note that the MIME type for OpenXPS is as follows:</span></span>

<dl> <span data-ttu-id="7ee30-117">oXPS do aplicativo \\</span><span class="sxs-lookup"><span data-stu-id="7ee30-117">application\\oxps</span></span>  
</dl>

## <a name="sending-openxps-data-to-the-xps-print-api"></a><span data-ttu-id="7ee30-118">Enviando dados do OpenXPS para a API de impressão do XPS</span><span class="sxs-lookup"><span data-stu-id="7ee30-118">Sending OpenXPS data to the XPS Print API</span></span>

<span data-ttu-id="7ee30-119">Específico do OpenXPS, o OM XPS aceita MSXPS e OpenXPS e fornece métodos para conversão e serialização em qualquer formato.</span><span class="sxs-lookup"><span data-stu-id="7ee30-119">Specific to OpenXPS, XPS OM accepts both MSXPS and OpenXPS, and provides methods for conversion and serialization to either format.</span></span> <span data-ttu-id="7ee30-120">Isso permite que os desenvolvedores de aplicativos sejam independentes do driver de destino, se desejarem.</span><span class="sxs-lookup"><span data-stu-id="7ee30-120">This allows application developers to be agnostic of the target driver, if they want.</span></span> <span data-ttu-id="7ee30-121">Isso também significa que os desenvolvedores de aplicativos sempre podem enviar trabalhos de impressão como um OM XPS para StartXpsPrintJob1 ou IDocumentPackageTarget, sabendo que o sistema de impressão tratará qualquer conversão necessária.</span><span class="sxs-lookup"><span data-stu-id="7ee30-121">This also means that app developers can always submit print jobs as XPS OM to either StartXpsPrintJob1 or IDocumentPackageTarget, knowing that the print system will handle any necessary conversion.</span></span>

<span data-ttu-id="7ee30-122">É claro que impedir a conversão entre formatos XPS melhorará o desempenho de ponta a ponta.</span><span class="sxs-lookup"><span data-stu-id="7ee30-122">Of course, preventing conversion between XPS formats will improve end-to-end performance.</span></span> <span data-ttu-id="7ee30-123">A partir do aplicativo, o desenvolvedor pode verificar a seguinte chave do registro para determinar o formato XPS preferencial do driver de impressão de destino:</span><span class="sxs-lookup"><span data-stu-id="7ee30-123">From the application, the developer can check the following registry key to determine the preferred XPS format of the targeted print driver:</span></span>

``` syntax
HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Print\Printers\[PrintDriverName]\PrintDriverData\XpsFormat
```

<span data-ttu-id="7ee30-124">Depois que o formato XPS preferido for determinado, o aplicativo poderá fornecer objetos de OM XPS que não exigirão conversão.</span><span class="sxs-lookup"><span data-stu-id="7ee30-124">Once the preferred XPS format has been determined, the application can provide XPS OM objects that will not require conversion.</span></span> <span data-ttu-id="7ee30-125">De uma determinada observação é o uso da foto de HD em MSXPS e JPEGXR no OpenXPS.</span><span class="sxs-lookup"><span data-stu-id="7ee30-125">Of particular note is the use of HD Photo in MSXPS and JPEGXR in OpenXPS.</span></span> <span data-ttu-id="7ee30-126">Converter de JPEGXR para foto de HD é relativamente leve, já que a principal diferença nessa conversão é que o HD Photo ignora 4 bits de controle que o JPEGXR exige.</span><span class="sxs-lookup"><span data-stu-id="7ee30-126">Converting from JPEGXR to HD Photo is relatively lightweight since the primary difference in this conversion is that HD Photo ignores 4 control bits that JPEGXR requires.</span></span> <span data-ttu-id="7ee30-127">No entanto, a conversão de foto de HD para JPEGXR exige que a imagem inteira seja codificada novamente para gerar os bits de controle necessários.</span><span class="sxs-lookup"><span data-stu-id="7ee30-127">However, converting from HD Photo to JPEGXR requires the entire image to be re-encoded in order to generate the required control bits.</span></span> <span data-ttu-id="7ee30-128">Portanto, o fornecimento de imagens JPEGXR para imagens de alta resolução garantirá a compatibilidade com o OpenXPS e minimizará o custo de conversão da imagem para MSXPS.</span><span class="sxs-lookup"><span data-stu-id="7ee30-128">Thus, providing JPEGXR images for high-resolution images will ensure compatibility with OpenXPS and minimize the conversion cost of the image for MSXPS.</span></span>

<span data-ttu-id="7ee30-129">O cabeçalho *Xpsobjectmodel \_ 1. h* define as APIs e os objetos adicionais para OpenXPS.</span><span class="sxs-lookup"><span data-stu-id="7ee30-129">The *Xpsobjectmodel\_1.h* header defines the additional APIs and objects for OpenXPS.</span></span> <span data-ttu-id="7ee30-130">E a interface IXpsOMObjectFactory1 fornece métodos adicionais para conversão de imagem.</span><span class="sxs-lookup"><span data-stu-id="7ee30-130">And the IXpsOMObjectFactory1 interface provides additional methods for image conversion.</span></span> <span data-ttu-id="7ee30-131">Esta é a sintaxe:</span><span class="sxs-lookup"><span data-stu-id="7ee30-131">Here's the syntax:</span></span>


```C++
IXpsOMObjectFactory1->ConvertHDPhotoToJpegXR(IXpsOMImageResource *imageResource);

IXpsOMObjectFactory1->ConvertJpegXRToHDPhoto(IXpsOMImageResource *imageResource);
```



<span data-ttu-id="7ee30-132">O Windows 8 fornece as seguintes enumerações novas e atualizadas.</span><span class="sxs-lookup"><span data-stu-id="7ee30-132">Windows 8 provides the following new and updated enumerations.</span></span>

<span data-ttu-id="7ee30-133">Nova enumeração:</span><span class="sxs-lookup"><span data-stu-id="7ee30-133">New enumeration:</span></span>

<dl>

[<span data-ttu-id="7ee30-134">**\_tipo de documento XPS \_**</span><span class="sxs-lookup"><span data-stu-id="7ee30-134">**XPS\_DOCUMENT\_TYPE**</span></span>](/windows/win32/api/xpsobjectmodel_1/ne-xpsobjectmodel_1-xps_document_type)  
</dl>

<span data-ttu-id="7ee30-135">Enumeração atualizada</span><span class="sxs-lookup"><span data-stu-id="7ee30-135">Updated enumeration</span></span>

<dl>

[<span data-ttu-id="7ee30-136">**\_tipo de imagem XPS \_**</span><span class="sxs-lookup"><span data-stu-id="7ee30-136">**XPS\_IMAGE\_TYPE**</span></span>](/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_image_type)  
</dl>

<span data-ttu-id="7ee30-137">Os novos métodos getdocumenttype permitem que um aplicativo determine o formato XPS dos documentos.</span><span class="sxs-lookup"><span data-stu-id="7ee30-137">The new GetDocumentType methods allow an application to determine the XPS format of documents.</span></span> <span data-ttu-id="7ee30-138">Eles estão disponíveis em [**IXpsOMObjectFactory1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsomobjectfactory1), [**IXpsOMPackage1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsompackage1)e [**IXpsOMPage1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsompage1).</span><span class="sxs-lookup"><span data-stu-id="7ee30-138">These are available in [**IXpsOMObjectFactory1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsomobjectfactory1), [**IXpsOMPackage1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsompackage1), and [**IXpsOMPage1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsompage1).</span></span> <span data-ttu-id="7ee30-139">Aqui está uma lista dos métodos.</span><span class="sxs-lookup"><span data-stu-id="7ee30-139">Here's a list of the methods.</span></span>

<dl>

[<span data-ttu-id="7ee30-140">**IXpsOMObjectFactory1::GetDocumentTypeFromFile**</span><span class="sxs-lookup"><span data-stu-id="7ee30-140">**IXpsOMObjectFactory1::GetDocumentTypeFromFile**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromfile)  
[<span data-ttu-id="7ee30-141">**IXpsOMObjectFactory1::GetDocumentTypeFromStream**</span><span class="sxs-lookup"><span data-stu-id="7ee30-141">**IXpsOMObjectFactory1::GetDocumentTypeFromStream**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromstream)  
[<span data-ttu-id="7ee30-142">**IXpsOMPackage1:: getdocumenttype**</span><span class="sxs-lookup"><span data-stu-id="7ee30-142">**IXpsOMPackage1::GetDocumentType**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompackage1-getdocumenttype)  
[<span data-ttu-id="7ee30-143">**IXpsOMPage1:: getdocumenttype**</span><span class="sxs-lookup"><span data-stu-id="7ee30-143">**IXpsOMPage1::GetDocumentType**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompage1-getdocumenttype)  
</dl>

<span data-ttu-id="7ee30-144">O Windows 8 fornece os seguintes novos códigos de erro para dar suporte ao OpenXPS:</span><span class="sxs-lookup"><span data-stu-id="7ee30-144">Windows 8 provides the following new error codes in support of OpenXPS:</span></span>

<dl> <span data-ttu-id="7ee30-145">\_namespace XPS E \_ incompatível \_ .</span><span class="sxs-lookup"><span data-stu-id="7ee30-145">XPS\_E\_MISMATCHED\_NAMESPACE.</span></span> <dl> <span data-ttu-id="7ee30-146">Esse erro será retornado se houver um namespace incompatível.</span><span class="sxs-lookup"><span data-stu-id="7ee30-146">This error is returned, if there is a mismatched namespace.</span></span>  
</dl> </dd> XPS\_E\_ABSOLUTE\_REFERENCE. <dl> <span data-ttu-id="7ee30-147">Esse erro será retornado se MSXPS usar URIs absolutos em referências internas ou tentar usar referências internas para serializar no fluxo.</span><span class="sxs-lookup"><span data-stu-id="7ee30-147">This error is returned if MSXPS uses absolute URIs in internal references, or attempts to use internal references to serialize in the stream.</span></span> <span data-ttu-id="7ee30-148">Isso ocorre porque o OM XPS gera URIs relativos.</span><span class="sxs-lookup"><span data-stu-id="7ee30-148">That is because XPS OM generates relative URIs.</span></span> <span data-ttu-id="7ee30-149">E, embora o MSXPS dê suporte a URIs relativos e absolutos, o OpenXPS requer URIs relativos.</span><span class="sxs-lookup"><span data-stu-id="7ee30-149">And although MSXPS supports both relative and absolute URIs, OpenXPS requires relative URIs.</span></span>  
</dl> </dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="7ee30-150">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7ee30-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ee30-151">Suporte de driver para OpenXPS</span><span class="sxs-lookup"><span data-stu-id="7ee30-151">Driver Support for OpenXPS</span></span>](/windows-hardware/drivers/print/printer-driver-overview)
</dt> <dt>

[<span data-ttu-id="7ee30-152">**IPrintDocumentPackageTarget**</span><span class="sxs-lookup"><span data-stu-id="7ee30-152">**IPrintDocumentPackageTarget**</span></span>](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget)
</dt> <dt>

[<span data-ttu-id="7ee30-153">**IXpsOMObjectFactory1::GetDocumentTypeFromFile**</span><span class="sxs-lookup"><span data-stu-id="7ee30-153">**IXpsOMObjectFactory1::GetDocumentTypeFromFile**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromfile)
</dt> <dt>

[<span data-ttu-id="7ee30-154">**IXpsOMObjectFactory1::GetDocumentTypeFromStream**</span><span class="sxs-lookup"><span data-stu-id="7ee30-154">**IXpsOMObjectFactory1::GetDocumentTypeFromStream**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromstream)
</dt> <dt>

[<span data-ttu-id="7ee30-155">**IXpsOMPackage1:: getdocumenttype**</span><span class="sxs-lookup"><span data-stu-id="7ee30-155">**IXpsOMPackage1::GetDocumentType**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompackage1-getdocumenttype)
</dt> <dt>

[<span data-ttu-id="7ee30-156">**IXpsOMPage1:: getdocumenttype**</span><span class="sxs-lookup"><span data-stu-id="7ee30-156">**IXpsOMPage1::GetDocumentType**</span></span>](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompage1-getdocumenttype)
</dt> <dt>

[<span data-ttu-id="7ee30-157">**\_tipo de documento XPS \_**</span><span class="sxs-lookup"><span data-stu-id="7ee30-157">**XPS\_DOCUMENT\_TYPE**</span></span>](/windows/win32/api/xpsobjectmodel_1/ne-xpsobjectmodel_1-xps_document_type)
</dt> <dt>

[<span data-ttu-id="7ee30-158">**\_tipo de imagem XPS \_**</span><span class="sxs-lookup"><span data-stu-id="7ee30-158">**XPS\_IMAGE\_TYPE**</span></span>](/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_image_type)
</dt> </dl>

 

 
