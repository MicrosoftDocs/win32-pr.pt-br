---
title: Introdução com o SDK do Windows Media Player
description: Introdução com o SDK do Windows Media Player
ms.assetid: 47c333dc-dad3-4430-a053-016d2c931f74
keywords:
- Windows Media Player Mobile, plug-ins
- Windows Media Player Mobile, plug-ins de interface do usuário
- Plug-ins móveis do Windows Media Player
- plug-ins, interface do usuário
- plug-ins, Windows Media Player Mobile
- plug-ins de interface do usuário, Windows Media Player Mobile
- Plug-ins de interface do usuário, Windows Media Player Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a962c1f815f820a0b2e8125872baf9d02e301dc
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103644100"
---
# <a name="getting-started-with-the-windows-media-player-sdk"></a><span data-ttu-id="c7e07-110">Introdução com o SDK do Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="c7e07-110">Getting Started with the Windows Media Player SDK</span></span>

<span data-ttu-id="c7e07-111">Para criar seu plug-in, primeiro você precisa instalar o Microsoft eMbedded Visual C++ 4,0 e o Visual Studio 2003.</span><span class="sxs-lookup"><span data-stu-id="c7e07-111">To create your plug-in, you first need to install Microsoft eMbedded Visual C++ 4.0 and Visual Studio 2003.</span></span> <span data-ttu-id="c7e07-112">Você também deve instalar o SDK do Pocket PC 2003 ou o SDK do Smartphone 2003, que são downloads separados.</span><span class="sxs-lookup"><span data-stu-id="c7e07-112">You must also install the Pocket PC 2003 SDK or the Smartphone 2003 SDK, which are separate downloads.</span></span> <span data-ttu-id="c7e07-113">Para compilar e executar o projeto, um dispositivo Pocket PC ou smartphone que executa o sistema operacional Windows Mobile 2003 Second Edition deve ser sincronizado com o computador de desenvolvimento usando o Microsoft ActiveSync® 3.7.1 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="c7e07-113">To compile and run the project, a Pocket PC or Smartphone device running the Windows Mobile 2003 Second Edition operating system must be synchronized with the development computer by using Microsoft ActiveSync® 3.7.1 or later.</span></span>

<span data-ttu-id="c7e07-114">Como os plug-ins da interface do usuário em dispositivos Windows Mobile usam o mesmo modelo de plug-in que as versões da área de trabalho, você pode usar o assistente de plug-in do Windows Media Player como um ponto de partida ao criar um plug-in de interface do usuário em segundo plano que funcionará com o Windows Media Player 10 Mobile.</span><span class="sxs-lookup"><span data-stu-id="c7e07-114">Because UI plug-ins on Windows Mobile devices use the same plug-in model as the desktop versions, you can use the Windows Media Player Plug-in Wizard as a starting point when creating a background UI plug-in that will work with Windows Media Player 10 Mobile.</span></span>

<span data-ttu-id="c7e07-115">Para criar o código de plug-in da interface do usuário, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c7e07-115">To create UI plug-in code, do the following:</span></span>

1.  <span data-ttu-id="c7e07-116">Abra o Visual Studio 2003 e inicie um novo projeto no Visual C++.</span><span class="sxs-lookup"><span data-stu-id="c7e07-116">Open Visual Studio 2003, and start a new project in Visual C++.</span></span>
2.  <span data-ttu-id="c7e07-117">Selecione **Assistente de plug-in do Windows Media Player** no painel **modelos** .</span><span class="sxs-lookup"><span data-stu-id="c7e07-117">Select **Windows Media Player Plug-in Wizard** from the **Templates** pane.</span></span>
3.  <span data-ttu-id="c7e07-118">Nomeie o projeto NetworkPlugin e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="c7e07-118">Name your project NetworkPlugin and click **OK**.</span></span>
4.  <span data-ttu-id="c7e07-119">Selecione **plug-in de interface do usuário** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="c7e07-119">Select **UI Plug-in** and click **Next**.</span></span>
5.  <span data-ttu-id="c7e07-120">Selecione **plano de fundo** e clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="c7e07-120">Select **Background** and click **Next**.</span></span>
6.  <span data-ttu-id="c7e07-121">Clique em **Avançar** para concluir o assistente.</span><span class="sxs-lookup"><span data-stu-id="c7e07-121">Click **Next** to finish the wizard.</span></span> <span data-ttu-id="c7e07-122">Se você pretende monitorar eventos com seu plug-in, você deve verificar a **escuta de eventos** antes de concluir o assistente e deve ler a documentação da interface **IWMPEvents** para descobrir quais eventos têm suporte no Windows Media Player 10 Mobile.</span><span class="sxs-lookup"><span data-stu-id="c7e07-122">If you are going to monitor events with your plug-in, you must check **Listen to events** before finishing the wizard, and you should read the documentation for the **IWMPEvents** interface to find out which events are supported on Windows Media Player 10 Mobile.</span></span>

