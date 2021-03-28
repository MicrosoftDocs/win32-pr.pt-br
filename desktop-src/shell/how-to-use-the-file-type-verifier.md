---
description: Este tópico descreve como usar o verificador de tipo de arquivo que é fornecido no SDK do Windows 7.
ms.assetid: 96FCA74B-DEB2-49D1-B670-EBD8BE0783F1
title: Como usar o verificador de tipo de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f083897499f972f945867a0c02318df192e734d9
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/28/2021
ms.locfileid: "104172379"
---
# <a name="how-to-use-the-file-type-verifier"></a><span data-ttu-id="fee04-103">Como usar o verificador de tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="fee04-103">How to Use the File Type Verifier</span></span>

<span data-ttu-id="fee04-104">Este tópico descreve como usar o verificador de tipo de arquivo que é fornecido no [SDK do Windows 7](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="fee04-104">This topic describes how to use the File Type Verifier that is provided in the [Windows 7 SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="fee04-105">Se o programa criar os tipos de arquivo com os quais os usuários devem interagir do shell do Windows (normalmente armazenados na pasta conhecida de um usuário, como **meus documentos**), é muito importante testar seu aplicativo e verificar se os arquivos que ele cria estão corretamente registrados e fornecer uma experiência de usuário de alta qualidade ao procurar e Pesquisar arquivos.</span><span class="sxs-lookup"><span data-stu-id="fee04-105">If your program creates file types that users are expected to interact with from the Windows Shell (typically stored in a user's known folder such as **My Documents**), it is very important to test your application and verify that the files it creates are properly registered and provide a high-quality user experience when browsing and searching files.</span></span> <span data-ttu-id="fee04-106">Isso é especialmente importante se você espera que os usuários executem seus aplicativos no Windows 7, que se baseiam em manipuladores de tipo de arquivo de alta qualidade para muitos dos recursos do Shell.</span><span class="sxs-lookup"><span data-stu-id="fee04-106">This is especially important if you expect users to run your applications on Windows 7, which relies on high-quality file type handlers for many of the Shell features.</span></span>

<span data-ttu-id="fee04-107">Para verificar o tipo de arquivo usando o verificador de tipo de arquivo, siga estas etapas.</span><span class="sxs-lookup"><span data-stu-id="fee04-107">To verify your file type using the File Type Verifier, follow these steps.</span></span>

## <a name="instructions"></a><span data-ttu-id="fee04-108">Instruções</span><span class="sxs-lookup"><span data-stu-id="fee04-108">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="fee04-109">Etapa 1:</span><span class="sxs-lookup"><span data-stu-id="fee04-109">Step 1:</span></span>

<span data-ttu-id="fee04-110">Instale o aplicativo em seu ambiente de teste e copie o verificador de tipo de arquivo para esse ambiente.</span><span class="sxs-lookup"><span data-stu-id="fee04-110">Install the application on your test environment, and copy the File Type Verifier to that environment.</span></span> <span data-ttu-id="fee04-111">O verificador de tipo de arquivo está disponível no [SDK do Windows 7](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="fee04-111">The File Type Verifier is available in the [Windows 7 SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

### <a name="step-2"></a><span data-ttu-id="fee04-112">Etapa 2:</span><span class="sxs-lookup"><span data-stu-id="fee04-112">Step 2:</span></span>

<span data-ttu-id="fee04-113">Use seu aplicativo para criar um arquivo a ser testado.</span><span class="sxs-lookup"><span data-stu-id="fee04-113">Use your application to create a file to be tested.</span></span>

### <a name="step-3"></a><span data-ttu-id="fee04-114">Etapa 3:</span><span class="sxs-lookup"><span data-stu-id="fee04-114">Step 3:</span></span>

<span data-ttu-id="fee04-115">Inicie o verificador de tipo de arquivo.</span><span class="sxs-lookup"><span data-stu-id="fee04-115">Start the File Type Verifier.</span></span>

### <a name="step-4"></a><span data-ttu-id="fee04-116">Etapa 4:</span><span class="sxs-lookup"><span data-stu-id="fee04-116">Step 4:</span></span>

<span data-ttu-id="fee04-117">Selecione a categoria para o tipo de arquivo, conforme mostrado na captura de tela a seguir.</span><span class="sxs-lookup"><span data-stu-id="fee04-117">Select the category for your file type, as shown in the following screen shot.</span></span>

![Captura de tela que mostra a função de arrastar e soltar.](images/file-assoc/filetypeverifier1.png)

<span data-ttu-id="fee04-119">A seleção de categoria determina o conjunto de testes que serão executados pela ferramenta.</span><span class="sxs-lookup"><span data-stu-id="fee04-119">The category selection determines the set of tests that will be run by the tool.</span></span> <span data-ttu-id="fee04-120">Se o seu tipo puder se enquadrar em mais de uma categoria (por exemplo, um arquivo TIF pode ser uma imagem ou um documento, dependendo do conteúdo), execute a ferramenta novamente com cada categoria apropriada.</span><span class="sxs-lookup"><span data-stu-id="fee04-120">If your type could fall under more than one category (for example, a TIF file might be a Picture or a Document depending on the content), run the tool again with each appropriate category.</span></span>

### <a name="step-5"></a><span data-ttu-id="fee04-121">Etapa 5:</span><span class="sxs-lookup"><span data-stu-id="fee04-121">Step 5:</span></span>

<span data-ttu-id="fee04-122">Usando o Windows Explorer, localize um arquivo a ser testado e use o mouse para arrastá-lo para o destino no verificador de tipo de arquivo, conforme mostrado na captura de tela a seguir.</span><span class="sxs-lookup"><span data-stu-id="fee04-122">Using Windows Explorer, locate a file to be tested and use the mouse to drag it to the target in File Type Verifier, as shown in the following screen shot.</span></span>

![captura de tela mostrando a função de arrastar e soltar](images/file-assoc/filetypeverifier2.png)

### <a name="step-6"></a><span data-ttu-id="fee04-124">Etapa 6:</span><span class="sxs-lookup"><span data-stu-id="fee04-124">Step 6:</span></span>

<span data-ttu-id="fee04-125">Aguarde até que a ferramenta de verificação de tipo de arquivo continue em uma série de testes.</span><span class="sxs-lookup"><span data-stu-id="fee04-125">Wait for the File Type Verifier tool to proceed through a series of tests.</span></span> <span data-ttu-id="fee04-126">O progresso do teste é mostrado pela barra de progresso, como na captura de tela a seguir.</span><span class="sxs-lookup"><span data-stu-id="fee04-126">The progress of the testing is shown by the progress bar, as in the following screen shot.</span></span>

![captura de tela mostrando a barra de progresso](images/file-assoc/filetypeverifier3.png)

### <a name="step-7"></a><span data-ttu-id="fee04-128">Etapa 7:</span><span class="sxs-lookup"><span data-stu-id="fee04-128">Step 7:</span></span>

<span data-ttu-id="fee04-129">Examine o resumo dos resultados dos testes de tipo de arquivo de documento, conforme mostrado na captura de tela a seguir.</span><span class="sxs-lookup"><span data-stu-id="fee04-129">Review the results summary of your Document file type tests, as shown in the following screen shot.</span></span>

![captura de tela mostrando Resumo dos resultados](images/file-assoc/filetypeverifier4.png)

### <a name="step-8"></a><span data-ttu-id="fee04-131">Etapa 8:</span><span class="sxs-lookup"><span data-stu-id="fee04-131">Step 8:</span></span>

<span data-ttu-id="fee04-132">Clique em qualquer um dos resultados na página Resumo para exibir o log detalhado.</span><span class="sxs-lookup"><span data-stu-id="fee04-132">Click any of the results on the summary page to view the detailed log.</span></span> <span data-ttu-id="fee04-133">Um log de exemplo para um Gerenciador de visualização é mostrado na captura de tela a seguir.</span><span class="sxs-lookup"><span data-stu-id="fee04-133">An example log for a preview handler is shown in the following screen shot.</span></span>

![captura de tela mostrando log do Gerenciador de visualização](images/file-assoc/filetypeverifier5.png)

### <a name="step-9"></a><span data-ttu-id="fee04-135">Etapa 9:</span><span class="sxs-lookup"><span data-stu-id="fee04-135">Step 9:</span></span>

<span data-ttu-id="fee04-136">Para salvar uma cópia do arquivo de log, clique em **salvar arquivo de log** na parte inferior da exibição do log e escolha um local apropriado para armazená-lo em seu computador.</span><span class="sxs-lookup"><span data-stu-id="fee04-136">To save a copy of the log file, click **Save Log File** at the bottom of the log display and choose an appropriate location for storing it on your computer.</span></span>

### <a name="step-10"></a><span data-ttu-id="fee04-137">Etapa 10:</span><span class="sxs-lookup"><span data-stu-id="fee04-137">Step 10:</span></span>

<span data-ttu-id="fee04-138">Se as falhas forem relatadas, faça as alterações apropriadas em seu aplicativo e execute a ferramenta novamente para verificar se as falhas não estão mais aparecendo nos testes.</span><span class="sxs-lookup"><span data-stu-id="fee04-138">If failures are reported, make the appropriate changes in your application and run the tool again to verify that the failures are no longer showing up in the tests.</span></span> <span data-ttu-id="fee04-139">Se os avisos forem relatados, avalie-os e decida se eles são relevantes para o tipo de arquivo específico e faça as alterações apropriadas em seu aplicativo, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="fee04-139">If warnings are reported, evaluate them and decide whether they are relevant for your particular file type and make the appropriate changes to your application as necessary.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fee04-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fee04-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fee04-141">SDK do Windows 7</span><span class="sxs-lookup"><span data-stu-id="fee04-141">Windows 7 SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx)
</dt> </dl>

 

 



