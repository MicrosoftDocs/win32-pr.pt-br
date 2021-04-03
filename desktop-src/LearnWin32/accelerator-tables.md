---
title: Tabelas do acelerador
description: .
ms.assetid: 4F2CFD7C-90D3-4C3F-9A42-05B915914EF6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9929445809bee71f273b6bd2334e182de59edbfa
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007558"
---
# <a name="accelerator-tables"></a><span data-ttu-id="36e50-103">Tabelas do acelerador</span><span class="sxs-lookup"><span data-stu-id="36e50-103">Accelerator Tables</span></span>

<span data-ttu-id="36e50-104">Os aplicativos geralmente definem atalhos de teclado, como CTRL + O para o comando File Open.</span><span class="sxs-lookup"><span data-stu-id="36e50-104">Applications often define keyboard shortcuts, such as CTRL+O for the File Open command.</span></span> <span data-ttu-id="36e50-105">Você pode implementar atalhos de teclado manipulando mensagens do [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) individuais, mas as tabelas de aceleração fornecem uma solução melhor que:</span><span class="sxs-lookup"><span data-stu-id="36e50-105">You could implement keyboard shortcuts by handling individual [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) messages, but accelerator tables provide a better solution that:</span></span>

-   <span data-ttu-id="36e50-106">Requer menos codificação.</span><span class="sxs-lookup"><span data-stu-id="36e50-106">Requires less coding.</span></span>
-   <span data-ttu-id="36e50-107">Consolida todos os seus atalhos em um arquivo de dados.</span><span class="sxs-lookup"><span data-stu-id="36e50-107">Consolidates all of your shortcuts into one data file.</span></span>
-   <span data-ttu-id="36e50-108">Dá suporte à localização em outros idiomas.</span><span class="sxs-lookup"><span data-stu-id="36e50-108">Supports localization into other languages.</span></span>
-   <span data-ttu-id="36e50-109">Permite que atalhos e comandos de menu usem a mesma lógica do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="36e50-109">Enables shortcuts and menu commands to use the same application logic.</span></span>

<span data-ttu-id="36e50-110">Uma *tabela de acelerador* é um recurso de dados que mapeia combinações de teclado, como CTRL + O, para comandos de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="36e50-110">An *accelerator table* is a data resource that maps keyboard combinations, such as CTRL+O, to application commands.</span></span> <span data-ttu-id="36e50-111">Antes de veremos como usar uma tabela de acelerador, precisaremos de uma rápida introdução aos recursos.</span><span class="sxs-lookup"><span data-stu-id="36e50-111">Before we see how to use an accelerator table, we'll need a quick introduction to resources.</span></span> <span data-ttu-id="36e50-112">Um *recurso* é um blob de dados que é compilado em um binário de aplicativo (exe ou dll).</span><span class="sxs-lookup"><span data-stu-id="36e50-112">A *resource* is a data blob that is built into an application binary (EXE or DLL).</span></span> <span data-ttu-id="36e50-113">Os recursos armazenam dados que são necessários para o aplicativo, como menus, cursores, ícones, imagens, cadeias de caracteres de texto ou qualquer dado de aplicativo personalizado.</span><span class="sxs-lookup"><span data-stu-id="36e50-113">Resources store data that are needed by the application, such as menus, cursors, icons, images, text strings, or any custom application data.</span></span> <span data-ttu-id="36e50-114">O aplicativo carrega os dados do recurso do binário em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="36e50-114">The application loads the resource data from the binary at run time.</span></span> <span data-ttu-id="36e50-115">Para incluir recursos em um binário, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="36e50-115">To include resources in a binary, do the following:</span></span>