<span data-ttu-id="c7e07-123">Agora que você criou o código de plug-in da interface do usuário, precisará criar um projeto Windows CE DLL vazio no eMbedded Visual C++ 4,0.</span><span class="sxs-lookup"><span data-stu-id="c7e07-123">Now that you have created your UI plug-in code, you need to create an empty Windows CE DLL project in eMbedded Visual C++ 4.0.</span></span> <span data-ttu-id="c7e07-124">Em seguida, copie os arquivos de origem gerados pelo Assistente para esse novo projeto para que eles sejam compilados com o compilador ARM4.</span><span class="sxs-lookup"><span data-stu-id="c7e07-124">Then copy your wizard-generated source files to that new project so that they will compile with the ARM4 compiler.</span></span>

<span data-ttu-id="c7e07-125">Para criar um projeto vazio</span><span class="sxs-lookup"><span data-stu-id="c7e07-125">To create an empty project</span></span>

1.  <span data-ttu-id="c7e07-126">Inicie um novo projeto no Visual C++ inserido e, em seguida, selecione **stone Dynamic-Link biblioteca** no painel **projetos** .</span><span class="sxs-lookup"><span data-stu-id="c7e07-126">Start a new project in eMbedded Visual C++, and then select **WCE Dynamic-Link Library** from the **Projects** pane.</span></span>
2.  <span data-ttu-id="c7e07-127">Nomeie seu projeto e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="c7e07-127">Name your project and click **OK**.</span></span>
3.  <span data-ttu-id="c7e07-128">Verifique se **um projeto Windows CE dll vazio** está selecionado e clique em **concluir**.</span><span class="sxs-lookup"><span data-stu-id="c7e07-128">Make sure **An empty Windows CE DLL project** is selected, and then click **Finish**.</span></span>
4.  <span data-ttu-id="c7e07-129">Clique no item de menu **projeto** .</span><span class="sxs-lookup"><span data-stu-id="c7e07-129">Click the **Project** menu item.</span></span>
5.  <span data-ttu-id="c7e07-130">Selecione **Adicionar ao projeto** e clique em **arquivos**.</span><span class="sxs-lookup"><span data-stu-id="c7e07-130">Select **Add to Project**, and then click **Files**.</span></span>
6.  <span data-ttu-id="c7e07-131">Selecione os arquivos C++ que você criou com o assistente de plug-in e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="c7e07-131">Select the C++ files you created with the plug-in wizard, and then click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c7e07-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c7e07-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7e07-133">**Criando um plug-in de interface do usuário para o Windows Media Player 10 Mobile**</span><span class="sxs-lookup"><span data-stu-id="c7e07-133">**Creating a User Interface Plug-in for Windows Media Player 10 Mobile**</span></span>](creating-a-user-interface-plug-in-for-windows-media-player-10-mobile.md)
</dt> <dt>

[<span data-ttu-id="c7e07-134">**Interface IWMPEvents**</span><span class="sxs-lookup"><span data-stu-id="c7e07-134">**IWMPEvents Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents)
</dt> </dl>

 

 




