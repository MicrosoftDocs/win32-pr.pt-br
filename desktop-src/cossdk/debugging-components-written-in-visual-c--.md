---
description: Quando estiver pronto para depurar a funcionalidade COM+ em seus componentes do Microsoft Visual C++, você poderá configurar Visual C++ projeto ou a ferramenta administrativa serviços de componentes para iniciar o depurador.
ms.assetid: 206467ac-108a-49de-a884-66959dc77650
title: Componentes de depuração escritos em Visual C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a14e4b6324cc69531f09612c2af37fa03a036fd4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105790625"
---
# <a name="debugging-components-written-in-visual-c"></a><span data-ttu-id="fc564-103">Componentes de depuração escritos em Visual C++</span><span class="sxs-lookup"><span data-stu-id="fc564-103">Debugging Components Written in Visual C++</span></span>

<span data-ttu-id="fc564-104">Quando estiver pronto para depurar a funcionalidade COM+ em seus componentes do Microsoft Visual C++, você poderá configurar Visual C++ projeto ou a ferramenta administrativa serviços de componentes para iniciar o depurador.</span><span class="sxs-lookup"><span data-stu-id="fc564-104">When you are ready to debug the COM+ functionality in your Microsoft Visual C++ components, you can configure Visual C++ project or the Component Services administrative tool to launch the debugger.</span></span> <span data-ttu-id="fc564-105">Se você estiver usando Visual C++, poderá depurar com um cliente remoto usando o RPC OLE e a depuração Just-in-time (JIT).</span><span class="sxs-lookup"><span data-stu-id="fc564-105">If you are using Visual C++, you can debug with a remote client using OLE RPC and just-in-time (JIT) debugging.</span></span> <span data-ttu-id="fc564-106">Se não for possível executar o cliente no depurador ou se o cliente estiver em execução em outra máquina, você poderá usar a configuração iniciar do COM+ **no depurador** .</span><span class="sxs-lookup"><span data-stu-id="fc564-106">If you are unable to run your client under the debugger or if the client is running on another machine, you can use the COM+ **Launch in debugger** setting.</span></span> <span data-ttu-id="fc564-107">Você verá isso na ferramenta administrativa serviços de componentes como uma caixa de seleção na guia **avançado** da caixa de diálogo **Propriedades** do aplicativo com+.</span><span class="sxs-lookup"><span data-stu-id="fc564-107">You will find this in the Component Services administrative tool as a check box on the **Advanced** tab of the COM+ application **Properties** dialog box.</span></span>

<span data-ttu-id="fc564-108">Quando terminar a depuração, você deverá desligar os aplicativos COM+ que está depurando.</span><span class="sxs-lookup"><span data-stu-id="fc564-108">When you are finished debugging, you should shut down the COM+ applications you are debugging.</span></span> <span data-ttu-id="fc564-109">Se um processo do servidor for deixado em execução, você poderá receber uma mensagem de erro na próxima vez que tentar criar uma DLL quando a DLL existente ainda estiver carregada na memória.</span><span class="sxs-lookup"><span data-stu-id="fc564-109">If a server process is left running, you might get an error message the next time you try to build a DLL when the existing DLL is still loaded in memory.</span></span> <span data-ttu-id="fc564-110">Para desligar um aplicativo COM+, clique com o botão direito do mouse no aplicativo na árvore de console e clique em **desligar**.</span><span class="sxs-lookup"><span data-stu-id="fc564-110">To shut down a COM+ application, right-click the application in the console tree and then click **Shut down**.</span></span>

