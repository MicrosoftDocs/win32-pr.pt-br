---
description: O uso do ambiente de desenvolvimento integrado (IDE) da Microsoft Visual Basic para depuração oferece Visual Basic aos desenvolvedores acesso a ferramentas familiares e à facilidade de uso.
ms.assetid: d31efc97-c286-434d-93f5-77b34ec16205
title: Depuração no IDE Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74574fdb289e1ad334337f17943c6961b95bf288
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370392"
---
# <a name="debugging-in-the-visual-basic-ide"></a><span data-ttu-id="ac417-103">Depuração no IDE Visual Basic</span><span class="sxs-lookup"><span data-stu-id="ac417-103">Debugging in the Visual Basic IDE</span></span>

<span data-ttu-id="ac417-104">O uso do ambiente de desenvolvimento integrado (IDE) da Microsoft Visual Basic para depuração oferece Visual Basic aos desenvolvedores acesso a ferramentas familiares e à facilidade de uso.</span><span class="sxs-lookup"><span data-stu-id="ac417-104">Using the Microsoft Visual Basic integrated development environment (IDE) for debugging gives Visual Basic developers access to familiar tools and ease-of-use.</span></span> <span data-ttu-id="ac417-105">Embora muitos componentes eventualmente precisem ser mais totalmente depurados usando o ambiente de Microsoft Visual C++, uma estratégia pode ser primeiro depurar o máximo de funcionalidade possível com Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="ac417-105">While many components will eventually need to be more fully debugged using the Microsoft Visual C++ environment, one strategy might be to first debug as much functionality as possible with Visual Basic.</span></span> <span data-ttu-id="ac417-106">Por exemplo, talvez você queira usar o Visual Basic IDE para depuração no COM+ quando ainda não estiver Depurando vários threads, rastreamento de componentes, chamadas remotas ou isolamento de processo.</span><span class="sxs-lookup"><span data-stu-id="ac417-106">For example, you might want to use the Visual Basic IDE for debugging within COM+ when you aren't yet debugging multithreading, component tracking, remote calls, or process isolation.</span></span>

<span data-ttu-id="ac417-107">Em geral, ao usar o ambiente de Visual Basic para depuração, você primeiro compila o projeto e adiciona a DLL a um aplicativo COM+.</span><span class="sxs-lookup"><span data-stu-id="ac417-107">In general, when using the Visual Basic environment for debugging, you first compile the project and add the DLL to a COM+ application.</span></span> <span data-ttu-id="ac417-108">Em seguida, defina a compatibilidade binária para o projeto, referenciando a DLL que você criou e inicie o projeto para iniciar a depuração.</span><span class="sxs-lookup"><span data-stu-id="ac417-108">Then you set binary compatibility for the project, referencing the DLL you made, and start the project to begin debugging.</span></span>

## <a name="general-guidelines-for-debugging-in-the-visual-basic-environment"></a><span data-ttu-id="ac417-109">Diretrizes gerais para depuração no ambiente de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="ac417-109">General Guidelines for Debugging in the Visual Basic Environment</span></span>

-   <span data-ttu-id="ac417-110">Enquanto você estiver Depurando usando Visual Basic, o COM+ tratará os componentes de Visual Basic como se eles pertencessem a um aplicativo de biblioteca, mesmo se os componentes estiverem registrados como pertencentes a um aplicativo de servidor.</span><span class="sxs-lookup"><span data-stu-id="ac417-110">While you are debugging using Visual Basic, COM+ treats the Visual Basic components as if they belong to a library application, even if the components are registered as belonging to a server application.</span></span> <span data-ttu-id="ac417-111">Como ele é executado como um aplicativo de biblioteca, os ícones de componente na ferramenta administrativa serviços de componentes não giram conforme os componentes são depurados.</span><span class="sxs-lookup"><span data-stu-id="ac417-111">Because it runs as a library application, the component icons in the Component Services administrative tool do not spin as the components are debugged.</span></span>
-   <span data-ttu-id="ac417-112">Se você alterar os atributos de transação em um componente durante a depuração ou fizer uma alteração de código-fonte que exija Visual Basic para gerar um novo CLSID ou ProgID, certifique-se de excluir e reinstalar o aplicativo COM+ que contém o componente.</span><span class="sxs-lookup"><span data-stu-id="ac417-112">If you change transaction attributes on a component during debugging or make a source code change that requires Visual Basic to generate a new CLSID or ProgID, be sure to delete and reinstall the COM+ application containing the component.</span></span> <span data-ttu-id="ac417-113">Se você tiver definido a compatibilidade binária para o componente, você será avisado de que as alterações ocorreram.</span><span class="sxs-lookup"><span data-stu-id="ac417-113">If you have set binary compatibility for the component, you will be warned that changes have occurred.</span></span>

## <a name="notes-on-debugging-within-a-com-application"></a><span data-ttu-id="ac417-114">Observações sobre depuração em um aplicativo COM+</span><span class="sxs-lookup"><span data-stu-id="ac417-114">Notes on Debugging Within a COM+ Application</span></span>

