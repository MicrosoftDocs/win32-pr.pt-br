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
# <a name="how-to-retrieve-a-printer-device-context"></a><span data-ttu-id="a5773-103">Como recuperar um contexto de dispositivo de impressora</span><span class="sxs-lookup"><span data-stu-id="a5773-103">How To: Retrieve a Printer Device Context</span></span>

<span data-ttu-id="a5773-104">Este tópico descreve como recuperar um contexto de dispositivo de impressora.</span><span class="sxs-lookup"><span data-stu-id="a5773-104">This topic describes how to retrieve a printer device context.</span></span> <span data-ttu-id="a5773-105">Você pode recuperar um contexto de dispositivo de impressora chamando a função [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) diretamente ou pode ser retornado por uma caixa de diálogo **Imprimir** comum.</span><span class="sxs-lookup"><span data-stu-id="a5773-105">You can retrieve a printer device context by calling the [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) function directly, or it can be returned by a **Print** common dialog box.</span></span>

<span data-ttu-id="a5773-106">Quando você exibe uma caixa de diálogo **Imprimir** comum, um usuário poderá selecionar a impressora, as páginas do documento e o número de cópias de documentos que deseja imprimir.</span><span class="sxs-lookup"><span data-stu-id="a5773-106">When you display a **Print** common dialog box a user will be able to select the printer, the pages of the document, and the number of document copies they want to print.</span></span> <span data-ttu-id="a5773-107">A caixa de diálogo **Imprimir** comum retorna essas seleções em uma estrutura de dados.</span><span class="sxs-lookup"><span data-stu-id="a5773-107">The **Print** common dialog box returns these selections in a data structure.</span></span>

<span data-ttu-id="a5773-108">Este tópico descreve como obter um contexto de dispositivo de impressora usando os métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="a5773-108">This topic describes how to obtain a printer device context by using the following methods.</span></span>

