---
title: Usando aceleradores de teclado
description: Esta seção aborda as tarefas associadas a aceleradores de teclado.
ms.assetid: 11c42d69-7454-43e6-9f44-c14a283814ce
keywords:
- entrada do usuário, aceleradores de teclado
- capturando entrada do usuário, aceleradores de teclado
- aceleradores de teclado
- aceleradores
- tabelas do acelerador
- recursos da tabela de aceleração
- função de acelerador de conversão
- WM_COMMAND mensagem
- WM_SYS mensagem de comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2241ba828ea9e6be5e4bb0b7471adcc3130940ca
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007535"
---
# <a name="using-keyboard-accelerators"></a><span data-ttu-id="b14c5-112">Usando aceleradores de teclado</span><span class="sxs-lookup"><span data-stu-id="b14c5-112">Using Keyboard Accelerators</span></span>

<span data-ttu-id="b14c5-113">Esta seção aborda as tarefas associadas a aceleradores de teclado.</span><span class="sxs-lookup"><span data-stu-id="b14c5-113">This section covers tasks that are associated with keyboard accelerators.</span></span>

-   [<span data-ttu-id="b14c5-114">Usando um recurso de tabela de acelerador</span><span class="sxs-lookup"><span data-stu-id="b14c5-114">Using an Accelerator Table Resource</span></span>](#using-an-accelerator-table-resource)
    -   [<span data-ttu-id="b14c5-115">Criando o recurso de tabela de acelerador</span><span class="sxs-lookup"><span data-stu-id="b14c5-115">Creating the Accelerator Table Resource</span></span>](#creating-the-accelerator-table-resource)
    -   [<span data-ttu-id="b14c5-116">Carregando o recurso de tabela de acelerador</span><span class="sxs-lookup"><span data-stu-id="b14c5-116">Loading the Accelerator Table Resource</span></span>](#loading-the-accelerator-table-resource)
    -   [<span data-ttu-id="b14c5-117">Chamando a função acelerador de conversão</span><span class="sxs-lookup"><span data-stu-id="b14c5-117">Calling the Translate Accelerator Function</span></span>](#calling-the-translate-accelerator-function)
    -   [<span data-ttu-id="b14c5-118">Processando \_ mensagens de comando do WM</span><span class="sxs-lookup"><span data-stu-id="b14c5-118">Processing WM\_COMMAND Messages</span></span>](/windows)
    -   [<span data-ttu-id="b14c5-119">Destruindo o recurso de tabela de acelerador</span><span class="sxs-lookup"><span data-stu-id="b14c5-119">Destroying the Accelerator Table Resource</span></span>](#destroying-the-accelerator-table-resource)
    -   [<span data-ttu-id="b14c5-120">Criando aceleradores para atributos de fonte</span><span class="sxs-lookup"><span data-stu-id="b14c5-120">Creating Accelerators for Font Attributes</span></span>](#creating-accelerators-for-font-attributes)
-   [<span data-ttu-id="b14c5-121">Usando uma tabela de acelerador criada em tempo de execução</span><span class="sxs-lookup"><span data-stu-id="b14c5-121">Using an Accelerator Table Created at Run Time</span></span>](#using-an-accelerator-table-created-at-run-time)
    -   [<span data-ttu-id="b14c5-122">Criando uma tabela de acelerador de Run-Time</span><span class="sxs-lookup"><span data-stu-id="b14c5-122">Creating a Run-Time Accelerator Table</span></span>](#creating-a-run-time-accelerator-table)
    -   [<span data-ttu-id="b14c5-123">Aceleradores de processamento</span><span class="sxs-lookup"><span data-stu-id="b14c5-123">Processing Accelerators</span></span>](#processing-accelerators)
    -   [<span data-ttu-id="b14c5-124">Destruindo uma tabela de acelerador de Run-Time</span><span class="sxs-lookup"><span data-stu-id="b14c5-124">Destroying a Run-Time Accelerator Table</span></span>](#destroying-a-run-time-accelerator-table)
    -   [<span data-ttu-id="b14c5-125">Criando aceleradores editáveis do usuário</span><span class="sxs-lookup"><span data-stu-id="b14c5-125">Creating User Editable Accelerators</span></span>](#creating-user-editable-accelerators)

## <a name="using-an-accelerator-table-resource"></a><span data-ttu-id="b14c5-126">Usando um recurso de tabela de acelerador</span><span class="sxs-lookup"><span data-stu-id="b14c5-126">Using an Accelerator Table Resource</span></span>

<span data-ttu-id="b14c5-127">A maneira mais comum de adicionar suporte a acelerador a um aplicativo é incluir um recurso de tabela de acelerador com o arquivo executável do aplicativo e, em seguida, carregar o recurso em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="b14c5-127">The most common way to add accelerator support to an application is to include an accelerator-table resource with the application's executable file and then load the resource at run time.</span></span>

<span data-ttu-id="b14c5-128">Esta seção aborda os tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="b14c5-128">This section covers the following topics.</span></span>

-   [<span data-ttu-id="b14c5-129">Criando o recurso de tabela de acelerador</span><span class="sxs-lookup"><span data-stu-id="b14c5-129">Creating the Accelerator Table Resource</span></span>](#creating-the-accelerator-table-resource)
-   [<span data-ttu-id="b14c5-130">Carregando o recurso de tabela de acelerador</span><span class="sxs-lookup"><span data-stu-id="b14c5-130">Loading the Accelerator Table Resource</span></span>](#loading-the-accelerator-table-resource)
-   [<span data-ttu-id="b14c5-131">Chamando a função acelerador de conversão</span><span class="sxs-lookup"><span data-stu-id="b14c5-131">Calling the Translate Accelerator Function</span></span>](#calling-the-translate-accelerator-function)
-   [<span data-ttu-id="b14c5-132">Processando \_ mensagens de comando do WM</span><span class="sxs-lookup"><span data-stu-id="b14c5-132">Processing WM\_COMMAND Messages</span></span>](/windows)
-   [<span data-ttu-id="b14c5-133">Destruindo o recurso de tabela de acelerador</span><span class="sxs-lookup"><span data-stu-id="b14c5-133">Destroying the Accelerator Table Resource</span></span>](#destroying-the-accelerator-table-resource)
-   [<span data-ttu-id="b14c5-134">Criando aceleradores para atributos de fonte</span><span class="sxs-lookup"><span data-stu-id="b14c5-134">Creating Accelerators for Font Attributes</span></span>](#creating-accelerators-for-font-attributes)

### <a name="creating-the-accelerator-table-resource"></a><span data-ttu-id="b14c5-135">Criando o recurso de tabela de acelerador</span><span class="sxs-lookup"><span data-stu-id="b14c5-135">Creating the Accelerator Table Resource</span></span>

<span data-ttu-id="b14c5-136">Você cria um recurso de tabela de aceleração usando [a instrução](./accelerators-resource.md) Accelerators no arquivo de definição de recurso do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b14c5-136">You create an accelerator-table resource by using the [ACCELERATORS](./accelerators-resource.md) statement in your application's resource-definition file.</span></span> <span data-ttu-id="b14c5-137">Você deve atribuir um nome ou identificador de recurso à tabela de aceleração, preferencialmente, ao contrário de qualquer outro recurso.</span><span class="sxs-lookup"><span data-stu-id="b14c5-137">You must assign a name or resource identifier to the accelerator table, preferably unlike that of any other resource.</span></span> <span data-ttu-id="b14c5-138">O sistema usa esse identificador para carregar o recurso em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="b14c5-138">The system uses this identifier to load the resource at run time.</span></span>

<span data-ttu-id="b14c5-139">Cada acelerador que você define requer uma entrada separada na tabela do acelerador.</span><span class="sxs-lookup"><span data-stu-id="b14c5-139">Each accelerator you define requires a separate entry in the accelerator table.</span></span> <span data-ttu-id="b14c5-140">Em cada entrada, você define o pressionamento de teclas (um código de caractere ASCII ou o código de chave virtual) que gera o acelerador e o identificador do acelerador.</span><span class="sxs-lookup"><span data-stu-id="b14c5-140">In each entry, you define the keystroke (either an ASCII character code or virtual-key code) that generates the accelerator and the accelerator's identifier.</span></span> <span data-ttu-id="b14c5-141">Você também deve especificar se o pressionamento de tecla deve ser usado em alguma combinação com as teclas ALT, SHIFT ou CTRL.</span><span class="sxs-lookup"><span data-stu-id="b14c5-141">You must also specify whether the keystroke must be used in some combination with the ALT, SHIFT, or CTRL keys.</span></span> <span data-ttu-id="b14c5-142">Para obter mais informações sobre chaves virtuais, consulte [entrada de teclado](/windows/desktop/inputdev/keyboard-input).</span><span class="sxs-lookup"><span data-stu-id="b14c5-142">For more information about virtual keys, see [Keyboard Input](/windows/desktop/inputdev/keyboard-input).</span></span>

<span data-ttu-id="b14c5-143">Uma tecla ASCII é especificada colocando o caractere ASCII entre aspas duplas ou usando o valor inteiro do caractere em combinação com o sinalizador ASCII.</span><span class="sxs-lookup"><span data-stu-id="b14c5-143">An ASCII keystroke is specified either by enclosing the ASCII character in double quotation marks or by using the integer value of the character in combination with the ASCII flag.</span></span> <span data-ttu-id="b14c5-144">Os exemplos a seguir mostram como definir aceleradores ASCII.</span><span class="sxs-lookup"><span data-stu-id="b14c5-144">The following examples show how to define ASCII accelerators.</span></span>

``` syntax
"A", ID_ACCEL1         ; SHIFT+A 
65,  ID_ACCEL2, ASCII  ; SHIFT+A 
```

<span data-ttu-id="b14c5-145">Um pressionamento de tecla de código de chave virtual é especificado de forma diferente, dependendo se a tecla de pressionamento é uma chave alfanumérica ou não alfanumérica.</span><span class="sxs-lookup"><span data-stu-id="b14c5-145">A virtual-key code keystroke is specified differently depending on whether the keystroke is an alphanumeric key or a non-alphanumeric key.</span></span> <span data-ttu-id="b14c5-146">Para uma chave alfanumérica, a letra ou o número da chave, entre aspas duplas, é combinado com o sinalizador **VIRTKEY** .</span><span class="sxs-lookup"><span data-stu-id="b14c5-146">For an alphanumeric key, the key's letter or number, enclosed in double quotation marks, is combined with the **VIRTKEY** flag.</span></span> <span data-ttu-id="b14c5-147">Para uma chave não alfanumérica, o código de chave virtual para a chave específica é combinado com o sinalizador **VIRTKEY** .</span><span class="sxs-lookup"><span data-stu-id="b14c5-147">For a non-alphanumeric key, the virtual-key code for the specific key is combined with the **VIRTKEY** flag.</span></span> <span data-ttu-id="b14c5-148">Os exemplos a seguir mostram como definir aceleradores de código de chave virtual.</span><span class="sxs-lookup"><span data-stu-id="b14c5-148">The following examples show how to define virtual-key code accelerators.</span></span>

``` syntax
"a",       ID_ACCEL3, VIRTKEY   ; A (caps-lock on) or a 
VK_INSERT, ID_ACCEL4, VIRTKEY   ; INSERT key 
```

<span data-ttu-id="b14c5-149">O exemplo a seguir mostra um recurso de tabela de aceleração que define aceleradores para operações de arquivo.</span><span class="sxs-lookup"><span data-stu-id="b14c5-149">The following example shows an accelerator-table resource that defines accelerators for file operations.</span></span> <span data-ttu-id="b14c5-150">O nome do recurso é *FileAccel*.</span><span class="sxs-lookup"><span data-stu-id="b14c5-150">The name of the resource is *FileAccel*.</span></span>

``` syntax
FileAccel ACCELERATORS 
BEGIN 
    VK_F12, IDM_OPEN, CONTROL, VIRTKEY  ; CTRL+F12 
    VK_F4,  IDM_CLOSE, ALT, VIRTKEY     ; ALT+F4 
    VK_F12, IDM_SAVE, SHIFT, VIRTKEY    ; SHIFT+F12 
    VK_F12, IDM_SAVEAS, VIRTKEY         ; F12 
END 
```

<span data-ttu-id="b14c5-151">Se você quiser que o usuário pressione as teclas ALT, SHIFT ou CTRL em alguma combinação com o pressionamento de teclas do acelerador, especifique os sinalizadores ALT, SHIFT e CONTROL na definição do acelerador.</span><span class="sxs-lookup"><span data-stu-id="b14c5-151">If you want the user to press the ALT, SHIFT, or CTRL keys in some combination with the accelerator keystroke, specify the ALT, SHIFT, and CONTROL flags in the accelerator's definition.</span></span> <span data-ttu-id="b14c5-152">Estes são alguns exemplos:</span><span class="sxs-lookup"><span data-stu-id="b14c5-152">Following are some examples.</span></span>

``` syntax
"B",   ID_ACCEL5, ALT                   ; ALT_SHIFT+B 
"I",   ID_ACCEL6, CONTROL, VIRTKEY      ; CTRL+I 
VK_F5, ID_ACCEL7, CONTROL, ALT, VIRTKEY ; CTRL+ALT+F5 
```

<span data-ttu-id="b14c5-153">Por padrão, quando uma chave de acelerador corresponde a um item de menu, o sistema realça o item de menu.</span><span class="sxs-lookup"><span data-stu-id="b14c5-153">By default, when an accelerator key corresponds to a menu item, the system highlights the menu item.</span></span> <span data-ttu-id="b14c5-154">Você pode usar o sinalizador **inverter** para evitar o realce de um acelerador individual.</span><span class="sxs-lookup"><span data-stu-id="b14c5-154">You can use the **NOINVERT** flag to prevent highlighting for an individual accelerator.</span></span> <span data-ttu-id="b14c5-155">O exemplo a seguir mostra como usar o sinalizador **Invert** :</span><span class="sxs-lookup"><span data-stu-id="b14c5-155">The following example shows how to use the **NOINVERT** flag:</span></span>

``` syntax
VK_DELETE, ID_ACCEL8, VIRTKEY, SHIFT, NOINVERT  ; SHIFT+DELETE 
```

<span data-ttu-id="b14c5-156">Para definir os aceleradores que correspondem aos itens de menu em seu aplicativo, inclua os aceleradores no texto dos itens de menu.</span><span class="sxs-lookup"><span data-stu-id="b14c5-156">To define accelerators that correspond to menu items in your application, include the accelerators in the text of the menu items.</span></span> <span data-ttu-id="b14c5-157">O exemplo a seguir mostra como incluir aceleradores no texto do item de menu em um arquivo de definição de recurso.</span><span class="sxs-lookup"><span data-stu-id="b14c5-157">The following example shows how to include accelerators in menu-item text in a resource-definition file.</span></span>

``` syntax
FilePopup MENU 
BEGIN 
    POPUP   "&File" 
    BEGIN 
        MENUITEM    "&New..",           IDM_NEW 
        MENUITEM    "&Open\tCtrl+F12",  IDM_OPEN 
        MENUITEM    "&Close\tAlt+F4"    IDM_CLOSE 
        MENUITEM    "&Save\tShift+F12", IDM_SAVE 
        MENUITEM    "Save &As...\tF12", IDM_SAVEAS 
    END 
END 
```

### <a name="loading-the-accelerator-table-resource"></a><span data-ttu-id="b14c5-158">Carregando o recurso de tabela de acelerador</span><span class="sxs-lookup"><span data-stu-id="b14c5-158">Loading the Accelerator Table Resource</span></span>

<span data-ttu-id="b14c5-159">Um aplicativo carrega um recurso de tabela de aceleração chamando a função [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) e especificando o identificador de instância para o aplicativo cujo arquivo executável contém o recurso e o nome ou identificador do recurso.</span><span class="sxs-lookup"><span data-stu-id="b14c5-159">An application loads an accelerator-table resource by calling the [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) function and specifying the instance handle to the application whose executable file contains the resource and the name or identifier of the resource.</span></span> <span data-ttu-id="b14c5-160">O **LoadAccelerators** carrega a tabela de acelerador especificada na memória e retorna o identificador para a tabela de acelerador.</span><span class="sxs-lookup"><span data-stu-id="b14c5-160">**LoadAccelerators** loads the specified accelerator table into memory and returns the handle to the accelerator table.</span></span>

<span data-ttu-id="b14c5-161">Um aplicativo pode carregar um recurso de tabela de aceleração a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="b14c5-161">An application can load an accelerator-table resource at any time.</span></span> <span data-ttu-id="b14c5-162">Normalmente, um aplicativo de thread único carrega sua tabela de acelerador antes de inserir seu loop de mensagem principal.</span><span class="sxs-lookup"><span data-stu-id="b14c5-162">Usually, a single-threaded application loads its accelerator table before entering its main message loop.</span></span> <span data-ttu-id="b14c5-163">Um aplicativo que usa vários threads normalmente carrega o recurso de tabela de aceleração para um thread antes de inserir o loop de mensagem para o thread.</span><span class="sxs-lookup"><span data-stu-id="b14c5-163">An application that uses multiple threads typically loads the accelerator-table resource for a thread before entering the message loop for the thread.</span></span> <span data-ttu-id="b14c5-164">Um aplicativo ou thread também pode usar várias tabelas de acelerador, cada uma associada a uma janela específica no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b14c5-164">An application or thread might also use multiple accelerator tables, each associated with a particular window in the application.</span></span> <span data-ttu-id="b14c5-165">Esse aplicativo carregaria a tabela de acelerador para a janela cada vez que o usuário ativou a janela.</span><span class="sxs-lookup"><span data-stu-id="b14c5-165">Such an application would load the accelerator table for the window each time the user activated the window.</span></span> <span data-ttu-id="b14c5-166">Para obter mais informações sobre threads, consulte [processos e threads](/windows/desktop/ProcThread/processes-and-threads).</span><span class="sxs-lookup"><span data-stu-id="b14c5-166">For more information about threads, see [Processes and Threads](/windows/desktop/ProcThread/processes-and-threads).</span></span>

### <a name="calling-the-translate-accelerator-function"></a><span data-ttu-id="b14c5-167">Chamando a função acelerador de conversão</span><span class="sxs-lookup"><span data-stu-id="b14c5-167">Calling the Translate Accelerator Function</span></span>

<span data-ttu-id="b14c5-168">Para os aceleradores de processo, o loop de mensagem de um aplicativo (ou de thread) deve conter uma chamada para a função [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) .</span><span class="sxs-lookup"><span data-stu-id="b14c5-168">To process accelerators, an application's (or thread's) message loop must contain a call to the [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) function.</span></span> <span data-ttu-id="b14c5-169">**TranslateAccelerator** compara pressionamentos de teclas em uma tabela de acelerador e, se encontrar uma correspondência, converte os pressionamentos de tecla em uma mensagem de [**\_ comando do WM**](wm-command.md) (ou [**WM \_ SYSCOMMAND**](wm-syscommand.md)).</span><span class="sxs-lookup"><span data-stu-id="b14c5-169">**TranslateAccelerator** compares keystrokes to an accelerator table and, if it finds a match, translates the keystrokes into a [**WM\_COMMAND**](wm-command.md) (or [**WM\_SYSCOMMAND**](wm-syscommand.md)) message.</span></span> <span data-ttu-id="b14c5-170">Em seguida, a função envia a mensagem a um procedimento de janela.</span><span class="sxs-lookup"><span data-stu-id="b14c5-170">The function then sends the message to a window procedure.</span></span> <span data-ttu-id="b14c5-171">Os parâmetros da função **TranslateAccelerator** incluem o identificador para a janela que deve receber as mensagens de **\_ comando do WM** , o identificador para a tabela de acelerador usada para converter Aceleradores e um ponteiro para uma estrutura de [**msg**](/windows/win32/api/winuser/ns-winuser-msg) que contém uma mensagem da fila.</span><span class="sxs-lookup"><span data-stu-id="b14c5-171">The parameters of the **TranslateAccelerator** function include the handle to the window that is to receive the **WM\_COMMAND** messages, the handle to the accelerator table used to translate accelerators, and a pointer to an [**MSG**](/windows/win32/api/winuser/ns-winuser-msg) structure containing a message from the queue.</span></span> <span data-ttu-id="b14c5-172">O exemplo a seguir mostra como chamar **TranslateAccelerator** de dentro de um loop de mensagem.</span><span class="sxs-lookup"><span data-stu-id="b14c5-172">The following example shows how to call **TranslateAccelerator** from within a message loop.</span></span>


```
MSG msg;
BOOL bRet;

while ( (bRet = GetMessage(&msg, (HWND) NULL, 0, 0)) != 0)
{
    if (bRet == -1) 
    {
        // handle the error and possibly exit
    }
    else
    { 
        // Check for accelerator keystrokes. 
     
        if (!TranslateAccelerator( 
                hwndMain,      // handle to receiving window 
                haccel,        // handle to active accelerator table 
                &msg))         // message data 
        {
            TranslateMessage(&msg); 
            DispatchMessage(&msg); 
        } 
    } 
}
```



### <a name="processing-wm_command-messages"></a><span data-ttu-id="b14c5-173">Processando \_ mensagens de comando do WM</span><span class="sxs-lookup"><span data-stu-id="b14c5-173">Processing WM\_COMMAND Messages</span></span>

<span data-ttu-id="b14c5-174">Quando um acelerador é usado, a janela especificada na função [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) recebe um [**\_ comando do WM**](wm-command.md) ou uma mensagem do [**WM \_ SYSCOMMAND**](wm-syscommand.md) .</span><span class="sxs-lookup"><span data-stu-id="b14c5-174">When an accelerator is used, the window specified in the [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) function receives a [**WM\_COMMAND**](wm-command.md) or [**WM\_SYSCOMMAND**](wm-syscommand.md) message.</span></span> <span data-ttu-id="b14c5-175">A palavra de ordem inferior do parâmetro *wParam* contém o identificador do acelerador.</span><span class="sxs-lookup"><span data-stu-id="b14c5-175">The low-order word of the *wParam* parameter contains the identifier of the accelerator.</span></span> <span data-ttu-id="b14c5-176">O procedimento de janela examina o identificador para determinar a origem da mensagem **de \_ comando do WM** e processa a mensagem de acordo.</span><span class="sxs-lookup"><span data-stu-id="b14c5-176">The window procedure examines the identifier to determine the source of the **WM\_COMMAND** message and process the message accordingly.</span></span>

<span data-ttu-id="b14c5-177">Normalmente, se um acelerador corresponder a um item de menu no aplicativo, o acelerador e o item de menu serão atribuídos ao mesmo identificador.</span><span class="sxs-lookup"><span data-stu-id="b14c5-177">Typically, if an accelerator corresponds to a menu item in the application, the accelerator and menu item are assigned the same identifier.</span></span> <span data-ttu-id="b14c5-178">Se você precisar saber se uma mensagem [**de \_ comando do WM**](wm-command.md) foi gerada por um acelerador ou por um item de menu, poderá examinar a palavra de ordem superior do parâmetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="b14c5-178">If you need to know whether a [**WM\_COMMAND**](wm-command.md) message was generated by an accelerator or by a menu item, you can examine the high-order word of the *wParam* parameter.</span></span> <span data-ttu-id="b14c5-179">Se um acelerador gerar a mensagem, a palavra de ordem superior será 1; se um item de menu gerou a mensagem, a palavra de ordem superior será 0.</span><span class="sxs-lookup"><span data-stu-id="b14c5-179">If an accelerator generated the message, the high-order word is 1; if a menu item generated the message, the high-order word is 0.</span></span>

### <a name="destroying-the-accelerator-table-resource"></a><span data-ttu-id="b14c5-180">Destruindo o recurso de tabela de acelerador</span><span class="sxs-lookup"><span data-stu-id="b14c5-180">Destroying the Accelerator Table Resource</span></span>

<span data-ttu-id="b14c5-181">O sistema destrói automaticamente os recursos da tabela de aceleradores carregados pela função [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) , removendo o recurso da memória depois que o aplicativo é fechado.</span><span class="sxs-lookup"><span data-stu-id="b14c5-181">The system automatically destroys accelerator-table resources loaded by the [**LoadAccelerators**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) function, removing the resource from memory after the application closes.</span></span>

### <a name="creating-accelerators-for-font-attributes"></a><span data-ttu-id="b14c5-182">Criando aceleradores para atributos de fonte</span><span class="sxs-lookup"><span data-stu-id="b14c5-182">Creating Accelerators for Font Attributes</span></span>

<span data-ttu-id="b14c5-183">O exemplo nesta seção mostra como executar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="b14c5-183">The example in this section shows how to perform the following tasks:</span></span>

-   <span data-ttu-id="b14c5-184">Crie um recurso de tabela de aceleração.</span><span class="sxs-lookup"><span data-stu-id="b14c5-184">Create an accelerator-table resource.</span></span>
-   <span data-ttu-id="b14c5-185">Carregue a tabela do acelerador em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="b14c5-185">Load the accelerator table at run time.</span></span>
-   <span data-ttu-id="b14c5-186">Converter aceleradores em um loop de mensagem.</span><span class="sxs-lookup"><span data-stu-id="b14c5-186">Translate accelerators in a message loop.</span></span>
-   <span data-ttu-id="b14c5-187">Processar mensagens de [**\_ comando do WM**](wm-command.md) geradas pelos aceleradores.</span><span class="sxs-lookup"><span data-stu-id="b14c5-187">Process [**WM\_COMMAND**](wm-command.md) messages generated by the accelerators.</span></span>

<span data-ttu-id="b14c5-188">Essas tarefas são demonstradas no contexto de um aplicativo que inclui um menu de **caracteres** e aceleradores correspondentes que permitem ao usuário selecionar atributos da fonte atual.</span><span class="sxs-lookup"><span data-stu-id="b14c5-188">These tasks are demonstrated in the context of an application that includes a **Character** menu and corresponding accelerators that allow the user to select attributes of the current font.</span></span>

<span data-ttu-id="b14c5-189">A seguinte parte de um arquivo de definição de recurso define o menu de **caracteres** e a tabela de acelerador associada.</span><span class="sxs-lookup"><span data-stu-id="b14c5-189">The following portion of a resource-definition file defines the **Character** menu and the associated accelerator table.</span></span> <span data-ttu-id="b14c5-190">Observe que os itens de menu mostram os pressionamentos de teclas do acelerador e que cada acelerador tem o mesmo identificador de seu item de menu associado.</span><span class="sxs-lookup"><span data-stu-id="b14c5-190">Note that the menu items show the accelerator keystrokes and that each accelerator has the same identifier as its associated menu item.</span></span>


```
#include <windows.h> 
#include "acc.h" 
 
MainMenu MENU 
{ 
    POPUP   "&Character" 
    { 
        MENUITEM    "&Regular\tF5",         IDM_REGULAR 
        MENUITEM    "&Bold\tCtrl+B",        IDM_BOLD 
        MENUITEM    "&Italic\tCtrl+I",      IDM_ITALIC 
        MENUITEM    "&Underline\tCtrl+U",   IDM_ULINE 
    }
} 
 
FontAccel ACCELERATORS 
{ 
    VK_F5,  IDM_REGULAR,    VIRTKEY 
    "B",    IDM_BOLD,       CONTROL, VIRTKEY 
    "I",    IDM_ITALIC,     CONTROL, VIRTKEY 
    "U",    IDM_ULINE,      CONTROL, VIRTKEY 
}
 
```



<span data-ttu-id="b14c5-191">As seções a seguir do arquivo de origem do aplicativo mostram como implementar os aceleradores.</span><span class="sxs-lookup"><span data-stu-id="b14c5-191">The following sections from the application's source file show how to implement the accelerators.</span></span>


```
HWND hwndMain;      // handle to main window 
HANDLE hinstAcc;    // handle to application instance 
int WINAPI WinMain(HINSTANCE hinst, HINSTANCE hinstPrev, LPSTR lpCmdLine, int nCmdShow) 
{ 
    MSG msg;            // application messages 
    BOOL bRet;          // for return value of GetMessage
    HACCEL haccel;      // handle to accelerator table 
 
    // Perform the initialization procedure. 
 
    // Create a main window for this application instance. 
 
    hwndMain = CreateWindowEx(0L, "MainWindowClass", 
        "Sample Application", WS_OVERLAPPEDWINDOW, CW_USEDEFAULT, 
        CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, NULL, NULL, 
        hinst, NULL ); 
 
    // If a window cannot be created, return "failure." 
 
    if (!hwndMain) 
        return FALSE; 
 
    // Make the window visible and update its client area. 
 
    ShowWindow(hwndMain, nCmdShow); 
    UpdateWindow(hwndMain); 
 
    // Load the accelerator table. 
 
    haccel = LoadAccelerators(hinstAcc, "FontAccel"); 
    if (haccel == NULL) 
        HandleAccelErr(ERR_LOADING);     // application defined 
 
    // Get and dispatch messages until a WM_QUIT message is 
    // received. 
 
    while ((bRet = GetMessage(&msg, NULL, 0, 0)) != 0)
    {
        if (bRet == -1)
        {
            // handle the error and possibly exit
        }
        else
        { 
            // Check for accelerator keystrokes. 
     
            if (!TranslateAccelerator( 
                    hwndMain,  // handle to receiving window 
                    haccel,    // handle to active accelerator table 
                    &msg))         // message data 
            {
                TranslateMessage(&msg); 
                DispatchMessage(&msg); 
            } 
        } 
    }
    return msg.wParam; 
} 
 
LRESULT APIENTRY MainWndProc(HWND hwndMain, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    BYTE fbFontAttrib;        // array of font-attribute flags 
    static HMENU hmenu;       // handle to main menu 
 
    switch (uMsg) 
    { 
        case WM_CREATE: 
 
            // Add a check mark to the Regular menu item to 
            // indicate that it is the default. 
 
            hmenu = GetMenu(hwndMain); 
            CheckMenuItem(hmenu, IDM_REGULAR, MF_BYCOMMAND | 
                MF_CHECKED); 
            return 0; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                // Process the accelerator and menu commands. 
 
                case IDM_REGULAR: 
                case IDM_BOLD: 
                case IDM_ITALIC: 
                case IDM_ULINE: 
 
                    // GetFontAttributes is an application-defined 
                    // function that sets the menu-item check marks 
                    // and returns the user-selected font attributes. 
 
                    fbFontAttrib = GetFontAttributes( 
                        (BYTE) LOWORD(wParam), hmenu); 
 
                    // SetFontAttributes is an application-defined 
                    // function that creates a font with the 
                    // user-specified attributes the font with 
                    // the main window's device context. 
 
                    SetFontAttributes(fbFontAttrib); 
                    break; 
 
                default: 
                    break; 
            } 
            break; 
 
            // Process other messages. 
 
        default: 
            return DefWindowProc(hwndMain, uMsg, wParam, lParam); 
    } 
    return NULL; 
}
```



## <a name="using-an-accelerator-table-created-at-run-time"></a><span data-ttu-id="b14c5-192">Usando uma tabela de acelerador criada em tempo de execução</span><span class="sxs-lookup"><span data-stu-id="b14c5-192">Using an Accelerator Table Created at Run Time</span></span>

<span data-ttu-id="b14c5-193">Este tópico discute como usar tabelas de acelerador criadas em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="b14c5-193">This topic discusses how to use accelerator tables created at run time.</span></span>

-   [<span data-ttu-id="b14c5-194">Criando uma tabela de acelerador de Run-Time</span><span class="sxs-lookup"><span data-stu-id="b14c5-194">Creating a Run-Time Accelerator Table</span></span>](#creating-a-run-time-accelerator-table)
-   [<span data-ttu-id="b14c5-195">Aceleradores de processamento</span><span class="sxs-lookup"><span data-stu-id="b14c5-195">Processing Accelerators</span></span>](#processing-accelerators)
-   [<span data-ttu-id="b14c5-196">Destruindo uma tabela de acelerador de Run-Time</span><span class="sxs-lookup"><span data-stu-id="b14c5-196">Destroying a Run-Time Accelerator Table</span></span>](#destroying-a-run-time-accelerator-table)
-   [<span data-ttu-id="b14c5-197">Criando aceleradores editáveis do usuário</span><span class="sxs-lookup"><span data-stu-id="b14c5-197">Creating User Editable Accelerators</span></span>](#creating-user-editable-accelerators)

### <a name="creating-a-run-time-accelerator-table"></a><span data-ttu-id="b14c5-198">Criando uma tabela de acelerador de Run-Time</span><span class="sxs-lookup"><span data-stu-id="b14c5-198">Creating a Run-Time Accelerator Table</span></span>

<span data-ttu-id="b14c5-199">A primeira etapa na criação de uma tabela aceleradora em tempo de execução está preenchendo uma matriz de estruturas [**da aceleração extra**](/windows/win32/api/winuser/ns-winuser-accel) .</span><span class="sxs-lookup"><span data-stu-id="b14c5-199">The first step in creating an accelerator table at run time is filling an array of [**ACCEL**](/windows/win32/api/winuser/ns-winuser-accel) structures.</span></span> <span data-ttu-id="b14c5-200">Cada estrutura na matriz define um acelerador na tabela.</span><span class="sxs-lookup"><span data-stu-id="b14c5-200">Each structure in the array defines an accelerator in the table.</span></span> <span data-ttu-id="b14c5-201">A definição de um acelerador inclui seus sinalizadores, sua chave e seu identificador.</span><span class="sxs-lookup"><span data-stu-id="b14c5-201">An accelerator's definition includes its flags, its key, and its identifier.</span></span> <span data-ttu-id="b14c5-202">A estrutura **da aceleração extra** tem o seguinte formato.</span><span class="sxs-lookup"><span data-stu-id="b14c5-202">The **ACCEL** structure has the following form.</span></span>

``` syntax
typedef struct tagACCEL { // accl 
    BYTE   fVirt; 
    WORD   key; 
    WORD   cmd; 
} ACCEL;
```

<span data-ttu-id="b14c5-203">Você define um pressionamento de teclas do acelerador especificando um código de caractere ASCII ou um código de chave virtual no membro de **chave** da estrutura [**da aceleração extra**](/windows/win32/api/winuser/ns-winuser-accel) .</span><span class="sxs-lookup"><span data-stu-id="b14c5-203">You define an accelerator's keystroke by specifying an ASCII character code or a virtual-key code in the **key** member of the [**ACCEL**](/windows/win32/api/winuser/ns-winuser-accel) structure.</span></span> <span data-ttu-id="b14c5-204">Se você especificar um código de chave virtual, deverá primeiro incluir o sinalizador **FVIRTKEY** no membro **fVirt** ; caso contrário, o sistema interpretará o código como um código de caractere ASCII.</span><span class="sxs-lookup"><span data-stu-id="b14c5-204">If you specify a virtual-key code, you must first include the **FVIRTKEY** flag in the **fVirt** member; otherwise, the system interprets the code as an ASCII character code.</span></span> <span data-ttu-id="b14c5-205">Você pode incluir o sinalizador **FCONTROL**, **FALT** ou **FSHIFT** , ou todos os três, para combinar a tecla CTRL, ALT ou Shift com o pressionamento de teclas.</span><span class="sxs-lookup"><span data-stu-id="b14c5-205">You can include the **FCONTROL**, **FALT**, or **FSHIFT** flag, or all three, to combine the CTRL, ALT, or SHIFT key with the keystroke.</span></span>

<span data-ttu-id="b14c5-206">Para criar a tabela de acelerador, passe um ponteiro para a matriz de estruturas [**da aceleração extra**](/windows/win32/api/winuser/ns-winuser-accel) para a função [**CreateAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea) .</span><span class="sxs-lookup"><span data-stu-id="b14c5-206">To create the accelerator table, pass a pointer to the array of [**ACCEL**](/windows/win32/api/winuser/ns-winuser-accel) structures to the [**CreateAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-createacceleratortablea) function.</span></span> <span data-ttu-id="b14c5-207">**CreateAcceleratorTable** cria a tabela de acelerador e retorna o identificador para a tabela.</span><span class="sxs-lookup"><span data-stu-id="b14c5-207">**CreateAcceleratorTable** creates the accelerator table and returns the handle to the table.</span></span>

### <a name="processing-accelerators"></a><span data-ttu-id="b14c5-208">Aceleradores de processamento</span><span class="sxs-lookup"><span data-stu-id="b14c5-208">Processing Accelerators</span></span>

<span data-ttu-id="b14c5-209">O processo de carregar e chamar aceleradores fornecidos por uma tabela de acelerador criada em tempo de execução é o mesmo que processar os fornecidos por um recurso de tabela de aceleração.</span><span class="sxs-lookup"><span data-stu-id="b14c5-209">The process of loading and calling accelerators provided by an accelerator table created at run time is the same as processing those provided by an accelerator-table resource.</span></span> <span data-ttu-id="b14c5-210">Para obter mais informações, consulte [carregando o recurso de tabela de acelerador](#loading-the-accelerator-table-resource) por meio do [processamento de mensagens de \_ comando do WM](/windows).</span><span class="sxs-lookup"><span data-stu-id="b14c5-210">For more information, see [Loading the Accelerator Table Resource](#loading-the-accelerator-table-resource) through [Processing WM\_COMMAND Messages](/windows).</span></span>

### <a name="destroying-a-run-time-accelerator-table"></a><span data-ttu-id="b14c5-211">Destruindo uma tabela de acelerador de Run-Time</span><span class="sxs-lookup"><span data-stu-id="b14c5-211">Destroying a Run-Time Accelerator Table</span></span>

<span data-ttu-id="b14c5-212">O sistema destrói automaticamente as tabelas aceleradoras criadas em tempo de execução, removendo os recursos da memória depois que o aplicativo é fechado.</span><span class="sxs-lookup"><span data-stu-id="b14c5-212">The system automatically destroys accelerator tables created at run time, removing the resources from memory after the application closes.</span></span> <span data-ttu-id="b14c5-213">Você pode destruir uma tabela de acelerador e removê-la da memória anteriormente passando o identificador da tabela para a função [**DestroyAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-destroyacceleratortable) .</span><span class="sxs-lookup"><span data-stu-id="b14c5-213">You can destroy an accelerator table and remove it from memory earlier by passing the table's handle to the [**DestroyAcceleratorTable**](/windows/desktop/api/Winuser/nf-winuser-destroyacceleratortable) function.</span></span>

### <a name="creating-user-editable-accelerators"></a><span data-ttu-id="b14c5-214">Criando aceleradores editáveis do usuário</span><span class="sxs-lookup"><span data-stu-id="b14c5-214">Creating User Editable Accelerators</span></span>

<span data-ttu-id="b14c5-215">Este exemplo mostra como construir uma caixa de diálogo que permite ao usuário alterar o acelerador associado a um item de menu.</span><span class="sxs-lookup"><span data-stu-id="b14c5-215">This example shows how to construct a dialog box that allows the user to change the accelerator associated with a menu item.</span></span> <span data-ttu-id="b14c5-216">A caixa de diálogo consiste em uma caixa de combinação que contém itens de menu, uma caixa de combinação que contém os nomes das chaves e as caixas de seleção para selecionar as teclas CTRL, ALT e SHIFT.</span><span class="sxs-lookup"><span data-stu-id="b14c5-216">The dialog box consists of a combo box containing menu items, a combo box containing the names of keys, and check boxes for selecting the CTRL, ALT, and SHIFT keys.</span></span> <span data-ttu-id="b14c5-217">A ilustração a seguir mostra a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b14c5-217">The following illustration shows the dialog box.</span></span>

![caixa de diálogo com caixas de combinação e caixas de seleção](images/useredit.gif)

<span data-ttu-id="b14c5-219">O exemplo a seguir mostra como a caixa de diálogo é definida no arquivo de definição de recurso.</span><span class="sxs-lookup"><span data-stu-id="b14c5-219">The following example shows how the dialog box is defined in the resource-definition file.</span></span>

``` syntax
EdAccelBox DIALOG 5, 17, 193, 114 
STYLE DS_MODALFRAME | WS_POPUP | WS_VISIBLE | WS_CAPTION 
CAPTION "Edit Accelerators" 
BEGIN 
    COMBOBOX        IDD_MENUITEMS, 10, 22, 52, 53, 
                        CBS_SIMPLE | CBS_SORT | WS_VSCROLL | 
                        WS_TABSTOP 
    CONTROL         "Control", IDD_CNTRL, "Button", 
                        BS_AUTOCHECKBOX | WS_TABSTOP, 
                        76, 35, 40, 10 
    CONTROL         "Alt", IDD_ALT, "Button", 
                        BS_AUTOCHECKBOX | WS_TABSTOP, 
                        76, 48, 40, 10 
    CONTROL         "Shift", IDD_SHIFT, "Button", 
                        BS_AUTOCHECKBOX | WS_TABSTOP, 
                        76, 61, 40, 10 
    COMBOBOX        IDD_KEYSTROKES, 124, 22, 58, 58, 
                        CBS_SIMPLE | CBS_SORT | WS_VSCROLL | 
                        WS_TABSTOP 
    PUSHBUTTON      "Ok", IDOK, 43, 92, 40, 14 
    PUSHBUTTON      "Cancel", IDCANCEL, 103, 92, 40, 14 
    LTEXT           "Select Item:", 101, 10, 12, 43, 8 
    LTEXT           "Select Keystroke:", 102, 123, 12, 60, 8 
END
```

<span data-ttu-id="b14c5-220">A barra de menus do aplicativo contém um submenu de **caracteres** cujos itens têm aceleradores associados a eles.</span><span class="sxs-lookup"><span data-stu-id="b14c5-220">The application's menu bar contains a **Character** submenu whose items have accelerators associated with them.</span></span>

``` syntax
MainMenu MENU 
{ 
    POPUP "&Character" 
    { 
        MENUITEM    "&Regular\tF5",         IDM_REGULAR 
        MENUITEM    "&Bold\tCtrl+B",        IDM_BOLD 
        MENUITEM    "&Italic\tCtrl+I",      IDM_ITALIC 
        MENUITEM    "&Underline\tCtrl+U",   IDM_ULINE 
    }
} 
 
FontAccel ACCELERATORS 
{ 
    VK_F5,  IDM_REGULAR,    VIRTKEY 
    "B",    IDM_BOLD,       CONTROL, VIRTKEY 
    "I",    IDM_ITALIC,     CONTROL, VIRTKEY 
    "U",    IDM_ULINE,      CONTROL, VIRTKEY 
}
 
```

<span data-ttu-id="b14c5-221">Os valores de item de menu para o modelo de menu são constantes definidas da seguinte maneira no arquivo de cabeçalho do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b14c5-221">The menu item values for the menu template are constants defined as follows in the application's header file.</span></span>

``` syntax
#define IDM_REGULAR    1100
#define IDM_BOLD       1200
#define IDM_ITALIC     1300
#define IDM_ULINE      1400
```

<span data-ttu-id="b14c5-222">A caixa de diálogo usa uma matriz de estruturas VKEY definidas pelo aplicativo, cada uma contendo uma cadeia de caracteres de texto de pressionamento de tecla e uma cadeia de texto de acelerador.</span><span class="sxs-lookup"><span data-stu-id="b14c5-222">The dialog box uses an array of application-defined VKEY structures, each containing a keystroke-text string and an accelerator-text string.</span></span> <span data-ttu-id="b14c5-223">Quando a caixa de diálogo é criada, ela analisa a matriz e adiciona cada cadeia de caracteres de texto de pressionamento de tecla à caixa de combinação **selecionar pressionamentos** de teclas.</span><span class="sxs-lookup"><span data-stu-id="b14c5-223">When the dialog box is created, it parses the array and adds each keystroke-text string to the **Select Keystroke** combo box.</span></span> <span data-ttu-id="b14c5-224">Quando o usuário clica no botão **OK** , a caixa de diálogo procura a cadeia de caracteres de texto de pressionamento de teclas selecionada e recupera a cadeia de caracteres de texto de acelerador correspondente.</span><span class="sxs-lookup"><span data-stu-id="b14c5-224">When the user clicks the **OK** button, the dialog box looks up the selected keystroke-text string and retrieves the corresponding accelerator-text string.</span></span> <span data-ttu-id="b14c5-225">A caixa de diálogo acrescenta a cadeia de texto Accelerator-Text ao texto do item de menu selecionado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="b14c5-225">The dialog box appends the accelerator-text string to the text of the menu item that the user selected.</span></span> <span data-ttu-id="b14c5-226">O exemplo a seguir mostra a matriz de estruturas VKEY:</span><span class="sxs-lookup"><span data-stu-id="b14c5-226">The following example shows the array of VKEY structures:</span></span>


```
// VKey Lookup Support 
 
#define MAXKEYS 25 
 
typedef struct _VKEYS { 
    char *pKeyName; 
    char *pKeyString; 
} VKEYS; 
 
VKEYS vkeys[MAXKEYS] = { 
    "BkSp",     "Back Space", 
    "PgUp",     "Page Up", 
    "PgDn",     "Page Down", 
    "End",      "End", 
    "Home",     "Home", 
    "Lft",      "Left", 
    "Up",       "Up", 
    "Rgt",      "Right", 
    "Dn",       "Down", 
    "Ins",      "Insert", 
    "Del",      "Delete", 
    "Mult",     "Multiply", 
    "Add",      "Add", 
    "Sub",      "Subtract", 
    "DecPt",    "Decimal Point", 
    "Div",      "Divide", 
    "F2",       "F2", 
    "F3",       "F3", 
    "F5",       "F5", 
    "F6",       "F6", 
    "F7",       "F7", 
    "F8",       "F8", 
    "F9",       "F9", 
    "F11",      "F11", 
    "F12",      "F12" 
};
```



<span data-ttu-id="b14c5-227">O procedimento de inicialização da caixa de diálogo preenche as caixas de combinação **selecionar item** e **selecionar pressionamentos de teclas** .</span><span class="sxs-lookup"><span data-stu-id="b14c5-227">The dialog box's initialization procedure fills the **Select Item** and **Select Keystroke** combo boxes.</span></span> <span data-ttu-id="b14c5-228">Depois que o usuário seleciona um item de menu e um acelerador associado, a caixa de diálogo examina os controles na caixa de diálogo para obter a seleção do usuário, atualiza o texto do item de menu e cria uma nova tabela de acelerador que contém o novo acelerador definido pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="b14c5-228">After the user selects a menu item and associated accelerator, the dialog box examines the controls in the dialog box to get the user's selection, updates the text of the menu item, and then creates a new accelerator table that contains the user-defined new accelerator.</span></span> <span data-ttu-id="b14c5-229">O exemplo a seguir mostra o procedimento da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b14c5-229">The following example shows the dialog-box procedure.</span></span> <span data-ttu-id="b14c5-230">Observe que você deve inicializar em seu procedimento de janela.</span><span class="sxs-lookup"><span data-stu-id="b14c5-230">Note that you must initialize in your window procedure.</span></span>


```
// Global variables 
 
HWND hwndMain;      // handle to main window 
HACCEL haccel;      // handle to accelerator table 
 
// Dialog-box procedure 
 
BOOL CALLBACK EdAccelProc(HWND hwndDlg, UINT uMsg, WPARAM wParam, LPARAM lParam) 
{ 
    int nCurSel;            // index of list box item 
    UINT idItem;            // menu-item identifier 
    UINT uItemPos;          // menu-item position 
    UINT i, j = 0;          // loop counters 
    static UINT cItems;     // count of items in menu 
    char szTemp[32];        // temporary buffer 
    char szAccelText[32];   // buffer for accelerator text 
    char szKeyStroke[16];   // buffer for keystroke text 
    static char szItem[32]; // buffer for menu-item text 
    HWND hwndCtl;           // handle to control window 
    static HMENU hmenu;     // handle to "Character" menu 
    PCHAR pch, pch2;        // pointers for string copying 
    WORD wVKCode;           // accelerator virtual-key code 
    BYTE fAccelFlags;       // fVirt flags for ACCEL structure 
    LPACCEL lpaccelNew;     // pointer to new accelerator table 
    HACCEL haccelOld;       // handle to old accelerator table 
    int cAccelerators;      // number of accelerators in table 
    static BOOL fItemSelected = FALSE; // item selection flag 
    static BOOL fKeySelected = FALSE;  // key selection flag 
    HRESULT hr;
    INT numTCHAR;           // TCHARs in listbox text
 
    switch (uMsg) 
    { 
        case WM_INITDIALOG: 
 
            // Get the handle to the menu-item combo box. 
 
            hwndCtl = GetDlgItem(hwndDlg, IDD_MENUITEMS); 
 
            // Get the handle to the Character submenu and
            // count the number of items it has. In this example, 
            // the menu has position 0. You must alter this value 
            // if you add additional menus. 
            hmenu = GetSubMenu(GetMenu(hwndMain), 0); 
            cItems = GetMenuItemCount(hmenu); 
 
            // Get the text of each item, strip out the '&' and 
            // the accelerator text, and add the text to the 
            // menu-item combo box. 
 
            for (i = 0; i < cItems; i++) 
            { 
                if (!(GetMenuString(hmenu, i, szTemp, 
                        sizeof(szTemp)/sizeof(TCHAR), MF_BYPOSITION))) 
                    continue; 
                for (pch = szTemp, pch2 = szItem; *pch != '\0'; ) 
                { 
                    if (*pch != '&') 
                    { 
                        if (*pch == '\t') 
                        { 
                            *pch = '\0'; 
                            *pch2 = '\0'; 
                        } 
                        else *pch2++ = *pch++; 
                    } 
                    else pch++; 
                } 
                SendMessage(hwndCtl, CB_ADDSTRING, 0, 
                    (LONG) (LPSTR) szItem); 
            } 
 
            // Now fill the keystroke combo box with the list of 
            // keystrokes that will be allowed for accelerators. 
            // The list of keystrokes is in the application-defined 
            // structure called "vkeys". 
 
            hwndCtl = GetDlgItem(hwndDlg, IDD_KEYSTROKES); 
            for (i = 0; i < MAXKEYS; i++) 
            {
                SendMessage(hwndCtl, CB_ADDSTRING, 0, 
                    (LONG) (LPSTR) vkeys[i].pKeyString); 
            }
 
            return TRUE; 
 
        case WM_COMMAND: 
            switch (LOWORD(wParam)) 
            { 
                case IDD_MENUITEMS: 
 
                    // The user must select an item from the combo 
                    // box. This flag is checked during IDOK
                    // processing to be sure a selection was made. 
 
                    fItemSelected = TRUE; 
                    return 0; 
 
                case IDD_KEYSTROKES: 
 
                    // The user must select an item from the combo
                    // box. This flag is checked during IDOK
                    // processing to be sure a selection was made. 
 
                    fKeySelected = TRUE; 
 
                    return 0; 
 
                case IDOK: 
 
                    // If the user has not selected a menu item 
                    // and a keystroke, display a reminder in a 
                    // message box. 
 
                    if (!fItemSelected || !fKeySelected) 
                    { 
                        MessageBox(hwndDlg, 
                            "Item or key not selected.", NULL, 
                            MB_OK); 
                        return 0; 
                    } 
 
                    // Determine whether the CTRL, ALT, and SHIFT 
                    // keys are selected. Concatenate the 
                    // appropriate strings to the accelerator- 
                    // text buffer, and set the appropriate 
                    // accelerator flags. 
 
                    szAccelText[0] = '\0'; 
                    hwndCtl = GetDlgItem(hwndDlg, IDD_CNTRL); 
                    if (SendMessage(hwndCtl, BM_GETCHECK, 0, 0) == 1) 
                    { 
                        hr = StringCchCat(szAccelText, 32, "Ctl+");
                        if (FAILED(hr))
                        {
                        // TODO: write error handler
                        }
                        fAccelFlags |= FCONTROL; 
                    } 
                    hwndCtl = GetDlgItem(hwndDlg, IDD_ALT); 
                    if (SendMessage(hwndCtl, BM_GETCHECK, 0, 0) == 1) 
                    { 
                        hr = StringCchCat(szAccelText, 32, "Alt+");
                        if (FAILED(hr))
                        {
                        // TODO: write error handler
                        }
                        fAccelFlags |= FALT; 
                    } 
                    hwndCtl = GetDlgItem(hwndDlg, IDD_SHIFT); 
                    if (SendMessage(hwndCtl, BM_GETCHECK, 0, 0) == 1) 
                    {
                        hr = StringCchCat(szAccelText, 32, "Shft+");
                        if (FAILED(hr))
                        {
                        // TODO: write error handler
                        }
                        fAccelFlags |= FSHIFT; 
                    } 
 
                    // Get the selected keystroke, and look up the 
                    // accelerator text and the virtual-key code 
                    // for the keystroke in the vkeys structure. 
 
                    hwndCtl = GetDlgItem(hwndDlg, IDD_KEYSTROKES); 
                    nCurSel = (int) SendMessage(hwndCtl, 
                        CB_GETCURSEL, 0, 0);
                    numTCHAR = SendMessage(hwndCtl, CB_GETLBTEXTLEN, 
                        nCursel, 0); 
                    if (numTCHAR <= 15)
                        {                   
                        SendMessage(hwndCtl, CB_GETLBTEXT, 
                            nCurSel, (LONG) (LPSTR) szKeyStroke);
                        }
                    else
                        {
                        // TODO: writer error handler
                        }
                         
                    for (i = 0; i < MAXKEYS; i++) 
                    {
                    //
                    // lstrcmp requires that both parameters are
                    // null-terminated.
                    //
                        if(lstrcmp(vkeys[i].pKeyString, szKeyStroke) 
                            == 0) 
                        { 
                            hr = StringCchCopy(szKeyStroke, 16, vkeys[i].pKeyName);
                            if (FAILED(hr))
                            {
                            // TODO: write error handler
                            }
                            break; 
                        } 
                    } 
 
                    // Concatenate the keystroke text to the 
                    // "Ctl+","Alt+", or "Shft+" string. 
 
                        hr = StringCchCat(szAccelText, 32, szKeyStroke);
                        if (FAILED(hr))
                        {
                        // TODO: write error handler
                        }
 
                    // Determine the position in the menu of the 
                    // selected menu item. Menu items in the 
                    // "Character" menu have positions 0,2,3, and 4.
                    // Note: the lstrcmp parameters must be
                    // null-terminated. 
 
                    if (lstrcmp(szItem, "Regular") == 0) 
                        uItemPos = 0; 
                    else if (lstrcmp(szItem, "Bold") == 0) 
                        uItemPos = 2; 
                    else if (lstrcmp(szItem, "Italic") == 0) 
                        uItemPos = 3; 
                    else if (lstrcmp(szItem, "Underline") == 0) 
                        uItemPos = 4; 
 
                    // Get the string that corresponds to the 
                    // selected item. 
 
                    GetMenuString(hmenu, uItemPos, szItem, 
                        sizeof(szItem)/sizeof(TCHAR), MF_BYPOSITION); 
 
                    // Append the new accelerator text to the 
                    // menu-item text. 
 
                    for (pch = szItem; *pch != '\t'; pch++); 
                        ++pch; 
 
                    for (pch2 = szAccelText; *pch2 != '\0'; pch2++) 
                        *pch++ = *pch2; 
                    *pch = '\0'; 
 
                    // Modify the menu item to reflect the new 
                    // accelerator text. 
 
                    idItem = GetMenuItemID(hmenu, uItemPos); 
                    ModifyMenu(hmenu, idItem, MF_BYCOMMAND | 
                        MF_STRING, idItem, szItem); 
 
                    // Reset the selection flags. 
 
                    fItemSelected = FALSE; 
                    fKeySelected = FALSE; 
 
                    // Save the current accelerator table. 
 
                    haccelOld = haccel; 
 
                    // Count the number of entries in the current 
                    // table, allocate a buffer for the table, and 
                    // then copy the table into the buffer. 
 
                    cAccelerators = CopyAcceleratorTable( 
                        haccelOld, NULL, 0); 
                    lpaccelNew = (LPACCEL) LocalAlloc(LPTR, 
                        cAccelerators * sizeof(ACCEL)); 
 
                    if (lpaccelNew != NULL) 
                    {
                        CopyAcceleratorTable(haccel, lpaccelNew, 
                            cAccelerators); 
                    }
 
                    // Find the accelerator that the user modified 
                    // and change its flags and virtual-key code 
                    // as appropriate. 
 
                    for (i = 0; i < (UINT) cAccelerators; i++) 
                    { 
                           if (lpaccelNew[i].cmd == (WORD) idItem)
                        {
                            lpaccelNew[i].fVirt = fAccelFlags; 
                            lpaccelNew[i].key = wVKCode; 
                        }
                    } 
 
                    // Create the new accelerator table, and 
                    // destroy the old one. 
 
                    DestroyAcceleratorTable(haccelOld); 
                    haccel = CreateAcceleratorTable(lpaccelNew, 
                        cAccelerators); 
 
                    // Destroy the dialog box. 
 
                    EndDialog(hwndDlg, TRUE); 
                    return 0; 
 
                case IDCANCEL: 
                    EndDialog(hwndDlg, TRUE); 
                    return TRUE; 
 
                default: 
                    break; 
            } 
        default: 
            break; 
    } 
    return FALSE; 
}
```



 

 