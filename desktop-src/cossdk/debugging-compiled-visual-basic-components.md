---
description: Considerando que, em muitos casos, você poderá depurar apenas uma parte da funcionalidade de seus componentes no ambiente do Microsoft Visual Basic, haverá situações em que você precisará depurar os componentes criados com Visual Basic depois que eles tiverem sido compilados. Como o ambiente de Visual Basic não permite isso, você deve usar o ambiente de Microsoft Visual C++.
ms.assetid: a58c5884-3c2d-4699-8b19-277003912dfd
title: Depurando componentes de Visual Basic compilados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07b32a39f0f1c50e1da4c9534b40658838361225
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089175"
---
# <a name="debugging-compiled-visual-basic-components"></a><span data-ttu-id="c65d2-104">Depurando componentes de Visual Basic compilados</span><span class="sxs-lookup"><span data-stu-id="c65d2-104">Debugging Compiled Visual Basic Components</span></span>

<span data-ttu-id="c65d2-105">Considerando que, em muitos casos, você poderá depurar apenas uma parte da funcionalidade do componente dentro do ambiente do Microsoft Visual Basic, haverá situações em que você precisará depurar os componentes criados com Visual Basic depois que eles tiverem sido compilados.</span><span class="sxs-lookup"><span data-stu-id="c65d2-105">Given that in many cases you will be able to debug only a portion of your component's functionality within the Microsoft Visual Basic environment, there will be situations in which you will need to debug components built with Visual Basic after they have been compiled.</span></span> <span data-ttu-id="c65d2-106">Como o ambiente de Visual Basic não permite isso, você deve usar o ambiente de Microsoft Visual C++.</span><span class="sxs-lookup"><span data-stu-id="c65d2-106">Since the Visual Basic environment doesn't enable this, you must instead use the Microsoft Visual C++ environment.</span></span>

<span data-ttu-id="c65d2-107">**Para depurar um componente de Visual Basic no ambiente de Visual C++**</span><span class="sxs-lookup"><span data-stu-id="c65d2-107">**To debug a Visual Basic component in the Visual C++ environment**</span></span>

1.  <span data-ttu-id="c65d2-108">No Visual Basic 6,0, abra o projeto Visual Basic que você deseja depurar.</span><span class="sxs-lookup"><span data-stu-id="c65d2-108">In Visual Basic 6.0, open the Visual Basic project that you want to debug.</span></span>

2.  <span data-ttu-id="c65d2-109">No menu **arquivo** , clique em **fazer YourProject.dll**.</span><span class="sxs-lookup"><span data-stu-id="c65d2-109">On the **File** menu, click **Make YourProject.dll**.</span></span>

3.  <span data-ttu-id="c65d2-110">Na caixa de diálogo **criar projeto** , clique em **Opções**.</span><span class="sxs-lookup"><span data-stu-id="c65d2-110">In the **Make Project** dialog box, click **Options**.</span></span>

4.  <span data-ttu-id="c65d2-111">Na caixa de diálogo **Propriedades do projeto** , na guia **Compilar** , clique em **Compilar para código nativo** e **sem otimização** e marque a caixa de seleção **criar informações de depuração simbólicas** .</span><span class="sxs-lookup"><span data-stu-id="c65d2-111">In the **Project Properties** dialog box, on the **Compile** tab, click **Compile to Native Code** and **No Optimization** and select the **Create Symbolic Debug Info** check box.</span></span>

5.  <span data-ttu-id="c65d2-112">Clique em **OK** e em **OK** novamente para compilar o projeto.</span><span class="sxs-lookup"><span data-stu-id="c65d2-112">Click **OK**, and then click **OK** again to compile your project.</span></span>

6.  <span data-ttu-id="c65d2-113">Mova a DLL compilada para o local onde os aplicativos COM+ são instalados normalmente.</span><span class="sxs-lookup"><span data-stu-id="c65d2-113">Move the compiled DLL to the location where COM+ applications are normally installed.</span></span>

    > [!Note]  
    > <span data-ttu-id="c65d2-114">Se você não mover a DLL, poderá receber uma mensagem de erro informando que não foi possível localizar informações de depuração simbólicas da DLL.</span><span class="sxs-lookup"><span data-stu-id="c65d2-114">If you don't move the DLL, you may get an error message informing you that symbolic debugging information for the DLL could not be located.</span></span> <span data-ttu-id="c65d2-115">Se você tiver problemas para fazer com que o depurador pare nos pontos de interrupção em seu componente, confirme se a DLL está no diretório de pacotes padrão, exclua o componente de seu pacote e adicione o componente novamente.</span><span class="sxs-lookup"><span data-stu-id="c65d2-115">If you have trouble getting the debugger to stop at breakpoints in your component, confirm that the DLL is in the standard packages directory, delete the component from its package, and re-add the component.</span></span>

     