-   [<span data-ttu-id="a5773-109">Chamar CreateDC</span><span class="sxs-lookup"><span data-stu-id="a5773-109">Call CreateDC</span></span>](#call-createdc)
-   [<span data-ttu-id="a5773-110">Exibir uma caixa de diálogo Imprimir comum</span><span class="sxs-lookup"><span data-stu-id="a5773-110">Display a Print Common Dialog Box</span></span>](#display-a-print-common-dialog-box)
    -   [<span data-ttu-id="a5773-111">Usando a função PrintDlgEx</span><span class="sxs-lookup"><span data-stu-id="a5773-111">Using the PrintDlgEx Function</span></span>](#using-the-printdlgex-function)
    -   [<span data-ttu-id="a5773-112">Usando a função PrintDlg</span><span class="sxs-lookup"><span data-stu-id="a5773-112">Using the PrintDlg Function</span></span>](#using-the-printdlg-function)

## <a name="call-createdc"></a><span data-ttu-id="a5773-113">Chamar CreateDC</span><span class="sxs-lookup"><span data-stu-id="a5773-113">Call CreateDC</span></span>

<span data-ttu-id="a5773-114">Se você souber o dispositivo para o qual deseja imprimir, poderá chamar [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) e passar essas informações diretamente para a função.</span><span class="sxs-lookup"><span data-stu-id="a5773-114">If you know the device to which you want to print, you can call [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) and pass that information directly to the function.</span></span> <span data-ttu-id="a5773-115">**CreateDC** retorna um contexto de dispositivo no qual você pode renderizar o conteúdo para impressão.</span><span class="sxs-lookup"><span data-stu-id="a5773-115">**CreateDC** returns a device context into which you can render the content to print.</span></span>

<span data-ttu-id="a5773-116">A chamada mais simples para recuperar um contexto de dispositivo é mostrada no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="a5773-116">The simplest call to retrieve a device context is shown in the code example that follows.</span></span> <span data-ttu-id="a5773-117">O código neste exemplo recupera um contexto de dispositivo para o dispositivo de vídeo padrão.</span><span class="sxs-lookup"><span data-stu-id="a5773-117">The code in this example retrieves a device context to the default display device.</span></span>


```C++
    hDC = CreateDC(TEXT("DISPLAY"),NULL,NULL,NULL);
```



<span data-ttu-id="a5773-118">Para renderizar em uma impressora específica, você deve especificar "WINSPOOL" como o dispositivo e passar o nome correto da impressora para [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca).</span><span class="sxs-lookup"><span data-stu-id="a5773-118">To render to a specific printer, you must specify "WINSPOOL" as the device and pass the correct name of the printer to [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca).</span></span> <span data-ttu-id="a5773-119">Você também pode passar uma estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) na chamada para **CreateDC** se desejar fornecer dados de inicialização específicos do dispositivo para o driver do dispositivo ao criar o contexto do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a5773-119">You can also pass a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure in the call to **CreateDC** if you want to provide device-specific initialization data for the device driver when you create the device context.</span></span>

<span data-ttu-id="a5773-120">O exemplo a seguir mostra uma chamada para [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) na qual o driver "winspool" é selecionado e o nome da impressora é especificado por nome.</span><span class="sxs-lookup"><span data-stu-id="a5773-120">The following example shows a call to [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) in which the "WINSPOOL" driver is selected and the printer name is specified by name.</span></span>


```C++
    printerDC = CreateDC( L"WINSPOOL", printerName, NULL, NULL);
```



<span data-ttu-id="a5773-121">Você pode obter a cadeia de caracteres exata do nome da impressora para passar para [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) chamando a função [**EnumPrinters**](enumprinters.md) .</span><span class="sxs-lookup"><span data-stu-id="a5773-121">You can obtain the exact printer name string to pass to [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) by calling the [**EnumPrinters**](enumprinters.md) function.</span></span> <span data-ttu-id="a5773-122">O exemplo de código a seguir mostra como chamar **EnumPrinters** e obter os nomes das impressoras locais e conectadas localmente.</span><span class="sxs-lookup"><span data-stu-id="a5773-122">The following code example shows how to call **EnumPrinters** and get the names of the local and locally connected printers.</span></span> <span data-ttu-id="a5773-123">Como o tamanho do buffer necessário não pode ser conhecido com antecedência, o **EnumPrinters** é chamado duas vezes.</span><span class="sxs-lookup"><span data-stu-id="a5773-123">Because the size of the required buffer cannot be known in advance, the **EnumPrinters** is called two times.</span></span> <span data-ttu-id="a5773-124">A primeira chamada retorna o tamanho do buffer necessário.</span><span class="sxs-lookup"><span data-stu-id="a5773-124">The first call returns the size of the required buffer.</span></span> <span data-ttu-id="a5773-125">Essas informações são usadas para alocar um buffer do tamanho necessário e a segunda chamada para **EnumPrinters** retorna os dados desejados.</span><span class="sxs-lookup"><span data-stu-id="a5773-125">That information is used to allocate a buffer of the required size, and the second call to **EnumPrinters** returns the data that you want.</span></span>


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



## <a name="display-a-print-common-dialog-box"></a><span data-ttu-id="a5773-126">Exibir uma caixa de diálogo Imprimir comum</span><span class="sxs-lookup"><span data-stu-id="a5773-126">Display a Print Common Dialog Box</span></span>

<span data-ttu-id="a5773-127">Você pode escolher entre duas caixas de diálogo de **impressão** comum para exibir a um usuário; a caixa de diálogo mais recente, que pode ser exibida chamando a função [**PRINTDLGEX**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) e a caixa de diálogo estilo mais antigo, que você pode exibir chamando a função [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a5773-127">You can choose from two **Print** common dialog boxes to display to a user; the newer dialog box, which you can display by calling the [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) function, and the older style dialog box, which you can display by calling the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) function.</span></span> <span data-ttu-id="a5773-128">As seções a seguir descrevem como chamar cada caixa de diálogo de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a5773-128">The following sections describe how to call each dialog box from an application.</span></span>

### <a name="using-the-printdlgex-function"></a><span data-ttu-id="a5773-129">Usando a função PrintDlgEx</span><span class="sxs-lookup"><span data-stu-id="a5773-129">Using the PrintDlgEx Function</span></span>

<span data-ttu-id="a5773-130">Chame a função [**PRINTDLGEX**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) para exibir a folha de propriedades **Imprimir** .</span><span class="sxs-lookup"><span data-stu-id="a5773-130">Call the [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) function to display the **Print** property sheet.</span></span> <span data-ttu-id="a5773-131">Usando a folha de propriedades, o usuário pode especificar informações sobre o trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="a5773-131">By using the property sheet, the user can specify information about the print job.</span></span> <span data-ttu-id="a5773-132">Por exemplo, o usuário pode selecionar um intervalo de páginas para imprimir, o número de cópias e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="a5773-132">For example, the user can select a range of pages to print, the number of copies, and so on.</span></span> <span data-ttu-id="a5773-133">O **PRINTDLGEX** também pode recuperar um identificador para um contexto de dispositivo para a impressora selecionada.</span><span class="sxs-lookup"><span data-stu-id="a5773-133">The **PrintDlgEx** can also retrieve a handle to a device context for the selected printer.</span></span> <span data-ttu-id="a5773-134">Você pode usar o identificador para renderizar a saída na impressora.</span><span class="sxs-lookup"><span data-stu-id="a5773-134">You can use the handle to render output on the printer.</span></span>

<span data-ttu-id="a5773-135">Para obter o código de exemplo que ilustra o uso de [**PRINTDLGEX**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) para recuperar um contexto de dispositivo de impressora, consulte "usando a folha de propriedades Imprimir" em [usando caixas de diálogo comuns](../dlgbox/using-common-dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="a5773-135">For sample code that illustrates the use of [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) to retrieve a printer device context, see "Using the Print Property Sheet" in [Using Common Dialog Boxes](../dlgbox/using-common-dialog-boxes.md).</span></span>

### <a name="using-the-printdlg-function"></a><span data-ttu-id="a5773-136">Usando a função PrintDlg</span><span class="sxs-lookup"><span data-stu-id="a5773-136">Using the PrintDlg Function</span></span>

<span data-ttu-id="a5773-137">Se seu aplicativo deve ser executado em um sistema que não dá suporte à função [**PRINTDLGEX**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) , como em um sistema que está executando uma versão do Windows anterior ao Windows 2000, ou não precisa da funcionalidade extra que a função **PRINTDLGEX** fornece, use a função [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a5773-137">If your application must run on a system that does not support the [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) function, such as on a system that is running a version of Windows earlier than Windows 2000, or does not need the extra functionality that the **PrintDlgEx** function provides, use the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) function.</span></span> <span data-ttu-id="a5773-138">As etapas a seguir descrevem como exibir a caixa de diálogo comum de **impressão** de estilo mais antigo.</span><span class="sxs-lookup"><span data-stu-id="a5773-138">The following steps describe how to display the older style **Print** common dialog box.</span></span>

1.  <span data-ttu-id="a5773-139">Inicialize a estrutura de dados [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) .</span><span class="sxs-lookup"><span data-stu-id="a5773-139">Initialize the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) data structure.</span></span>
2.  <span data-ttu-id="a5773-140">Chame [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) para exibir a caixa de diálogo **Imprimir** comum para o usuário.</span><span class="sxs-lookup"><span data-stu-id="a5773-140">Call [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) to display the **Print** common dialog box to the user.</span></span>
3.  <span data-ttu-id="a5773-141">Se a chamada [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) retornar **true**, bloqueie a memória da estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) retornada.</span><span class="sxs-lookup"><span data-stu-id="a5773-141">If the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) call returns **TRUE**, lock the returned [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure memory.</span></span> <span data-ttu-id="a5773-142">Se a chamada **PRINTDLG** retornar **false**, o usuário pressionou o botão **Cancelar** na caixa de diálogo **Imprimir** comum para que não haja nada mais a ser processado.</span><span class="sxs-lookup"><span data-stu-id="a5773-142">If the **PrintDlg** call returns **FALSE**, the user pressed the **Cancel** button in the **Print** common dialog box so there is nothing more to process.</span></span>
4.  <span data-ttu-id="a5773-143">Aloque um buffer de memória local grande o suficiente para conter uma cópia da estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) .</span><span class="sxs-lookup"><span data-stu-id="a5773-143">Allocate a local memory buffer that is large enough to contain a copy of the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure.</span></span>
5.  <span data-ttu-id="a5773-144">Copie a estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) retornada para a alocada localmente.</span><span class="sxs-lookup"><span data-stu-id="a5773-144">Copy the returned [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure to the locally allocated one.</span></span>
6.  <span data-ttu-id="a5773-145">Salve outras informações retornadas na estrutura [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) e que será necessário processar o trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="a5773-145">Save other information that is returned in the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure and that you will need to process the print job.</span></span>
7.  <span data-ttu-id="a5773-146">Libere o [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) e os buffers de memória que ele referencia.</span><span class="sxs-lookup"><span data-stu-id="a5773-146">Free the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) and the memory buffers it references.</span></span>

<span data-ttu-id="a5773-147">O código de exemplo a seguir ilustra como usar a função [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) para obter o contexto do dispositivo e o nome da impressora selecionada.</span><span class="sxs-lookup"><span data-stu-id="a5773-147">The following example code illustrates how to use the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) function to get the device context and the name of selected printer.</span></span>


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



<span data-ttu-id="a5773-148">Para obter mais informações sobre a função [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) , consulte "exibindo a caixa de diálogo Imprimir" em [usando caixas de diálogo comuns](../dlgbox/using-common-dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="a5773-148">For more information about the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) function, see "Displaying the Print Dialog Box" in [Using Common Dialog Boxes](../dlgbox/using-common-dialog-boxes.md).</span></span>

 

 