> [!Note]  
> <span data-ttu-id="fc564-111">Se você estiver usando transações, talvez também queira aumentar o tempo limite da transação, cujo padrão é de 60 segundos.</span><span class="sxs-lookup"><span data-stu-id="fc564-111">If you are using transactions, you might also want to increase the transaction time-out, which defaults to 60 seconds.</span></span> <span data-ttu-id="fc564-112">Você também pode especificar um valor de 0, especificando efetivamente um período de tempo limite de transação infinito.</span><span class="sxs-lookup"><span data-stu-id="fc564-112">You can also specify a value of 0, effectively specifying an infinite transaction time-out period.</span></span> <span data-ttu-id="fc564-113">Usando a ferramenta administrativa serviços de componentes, altere a configuração de tempo limite da transação na guia **Opções** da janela **Propriedades do meu computador** .</span><span class="sxs-lookup"><span data-stu-id="fc564-113">Using the Component Services administrative tool, change the transaction time-out setting on the **Options** tab of the **My Computer Properties** window.</span></span>

 

## <a name="debugging-server-application-components-with-visual-c"></a><span data-ttu-id="fc564-114">Depurando componentes de aplicativos de servidor com Visual C++</span><span class="sxs-lookup"><span data-stu-id="fc564-114">Debugging Server Application Components with Visual C++</span></span>

<span data-ttu-id="fc564-115">Ao depurar aplicativos de servidor COM+, talvez você queira depurar chamadas remotas carregando o cliente e o aplicativo de servidor no depurador.</span><span class="sxs-lookup"><span data-stu-id="fc564-115">When debugging COM+ server applications, you may want to debug remote calls by loading both the client and the server application into the debugger.</span></span> <span data-ttu-id="fc564-116">Com o Visual C++, você pode depurar chamadas remotas para seus componentes por meio das configurações JIT (just-in-time) e RPC do OLE.</span><span class="sxs-lookup"><span data-stu-id="fc564-116">With Visual C++, you can debug remote calls to your components through the just-in-time (JIT) and OLE RPC settings.</span></span> <span data-ttu-id="fc564-117">A configuração JIT faz com que o componente compilado inicie o depurador de Visual C++ quando ocorrer um erro; a configuração OLE RPC permite que o depurador passe do cliente para o componente conforme você percorre seu código.</span><span class="sxs-lookup"><span data-stu-id="fc564-117">The JIT setting causes the compiled component to start the Visual C++ debugger when an error occurs; the OLE RPC setting enables the debugger to step from client to component as you step through your code.</span></span>

<span data-ttu-id="fc564-118">Quando esses recursos estiverem habilitados, você poderá iniciar o cliente no depurador.</span><span class="sxs-lookup"><span data-stu-id="fc564-118">When these features are enabled, you can start your client under the debugger.</span></span> <span data-ttu-id="fc564-119">Quando o cliente fizer uma chamada para seu componente, o depurador irá entrar no código do componente no processo do servidor, mesmo se o servidor estiver em um computador diferente na rede.</span><span class="sxs-lookup"><span data-stu-id="fc564-119">When the client makes a call to your component, the debugger will step into the component's code in the server process, even if the server is on a different computer on the network.</span></span> <span data-ttu-id="fc564-120">Uma sessão de depuração é iniciada automaticamente no computador servidor, se necessário.</span><span class="sxs-lookup"><span data-stu-id="fc564-120">A debugging session is automatically started on the server computer if necessary.</span></span> <span data-ttu-id="fc564-121">Da mesma forma, a etapa única após a instrução return no código do componente retornará a depuração para a próxima instrução no código do cliente.</span><span class="sxs-lookup"><span data-stu-id="fc564-121">Similarly, single stepping past the return statement in the component's code will return debugging to the next statement in the client's code.</span></span>

