---
description: Este tópico descreve como coletar informações do trabalho de impressão do usuário.
ms.assetid: 98ae97e2-25c1-455c-8283-45bb07fb8251
title: Como coletar informações do trabalho de impressão do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c4ddbc874ddbb36aa9b82e8eafeadb46883f528
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104011006"
---
# <a name="how-to-collect-print-job-information-from-the-user"></a>Como coletar informações do trabalho de impressão do usuário

Este tópico descreve como coletar informações do trabalho de impressão do usuário.

## <a name="overview"></a>Visão geral

Coletar informações do trabalho de impressão do usuário chamando a função [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) . Essa função exibe a caixa de diálogo **Imprimir** comum para o usuário e retorna as informações do trabalho de impressão em uma estrutura de dados [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) .

A caixa de diálogo **Imprimir** comum é exibida quando o usuário inicia um trabalho de impressão. A caixa de diálogo **Imprimir** comum é uma caixa de diálogo modal, o que significa que o usuário não pode interagir com a janela principal até que a caixa de diálogo comum seja fechada.

## <a name="collecting-print-job-information"></a>Coletando informações do trabalho de impressão

1.  Inicialize o elemento de estrutura [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) .

    Antes que um programa possa exibir a caixa de diálogo **Imprimir** comum, ele deve alocar e inicializar uma estrutura [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) . Em seguida, ele passa essa estrutura para a função [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) , que exibe a caixa de diálogo e retorna os dados do trabalho de impressão na mesma estrutura. O exemplo de código a seguir mostra como o programa de exemplo executa essa etapa.

    ```C++
    // Initialize the print dialog box's data structure.
    pd.lStructSize = sizeof( pd );
    pd.Flags = 
        // Return a printer device context
        PD_RETURNDC 
        // Don't allow separate print to file.
        | PD_HIDEPRINTTOFILE        
        | PD_DISABLEPRINTTOFILE 
        // Don't allow selecting individual document pages to print.
        | PD_NOSELECTION;
    ```

    

2.  Exiba a caixa de diálogo **Imprimir** comum.

    Chame [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) com a estrutura [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) inicializada para exibir a caixa de diálogo **Imprimir** comum e coletar os dados do usuário, conforme mostrado no exemplo de código a seguir.

    ```C++
    // Display the printer dialog and retrieve the printer DC
    pdReturn = PrintDlg(&pd);
    ```

    

3.  Salve os campos da estrutura [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) e inicie o trabalho de impressão.

    A estrutura [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) contém os dados que descrevem as seleções que o usuário fez na caixa de diálogo Imprimir. Alguns membros da estrutura **PRINTDLG** são identificadores para objetos de memória global. O [programa de amostra de impressão](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208)) copia os dados dos objetos de memória global para os blocos de memória que o programa gerencia e copia outros campos da estrutura **PRINTDLG** para campos em uma estrutura de dados que o programa definiu.

    Depois de armazenar os dados da estrutura [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) na estrutura de dados do programa, você pode abrir a caixa de diálogo progresso da impressão. O procedimento da caixa de diálogo progresso da impressão manipula as mensagens da caixa de diálogo e inicia o thread de processamento de impressão.

    O exemplo de código a seguir mostra como copiar os dados da estrutura [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) para a estrutura de dados do programa e como iniciar o trabalho de impressão.

    ```C++
    // A printer was returned so copy the information from 
    //  the dialog box structure and save it to the application's
    //  data structure.
    //
    //  Lock the handles to get pointers to the memory they refer to.
    PDEVMODE    devmode = (PDEVMODE)GlobalLock(pd.hDevMode);
    LPDEVNAMES  devnames = (LPDEVNAMES)GlobalLock(pd.hDevNames);

    // Free any old devmode structures and allocate a new one and
    // copy the data to the application's data structure.
    if (NULL != threadInfo->devmode)
    {
        HeapFree(GetProcessHeap(), 0L, threadInfo->devmode);
    }

    threadInfo->devmode = (LPDEVMODE)HeapAlloc(
        GetProcessHeap(), 
        PRINT_SAMPLE_HEAP_FLAGS, 
        devmode->dmSize);

    if (NULL != threadInfo->devmode) 
    {
        memcpy(
            (LPVOID)threadInfo->devmode,
            devmode, 
            devmode->dmSize);
    }
    else
    {
        // Unable to allocate a new structure so leave
        // the pointer as NULL to indicate that it's empty.
    }

    // Save the printer name from the devmode structure
    //  This is to make it easier to use. It could be
    //  used directly from the devmode structure.
    threadInfo->printerName = threadInfo->devmode->dmDeviceName;

    // Set the number of copies as entered by the user
    threadInfo->copies = pd.nCopies;

    // Some implementations might support printing more than
    // one package in a print job. For this program, only
    // one package (XPS document) can be printed per print job.
    threadInfo->packages = 1;

    // free allocated buffers from PRINTDLG structure
    if (NULL != pd.hDevMode) GlobalFree(pd.hDevMode);
    if (NULL != pd.hDevNames) GlobalFree(pd.hDevNames);

    // Display the print progress dialog box
    DialogBox(
        threadInfo->applicationInstance, 
        MAKEINTRESOURCE(IDD_PRINT_DLG), 
        hWnd, 
        PrintDlgProc);
    ```

    

4.  Se o usuário clicar no botão **Cancelar** na caixa de diálogo **Imprimir** comum, nenhum outro processamento será executado.

 

 
