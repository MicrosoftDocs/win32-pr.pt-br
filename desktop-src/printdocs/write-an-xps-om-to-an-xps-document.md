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
# <a name="write-an-xps-om-to-an-xps-document"></a>Gravar um OM XPS em um documento XPS

Descreve como gravar o conteúdo de um OM XPS em um programa em um arquivo de documento XPS.

Se um programa tiver um OM XPS que contenha um documento completo, o programa poderá gravar o OM XPS em um arquivo como um documento XPS, chamando o método [**WriteToFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile) da interface [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) .

Antes de usar esses exemplos de código em um programa, leia o aviso de isenção de responsabilidade em [tarefas comuns de programação de documentos XPS](common-xps-document-tasks.md).

## <a name="writing-a-complete-xps-om-to-an-xps-document"></a>Escrevendo um OM XPS completo para um documento XPS

Depois de definir o conteúdo de um OM XPS, você pode salvar o OM XPS em um arquivo como um documento XPS, chamando o método [**WriteToFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetofile) da interface [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) .


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
> Gravar um OM XPS em um arquivo ou fluxo não cria automaticamente uma miniatura para o documento XPS. Para criar uma miniatura do documento XPS, use a interface [**IXpsOMThumbnailGenerator**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator) .

 

## <a name="incrementally-writing-an-xps-document"></a>Escrevendo um documento XPS de forma incremental

A interface [**IXpsOMPackageWriter**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) pode ser usada para gravar as partes de um documento XPS de forma incremental; por exemplo, quando as partes do documento são criadas ou processadas em sequência.

> [!Note]  
> Gravar um OM XPS em um arquivo ou fluxo não cria automaticamente uma miniatura para o documento XPS. Para criar uma miniatura do documento XPS, use a interface [**IXpsOMThumbnailGenerator**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator) .

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Próximas etapas**
</dt> <dt>

[Imprimir um OM XPS](print-an-xps-om.md)
</dt> <dt>

**Usado nesta seção**
</dt> <dt>

[**IOpcPartUri**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[**IXpsOMThumbnailGenerator**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomthumbnailgenerator)
</dt> <dt>

**Para obter mais informações**
</dt> <dt>

[Inicializar um OM XPS](xps-object-model-initialization.md)
</dt> <dt>

[Referência da API do documento XPS](xps-programming-reference.md)
</dt> <dt>

[Especificação de Papel XML](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
