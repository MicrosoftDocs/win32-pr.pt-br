---
description: Este tópico descreve como recuperar um contexto de dispositivo de impressora.
ms.assetid: b3eb9c48-f4c4-42f1-b189-1fa42670008e
title: Como recuperar um contexto de dispositivo de impressora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39fde55450273e42f3429f173150296fdd67a1c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105772915"
---
# <a name="how-to-retrieve-a-printer-device-context"></a>Como recuperar um contexto de dispositivo de impressora

Este tópico descreve como recuperar um contexto de dispositivo de impressora. Você pode recuperar um contexto de dispositivo de impressora chamando a função [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) diretamente ou pode ser retornado por uma caixa de diálogo **Imprimir** comum.

Quando você exibe uma caixa de diálogo **Imprimir** comum, um usuário poderá selecionar a impressora, as páginas do documento e o número de cópias de documentos que deseja imprimir. A caixa de diálogo **Imprimir** comum retorna essas seleções em uma estrutura de dados.

Este tópico descreve como obter um contexto de dispositivo de impressora usando os métodos a seguir.

-   [Chamar CreateDC](#call-createdc)
-   [Exibir uma caixa de diálogo Imprimir comum](#display-a-print-common-dialog-box)
    -   [Usando a função PrintDlgEx](#using-the-printdlgex-function)
    -   [Usando a função PrintDlg](#using-the-printdlg-function)

## <a name="call-createdc"></a>Chamar CreateDC

Se você souber o dispositivo para o qual deseja imprimir, poderá chamar [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) e passar essas informações diretamente para a função. **CreateDC** retorna um contexto de dispositivo no qual você pode renderizar o conteúdo para impressão.

A chamada mais simples para recuperar um contexto de dispositivo é mostrada no exemplo de código a seguir. O código neste exemplo recupera um contexto de dispositivo para o dispositivo de vídeo padrão.


```C++
    hDC = CreateDC(TEXT("DISPLAY"),NULL,NULL,NULL);
```



Para renderizar em uma impressora específica, você deve especificar "WINSPOOL" como o dispositivo e passar o nome correto da impressora para [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca). Você também pode passar uma estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) na chamada para **CreateDC** se desejar fornecer dados de inicialização específicos do dispositivo para o driver do dispositivo ao criar o contexto do dispositivo.

O exemplo a seguir mostra uma chamada para [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) na qual o driver "winspool" é selecionado e o nome da impressora é especificado por nome.


```C++
    printerDC = CreateDC( L"WINSPOOL", printerName, NULL, NULL);
```



Você pode obter a cadeia de caracteres exata do nome da impressora para passar para [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) chamando a função [**EnumPrinters**](enumprinters.md) . O exemplo de código a seguir mostra como chamar **EnumPrinters** e obter os nomes das impressoras locais e conectadas localmente. Como o tamanho do buffer necessário não pode ser conhecido com antecedência, o **EnumPrinters** é chamado duas vezes. A primeira chamada retorna o tamanho do buffer necessário. Essas informações são usadas para alocar um buffer do tamanho necessário e a segunda chamada para **EnumPrinters** retorna os dados desejados.


```C++
    fnReturn = EnumPrinters(
                PRINTER_ENUM_LOCAL | PRINTER_ENUM_CONNECTIONS,
                NULL,
                1L,                // printer info level
                (LPBYTE)NULL,
                0L,
                &dwNeeded,
                &dwReturned);
    
    if (dwNeeded > 0)
    {
        pInfo = (PRINTER_INFO_1 *)HeapAlloc(
                    GetProcessHeap(), 0L, dwNeeded);
    }

    if (NULL != pInfo)
    {
        dwReturned = 0;
        fnReturn = EnumPrinters(
                PRINTER_ENUM_LOCAL | PRINTER_ENUM_CONNECTIONS,
                NULL,
                1L,                // printer info level
                (LPBYTE)pInfo,
                dwNeeded,
                &dwNeeded,
                &dwReturned);
    }

    if (fnReturn)
    {
        // Review the information from all the printers
        //  returned by EnumPrinters.
        for (i=0; i < dwReturned; i++)
        {
            // pThisInfo[i]->pName contains the printer
            //  name to use in the CreateDC function call.
            //
            // When this desired printer is found in the list of
            //  returned printer, set the printerName value to 
            //  use in the call to CreateDC.

            // printerName = pThisInfo[i]->pName
        }
    }
```



## <a name="display-a-print-common-dialog-box"></a>Exibir uma caixa de diálogo Imprimir comum

Você pode escolher entre duas caixas de diálogo de **impressão** comum para exibir a um usuário; a caixa de diálogo mais recente, que pode ser exibida chamando a função [**PRINTDLGEX**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) e a caixa de diálogo estilo mais antigo, que você pode exibir chamando a função [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) . As seções a seguir descrevem como chamar cada caixa de diálogo de um aplicativo.

### <a name="using-the-printdlgex-function"></a>Usando a função PrintDlgEx

Chame a função [**PRINTDLGEX**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) para exibir a folha de propriedades **Imprimir** . Usando a folha de propriedades, o usuário pode especificar informações sobre o trabalho de impressão. Por exemplo, o usuário pode selecionar um intervalo de páginas para imprimir, o número de cópias e assim por diante. O **PRINTDLGEX** também pode recuperar um identificador para um contexto de dispositivo para a impressora selecionada. Você pode usar o identificador para renderizar a saída na impressora.

Para obter o código de exemplo que ilustra o uso de [**PRINTDLGEX**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) para recuperar um contexto de dispositivo de impressora, consulte "usando a folha de propriedades Imprimir" em [usando caixas de diálogo comuns](../dlgbox/using-common-dialog-boxes.md).

### <a name="using-the-printdlg-function"></a>Usando a função PrintDlg

Se seu aplicativo deve ser executado em um sistema que não dá suporte à função [**PRINTDLGEX**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) , como em um sistema que está executando uma versão do Windows anterior ao Windows 2000, ou não precisa da funcionalidade extra que a função **PRINTDLGEX** fornece, use a função [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) . As etapas a seguir descrevem como exibir a caixa de diálogo comum de **impressão** de estilo mais antigo.

1.  Inicialize a estrutura de dados [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) .
2.  Chame [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) para exibir a caixa de diálogo **Imprimir** comum para o usuário.
3.  Se a chamada [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) retornar **true**, bloqueie a memória da estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) retornada. Se a chamada **PRINTDLG** retornar **false**, o usuário pressionou o botão **Cancelar** na caixa de diálogo **Imprimir** comum para que não haja nada mais a ser processado.
4.  Aloque um buffer de memória local grande o suficiente para conter uma cópia da estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) .
5.  Copie a estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) retornada para a alocada localmente.
6.  Salve outras informações retornadas na estrutura [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) e que será necessário processar o trabalho de impressão.
7.  Libere o [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) e os buffers de memória que ele referencia.

