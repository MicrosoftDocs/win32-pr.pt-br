---
description: O Tablet PC inclui tecnologia para reconhecer a entrada à tinta que é mais comum na forma de manuscrito.
ms.assetid: 614971a8-2b56-40d4-abb6-aba5ded01883
title: Sobre o reconhecimento de manuscrito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ff794f018cd0019a5013bacf8b9edfbe45018d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812006"
---
# <a name="about-handwriting-recognition"></a><span data-ttu-id="2f473-103">Sobre o reconhecimento de manuscrito</span><span class="sxs-lookup"><span data-stu-id="2f473-103">About Handwriting Recognition</span></span>

<span data-ttu-id="2f473-104">O Tablet PC inclui tecnologia para reconhecer a entrada à tinta que é mais comum na forma de manuscrito.</span><span class="sxs-lookup"><span data-stu-id="2f473-104">Tablet PC includes technology for recognizing ink input that is most commonly in the form of handwriting.</span></span> <span data-ttu-id="2f473-105">O módulo de software que fornece o reconhecimento é chamado de reconhecedor.</span><span class="sxs-lookup"><span data-stu-id="2f473-105">The software module that provides the recognition is called a recognizer.</span></span> <span data-ttu-id="2f473-106">Um reconhecedor reconhece uma linguagem, um grupo de idiomas relacionados ou uma classe de objetos relacionados, como notas musicais, gestos do sistema ou formas geométricas.</span><span class="sxs-lookup"><span data-stu-id="2f473-106">A recognizer recognizes one language, a group of related languages, or a class of related objects such as musical notes, system gestures, or geometric shapes.</span></span> <span data-ttu-id="2f473-107">Você pode adicionar reconhecedores dinamicamente ao sistema de serviços de tinta.</span><span class="sxs-lookup"><span data-stu-id="2f473-107">You can dynamically add recognizers to the ink services system.</span></span>

## <a name="recognition-steps"></a><span data-ttu-id="2f473-108">Etapas de reconhecimento</span><span class="sxs-lookup"><span data-stu-id="2f473-108">Recognition Steps</span></span>

<span data-ttu-id="2f473-109">O reconhecimento é tratado pelo uso de um contexto de reconhecedor.</span><span class="sxs-lookup"><span data-stu-id="2f473-109">Recognition is handled through the use of a recognizer context.</span></span> <span data-ttu-id="2f473-110">O reconhecimento consiste em quatro etapas básicas:</span><span class="sxs-lookup"><span data-stu-id="2f473-110">Recognition consists of four basic steps:</span></span>

1.  <span data-ttu-id="2f473-111">Configurando as restrições de reconhecimento por:</span><span class="sxs-lookup"><span data-stu-id="2f473-111">Setting up the recognition constraints by:</span></span>
    -   <span data-ttu-id="2f473-112">Selecionar o reconhecedor e o modo de entrada (restrições geométricas).</span><span class="sxs-lookup"><span data-stu-id="2f473-112">Selecting the recognizer and input mode (geometric constraints).</span></span>
    -   <span data-ttu-id="2f473-113">Definindo as restrições de idioma.</span><span class="sxs-lookup"><span data-stu-id="2f473-113">Setting the language constraints.</span></span> <span data-ttu-id="2f473-114">Por exemplo, você pode restringir a entrada para caracteres alfanuméricos ou pode passar esquemas para auxiliar o reconhecedor.</span><span class="sxs-lookup"><span data-stu-id="2f473-114">For example, you can restrict input to alphanumeric characters or you can pass schemas to assist the recognizer.</span></span>
2.  <span data-ttu-id="2f473-115">Enviando tinta para o reconhecedor.</span><span class="sxs-lookup"><span data-stu-id="2f473-115">Sending ink to the recognizer.</span></span>
3.  <span data-ttu-id="2f473-116">Processando a entrada (reconhecendo).</span><span class="sxs-lookup"><span data-stu-id="2f473-116">Processing the input (recognizing).</span></span>
4.  <span data-ttu-id="2f473-117">Retornando os resultados do reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="2f473-117">Returning the results of the recognition.</span></span>

<span data-ttu-id="2f473-118">As etapas 2 e 3 podem ser repetidas em um loop ou todos os traços de tinta podem ser adicionados à tinta antes da tentativa de reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="2f473-118">Steps 2 and 3 may be repeated in a loop, or all of the ink strokes may be added to the ink before recognition is attempted.</span></span>

