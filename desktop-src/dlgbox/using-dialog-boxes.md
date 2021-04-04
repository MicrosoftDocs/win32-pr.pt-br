---
title: Usando caixas de diálogo
description: Use caixas de diálogo para exibir informações e solicitar entrada do usuário.
ms.assetid: 8a5b6bdd-4429-4f48-b846-6bd617a87abf
keywords:
- Interface do usuário do Windows, janelas
- Interface do usuário do Windows, caixas de diálogo
- janelas, caixas de diálogo
- caixas de diálogo, sobre
- caixas de diálogo, exibindo
- caixas de diálogo modais
- caixas de diálogo sem modo
- caixas de diálogo, modal
- caixas de diálogo, sem janela restrita
- caixas de diálogo, inicializando
- modelos de caixa de diálogo
- caixas de diálogo, modelos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21da47d7d59f4cadc21314566bce41a9ef3456a7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007977"
---
# <a name="using-dialog-boxes"></a><span data-ttu-id="35103-115">Usando caixas de diálogo</span><span class="sxs-lookup"><span data-stu-id="35103-115">Using Dialog Boxes</span></span>

<span data-ttu-id="35103-116">Use caixas de diálogo para exibir informações e solicitar entrada do usuário.</span><span class="sxs-lookup"><span data-stu-id="35103-116">You use dialog boxes to display information and prompt for input from the user.</span></span> <span data-ttu-id="35103-117">O aplicativo carrega e inicializa a caixa de diálogo, processa a entrada do usuário e destrói a caixa de diálogo quando o usuário conclui a tarefa.</span><span class="sxs-lookup"><span data-stu-id="35103-117">Your application loads and initializes the dialog box, processes user input, and destroys the dialog box when the user finishes the task.</span></span> <span data-ttu-id="35103-118">O processo de tratamento de caixas de diálogo varia, dependendo se a caixa de diálogo é modal ou sem janela restrita.</span><span class="sxs-lookup"><span data-stu-id="35103-118">The process for handling dialog boxes varies, depending on whether the dialog box is modal or modeless.</span></span> <span data-ttu-id="35103-119">Uma caixa de diálogo modal exige que o usuário feche a caixa de diálogo antes de ativar outra janela no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="35103-119">A modal dialog box requires the user to close the dialog box before activating another window in the application.</span></span> <span data-ttu-id="35103-120">No entanto, o usuário pode ativar o Windows em diferentes aplicativos.</span><span class="sxs-lookup"><span data-stu-id="35103-120">However, the user can activate windows in different applications.</span></span> <span data-ttu-id="35103-121">Uma caixa de diálogo sem janela restrita não requer uma resposta imediata do usuário.</span><span class="sxs-lookup"><span data-stu-id="35103-121">A modeless dialog box does not require an immediate response from the user.</span></span> <span data-ttu-id="35103-122">É semelhante a uma janela principal que contém controles.</span><span class="sxs-lookup"><span data-stu-id="35103-122">It is similar to a main window containing controls.</span></span>

<span data-ttu-id="35103-123">As seções a seguir discutem como usar os dois tipos de caixas de diálogo.</span><span class="sxs-lookup"><span data-stu-id="35103-123">The following sections discuss how to use both types of dialog boxes.</span></span>