> [!Note]  
> <span data-ttu-id="fc564-122">Talvez seja possível salvar algumas etapas usando a configuração **Iniciar no depurador** do com+.</span><span class="sxs-lookup"><span data-stu-id="fc564-122">You may be able to save a few steps by using the COM+ **Launch in debugger** setting.</span></span> <span data-ttu-id="fc564-123">Isso permite que você especifique o depurador de Visual C++ (ou outro) sem precisar fazer configurações de depuração especiais no ambiente de Visual C++.</span><span class="sxs-lookup"><span data-stu-id="fc564-123">This allows you to specify the Visual C++ (or other) debugger without having to make special debug settings in the Visual C++ environment.</span></span> <span data-ttu-id="fc564-124">Você verá isso na ferramenta administrativa serviços de componentes como uma caixa de seleção na guia **avançado** da caixa de diálogo **Propriedades** do aplicativo com+.</span><span class="sxs-lookup"><span data-stu-id="fc564-124">You will find this in the Component Services administrative tool as a check box on the **Advanced** tab of the COM+ application **Properties** dialog box.</span></span> <span data-ttu-id="fc564-125">Para obter mais informações, consulte "depuração sem Visual C++" neste tópico.</span><span class="sxs-lookup"><span data-stu-id="fc564-125">For more information, see "Debugging Without Visual C++" in this topic.</span></span>

 

<span data-ttu-id="fc564-126">Quando o aplicativo COM+ que contém o componente é um aplicativo de servidor, você deve começar encerrando o aplicativo usando a ferramenta administrativa serviços de componentes.</span><span class="sxs-lookup"><span data-stu-id="fc564-126">When the COM+ application containing your component is a server application, you must begin by shutting down the application using the Component Services administrative tool.</span></span> <span data-ttu-id="fc564-127">Para fazer isso, clique com o botão direito do mouse no aplicativo COM+ na árvore de console e clique em **desligar**.</span><span class="sxs-lookup"><span data-stu-id="fc564-127">To do this, right-click the COM+ application in the console tree and then click **Shut down**.</span></span>

<span data-ttu-id="fc564-128">**Para habilitar a depuração de RPC no Visual C++**</span><span class="sxs-lookup"><span data-stu-id="fc564-128">**To enable RPC debugging in Visual C++**</span></span>

1.  <span data-ttu-id="fc564-129">No Visual C++, no menu **ferramentas** , clique em **Opções**.</span><span class="sxs-lookup"><span data-stu-id="fc564-129">In Visual C++, on the **Tools** menu, click **Options**.</span></span>

2.  <span data-ttu-id="fc564-130">Na caixa de diálogo **Opções** , na guia **depurar** , marque as caixas de seleção **depuração de RPC OLE** e **depuração Just-in-time** .</span><span class="sxs-lookup"><span data-stu-id="fc564-130">In the **Options** dialog box, on the **Debug** tab, select the **OLE RPC debugging** and **Just-in time debugging** check boxes.</span></span>

3.  <span data-ttu-id="fc564-131">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="fc564-131">Click **OK**.</span></span>

<span data-ttu-id="fc564-132">Para iniciar a depuração, inicie o projeto de cliente no depurador.</span><span class="sxs-lookup"><span data-stu-id="fc564-132">To begin debugging, start your client project in the debugger.</span></span>

<span data-ttu-id="fc564-133">Você também pode depurar seu componente sem iniciar o cliente no depurador.</span><span class="sxs-lookup"><span data-stu-id="fc564-133">You can also debug your component without launching your client in the debugger.</span></span> <span data-ttu-id="fc564-134">Nesse caso, o componente deve iniciar o depurador por conta própria.</span><span class="sxs-lookup"><span data-stu-id="fc564-134">In this case, your component must launch the debugger on its own.</span></span> <span data-ttu-id="fc564-135">Para fazer isso, o projeto de componente deve especificar um executável para a sessão de depuração, juntamente com a ID do aplicativo COM+.</span><span class="sxs-lookup"><span data-stu-id="fc564-135">To do this, your component project must specify an executable for the debug session, along with the COM+ application ID.</span></span>

<span data-ttu-id="fc564-136">**Para habilitar um componente de aplicativo de servidor para iniciar o depurador de Visual C++**</span><span class="sxs-lookup"><span data-stu-id="fc564-136">**To enable a server application component to launch the Visual C++ debugger**</span></span>

1.  <span data-ttu-id="fc564-137">No menu **projeto** , clique em **configurações**.</span><span class="sxs-lookup"><span data-stu-id="fc564-137">On the **Project** menu, click **Settings**.</span></span>

