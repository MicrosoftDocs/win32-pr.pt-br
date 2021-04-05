---
description: O Windows Server 2008 R2 adiciona suporte para o reconhecimento de manuscrito do lado do servidor no Windows. Este tópico descreve como reconhecer manuscritos no Windows Server 2008 R2.
ms.assetid: ec22391d-a6e8-49b0-8650-943a661cbcd3
title: Reconhecimento de manuscrito no Windows Server 2008 R2
ms.topic: article
ms.date: 06/02/2020
ms.openlocfilehash: e014a69919c6bdc87b149f761eece14bcc3d69a4
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104008563"
---
# <a name="handwriting-recognition-in-windows-server-2008-r2"></a><span data-ttu-id="b1ab4-104">Reconhecimento de manuscrito no Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b1ab4-104">Handwriting Recognition in Windows Server 2008 R2</span></span>

<span data-ttu-id="b1ab4-105">O Windows Server 2008 R2 dá suporte ao reconhecimento de manuscrito do lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-105">Windows Server 2008 R2 supports server-side handwriting recognition.</span></span> <span data-ttu-id="b1ab4-106">O reconhecimento no lado do servidor permite que um servidor reconheça o conteúdo da entrada à caneta em páginas da Web.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-106">Server-side recognition lets a server recognize content from pen input on Web pages.</span></span> <span data-ttu-id="b1ab4-107">Isso é particularmente útil quando os usuários em uma rede especificam termos que são interpretados usando um dicionário personalizado.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-107">This is particularly useful when users on a network will be specifying terms that are interpreted using a custom dictionary.</span></span> <span data-ttu-id="b1ab4-108">Por exemplo, se você tivesse um aplicativo médico que consultou um banco de dados de servidor para nomes de pacientes, esses nomes poderiam ser adicionados a outro banco de dados que seria referenciado de forma cruzada ao executar pesquisas de um formulário do Silverlight manuscrito.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-108">For example, if you had a medical application that queried a server database for patient names, those names could be added to another database that would be cross-referenced when performing searches from a handwritten Silverlight form.</span></span>

## <a name="set-up-your-server-for-server-side-recognition"></a><span data-ttu-id="b1ab4-109">Configurar o servidor para o reconhecimento de Server-Side</span><span class="sxs-lookup"><span data-stu-id="b1ab4-109">Set up your Server for Server-Side Recognition</span></span>

<span data-ttu-id="b1ab4-110">As etapas a seguir devem ser seguidas para configurar o reconhecimento do lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-110">The following steps should be followed to set up server-side recognition.</span></span>

- <span data-ttu-id="b1ab4-111">Instalar Serviços de Reconhecimento de Manuscrito</span><span class="sxs-lookup"><span data-stu-id="b1ab4-111">Install Ink and Handwriting Services</span></span>
- <span data-ttu-id="b1ab4-112">Instalar o suporte para o servidor Web (IIS) e o servidor de aplicativos</span><span class="sxs-lookup"><span data-stu-id="b1ab4-112">Install Support for Web Server (IIS) and Application Server</span></span>
- <span data-ttu-id="b1ab4-113">Habilitar a função de experiência desktop</span><span class="sxs-lookup"><span data-stu-id="b1ab4-113">Enable the Desktop Experience Role</span></span>
- <span data-ttu-id="b1ab4-114">Iniciar o serviço de entrada do Tablet PC</span><span class="sxs-lookup"><span data-stu-id="b1ab4-114">Start the Tablet PC Input Service</span></span>

### <a name="install-ink-and-handwriting-services"></a><span data-ttu-id="b1ab4-115">Instalar Serviços de Reconhecimento de Manuscrito</span><span class="sxs-lookup"><span data-stu-id="b1ab4-115">Install Ink and Handwriting Services</span></span>

<span data-ttu-id="b1ab4-116">Para instalar os serviços de tinta e manuscrito, abra o Gerenciador de servidores clicando no ícone Gerenciador de servidores na bandeja de início rápido.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-116">To install Ink and Handwriting services, open the server manager by clicking the server manager icon from the Quick Launch tray.</span></span> <span data-ttu-id="b1ab4-117">No menu **recursos** , clique em **Adicionar recursos**.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-117">From the **Features** menu, click **Add Features**.</span></span> <span data-ttu-id="b1ab4-118">Certifique-se de marcar a caixa de seleção **serviços de reconhecimento de manuscrito** .</span><span class="sxs-lookup"><span data-stu-id="b1ab4-118">Make sure that you select the **Ink and Handwriting Services** check box.</span></span> <span data-ttu-id="b1ab4-119">A imagem a seguir mostra a caixa de diálogo **selecionar recursos** com **serviços de reconhecimento de manuscrito** selecionado.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-119">The following image shows the **Select Features** dialog box with **Ink and Handwriting Services** selected.</span></span>

<span data-ttu-id="b1ab4-120">![Caixa de diálogo Selecionar recursos com a caixa de seleção serviços de tinta e manuscrito marcada](images/setup-server-1-ink-and-handwriting.png)</span><span class="sxs-lookup"><span data-stu-id="b1ab4-120">![Select features dialog box with ink and handwriting services check box selected](images/setup-server-1-ink-and-handwriting.png)</span></span><br/>
<span data-ttu-id="b1ab4-121">*Caixa de diálogo Selecionar recursos com a caixa de seleção serviços de tinta e manuscrito marcada*</span><span class="sxs-lookup"><span data-stu-id="b1ab4-121">*Select features dialog box with ink and handwriting services check box selected*</span></span>

### <a name="installation-support-for-web-server-iis-and-application-server"></a><span data-ttu-id="b1ab4-122">Suporte para instalação do servidor Web (IIS) e servidor de aplicativos</span><span class="sxs-lookup"><span data-stu-id="b1ab4-122">Installation Support for Web Server (IIS) and Application Server</span></span>

