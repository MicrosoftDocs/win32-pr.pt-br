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
# <a name="app-support-for-openxps-printing"></a>Suporte de aplicativo para impressão OpenXPS

OpenXPS é o formato de especificação de papel XML aberto para documentos e é baseado na especificação padrão da ECMA (Associação de fabricantes de computadores Europeu).

O Windows 8 fornece suporte completo para a impressão OpenXPS por meio do modelo de driver de impressão v4, lado a lado com suporte contínuo para o formato XPS da Microsoft. E este tópico se concentra na parte desse suporte que é relevante para os desenvolvedores de aplicativos do Windows. Para obter informações sobre os requisitos de driver para o suporte do OpenXPS, consulte [suporte de driver para OpenXPS](/windows-hardware/drivers/print/printer-driver-overview).

## <a name="sending-xps-data-to-the-print-system"></a>Enviando dados XPS para o sistema de impressão

Recomendamos que você use [**IPrintDocumentPackageTarget**](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget) para enviar todos os trabalhos de impressão XPS para o sistema de impressão. O **IPrintDocumentPackageTarget** aceita o OM (modelo de objeto XPS) sem serialização, e isso ajuda a melhorar o desempenho geral.

Aqui está um breve resumo da interface **IPrintDocumentPackageTarget** :

-   Essa interface oferece suporte à impressão de soluções personalizadas, bem como a aplicativos de área de trabalho.

-   Para aplicativos de desktops, isso pode ser usado no lugar de [**StartXpsPrintJob1**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob1).

-   Disponível no Windows 7 com Service Pack 1 (SP1) + atualização de plataforma e Windows 8.

-   Inclua *DocumentTarget. h* em projetos para usar essas APIs.

Os aplicativos que consomem documentos OpenXPS devem observar que o tipo MIME para OpenXPS é o seguinte:

<dl> oXPS do aplicativo \\  
</dl>

## <a name="sending-openxps-data-to-the-xps-print-api"></a>Enviando dados do OpenXPS para a API de impressão do XPS

Específico do OpenXPS, o OM XPS aceita MSXPS e OpenXPS e fornece métodos para conversão e serialização em qualquer formato. Isso permite que os desenvolvedores de aplicativos sejam independentes do driver de destino, se desejarem. Isso também significa que os desenvolvedores de aplicativos sempre podem enviar trabalhos de impressão como um OM XPS para StartXpsPrintJob1 ou IDocumentPackageTarget, sabendo que o sistema de impressão tratará qualquer conversão necessária.

É claro que impedir a conversão entre formatos XPS melhorará o desempenho de ponta a ponta. A partir do aplicativo, o desenvolvedor pode verificar a seguinte chave do registro para determinar o formato XPS preferencial do driver de impressão de destino:

``` syntax
HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Print\Printers\[PrintDriverName]\PrintDriverData\XpsFormat
```

Depois que o formato XPS preferido for determinado, o aplicativo poderá fornecer objetos de OM XPS que não exigirão conversão. De uma determinada observação é o uso da foto de HD em MSXPS e JPEGXR no OpenXPS. Converter de JPEGXR para foto de HD é relativamente leve, já que a principal diferença nessa conversão é que o HD Photo ignora 4 bits de controle que o JPEGXR exige. No entanto, a conversão de foto de HD para JPEGXR exige que a imagem inteira seja codificada novamente para gerar os bits de controle necessários. Portanto, o fornecimento de imagens JPEGXR para imagens de alta resolução garantirá a compatibilidade com o OpenXPS e minimizará o custo de conversão da imagem para MSXPS.

O cabeçalho *Xpsobjectmodel \_ 1. h* define as APIs e os objetos adicionais para OpenXPS. E a interface IXpsOMObjectFactory1 fornece métodos adicionais para conversão de imagem. Esta é a sintaxe:


```C++
IXpsOMObjectFactory1->ConvertHDPhotoToJpegXR(IXpsOMImageResource *imageResource);

IXpsOMObjectFactory1->ConvertJpegXRToHDPhoto(IXpsOMImageResource *imageResource);
```



O Windows 8 fornece as seguintes enumerações novas e atualizadas.

Nova enumeração:

<dl>

[**\_tipo de documento XPS \_**](/windows/win32/api/xpsobjectmodel_1/ne-xpsobjectmodel_1-xps_document_type)  
</dl>

Enumeração atualizada

<dl>

[**\_tipo de imagem XPS \_**](/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_image_type)  
</dl>

Os novos métodos getdocumenttype permitem que um aplicativo determine o formato XPS dos documentos. Eles estão disponíveis em [**IXpsOMObjectFactory1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsomobjectfactory1), [**IXpsOMPackage1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsompackage1)e [**IXpsOMPage1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsompage1). Aqui está uma lista dos métodos.

<dl>

[**IXpsOMObjectFactory1::GetDocumentTypeFromFile**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromfile)  
[**IXpsOMObjectFactory1::GetDocumentTypeFromStream**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromstream)  
[**IXpsOMPackage1:: getdocumenttype**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompackage1-getdocumenttype)  
[**IXpsOMPage1:: getdocumenttype**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompage1-getdocumenttype)  
</dl>

O Windows 8 fornece os seguintes novos códigos de erro para dar suporte ao OpenXPS:

<dl> \_namespace XPS E \_ incompatível \_ . <dl> Esse erro será retornado se houver um namespace incompatível.  
</dl> </dd> XPS\_E\_ABSOLUTE\_REFERENCE. <dl> Esse erro será retornado se MSXPS usar URIs absolutos em referências internas ou tentar usar referências internas para serializar no fluxo. Isso ocorre porque o OM XPS gera URIs relativos. E, embora o MSXPS dê suporte a URIs relativos e absolutos, o OpenXPS requer URIs relativos.  
</dl> </dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Suporte de driver para OpenXPS](/windows-hardware/drivers/print/printer-driver-overview)
</dt> <dt>

[**IPrintDocumentPackageTarget**](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget)
</dt> <dt>

[**IXpsOMObjectFactory1::GetDocumentTypeFromFile**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromfile)
</dt> <dt>

[**IXpsOMObjectFactory1::GetDocumentTypeFromStream**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromstream)
</dt> <dt>

[**IXpsOMPackage1:: getdocumenttype**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompackage1-getdocumenttype)
</dt> <dt>

[**IXpsOMPage1:: getdocumenttype**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompage1-getdocumenttype)
</dt> <dt>

[**\_tipo de documento XPS \_**](/windows/win32/api/xpsobjectmodel_1/ne-xpsobjectmodel_1-xps_document_type)
</dt> <dt>

[**\_tipo de imagem XPS \_**](/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_image_type)
</dt> </dl>

 

 
