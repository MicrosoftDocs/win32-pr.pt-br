---
title: Como criar um controle de edição de linha única
description: Este tópico demonstra como criar uma caixa de diálogo que contém um controle de edição de linha única.
ms.assetid: 742DF606-9998-46D0-8D0A-F79508AAFFC0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 597c3e611f53af56a42f837c4d85a43f97ff846e371314b130d72c568aaf860e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829107"
---
# <a name="how-to-create-a-single-line-edit-control"></a>Como criar um controle de edição de linha única

Este tópico demonstra como criar uma caixa de diálogo que contém um controle de edição de linha única.

O controle de edição de linha única tem o estilo de [**\_ senha es**](edit-control-styles.md) . Por padrão, os controles de edição com esse estilo exibem um asterisco para cada caractere que é digitado pelo usuário. No entanto, este exemplo usa a mensagem em [**\_ SetPasswordChar**](em-setpasswordchar.md) para alterar o caractere padrão de um asterisco para um sinal de adição (+). A captura de tela a seguir mostra a caixa de diálogo depois que o usuário insere uma senha.

![captura de tela de uma caixa de diálogo que contém um controle de edição para inserir uma senha](images/passworddlg.png)

> [!Note]  
> Comctl32.dll versão 6 não é redistribuível. Para usar Comctl32.dll versão 6, especifique-o em um manifesto. Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).

 

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Windows Programação de interface do usuário

## <a name="instructions"></a>Instruções

### <a name="step-1-create-an-instance-of-the-password-dialog-box"></a>Etapa 1: criar uma instância da caixa de diálogo de senha.

O exemplo de código C++ a seguir usa a função caixa para criar uma caixa de diálogo modal. A **\_ senha** do modelo de caixa de diálogo IDD é passada como um parâmetro. Ele define, entre outras coisas, os estilos de janela, os botões e as dimensões da caixa de diálogo senha.


```C++
DialogBox(hInst,                   // application instance
    MAKEINTRESOURCE(IDD_PASSWORD), // dialog box resource
    hWnd,                          // owner window
    PasswordProc                    // dialog box window procedure
    );
```



### <a name="step-2-initialize-the-dialog-box-and-process-user-input"></a>Etapa 2: inicializar a caixa de diálogo e processar a entrada do usuário.

O procedimento de janela no exemplo a seguir inicializa a caixa de diálogo de senha e processa as mensagens de notificação e a entrada do usuário.

Durante a inicialização, o procedimento de janela altera o caractere de senha padrão para um **+** sinal e define o botão de pressão padrão como **Cancelar**.

Durante o processamento de entrada do usuário, o procedimento de janela altera o botão de ação padrão de **Cancelar** para **OK** assim que o usuário digita o texto no controle de edição. Se o usuário pressionar o botão **OK** , o procedimento de janela usará as mensagens em [**\_ LINELENGTH**](em-linelength.md) e em [**\_ getline**](em-getline.md) para recuperar o texto.



```C++
INT_PTR CALLBACK PasswordProc(HWND hDlg, UINT message, WPARAM wParam, LPARAM lParam) 
{ 
    TCHAR lpszPassword[16]; 
    WORD cchPassword; 

    switch (message) 
    { 
        case WM_INITDIALOG: 
            // Set password character to a plus sign (+) 
            SendDlgItemMessage(hDlg, 
                               IDE_PASSWORDEDIT, 
                               EM_SETPASSWORDCHAR, 
                               (WPARAM) '+', 
                               (LPARAM) 0); 

            // Set the default push button to "Cancel." 
            SendMessage(hDlg, 
                        DM_SETDEFID, 
                        (WPARAM) IDCANCEL, 
                        (LPARAM) 0); 

            return TRUE; 

        case WM_COMMAND: 
            // Set the default push button to "OK" when the user enters text. 
            if(HIWORD (wParam) == EN_CHANGE && 
                                LOWORD(wParam) == IDE_PASSWORDEDIT) 
            {
                SendMessage(hDlg, 
                            DM_SETDEFID, 
                            (WPARAM) IDOK, 
                            (LPARAM) 0); 
            }
            switch(wParam) 
            { 
                case IDOK: 
                    // Get number of characters. 
                    cchPassword = (WORD) SendDlgItemMessage(hDlg, 
                                                            IDE_PASSWORDEDIT, 
                                                            EM_LINELENGTH, 
                                                            (WPARAM) 0, 
                                                            (LPARAM) 0); 
                    if (cchPassword >= 16) 
                    { 
                        MessageBox(hDlg, 
                                   L"Too many characters.", 
                                   L"Error", 
                                   MB_OK); 

                        EndDialog(hDlg, TRUE); 
                        return FALSE; 
                    } 
                    else if (cchPassword == 0) 
                    { 
                        MessageBox(hDlg, 
                                   L"No characters entered.", 
                                   L"Error", 
                                   MB_OK); 

                        EndDialog(hDlg, TRUE); 
                        return FALSE; 
                    } 

                    // Put the number of characters into first word of buffer. 
                    *((LPWORD)lpszPassword) = cchPassword; 

                    // Get the characters. 
                    SendDlgItemMessage(hDlg, 
                                       IDE_PASSWORDEDIT, 
                                       EM_GETLINE, 
                                       (WPARAM) 0,       // line 0 
                                       (LPARAM) lpszPassword); 

                    // Null-terminate the string. 
                    lpszPassword[cchPassword] = 0; 

                    MessageBox(hDlg, 
                               lpszPassword, 
                               L"Did it work?", 
                               MB_OK); 

                    // Call a local password-parsing function. 
                    ParsePassword(lpszPassword); 

                    EndDialog(hDlg, TRUE); 
                    return TRUE; 

                case IDCANCEL: 
                    EndDialog(hDlg, TRUE); 
                    return TRUE; 
            } 
            return 0; 
    } 
    return FALSE; 
    
    UNREFERENCED_PARAMETER(lParam); 
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre os controles de edição](about-edit-controls.md)
</dt> <dt>

[Editar referência de controle](bumper-edit-control-edit-control-reference.md)
</dt> <dt>

[Usando controles de edição](/windows/desktop/Controls/using-edit-controls)
</dt> <dt>

[Controle de edição](edit-controls.md)
</dt> </dl>

 

 