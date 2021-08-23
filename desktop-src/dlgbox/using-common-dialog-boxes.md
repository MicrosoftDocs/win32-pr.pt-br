---
title: Usando caixas de diálogo comuns
description: Esta seção aborda tarefas que invocam caixas de diálogo comuns.
ms.assetid: ba038bc1-fb5c-4576-be80-7eae7339ba05
keywords:
- Biblioteca de caixas de diálogo comuns, tarefas
- caixas de diálogo comuns, usando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5da09fcc99cdde617c3fbdaf34e4465d9a768b0073c5dbd6d461a19060ca92bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985296"
---
# <a name="using-common-dialog-boxes"></a>Usando caixas de diálogo comuns

Esta seção aborda tarefas que invocam caixas de diálogo comuns:

-   [Escolhendo uma cor](#choosing-a-color)
-   [Escolhendo uma fonte](#choosing-a-font)
-   [Abrindo um arquivo](#opening-a-file)
-   [Exibindo a caixa de diálogo Imprimir](#displaying-the-print-dialog-box)
-   [Usando a folha de propriedades de impressão](#using-the-print-property-sheet)
-   [Configurando a página impressa](#setting-up-the-printed-page)
-   [Localizar texto](#finding-text)

## <a name="choosing-a-color"></a>Escolhendo uma cor

Este tópico descreve o código de exemplo que exibe uma caixa **de** diálogo Cor para que um usuário possa selecionar uma cor. O código de exemplo primeiro inicializa uma [**estrutura CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) e, em seguida, chama a [**função ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) para exibir a caixa de diálogo. Se a função retornar **TRUE**, indicando que o usuário selecionou uma cor, o código de exemplo usará a cor selecionada para criar um pincel sólido.

Este exemplo usa a [**estrutura CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) para inicializar a caixa de diálogo da seguinte forma:

-   Inicializa o membro **lpCustColors** com um ponteiro para uma matriz estática de valores. As cores na matriz são inicialmente pretas, mas a matriz estática preserva as cores personalizadas criadas pelo usuário para chamadas [**ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85)) subsequentes.
-   Define o **sinalizador CC \_ RGBINIT** e inicializa o membro **rgbResult** para especificar a cor inicialmente selecionada quando a caixa de diálogo é aberta. Se não for especificado, a seleção inicial será preta. O exemplo usa a *variável estática rgbCurrent* para preservar o valor selecionado entre chamadas para [**ChooseColor.**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85))
-   Define o **sinalizador CC \_ FULLOPEN** para que a extensão de cores personalizadas da caixa de diálogo seja sempre exibida.


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



## <a name="choosing-a-font"></a>Escolhendo uma fonte

Este tópico descreve o código de exemplo que exibe **uma** caixa de diálogo Fonte para que um usuário possa escolher os atributos de uma fonte. O código de exemplo primeiro inicializa uma estrutura [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) e, em seguida, chama a [**função ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) para exibir a caixa de diálogo.

Este exemplo define o **sinalizador \_ SCREENFONTS do CF** para especificar que a caixa de diálogo deve exibir apenas fontes de tela. Ele define o **sinalizador \_ EFEITOS DO CF** para exibir controles que permitem ao usuário selecionar opções de cores, sublinhados e de destaque.

Se [**ChooseFont**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) retornar **TRUE**, indicando que o usuário clicou no botão **OK,** a estrutura [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) conterá informações que descrevem os atributos de fonte e fonte selecionados pelo usuário, incluindo os membros da estrutura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) apontada pelo membro **lpLogFont.** O **membro rgbColors** contém a cor do texto selecionada. O código de exemplo usa essas informações para definir a fonte e a cor do texto para o contexto do dispositivo associado à janela do proprietário.


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



## <a name="opening-a-file"></a>Abrindo um arquivo

> [!Note]  
> Começando com Windows Vista, a caixa de diálogo Arquivo Comum foi superada pela Caixa de Diálogo de Item Comum quando usada para abrir um arquivo. Recomendamos que você use a API de Caixa de Diálogo de Item Comum em vez da API de Caixa de Diálogo de Arquivo Comum. Para obter mais informações, consulte [Caixa de diálogo Item Comum](/windows/win32/shell/common-file-dialog).

 

Este tópico descreve o código  de exemplo que exibe uma caixa de diálogo Abrir para que um usuário possa especificar a unidade, o diretório e o nome de um arquivo a ser aberto. O código de exemplo primeiro inicializa uma estrutura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) e, em seguida, chama a [**função GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) para exibir a caixa de diálogo.

Neste exemplo, o membro **lpstrFilter** é um ponteiro para um buffer que especifica dois filtros de nome de arquivo que o usuário pode selecionar para limitar os nomes de arquivo exibidos. O buffer contém uma matriz terminada em nulo duplo de cadeias de caracteres na qual cada par de cadeias de caracteres especifica um filtro. O **membro nFilterIndex** especifica que o primeiro padrão é usado quando a caixa de diálogo é criada.

Este exemplo define os **sinalizadores OFN \_ PATHMUSTEXIST** e **OFN \_ FILEMUSTEXIST** no **membro Flags.** Esses sinalizadores faz com que a caixa de diálogo verifique, antes de retornar, se o caminho e o nome de arquivo especificados pelo usuário realmente existem.

A [**função GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea) retornará **TRUE** se o usuário clicar no **botão OK** e o caminho e o nome do arquivo especificados existirem. Nesse caso, o buffer apontado pelo membro **lpstrFile** contém o caminho e o nome do arquivo. O código de exemplo usa essas informações em uma chamada para a função para abrir o arquivo.

Embora este exemplo não de definir o sinalizador **OFN \_ EXPLORER,** ele ainda exibe a caixa de diálogo Abrir no estilo **Explorer** padrão. No entanto, se você quiser fornecer um procedimento de gancho ou um modelo personalizado e quiser a interface do usuário do Explorer, deverá definir o **sinalizador OFN \_ EXPLORER.**

> [!Note]  
> Na linguagem de programação C, uma cadeia de caracteres entre aspas é terminada em nulo.

 


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



## <a name="displaying-the-print-dialog-box"></a>Exibindo a caixa de diálogo Imprimir

Este tópico descreve o código de exemplo que exibe **uma** caixa de diálogo Imprimir para que um usuário possa selecionar opções para imprimir um documento. O código de exemplo primeiro inicializa uma estrutura [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga) e, em seguida, chama a [**função PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) para exibir a caixa de diálogo.

Este exemplo define o **sinalizador PD \_ RETURNDC** no **membro Flags** da [**estrutura PRINTDLG.**](/windows/win32/api/commdlg/ns-commdlg-printdlga) Isso faz [**com que PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85)) retorne um alça de contexto do dispositivo para a impressora selecionada no **membro hDC.** Você pode usar o alça para renderizar a saída na impressora.

Na entrada, o código de exemplo define os **membros hDevMode** e **hDevNames** como **NULL.** Se a função retornar **TRUE**, esses membros retornarão alças para estruturas [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) que contêm a entrada do usuário e informações sobre a impressora. Você pode usar essas informações para preparar a saída a ser enviada para a impressora selecionada.


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



## <a name="using-the-print-property-sheet"></a>Usando a folha de propriedades de impressão

Este tópico descreve o código de exemplo que exibe uma **folha** de propriedades Imprimir para que um usuário possa selecionar opções para imprimir um documento. O código de exemplo primeiro inicializa uma estrutura [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) e, em seguida, chama a [**função PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) para exibir a folha de propriedades.

O código de exemplo define **o sinalizador PD \_ RETURNDC** **no membro Flags** da [**estrutura PRINTDLG.**](/windows/win32/api/commdlg/ns-commdlg-printdlga) Isso faz com [**que a função PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) retorne um alça de contexto do dispositivo para a impressora selecionada no **membro hDC.**

Na entrada, o código de exemplo define os **membros hDevMode** e **hDevNames** como **NULL.** Se a função retornar **S \_ OK**, esses membros retornarão alças para estruturas [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) que contêm a entrada do usuário e informações sobre a impressora. Você pode usar essas informações para preparar a saída a ser enviada para a impressora selecionada.

Após a conclusão da operação de impressão, o código de exemplo libera os buffers [**DEVMODE,**](/windows/win32/api/wingdi/ns-wingdi-devmodea) [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames)e [**PRINTPAGERANGE**](/windows/win32/api/commdlg/ns-commdlg-printpagerange) e chama a [**função DeleteDC**](/windows/desktop/api/wingdi/nf-wingdi-deletedc) para excluir o contexto do dispositivo.


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



## <a name="setting-up-the-printed-page"></a>Configurando a página impressa

Este tópico descreve o código de exemplo que exibe uma caixa de diálogo Configuração de Página para que um usuário possa selecionar os atributos da página impressa, como o tipo de papel, a origem do papel, **a** orientação da página e as margens da página. O código de exemplo primeiro inicializa uma estrutura [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga) e, em seguida, chama a [**função PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85)) para exibir a caixa de diálogo.

Este exemplo define o **sinalizador PSD \_ MARGINS** no membro **Flags** e usa o membro **rtMargin** para especificar os valores de margem iniciais. Ele define o **sinalizador PSD \_ INTHOUSANDTHSOFINCHES** para garantir que a caixa de diálogo expresse dimensões de margem em milésimos de polegada.

Na entrada, o código de exemplo define os **membros hDevMode** e **hDevNames** como **NULL.** Se a função retornar **TRUE**, a função usará esses membros para retornar alças para estruturas [**DEVNAMES**](/windows/win32/api/commdlg/ns-commdlg-devnames) que contêm a entrada do usuário e informações sobre a impressora. Você pode usar essas informações para preparar a saída a ser enviada para a impressora selecionada.

O exemplo a seguir também permite que um procedimento de gancho [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) personalize o desenho do conteúdo da página de exemplo.


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



O exemplo a seguir mostra um procedimento de gancho [**PagePaintHook**](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook) de exemplo que desenha o retângulo de margem na área da página de exemplo:


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



## <a name="finding-text"></a>Localizar texto

Este tópico descreve o código de exemplo  que exibe e gerencia uma caixa de diálogo Encontrar para que o usuário possa especificar os parâmetros de uma operação de pesquisa. A caixa de diálogo envia mensagens para o procedimento de janela para que você possa executar a operação de pesquisa.

O código para exibir e gerenciar **uma** caixa de diálogo Substituir é semelhante, exceto que ele usa a [**função ReplaceText**](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta) para exibir a caixa de diálogo. A **caixa de** diálogo Substituir também envia mensagens em resposta aos cliques do usuário **nos** botões Substituir e Substituir **Tudo.**

Para usar a **caixa de** diálogo Encontrar **ou** Substituir, você deve executar três tarefas separadas:

1.  Obter um identificador de mensagem para a [**mensagem registrada FINDMSGSTRING.**](findmsgstring.md)
2.  Exibir a caixa de diálogo.
3.  Processe [**mensagens FINDMSGSTRING**](findmsgstring.md) quando a caixa de diálogo estiver aberta.

Ao inicializar seu aplicativo, chame a [**função RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) para obter um identificador de mensagem para a [**mensagem registrada FINDMSGSTRING.**](findmsgstring.md)


```
UINT uFindReplaceMsg;  // message identifier for FINDMSGSTRING 

uFindReplaceMsg = RegisterWindowMessage(FINDMSGSTRING);
```



Para exibir uma **caixa de** diálogo Encontrar, primeiro inicialize uma [**estrutura FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) e, em seguida, chame a [**função FindText.**](/windows/desktop/api/Commdlg/nf-commdlg-findtexta) Observe que a **estrutura FINDREPLACE** e o buffer para a cadeia de caracteres de pesquisa devem ser uma variável global ou estática para que ela não saia do escopo antes que a caixa de diálogo feche. Você deve definir o **membro hwndOwner** para especificar a janela que recebe as mensagens registradas. Depois de criar a caixa de diálogo, você pode movê-la ou manipulá-la usando o alça retornada.


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



Quando a caixa de diálogo estiver aberta, o loop de mensagem principal deverá incluir uma chamada para a [**função IsDialogMessage.**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) Passe um alça para a caixa de diálogo como um parâmetro na **chamada IsDialogMessage.** Isso garante que a caixa de diálogo processe corretamente as mensagens do teclado.

Para monitorar mensagens enviadas da caixa de diálogo, o procedimento de janela deve verificar a mensagem registrada [**FINDMSGSTRING**](findmsgstring.md) e processar os valores passados na estrutura [**FINDREPLACE,**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) como no exemplo a seguir.


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



 

 