-   <span data-ttu-id="ac417-115">Se você fizer alterações no Visual Basic IDE nas interfaces do componente, nomes de classe, nomes de projeto, suporte transacional ou outras configurações, poderá haver incompatibilidade entre os dados de configuração no Gerenciador de serviços de componentes e a configuração real em execução no depurador de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="ac417-115">If you make changes in the Visual Basic IDE in your component's interfaces, class names, project names, transactional support or other settings, there may be mismatches between the configuration data in the Component Services explorer and the actual configuration running in the Visual Basic debugger.</span></span>
-   <span data-ttu-id="ac417-116">Não exporte um aplicativo COM+ enquanto estiver depurando um componente no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ac417-116">Do not export a COM+ application while you are debugging a component in the application.</span></span> <span data-ttu-id="ac417-117">O COM+ tratará o ambiente de desenvolvimento de Visual Basic como o componente.</span><span class="sxs-lookup"><span data-stu-id="ac417-117">COM+ will treat the Visual Basic development environment as the component.</span></span>
-   <span data-ttu-id="ac417-118">Se você estiver executando um componente fora do depurador e decidir iniciar a depuração, uma instância do componente ainda poderá estar em execução no COM+ quando você iniciá-lo no depurador.</span><span class="sxs-lookup"><span data-stu-id="ac417-118">If you are running a component outside the debugger and then decide to begin debugging, an instance of the component may still be running in COM+ when you start it in the debugger.</span></span> <span data-ttu-id="ac417-119">O COM+ detectará essa condição e tentará desligar silenciosamente a instância que ela controla.</span><span class="sxs-lookup"><span data-stu-id="ac417-119">COM+ will detect this condition and attempt to silently shut down the instance it controls.</span></span> <span data-ttu-id="ac417-120">Para evitar esse problema, remova o componente da ferramenta administrativa serviços de componentes antes de começar a depuração.</span><span class="sxs-lookup"><span data-stu-id="ac417-120">To avoid this problem, remove the component from the Component Services administrative tool before you begin debugging.</span></span>

<span data-ttu-id="ac417-121">**Para depurar usando o ambiente de Visual Basic**</span><span class="sxs-lookup"><span data-stu-id="ac417-121">**To debug using the Visual Basic environment**</span></span>

1.  <span data-ttu-id="ac417-122">Abra o projeto de componente no Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="ac417-122">Open the component project in Visual Basic.</span></span>

2.  <span data-ttu-id="ac417-123">Compile seu componente e, em seguida, defina a compatibilidade binária em seu projeto para o componente compilado.</span><span class="sxs-lookup"><span data-stu-id="ac417-123">Compile your component, and then set binary compatibility in your project to the compiled component.</span></span>

3.  <span data-ttu-id="ac417-124">Defina a propriedade MTSTransactionMode com um valor diferente de 0-NotAnMTSObject.</span><span class="sxs-lookup"><span data-stu-id="ac417-124">Set the MTSTransactionMode property to a value other than 0 - NotAnMTSObject.</span></span> <span data-ttu-id="ac417-125">Quando você inicia o projeto, essa configuração solicita Visual Basic para ativar o componente no COM+.</span><span class="sxs-lookup"><span data-stu-id="ac417-125">When you start the project, this setting prompts Visual Basic to activate your component within COM+.</span></span>

4.  <span data-ttu-id="ac417-126">No menu **projeto** , clique em **Propriedades** e, em seguida, insira o programa iniciar na guia **depuração** . O programa iniciar é o executável do cliente que chama esse componente.</span><span class="sxs-lookup"><span data-stu-id="ac417-126">From the **Project** menu, click **Properties**, and then enter the start program on the **Debugging** tab. The start program is the client executable that calls this component.</span></span>

    > [!Note]  
    > <span data-ttu-id="ac417-127">O programa de início deve ser local para o componente que você está depurando.</span><span class="sxs-lookup"><span data-stu-id="ac417-127">The start program must be local to the component you are debugging.</span></span>

     

5.  <span data-ttu-id="ac417-128">Pressione a tecla F5 para iniciar a depuração do componente.</span><span class="sxs-lookup"><span data-stu-id="ac417-128">Press the F5 key to begin debugging the component.</span></span>

<span data-ttu-id="ac417-129">Depois de pressionar F5, Visual Basic iniciará o aplicativo cliente e executará o componente no modo de depuração.</span><span class="sxs-lookup"><span data-stu-id="ac417-129">After you press F5, Visual Basic launches the client application and runs the component in debug mode.</span></span> <span data-ttu-id="ac417-130">Você pode inserir pontos de interrupção no código do componente e definir inspeções em variáveis.</span><span class="sxs-lookup"><span data-stu-id="ac417-130">You can place breakpoints in the component's code and set watches on variables.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ac417-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ac417-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac417-132">Suporte à depuração de Visual Basic COM+ em contraste com o MTS</span><span class="sxs-lookup"><span data-stu-id="ac417-132">COM+ Visual Basic Debugging Support Contrasted with MTS</span></span>](com--visual-basic-debugging-support-contrasted-with-mts.md)
</dt> <dt>

[<span data-ttu-id="ac417-133">Depurando componentes de Visual Basic compilados</span><span class="sxs-lookup"><span data-stu-id="ac417-133">Debugging Compiled Visual Basic Components</span></span>](debugging-compiled-visual-basic-components.md)
</dt> </dl>

 

 



