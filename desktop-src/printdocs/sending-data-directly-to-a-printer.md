---
description: O exemplo de código mais adiante neste tópico mostra como enviar dados de controle de impressora diretamente para impressoras que usam drivers de impressora baseados em GDI.
ms.assetid: 321f2333-d88e-4042-b9b1-0d918b3209d4
title: 'Como: enviar dados diretamente para uma impressora GDI'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1968b435068a62ce7a7d379a66c1500d04d8936a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105772733"
---
# <a name="how-to-send-data-directly-to-a-gdi-printer"></a><span data-ttu-id="a166d-103">Como: enviar dados diretamente para uma impressora GDI</span><span class="sxs-lookup"><span data-stu-id="a166d-103">How To: Send Data Directly to a GDI Printer</span></span>

<span data-ttu-id="a166d-104">O exemplo de código mais adiante neste tópico mostra como enviar dados de controle de impressora diretamente para impressoras que usam drivers de impressora baseados em GDI.</span><span class="sxs-lookup"><span data-stu-id="a166d-104">The code sample later in this topic shows how to send printer control data directly to printers that use GDI-based printer drivers.</span></span>

<span data-ttu-id="a166d-105">As etapas a seguir descrevem como enviar dados diretamente para uma impressora.</span><span class="sxs-lookup"><span data-stu-id="a166d-105">The following steps describe how to send data directly to a printer.</span></span> <span data-ttu-id="a166d-106">Essas etapas também são ilustradas no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="a166d-106">These steps are also illustrated in the code example that follows.</span></span>

1.  <span data-ttu-id="a166d-107">Chame [**OpenPrinter**](openprinter.md) para obter um identificador para a impressora.</span><span class="sxs-lookup"><span data-stu-id="a166d-107">Call [**OpenPrinter**](openprinter.md) to get a handle to the printer.</span></span>
2.  <span data-ttu-id="a166d-108">Inicialize uma estrutura [**DOCINFO**](/windows/desktop/api/wingdi/ns-wingdi-docinfoa) com os dados da impressora.</span><span class="sxs-lookup"><span data-stu-id="a166d-108">Initialize a [**DOCINFO**](/windows/desktop/api/wingdi/ns-wingdi-docinfoa) structure with the printer data.</span></span>
3.  <span data-ttu-id="a166d-109">Chame [**StartDocPrinter**](startdocprinter.md) para indicar que o aplicativo enviará dados de documento para a impressora.</span><span class="sxs-lookup"><span data-stu-id="a166d-109">Call [**StartDocPrinter**](startdocprinter.md) to indicate that the application will be sending document data to the printer.</span></span>
4.  <span data-ttu-id="a166d-110">Chame [**StartPagePrinter**](startpageprinter.md) para indicar que o aplicativo estará enviando uma nova página para a impressora.</span><span class="sxs-lookup"><span data-stu-id="a166d-110">Call [**StartPagePrinter**](startpageprinter.md) to indicate that the application will be sending a new page to the printer.</span></span>
5.  <span data-ttu-id="a166d-111">Chame [**WritePrinter**](writeprinter.md) para enviar os dados.</span><span class="sxs-lookup"><span data-stu-id="a166d-111">Call [**WritePrinter**](writeprinter.md) to send the data.</span></span>
6.  <span data-ttu-id="a166d-112">Chame [**EndPagePrinter**](endpageprinter.md) para indicar que todos os dados da página atual foram enviados.</span><span class="sxs-lookup"><span data-stu-id="a166d-112">Call [**EndPagePrinter**](endpageprinter.md) to indicate that all data for the current page has been sent.</span></span>
7.  <span data-ttu-id="a166d-113">Chame [**EndDocPrinter**](enddocprinter.md) para indicar que todos os dados deste documento foram enviados.</span><span class="sxs-lookup"><span data-stu-id="a166d-113">Call [**EndDocPrinter**](enddocprinter.md) to indicate that all data for this document has been sent.</span></span>
8.  <span data-ttu-id="a166d-114">Chame [**ClosePrinter**](closeprinter.md) para liberar os recursos.</span><span class="sxs-lookup"><span data-stu-id="a166d-114">Call [**ClosePrinter**](closeprinter.md) to release the resources.</span></span>

<span data-ttu-id="a166d-115">Envie dados de controle da impressora diretamente para impressoras que usam drivers de impressora baseados em GDI.</span><span class="sxs-lookup"><span data-stu-id="a166d-115">Send printer control data directly to printers that use GDI-based printer drivers.</span></span>


```C++
// 
// RawDataToPrinter - sends binary data directly to a printer 
//  
// szPrinterName: NULL-terminated string specifying printer name 
// lpData:        Pointer to raw data bytes 
// dwCount        Length of lpData in bytes 
//  
// Returns: TRUE for success, FALSE for failure. 
//  
BOOL RawDataToPrinter(LPTSTR szPrinterName, LPBYTE lpData, DWORD dwCount)
{
    BOOL     bStatus = FALSE;
    HANDLE     hPrinter = NULL;
    DOC_INFO_1 DocInfo;
    DWORD      dwJob = 0L;
    DWORD      dwBytesWritten = 0L;

    // Open a handle to the printer. 
    bStatus = OpenPrinter( szPrinterName, &hPrinter, NULL );
    if (bStatus) {
        // Fill in the structure with info about this "document." 
        DocInfo.pDocName = (LPTSTR)_T("My Document");
        DocInfo.pOutputFile = NULL;
        DocInfo.pDatatype = (LPTSTR)_T("RAW");

        // Inform the spooler the document is beginning. 
        dwJob = StartDocPrinter( hPrinter, 1, (LPBYTE)&DocInfo );
        if (dwJob > 0) {
            // Start a page. 
            bStatus = StartPagePrinter( hPrinter );
            if (bStatus) {
                // Send the data to the printer. 
                bStatus = WritePrinter( hPrinter, lpData, dwCount, &dwBytesWritten);
                EndPagePrinter (hPrinter);
            }
            // Inform the spooler that the document is ending. 
            EndDocPrinter( hPrinter );
        }
        // Close the printer handle. 
        ClosePrinter( hPrinter );
    }
    // Check to see if correct number of bytes were written. 
    if (!bStatus || (dwBytesWritten != dwCount)) {
        bStatus = FALSE;
    } else {
        bStatus = TRUE;
    }
    return bStatus;
}
```



## <a name="related-topics"></a><span data-ttu-id="a166d-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a166d-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a166d-117">**ClosePrinter**</span><span class="sxs-lookup"><span data-stu-id="a166d-117">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="a166d-118">**EndDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="a166d-118">**EndDocPrinter**</span></span>](enddocprinter.md)
</dt> <dt>

[<span data-ttu-id="a166d-119">**EndPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="a166d-119">**EndPagePrinter**</span></span>](endpageprinter.md)
</dt> <dt>

[<span data-ttu-id="a166d-120">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="a166d-120">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="a166d-121">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="a166d-121">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="a166d-122">**StartPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="a166d-122">**StartPagePrinter**</span></span>](startpageprinter.md)
</dt> <dt>

[<span data-ttu-id="a166d-123">**WritePrinter**</span><span class="sxs-lookup"><span data-stu-id="a166d-123">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

 
