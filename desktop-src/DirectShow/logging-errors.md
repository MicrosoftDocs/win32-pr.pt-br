---
description: Erros de log
ms.assetid: 690ea91b-5bc0-45f0-8354-ec625709f7bd
title: Erros de log
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76cded9d4cfaedd93e846fec52b07bf5d4eef9a5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645767"
---
# <a name="logging-errors"></a><span data-ttu-id="aa979-103">Erros de log</span><span class="sxs-lookup"><span data-stu-id="aa979-103">Logging Errors</span></span>

<span data-ttu-id="aa979-104">\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]</span><span class="sxs-lookup"><span data-stu-id="aa979-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="aa979-105">Os [serviços de edição do DirectShow](directshow-editing-services.md) (des) fornecem um mecanismo interno para registrar erros que ocorrem durante o carregamento, a construção ou a renderização de um projeto des.</span><span class="sxs-lookup"><span data-stu-id="aa979-105">[DirectShow Editing Services](directshow-editing-services.md) (DES) provides a built-in mechanism for logging errors that occur when loading, constructing, or rendering a DES project.</span></span> <span data-ttu-id="aa979-106">Este artigo apresenta um exemplo de aplicativo de console que carrega um arquivo de projeto XML e tenta renderizá-lo.</span><span class="sxs-lookup"><span data-stu-id="aa979-106">This article presents a sample console application that loads an XML project file and attempts to render it.</span></span> <span data-ttu-id="aa979-107">Se ocorrer um erro, o aplicativo imprime uma mensagem de erro na janela do console.</span><span class="sxs-lookup"><span data-stu-id="aa979-107">If an error occurs, the application prints an error message in the console window.</span></span> <span data-ttu-id="aa979-108">O código de exemplo apresentado neste artigo baseia-se no exemplo fornecido em [carregando e visualizando um projeto](loading-and-previewing-a-project.md).</span><span class="sxs-lookup"><span data-stu-id="aa979-108">The sample code presented in this article builds on the example given in [Loading and Previewing a Project](loading-and-previewing-a-project.md).</span></span>

> [!Note]  
> <span data-ttu-id="aa979-109">Seu aplicativo não é necessário para implementar o log de erros.</span><span class="sxs-lookup"><span data-stu-id="aa979-109">Your application is not required to implement error logging.</span></span> <span data-ttu-id="aa979-110">O DES não registra erros a menos que você solicite-o explicitamente.</span><span class="sxs-lookup"><span data-stu-id="aa979-110">DES does not log errors unless you explicitly request it.</span></span>

 

<span data-ttu-id="aa979-111">Este artigo pressupõe que você entende a programação de cliente COM e o modelo de linha do tempo DES.</span><span class="sxs-lookup"><span data-stu-id="aa979-111">This article assumes that you understand COM client programming and the DES timeline model.</span></span> <span data-ttu-id="aa979-112">Além disso, você precisa entender os conceitos básicos da programação de objetos COM.</span><span class="sxs-lookup"><span data-stu-id="aa979-112">In addition, you need to understand the basics of COM object programming.</span></span> <span data-ttu-id="aa979-113">Para obter informações sobre cronogramas em DES, consulte [o modelo de linha do tempo](the-timeline-model.md).</span><span class="sxs-lookup"><span data-stu-id="aa979-113">For information about timelines in DES, see [The Timeline Model](the-timeline-model.md).</span></span>

<span data-ttu-id="aa979-114">Este artigo inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="aa979-114">This article contains the following sections.</span></span>

-   [<span data-ttu-id="aa979-115">Visão geral do log de erros</span><span class="sxs-lookup"><span data-stu-id="aa979-115">Overview of Error Logging</span></span>](overview-of-error-logging.md)
-   [<span data-ttu-id="aa979-116">Criando uma classe de log de erros</span><span class="sxs-lookup"><span data-stu-id="aa979-116">Creating an Error Logging Class</span></span>](creating-an-error-logging-class.md)
-   [<span data-ttu-id="aa979-117">Implementando IAMErrorLog</span><span class="sxs-lookup"><span data-stu-id="aa979-117">Implementing IAMErrorLog</span></span>](implementing-iamerrorlog.md)
-   [<span data-ttu-id="aa979-118">Configurando o log de erros</span><span class="sxs-lookup"><span data-stu-id="aa979-118">Setting the Error Log</span></span>](setting-the-error-log.md)
-   [<span data-ttu-id="aa979-119">Log de erros DES: código de exemplo</span><span class="sxs-lookup"><span data-stu-id="aa979-119">DES Error Logging: Example Code</span></span>](des-error-logging--example-code.md)

## <a name="related-topics"></a><span data-ttu-id="aa979-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="aa979-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa979-121">Usando os serviços de edição do DirectShow</span><span class="sxs-lookup"><span data-stu-id="aa979-121">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 