2.  <span data-ttu-id="fc564-138">Na caixa de diálogo **configurações do projeto** , na caixa **configurações de** , selecione **depuração Win32**.</span><span class="sxs-lookup"><span data-stu-id="fc564-138">In the **Project Settings** dialog box, in the **Settings For** box, select **Win32 Debug**.</span></span>

3.  <span data-ttu-id="fc564-139">Na guia **depurar** , na caixa **categoria** , selecione **geral**.</span><span class="sxs-lookup"><span data-stu-id="fc564-139">On the **Debug** tab, in the **Category** box, select **General**.</span></span>

4.  <span data-ttu-id="fc564-140">Na caixa **executável para sessão de depuração** , insira o caminho totalmente qualificado para Dllhost.exe, seguido por um argumento ESPECIFICANDO a ID de aplicativo do aplicativo com+ que contém o componente.</span><span class="sxs-lookup"><span data-stu-id="fc564-140">In the **Executable for debug session** box, enter the fully qualified path for Dllhost.exe, followed by an argument specifying the application ID of the COM+ application containing the component.</span></span>

    > [!Note]  
    > <span data-ttu-id="fc564-141">Usando a ferramenta administrativa serviços de componentes, você encontrará a ID do aplicativo na guia **geral** da caixa de diálogo **Propriedades** do aplicativo com+.</span><span class="sxs-lookup"><span data-stu-id="fc564-141">Using the Component Services administrative tool, you will find the application ID on the **General** tab of the COM+ application's **Properties** dialog box.</span></span> <span data-ttu-id="fc564-142">A seguir está um exemplo:</span><span class="sxs-lookup"><span data-stu-id="fc564-142">Following is an example:</span></span>

     

    > [!Note]  
    > <span data-ttu-id="fc564-143">C: \\ WinNT \\ System32 \\Dllhost.exe/ProcessId: {applicationID}</span><span class="sxs-lookup"><span data-stu-id="fc564-143">C:\\Winnt\\System32\\Dllhost.exe /ProcessID:{applicationID}</span></span>

     

5.  <span data-ttu-id="fc564-144">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="fc564-144">Click **OK**.</span></span>

<span data-ttu-id="fc564-145">Agora você pode definir pontos de interrupção, iniciar o depurador e começar a fazer chamadas para seu componente.</span><span class="sxs-lookup"><span data-stu-id="fc564-145">You can now set breakpoints, start the debugger, and begin making calls to your component.</span></span>

## <a name="debugging-library-application-components-with-visual-c"></a><span data-ttu-id="fc564-146">Depurando componentes de aplicativos de biblioteca com Visual C++</span><span class="sxs-lookup"><span data-stu-id="fc564-146">Debugging Library Application Components with Visual C++</span></span>

<span data-ttu-id="fc564-147">Para depurar componentes em um aplicativo de biblioteca, você deve configurar o projeto do cliente, pois o processo do cliente hospedará o aplicativo de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="fc564-147">To debug components in a library application, you must configure the client's project because the client's process will host the library application.</span></span>

<span data-ttu-id="fc564-148">**Para habilitar a depuração de aplicativo de biblioteca com Visual C++**</span><span class="sxs-lookup"><span data-stu-id="fc564-148">**To enable library application debugging with Visual C++**</span></span>

1.  <span data-ttu-id="fc564-149">No Visual C++, no menu **projeto** , clique em **configurações**.</span><span class="sxs-lookup"><span data-stu-id="fc564-149">In Visual C++, on the **Project** menu, click **Settings**.</span></span>

2.  <span data-ttu-id="fc564-150">Na caixa de diálogo **configurações do projeto** , na caixa **configurações de** , clique em **depuração Win32**.</span><span class="sxs-lookup"><span data-stu-id="fc564-150">In the **Project Settings** dialog box, in the **Settings For** box, click **Win32 Debug**.</span></span>