1.  <span data-ttu-id="36e50-116">Crie um arquivo de definição de recurso (. rc).</span><span class="sxs-lookup"><span data-stu-id="36e50-116">Create a resource definition (.rc) file.</span></span> <span data-ttu-id="36e50-117">Esse arquivo define os tipos de recursos e seus identificadores.</span><span class="sxs-lookup"><span data-stu-id="36e50-117">This file defines the types of resources and their identifiers.</span></span> <span data-ttu-id="36e50-118">O arquivo de definição de recurso pode incluir referências a outros arquivos.</span><span class="sxs-lookup"><span data-stu-id="36e50-118">The resource definition file may include references to other files.</span></span> <span data-ttu-id="36e50-119">Por exemplo, um recurso de ícone é declarado no arquivo. rc, mas a imagem de ícone é armazenada em um arquivo separado.</span><span class="sxs-lookup"><span data-stu-id="36e50-119">For example, an icon resource is declared in the .rc file, but the icon image is stored in a separate file.</span></span>
2.  <span data-ttu-id="36e50-120">Use o compilador de recursos do Microsoft Windows (RC) para compilar o arquivo de definição de recurso em um arquivo de recurso compilado (. res).</span><span class="sxs-lookup"><span data-stu-id="36e50-120">Use the Microsoft Windows Resource Compiler (RC) to compile the resource definition file into a compiled resource (.res) file.</span></span> <span data-ttu-id="36e50-121">O compilador RC é fornecido com o Visual Studio e também o SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="36e50-121">The RC compiler is provided with Visual Studio and also the Windows SDK.</span></span>
3.  <span data-ttu-id="36e50-122">Vincule o arquivo de recurso compilado ao arquivo binário.</span><span class="sxs-lookup"><span data-stu-id="36e50-122">Link the compiled resource file to the binary file.</span></span>

<span data-ttu-id="36e50-123">Essas etapas são aproximadamente equivalentes ao processo de compilação/vínculo para arquivos de código.</span><span class="sxs-lookup"><span data-stu-id="36e50-123">These steps are roughly equivalent to the compile/link process for code files.</span></span> <span data-ttu-id="36e50-124">O Visual Studio fornece um conjunto de editores de recursos que facilitam a criação e a modificação de recursos.</span><span class="sxs-lookup"><span data-stu-id="36e50-124">Visual Studio provides a set of resource editors that make it easy to create and modify resources.</span></span> <span data-ttu-id="36e50-125">(Essas ferramentas não estão disponíveis nas Express Editions do Visual Studio.) Mas um arquivo. rc é simplesmente um arquivo de texto, e a sintaxe é documentada no MSDN, portanto, é possível criar um arquivo. rc usando qualquer editor de texto.</span><span class="sxs-lookup"><span data-stu-id="36e50-125">(These tools are not available in the Express editions of Visual Studio.) But an .rc file is simply a text file, and the syntax is documented on MSDN, so it is possible to create an .rc file using any text editor.</span></span> <span data-ttu-id="36e50-126">Para obter mais informações, consulte [About Resource files](/windows/desktop/menurc/about-resource-files).</span><span class="sxs-lookup"><span data-stu-id="36e50-126">For more information, see [About Resource Files](/windows/desktop/menurc/about-resource-files).</span></span>

## <a name="defining-an-accelerator-table"></a><span data-ttu-id="36e50-127">Definindo uma tabela de acelerador</span><span class="sxs-lookup"><span data-stu-id="36e50-127">Defining an Accelerator Table</span></span>

<span data-ttu-id="36e50-128">Uma tabela de acelerador é uma tabela de atalhos de teclado.</span><span class="sxs-lookup"><span data-stu-id="36e50-128">An accelerator table is a table of keyboard shortcuts.</span></span> <span data-ttu-id="36e50-129">Cada atalho é definido por:</span><span class="sxs-lookup"><span data-stu-id="36e50-129">Each shortcut is defined by:</span></span>

-   <span data-ttu-id="36e50-130">Um identificador numérico.</span><span class="sxs-lookup"><span data-stu-id="36e50-130">A numeric identifier.</span></span> <span data-ttu-id="36e50-131">Esse número identifica o comando do aplicativo que será invocado pelo atalho.</span><span class="sxs-lookup"><span data-stu-id="36e50-131">This number identifies the application command that will be invoked by the shortcut.</span></span>
-   <span data-ttu-id="36e50-132">O caractere ASCII ou o código de chave virtual do atalho.</span><span class="sxs-lookup"><span data-stu-id="36e50-132">The ASCII character or virtual-key code of the shortcut.</span></span>
-   <span data-ttu-id="36e50-133">Chaves modificadoras opcionais: ALT, SHIFT ou CTRL.</span><span class="sxs-lookup"><span data-stu-id="36e50-133">Optional modifier keys: ALT, SHIFT, or CTRL.</span></span>

