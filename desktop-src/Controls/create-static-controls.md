---
title: Como criar controles estáticos
description: O exemplo nesta seção demonstra como criar um controle estático animado.
ms.assetid: D2DA38CB-360C-49EC-90BC-9AFA88C4B751
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 217135a6590fcee60286d21f00233916c4eba967
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/17/2020
ms.locfileid: "104453893"
---
# <a name="how-to-create-static-controls"></a>Como criar controles estáticos

O exemplo nesta seção demonstra como criar um controle estático animado.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções

### <a name="create-a-static-control"></a>Criar um controle estático

O exemplo de código a seguir usa um temporizador e a mensagem do [**\_ ícone STM**](stm-seticon.md) para animar um controle de ícone estático em uma caixa de diálogo.


```C++
#define MAXICONS 3 
#define HALF_SECOND 500

INT_PTR CALLBACK StaticDlgProc(HWND hDlg, UINT message, WPARAM wParam, 
    LPARAM lParam) 
{ 
    static HICON aIcons[MAXICONS]; 
    static UINT i = 0; 
    static UINT idTimer = 1; 

    switch (message) 
    { 
        case WM_INITDIALOG: 

            // Load the icon resources. g_hInst is the global instance handle.
            aIcons[i]   = LoadIcon(g_hInst, MAKEINTRESOURCE(IDI_ICON1)); 
            aIcons[++i] = LoadIcon(g_hInst, MAKEINTRESOURCE(IDI_ICON2)); 
            aIcons[++i] = LoadIcon(g_hInst, MAKEINTRESOURCE(IDI_ICON3)); 
            
            // Reset the array index.
            i = 0;
 
            // Set a timer. 
            SetTimer(hDlg, idTimer, HALF_SECOND, (TIMERPROC) NULL); 
            return TRUE; 

        case WM_TIMER: 

            // Use STM_SETICON to associate a new icon with the static icon
            // control whenever a WM_TIMER message is received. 
            SendDlgItemMessage(hDlg, IDC_STATIC_ICON, STM_SETICON, 
                (WPARAM) aIcons[i], 0);                    

            // Reset the array index, if necessary.
            if (++i == MAXICONS)
                i = 0;

            return 0; 

        case WM_COMMAND: 
            if (wParam == IDOK 
                || wParam == IDCANCEL) 
            { 
                EndDialog(hDlg, TRUE); 
            } 
            return TRUE; 
 
        case WM_DESTROY: 
            KillTimer(hDlg, idTimer); 

            // Note that it is not necessary to call DestroyIcon here. LoadIcon
            // obtains a shared icon, which is valid as long as the module from 
            // which it was loaded is in memory. 
 
            return 0; 
    } 
    return FALSE; 

    UNREFERENCED_PARAMETER(lParam); 
} 
```



## <a name="remarks"></a>Comentários

O identificador do controle de ícone estático ( \_ ícone estático IDI \_ ) é definido em um arquivo de cabeçalho global e os ícones são carregados dos recursos do aplicativo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando controles estáticos](using-static-controls.md)
</dt> <dt>

[Demonstração de controles comuns do Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 




