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
# <a name="how-to-send-data-directly-to-a-gdi-printer"></a>Como: enviar dados diretamente para uma impressora GDI

O exemplo de código mais adiante neste tópico mostra como enviar dados de controle de impressora diretamente para impressoras que usam drivers de impressora baseados em GDI.

As etapas a seguir descrevem como enviar dados diretamente para uma impressora. Essas etapas também são ilustradas no exemplo de código a seguir.

1.  Chame [**OpenPrinter**](openprinter.md) para obter um identificador para a impressora.
2.  Inicialize uma estrutura [**DOCINFO**](/windows/desktop/api/wingdi/ns-wingdi-docinfoa) com os dados da impressora.
3.  Chame [**StartDocPrinter**](startdocprinter.md) para indicar que o aplicativo enviará dados de documento para a impressora.
4.  Chame [**StartPagePrinter**](startpageprinter.md) para indicar que o aplicativo estará enviando uma nova página para a impressora.
5.  Chame [**WritePrinter**](writeprinter.md) para enviar os dados.
6.  Chame [**EndPagePrinter**](endpageprinter.md) para indicar que todos os dados da página atual foram enviados.
7.  Chame [**EndDocPrinter**](enddocprinter.md) para indicar que todos os dados deste documento foram enviados.
8.  Chame [**ClosePrinter**](closeprinter.md) para liberar os recursos.

Envie dados de controle da impressora diretamente para impressoras que usam drivers de impressora baseados em GDI.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**ClosePrinter**](closeprinter.md)
</dt> <dt>

[**EndDocPrinter**](enddocprinter.md)
</dt> <dt>

[**EndPagePrinter**](endpageprinter.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> <dt>

[**StartPagePrinter**](startpageprinter.md)
</dt> <dt>

[**WritePrinter**](writeprinter.md)
</dt> </dl>

 

 