<span data-ttu-id="36e50-134">A própria tabela do acelerador tem um identificador numérico, que identifica a tabela na lista de recursos do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="36e50-134">The accelerator table itself has a numeric identifier, which identifies the table in the list of application resources.</span></span> <span data-ttu-id="36e50-135">Vamos criar uma tabela de acelerador para um simples programa de desenho.</span><span class="sxs-lookup"><span data-stu-id="36e50-135">Let's create an accelerator table for a simple drawing program.</span></span> <span data-ttu-id="36e50-136">Este programa terá dois modos, modo de desenho e modo de seleção.</span><span class="sxs-lookup"><span data-stu-id="36e50-136">This program will have two modes, draw mode and selection mode.</span></span> <span data-ttu-id="36e50-137">No modo de desenho, o usuário pode desenhar formas.</span><span class="sxs-lookup"><span data-stu-id="36e50-137">In draw mode, the user can draw shapes.</span></span> <span data-ttu-id="36e50-138">No modo de seleção, o usuário pode selecionar formas.</span><span class="sxs-lookup"><span data-stu-id="36e50-138">In selection mode, the user can select shapes.</span></span> <span data-ttu-id="36e50-139">Para este programa, gostaríamos de definir os seguintes atalhos de teclado.</span><span class="sxs-lookup"><span data-stu-id="36e50-139">For this program, we would like to define the following keyboard shortcuts.</span></span>



| <span data-ttu-id="36e50-140">Atalho</span><span class="sxs-lookup"><span data-stu-id="36e50-140">Shortcut</span></span> | <span data-ttu-id="36e50-141">Comando</span><span class="sxs-lookup"><span data-stu-id="36e50-141">Command</span></span>                   |
|----------|---------------------------|
| <span data-ttu-id="36e50-142">CTRL+M</span><span class="sxs-lookup"><span data-stu-id="36e50-142">CTRL+M</span></span>   | <span data-ttu-id="36e50-143">Alternar entre os modos.</span><span class="sxs-lookup"><span data-stu-id="36e50-143">Toggle between modes.</span></span>     |
| <span data-ttu-id="36e50-144">F1</span><span class="sxs-lookup"><span data-stu-id="36e50-144">F1</span></span>       | <span data-ttu-id="36e50-145">Alterne para o modo de desenho.</span><span class="sxs-lookup"><span data-stu-id="36e50-145">Switch to draw mode.</span></span>      |
| <span data-ttu-id="36e50-146">F2</span><span class="sxs-lookup"><span data-stu-id="36e50-146">F2</span></span>       | <span data-ttu-id="36e50-147">Alternar para o modo de seleção.</span><span class="sxs-lookup"><span data-stu-id="36e50-147">Switch to selection mode.</span></span> |



 

<span data-ttu-id="36e50-148">Primeiro, defina identificadores numéricos para a tabela e para os comandos do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="36e50-148">First, define numeric identifiers for the table and for the application commands.</span></span> <span data-ttu-id="36e50-149">Esses valores são arbitrários.</span><span class="sxs-lookup"><span data-stu-id="36e50-149">These values are arbitrary.</span></span> <span data-ttu-id="36e50-150">Você pode atribuir constantes simbólicas para os identificadores definindo-os em um arquivo de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="36e50-150">You can assign symbolic constants for the identifiers by defining them in a header file.</span></span> <span data-ttu-id="36e50-151">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="36e50-151">For example:</span></span>


```C++
#define IDR_ACCEL1                      101
#define ID_TOGGLE_MODE                40002
#define ID_DRAW_MODE                  40003
#define ID_SELECT_MODE                40004
```



<span data-ttu-id="36e50-152">Neste exemplo, o valor `IDR_ACCEL1` identifica a tabela de acelerador e as três constantes a seguir definem os comandos do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="36e50-152">In this example, the value `IDR_ACCEL1` identifies the accelerator table, and the next three constants define the application commands.</span></span> <span data-ttu-id="36e50-153">Por convenção, um arquivo de cabeçalho que define constantes de recurso é geralmente denominado Resource. h.</span><span class="sxs-lookup"><span data-stu-id="36e50-153">By convention, a header file that defines resource constants is often named resource.h.</span></span> <span data-ttu-id="36e50-154">A próxima listagem mostra o arquivo de definição de recurso.</span><span class="sxs-lookup"><span data-stu-id="36e50-154">The next listing shows the resource definition file.</span></span>