7.  <span data-ttu-id="c65d2-116">Iniciar Visual C++.</span><span class="sxs-lookup"><span data-stu-id="c65d2-116">Start Visual C++.</span></span>

8.  <span data-ttu-id="c65d2-117">No menu **arquivo** , clique em **abrir espaço de trabalho**.</span><span class="sxs-lookup"><span data-stu-id="c65d2-117">On the **File** menu, click **Open Workspace**.</span></span>

9.  <span data-ttu-id="c65d2-118">Na caixa de diálogo **abrir espaço de trabalho** , defina **arquivos do tipo** como **todos os arquivos ( \* . \* )**, selecione o componente compilado e clique em **abrir**.</span><span class="sxs-lookup"><span data-stu-id="c65d2-118">In the **Open Workspace** dialog box, set **Files of Type** to **All files(\*.\*)**, select your compiled component, and click **Open**.</span></span>

10. <span data-ttu-id="c65d2-119">No menu **arquivo** , clique em **abrir** (não **abra espaço de trabalho**) e abra o módulo Visual Basic (. bas), formulário (. frm) ou classe (. CLS) que você deseja depurar.</span><span class="sxs-lookup"><span data-stu-id="c65d2-119">From the **File** menu, click **Open** (not **Open Workspace**) and open the Visual Basic module (.bas), form (.frm), or class (.cls) that you want to debug.</span></span>

11. <span data-ttu-id="c65d2-120">No menu **projeto** , clique em **configurações**.</span><span class="sxs-lookup"><span data-stu-id="c65d2-120">On the **Project** menu, click **Settings**.</span></span>

12. <span data-ttu-id="c65d2-121">Na caixa de diálogo **configurações do projeto** , na guia **depurar** , selecione **geral** na caixa **categoria** .</span><span class="sxs-lookup"><span data-stu-id="c65d2-121">In the **Project Settings** dialog box, on the **Debug** tab, select **General** in the **Category** box.</span></span>

13. <span data-ttu-id="c65d2-122">Na caixa **executável para sessão de depuração** , insira o caminho totalmente qualificado para Dllhost.exe, seguido por um argumento ESPECIFICANDO a ID do processo do aplicativo com+ que contém o componente.</span><span class="sxs-lookup"><span data-stu-id="c65d2-122">In the **Executable for debug session** box, enter the fully qualified path for Dllhost.exe, followed by an argument specifying the process ID of the COM+ application containing the component.</span></span> <span data-ttu-id="c65d2-123">Você encontrará a ID do processo na guia **geral** da caixa de diálogo **Propriedades** do aplicativo com+.</span><span class="sxs-lookup"><span data-stu-id="c65d2-123">You will find the process ID on the **General** tab of the COM+ application's **Properties** dialog box.</span></span> <span data-ttu-id="c65d2-124">Veja a seguir um exemplo: C: \\ WinNT \\ System32 \\Dllhost.exe/ProcessId: { <processID> }.</span><span class="sxs-lookup"><span data-stu-id="c65d2-124">Following is an example: C:\\Winnt\\System32\\Dllhost.exe /ProcessID:{<processID>}.</span></span>

14. <span data-ttu-id="c65d2-125">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="c65d2-125">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c65d2-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c65d2-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c65d2-127">Suporte à depuração de Visual Basic COM+ em contraste com o MTS</span><span class="sxs-lookup"><span data-stu-id="c65d2-127">COM+ Visual Basic Debugging Support Contrasted with MTS</span></span>](com--visual-basic-debugging-support-contrasted-with-mts.md)
</dt> <dt>

[<span data-ttu-id="c65d2-128">Depuração no IDE Visual Basic</span><span class="sxs-lookup"><span data-stu-id="c65d2-128">Debugging in the Visual Basic IDE</span></span>](debugging-in-the-visual-basic-ide.md)
</dt> </dl>

 

 



