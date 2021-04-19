---
title: Usando caixas de diálogo comuns
description: Esta seção aborda as tarefas que invocam caixas de diálogo comuns.
ms.assetid: ba038bc1-fb5c-4576-be80-7eae7339ba05
keywords:
- Biblioteca de caixa de diálogo comum, tarefas
- caixas de diálogo comuns, usando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 773382a34b048e812a3fb093da0492b0c628fb14
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590653"
---
# <a name="using-common-dialog-boxes"></a><span data-ttu-id="fb6b5-105">Usando caixas de diálogo comuns</span><span class="sxs-lookup"><span data-stu-id="fb6b5-105">Using Common Dialog Boxes</span></span>

<span data-ttu-id="fb6b5-106">Esta seção aborda as tarefas que invocam caixas de diálogo comuns:</span><span class="sxs-lookup"><span data-stu-id="fb6b5-106">This section covers tasks that invoke common dialog boxes:</span></span>

-   [<span data-ttu-id="fb6b5-107">Escolhendo uma cor</span><span class="sxs-lookup"><span data-stu-id="fb6b5-107">Choosing a Color</span></span>](#choosing-a-color)
-   [<span data-ttu-id="fb6b5-108">Escolhendo uma fonte</span><span class="sxs-lookup"><span data-stu-id="fb6b5-108">Choosing a Font</span></span>](#choosing-a-font)
-   [<span data-ttu-id="fb6b5-109">Abrindo um arquivo</span><span class="sxs-lookup"><span data-stu-id="fb6b5-109">Opening a File</span></span>](#opening-a-file)
-   [<span data-ttu-id="fb6b5-110">Exibindo a caixa de diálogo Imprimir</span><span class="sxs-lookup"><span data-stu-id="fb6b5-110">Displaying the Print Dialog Box</span></span>](#displaying-the-print-dialog-box)
-   [<span data-ttu-id="fb6b5-111">Usando a folha de propriedades Imprimir</span><span class="sxs-lookup"><span data-stu-id="fb6b5-111">Using the Print Property Sheet</span></span>](#using-the-print-property-sheet)
-   [<span data-ttu-id="fb6b5-112">Configurando a página impressa</span><span class="sxs-lookup"><span data-stu-id="fb6b5-112">Setting Up the Printed Page</span></span>](#setting-up-the-printed-page)
-   [<span data-ttu-id="fb6b5-113">Localizando texto</span><span class="sxs-lookup"><span data-stu-id="fb6b5-113">Finding Text</span></span>](#finding-text)

## <a name="choosing-a-color"></a><span data-ttu-id="fb6b5-114">Escolhendo uma cor</span><span class="sxs-lookup"><span data-stu-id="fb6b5-114">Choosing a Color</span></span>

<span data-ttu-id="fb6b5-115">Este tópico descreve o código de exemplo que exibe uma caixa de diálogo de **cor** para que um usuário possa selecionar uma cor.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-115">This topic describes sample code that displays a **Color** dialog box so that a user can select a color.</span></span> <span data-ttu-id="fb6b5-116">O código de exemplo primeiro Inicializa uma estrutura [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) e, em seguida, chama a função [**CHOOSECOLOR**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) para exibir a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-116">The sample code first initializes a [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) structure, and then calls the [**ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) function to display the dialog box.</span></span> <span data-ttu-id="fb6b5-117">Se a função retornar **true**, indicando que o usuário selecionou uma cor, o código de exemplo usará a cor selecionada para criar um novo pincel sólido.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-117">If the function returns **TRUE**, indicating that the user selected a color, the sample code uses the selected color to create a new solid brush.</span></span>

<span data-ttu-id="fb6b5-118">Este exemplo usa a estrutura [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) para inicializar a caixa de diálogo da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="fb6b5-118">This example uses the [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) structure to initialize the dialog box as follows:</span></span>

-   <span data-ttu-id="fb6b5-119">Inicializa o membro **lpCustColors** com um ponteiro para uma matriz estática de valores.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-119">Initializes the **lpCustColors** member with a pointer to a static array of values.</span></span> <span data-ttu-id="fb6b5-120">As cores na matriz são inicialmente pretas, mas a matriz estática preserva as cores personalizadas criadas pelo usuário para chamadas [**CHOOSECOLOR**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) subsequentes.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-120">The colors in the array are initially black, but the static array preserves custom colors created by the user for subsequent [**ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) calls.</span></span>
-   <span data-ttu-id="fb6b5-121">Define o sinalizador **CC \_ RGBINIT** e inicializa o membro **rgbResult** para especificar a cor selecionada inicialmente quando a caixa de diálogo é aberta.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-121">Sets the **CC\_RGBINIT** flag and initializes the **rgbResult** member to specify the color that is initially selected when the dialog box opens.</span></span> <span data-ttu-id="fb6b5-122">Se não for especificado, a seleção inicial será preta.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-122">If not specified, the initial selection is black.</span></span> <span data-ttu-id="fb6b5-123">O exemplo usa a variável estática *rgbCurrent* para preservar o valor selecionado entre chamadas para [**CHOOSECOLOR**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fb6b5-123">The example uses the *rgbCurrent* static variable to preserve the selected value between calls to [**ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)).</span></span>
-   <span data-ttu-id="fb6b5-124">Define o **sinalizador \_ FULLOPEN CC** para que a extensão cores personalizadas da caixa de diálogo seja sempre exibida.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-124">Sets the **CC\_FULLOPEN** flag so the custom colors extension of the dialog box is always displayed.</span></span>


```
CHOOSECOLOR cc;                 // common dialog box structure 
static COLORREF acrCustClr[16]; // array of custom colors 
HWND hwnd;                      // owner window
HBRUSH hbrush;                  // brush handle
static DWORD rgbCurrent;        // initial color selection

// Initialize CHOOSECOLOR 
ZeroMemory(&cc, sizeof(cc));
cc.lStructSize = sizeof(cc);
cc.hwndOwner = hwnd;
cc.lpCustColors = (LPDWORD) acrCustClr;
cc.rgbResult = rgbCurrent;
cc.Flags = CC_FULLOPEN | CC_RGBINIT;
 
if (ChooseColor(&cc)==TRUE) 
{
    hbrush = CreateSolidBrush(cc.rgbResult);
    rgbCurrent = cc.rgbResult; 
}
```



## <a name="choosing-a-font"></a><span data-ttu-id="fb6b5-125">Escolhendo uma fonte</span><span class="sxs-lookup"><span data-stu-id="fb6b5-125">Choosing a Font</span></span>

<span data-ttu-id="fb6b5-126">Este tópico descreve o código de exemplo que exibe uma caixa de diálogo de **fonte** para que um usuário possa escolher os atributos de uma fonte.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-126">This topic describes sample code that displays a **Font** dialog box so that a user can choose the attributes of a font.</span></span> <span data-ttu-id="fb6b5-127">O código de exemplo primeiro Inicializa uma estrutura [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) e, em seguida, chama a função [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) para exibir a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-127">The sample code first initializes a [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure, and then calls the [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) function to display the dialog box.</span></span>

<span data-ttu-id="fb6b5-128">Este exemplo define o **sinalizador \_ SCREENFONTS do CF** para especificar que a caixa de diálogo deve exibir apenas as fontes da tela.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-128">This example sets the **CF\_SCREENFONTS** flag to specify that the dialog box should display only screen fonts.</span></span> <span data-ttu-id="fb6b5-129">Ele define o sinalizador de **\_ efeitos do CF** para exibir os controles que permitem ao usuário selecionar as opções de riscar, sublinhado e cor.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-129">It sets the **CF\_EFFECTS** flag to display controls that allow the user to select strikeout, underline, and color options.</span></span>

<span data-ttu-id="fb6b5-130">Se [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) retornar **true**, indicando que o usuário clicou no botão **OK** , a estrutura [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) contém informações que descrevem os atributos Font e Font selecionados pelo usuário, incluindo os membros da estrutura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) apontados pelo membro **lpLogFont** .</span><span class="sxs-lookup"><span data-stu-id="fb6b5-130">If [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) returns **TRUE**, indicating that the user clicked the **OK** button, the [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure contains information that describes the font and font attributes selected by the user, including the members of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure pointed to by the **lpLogFont** member.</span></span> <span data-ttu-id="fb6b5-131">O membro **rgbColors** contém a cor de texto selecionada.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-131">The **rgbColors** member contains the selected text color.</span></span> <span data-ttu-id="fb6b5-132">O código de exemplo usa essas informações para definir a fonte e a cor do texto para o contexto do dispositivo associado à janela do proprietário.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-132">The sample code uses this information to set the font and text color for the device context associated with the owner window.</span></span>


```
HWND hwnd;                // owner window
HDC hdc;                  // display device context of owner window

CHOOSEFONT cf;            // common dialog box structure
static LOGFONT lf;        // logical font structure
static DWORD rgbCurrent;  // current text color
HFONT hfont, hfontPrev;
DWORD rgbPrev;

// Initialize CHOOSEFONT
ZeroMemory(&cf, sizeof(cf));
cf.lStructSize = sizeof (cf);
cf.hwndOwner = hwnd;
cf.lpLogFont = &lf;
cf.rgbColors = rgbCurrent;
cf.Flags = CF_SCREENFONTS | CF_EFFECTS;

if (ChooseFont(&cf)==TRUE)
{
    hfont = CreateFontIndirect(cf.lpLogFont);
    hfontPrev = SelectObject(hdc, hfont);
    rgbCurrent= cf.rgbColors;
    rgbPrev = SetTextColor(hdc, rgbCurrent);
 .
 .
 .
}
```



## <a name="opening-a-file"></a><span data-ttu-id="fb6b5-133">Abrindo um arquivo</span><span class="sxs-lookup"><span data-stu-id="fb6b5-133">Opening a File</span></span>

> [!Note]  
> <span data-ttu-id="fb6b5-134">A partir do Windows Vista, a caixa de diálogo Common File foi substituída pela caixa de diálogo de item comum quando usada para abrir um arquivo.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-134">Starting with Windows Vista, the Common File Dialog has been superseded by the Common Item Dialog when used to open a file.</span></span> <span data-ttu-id="fb6b5-135">Recomendamos que você use a API de caixa de diálogo de item comum em vez da API de caixa de diálogo de arquivo comum.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-135">We recommend that you use the Common Item Dialog API instead of the Common File Dialog API.</span></span> <span data-ttu-id="fb6b5-136">Para obter mais informações, consulte [caixa de diálogo de item comum](/windows/win32/shell/common-file-dialog).</span><span class="sxs-lookup"><span data-stu-id="fb6b5-136">For more information, see [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span>

 

<span data-ttu-id="fb6b5-137">Este tópico descreve o código de exemplo que exibe uma caixa de diálogo **aberta** para que um usuário possa especificar a unidade, o diretório e o nome de um arquivo a ser aberto.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-137">This topic describes sample code that displays an **Open** dialog box so that a user can specify the drive, directory, and name of a file to open.</span></span> <span data-ttu-id="fb6b5-138">O código de exemplo primeiro Inicializa uma estrutura [**da OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) e, em seguida, chama a função [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) para exibir a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-138">The sample code first initializes an [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure, and then calls the [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) function to display the dialog box.</span></span>

<span data-ttu-id="fb6b5-139">Neste exemplo, o membro **lpstrFilter** é um ponteiro para um buffer que especifica dois filtros de nome de arquivo que o usuário pode selecionar para limitar os nomes de arquivo que são exibidos.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-139">In this example, the **lpstrFilter** member is a pointer to a buffer that specifies two file name filters that the user can select to limit the file names that are displayed.</span></span> <span data-ttu-id="fb6b5-140">O buffer contém uma matriz de terminação de nulo duplo de cadeias de caracteres em que cada par de cadeias de caracteres especifica um filtro.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-140">The buffer contains a double-null terminated array of strings in which each pair of strings specifies a filter.</span></span> <span data-ttu-id="fb6b5-141">O membro **nFilterIndex** especifica que o primeiro padrão é usado quando a caixa de diálogo é criada.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-141">The **nFilterIndex** member specifies that the first pattern is used when the dialog box is created.</span></span>

<span data-ttu-id="fb6b5-142">Este exemplo define os sinalizadores **OFN \_ PATHMUSTEXIST** e **OFN \_ FILEMUSTEXIST** no membro **flags** .</span><span class="sxs-lookup"><span data-stu-id="fb6b5-142">This example sets the **OFN\_PATHMUSTEXIST** and **OFN\_FILEMUSTEXIST** flags in the **Flags** member.</span></span> <span data-ttu-id="fb6b5-143">Esses sinalizadores fazem com que a caixa de diálogo Verifique, antes de retornar, que o caminho e o nome de arquivo especificados pelo usuário realmente existem.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-143">These flags cause the dialog box to verify, before returning, that the path and file name specified by the user actually exist.</span></span>

<span data-ttu-id="fb6b5-144">A função [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) retornará **true** se o usuário clicar no botão **OK** e o caminho e o nome do arquivo especificados existirem.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-144">The [**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) function returns **TRUE** if the user clicks the **OK** button and the specified path and file name exist.</span></span> <span data-ttu-id="fb6b5-145">Nesse caso, o buffer apontado pelo membro **lpstrFile** contém o caminho e o nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-145">In this case, the buffer pointed to by the **lpstrFile** member contains the path and file name.</span></span> <span data-ttu-id="fb6b5-146">O código de exemplo usa essas informações em uma chamada para a função para abrir o arquivo.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-146">The sample code uses this information in a call to the function to open the file.</span></span>

<span data-ttu-id="fb6b5-147">Embora este exemplo não defina o sinalizador **OFN \_ Explorer** , ele ainda exibirá a caixa de diálogo padrão **Open** Explorer-Style.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-147">Although this example does not set the **OFN\_EXPLORER** flag, it still displays the default Explorer-style **Open** dialog box.</span></span> <span data-ttu-id="fb6b5-148">No entanto, se você quiser fornecer um procedimento de gancho ou um modelo personalizado e desejar a interface do usuário do Explorer, deverá definir o sinalizador do **OFN \_ Explorer** .</span><span class="sxs-lookup"><span data-stu-id="fb6b5-148">However, if you want to provide a hook procedure or a custom template and you want the Explorer user interface, you must set the **OFN\_EXPLORER** flag.</span></span>

> [!Note]  
> <span data-ttu-id="fb6b5-149">Na linguagem de programação C, uma cadeia de caracteres entre aspas é terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-149">In the C programming language, a string enclosed in quotation marks is null-terminated.</span></span>

 


```
OPENFILENAME ofn;       // common dialog box structure
char szFile[260];       // buffer for file name
HWND hwnd;              // owner window
HANDLE hf;              // file handle

// Initialize OPENFILENAME
ZeroMemory(&ofn, sizeof(ofn));
ofn.lStructSize = sizeof(ofn);
ofn.hwndOwner = hwnd;
ofn.lpstrFile = szFile;
// Set lpstrFile[0] to '\0' so that GetOpenFileName does not 
// use the contents of szFile to initialize itself.
ofn.lpstrFile[0] = '\0';
ofn.nMaxFile = sizeof(szFile);
ofn.lpstrFilter = "All\0*.*\0Text\0*.TXT\0";
ofn.nFilterIndex = 1;
ofn.lpstrFileTitle = NULL;
ofn.nMaxFileTitle = 0;
ofn.lpstrInitialDir = NULL;
ofn.Flags = OFN_PATHMUSTEXIST | OFN_FILEMUSTEXIST;

// Display the Open dialog box. 

if (GetOpenFileName(&ofn)==TRUE) 
    hf = CreateFile(ofn.lpstrFile, 
                    GENERIC_READ,
                    0,
                    (LPSECURITY_ATTRIBUTES) NULL,
                    OPEN_EXISTING,
                    FILE_ATTRIBUTE_NORMAL,
                    (HANDLE) NULL);
```



## <a name="displaying-the-print-dialog-box"></a><span data-ttu-id="fb6b5-150">Exibindo a caixa de diálogo Imprimir</span><span class="sxs-lookup"><span data-stu-id="fb6b5-150">Displaying the Print Dialog Box</span></span>

<span data-ttu-id="fb6b5-151">Este tópico descreve o código de exemplo que exibe uma caixa de diálogo de **impressão** para que um usuário possa selecionar opções para imprimir um documento.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-151">This topic describes sample code that displays a **Print** dialog box so that a user can select options for printing a document.</span></span> <span data-ttu-id="fb6b5-152">O código de exemplo primeiro Inicializa uma estrutura [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) e, em seguida, chama a função [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) para exibir a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-152">The sample code first initializes a [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure, and then calls the [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) function to display the dialog box.</span></span>

<span data-ttu-id="fb6b5-153">Este exemplo define o sinalizador **PD \_ RETURNDC** no membro **flags** da estrutura [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) .</span><span class="sxs-lookup"><span data-stu-id="fb6b5-153">This example sets the **PD\_RETURNDC** flag in the **Flags** member of the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure.</span></span> <span data-ttu-id="fb6b5-154">Isso faz com que o [**PRINTDLG**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) retorne um identificador de contexto de dispositivo para a impressora selecionada no membro **HDC** .</span><span class="sxs-lookup"><span data-stu-id="fb6b5-154">This causes [**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) to return a device context handle to the selected printer in the **hDC** member.</span></span> <span data-ttu-id="fb6b5-155">Você pode usar o identificador para renderizar a saída na impressora.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-155">You can use the handle to render output on the printer.</span></span>

<span data-ttu-id="fb6b5-156">Na entrada, o código de exemplo define os membros **hDevMode** e **hDevNames** como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-156">On input, the sample code sets the **hDevMode** and **hDevNames** members to **NULL**.</span></span> <span data-ttu-id="fb6b5-157">Se a função retornar **true**, esses membros retornarão identificadores para estruturas [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) que contêm a entrada do usuário e informações sobre a impressora.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-157">If the function returns **TRUE**, these members return handles to [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) structures that contain the user input and information about the printer.</span></span> <span data-ttu-id="fb6b5-158">Você pode usar essas informações para preparar a saída a ser enviada para a impressora selecionada.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-158">You can use this information to prepare the output to be sent to the selected printer.</span></span>


```
PRINTDLG pd;
HWND hwnd;

// Initialize PRINTDLG
ZeroMemory(&pd, sizeof(pd));
pd.lStructSize = sizeof(pd);
pd.hwndOwner   = hwnd;
pd.hDevMode    = NULL;     // Don't forget to free or store hDevMode.
pd.hDevNames   = NULL;     // Don't forget to free or store hDevNames.
pd.Flags       = PD_USEDEVMODECOPIESANDCOLLATE | PD_RETURNDC; 
pd.nCopies     = 1;
pd.nFromPage   = 0xFFFF; 
pd.nToPage     = 0xFFFF; 
pd.nMinPage    = 1; 
pd.nMaxPage    = 0xFFFF; 

if (PrintDlg(&pd)==TRUE) 
{
    // GDI calls to render output. 

    // Delete DC when done.
    DeleteDC(pd.hDC);
}
```



## <a name="using-the-print-property-sheet"></a><span data-ttu-id="fb6b5-159">Usando a folha de propriedades Imprimir</span><span class="sxs-lookup"><span data-stu-id="fb6b5-159">Using the Print Property Sheet</span></span>

<span data-ttu-id="fb6b5-160">Este tópico descreve o código de exemplo que exibe uma folha de propriedades de **impressão** para que um usuário possa selecionar opções para imprimir um documento.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-160">This topic describes sample code that displays a **Print** property sheet so that a user can select options for printing a document.</span></span> <span data-ttu-id="fb6b5-161">O código de exemplo primeiro Inicializa uma estrutura [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) e, em seguida, chama a função [**PRINTDLGEX**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) para exibir a folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-161">The sample code first initializes a [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) structure, then calls the [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) function to display the property sheet.</span></span>

<span data-ttu-id="fb6b5-162">O código de exemplo define o sinalizador **PD \_ RETURNDC** no membro **flags** da estrutura [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) .</span><span class="sxs-lookup"><span data-stu-id="fb6b5-162">The sample code sets the **PD\_RETURNDC** flag in the **Flags** member of the [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) structure.</span></span> <span data-ttu-id="fb6b5-163">Isso faz com que a função [**PRINTDLGEX**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) retorne um identificador de contexto de dispositivo para a impressora selecionada no membro **HDC** .</span><span class="sxs-lookup"><span data-stu-id="fb6b5-163">This causes the [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) function to return a device context handle to the selected printer in the **hDC** member.</span></span>

<span data-ttu-id="fb6b5-164">Na entrada, o código de exemplo define os membros **hDevMode** e **hDevNames** como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-164">On input, the sample code sets the **hDevMode** and **hDevNames** members to **NULL**.</span></span> <span data-ttu-id="fb6b5-165">Se a função retornar **S \_ OK**, esses membros retornarão identificadores para estruturas [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) que contêm a entrada do usuário e informações sobre a impressora.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-165">If the function returns **S\_OK**, these members return handles to [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) structures containing the user input and information about the printer.</span></span> <span data-ttu-id="fb6b5-166">Você pode usar essas informações para preparar a saída a ser enviada para a impressora selecionada.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-166">You can use this information to prepare the output to be sent to the selected printer.</span></span>

<span data-ttu-id="fb6b5-167">Depois que a operação de impressão for concluída, o código de exemplo liberará os buffers [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea), [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames)e [**PRINTPAGERANGE**](/windows/win32/api/commdlg/ns-commdlg-printpagerange) e chamará a função [**DeleteDC**](/windows/desktop/api/wingdi/nf-wingdi-deletedc) para excluir o contexto do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-167">After the printing operation has been completed, the sample code frees the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea), [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames), and [**PRINTPAGERANGE**](/windows/win32/api/commdlg/ns-commdlg-printpagerange) buffers and calls the [**DeleteDC**](/windows/desktop/api/wingdi/nf-wingdi-deletedc) function to delete the device context.</span></span>


```
// hWnd is the window that owns the property sheet.
HRESULT DisplayPrintPropertySheet(HWND hWnd)
{
    HRESULT hResult;
    PRINTDLGEX pdx = {0};
    LPPRINTPAGERANGE pPageRanges = NULL;

    // Allocate an array of PRINTPAGERANGE structures.
    pPageRanges = (LPPRINTPAGERANGE) GlobalAlloc(GPTR, 10 * sizeof(PRINTPAGERANGE));
    if (!pPageRanges)
        return E_OUTOFMEMORY;

    //  Initialize the PRINTDLGEX structure.
    pdx.lStructSize = sizeof(PRINTDLGEX);
    pdx.hwndOwner = hWnd;
    pdx.hDevMode = NULL;
    pdx.hDevNames = NULL;
    pdx.hDC = NULL;
    pdx.Flags = PD_RETURNDC | PD_COLLATE;
    pdx.Flags2 = 0;
    pdx.ExclusionFlags = 0;
    pdx.nPageRanges = 0;
    pdx.nMaxPageRanges = 10;
    pdx.lpPageRanges = pPageRanges;
    pdx.nMinPage = 1;
    pdx.nMaxPage = 1000;
    pdx.nCopies = 1;
    pdx.hInstance = 0;
    pdx.lpPrintTemplateName = NULL;
    pdx.lpCallback = NULL;
    pdx.nPropertyPages = 0;
    pdx.lphPropertyPages = NULL;
    pdx.nStartPage = START_PAGE_GENERAL;
    pdx.dwResultAction = 0;
    
    //  Invoke the Print property sheet.
    
    hResult = PrintDlgEx(&pdx);

    if ((hResult == S_OK) && pdx.dwResultAction == PD_RESULT_PRINT) 
    {
        // User clicked the Print button, so use the DC and other information returned in the 
        // PRINTDLGEX structure to print the document.
    }

    if (pdx.hDevMode != NULL) 
        GlobalFree(pdx.hDevMode); 
    if (pdx.hDevNames != NULL) 
        GlobalFree(pdx.hDevNames); 
    if (pdx.lpPageRanges != NULL)
        GlobalFree(pPageRanges);

    if (pdx.hDC != NULL) 
        DeleteDC(pdx.hDC);

    return hResult;
}
```



## <a name="setting-up-the-printed-page"></a><span data-ttu-id="fb6b5-168">Configurando a página impressa</span><span class="sxs-lookup"><span data-stu-id="fb6b5-168">Setting Up the Printed Page</span></span>

<span data-ttu-id="fb6b5-169">Este tópico descreve o código de exemplo que exibe uma caixa de diálogo de **configuração de página** para que um usuário possa selecionar os atributos da página impressa, como o tipo de papel, fonte de papel, orientação da página e margens da página.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-169">This topic describes sample code that displays a **Page Setup** dialog box so that a user can select the attributes of the printed page, such as the paper type, paper source, page orientation, and page margins.</span></span> <span data-ttu-id="fb6b5-170">O código de exemplo primeiro Inicializa uma estrutura [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) e, em seguida, chama a função [**PAGESETUPDLG**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) para exibir a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-170">The sample code first initializes a [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) structure, and then calls the [**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) function to display the dialog box.</span></span>

<span data-ttu-id="fb6b5-171">Este exemplo define o sinalizador de **\_ margens do PSD** no membro **flags** e usa o membro **rtMargin** para especificar os valores da margem inicial.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-171">This example sets the **PSD\_MARGINS** flag in the **Flags** member and uses the **rtMargin** member to specify the initial margin values.</span></span> <span data-ttu-id="fb6b5-172">Ele define o **sinalizador \_ INTHOUSANDTHSOFINCHES do PSD** para garantir que a caixa de diálogo expresse as dimensões da margem em milésimos de uma polegada.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-172">It sets the **PSD\_INTHOUSANDTHSOFINCHES** flag to ensure that the dialog box expresses margin dimensions in thousandths of an inch.</span></span>

<span data-ttu-id="fb6b5-173">Na entrada, o código de exemplo define os membros **hDevMode** e **hDevNames** como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-173">On input, the sample code sets the **hDevMode** and **hDevNames** members to **NULL**.</span></span> <span data-ttu-id="fb6b5-174">Se a função retornar **true**, a função usará esses membros para retornar identificadores para estruturas [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) que contêm a entrada do usuário e informações sobre a impressora.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-174">If the function returns **TRUE**, the function uses these members to return handles to [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) structures containing the user input and information about the printer.</span></span> <span data-ttu-id="fb6b5-175">Você pode usar essas informações para preparar a saída a ser enviada para a impressora selecionada.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-175">You can use this information to prepare the output to be sent to the selected printer.</span></span>

<span data-ttu-id="fb6b5-176">O exemplo a seguir também habilita um procedimento de gancho [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) para personalizar o desenho do conteúdo da página de exemplo.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-176">The following example also enables a [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure to customize drawing the contents of the sample page.</span></span>


```
PAGESETUPDLG psd;    // common dialog box structure
HWND hwnd;           // owner window

// Initialize PAGESETUPDLG
ZeroMemory(&psd, sizeof(psd));
psd.lStructSize = sizeof(psd);
psd.hwndOwner   = hwnd;
psd.hDevMode    = NULL; // Don't forget to free or store hDevMode.
psd.hDevNames   = NULL; // Don't forget to free or store hDevNames.
psd.Flags       = PSD_INTHOUSANDTHSOFINCHES | PSD_MARGINS | 
                  PSD_ENABLEPAGEPAINTHOOK; 
psd.rtMargin.top = 1000;
psd.rtMargin.left = 1250;
psd.rtMargin.right = 1250;
psd.rtMargin.bottom = 1000;
psd.lpfnPagePaintHook = PaintHook;

if (PageSetupDlg(&psd)==TRUE)
{
    // check paper size and margin values here.
}
```



<span data-ttu-id="fb6b5-177">O exemplo a seguir mostra um exemplo de procedimento de gancho [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) que desenha o retângulo de margem na área da página de exemplo:</span><span class="sxs-lookup"><span data-stu-id="fb6b5-177">The following example shows a sample [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) hook procedure that draws the margin rectangle in the sample page area:</span></span>


```
BOOL CALLBACK PaintHook(HWND hwndDlg, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    LPRECT lprc; 
    COLORREF crMargRect; 
    HDC hdc, hdcOld; 
 
    switch (uMsg) 
    { 
        // Draw the margin rectangle. 
        case WM_PSD_MARGINRECT: 
            hdc = (HDC) wParam; 
            lprc = (LPRECT) lParam; 
 
            // Get the system highlight color. 
            crMargRect = GetSysColor(COLOR_HIGHLIGHT); 
 
            // Create a dash-dot pen of the system highlight color and 
            // select it into the DC of the sample page. 
            hdcOld = SelectObject(hdc, CreatePen(PS_DASHDOT, .5, crMargRect)); 
 
            // Draw the margin rectangle. 
            Rectangle(hdc, lprc->left, lprc->top, lprc->right, lprc->bottom); 
 
            // Restore the previous pen to the DC. 
            SelectObject(hdc, hdcOld); 
            return TRUE; 
 
        default: 
            return FALSE; 
    } 
    return TRUE; 
}
```



## <a name="finding-text"></a><span data-ttu-id="fb6b5-178">Localizando texto</span><span class="sxs-lookup"><span data-stu-id="fb6b5-178">Finding Text</span></span>

<span data-ttu-id="fb6b5-179">Este tópico descreve o código de exemplo que exibe e gerencia uma caixa de diálogo **Localizar** para que o usuário possa especificar os parâmetros de uma operação de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-179">This topic describes sample code that displays and manages a **Find** dialog box so that the user can specify the parameters of a search operation.</span></span> <span data-ttu-id="fb6b5-180">A caixa de diálogo envia mensagens para o procedimento de janela para que você possa executar a operação de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-180">The dialog box sends messages to the window procedure so you can perform the search operation.</span></span>

<span data-ttu-id="fb6b5-181">O código para exibir e gerenciar uma caixa de diálogo de **substituição** é semelhante, exceto pelo fato de que ela usa a função [**ReplaceText**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) para exibir a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-181">The code for displaying and managing a **Replace** dialog box is similar, except that it uses the [**ReplaceText**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) function to display the dialog box.</span></span> <span data-ttu-id="fb6b5-182">A caixa de diálogo **substituir** também envia mensagens em resposta aos cliques do usuário nos botões **substituir** e **substituir tudo** .</span><span class="sxs-lookup"><span data-stu-id="fb6b5-182">The **Replace** dialog box also sends messages in response to user clicks on the **Replace** and **Replace All** buttons.</span></span>

<span data-ttu-id="fb6b5-183">Para usar a caixa de diálogo **Localizar** ou **substituir** , você deve executar três tarefas separadas:</span><span class="sxs-lookup"><span data-stu-id="fb6b5-183">To use the **Find** or **Replace** dialog box, you must perform three separate tasks:</span></span>

1.  <span data-ttu-id="fb6b5-184">Obtenha um identificador de mensagem para a mensagem registrada [**FINDMSGSTRING**](findmsgstring.md) .</span><span class="sxs-lookup"><span data-stu-id="fb6b5-184">Get a message identifier for the [**FINDMSGSTRING**](findmsgstring.md) registered message.</span></span>
2.  <span data-ttu-id="fb6b5-185">Exibir a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-185">Display the dialog box.</span></span>
3.  <span data-ttu-id="fb6b5-186">Processar mensagens [**FINDMSGSTRING**](findmsgstring.md) quando a caixa de diálogo estiver aberta.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-186">Process [**FINDMSGSTRING**](findmsgstring.md) messages when the dialog box is open.</span></span>

<span data-ttu-id="fb6b5-187">Ao inicializar o aplicativo, chame a função [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) para obter um identificador de mensagem para a mensagem registrada [**FINDMSGSTRING**](findmsgstring.md) .</span><span class="sxs-lookup"><span data-stu-id="fb6b5-187">When you initialize your application, call the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get a message identifier for the [**FINDMSGSTRING**](findmsgstring.md) registered message.</span></span>


```
UINT uFindReplaceMsg;  // message identifier for FINDMSGSTRING 

uFindReplaceMsg = RegisterWindowMessage(FINDMSGSTRING);
```



<span data-ttu-id="fb6b5-188">Para exibir uma caixa de diálogo **Localizar** , primeiro inicialize uma estrutura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) e, em seguida, chame a função [**FindText**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) .</span><span class="sxs-lookup"><span data-stu-id="fb6b5-188">To display a **Find** dialog box, first initialize a [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) structure and then call the [**FindText**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) function.</span></span> <span data-ttu-id="fb6b5-189">Observe que a estrutura **FINDREPLACE** e o buffer da cadeia de caracteres de pesquisa devem ser uma variável global ou estática para que ela não saia do escopo antes que a caixa de diálogo seja fechada.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-189">Note that the **FINDREPLACE** structure and the buffer for the search string should be a global or static variable so that it does not go out of scope before the dialog box closes.</span></span> <span data-ttu-id="fb6b5-190">Você deve definir o membro **hwndOwner** para especificar a janela que recebe as mensagens registradas.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-190">You must set the **hwndOwner** member to specify the window that receives the registered messages.</span></span> <span data-ttu-id="fb6b5-191">Depois de criar a caixa de diálogo, você pode movê-la ou manipulá-la usando o identificador retornado.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-191">After you create the dialog box, you can move or manipulate it by using the returned handle.</span></span>


```
FINDREPLACE fr;       // common dialog box structure
HWND hwnd;            // owner window
CHAR szFindWhat[80];  // buffer receiving string
HWND hdlg = NULL;     // handle to Find dialog box

// Initialize FINDREPLACE
ZeroMemory(&fr, sizeof(fr));
fr.lStructSize = sizeof(fr);
fr.hwndOwner = hwnd;
fr.lpstrFindWhat = szFindWhat;
fr.wFindWhatLen = 80;
fr.Flags = 0;

hdlg = FindText(&fr);
```



<span data-ttu-id="fb6b5-192">Quando a caixa de diálogo é aberta, o loop de mensagem principal deve incluir uma chamada para a função [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) .</span><span class="sxs-lookup"><span data-stu-id="fb6b5-192">When the dialog box is open, your main message loop must include a call to the [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) function.</span></span> <span data-ttu-id="fb6b5-193">Passe um identificador para a caixa de diálogo como um parâmetro na chamada **IsDialogMessage** .</span><span class="sxs-lookup"><span data-stu-id="fb6b5-193">Pass a handle to the dialog box as a parameter in the **IsDialogMessage** call.</span></span> <span data-ttu-id="fb6b5-194">Isso garante que a caixa de diálogo processe corretamente as mensagens do teclado.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-194">This ensures that the dialog box correctly processes keyboard messages.</span></span>

<span data-ttu-id="fb6b5-195">Para monitorar as mensagens enviadas da caixa de diálogo, o procedimento de janela deve verificar a mensagem registrada [**FINDMSGSTRING**](findmsgstring.md) e processar os valores passados na estrutura [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) como no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="fb6b5-195">To monitor messages sent from the dialog box, your window procedure must check for the [**FINDMSGSTRING**](findmsgstring.md) registered message and process the values passed in the [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) structure as in the following example.</span></span>


```
LPFINDREPLACE lpfr;

if (message == uFindReplaceMsg)
{ 
    // Get pointer to FINDREPLACE structure from lParam.
    lpfr = (LPFINDREPLACE)lParam;

    // If the FR_DIALOGTERM flag is set, 
    // invalidate the handle that identifies the dialog box. 
    if (lpfr->Flags & FR_DIALOGTERM)
    { 
        hdlg = NULL; 
        return 0; 
    } 

    // If the FR_FINDNEXT flag is set, 
    // call the application-defined search routine
    // to search for the requested string. 
    if (lpfr->Flags & FR_FINDNEXT) 
    {
        SearchFile(lpfr->lpstrFindWhat,
                   (BOOL) (lpfr->Flags & FR_DOWN), 
                   (BOOL) (lpfr->Flags & FR_MATCHCASE)); 
    }

    return 0; 
}
```



 

 