```C++
#include "resource.h"

IDR_ACCEL1 ACCELERATORS
{
    0x4D,   ID_TOGGLE_MODE, VIRTKEY, CONTROL    // ctrl-M
    0x70,   ID_DRAW_MODE, VIRTKEY               // F1
    0x71,   ID_SELECT_MODE, VIRTKEY             // F2
}
```



<span data-ttu-id="36e50-155">Os atalhos do acelerador são definidos entre chaves.</span><span class="sxs-lookup"><span data-stu-id="36e50-155">The accelerator shortcuts are defined within the curly braces.</span></span> <span data-ttu-id="36e50-156">Cada atalho contém as entradas a seguir.</span><span class="sxs-lookup"><span data-stu-id="36e50-156">Each shortcut contains the following entries.</span></span>

-   <span data-ttu-id="36e50-157">O código de chave virtual ou o caractere ASCII que invoca o atalho.</span><span class="sxs-lookup"><span data-stu-id="36e50-157">The virtual-key code or ASCII character that invokes the shortcut.</span></span>
-   <span data-ttu-id="36e50-158">O comando do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="36e50-158">The application command.</span></span> <span data-ttu-id="36e50-159">Observe que as constantes simbólicas são usadas no exemplo.</span><span class="sxs-lookup"><span data-stu-id="36e50-159">Notice that symbolic constants are used in the example.</span></span> <span data-ttu-id="36e50-160">O arquivo de definição de recurso inclui Resource. h, em que essas constantes são definidas.</span><span class="sxs-lookup"><span data-stu-id="36e50-160">The resource definition file includes resource.h, where these constants are defined.</span></span>
-   <span data-ttu-id="36e50-161">A palavra-chave **VIRTKEY** significa que a primeira entrada é um código de chave virtual.</span><span class="sxs-lookup"><span data-stu-id="36e50-161">The keyword **VIRTKEY** means the first entry is a virtual-key code.</span></span> <span data-ttu-id="36e50-162">A outra opção é usar caracteres ASCII.</span><span class="sxs-lookup"><span data-stu-id="36e50-162">The other option is to use ASCII characters.</span></span>
-   <span data-ttu-id="36e50-163">Modificadores opcionais: ALT, CONTROL ou SHIFT.</span><span class="sxs-lookup"><span data-stu-id="36e50-163">Optional modifiers: ALT, CONTROL, or SHIFT.</span></span>

<span data-ttu-id="36e50-164">Se você usar caracteres ASCII para atalhos, um caractere minúsculo será um atalho diferente de um caractere maiúsculo.</span><span class="sxs-lookup"><span data-stu-id="36e50-164">If you use ASCII characters for shortcuts, then a lowercase character will be a different shortcut than an uppercase character.</span></span> <span data-ttu-id="36e50-165">(Por exemplo, digitar ' a ' pode invocar um comando diferente do que digitar ' A '.) Isso pode confundir os usuários, portanto, geralmente é melhor usar códigos de chave virtual, em vez de caracteres ASCII, para atalhos.</span><span class="sxs-lookup"><span data-stu-id="36e50-165">(For example, typing 'a' might invoke a different command than typing 'A'.) That might confuse users, so it is generally better to use virtual-key codes, rather than ASCII characters, for shortcuts.</span></span>

## <a name="loading-the-accelerator-table"></a><span data-ttu-id="36e50-166">Carregando a tabela de acelerador</span><span class="sxs-lookup"><span data-stu-id="36e50-166">Loading the Accelerator Table</span></span>

<span data-ttu-id="36e50-167">O recurso para a tabela de acelerador deve ser carregado antes que o programa possa usá-lo.</span><span class="sxs-lookup"><span data-stu-id="36e50-167">The resource for the accelerator table must be loaded before the program can use it.</span></span> <span data-ttu-id="36e50-168">Para carregar uma tabela de acelerador, chame a função [**LoadAccelerators**](/windows/desktop/api/winuser/nf-winuser-loadacceleratorsa) .</span><span class="sxs-lookup"><span data-stu-id="36e50-168">To load an accelerator table, call the [**LoadAccelerators**](/windows/desktop/api/winuser/nf-winuser-loadacceleratorsa) function.</span></span>


