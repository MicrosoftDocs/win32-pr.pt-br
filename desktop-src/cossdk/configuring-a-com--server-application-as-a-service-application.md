---
description: Um aplicativo de servidor COM+ pode ser criado como um serviço para ser iniciado automaticamente durante a inicialização do sistema ou manualmente por ativações.
ms.assetid: 56487746-328d-4435-af58-368aaa15b32a
title: Configurando um aplicativo de servidor do COM+ como um aplicativo de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b3bbf8b691221590d6588c48dbef5198772439
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826256"
---
# <a name="configuring-a-com-server-application-as-a-service-application"></a><span data-ttu-id="4cedf-103">Configurando um aplicativo de servidor do COM+ como um aplicativo de serviço</span><span class="sxs-lookup"><span data-stu-id="4cedf-103">Configuring a COM+ Server Application as a Service Application</span></span>

<span data-ttu-id="4cedf-104">Um aplicativo de servidor COM+ pode ser criado como um serviço para ser iniciado automaticamente durante a inicialização do sistema ou manualmente por ativações.</span><span class="sxs-lookup"><span data-stu-id="4cedf-104">A COM+ server application can be created as a service to start either automatically during the system startup or manually by activations.</span></span> <span data-ttu-id="4cedf-105">Se o serviço não for iniciado, a opção de tratamento de erros especificará a severidade do erro e determinará a ação a ser executada.</span><span class="sxs-lookup"><span data-stu-id="4cedf-105">If the service fails to start, the option for error handling specifies the severity of the error and determines the action to be taken.</span></span> <span data-ttu-id="4cedf-106">A opção de configurar um serviço para ser executado como a conta do sistema local também está disponível, bem como a opção de atribuir uma conta de usuário específica para a qual o aplicativo do servidor COM+ será executado.</span><span class="sxs-lookup"><span data-stu-id="4cedf-106">The option to configure a service to run as the local system account is also available, as well as the option to assign a specific user account for which the COM+ server application will run.</span></span> <span data-ttu-id="4cedf-107">As dependências também podem ser selecionadas em uma lista de serviços registrados no computador usando os serviços de componentes.</span><span class="sxs-lookup"><span data-stu-id="4cedf-107">Dependencies can also be selected from a list of services registered on the computer using Component Services.</span></span> <span data-ttu-id="4cedf-108">Isso determinará quais serviços devem ser executados antes que este serviço seja iniciado.</span><span class="sxs-lookup"><span data-stu-id="4cedf-108">This will determine which services must be executed before this service is started.</span></span>

<span data-ttu-id="4cedf-109">**Para configurar um aplicativo COM+ para ser executado como um serviço**</span><span class="sxs-lookup"><span data-stu-id="4cedf-109">**To configure a COM+ application to run as a service**</span></span>

1.  <span data-ttu-id="4cedf-110">Na árvore de console da ferramenta administrativa serviços de componentes, localize o aplicativo de servidor COM+ que você deseja executar como um serviço.</span><span class="sxs-lookup"><span data-stu-id="4cedf-110">In the console tree of the Component Services administrative tool, locate the COM+ server application you want to run as a service.</span></span>

2.  <span data-ttu-id="4cedf-111">Clique com o botão direito do mouse no aplicativo do servidor COM+ e clique em **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="4cedf-111">Right-click the COM+ server application, and then click **Properties**.</span></span>

3.  <span data-ttu-id="4cedf-112">Na caixa de diálogo **Propriedades** , clique na guia **ativação** .</span><span class="sxs-lookup"><span data-stu-id="4cedf-112">In the **Properties** dialog box, click the **Activation** tab.</span></span>

4.  <span data-ttu-id="4cedf-113">Na caixa **tipo de ativação** , marque a caixa de seleção **Executar aplicativo como serviço NT** .</span><span class="sxs-lookup"><span data-stu-id="4cedf-113">In the **Activation type** box, check the **Run application as NT Service** check box.</span></span>

    > [!Note]  
    > <span data-ttu-id="4cedf-114">A caixa de seleção **Executar aplicativo como serviço do NT** é habilitada somente para aplicativos de servidor e está desabilitada para aplicativos de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="4cedf-114">The **Run application as NT Service** check box is enabled only for server applications and is disabled for library applications.</span></span>

     

5.  <span data-ttu-id="4cedf-115">Clique no botão **Configurar novo serviço** .</span><span class="sxs-lookup"><span data-stu-id="4cedf-115">Click the **Setup New Service** button.</span></span>

6.  <span data-ttu-id="4cedf-116">Na caixa **tipo de inicialização** na caixa de diálogo **nome do serviço** , selecione **automático** ou **manual**.</span><span class="sxs-lookup"><span data-stu-id="4cedf-116">In the **Startup type** box in the **Service Name** dialog box, select **Automatic** or **Manual**.</span></span>

