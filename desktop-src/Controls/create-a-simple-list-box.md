---
title: Como criar uma caixa de listagem simples
description: Este tópico demonstra como inicializar e recuperar itens de uma caixa de listagem simples.
ms.assetid: 4A717010-A1D3-4FFB-8E4E-D5C4F9D8D952
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ca2230b265d61e9a59a8892e14127d25bf2cfd2
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104008609"
---
# <a name="how-to-create-a-simple-list-box"></a>Como criar uma caixa de listagem simples

Este tópico demonstra como inicializar e recuperar itens de uma caixa de listagem simples.

O exemplo de código C++ neste tópico inclui um procedimento de caixa de diálogo que preenche uma caixa de listagem com informações sobre os jogadores em uma equipe esportiva. Quando o usuário seleciona o nome de um player na lista, as informações sobre o Player são exibidas na caixa de diálogo. O estilo de janela da caixa de listagem inclui [**lbs \_ Sort**](list-box-styles.md), o que resulta em uma lista classificada de itens. A captura de tela a seguir mostra a caixa de diálogo.

![captura de tela de uma caixa de diálogo contendo uma caixa de listagem rotulada, texto sobre o item da caixa de listagem selecionado e um botão OK](images/lb-roster.png)

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções


O aplicativo deve executar as seguintes tarefas relacionadas à caixa de listagem:

-   Inicializar a caixa de listagem
-   Recuperar a seleção do usuário na caixa de listagem

No exemplo de código C++ a seguir, as informações sobre os jogadores são armazenadas em uma matriz de estruturas. Durante a inicialização, o procedimento da caixa de diálogo usa a mensagem de [**\_ AddString do lb**](lb-addstring.md) para adicionar os nomes dos membros da equipe à caixa de listagem (**exemplo de \_ ListBox \_ da IDC**) um de cada vez. Ele também usa a [**mensagem \_ SETITEMDATA de lb**](lb-setitemdata.md) para adicionar o índice de matriz do Player à caixa de listagem como dados de item. Posteriormente, quando o usuário seleciona um player na caixa de listagem, o procedimento da caixa de diálogo usa a mensagem [**\_ GETITEMDATA de lb**](lb-getitemdata.md) para recuperar o índice de matriz correspondente. Em seguida, ele usa o índice de matriz para recuperar informações do Player da matriz.



```C++
typedef struct 
{ 
    TCHAR achName[MAX_PATH]; 
    TCHAR achPosition[12]; 
    int nGamesPlayed; 
    int nGoalsScored; 
} Player; 

Player Roster[] = 
{ 
    {TEXT("Haas, Jonathan"), TEXT("Midfield"), 18, 4 }, 
    {TEXT("Pai, Jyothi"), TEXT("Forward"), 36, 12 }, 
    {TEXT("Hanif, Kerim"), TEXT("Back"), 26, 0 }, 
    {TEXT("Anderberg, Michael"), TEXT("Back"), 24, 2 }, 
    {TEXT("Jelitto, Jacek"), TEXT("Midfield"), 26, 3 }, 
    {TEXT("Raposo, Rui"), TEXT("Back"), 24, 3}, 
    {TEXT("Joseph, Brad"), TEXT("Forward"), 13, 3 }, 
    {TEXT("Bouchard, Thomas"), TEXT("Forward"), 28, 5 }, 
    {TEXT("Salmre, Ivo "), TEXT("Midfield"), 27, 7 }, 
    {TEXT("Camp, David"), TEXT("Midfield"), 22, 3 }, 
    {TEXT("Kohl, Franz"), TEXT("Goalkeeper"), 17, 0 }, 
}; 


INT_PTR CALLBACK ListBoxExampleProc(HWND hDlg, UINT message, 
        WPARAM wParam, LPARAM lParam)
{
    switch (message)
    {
    case WM_INITDIALOG:
        {
            // Add items to list. 
            HWND hwndList = GetDlgItem(hDlg, IDC_LISTBOX_EXAMPLE);  
            for (int i = 0; i < ARRAYSIZE(Roster); i++) 
            { 
                int pos = (int)SendMessage(hwndList, LB_ADDSTRING, 0, 
                    (LPARAM) Roster[i].achName); 
                // Set the array index of the player as item data.
                // This enables us to retrieve the item from the array
                // even after the items are sorted by the list box.
                SendMessage(hwndList, LB_SETITEMDATA, pos, (LPARAM) i); 
            } 
            // Set input focus to the list box.
            SetFocus(hwndList); 
            return TRUE;               
        } 

    case WM_COMMAND:
        switch (LOWORD(wParam))
        {
        case IDOK:
        case IDCANCEL:
            EndDialog(hDlg, LOWORD(wParam));
            return TRUE;

        case IDC_LISTBOX_EXAMPLE:
            {
                switch (HIWORD(wParam)) 
                { 
                case LBN_SELCHANGE:
                    {
                        HWND hwndList = GetDlgItem(hDlg, IDC_LISTBOX_EXAMPLE); 

                        // Get selected index.
                        int lbItem = (int)SendMessage(hwndList, LB_GETCURSEL, 0, 0); 

                        // Get item data.
                        int i = (int)SendMessage(hwndList, LB_GETITEMDATA, lbItem, 0);

                        // Do something with the data from Roster[i]
                        TCHAR buff[MAX_PATH];
                        StringCbPrintf (buff, ARRAYSIZE(buff),  
                            TEXT("Position: %s\nGames played: %d\nGoals: %d"), 
                            Roster[i].achPosition, Roster[i].nGamesPlayed, 
                            Roster[i].nGoalsScored);

                        SetDlgItemText(hDlg, IDC_STATISTICS, buff); 
                        return TRUE; 
                    } 
                }
            }
            return TRUE;
        }
    }
    return FALSE;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de controle de caixa de listagem](bumper-list-box-list-box-control-reference.md)
</dt> <dt>

[Sobre as caixas de listagem](about-list-boxes.md)
</dt> <dt>

[Usando caixas de listagem](using-list-boxes.md)
</dt> </dl>

 

 