```C++
    HACCEL hAccel = LoadAccelerators(hInstance, MAKEINTRESOURCE(IDR_ACCEL1));
```



<span data-ttu-id="36e50-169">Chame essa função antes de inserir o loop de mensagem.</span><span class="sxs-lookup"><span data-stu-id="36e50-169">Call this function before you enter the message loop.</span></span> <span data-ttu-id="36e50-170">O primeiro parâmetro é o identificador para o módulo.</span><span class="sxs-lookup"><span data-stu-id="36e50-170">The first parameter is the handle to the module.</span></span> <span data-ttu-id="36e50-171">(Esse parâmetro é passado para sua função [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) .</span><span class="sxs-lookup"><span data-stu-id="36e50-171">(This parameter is passed to your [**WinMain**](/windows/desktop/api/winbase/nf-winbase-winmain) function.</span></span> <span data-ttu-id="36e50-172">Para obter detalhes, consulte [WinMain: o ponto de entrada do aplicativo](winmain--the-application-entry-point.md).) O segundo parâmetro é o identificador de recurso.</span><span class="sxs-lookup"><span data-stu-id="36e50-172">For details, see [WinMain: The Application Entry Point](winmain--the-application-entry-point.md).) The second parameter is the resource identifier.</span></span> <span data-ttu-id="36e50-173">A função retorna um identificador para o recurso.</span><span class="sxs-lookup"><span data-stu-id="36e50-173">The function returns a handle to the resource.</span></span> <span data-ttu-id="36e50-174">Lembre-se de que um identificador é um tipo opaco que se refere a um objeto gerenciado pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="36e50-174">Recall that a handle is an opaque type that refers to an object managed by the system.</span></span> <span data-ttu-id="36e50-175">Se a função falhar, ela retornará **NULL**.</span><span class="sxs-lookup"><span data-stu-id="36e50-175">If the function fails, it returns **NULL**.</span></span>

<span data-ttu-id="36e50-176">Você pode liberar uma tabela de acelerador chamando [**DestroyAcceleratorTable**](/windows/desktop/api/winuser/nf-winuser-destroyacceleratortable).</span><span class="sxs-lookup"><span data-stu-id="36e50-176">You can release an accelerator table by calling [**DestroyAcceleratorTable**](/windows/desktop/api/winuser/nf-winuser-destroyacceleratortable).</span></span> <span data-ttu-id="36e50-177">No entanto, o sistema libera automaticamente a tabela quando o programa é encerrado, portanto, você só precisa chamar essa função se estiver substituindo uma tabela por outra.</span><span class="sxs-lookup"><span data-stu-id="36e50-177">However, the system automatically releases the table when the program exits, so you only need to call this function if you are replacing one table with another.</span></span> <span data-ttu-id="36e50-178">Há um exemplo interessante disso no tópico [criando aceleradores editáveis do usuário](/windows/desktop/menurc/using-keyboard-accelerators).</span><span class="sxs-lookup"><span data-stu-id="36e50-178">There is an interesting example of this in the topic [Creating User Editable Accelerators](/windows/desktop/menurc/using-keyboard-accelerators).</span></span>

## <a name="translating-key-strokes-into-commands"></a><span data-ttu-id="36e50-179">Convertendo traços de chave em comandos</span><span class="sxs-lookup"><span data-stu-id="36e50-179">Translating Key Strokes into Commands</span></span>

<span data-ttu-id="36e50-180">Uma tabela de acelerador funciona convertendo os traços de chave em mensagens de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="36e50-180">An accelerator table works by translating key strokes into [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) messages.</span></span> <span data-ttu-id="36e50-181">O parâmetro *wParam* do **\_ comando do WM** contém o identificador numérico do comando.</span><span class="sxs-lookup"><span data-stu-id="36e50-181">The *wParam* parameter of **WM\_COMMAND** contains the numeric identifier of the command.</span></span> <span data-ttu-id="36e50-182">Por exemplo, usando a tabela mostrada anteriormente, o pressionamento de tecla CTRL + M é convertido em uma mensagem de **\_ comando do WM** com o valor `ID_TOGGLE_MODE` .</span><span class="sxs-lookup"><span data-stu-id="36e50-182">For example, using the table shown previously, the key stroke CTRL+M is translated into a **WM\_COMMAND** message with the value `ID_TOGGLE_MODE`.</span></span> <span data-ttu-id="36e50-183">Para fazer isso acontecer, altere o loop de mensagem para o seguinte:</span><span class="sxs-lookup"><span data-stu-id="36e50-183">To make this happen, change your message loop to the following:</span></span>