<span data-ttu-id="b1ab4-123">Abra o Gerenciador de servidores como você fez para a primeira etapa.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-123">Open the server manager as you did for the first step.</span></span> <span data-ttu-id="b1ab4-124">Em seguida, você precisará adicionar o servidor Web (IIS) e as funções de servidor de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-124">Next, you will need to add the Web Server (IIS) and Application Server roles.</span></span> <span data-ttu-id="b1ab4-125">No menu **funções** , clique em **adicionar funções**.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-125">From the **Roles** menu, click **Add Roles**.</span></span> <span data-ttu-id="b1ab4-126">O assistente para adicionar funções é exibido.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-126">The Add Roles wizard appears.</span></span> <span data-ttu-id="b1ab4-127">Clique em **Próximo**.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-127">Click **Next**.</span></span> <span data-ttu-id="b1ab4-128">Verifique se **servidor de aplicativos** e **servidor Web (IIS)** estão selecionados.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-128">Make sure **Application Server** and **Web Server (IIS)** are selected.</span></span> <span data-ttu-id="b1ab4-129">A imagem a seguir mostra a caixa de diálogo **selecionar funções de servidor** com o **servidor Web (IIS)** e funções de **servidor de aplicativos** selecionadas.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-129">The following image shows the **Select Server Roles** dialog box with the **Web Server (IIS)** and **Application Server** roles selected.</span></span>

<span data-ttu-id="b1ab4-130">![Caixa de diálogo Selecionar funções de servidor com servidor Web (IIS) e funções de servidor de aplicativos selecionadas](images/setup-server-2-select-server-roles.png)</span><span class="sxs-lookup"><span data-stu-id="b1ab4-130">![Select server roles dialog box with web server (iis) and application server roles selected](images/setup-server-2-select-server-roles.png)</span></span><br/>
<span data-ttu-id="b1ab4-131">*Caixa de diálogo Selecionar funções de servidor com servidor Web (IIS) e funções de servidor de aplicativos selecionadas*</span><span class="sxs-lookup"><span data-stu-id="b1ab4-131">*Select server roles dialog box with web server (iis) and application server roles selected*</span></span>

<span data-ttu-id="b1ab4-132">Ao selecionar **servidor de aplicativos**, você será solicitado a instalar a estrutura ASP.net.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-132">When you select **Application Server**, you will be asked to install the ASP.NET framework.</span></span> <span data-ttu-id="b1ab4-133">Clique no botão **Adicionar recursos necessários** .</span><span class="sxs-lookup"><span data-stu-id="b1ab4-133">Click the **Add the Required Features** button.</span></span> <span data-ttu-id="b1ab4-134">Depois de clicar em **Avançar**, você verá uma caixa de diálogo visão geral; clique em **Avançar**.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-134">After you click **Next**, you will be presented with an overview dialog box; click **Next**.</span></span> <span data-ttu-id="b1ab4-135">A caixa de diálogo **selecionar serviços de função** agora deve estar disponível.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-135">The **Select Role Services** dialog box should now be available.</span></span> <span data-ttu-id="b1ab4-136">Verifique se o **servidor Web (IIS)** está selecionado.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-136">Make sure that **Web Server (IIS)** is selected.</span></span> <span data-ttu-id="b1ab4-137">A imagem a seguir mostra a caixa de diálogo **selecionar serviços de função** com o servidor Web (IIS) habilitado.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-137">The following image shows the **Select Role Services** dialog box with Web Server (IIS) enabled.</span></span>

<span data-ttu-id="b1ab4-138">![Caixa de diálogo Selecionar Serviços de função com o servidor Web (IIS) habilitado](images/setup-server-3-select-role-services.png)</span><span class="sxs-lookup"><span data-stu-id="b1ab4-138">![Select role services dialog box with web server (iis) enabled](images/setup-server-3-select-role-services.png)</span></span><br/>
<span data-ttu-id="b1ab4-139">*Caixa de diálogo Selecionar Serviços de função com o servidor Web (IIS) habilitado*</span><span class="sxs-lookup"><span data-stu-id="b1ab4-139">*Select role services dialog box with web server (iis) enabled*</span></span>

<span data-ttu-id="b1ab4-140">Clique em **Próximo**.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-140">Click **Next**.</span></span> <span data-ttu-id="b1ab4-141">Uma caixa de diálogo visão geral é exibida; clique em **Avançar** novamente.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-141">An overview dialog box appears; click **Next** again.</span></span> <span data-ttu-id="b1ab4-142">Agora você verá uma página que oferece opções para funções para o servidor Web (IIS).</span><span class="sxs-lookup"><span data-stu-id="b1ab4-142">You will now be presented with a page offering you options for roles for Web Server (IIS).</span></span> <span data-ttu-id="b1ab4-143">Clique em **Próximo**.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-143">Click **Next**.</span></span> <span data-ttu-id="b1ab4-144">Na próxima página, o botão **instalar** ficará ativo.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-144">On the next page, the **Install** button will become active.</span></span> <span data-ttu-id="b1ab4-145">Clique em **instalar** e você instalará o suporte para o servidor Web (IIS) e o servidor de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-145">Click **Install** and you will install support for Web Server (IIS) and Application Server.</span></span>

### <a name="enable-the-desktop-experience-role"></a><span data-ttu-id="b1ab4-146">Habilitar a função de experiência desktop</span><span class="sxs-lookup"><span data-stu-id="b1ab4-146">Enable the Desktop Experience Role</span></span>

