---
description: Este tópico descreve como enviar dados de controle de impressora diretamente para impressoras que usam drivers de impressora XPSDrv.
ms.assetid: 7e98e08a-d572-451d-befb-18fc86f0e505
title: 'Como: enviar dados diretamente para uma impressora XPS'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d78a8c36d6862860862059f9bbcc8db25e171b19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105808369"
---
# <a name="how-to-send-data-directly-to-an-xps-printer"></a><span data-ttu-id="3e000-103">Como: enviar dados diretamente para uma impressora XPS</span><span class="sxs-lookup"><span data-stu-id="3e000-103">How To: Send Data Directly to an XPS Printer</span></span>

<span data-ttu-id="3e000-104">Este tópico descreve como enviar dados de controle de impressora diretamente para impressoras que usam drivers de impressora XPSDrv.</span><span class="sxs-lookup"><span data-stu-id="3e000-104">This topic describes how to send printer control data directly to printers that use XPSDrv printer drivers.</span></span>

<span data-ttu-id="3e000-105">As etapas a seguir descrevem como enviar dados diretamente para uma impressora.</span><span class="sxs-lookup"><span data-stu-id="3e000-105">The following steps describe how to send data directly to a printer.</span></span> <span data-ttu-id="3e000-106">Essas etapas também são ilustradas no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="3e000-106">These steps are also illustrated in the code example that follows.</span></span>

1.  <span data-ttu-id="3e000-107">Chame [**OpenPrinter**](openprinter.md) para obter um identificador para a impressora.</span><span class="sxs-lookup"><span data-stu-id="3e000-107">Call [**OpenPrinter**](openprinter.md) to get a handle to the printer.</span></span>
2.  <span data-ttu-id="3e000-108">Inicialize uma estrutura [**DOCINFO**](/windows/desktop/api/wingdi/ns-wingdi-docinfoa) com os dados da impressora.</span><span class="sxs-lookup"><span data-stu-id="3e000-108">Initialize a [**DOCINFO**](/windows/desktop/api/wingdi/ns-wingdi-docinfoa) structure with the printer data.</span></span>
3.  <span data-ttu-id="3e000-109">Chame [**StartDocPrinter**](startdocprinter.md) para indicar que o aplicativo enviará dados de documento para a impressora.</span><span class="sxs-lookup"><span data-stu-id="3e000-109">Call [**StartDocPrinter**](startdocprinter.md) to indicate that the application will be sending document data to the printer.</span></span>
4.  <span data-ttu-id="3e000-110">Chame [**WritePrinter**](writeprinter.md) para enviar os dados.</span><span class="sxs-lookup"><span data-stu-id="3e000-110">Call [**WritePrinter**](writeprinter.md) to send the data.</span></span>
5.  <span data-ttu-id="3e000-111">Chame [**EndDocPrinter**](enddocprinter.md) para indicar que todos os dados deste documento foram enviados.</span><span class="sxs-lookup"><span data-stu-id="3e000-111">Call [**EndDocPrinter**](enddocprinter.md) to indicate that all data for this document has been sent.</span></span>
6.  <span data-ttu-id="3e000-112">Chame [**ClosePrinter**](closeprinter.md) para liberar os recursos.</span><span class="sxs-lookup"><span data-stu-id="3e000-112">Call [**ClosePrinter**](closeprinter.md) to release the resources.</span></span>

<span data-ttu-id="3e000-113">Envie dados de controle de impressora diretamente para impressoras que usam drivers de impressora XPSDrv.</span><span class="sxs-lookup"><span data-stu-id="3e000-113">Send printer control data directly to printers that use XPSDrv printer drivers.</span></span>


```C++
// 
//  RawDataToXpsPrinter - sends binary data directly to a printer 
//          with an XPSDrv Printer Driver 
//  
// szPrinterName: NULL-terminated string specifying printer name 
// lpData:        Pointer to raw data bytes 
// dwCount        Length of lpData in bytes 
//  
// Returns: TRUE for success, FALSE for failure. 
//  
BOOL RawDataToXpsPrinter (LPTSTR szPrinterName, LPBYTE lpData, DWORD dwCount)
{
    BOOL     bStatus = FALSE;
    HANDLE     hPrinter = NULL;
    DOC_INFO_1       DocInfo;
    DWORD    dwPrtJob = 0L;
    DWORD    dwBytesWritten = 0L;

    // Open a handle to the printer. 
    bStatus = OpenPrinter (szPrinterName, &hPrinter, NULL);
    
    if (bStatus) {
        // Fill in the structure with info about this "document." 
        DocInfo.pDocName = (LPTSTR)_T("My Document");
        DocInfo.pOutputFile = NULL;

        // Enter the datatype of this buffer.
        //  Use "XPS_PASS" when the data buffer should bypass the 
        //    print filter pipeline of the XPSDrv printer driver. 
        //    This datatype would be used to send the buffer directly 
        //    to the printer, such as when sending print head alignment 
        //    commands. Normally, a data buffer would be sent as the
        //    "RAW" datatype.
        //
        DocInfo.pDatatype = (LPTSTR)_T("XPS_PASS");

        dwPrtJob = StartDocPrinter (
                        hPrinter,
                        1,
                        (LPBYTE)&DocInfo);

        if (dwPrtJob > 0) {
                // Send the data to the printer. 
                bStatus = WritePrinter (
                hPrinter,
                lpData,
                dwCount,
                &dwBytesWritten);
        }
        
        EndDocPrinter (hPrinter);

        // Close the printer handle. 
        bStatus = ClosePrinter(hPrinter);
    }
    
    if (!bStatus || (dwCount != dwBytesWritten)) {
        bStatus = FALSE;
    } else {
        bStatus = TRUE;
    }

    return bStatus;
}
```



## <a name="related-topics"></a><span data-ttu-id="3e000-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3e000-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e000-115">**ClosePrinter**</span><span class="sxs-lookup"><span data-stu-id="3e000-115">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="3e000-116">**EndDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="3e000-116">**EndDocPrinter**</span></span>](enddocprinter.md)
</dt> <dt>

[<span data-ttu-id="3e000-117">**EndPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="3e000-117">**EndPagePrinter**</span></span>](endpageprinter.md)
</dt> <dt>

[<span data-ttu-id="3e000-118">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="3e000-118">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="3e000-119">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="3e000-119">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="3e000-120">**StartPagePrinter**</span><span class="sxs-lookup"><span data-stu-id="3e000-120">**StartPagePrinter**</span></span>](startpageprinter.md)
</dt> <dt>

[<span data-ttu-id="3e000-121">**WritePrinter**</span><span class="sxs-lookup"><span data-stu-id="3e000-121">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

 