```C++
    MSG msg;
    while (GetMessage(&msg, NULL, 0, 0))
    {
        if (!TranslateAccelerator(win.Window(), hAccel, &msg))
        {
            TranslateMessage(&msg);
            DispatchMessage(&msg);
        }
    }
```



<span data-ttu-id="36e50-184">Esse código adiciona uma chamada para a função [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) dentro do loop de mensagem.</span><span class="sxs-lookup"><span data-stu-id="36e50-184">This code adds a call to the [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) function inside the message loop.</span></span> <span data-ttu-id="36e50-185">A função **TranslateAccelerator** examina cada mensagem de janela, procurando mensagens de chave para baixo.</span><span class="sxs-lookup"><span data-stu-id="36e50-185">The **TranslateAccelerator** function examines each window message, looking for key-down messages.</span></span> <span data-ttu-id="36e50-186">Se o usuário pressionar uma das combinações de teclas listadas na tabela do acelerador, **TranslateAccelerator** enviará uma mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) para a janela.</span><span class="sxs-lookup"><span data-stu-id="36e50-186">If the user presses one of the key combinations listed in the accelerator table, **TranslateAccelerator** sends a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message to the window.</span></span> <span data-ttu-id="36e50-187">A função envia **o \_ comando do WM** invocando diretamente o procedimento de janela.</span><span class="sxs-lookup"><span data-stu-id="36e50-187">The function sends **WM\_COMMAND** by directly invoking the window procedure.</span></span> <span data-ttu-id="36e50-188">Quando **TranslateAccelerator** converte com êxito um traço de chave, a função retorna um valor diferente de zero, o que significa que você deve ignorar o processamento normal da mensagem.</span><span class="sxs-lookup"><span data-stu-id="36e50-188">When **TranslateAccelerator** successfully translates a key stroke, the function returns a non-zero value, which means you should skip the normal processing for the message.</span></span> <span data-ttu-id="36e50-189">Caso contrário, **TranslateAccelerator** retornará zero.</span><span class="sxs-lookup"><span data-stu-id="36e50-189">Otherwise, **TranslateAccelerator** returns zero.</span></span> <span data-ttu-id="36e50-190">Nesse caso, passe a mensagem de janela para [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) e [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage), como de costume.</span><span class="sxs-lookup"><span data-stu-id="36e50-190">In that case, pass the window message to [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) and [**DispatchMessage**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage), as normal.</span></span>

<span data-ttu-id="36e50-191">Veja como o programa de desenho pode manipular a mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) :</span><span class="sxs-lookup"><span data-stu-id="36e50-191">Here is how the drawing program might handle the [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message:</span></span>


```C++
    case WM_COMMAND:
        switch (LOWORD(wParam))
        {
        case ID_DRAW_MODE:
            SetMode(DrawMode);
            break;

        case ID_SELECT_MODE:
            SetMode(SelectMode);
            break;

        case ID_TOGGLE_MODE:
            if (mode == DrawMode)
            {
                SetMode(SelectMode);
            }
            else
            {
                SetMode(DrawMode);
            }
            break;
        }
        return 0;

```



<span data-ttu-id="36e50-192">Esse código pressupõe que `SetMode` é uma função definida pelo aplicativo para alternar entre os dois modos.</span><span class="sxs-lookup"><span data-stu-id="36e50-192">This code assumes that `SetMode` is a function defined by the application to switch between the two modes.</span></span> <span data-ttu-id="36e50-193">Os detalhes de como você trataria cada comando obviamente dependem do seu programa.</span><span class="sxs-lookup"><span data-stu-id="36e50-193">The details of how you would handle each command obviously depend on your program.</span></span>

## <a name="next"></a><span data-ttu-id="36e50-194">Avançar</span><span class="sxs-lookup"><span data-stu-id="36e50-194">Next</span></span>

[<span data-ttu-id="36e50-195">Definindo a imagem do cursor</span><span class="sxs-lookup"><span data-stu-id="36e50-195">Setting the Cursor Image</span></span>](setting-the-cursor-image.md)

 

 