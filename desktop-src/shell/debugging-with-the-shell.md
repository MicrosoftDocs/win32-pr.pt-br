---
description: Este tópico explica como depurar Shell e DLLs de extensão de namespace.
title: Depuração com o Shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2fcaf633-9a6d-4fda-a690-28445b10a6d6
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 3ca6e30809565408454976e1b07ff37dcc8f8f8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501431"
---
# <a name="debugging-with-the-shell"></a><span data-ttu-id="39b8e-103">Depuração com o Shell</span><span class="sxs-lookup"><span data-stu-id="39b8e-103">Debugging with the Shell</span></span>

<span data-ttu-id="39b8e-104">Este tópico explica como depurar Shell e DLLs de extensão de namespace.</span><span class="sxs-lookup"><span data-stu-id="39b8e-104">This topic explains how to debug Shell and namespace extension DLLs.</span></span>

-   [<span data-ttu-id="39b8e-105">Executando o Shell em um depurador</span><span class="sxs-lookup"><span data-stu-id="39b8e-105">Running the Shell Under a Debugger</span></span>](#running-the-shell-under-a-debugger)
-   [<span data-ttu-id="39b8e-106">Executando e testando extensões do Shell</span><span class="sxs-lookup"><span data-stu-id="39b8e-106">Running and Testing Shell Extensions</span></span>](#running-and-testing-shell-extensions)
-   [<span data-ttu-id="39b8e-107">Descarregando a DLL</span><span class="sxs-lookup"><span data-stu-id="39b8e-107">Unloading the DLL</span></span>](#unloading-the-dll)

## <a name="running-the-shell-under-a-debugger"></a><span data-ttu-id="39b8e-108">Executando o Shell em um depurador</span><span class="sxs-lookup"><span data-stu-id="39b8e-108">Running the Shell Under a Debugger</span></span>

<span data-ttu-id="39b8e-109">Para depurar sua extensão, você precisa executar o Shell do depurador.</span><span class="sxs-lookup"><span data-stu-id="39b8e-109">To debug your extension, you need to run the Shell from the debugger.</span></span> <span data-ttu-id="39b8e-110">Siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="39b8e-110">Follow these steps:</span></span>

1.  <span data-ttu-id="39b8e-111">Carregue o projeto da extensão no depurador, mas não o execute.</span><span class="sxs-lookup"><span data-stu-id="39b8e-111">Load the extension's project into the debugger, but do not run it.</span></span>
2.  <span data-ttu-id="39b8e-112">Desligue o Shell.</span><span class="sxs-lookup"><span data-stu-id="39b8e-112">Shut down the Shell.</span></span>

    -   <span data-ttu-id="39b8e-113">Para o Windows Vista e posterior:</span><span class="sxs-lookup"><span data-stu-id="39b8e-113">For Windows Vista and later:</span></span>
        1.  <span data-ttu-id="39b8e-114">Exibir o menu **Iniciar** .</span><span class="sxs-lookup"><span data-stu-id="39b8e-114">Display the **Start** menu.</span></span>
        2.  <span data-ttu-id="39b8e-115">Pressione CTRL + SHIFT e clique com o botão direito do mouse no plano de fundo da metade direita do menu **Iniciar** .</span><span class="sxs-lookup"><span data-stu-id="39b8e-115">Press CTRL+SHIFT and right-click on the background of the right half of the **Start** menu.</span></span>
        3.  <span data-ttu-id="39b8e-116">No menu que aparece, escolha **sair do Gerenciador**.</span><span class="sxs-lookup"><span data-stu-id="39b8e-116">From the menu that appears, choose **Exit Explorer**.</span></span>
    -   <span data-ttu-id="39b8e-117">Para o Windows XP:</span><span class="sxs-lookup"><span data-stu-id="39b8e-117">For Windows XP:</span></span>
        1.  <span data-ttu-id="39b8e-118">No menu **Iniciar** , escolha **desligar**.</span><span class="sxs-lookup"><span data-stu-id="39b8e-118">From the **Start** menu, choose **Shut down**.</span></span>
        2.  <span data-ttu-id="39b8e-119">Pressione CTRL + ALT + SHIFT e clique em **não** na caixa de diálogo **desligar o Windows** .</span><span class="sxs-lookup"><span data-stu-id="39b8e-119">Press CTRL+ALT+SHIFT, and click **No** in the **Shut Down Windows** dialog box.</span></span>

    <span data-ttu-id="39b8e-120">O Shell agora está desligado, mas todos os outros aplicativos ainda estão em execução, incluindo o depurador.</span><span class="sxs-lookup"><span data-stu-id="39b8e-120">The Shell is now shut down, but all other applications are still running, including the debugger.</span></span>

3.  <span data-ttu-id="39b8e-121">Defina o depurador para executar a DLL de extensão com Explorer.exe do diretório do **Windows** .</span><span class="sxs-lookup"><span data-stu-id="39b8e-121">Set the debugger to run the extension DLL with Explorer.exe from the **Windows** directory.</span></span>
4.  <span data-ttu-id="39b8e-122">Execute o projeto do depurador.</span><span class="sxs-lookup"><span data-stu-id="39b8e-122">Run the project from the debugger.</span></span> <span data-ttu-id="39b8e-123">O shell será iniciado como de costume, mas o depurador será anexado ao processo do Shell.</span><span class="sxs-lookup"><span data-stu-id="39b8e-123">The Shell will launch as usual, but the debugger will be attached to the Shell's process.</span></span>

## <a name="running-and-testing-shell-extensions"></a><span data-ttu-id="39b8e-124">Executando e testando extensões do Shell</span><span class="sxs-lookup"><span data-stu-id="39b8e-124">Running and Testing Shell Extensions</span></span>

<span data-ttu-id="39b8e-125">Você pode executar e testar suas extensões em um processo separado do Windows Explorer para evitar parar e reiniciar a área de trabalho e a barra de tarefas.</span><span class="sxs-lookup"><span data-stu-id="39b8e-125">You can run and test your extensions in a separate Windows Explorer process to avoid stopping and restarting the desktop and taskbar.</span></span> <span data-ttu-id="39b8e-126">A área de trabalho e a barra de tarefas ainda podem ser usadas enquanto você executa e testa as extensões.</span><span class="sxs-lookup"><span data-stu-id="39b8e-126">Your desktop and taskbar can still be used while you run and test the extensions.</span></span>

<span data-ttu-id="39b8e-127">Para habilitar esse recurso, adicione a seguinte \_ entrada reg DWORD ao registro.</span><span class="sxs-lookup"><span data-stu-id="39b8e-127">To enable this feature, add the following REG\_DWORD entry to the registry.</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  DesktopProcess = 1
```

<span data-ttu-id="39b8e-128">Para que essa entrada tenha efeito, você deve fazer logoff e logon novamente.</span><span class="sxs-lookup"><span data-stu-id="39b8e-128">For this entry to take effect, you must log off and log on again.</span></span> <span data-ttu-id="39b8e-129">Essa configuração faz com que as janelas da área de trabalho e da barra de tarefas sejam criadas em um Explorer.exe processo e todas as outras janelas de navegador e de pasta sejam abertas em um processo de Explorer.exe diferente.</span><span class="sxs-lookup"><span data-stu-id="39b8e-129">This setting causes the desktop and taskbar windows to be created in one Explorer.exe process and all other Explorer and folder windows to be opened in a different Explorer.exe process.</span></span>

<span data-ttu-id="39b8e-130">Além de tornar a execução e o teste de suas extensões mais convenientes, essa configuração também torna a área de trabalho mais robusta, pois está relacionada às extensões do Shell.</span><span class="sxs-lookup"><span data-stu-id="39b8e-130">In addition to making the running and testing of your extensions more convenient, this setting also makes the desktop more robust as it relates to Shell extensions.</span></span> <span data-ttu-id="39b8e-131">Muitas dessas extensões (extensões de menu de atalho, por exemplo) serão carregadas no processo não Explorer.exe da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="39b8e-131">Many such extensions (shortcut menu extensions, for example) will be loaded into the nondesktop Explorer.exe process.</span></span> <span data-ttu-id="39b8e-132">Se esse processo for encerrado, a área de trabalho e a barra de tarefas não serão afetadas e a próxima janela de navegador ou pasta recriará o processo encerrado.</span><span class="sxs-lookup"><span data-stu-id="39b8e-132">If this process terminates, the desktop and taskbar will be unaffected, and the next Explorer or folder window will re-create the terminated process.</span></span>

## <a name="unloading-the-dll"></a><span data-ttu-id="39b8e-133">Descarregando a DLL</span><span class="sxs-lookup"><span data-stu-id="39b8e-133">Unloading the DLL</span></span>

<span data-ttu-id="39b8e-134">O Shell descarregará automaticamente qualquer DLL quando sua contagem de uso for zero, mas somente depois que a DLL não tiver sido usada por um período de tempo.</span><span class="sxs-lookup"><span data-stu-id="39b8e-134">The Shell automatically unloads any DLL when its usage count is zero, but only after the DLL has not been used for a period of time.</span></span> <span data-ttu-id="39b8e-135">Esse período inativo pode ser muito demorado às vezes, especialmente quando um DLL de extensão de Shell está sendo depurado.</span><span class="sxs-lookup"><span data-stu-id="39b8e-135">This inactive period might be unacceptably long at times, especially when a Shell extension DLL is being debugged.</span></span> <span data-ttu-id="39b8e-136">Você pode encurtar o período inativo adicionando as informações a seguir ao registro.</span><span class="sxs-lookup"><span data-stu-id="39b8e-136">You can shorten the inactive period by adding the following information to the registry.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AlwaysUnloadDll
```

 

 