O código de exemplo a seguir ilustra como usar a função [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) para obter o contexto do dispositivo e o nome da impressora selecionada.


```C++
// Display the printer dialog box so the user can select the 
//  printer and the number of copies to print.
BOOL            printDlgReturn = FALSE;
HDC                printerDC = NULL;
PRINTDLG        printDlgInfo = {0};
LPWSTR            localPrinterName = NULL;
PDEVMODE        returnedDevmode = NULL;
PDEVMODE        localDevmode = NULL;
int                localNumberOfCopies = 0;

// Initialize the print dialog box's data structure.
printDlgInfo.lStructSize = sizeof( printDlgInfo );
printDlgInfo.Flags = 
    // Return a printer device context.
    PD_RETURNDC 
    // Don't allow separate print to file.
    // Remove these flags if you want to support this feature.
    | PD_HIDEPRINTTOFILE        
    | PD_DISABLEPRINTTOFILE 
    // Don't allow selecting individual document pages to print.
    // Remove this flag if you want to support this feature.
    | PD_NOSELECTION;

// Display the printer dialog and retrieve the printer DC.
printDlgReturn = PrintDlg(&printDlgInfo);

// Check the return value.
if (TRUE == printDlgReturn)
{
    // The user clicked OK so the printer dialog box data 
    //  structure was returned with the user's selections.
    //  Copy the relevant data from the data structure and 
    //  save them to a local data structure.

    //
    // Get the HDC of the selected printer
    printerDC = printDlgInfo.hDC;
    
    // In this example, the DEVMODE structure returned by 
    //    the printer dialog box is copied to a local memory
    //    block and a pointer to the printer name that is 
    //    stored in the copied DEVMODE structure is saved.

    //
    //  Lock the handle to get a pointer to the DEVMODE structure.
    returnedDevmode = (PDEVMODE)GlobalLock(printDlgInfo.hDevMode);

    localDevmode = (LPDEVMODE)HeapAlloc(
                        GetProcessHeap(), 
                        HEAP_ZERO_MEMORY | HEAP_GENERATE_EXCEPTIONS, 
                        returnedDevmode->dmSize);

    if (NULL != localDevmode) 
    {
        memcpy(
            (LPVOID)localDevmode,
            (LPVOID)returnedDevmode, 
            returnedDevmode->dmSize);

        // Save the printer name from the DEVMODE structure.
        //  This is done here just to illustrate how to access
        //  the name field. The printer name can also be accessed
        //  by referring to the dmDeviceName in the local 
        //  copy of the DEVMODE structure.
        localPrinterName = localDevmode->dmDeviceName;

        // Save the number of copies as entered by the user
        localNumberOfCopies = printDlgInfo.nCopies;    
    }
    else
    {
        // Unable to allocate a new structure so leave
        //  the pointer as NULL to indicate that it's empty.
    }

    // Free the DEVMODE structure returned by the print 
    //  dialog box.
    if (NULL != printDlgInfo.hDevMode) 
    {
        GlobalFree(printDlgInfo.hDevMode);
    }
}
else
{
    // The user cancelled out of the print dialog box.
}
```



Para obter mais informações sobre a função [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) , consulte "exibindo a caixa de diálogo Imprimir" em [usando caixas de diálogo comuns](../dlgbox/using-common-dialog-boxes.md).

 

 
