---
title: Como criar um controle de edição de linha única
description: Este tópico demonstra como criar uma caixa de diálogo que contém um controle de edição de linha única.
ms.assetid: 742DF606-9998-46D0-8D0A-F79508AAFFC0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0d5d39a4c9fbc806de6ca151606e770eb0cea9b
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104008611"
---
# <a name="how-to-create-a-single-line-edit-control"></a><span data-ttu-id="1bbdb-103">Como criar um controle de edição de linha única</span><span class="sxs-lookup"><span data-stu-id="1bbdb-103">How to Create a Single Line Edit Control</span></span>

<span data-ttu-id="1bbdb-104">Este tópico demonstra como criar uma caixa de diálogo que contém um controle de edição de linha única.</span><span class="sxs-lookup"><span data-stu-id="1bbdb-104">This topic demonstrates how to create a dialog box that contains a single-line edit control.</span></span>

<span data-ttu-id="1bbdb-105">O controle de edição de linha única tem o estilo de [**\_ senha es**](edit-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="1bbdb-105">The single-line edit control has the [**ES\_PASSWORD**](edit-control-styles.md) style.</span></span> <span data-ttu-id="1bbdb-106">Por padrão, os controles de edição com esse estilo exibem um asterisco para cada caractere que é digitado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="1bbdb-106">By default, edit controls with this style display an asterisk for each character that is typed by the user.</span></span> <span data-ttu-id="1bbdb-107">No entanto, este exemplo usa a mensagem em [**\_ SetPasswordChar**](em-setpasswordchar.md) para alterar o caractere padrão de um asterisco para um sinal de adição (+).</span><span class="sxs-lookup"><span data-stu-id="1bbdb-107">This example, however, uses the [**EM\_SETPASSWORDCHAR**](em-setpasswordchar.md) message to change the default character from an asterisk to a plus sign (+).</span></span> <span data-ttu-id="1bbdb-108">A captura de tela a seguir mostra a caixa de diálogo depois que o usuário insere uma senha.</span><span class="sxs-lookup"><span data-stu-id="1bbdb-108">The following screen shot shows the dialog box after the user has entered a password.</span></span>

![captura de tela de uma caixa de diálogo que contém um controle de edição para inserir uma senha](images/passworddlg.png)

> [!Note]  
> <span data-ttu-id="1bbdb-110">Comctl32.dll versão 6 não é redistribuível.</span><span class="sxs-lookup"><span data-stu-id="1bbdb-110">Comctl32.dll version 6 is not redistributable.</span></span> <span data-ttu-id="1bbdb-111">Para usar Comctl32.dll versão 6, especifique-o em um manifesto.</span><span class="sxs-lookup"><span data-stu-id="1bbdb-111">To use Comctl32.dll version 6, specify it in a manifest.</span></span> <span data-ttu-id="1bbdb-112">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1bbdb-112">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="what-you-need-to-know"></a><span data-ttu-id="1bbdb-113">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="1bbdb-113">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="1bbdb-114">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="1bbdb-114">Technologies</span></span>

-   [<span data-ttu-id="1bbdb-115">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="1bbdb-115">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="1bbdb-116">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="1bbdb-116">Prerequisites</span></span>

-   <span data-ttu-id="1bbdb-117">C/C++</span><span class="sxs-lookup"><span data-stu-id="1bbdb-117">C/C++</span></span>
-   <span data-ttu-id="1bbdb-118">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="1bbdb-118">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="1bbdb-119">Instruções</span><span class="sxs-lookup"><span data-stu-id="1bbdb-119">Instructions</span></span>

### <a name="step-1-create-an-instance-of-the-password-dialog-box"></a><span data-ttu-id="1bbdb-120">Etapa 1: criar uma instância da caixa de diálogo de senha.</span><span class="sxs-lookup"><span data-stu-id="1bbdb-120">Step 1: Create an instance of the password dialog box.</span></span>

<span data-ttu-id="1bbdb-121">O exemplo de código C++ a seguir usa a função caixa para criar uma caixa de diálogo modal.</span><span class="sxs-lookup"><span data-stu-id="1bbdb-121">The following C++ code example uses the DialogBox function to create a modal dialog box.</span></span> <span data-ttu-id="1bbdb-122">A **\_ senha** do modelo de caixa de diálogo IDD é passada como um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="1bbdb-122">The dialog box template **IDD\_PASSWORD** is passed as a parameter.</span></span> <span data-ttu-id="1bbdb-123">Ele define, entre outras coisas, os estilos de janela, os botões e as dimensões da caixa de diálogo senha.</span><span class="sxs-lookup"><span data-stu-id="1bbdb-123">It defines, among other things, the window styles, buttons, and dimensions of the password dialog box.</span></span>


```C++
DialogBox(hInst,                   // application instance
    MAKEINTRESOURCE(IDD_PASSWORD), // dialog box resource
    hWnd,                          // owner window
    PasswordProc                    // dialog box window procedure
    );
```



### <a name="step-2-initialize-the-dialog-box-and-process-user-input"></a><span data-ttu-id="1bbdb-124">Etapa 2: inicializar a caixa de diálogo e processar a entrada do usuário.</span><span class="sxs-lookup"><span data-stu-id="1bbdb-124">Step 2: Initialize the dialog box and process user input.</span></span>

<span data-ttu-id="1bbdb-125">O procedimento de janela no exemplo a seguir inicializa a caixa de diálogo de senha e processa as mensagens de notificação e a entrada do usuário.</span><span class="sxs-lookup"><span data-stu-id="1bbdb-125">The window procedure in the following example initializes the password dialog box and processes notification messages and user input.</span></span>

<span data-ttu-id="1bbdb-126">Durante a inicialização, o procedimento de janela altera o caractere de senha padrão para um **+** sinal e define o botão de pressão padrão como **Cancelar**.</span><span class="sxs-lookup"><span data-stu-id="1bbdb-126">During initialization, the window procedure changes the default password character to a **+** sign and sets the default pushbutton to **Cancel**.</span></span>

<span data-ttu-id="1bbdb-127">Durante o processamento de entrada do usuário, o procedimento de janela altera o botão de ação padrão de **Cancelar** para **OK** assim que o usuário digita o texto no controle de edição.</span><span class="sxs-lookup"><span data-stu-id="1bbdb-127">During user input processing, the window procedure changes the default push button from **CANCEL** to **OK** as soon as the user enters text in the edit control.</span></span> <span data-ttu-id="1bbdb-128">Se o usuário pressionar o botão **OK** , o procedimento de janela usará as mensagens em [**\_ LINELENGTH**](em-linelength.md) e em [**\_ getline**](em-getline.md) para recuperar o texto.</span><span class="sxs-lookup"><span data-stu-id="1bbdb-128">If the user presses the **OK** button, the window procedure uses the [**EM\_LINELENGTH**](em-linelength.md) and [**EM\_GETLINE**](em-getline.md) messages to retrieve the text.</span></span>



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



## <a name="related-topics"></a><span data-ttu-id="1bbdb-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1bbdb-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1bbdb-130">Sobre os controles de edição</span><span class="sxs-lookup"><span data-stu-id="1bbdb-130">About Edit Controls</span></span>](about-edit-controls.md)
</dt> <dt>

[<span data-ttu-id="1bbdb-131">Editar referência de controle</span><span class="sxs-lookup"><span data-stu-id="1bbdb-131">Edit Control Reference</span></span>](bumper-edit-control-edit-control-reference.md)
</dt> <dt>

[<span data-ttu-id="1bbdb-132">Usando controles de edição</span><span class="sxs-lookup"><span data-stu-id="1bbdb-132">Using Edit Controls</span></span>](/windows/desktop/Controls/using-edit-controls)
</dt> <dt>

[<span data-ttu-id="1bbdb-133">Controle de edição</span><span class="sxs-lookup"><span data-stu-id="1bbdb-133">Edit Control</span></span>](edit-controls.md)
</dt> </dl>

 

 