<span data-ttu-id="b1ab4-147">Para habilitar a experiência desktop, clique em **Iniciar**, **Ferramentas administrativas** e, em seguida, clique em **Gerenciador do servidor**.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-147">To enable the desktop experience, click **Start**, click **Administrative Tools**, and then click **Server Manager**.</span></span> <span data-ttu-id="b1ab4-148">Selecione **Adicionar serviços** e, em seguida, selecione o serviço **experiência desktop** .</span><span class="sxs-lookup"><span data-stu-id="b1ab4-148">Select **Add Services** and then select the **Desktop Experience** service.</span></span> <span data-ttu-id="b1ab4-149">A imagem a seguir mostra a caixa de diálogo **selecionar recursos** com o item de experiência desktop instalado.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-149">The following image shows the **Select Features** dialog box with the Desktop Experience item installed.</span></span>

<span data-ttu-id="b1ab4-150">![Caixa de diálogo Selecionar recursos com o serviço de experiência de área de trabalho selecionado](images/setup-server-4-desktop-experience.png)</span><span class="sxs-lookup"><span data-stu-id="b1ab4-150">![Select features dialog box with desktop experience service selected](images/setup-server-4-desktop-experience.png)</span></span><br/>
<span data-ttu-id="b1ab4-151">*Caixa de diálogo Selecionar recursos com o serviço de experiência de área de trabalho selecionado*</span><span class="sxs-lookup"><span data-stu-id="b1ab4-151">*Select features dialog box with desktop experience service selected*</span></span>

<span data-ttu-id="b1ab4-152">Clique em **Avançar** para instalar a experiência desktop.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-152">Click **Next** to install the Desktop Experience.</span></span>

### <a name="start-the-tablet-service"></a><span data-ttu-id="b1ab4-153">Iniciar o serviço do Tablet</span><span class="sxs-lookup"><span data-stu-id="b1ab4-153">Start the Tablet Service</span></span>

<span data-ttu-id="b1ab4-154">Depois de instalar o serviço de experiência desktop, o serviço de entrada do Tablet PC será exibido no menu **Serviços** .</span><span class="sxs-lookup"><span data-stu-id="b1ab4-154">After you have installed the Desktop Experience service, the Tablet PC Input service will appear in the **Services** menu.</span></span> <span data-ttu-id="b1ab4-155">Para acessar o menu **Serviços** , clique em **Iniciar**, **Ferramentas administrativas** e, em seguida, clique em **Serviços**.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-155">To access the **Services** menu, click **Start**, click **Administrative Tools**, and then click **Services**.</span></span> <span data-ttu-id="b1ab4-156">Para iniciar o serviço, clique com o botão direito do mouse em **serviço de entrada do Tablet PC** e clique em **Iniciar**.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-156">To start the service, right-click **Tablet PC Input Service** and then click **Start**.</span></span> <span data-ttu-id="b1ab4-157">A imagem a seguir mostra o menu **Serviços** com o serviço de entrada do Tablet PC iniciado.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-157">The following image shows the **Services** menu with the Tablet PC Input Service started.</span></span>

<span data-ttu-id="b1ab4-158">![Menu de serviços com o serviço de entrada do Tablet PC iniciado](images/setup-server-5-tablet-pc-input-service.png)</span><span class="sxs-lookup"><span data-stu-id="b1ab4-158">![Services menu with the tablet pc input service started](images/setup-server-5-tablet-pc-input-service.png)</span></span><br/>
<span data-ttu-id="b1ab4-159">*Menu de serviços com o serviço de entrada do Tablet PC iniciado*</span><span class="sxs-lookup"><span data-stu-id="b1ab4-159">*Services menu with the tablet pc input service started*</span></span>

## <a name="performing-server-side-recognition-using-silverlight"></a><span data-ttu-id="b1ab4-160">Executando o reconhecimento de Server-Side usando o Silverlight</span><span class="sxs-lookup"><span data-stu-id="b1ab4-160">Performing Server-Side Recognition Using Silverlight</span></span>

<span data-ttu-id="b1ab4-161">Esta seção mostra como criar um aplicativo Web que usa o Silverlight para capturar a entrada de manuscrito.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-161">This section shows how to create a Web application that uses Silverlight to capture handwriting input.</span></span> <span data-ttu-id="b1ab4-162">Use as etapas a seguir para programar o reconhecedor no Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-162">Use the following steps to program the recognizer in Visual Studio 2008.</span></span>

- <span data-ttu-id="b1ab4-163">Instale e atualize o Visual Studio 2008 para adicionar suporte ao Silverlight.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-163">Install and update Visual Studio 2008 to add support for Silverlight.</span></span>
- <span data-ttu-id="b1ab4-164">Crie um novo projeto do Silverlight no Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-164">Create a new Silverlight project in Visual Studio 2008.</span></span>
- <span data-ttu-id="b1ab4-165">Adicione as referências de serviço necessárias ao seu projeto.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-165">Add the necessary service references to your project.</span></span>
- <span data-ttu-id="b1ab4-166">Crie um serviço WCF do Silverlight para reconhecimento de tinta.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-166">Create a Silverlight WCF Service for ink recognition.</span></span>
- <span data-ttu-id="b1ab4-167">Adicione a referência de serviço ao seu projeto de cliente.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-167">Add the service reference to your client project.</span></span>
- <span data-ttu-id="b1ab4-168">Adicione a classe InkCollector ao projeto InkRecognition.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-168">Add the InkCollector class to the InkRecognition project.</span></span>
- <span data-ttu-id="b1ab4-169">Remover diretivas de transporte seguras da configuração do cliente</span><span class="sxs-lookup"><span data-stu-id="b1ab4-169">Remove secure transport directives from the client configuration</span></span>

### <a name="install-and-update-visual-studio-2008-to-add-support-for-silverlight"></a><span data-ttu-id="b1ab4-170">Instalar e atualizar o Visual Studio 2008 para adicionar suporte ao Silverlight</span><span class="sxs-lookup"><span data-stu-id="b1ab4-170">Install and Update Visual Studio 2008 to Add Support for Silverlight</span></span>

<span data-ttu-id="b1ab4-171">Antes de começar, você deve executar as etapas a seguir no servidor Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-171">Before you begin, you must perform the following steps on your Windows Server 2008 R2 server.</span></span>

