---
description: O XPS&\# 160; Imprimir&\# 160; A API fornece uma interface para o spooler de impressão que os aplicativos podem usar para imprimir trabalhos que enviam documentos XPS para uma impressora.
ms.assetid: d3bf7b1d-df21-4e7b-803b-45b65d46b2ca
title: Sobre a API de impressão do XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b1467458a737a6faaddb5ed45c81623207ccdb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091598"
---
# <a name="about-the-xps-print-api"></a><span data-ttu-id="5b206-103">Sobre a API de impressão do XPS</span><span class="sxs-lookup"><span data-stu-id="5b206-103">About the XPS Print API</span></span>

<span data-ttu-id="5b206-104">A [API de impressão XPS](xps-printing.md) fornece uma interface para o spooler de impressão que os aplicativos podem usar para imprimir trabalhos que enviam documentos XPS para uma impressora.</span><span class="sxs-lookup"><span data-stu-id="5b206-104">The [XPS Print API](xps-printing.md) provides an interface to the print spooler that applications can use to print jobs that send XPS documents to a printer.</span></span>

<span data-ttu-id="5b206-105">Se a impressora de destino usar um driver de impressora XPSDrv, a API de impressão XPS possibilitará que o driver de impressora XPSDrv receba eventos de documento à medida que o spooler de impressão processar um trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="5b206-105">If the destination printer uses an XPSDrv printer driver, the XPS Print API makes it possible for the XPSDrv printer driver to receive document events as the print spooler processes a print job.</span></span> <span data-ttu-id="5b206-106">Para obter uma descrição dos eventos de documento que são enviados para o driver de impressora XPSDrv, consulte [eventos de documento do driver XPS](/windows-hardware/drivers/print/xps-driver-document-events).</span><span class="sxs-lookup"><span data-stu-id="5b206-106">For a description of the document events that are sent to the XPSDrv printer driver see [XPS Driver Document Events](/windows-hardware/drivers/print/xps-driver-document-events).</span></span>

<span data-ttu-id="5b206-107">Se a impressora de destino usar um driver de impressora GDI, a [API de impressão XPS](xps-printing.md) permitirá que o sistema manipule a conversão necessária dos dados de trabalho de impressão do formato XPS para o formato EMF (metarquivo avançado) que o driver de impressora GDI usa.</span><span class="sxs-lookup"><span data-stu-id="5b206-107">If the destination printer uses a GDI printer driver, the [XPS Print API](xps-printing.md) lets the system handle the necessary conversion of the print job data from XPS format to the Enhanced Metafile (EMF) format that the GDI printer driver uses.</span></span> <span data-ttu-id="5b206-108">Para obter uma descrição dos eventos de documento do driver de impressora GDI, consulte a [função DocumentEvent](documentevent.md).</span><span class="sxs-lookup"><span data-stu-id="5b206-108">For a description of the GDI printer driver document events see [DocumentEvent Function](documentevent.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5b206-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5b206-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b206-110">Usando a API de impressão XPS</span><span class="sxs-lookup"><span data-stu-id="5b206-110">Using the XPS Print API</span></span>](using-the-xps-print-api.md)
</dt> <dt>

[<span data-ttu-id="5b206-111">Referência da API de impressão do XPS</span><span class="sxs-lookup"><span data-stu-id="5b206-111">XPS Print API Reference</span></span>](xpsprint-api.md)
</dt> </dl>

 

 