## <a name="samples-and-related-topics"></a><span data-ttu-id="2f473-119">Exemplos e tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2f473-119">Samples and Related Topics</span></span>

<span data-ttu-id="2f473-120">[Exemplo de reconhecimento avançado](advanced-recognition-sample.md) demonstra como usar os reconhecedores com objetos de [**tinta**](inkdisp-class.md) para executar o reconhecimento de tinta.</span><span class="sxs-lookup"><span data-stu-id="2f473-120">[Advanced Recognition Sample](advanced-recognition-sample.md) demonstrates how to use recognizers with [**Ink**](inkdisp-class.md) objects to perform ink recognition.</span></span>

<span data-ttu-id="2f473-121">O [modelo de exemplo de DLL do Recognizer](recognizer-dll-sample-template.md) contém um modelo para criar uma DLL de reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="2f473-121">[Recognizer DLL Sample Template](recognizer-dll-sample-template.md) contains a template for creating a recognizer DLL.</span></span> <span data-ttu-id="2f473-122">O modelo contém funções para registrar e cancelar o registro do servidor, bem como esqueletos para funções de reconhecedor primário.</span><span class="sxs-lookup"><span data-stu-id="2f473-122">The template contains functions for registering and unregistering the server, as well as skeletons for primary recognizer functions.</span></span>

<span data-ttu-id="2f473-123">As seções a seguir descrevem os conceitos básicos por trás da tecnologia de reconhecimento do Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="2f473-123">The following sections describe the basic concepts behind the Tablet PC recognition technology.</span></span> <span data-ttu-id="2f473-124">Para obter informações detalhadas sobre como criar Reconhecedores personalizados, consulte [criando um reconhecedor](creating-a-recognizer.md).</span><span class="sxs-lookup"><span data-stu-id="2f473-124">For detailed information about creating custom recognizers, see [Creating a Recognizer](creating-a-recognizer.md).</span></span>

-   [<span data-ttu-id="2f473-125">Reconhecedores de texto</span><span class="sxs-lookup"><span data-stu-id="2f473-125">Text Recognizers</span></span>](text-recognizers.md)
-   [<span data-ttu-id="2f473-126">Reconhecedores de objetos</span><span class="sxs-lookup"><span data-stu-id="2f473-126">Object Recognizers</span></span>](object-recognizers.md)
-   [<span data-ttu-id="2f473-127">Usando a coleção Recognizers</span><span class="sxs-lookup"><span data-stu-id="2f473-127">Using the Recognizers Collection</span></span>](using-the-recognizers-collection.md)
-   [<span data-ttu-id="2f473-128">Contexto do reconhecedor</span><span class="sxs-lookup"><span data-stu-id="2f473-128">Recognizer Context</span></span>](recognizer-context.md)
-   [<span data-ttu-id="2f473-129">Segmentos de reconhecimento</span><span class="sxs-lookup"><span data-stu-id="2f473-129">Recognition Segments</span></span>](recognition-segments.md)
-   [<span data-ttu-id="2f473-130">Reconhecimento de texto angular</span><span class="sxs-lookup"><span data-stu-id="2f473-130">Recognition of Angled Text</span></span>](recognition-of-angled-text.md)
-   [<span data-ttu-id="2f473-131">Suporte à reordenação de Stroke do Recognizer</span><span class="sxs-lookup"><span data-stu-id="2f473-131">Recognizer Stroke Reordering Support</span></span>](recognizer-stroke-reordering-support.md)
-   [<span data-ttu-id="2f473-132">Dicionários e factos</span><span class="sxs-lookup"><span data-stu-id="2f473-132">Dictionaries and Factoids</span></span>](dictionaries-and-factoids.md)
-   <span data-ttu-id="2f473-133">[Propriedade de confiança \[ sobre reconhecimento\]](confidence-property--about-recognition.md)</span><span class="sxs-lookup"><span data-stu-id="2f473-133">[Confidence Property \[About Recognition\]](confidence-property--about-recognition.md)</span></span>
-   [<span data-ttu-id="2f473-134">Alternativos</span><span class="sxs-lookup"><span data-stu-id="2f473-134">Alternates</span></span>](alternates.md)
-   [<span data-ttu-id="2f473-135">Segmentos de tinta e alternativas</span><span class="sxs-lookup"><span data-stu-id="2f473-135">Ink Segments and Alternates</span></span>](ink-segments-and-alternates.md)

 

 