- <span data-ttu-id="b1ab4-172">Instale o Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-172">Install Visual Studio 2008.</span></span>
- <span data-ttu-id="b1ab4-173">Instale o [Microsoft Visual Studio 2008 Service Pack 1](https://www.microsoft.com/download/details.aspx?id=10986).</span><span class="sxs-lookup"><span data-stu-id="b1ab4-173">Install [Microsoft Visual Studio 2008 Service Pack 1](https://www.microsoft.com/download/details.aspx?id=10986).</span></span>
- <span data-ttu-id="b1ab4-174">Instale [o SDK do Microsoft Silverlight 5](https://www.microsoft.com/silverlight/).</span><span class="sxs-lookup"><span data-stu-id="b1ab4-174">Install [Microsoft Silverlight 5 SDK](https://www.microsoft.com/silverlight/).</span></span>

<span data-ttu-id="b1ab4-175">Depois de instalar esses aplicativos e atualizações, você estará pronto para criar o aplicativo Web de reconhecimento do lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-175">After you have installed these applications and updates, you are ready to create your server-side recognition Web application.</span></span>

### <a name="create-a-new-silverlight-web-project-in-visual-studio-2008"></a><span data-ttu-id="b1ab4-176">Criar um novo projeto Web do Silverlight no Visual Studio 2008</span><span class="sxs-lookup"><span data-stu-id="b1ab4-176">Create a new Silverlight Web Project in Visual Studio 2008</span></span>

<span data-ttu-id="b1ab4-177">No menu **Arquivo**, clique em **Novo Projeto**.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-177">From the **File** menu, click **New Project**.</span></span> <span data-ttu-id="b1ab4-178">Selecione o modelo de aplicativo do Silverlight na lista de projetos do Visual C \# .</span><span class="sxs-lookup"><span data-stu-id="b1ab4-178">Select the Silverlight Application template from the Visual C\# project list.</span></span> <span data-ttu-id="b1ab4-179">Nomeie o projeto InkRecognition e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-179">Name your project InkRecognition and click **OK**.</span></span> <span data-ttu-id="b1ab4-180">A imagem a seguir mostra o \# projeto C Silverlight selecionado e nomeado InkRecognition.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-180">The following image shows the C\# Silverlight project selected and named InkRecognition.</span></span>

<span data-ttu-id="b1ab4-181">![\#projeto Silverlight c selecionado, com o nome InkRecognition](images/project-1-new-project.png)</span><span class="sxs-lookup"><span data-stu-id="b1ab4-181">![c\# silverlight project selected, with the name inkrecognition](images/project-1-new-project.png)</span></span><br/>
<span data-ttu-id="b1ab4-182">*\#projeto Silverlight c selecionado, com o nome InkRecognition*</span><span class="sxs-lookup"><span data-stu-id="b1ab4-182">*c\# silverlight project selected, with the name inkrecognition*</span></span>

<span data-ttu-id="b1ab4-183">Depois de clicar em **OK**, uma caixa de diálogo solicitará que você adicione um aplicativo do Silverlight ao seu projeto.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-183">After you click **OK**, a dialog box prompts you to add a Silverlight application to your project.</span></span> <span data-ttu-id="b1ab4-184">Selecione **Adicionar um novo projeto Web ASP.net à solução para hospedar o Silverlight** e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-184">Select **Add a new ASP.NET Web project to the solution to host Silverlight** and click **OK**.</span></span> <span data-ttu-id="b1ab4-185">A imagem a seguir mostra como configurar o projeto de exemplo antes de clicar em **OK**.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-185">The following image shows how to set up the example project before you click **OK**.</span></span>

<span data-ttu-id="b1ab4-186">![Caixa de diálogo com solicitação para adicionar um aplicativo do Silverlight a um projeto](images/project-2-add-a-new-aspnetproject.png)</span><span class="sxs-lookup"><span data-stu-id="b1ab4-186">![Dialog box with prompt for adding a silverlight application to a project](images/project-2-add-a-new-aspnetproject.png)</span></span><br/>
<span data-ttu-id="b1ab4-187">*Caixa de diálogo com solicitação para adicionar um aplicativo do Silverlight a um projeto*</span><span class="sxs-lookup"><span data-stu-id="b1ab4-187">*Dialog box with prompt for adding a silverlight application to a project*</span></span>

### <a name="add-the-necessary-service-references-to-your-project"></a><span data-ttu-id="b1ab4-188">Adicionar as referências de serviço necessárias ao seu projeto</span><span class="sxs-lookup"><span data-stu-id="b1ab4-188">Add the Necessary Service References to your Project</span></span>

<span data-ttu-id="b1ab4-189">Agora você tem o projeto de cliente Silverlight genérico (InkRecognition) com um projeto Web (InkRecognition. Web) configurado em sua solução.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-189">Now you have your generic Silverlight client project (InkRecognition) with a Web project (InkRecognition.Web) set up in your solution.</span></span> <span data-ttu-id="b1ab4-190">O projeto será aberto com Page. XAML e default. aspx aberto.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-190">The project will open with Page.xaml and Default.aspx open.</span></span> <span data-ttu-id="b1ab4-191">Feche essas janelas e adicione as referências System. Runtime. Serialization e System. ServiceModel ao projeto InkRecognition clicando com o botão direito do mouse na pasta referências no projeto InkRecognition e selecionando **Adicionar referência**.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-191">Close these windows and add the System.Runtime.Serialization and System.ServiceModel references to the InkRecognition project by right-clicking on the references folder in the InkRecognition project and selecting **Add Reference**.</span></span> <span data-ttu-id="b1ab4-192">A imagem a seguir mostra a caixa de diálogo com as referências de requisito selecionadas.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-192">The following image shows the dialog box with the requisite references selected.</span></span>

<span data-ttu-id="b1ab4-193">![Caixa de diálogo Adicionar referências com System. Runtime. Serialization e System. ServiceModel selecionados](images/project-3a-add-references-to-inkreco.png)</span><span class="sxs-lookup"><span data-stu-id="b1ab4-193">![Add references dialog box with system.runtime.serialization and system.servicemodel selected](images/project-3a-add-references-to-inkreco.png)</span></span><br/>
<span data-ttu-id="b1ab4-194">*Caixa de diálogo Adicionar referências com System. Runtime. Serialization e System. ServiceModel selecionados*</span><span class="sxs-lookup"><span data-stu-id="b1ab4-194">*Add references dialog box with system.runtime.serialization and system.servicemodel selected*</span></span>

<span data-ttu-id="b1ab4-195">Em seguida, você precisa adicionar as referências de System. ServiceModel e Microsoft. Ink ao projeto InkRecognition. Web.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-195">Next, you need to add the System.ServiceModel and Microsoft.Ink references to the InkRecognition.Web project.</span></span> <span data-ttu-id="b1ab4-196">A referência de Microsoft. Ink não aparecerá nas referências do .NET por padrão, portanto, pesquise a pasta do Windows para Microsoft.Ink.dll.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-196">The Microsoft.Ink reference will not appear in the .NET references by default, so search your Windows folder for Microsoft.Ink.dll.</span></span> <span data-ttu-id="b1ab4-197">Depois de localizar a DLL, adicione o assembly às referências do projeto: selecione a guia **procurar** , altere para a pasta que contém Microsoft.Ink.dll, selecione Microsoft.Ink.dll e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-197">After you have located the DLL, add the assembly to the project references: select the **Browse** tab, change to the folder containing Microsoft.Ink.dll, select Microsoft.Ink.dll, and then click **OK**.</span></span> <span data-ttu-id="b1ab4-198">A imagem a seguir mostra a solução do projeto no Windows Explorer com todos os assemblies de referência adicionados.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-198">The following image shows the project's solution in Windows Explorer with all of the reference assemblies added.</span></span>

<span data-ttu-id="b1ab4-199">![projeto InkRecognition no Windows Explorer com todos os assemblies de referência adicionados](images/project-3b-with-reference-assemblies.png)</span><span class="sxs-lookup"><span data-stu-id="b1ab4-199">![inkrecognition project in windows explorer with all reference assemblies added](images/project-3b-with-reference-assemblies.png)</span></span><br/>
<span data-ttu-id="b1ab4-200">*projeto InkRecognition no Windows Explorer com todos os assemblies de referência adicionados*</span><span class="sxs-lookup"><span data-stu-id="b1ab4-200">*inkrecognition project in windows explorer with all reference assemblies added*</span></span>

### <a name="create-a-silverlight-wcf-service-for-ink-recognition"></a><span data-ttu-id="b1ab4-201">Criar um serviço WCF do Silverlight para reconhecimento de tinta</span><span class="sxs-lookup"><span data-stu-id="b1ab4-201">Create a Silverlight WCF Service for Ink Recognition</span></span>

<span data-ttu-id="b1ab4-202">Em seguida, você adicionará um serviço WCF para reconhecimento de tinta ao projeto.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-202">Next, you will add a WCF service for ink recognition to the project.</span></span> <span data-ttu-id="b1ab4-203">Clique com o botão direito do mouse no projeto InkRecognition. Web, clique em **Adicionar** e em **novo item**.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-203">Right-click your InkRecognition.Web project, click **Add**, and then click **New Item**.</span></span> <span data-ttu-id="b1ab4-204">Selecione o modelo de serviço WCF Silverlight, altere o nome para InkRecogitionService e clique em **Adicionar**.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-204">Select the WCF Silverlight Service template, change the name to InkRecogitionService, and then click **Add**.</span></span> <span data-ttu-id="b1ab4-205">A imagem a seguir mostra a caixa de diálogo **Adicionar novo item** com o serviço WCF do Silverlight selecionado e nomeado.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-205">The following image shows the **Add New Item** dialog box with the Silverlight WCF service selected and named.</span></span>

<span data-ttu-id="b1ab4-206">![Caixa de diálogo Adicionar novo item com o serviço WCF do Silverlight selecionado e nomeado](images/project-4-add-wcf-service.png)</span><span class="sxs-lookup"><span data-stu-id="b1ab4-206">![Add new item dialog box with silverlight wcf service selected and named](images/project-4-add-wcf-service.png)</span></span><br/>
<span data-ttu-id="b1ab4-207">*Caixa de diálogo Adicionar novo item com o serviço WCF do Silverlight selecionado e nomeado*</span><span class="sxs-lookup"><span data-stu-id="b1ab4-207">*Add new item dialog box with silverlight wcf service selected and named*</span></span>

<span data-ttu-id="b1ab4-208">Depois de adicionar o serviço WCF Silverlight, o código de serviço por trás do, InkRecognitionService. cs, será aberto.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-208">After you add the WCF Silverlight service, the service code behind, InkRecognitionService.cs, will open.</span></span> <span data-ttu-id="b1ab4-209">Substitua o código do serviço pelo código a seguir.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-209">Replace the service code with the following code.</span></span>

```CSharp
using System;
using System.Linq;
using System.Runtime.Serialization;
using System.ServiceModel;
using System.ServiceModel.Activation;
using System.Collections.Generic;
using System.Text;
using Microsoft.Ink;

namespace InkRecognition.Web
{
    [ServiceContract(Namespace = "")]
    [AspNetCompatibilityRequirements(RequirementsMode = AspNetCompatibilityRequirementsMode.Allowed)]
    public class InkRecognitionService
    {
        [OperationContract]
        public string[] Recognize(int[][] packets)
        {
            // Deserialize ink.
            Ink ink = new Ink();
            Tablet tablet = new Tablets().DefaultTablet;
            TabletPropertyDescriptionCollection desc = new TabletPropertyDescriptionCollection();
            desc.Add(new TabletPropertyDescription(PacketProperty.X, tablet.GetPropertyMetrics(PacketProperty.X)));
            desc.Add(new TabletPropertyDescription(PacketProperty.Y, tablet.GetPropertyMetrics(PacketProperty.Y)));
            int numOfStrokes = packets.GetUpperBound(0) + 1;
            for (int i = 0; i < numOfStrokes; i++)
            {
                ink.CreateStroke(packets[i], desc);
            }

            // Recognize ink.
            RecognitionStatus recoStatus;
            RecognizerContext recoContext = new RecognizerContext();
            recoContext.RecognitionFlags = RecognitionModes.LineMode | RecognitionModes.TopInkBreaksOnly;
            recoContext.Strokes = ink.Strokes;
            RecognitionResult recoResult = recoContext.Recognize(out recoStatus);
            RecognitionAlternates alternates = recoResult.GetAlternatesFromSelection();
            string[] results = new string[alternates.Count];
            for (int i = 0; i < alternates.Count; i++)
            {
                results[i] = alternates[i].ToString();
            }

            // Send results to client.
            return results;
        }
    }
}
```

### <a name="add-the-service-reference-to-your-client-project"></a><span data-ttu-id="b1ab4-210">Adicionar a referência de serviço ao seu projeto de cliente</span><span class="sxs-lookup"><span data-stu-id="b1ab4-210">Add the Service Reference to your Client Project</span></span>

<span data-ttu-id="b1ab4-211">Agora que você tem o serviço WCF do Silverlight para InkRecognition, você consumirá o serviço do seu aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-211">Now that you have your Silverlight WCF service for InkRecognition, you will consume the service from your client application.</span></span> <span data-ttu-id="b1ab4-212">Clique com o botão direito do mouse no projeto InkRecognition e selecione **Adicionar referência de serviço**.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-212">Right-click the InkRecognition project and select **Add Service Reference**.</span></span> <span data-ttu-id="b1ab4-213">Na caixa de diálogo **Adicionar referência de serviço** exibida, selecione **descobrir** para descobrir serviços da solução atual.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-213">From the **Add Service Reference** dialog box that appears, select **Discover** to discover services from the current solution.</span></span> <span data-ttu-id="b1ab4-214">InkRecognitionService aparecerá no painel serviços.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-214">InkRecognitionService will appear in the Services pane.</span></span> <span data-ttu-id="b1ab4-215">Clique duas vezes em InkRecognitionService no painel serviços, altere o namespace para InkRecognitionServiceReference e clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-215">Double-click InkRecognitionService from the Services pane, change the namespace to InkRecognitionServiceReference, and then click **OK**.</span></span> <span data-ttu-id="b1ab4-216">A imagem a seguir mostra a caixa de diálogo **Adicionar referência de serviço** com InkRecognitionService selecionado e o namespace alterado.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-216">The following image shows the **Add Service Reference** dialog box with InkRecognitionService selected and the namespace changed.</span></span>

<span data-ttu-id="b1ab4-217">![Caixa de diálogo Adicionar referência de serviço com inkrecognitionservice selecionado e namespace alterado](images/project-5-discover-service-reference.png)</span><span class="sxs-lookup"><span data-stu-id="b1ab4-217">![Add service reference dialog box with inkrecognitionservice selected and namespace changed](images/project-5-discover-service-reference.png)</span></span><br/>
<span data-ttu-id="b1ab4-218">*Caixa de diálogo Adicionar referência de serviço com inkrecognitionservice selecionado e namespace alterado*</span><span class="sxs-lookup"><span data-stu-id="b1ab4-218">*Add service reference dialog box with inkrecognitionservice selected and namespace changed*</span></span>

### <a name="add-the-inkcollector-class-to-the-inkrecognition-project"></a><span data-ttu-id="b1ab4-219">Adicionar a classe InkCollector ao projeto InkRecognition</span><span class="sxs-lookup"><span data-stu-id="b1ab4-219">Add the InkCollector Class to the InkRecognition Project</span></span>

<span data-ttu-id="b1ab4-220">Clique com o botão direito do mouse no projeto InkRecognition, clique em **Adicionar** e em **novo item**.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-220">Right-click the InkRecognition project, click **Add**, and then click **New Item**.</span></span> <span data-ttu-id="b1ab4-221">No menu do **Visual \# c** , selecione **\# classe C**.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-221">From the **Visual C\#** menu, select **C\# class**.</span></span> <span data-ttu-id="b1ab4-222">Nomeie a classe como InkCollector.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-222">Name the class InkCollector.</span></span> <span data-ttu-id="b1ab4-223">A imagem a seguir mostra a caixa de diálogo com a \# classe C selecionada e nomeada.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-223">The following image shows the dialog box with the C\# class selected and named.</span></span>

<span data-ttu-id="b1ab4-224">![Caixa de diálogo Adicionar novo item com a \# classe c selecionada e nomeada](images/project-6-add-ink-collector.png)</span><span class="sxs-lookup"><span data-stu-id="b1ab4-224">![Add new item dialog box with c\# class selected and named](images/project-6-add-ink-collector.png)</span></span><br/>
<span data-ttu-id="b1ab4-225">*Caixa de diálogo Adicionar novo item com a \# classe c selecionada e nomeada*</span><span class="sxs-lookup"><span data-stu-id="b1ab4-225">*Add new item dialog box with c\# class selected and named*</span></span>

<span data-ttu-id="b1ab4-226">Depois de adicionar a classe InkCollector, a definição de classe será aberta.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-226">After you add the InkCollector class, the class definition will open.</span></span> <span data-ttu-id="b1ab4-227">Substitua o código no coletor de tinta pelo código a seguir.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-227">Replace the code in the Ink Collector with the following code.</span></span>

```CSharp
using System;
using System.Net;
using System.Windows;
using System.Windows.Controls;
using System.Windows.Documents;
using System.Windows.Ink;
using System.Windows.Input;
using System.Windows.Media;
using System.Windows.Media.Animation;
using System.Windows.Shapes;

namespace InkRecognition
{
    public class InkCollector : IDisposable
    {
        public InkCollector(InkPresenter presenter)
        {
            _presenter = presenter;
            _presenter.Cursor = Cursors.Stylus;
            _presenter.MouseLeftButtonDown += new MouseButtonEventHandler(_presenter_MouseLeftButtonDown);
            _presenter.MouseMove += new MouseEventHandler(_presenter_MouseMove);
            _presenter.MouseLeftButtonUp += new MouseButtonEventHandler(_presenter_MouseLeftButtonUp);
        }

        void _presenter_MouseLeftButtonDown(object sender, MouseButtonEventArgs e)
        {
            _presenter.CaptureMouse();
            if (!e.StylusDevice.Inverted)
            {
                _presenter.Cursor = Cursors.Stylus;
                _stroke = new Stroke(e.StylusDevice.GetStylusPoints(_presenter));
                _stroke.DrawingAttributes = _drawingAttributes;
                _presenter.Strokes.Add(_stroke);
            }
            else
            {
                _presenter.Cursor = Cursors.Eraser;
                _erasePoints = e.StylusDevice.GetStylusPoints(_presenter);
            }
        }

        void _presenter_MouseMove(object sender, MouseEventArgs e)
        {
            if (!e.StylusDevice.Inverted)
            {
                _presenter.Cursor = Cursors.Stylus;
            }
            else
            {
                _presenter.Cursor = Cursors.Eraser;
            }
            if (_stroke != null)
            {
                _stroke.StylusPoints.Add(e.StylusDevice.GetStylusPoints(_presenter));
            }
            else if (_erasePoints != null)
            {
                _erasePoints.Add(e.StylusDevice.GetStylusPoints(_presenter));
                StrokeCollection hitStrokes = _presenter.Strokes.HitTest(_erasePoints);
                if (hitStrokes.Count > 0)
                {
                    foreach (Stroke hitStroke in hitStrokes)
                    {
                        _presenter.Strokes.Remove(hitStroke);
                    }
                }
            }
        }

        void _presenter_MouseLeftButtonUp(object sender, MouseButtonEventArgs e)
        {
            _presenter.ReleaseMouseCapture();
            if (_stroke != null)
            {
                _stroke.StylusPoints.Add(e.StylusDevice.GetStylusPoints(_presenter));
            }
            _stroke = null;
            _erasePoints = null;
        }

        public DrawingAttributes DefaultDrawingAttributes
        {
            get { return _drawingAttributes; }
            set { _drawingAttributes = value; }
        }

        public void Dispose()
        {
            _presenter.MouseLeftButtonDown -= new MouseButtonEventHandler(_presenter_MouseLeftButtonDown);
            _presenter.MouseMove -= new MouseEventHandler(_presenter_MouseMove);
            _presenter.MouseLeftButtonUp -= new MouseButtonEventHandler(_presenter_MouseLeftButtonUp);
            _presenter = null;
        }

        private InkPresenter _presenter = null;
        private Stroke _stroke = null;
        private StylusPointCollection _erasePoints = null;
        private DrawingAttributes _drawingAttributes = new DrawingAttributes();
    }
}
```

### <a name="update-the-xaml-for-the-default-page-and-add-a-code-behind-for-handwriting-recognition"></a><span data-ttu-id="b1ab4-228">Atualizar o XAML para a página padrão e adicionar um code-behind para reconhecimento de manuscrito</span><span class="sxs-lookup"><span data-stu-id="b1ab4-228">Update the XAML for the Default Page and Add a Code Behind for Handwriting Recognition</span></span>

<span data-ttu-id="b1ab4-229">Agora que você tem uma classe que coleta tinta, será necessário atualizar o XAML em Page. XAML com o XAML a seguir.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-229">Now that you have a class that collects ink, you will need to update the XAML in page.xaml with the following XAML.</span></span> <span data-ttu-id="b1ab4-230">O código a seguir adiciona um gradiente amarelo à área de entrada, um controle InkCanvas e um botão que irá disparar o reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-230">The following code adds a yellow gradient to the input area, an InkCanvas control, and a button that will trigger recognition.</span></span>

```XML
<UserControl x:Class="InkRecognition.Page"
    xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation" 
    xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml">
    <Grid x:Name="LayoutRoot" Background="White">
        <Grid.RowDefinitions>
            <RowDefinition Height="Auto"/>
            <RowDefinition Height="Auto"/>
        </Grid.RowDefinitions>
        <Border Margin="5" Grid.Row="0" BorderThickness="4" BorderBrush="Black" CornerRadius="5" Height="200">
            <Grid>
                <InkPresenter x:Name="inkCanvas">
                    <InkPresenter.Background>
                        <LinearGradientBrush StartPoint="0.5,0" EndPoint="0.5,1">
                            <GradientStop Offset="0" Color="Yellow"/>
                            <GradientStop Offset="1" Color="LightYellow"/>
                        </LinearGradientBrush>
                    </InkPresenter.Background>
                </InkPresenter>
                <Button Grid.Row="0" HorizontalAlignment="Right" VerticalAlignment="Bottom" Margin="10" Content="Recognize" Click="RecoButton_Click"/>
            </Grid>
        </Border>
        <Grid Grid.Row="1">
            <Grid.ColumnDefinitions>
                <ColumnDefinition Width="Auto"/>
                <ColumnDefinition Width="*"/>
            </Grid.ColumnDefinitions>
            <TextBlock Grid.Column="0" FontSize="28" Text="Result: "/>
            <ComboBox x:Name="results" Grid.Column="1" FontSize="28"/>
        </Grid>
    </Grid>
</UserControl>
```

<span data-ttu-id="b1ab4-231">Substitua a página code-behind, Page. XAML. cs, pelo código a seguir, que adicionará um manipulador de eventos para o botão **reconhecer** .</span><span class="sxs-lookup"><span data-stu-id="b1ab4-231">Replace the code behind page, Page.xaml.cs, with the following code that will add an event handler for the **Recognize** button.</span></span>

```CSharp
using System;
using System.Collections.Generic;
using System.Collections.ObjectModel;
using System.Linq;
using System.Net;
using System.Windows;
using System.Windows.Controls;
using System.Windows.Ink;
using System.Windows.Input;
using System.Windows.Media;
using System.Windows.Media.Animation;
using System.Windows.Shapes;
using InkRecognition.InkRecognitionServiceReference;

namespace InkRecognition
{
    public partial class Page : UserControl
    {
        public Page()
        {
            InitializeComponent();
            inkCol = new InkCollector(inkCanvas);
            recoClient = new InkRecognitionServiceClient();
            recoClient.RecognizeCompleted += new EventHandler<RecognizeCompletedEventArgs>(recoClient_RecognizeCompleted);
        }

        private void RecoButton_Click(object sender, RoutedEventArgs e)
        {
            // Serialize the ink into an array on ints.
            ObservableCollection<ObservableCollection<int>> packets = new ObservableCollection<ObservableCollection<int>>();
            double pixelToHimetricMultiplier = 2540d / 96d;

            foreach (Stroke stroke in inkCanvas.Strokes)
            {
                packets.Add(new ObservableCollection<int>());
                int index = inkCanvas.Strokes.IndexOf(stroke);
                for (int i = 0; i < stroke.StylusPoints.Count; i += 2)
                {
                    packets[index].Add(Convert.ToInt32(stroke.StylusPoints[i].X * pixelToHimetricMultiplier));
                    packets[index].Add(Convert.ToInt32(stroke.StylusPoints[i].Y * pixelToHimetricMultiplier));
                }
            }

            // Call the Web service.
            recoClient.RecognizeAsync(packets);
        }

        void recoClient_RecognizeCompleted(object sender, RecognizeCompletedEventArgs e)
        {
            // We have received results from the server, now display them.
            results.ItemsSource = e.Result;
            UpdateLayout();
            results.SelectedIndex = 0;
            inkCanvas.Strokes.Clear();
        }

        private InkRecognitionServiceClient recoClient = null;
        private InkCollector inkCol = null;
    }
}
```

### <a name="remove-secure-transport-directives-from-the-client-configuration"></a><span data-ttu-id="b1ab4-232">Remover diretivas de transporte seguras da configuração do cliente</span><span class="sxs-lookup"><span data-stu-id="b1ab4-232">Remove Secure Transport Directives from the Client Configuration</span></span>

<span data-ttu-id="b1ab4-233">Antes de consumir o serviço WCF, você deve remover todas as opções de transporte seguro da configuração de serviço, pois os transportes seguros atualmente não têm suporte nos serviços WCF do Silverlight 2,0.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-233">Before you can consume the WCF service, you must remove all secure transport options from the service configuration because secure transports are not currently supported in Silverlight 2.0 WCF services.</span></span> <span data-ttu-id="b1ab4-234">No projeto InkRecognition, atualize as configurações de segurança em perreferences. ClientConfig.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-234">From the InkRecognition project, update the security settings in ServiceReferences.ClientConfig.</span></span> <span data-ttu-id="b1ab4-235">Alterar o XML de segurança de</span><span class="sxs-lookup"><span data-stu-id="b1ab4-235">Change the security XML from</span></span>

```XML
          <security mode="None">
            <transport>
              <extendedProtectionPolicy policyEnforcement="WhenSupported" />
            </transport>
          </security>
```

<span data-ttu-id="b1ab4-236">como</span><span class="sxs-lookup"><span data-stu-id="b1ab4-236">to</span></span>

```XML
       <security mode="None"/>
```

<span data-ttu-id="b1ab4-237">Agora, seu aplicativo deve ser executado.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-237">Now, your application should run.</span></span> <span data-ttu-id="b1ab4-238">A imagem a seguir mostra como o aplicativo aparece em awebpagewith algum manuscrito inserido na caixa de reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="b1ab4-238">The following image shows how the application looks within awebpagewith some handwriting entered into the recognition box.</span></span>

<span data-ttu-id="b1ab4-239">![Aplicativo em awebpagewith algum manuscrito inserido na caixa de reconhecimento](images/demo-1.png)</span><span class="sxs-lookup"><span data-stu-id="b1ab4-239">![Application within awebpagewith some handwriting entered into recognition box](images/demo-1.png)</span></span><br/>
<span data-ttu-id="b1ab4-240">*Aplicativo em awebpagewith algum manuscrito inserido na caixa de reconhecimento*</span><span class="sxs-lookup"><span data-stu-id="b1ab4-240">*Application within awebpagewith some handwriting entered into recognition box*</span></span>

<span data-ttu-id="b1ab4-241">A imagem a seguir mostra o texto reconhecido na lista suspensa **resultado** .</span><span class="sxs-lookup"><span data-stu-id="b1ab4-241">The following image shows the recognized text in the **Result** drop-down list.</span></span>

<span data-ttu-id="b1ab4-242">![Aplicativo em awebpagewith texto reconhecido na lista suspensa de resultados](images/demo-2.png)</span><span class="sxs-lookup"><span data-stu-id="b1ab4-242">![Application within awebpagewith recognized text in result drop-down list](images/demo-2.png)</span></span><br/>
<span data-ttu-id="b1ab4-243">*Aplicativo em awebpagewith texto reconhecido na lista suspensa de resultados*</span><span class="sxs-lookup"><span data-stu-id="b1ab4-243">*Application within awebpagewith recognized text in result drop-down list*</span></span>

 

 