-   [<span data-ttu-id="35103-124">Exibindo uma caixa de mensagem</span><span class="sxs-lookup"><span data-stu-id="35103-124">Displaying a Message Box</span></span>](#displaying-a-message-box)
-   [<span data-ttu-id="35103-125">Criando uma caixa de diálogo modal</span><span class="sxs-lookup"><span data-stu-id="35103-125">Creating a Modal Dialog Box</span></span>](#creating-a-modal-dialog-box)
-   [<span data-ttu-id="35103-126">Criando uma caixa de diálogo sem janela restrita</span><span class="sxs-lookup"><span data-stu-id="35103-126">Creating a Modeless Dialog Box</span></span>](#creating-a-modeless-dialog-box)
-   [<span data-ttu-id="35103-127">Inicializando uma caixa de diálogo</span><span class="sxs-lookup"><span data-stu-id="35103-127">Initializing a Dialog Box</span></span>](#initializing-a-dialog-box)
-   [<span data-ttu-id="35103-128">Criando um modelo na memória</span><span class="sxs-lookup"><span data-stu-id="35103-128">Creating a Template in Memory</span></span>](#creating-a-template-in-memory)

## <a name="displaying-a-message-box"></a><span data-ttu-id="35103-129">Exibindo uma caixa de mensagem</span><span class="sxs-lookup"><span data-stu-id="35103-129">Displaying a Message Box</span></span>

<span data-ttu-id="35103-130">A forma mais simples da caixa de diálogo modal é a caixa de mensagem.</span><span class="sxs-lookup"><span data-stu-id="35103-130">The simplest form of modal dialog box is the message box.</span></span> <span data-ttu-id="35103-131">A maioria dos aplicativos usa caixas de mensagens para avisar o usuário sobre erros e solicitar instruções sobre como proceder após a ocorrência de um erro.</span><span class="sxs-lookup"><span data-stu-id="35103-131">Most applications use message boxes to warn the user of errors and to prompt for directions on how to proceed after an error has occurred.</span></span> <span data-ttu-id="35103-132">Você cria uma caixa de mensagem usando a função [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) ou [**MessageBoxEx**](/windows/desktop/api/Winuser/nf-winuser-messageboxexa) , especificando a mensagem e o número e o tipo de botões a serem exibidos.</span><span class="sxs-lookup"><span data-stu-id="35103-132">You create a message box by using the [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) or [**MessageBoxEx**](/windows/desktop/api/Winuser/nf-winuser-messageboxexa) function, specifying the message and the number and type of buttons to display.</span></span> <span data-ttu-id="35103-133">O sistema cria uma caixa de diálogo modal, fornecendo seu próprio modelo e procedimento de caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="35103-133">The system creates a modal dialog box, providing its own dialog box template and procedure.</span></span> <span data-ttu-id="35103-134">Depois que o usuário fecha a caixa de mensagem, **MessageBox** ou **MessageBoxEx** retorna um valor que identifica o botão escolhido pelo usuário para fechar a caixa de mensagem.</span><span class="sxs-lookup"><span data-stu-id="35103-134">After the user closes the message box, **MessageBox** or **MessageBoxEx** returns a value identifying the button chosen by the user to close the message box.</span></span>

<span data-ttu-id="35103-135">No exemplo a seguir, o aplicativo exibe uma caixa de mensagem que solicita ao usuário uma ação após a ocorrência de uma condição de erro.</span><span class="sxs-lookup"><span data-stu-id="35103-135">In the following example, the application displays a message box that prompts the user for an action after an error condition has occurred.</span></span> <span data-ttu-id="35103-136">A caixa de mensagem exibe a mensagem que descreve a condição de erro e como resolvê-la.</span><span class="sxs-lookup"><span data-stu-id="35103-136">The message box displays the message that describes the error condition and how to resolve it.</span></span> <span data-ttu-id="35103-137">O estilo **MB \_ YesNo** direciona a [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) para fornecer dois botões com os quais o usuário pode escolher como proceder:</span><span class="sxs-lookup"><span data-stu-id="35103-137">The **MB\_YESNO** style directs [**MessageBox**](/windows/desktop/api/Winuser/nf-winuser-messagebox) to provide two buttons with which the user can choose how to proceed:</span></span>


```
int DisplayConfirmSaveAsMessageBox()
{
    int msgboxID = MessageBox(
        NULL,
        L"temp.txt already exists.\nDo you want to replace it?",
        L"Confirm Save As",
        MB_ICONEXCLAMATION | MB_YESNO
    );

    if (msgboxID == IDYES)
    {
        // TODO: add code
    }

    return msgboxID;    
}
```



<span data-ttu-id="35103-138">A imagem a seguir mostra a saída do exemplo de código anterior:</span><span class="sxs-lookup"><span data-stu-id="35103-138">The following image shows the output from the preceding code example:</span></span>

![caixa de mensagem](images/messagebox-01.png)

## <a name="creating-a-modal-dialog-box"></a><span data-ttu-id="35103-140">Criando uma caixa de diálogo modal</span><span class="sxs-lookup"><span data-stu-id="35103-140">Creating a Modal Dialog Box</span></span>

<span data-ttu-id="35103-141">Você cria uma caixa de diálogo modal usando a função [**caixa**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) .</span><span class="sxs-lookup"><span data-stu-id="35103-141">You create a modal dialog box by using the [**DialogBox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) function.</span></span> <span data-ttu-id="35103-142">Você deve especificar o identificador ou o nome de um recurso de modelo de caixa de diálogo e um ponteiro para o procedimento da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="35103-142">You must specify the identifier or name of a dialog box template resource and a pointer to the dialog box procedure.</span></span> <span data-ttu-id="35103-143">A função **caixa** carrega o modelo, exibe a caixa de diálogo e processa todas as entradas do usuário até que o usuário feche a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="35103-143">The **DialogBox** function loads the template, displays the dialog box, and processes all user input until the user closes the dialog box.</span></span>

<span data-ttu-id="35103-144">No exemplo a seguir, o aplicativo exibe uma caixa de diálogo modal quando o usuário clica em **Excluir item** de um menu de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="35103-144">In the following example, the application displays a modal dialog box when the user clicks **Delete Item** from an application menu.</span></span> <span data-ttu-id="35103-145">A caixa de diálogo contém um controle de edição (no qual o usuário insere o nome de um item) e os botões **OK** e **Cancelar** .</span><span class="sxs-lookup"><span data-stu-id="35103-145">The dialog box contains an edit control (in which the user enters the name of an item) and **OK** and **Cancel** buttons.</span></span> <span data-ttu-id="35103-146">Os identificadores de controle para esses controles são ID \_ ItemName, IDOK e IDCANCEL, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="35103-146">The control identifiers for these controls are ID\_ITEMNAME, IDOK, and IDCANCEL, respectively.</span></span>

<span data-ttu-id="35103-147">A primeira parte do exemplo consiste nas instruções que criam a caixa de diálogo modal.</span><span class="sxs-lookup"><span data-stu-id="35103-147">The first part of the example consists of the statements that create the modal dialog box.</span></span> <span data-ttu-id="35103-148">Essas instruções, no procedimento de janela da janela principal do aplicativo, criam a caixa de diálogo quando o sistema recebe uma mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) que tem o \_ identificador de menu DELETEITEM da IDM.</span><span class="sxs-lookup"><span data-stu-id="35103-148">These statements, in the window procedure for the application's main window, create the dialog box when the system receives a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message having the IDM\_DELETEITEM menu identifier.</span></span> <span data-ttu-id="35103-149">A segunda parte do exemplo é o procedimento da caixa de diálogo, que recupera o conteúdo do controle de edição e fecha a caixa de diálogo após receber uma mensagem de **\_ comando do WM** .</span><span class="sxs-lookup"><span data-stu-id="35103-149">The second part of the example is the dialog box procedure, which retrieves the contents of the edit control and closes the dialog box upon receiving a **WM\_COMMAND** message.</span></span>

<span data-ttu-id="35103-150">As instruções a seguir criam a caixa de diálogo modal.</span><span class="sxs-lookup"><span data-stu-id="35103-150">The following statements create the modal dialog box.</span></span> <span data-ttu-id="35103-151">O modelo de caixa de diálogo é um recurso no arquivo executável do aplicativo e tem o identificador de recurso DLG \_ DELETEITEM.</span><span class="sxs-lookup"><span data-stu-id="35103-151">The dialog box template is a resource in the application's executable file and has the resource identifier DLG\_DELETEITEM.</span></span>


```
case WM_COMMAND: 
    switch (LOWORD(wParam)) 
    { 
        case IDM_DELETEITEM: 
            if (DialogBox(hinst, 
                          MAKEINTRESOURCE(DLG_DELETEITEM), 
                          hwnd, 
                          (DLGPROC)DeleteItemProc)==IDOK) 
            {
                // Complete the command; szItemName contains the 
                // name of the item to delete. 
            }

            else 
            {
                // Cancel the command. 
            } 
            break; 
    } 
    return 0L; 
```



<span data-ttu-id="35103-152">Neste exemplo, o aplicativo especifica sua janela principal como a janela do proprietário da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="35103-152">In this example, the application specifies its main window as the owner window for the dialog box.</span></span> <span data-ttu-id="35103-153">Quando o sistema exibe inicialmente a caixa de diálogo, sua posição é relativa ao canto superior esquerdo da área do cliente da janela do proprietário.</span><span class="sxs-lookup"><span data-stu-id="35103-153">When the system initially displays the dialog box, its position is relative to the upper left corner of the owner window's client area.</span></span> <span data-ttu-id="35103-154">O aplicativo usa o valor de retorno de [**caixa**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) para determinar se deseja prosseguir com a operação ou cancelá-lo.</span><span class="sxs-lookup"><span data-stu-id="35103-154">The application uses the return value from [**DialogBox**](/windows/desktop/api/Winuser/nf-winuser-dialogboxa) to determine whether to proceed with the operation or cancel it.</span></span> <span data-ttu-id="35103-155">As instruções a seguir definem o procedimento da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="35103-155">The following statements define the dialog box procedure.</span></span>


```
char szItemName[80]; // receives name of item to delete. 
 
BOOL CALLBACK DeleteItemProc(HWND hwndDlg, 
                             UINT message, 
                             WPARAM wParam, 
                             LPARAM lParam) 
{ 
    switch (message) 
    { 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDOK: 
                    if (!GetDlgItemText(hwndDlg, ID_ITEMNAME, szItemName, 80)) 
                         *szItemName=0; 
 
                    // Fall through. 
 
                case IDCANCEL: 
                    EndDialog(hwndDlg, wParam); 
                    return TRUE; 
            } 
    } 
    return FALSE; 
} 
```



<span data-ttu-id="35103-156">Neste exemplo, o procedimento usa [**GetDlgItemText**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemtexta) para recuperar o texto atual do controle de edição identificado pela ID \_ ItemName.</span><span class="sxs-lookup"><span data-stu-id="35103-156">In this example, the procedure uses [**GetDlgItemText**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemtexta) to retrieve the current text from the edit control identified by ID\_ITEMNAME.</span></span> <span data-ttu-id="35103-157">Em seguida, o procedimento chama a função [**EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog) para definir o valor de retorno da caixa de diálogo como IDOK ou IDCANCEL, dependendo da mensagem recebida e iniciar o processo de fechamento da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="35103-157">The procedure then calls the [**EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog) function to set the dialog box's return value to either IDOK or IDCANCEL, depending on the message received, and to begin the process of closing the dialog box.</span></span> <span data-ttu-id="35103-158">Os identificadores IDOK e IDCANCEL correspondem aos botões **OK** e **Cancelar** .</span><span class="sxs-lookup"><span data-stu-id="35103-158">The IDOK and IDCANCEL identifiers correspond to the **OK** and **Cancel** buttons.</span></span> <span data-ttu-id="35103-159">Depois que o procedimento chama **EndDialog**, o sistema envia mensagens adicionais ao procedimento para destruir a caixa de diálogo e retorna o valor de retorno da caixa de diálogo para a função que criou a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="35103-159">After the procedure calls **EndDialog**, the system sends additional messages to the procedure to destroy the dialog box and returns the dialog box's return value back to the function that created the dialog box.</span></span>

## <a name="creating-a-modeless-dialog-box"></a><span data-ttu-id="35103-160">Criando uma caixa de diálogo sem janela restrita</span><span class="sxs-lookup"><span data-stu-id="35103-160">Creating a Modeless Dialog Box</span></span>

<span data-ttu-id="35103-161">Você cria uma caixa de diálogo sem janela restrita usando a função [**CreateDialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) , especificando o identificador ou o nome de um recurso de modelo de caixa de diálogo e um ponteiro para o procedimento da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="35103-161">You create a modeless dialog box by using the [**CreateDialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) function, specifying the identifier or name of a dialog box template resource and a pointer to the dialog box procedure.</span></span> <span data-ttu-id="35103-162">**CreateDialog** carrega o modelo, cria a caixa de diálogo e, opcionalmente, exibe-o.</span><span class="sxs-lookup"><span data-stu-id="35103-162">**CreateDialog** loads the template, creates the dialog box, and optionally displays it.</span></span> <span data-ttu-id="35103-163">Seu aplicativo é responsável por recuperar e expedir mensagens de entrada do usuário para o procedimento da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="35103-163">Your application is responsible for retrieving and dispatching user input messages to the dialog box procedure.</span></span>

<span data-ttu-id="35103-164">No exemplo a seguir, o aplicativo exibe uma caixa de diálogo sem janela restrita — se ela ainda não estiver exibida — quando o usuário clicar em **ir para** de um menu de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="35103-164">In the following example, the application displays a modeless dialog box — if it is not already displayed — when the user clicks **Go To** from an application menu.</span></span> <span data-ttu-id="35103-165">A caixa de diálogo contém um controle de edição, uma caixa de seleção e os botões **OK** e **Cancelar** .</span><span class="sxs-lookup"><span data-stu-id="35103-165">The dialog box contains an edit control, a check box, and **OK** and **Cancel** buttons.</span></span> <span data-ttu-id="35103-166">O modelo de caixa de diálogo é um recurso no arquivo executável do aplicativo e tem o identificador de recurso DLG \_ goto.</span><span class="sxs-lookup"><span data-stu-id="35103-166">The dialog box template is a resource in the application's executable file and has the resource identifier DLG\_GOTO.</span></span> <span data-ttu-id="35103-167">O usuário insere um número de linha no controle de edição e marca a caixa de seleção para especificar que o número de linha é relativo à linha atual.</span><span class="sxs-lookup"><span data-stu-id="35103-167">The user enters a line number in the edit control and checks the check box to specify that the line number is relative to the current line.</span></span> <span data-ttu-id="35103-168">Os identificadores de controle são ID \_ line, ID \_ ABSREL, IDOK e IDCANCEL.</span><span class="sxs-lookup"><span data-stu-id="35103-168">The control identifiers are ID\_LINE, ID\_ABSREL, IDOK, and IDCANCEL.</span></span>

<span data-ttu-id="35103-169">As instruções na primeira parte do exemplo criam a caixa de diálogo sem janela restrita.</span><span class="sxs-lookup"><span data-stu-id="35103-169">The statements in the first part of the example create the modeless dialog box.</span></span> <span data-ttu-id="35103-170">Essas instruções, no procedimento de janela da janela principal do aplicativo, criam a caixa de diálogo quando o procedimento de janela recebe uma mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) que tem o identificador de menu do IDM \_ goto, mas somente se a variável global ainda não contiver um identificador válido.</span><span class="sxs-lookup"><span data-stu-id="35103-170">These statements, in the window procedure for the application's main window, create the dialog box when the window procedure receives a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message having the IDM\_GOTO menu identifier, but only if the global variable does not already contain a valid handle.</span></span> <span data-ttu-id="35103-171">A segunda parte do exemplo é o loop de mensagem principal do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="35103-171">The second part of the example is the application's main message loop.</span></span> <span data-ttu-id="35103-172">O loop inclui a função [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) para garantir que o usuário possa usar a interface de teclado da caixa de diálogo nesta caixa de diálogo sem janela restrita.</span><span class="sxs-lookup"><span data-stu-id="35103-172">The loop includes the [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) function to ensure that the user can use the dialog box keyboard interface in this modeless dialog box.</span></span> <span data-ttu-id="35103-173">A terceira parte do exemplo é o procedimento da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="35103-173">The third part of the example is the dialog box procedure.</span></span> <span data-ttu-id="35103-174">O procedimento recupera o conteúdo do controle de edição e a caixa de seleção quando o usuário clica no botão **OK** .</span><span class="sxs-lookup"><span data-stu-id="35103-174">The procedure retrieves the contents of the edit control and check box when the user clicks the **OK** button.</span></span> <span data-ttu-id="35103-175">O procedimento destrói a caixa de diálogo quando o usuário clica no botão **Cancelar** .</span><span class="sxs-lookup"><span data-stu-id="35103-175">The procedure destroys the dialog box when the user clicks the **Cancel** button.</span></span>


```
HWND hwndGoto = NULL;  // Window handle of dialog box 
                
...

case WM_COMMAND: 
    switch (LOWORD(wParam)) 
    { 
        case IDM_GOTO: 
            if (!IsWindow(hwndGoto)) 
            { 
                hwndGoto = CreateDialog(hinst, 
                                        MAKEINTRESOURCE(DLG_GOTO), 
                                        hwnd, 
                                        (DLGPROC)GoToProc); 
                ShowWindow(hwndGoto, SW_SHOW); 
            } 
            break; 
    } 
    return 0L; 
```



<span data-ttu-id="35103-176">Nas instruções anteriores, [**CreateDialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) só será chamado se não `hwndGoto` contiver um identificador de janela válido.</span><span class="sxs-lookup"><span data-stu-id="35103-176">In the preceding statements, [**CreateDialog**](/windows/desktop/api/Winuser/nf-winuser-createdialoga) is called only if `hwndGoto` does not contain a valid window handle.</span></span> <span data-ttu-id="35103-177">Isso garante que o aplicativo não exiba duas caixas de diálogo ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="35103-177">This ensures that the application does not display two dialog boxes at the same time.</span></span> <span data-ttu-id="35103-178">Para dar suporte a esse método de verificação, o procedimento de caixa de diálogo deve definir como **NULL** quando destrói a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="35103-178">To support this method of checking, the dialog procedure must set to **NULL** when it destroys the dialog box.</span></span>

<span data-ttu-id="35103-179">O loop de mensagem para um aplicativo consiste nas instruções a seguir.</span><span class="sxs-lookup"><span data-stu-id="35103-179">The message loop for an application consists of the following statements.</span></span>


```
BOOL bRet;

while ((bRet = GetMessage(&msg, NULL, 0, 0)) != 0) 
{ 
    if (bRet == -1)
    {
        // Handle the error and possibly exit
    }
    else if (!IsWindow(hwndGoto) || !IsDialogMessage(hwndGoto, &msg)) 
    { 
        TranslateMessage(&msg); 
        DispatchMessage(&msg); 
    } 
} 
```



<span data-ttu-id="35103-180">O loop verifica a validade do identificador de janela para a caixa de diálogo e só chama a função [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) se o identificador for válido.</span><span class="sxs-lookup"><span data-stu-id="35103-180">The loop checks the validity of the window handle to the dialog box and only calls the [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) function if the handle is valid.</span></span> <span data-ttu-id="35103-181">**IsDialogMessage** só processará a mensagem se ela pertencer à caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="35103-181">**IsDialogMessage** only processes the message if it belongs to the dialog box.</span></span> <span data-ttu-id="35103-182">Caso contrário, ele retornará **false** e o loop expedirá a mensagem para a janela apropriada.</span><span class="sxs-lookup"><span data-stu-id="35103-182">Otherwise, it returns **FALSE** and the loop dispatches the message to the appropriate window.</span></span>

<span data-ttu-id="35103-183">As instruções a seguir definem o procedimento da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="35103-183">The following statements define the dialog box procedure.</span></span>


```
int iLine;             // Receives line number.
BOOL fRelative;        // Receives check box status. 
 
BOOL CALLBACK GoToProc(HWND hwndDlg, UINT message, WPARAM wParam, LPARAM lParam) 
{ 
    BOOL fError; 
 
    switch (message) 
    { 
        case WM_INITDIALOG: 
            CheckDlgButton(hwndDlg, ID_ABSREL, fRelative); 
            return TRUE; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDOK: 
                    fRelative = IsDlgButtonChecked(hwndDlg, ID_ABSREL); 
                    iLine = GetDlgItemInt(hwndDlg, ID_LINE, &fError, fRelative); 
                    if (fError) 
                    { 
                        MessageBox(hwndDlg, SZINVALIDNUMBER, SZGOTOERR, MB_OK); 
                        SendDlgItemMessage(hwndDlg, ID_LINE, EM_SETSEL, 0, -1L); 
                    } 
                    else 

                    // Notify the owner window to carry out the task. 
 
                    return TRUE; 
 
                case IDCANCEL: 
                    DestroyWindow(hwndDlg); 
                    hwndGoto = NULL; 
                    return TRUE; 
            } 
    } 
    return FALSE; 
} 
```



<span data-ttu-id="35103-184">Nas instruções anteriores, o procedimento processa as mensagens de [**\_ comando**](/windows/desktop/menurc/wm-command) do [**WM \_ INITDIALOG**](wm-initdialog.md) e do WM.</span><span class="sxs-lookup"><span data-stu-id="35103-184">In the preceding statements, the procedure processes the [**WM\_INITDIALOG**](wm-initdialog.md) and [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) messages.</span></span> <span data-ttu-id="35103-185">Durante o processamento do **WM \_ INITDIALOG** , o procedimento Inicializa a caixa de seleção passando o valor atual da variável global para [**CheckDlgButton**](https://msdn.microsoft.com/library/Cc410649(v=MSDN.10).aspx).</span><span class="sxs-lookup"><span data-stu-id="35103-185">During **WM\_INITDIALOG** processing, the procedure initializes the check box by passing the current value of the global variable to [**CheckDlgButton**](https://msdn.microsoft.com/library/Cc410649(v=MSDN.10).aspx).</span></span> <span data-ttu-id="35103-186">Em seguida, o procedimento retorna **true** para instruir o sistema a definir o foco de entrada padrão.</span><span class="sxs-lookup"><span data-stu-id="35103-186">The procedure then returns **TRUE** to direct the system to set the default input focus.</span></span>

<span data-ttu-id="35103-187">Durante o processamento de [**\_ comandos do WM**](/windows/desktop/menurc/wm-command) , o procedimento fecha a caixa de diálogo somente se o usuário clicar no botão **Cancelar** , ou seja, o botão que tem o identificador IDCANCEL.</span><span class="sxs-lookup"><span data-stu-id="35103-187">During [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) processing, the procedure closes the dialog box only if the user clicks the **Cancel** button — that is, the button having the IDCANCEL identifier.</span></span> <span data-ttu-id="35103-188">O procedimento deve chamar [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) para fechar uma caixa de diálogo sem janela restrita.</span><span class="sxs-lookup"><span data-stu-id="35103-188">The procedure must call [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) to close a modeless dialog box.</span></span> <span data-ttu-id="35103-189">Observe que o procedimento também define a variável como **NULL** para garantir que outras instruções que dependem dessa variável operem corretamente.</span><span class="sxs-lookup"><span data-stu-id="35103-189">Notice that the procedure also sets the variable to **NULL** to ensure that other statements that depend on this variable operate correctly.</span></span>

<span data-ttu-id="35103-190">Se o usuário clicar no botão **OK** , o procedimento recuperará o estado atual da caixa de seleção e o atribuirá à variável **fRelative** .</span><span class="sxs-lookup"><span data-stu-id="35103-190">If the user clicks the **OK** button, the procedure retrieves the current state of the check box and assigns it to the **fRelative** variable.</span></span> <span data-ttu-id="35103-191">Em seguida, ele usa a variável para recuperar o número de linha do controle de edição.</span><span class="sxs-lookup"><span data-stu-id="35103-191">It then uses the variable to retrieve the line number from the edit control.</span></span> <span data-ttu-id="35103-192">[**GetDlgItemInt**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemint) converte o texto no controle de edição em um número inteiro.</span><span class="sxs-lookup"><span data-stu-id="35103-192">[**GetDlgItemInt**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemint) translates the text in the edit control into an integer.</span></span> <span data-ttu-id="35103-193">O valor de **fRelative** determina se a função interpreta o número como um valor assinado ou sem sinal.</span><span class="sxs-lookup"><span data-stu-id="35103-193">The value of **fRelative** determines whether the function interprets the number as a signed or unsigned value.</span></span> <span data-ttu-id="35103-194">Se o texto do controle de edição não for um número válido, **GetDlgItemInt** definirá o valor da variável **referenciadora** como diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="35103-194">If the edit control text is not a valid number, **GetDlgItemInt** sets the value of the **fError** variable to nonzero.</span></span> <span data-ttu-id="35103-195">O procedimento verifica esse valor para determinar se uma mensagem de erro deve ser exibida ou executar a tarefa.</span><span class="sxs-lookup"><span data-stu-id="35103-195">The procedure checks this value to determine whether to display an error message or carry out the task.</span></span> <span data-ttu-id="35103-196">No caso de um erro, o procedimento da caixa de diálogo envia uma mensagem para o controle de edição, direcionando-o para selecionar o texto no controle para que o usuário possa substituí-lo facilmente.</span><span class="sxs-lookup"><span data-stu-id="35103-196">In the event of an error, the dialog box procedure sends a message to the edit control, directing it to select the text in the control so that the user can easily replace it.</span></span> <span data-ttu-id="35103-197">Se **GetDlgItemInt** não retornar um erro, o procedimento poderá executar a tarefa solicitada ou enviar uma mensagem para a janela do proprietário, direcionando-a para realizar a operação.</span><span class="sxs-lookup"><span data-stu-id="35103-197">If **GetDlgItemInt** does not return an error, the procedure can either carry out the requested task itself or send a message to the owner window, directing it to carry out the operation.</span></span>

## <a name="initializing-a-dialog-box"></a><span data-ttu-id="35103-198">Inicializando uma caixa de diálogo</span><span class="sxs-lookup"><span data-stu-id="35103-198">Initializing a Dialog Box</span></span>

<span data-ttu-id="35103-199">Você inicializa a caixa de diálogo e seu conteúdo durante o processamento da mensagem [**\_ INITDIALOG do WM**](wm-initdialog.md) .</span><span class="sxs-lookup"><span data-stu-id="35103-199">You initialize the dialog box and its contents while processing the [**WM\_INITDIALOG**](wm-initdialog.md) message.</span></span> <span data-ttu-id="35103-200">A tarefa mais comum é inicializar os controles para refletir as configurações da caixa de diálogo atual.</span><span class="sxs-lookup"><span data-stu-id="35103-200">The most common task is to initialize the controls to reflect the current dialog box settings.</span></span> <span data-ttu-id="35103-201">Outra tarefa comum é centralizar uma caixa de diálogo na tela ou dentro de sua janela de proprietário.</span><span class="sxs-lookup"><span data-stu-id="35103-201">Another common task is to center a dialog box on the screen or within its owner window.</span></span> <span data-ttu-id="35103-202">Uma tarefa útil para algumas caixas de diálogo é definir o foco de entrada para um controle especificado em vez de aceitar o foco de entrada padrão.</span><span class="sxs-lookup"><span data-stu-id="35103-202">A useful task for some dialog boxes is to set the input focus to a specified control rather than accept the default input focus.</span></span>

<span data-ttu-id="35103-203">No exemplo a seguir, o procedimento da caixa de diálogo centraliza a caixa de diálogo e define o foco de entrada durante o processamento da mensagem [**\_ INITDIALOG do WM**](wm-initdialog.md) .</span><span class="sxs-lookup"><span data-stu-id="35103-203">In the following example, the dialog box procedure centers the dialog box and sets the input focus while processing the [**WM\_INITDIALOG**](wm-initdialog.md) message.</span></span> <span data-ttu-id="35103-204">Para centralizar a caixa de diálogo, o procedimento recupera os retângulos da janela para a caixa de diálogo e a janela do proprietário e calcula uma nova posição para a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="35103-204">To center the dialog box, the procedure retrieves the window rectangles for the dialog box and the owner window and calculates a new position for the dialog box.</span></span> <span data-ttu-id="35103-205">Para definir o foco de entrada, o procedimento verifica o parâmetro *wParam* para determinar o identificador do foco de entrada padrão.</span><span class="sxs-lookup"><span data-stu-id="35103-205">To set the input focus, the procedure checks the *wParam* parameter to determine the identifier of the default input focus.</span></span>


```
HWND hwndOwner; 
RECT rc, rcDlg, rcOwner; 

....
 
case WM_INITDIALOG: 

    // Get the owner window and dialog box rectangles. 

    if ((hwndOwner = GetParent(hwndDlg)) == NULL) 
    {
        hwndOwner = GetDesktopWindow(); 
    }

    GetWindowRect(hwndOwner, &rcOwner); 
    GetWindowRect(hwndDlg, &rcDlg); 
    CopyRect(&rc, &rcOwner); 

    // Offset the owner and dialog box rectangles so that right and bottom 
    // values represent the width and height, and then offset the owner again 
    // to discard space taken up by the dialog box. 

    OffsetRect(&rcDlg, -rcDlg.left, -rcDlg.top); 
    OffsetRect(&rc, -rc.left, -rc.top); 
    OffsetRect(&rc, -rcDlg.right, -rcDlg.bottom); 

    // The new position is the sum of half the remaining space and the owner's 
    // original position. 

    SetWindowPos(hwndDlg, 
                 HWND_TOP, 
                 rcOwner.left + (rc.right / 2), 
                 rcOwner.top + (rc.bottom / 2), 
                 0, 0,          // Ignores size arguments. 
                 SWP_NOSIZE); 

    if (GetDlgCtrlID((HWND) wParam) != ID_ITEMNAME) 
    { 
        SetFocus(GetDlgItem(hwndDlg, ID_ITEMNAME)); 
        return FALSE; 
    } 
    return TRUE; 
```



<span data-ttu-id="35103-206">Nas instruções anteriores, o procedimento usa a função [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent) para recuperar o identificador de janela do proprietário para uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="35103-206">In the preceding statements, the procedure uses the [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent) function to retrieve the owner window handle to a dialog box.</span></span> <span data-ttu-id="35103-207">A função retorna o identificador de janela do proprietário para caixas de diálogo e o identificador da janela pai para janelas filhas.</span><span class="sxs-lookup"><span data-stu-id="35103-207">The function returns the owner window handle to dialog boxes, and the parent window handle to child windows.</span></span> <span data-ttu-id="35103-208">Como um aplicativo pode criar uma caixa de diálogo que não tem proprietário, o procedimento verifica o identificador retornado e usa a função [**GetDesktopWindow**](/windows/desktop/api/winuser/nf-winuser-getdesktopwindow) para recuperar o identificador da janela da área de trabalho, se necessário.</span><span class="sxs-lookup"><span data-stu-id="35103-208">Because an application can create a dialog box that has no owner, the procedure checks the returned handle and uses the [**GetDesktopWindow**](/windows/desktop/api/winuser/nf-winuser-getdesktopwindow) function to retrieve the desktop window handle, if necessary.</span></span> <span data-ttu-id="35103-209">Depois de calcular a nova posição, o procedimento usa a função [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) para mover a caixa de diálogo, especificando o \_ valor superior de HWND para garantir que a caixa de diálogo permaneça na parte superior da janela do proprietário.</span><span class="sxs-lookup"><span data-stu-id="35103-209">After calculating the new position, the procedure uses the [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) function to move the dialog box, specifying the HWND\_TOP value to ensure that the dialog box remains on top of the owner window.</span></span>

<span data-ttu-id="35103-210">Antes de definir o foco de entrada, o procedimento verifica o identificador de controle do foco de entrada padrão.</span><span class="sxs-lookup"><span data-stu-id="35103-210">Before setting the input focus, the procedure checks the control identifier of the default input focus.</span></span> <span data-ttu-id="35103-211">O sistema passa o identificador de janela do foco de entrada padrão no parâmetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="35103-211">The system passes the window handle of the default input focus in the *wParam* parameter.</span></span> <span data-ttu-id="35103-212">A função [**GetDlgCtrlID**](/windows/desktop/api/Winuser/nf-winuser-getdlgctrlid) retorna o identificador do controle identificado pelo identificador de janela.</span><span class="sxs-lookup"><span data-stu-id="35103-212">The [**GetDlgCtrlID**](/windows/desktop/api/Winuser/nf-winuser-getdlgctrlid) function returns the identifier for the control identified by the window handle.</span></span> <span data-ttu-id="35103-213">Se o identificador não corresponder ao identificador correto, o procedimento usará a função [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) para definir o foco de entrada.</span><span class="sxs-lookup"><span data-stu-id="35103-213">If the identifier does not match the correct identifier, the procedure uses the [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) function to set the input focus.</span></span> <span data-ttu-id="35103-214">A função [**GetDlgItem**](/windows/desktop/api/Winuser/nf-winuser-getdlgitem) é necessária para recuperar o identificador de janela do controle desejado.</span><span class="sxs-lookup"><span data-stu-id="35103-214">The [**GetDlgItem**](/windows/desktop/api/Winuser/nf-winuser-getdlgitem) function is required to retrieve the window handle of the desired control.</span></span>

## <a name="creating-a-template-in-memory"></a><span data-ttu-id="35103-215">Criando um modelo na memória</span><span class="sxs-lookup"><span data-stu-id="35103-215">Creating a Template in Memory</span></span>

<span data-ttu-id="35103-216">Às vezes, os aplicativos adaptam ou modificam o conteúdo das caixas de diálogo dependendo do estado atual dos dados que estão sendo processados.</span><span class="sxs-lookup"><span data-stu-id="35103-216">Applications sometimes adapt or modify the content of dialog boxes depending on the current state of the data being processed.</span></span> <span data-ttu-id="35103-217">Nesses casos, não é prático fornecer todos os modelos de caixa de diálogo possíveis como recursos no arquivo executável do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="35103-217">In such cases, it is not practical to provide all possible dialog box templates as resources in the application's executable file.</span></span> <span data-ttu-id="35103-218">Mas a criação de modelos na memória proporciona ao aplicativo mais flexibilidade para se adaptar a qualquer circunstância.</span><span class="sxs-lookup"><span data-stu-id="35103-218">But creating templates in memory gives the application more flexibility to adapt to any circumstances.</span></span>

<span data-ttu-id="35103-219">No exemplo a seguir, o aplicativo cria um modelo na memória para uma caixa de diálogo modal que contém um botão de mensagem e **OK** e **ajuda** .</span><span class="sxs-lookup"><span data-stu-id="35103-219">In the following example, the application creates a template in memory for a modal dialog box that contains a message and **OK** and **Help** buttons.</span></span>

<span data-ttu-id="35103-220">Em um modelo de caixa de diálogo, todas as cadeias de caracteres, como a caixa de diálogo e os títulos dos botões, devem ser cadeias Unicode.</span><span class="sxs-lookup"><span data-stu-id="35103-220">In a dialog template, all character strings, such as the dialog box and button titles, must be Unicode strings.</span></span> <span data-ttu-id="35103-221">Este exemplo usa a função [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) para gerar essas cadeias de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="35103-221">This example uses the [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) function to generate these Unicode strings.</span></span>

<span data-ttu-id="35103-222">As estruturas [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) em um modelo de caixa de diálogo devem ser alinhadas em limites **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="35103-222">The [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) structures in a dialog template must be aligned on **DWORD** boundaries.</span></span> <span data-ttu-id="35103-223">Para alinhar essas estruturas, este exemplo usa uma rotina auxiliar que usa um ponteiro de entrada e retorna o ponteiro mais próximo que está alinhado em um limite **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="35103-223">To align these structures, this example uses a helper routine that takes an input pointer and returns the closest pointer that is aligned on a **DWORD** boundary.</span></span>


```
#define ID_HELP   150
#define ID_TEXT   200

LPWORD lpwAlign(LPWORD lpIn)
{
    ULONG ul;

    ul = (ULONG)lpIn;
    ul ++;
    ul >>=1;
    ul <<=1;
    return (LPWORD)ul;
}

LRESULT DisplayMyMessage(HINSTANCE hinst, HWND hwndOwner, LPSTR lpszMessage)
{
    HGLOBAL hgbl;
    LPDLGTEMPLATE lpdt;
    LPDLGITEMTEMPLATE lpdit;
    LPWORD lpw;
    LPWSTR lpwsz;
    LRESULT ret;
    int nchar;

    hgbl = GlobalAlloc(GMEM_ZEROINIT, 1024);
    if (!hgbl)
        return -1;
 
    lpdt = (LPDLGTEMPLATE)GlobalLock(hgbl);
 
    // Define a dialog box.
 
    lpdt->style = WS_POPUP | WS_BORDER | WS_SYSMENU | DS_MODALFRAME | WS_CAPTION;
    lpdt->cdit = 3;         // Number of controls
    lpdt->x  = 10;  lpdt->y  = 10;
    lpdt->cx = 100; lpdt->cy = 100;

    lpw = (LPWORD)(lpdt + 1);
    *lpw++ = 0;             // No menu
    *lpw++ = 0;             // Predefined dialog box class (by default)

    lpwsz = (LPWSTR)lpw;
    nchar = 1 + MultiByteToWideChar(CP_ACP, 0, "My Dialog", -1, lpwsz, 50);
    lpw += nchar;

    //-----------------------
    // Define an OK button.
    //-----------------------
    lpw = lpwAlign(lpw);    // Align DLGITEMTEMPLATE on DWORD boundary
    lpdit = (LPDLGITEMTEMPLATE)lpw;
    lpdit->x  = 10; lpdit->y  = 70;
    lpdit->cx = 80; lpdit->cy = 20;
    lpdit->id = IDOK;       // OK button identifier
    lpdit->style = WS_CHILD | WS_VISIBLE | BS_DEFPUSHBUTTON;

    lpw = (LPWORD)(lpdit + 1);
    *lpw++ = 0xFFFF;
    *lpw++ = 0x0080;        // Button class

    lpwsz = (LPWSTR)lpw;
    nchar = 1 + MultiByteToWideChar(CP_ACP, 0, "OK", -1, lpwsz, 50);
    lpw += nchar;
    *lpw++ = 0;             // No creation data

    //-----------------------
    // Define a Help button.
    //-----------------------
    lpw = lpwAlign(lpw);    // Align DLGITEMTEMPLATE on DWORD boundary
    lpdit = (LPDLGITEMTEMPLATE)lpw;
    lpdit->x  = 55; lpdit->y  = 10;
    lpdit->cx = 40; lpdit->cy = 20;
    lpdit->id = ID_HELP;    // Help button identifier
    lpdit->style = WS_CHILD | WS_VISIBLE | BS_PUSHBUTTON;

    lpw = (LPWORD)(lpdit + 1);
    *lpw++ = 0xFFFF;
    *lpw++ = 0x0080;        // Button class atom

    lpwsz = (LPWSTR)lpw;
    nchar = 1 + MultiByteToWideChar(CP_ACP, 0, "Help", -1, lpwsz, 50);
    lpw += nchar;
    *lpw++ = 0;             // No creation data

    //-----------------------
    // Define a static text control.
    //-----------------------
    lpw = lpwAlign(lpw);    // Align DLGITEMTEMPLATE on DWORD boundary
    lpdit = (LPDLGITEMTEMPLATE)lpw;
    lpdit->x  = 10; lpdit->y  = 10;
    lpdit->cx = 40; lpdit->cy = 20;
    lpdit->id = ID_TEXT;    // Text identifier
    lpdit->style = WS_CHILD | WS_VISIBLE | SS_LEFT;

    lpw = (LPWORD)(lpdit + 1);
    *lpw++ = 0xFFFF;
    *lpw++ = 0x0082;        // Static class

    for (lpwsz = (LPWSTR)lpw; *lpwsz++ = (WCHAR)*lpszMessage++;);
    lpw = (LPWORD)lpwsz;
    *lpw++ = 0;             // No creation data

    GlobalUnlock(hgbl); 
    ret = DialogBoxIndirect(hinst, 
                           (LPDLGTEMPLATE)hgbl, 
                           hwndOwner, 
                           (DLGPROC)DialogProc); 
    GlobalFree(hgbl); 
    return ret; 
}
```



 

 