3.  <span data-ttu-id="fc564-151">Na guia **depurar** , na caixa **categoria** , clique em **DLLs adicionais**.</span><span class="sxs-lookup"><span data-stu-id="fc564-151">On the **Debug** tab, in the **Category** box, click **Additional DLLs**.</span></span>

4.  <span data-ttu-id="fc564-152">Na lista de **módulos** , adicione as DLLs de componentes em seu aplicativo de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="fc564-152">In the **Modules** list, add the component DLLs in your library application.</span></span> <span data-ttu-id="fc564-153">Isso permite que você defina pontos de interrupção antes que sua DLL seja realmente carregada.</span><span class="sxs-lookup"><span data-stu-id="fc564-153">This allows you to set breakpoints before your DLL is actually loaded.</span></span>

5.  <span data-ttu-id="fc564-154">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="fc564-154">Click **OK**.</span></span>

## <a name="debugging-without-visual-c"></a><span data-ttu-id="fc564-155">Depuração sem Visual C++</span><span class="sxs-lookup"><span data-stu-id="fc564-155">Debugging Without Visual C++</span></span>

<span data-ttu-id="fc564-156">Se você estiver ou não usando Visual C++ para depuração, poderá usar a configuração **Iniciar no depurador** para especificar o depurador no qual os componentes devem ser executados.</span><span class="sxs-lookup"><span data-stu-id="fc564-156">Whether or not you are using Visual C++ for debugging, you can use the **Launch in debugger** setting to specify the debugger in which your components should run.</span></span>

<span data-ttu-id="fc564-157">**Para especificar um depurador da ferramenta administrativa serviços de componentes**</span><span class="sxs-lookup"><span data-stu-id="fc564-157">**To specify a debugger from the Component Services administrative tool**</span></span>

1.  <span data-ttu-id="fc564-158">Na árvore de console, selecione o aplicativo de biblioteca COM+ que contém os componentes que você deseja depurar.</span><span class="sxs-lookup"><span data-stu-id="fc564-158">In the console tree, select the COM+ library application containing the components you wish to debug.</span></span>

2.  <span data-ttu-id="fc564-159">Clique com o botão direito do mouse no aplicativo e clique em **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="fc564-159">Right-click the application, and then click **Properties**.</span></span>

3.  <span data-ttu-id="fc564-160">Na caixa de diálogo **Propriedades** do aplicativo, clique na guia **avançado** .</span><span class="sxs-lookup"><span data-stu-id="fc564-160">In the application's **Properties** dialog box, click the **Advanced** tab.</span></span>

4.  <span data-ttu-id="fc564-161">Em **depuração**, marque a caixa de seleção **Iniciar no depurador** .</span><span class="sxs-lookup"><span data-stu-id="fc564-161">Under **Debugging**, select the **Launch in debugger** check box.</span></span>

5.  <span data-ttu-id="fc564-162">Na caixa **caminho do depurador** , insira o caminho para o depurador que você deseja usar.</span><span class="sxs-lookup"><span data-stu-id="fc564-162">In the **Debugger path** box, enter path to the debugger you want to use.</span></span> <span data-ttu-id="fc564-163">Você também pode clicar em **procurar** para localizar o depurador.</span><span class="sxs-lookup"><span data-stu-id="fc564-163">You can also click **Browse** to locate the debugger.</span></span> <span data-ttu-id="fc564-164">Veja a seguir um exemplo: C: \\ WinNT \\ System32 \\Ntsd.exe.</span><span class="sxs-lookup"><span data-stu-id="fc564-164">Following is an example: C:\\Winnt\\System32\\Ntsd.exe.</span></span>

6.  <span data-ttu-id="fc564-165">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="fc564-165">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc564-166">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fc564-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc564-167">Componentes de depuração escritos em Visual Basic</span><span class="sxs-lookup"><span data-stu-id="fc564-167">Debugging Components Written in Visual Basic</span></span>](debugging-components-written-in-visual-basic.md)
</dt> </dl>

 

 



