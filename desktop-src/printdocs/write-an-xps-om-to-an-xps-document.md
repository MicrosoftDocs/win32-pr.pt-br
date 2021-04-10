---
description: Descreve como gravar o conteúdo de um OM XPS em um programa em um arquivo de documento XPS.
ms.assetid: 8bee8059-b901-4a99-a7e4-60dad831c239
title: Gravar um OM XPS em um documento XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 811f773394ee9dbbcf77dc75d1429322bb733631
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170356"
---
# <a name="write-an-xps-om-to-an-xps-document"></a><span data-ttu-id="904b2-103">Gravar um OM XPS em um documento XPS</span><span class="sxs-lookup"><span data-stu-id="904b2-103">Write an XPS OM to an XPS Document</span></span>

<span data-ttu-id="904b2-104">Descreve como gravar o conteúdo de um OM XPS em um programa em um arquivo de documento XPS.</span><span class="sxs-lookup"><span data-stu-id="904b2-104">Describes how to write the contents of an XPS OM in a program to an XPS document file.</span></span>

<span data-ttu-id="904b2-105">Se um programa tiver um OM XPS que contenha um documento completo, o programa poderá gravar o OM XPS em um arquivo como um documento XPS, chamando o método [**WriteToFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile) da interface [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) .</span><span class="sxs-lookup"><span data-stu-id="904b2-105">If a program has an XPS OM that contains a complete document, the program can write the XPS OM to a file as an XPS document, by calling the [**WriteToFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile) method of the [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) interface.</span></span>

<span data-ttu-id="904b2-106">Antes de usar esses exemplos de código em um programa, leia o aviso de isenção de responsabilidade em [tarefas comuns de programação de documentos XPS](common-xps-document-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="904b2-106">Before using these code examples in a program, read the disclaimer in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).</span></span>

## <a name="writing-a-complete-xps-om-to-an-xps-document"></a><span data-ttu-id="904b2-107">Escrevendo um OM XPS completo para um documento XPS</span><span class="sxs-lookup"><span data-stu-id="904b2-107">Writing a complete XPS OM to an XPS document</span></span>

<span data-ttu-id="904b2-108">Depois de definir o conteúdo de um OM XPS, você pode salvar o OM XPS em um arquivo como um documento XPS, chamando o método [**WriteToFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile) da interface [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) .</span><span class="sxs-lookup"><span data-stu-id="904b2-108">After you set the contents of an XPS OM, you can save the XPS OM to a file as an XPS document, by calling the [**WriteToFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile) method of the [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) interface.</span></span>


```C++
    HRESULT hr = S_OK;

    hr = xpsPackage->WriteToFile(
        fileName,
        NULL,                    // LPSECURITY_ATTRIBUTES
        FILE_ATTRIBUTE_NORMAL,
        FALSE                    // Optimize Markup Size
        );

```



> [!Note]  
> <span data-ttu-id="904b2-109">Gravar um OM XPS em um arquivo ou fluxo não cria automaticamente uma miniatura para o documento XPS.</span><span class="sxs-lookup"><span data-stu-id="904b2-109">Writing an XPS OM to a file or stream does not automatically create a thumbnail for the XPS document.</span></span> <span data-ttu-id="904b2-110">Para criar uma miniatura do documento XPS, use a interface [**IXpsOMThumbnailGenerator**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator) .</span><span class="sxs-lookup"><span data-stu-id="904b2-110">To create a thumbnail of the XPS document, use the [**IXpsOMThumbnailGenerator**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator) interface.</span></span>

 

## <a name="incrementally-writing-an-xps-document"></a><span data-ttu-id="904b2-111">Escrevendo um documento XPS de forma incremental</span><span class="sxs-lookup"><span data-stu-id="904b2-111">Incrementally writing an XPS document</span></span>

<span data-ttu-id="904b2-112">A interface [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) pode ser usada para gravar as partes de um documento XPS de forma incremental; por exemplo, quando as partes do documento são criadas ou processadas em sequência.</span><span class="sxs-lookup"><span data-stu-id="904b2-112">The [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) interface can be used to write the parts of an XPS document incrementally; for example, when the document parts are created or processed in sequence.</span></span>

> [!Note]  
> <span data-ttu-id="904b2-113">Gravar um OM XPS em um arquivo ou fluxo não cria automaticamente uma miniatura para o documento XPS.</span><span class="sxs-lookup"><span data-stu-id="904b2-113">Writing an XPS OM to a file or stream does not automatically create a thumbnail for the XPS document.</span></span> <span data-ttu-id="904b2-114">Para criar uma miniatura do documento XPS, use a interface [**IXpsOMThumbnailGenerator**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator) .</span><span class="sxs-lookup"><span data-stu-id="904b2-114">To create a thumbnail of the XPS document, use the [**IXpsOMThumbnailGenerator**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator) interface.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="904b2-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="904b2-115">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="904b2-116">**Próximas etapas**</span><span class="sxs-lookup"><span data-stu-id="904b2-116">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="904b2-117">Imprimir um OM XPS</span><span class="sxs-lookup"><span data-stu-id="904b2-117">Print an XPS OM</span></span>](print-an-xps-om.md)
</dt> <dt>

<span data-ttu-id="904b2-118">**Usado nesta seção**</span><span class="sxs-lookup"><span data-stu-id="904b2-118">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="904b2-119">**IOpcPartUri**</span><span class="sxs-lookup"><span data-stu-id="904b2-119">**IOpcPartUri**</span></span>](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[<span data-ttu-id="904b2-120">**IXpsOMPackage**</span><span class="sxs-lookup"><span data-stu-id="904b2-120">**IXpsOMPackage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[<span data-ttu-id="904b2-121">**IXpsOMThumbnailGenerator**</span><span class="sxs-lookup"><span data-stu-id="904b2-121">**IXpsOMThumbnailGenerator**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator)
</dt> <dt>

<span data-ttu-id="904b2-122">**Para obter mais informações**</span><span class="sxs-lookup"><span data-stu-id="904b2-122">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="904b2-123">Inicializar um OM XPS</span><span class="sxs-lookup"><span data-stu-id="904b2-123">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)
</dt> <dt>

[<span data-ttu-id="904b2-124">Referência da API do documento XPS</span><span class="sxs-lookup"><span data-stu-id="904b2-124">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="904b2-125">Especificação de Papel XML</span><span class="sxs-lookup"><span data-stu-id="904b2-125">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