7.  <span data-ttu-id="4cedf-117">Adicional Para especificar a ação a ser tomada para um erro específico, selecione **ignorar**, **normal**, **grave** ou **crítico** na caixa **tratamento de erros** .</span><span class="sxs-lookup"><span data-stu-id="4cedf-117">(Optional) To specify the action to be taken for a particular error, select **Ignore**, **Normal**, **Severe**, or **Critical** in the **Error Handling** box.</span></span> <span data-ttu-id="4cedf-118">O comportamento associado a cada opção é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="4cedf-118">The behavior associated with each option is as follows:</span></span>

    1.  <span data-ttu-id="4cedf-119">**Ignorar**.</span><span class="sxs-lookup"><span data-stu-id="4cedf-119">**Ignore**.</span></span> <span data-ttu-id="4cedf-120">O programa de inicialização registra o erro, mas continua a operação de inicialização.</span><span class="sxs-lookup"><span data-stu-id="4cedf-120">The startup program logs the error but continues the startup operation.</span></span>
    2.  <span data-ttu-id="4cedf-121">**Normal**.</span><span class="sxs-lookup"><span data-stu-id="4cedf-121">**Normal**.</span></span> <span data-ttu-id="4cedf-122">O erro é registrado, uma caixa de mensagem é exibida e o programa de inicialização continua a operação de inicialização.</span><span class="sxs-lookup"><span data-stu-id="4cedf-122">The error is logged, a message box is displayed, and the startup program continues the startup operation.</span></span>
    3.  <span data-ttu-id="4cedf-123">**Grave**.</span><span class="sxs-lookup"><span data-stu-id="4cedf-123">**Severe**.</span></span> <span data-ttu-id="4cedf-124">O erro é registrado e o sistema é reiniciado com a última configuração válida conhecida.</span><span class="sxs-lookup"><span data-stu-id="4cedf-124">The error is logged, and the system is restarted with the last known good configuration.</span></span> <span data-ttu-id="4cedf-125">Se for a última configuração válida que está sendo iniciada quando o erro for registrado, a operação de inicialização continuará.</span><span class="sxs-lookup"><span data-stu-id="4cedf-125">If it is the last known good configuration that is being started when the error is logged, the startup operation continues.</span></span>
    4.  <span data-ttu-id="4cedf-126">**Crítica**.</span><span class="sxs-lookup"><span data-stu-id="4cedf-126">**Critical**.</span></span> <span data-ttu-id="4cedf-127">O erro é registrado e o sistema é reiniciado com a última configuração válida conhecida.</span><span class="sxs-lookup"><span data-stu-id="4cedf-127">The error is logged, and the system is restarted with the last known good configuration.</span></span> <span data-ttu-id="4cedf-128">Se for a última configuração válida que está sendo iniciada quando o erro for registrado, a operação de inicialização falhará.</span><span class="sxs-lookup"><span data-stu-id="4cedf-128">If it is the last known good configuration that is being started when the error is logged, the startup operation fails.</span></span>

8.  <span data-ttu-id="4cedf-129">Adicional Para definir outros serviços como dependentes, selecione os serviços dependentes da lista na caixa **dependências** .</span><span class="sxs-lookup"><span data-stu-id="4cedf-129">(Optional) To set other services as dependent, select the dependent services from the list in the **Dependencies** box.</span></span>

9.  <span data-ttu-id="4cedf-130">Adicional Para indicar que o serviço deve ter permissão para interagir com a área de trabalho, marque a caixa de seleção **permitir que o serviço interaja com a área de trabalho** .</span><span class="sxs-lookup"><span data-stu-id="4cedf-130">(Optional) To indicate that the service should be allowed to interact with the desktop, check the **Allow service to interact with desktop** check box.</span></span>

10. <span data-ttu-id="4cedf-131">Clique em **Criar**.</span><span class="sxs-lookup"><span data-stu-id="4cedf-131">Click **Create**.</span></span>

11. <span data-ttu-id="4cedf-132">Adicional Para atribuir o serviço a uma conta de usuário:</span><span class="sxs-lookup"><span data-stu-id="4cedf-132">(Optional) To assign the service to a user account:</span></span>

    1.  <span data-ttu-id="4cedf-133">Na guia **identidade** , selecione **este usuário**.</span><span class="sxs-lookup"><span data-stu-id="4cedf-133">In the **Identity** tab, select **This user**.</span></span>
    2.  <span data-ttu-id="4cedf-134">Para selecionar o usuário, insira o nome de usuário na caixa **usuário** ou clique no botão **procurar** .</span><span class="sxs-lookup"><span data-stu-id="4cedf-134">To select the user, enter the user name in the **User** box or click the **Browse** button.</span></span>
    3.  <span data-ttu-id="4cedf-135">Digite a senha da conta de usuário na caixa **senha** .</span><span class="sxs-lookup"><span data-stu-id="4cedf-135">Enter the password for the user account in the **Password** box.</span></span>
    4.  <span data-ttu-id="4cedf-136">Digite a mesma senha na caixa **Confirmar senha** .</span><span class="sxs-lookup"><span data-stu-id="4cedf-136">Enter the same password in the **Confirm Password** box.</span></span>

 

 



