---
title: Exemplos de código do Win32 para desktop
description: Sobre os exemplos repositórios para Win32 e como Pesquisar neles.
ms.topic: article
ms.date: 03/19/2021
ms.openlocfilehash: 5a4083697d444f36b31c553a2d6159d4370565d4
ms.sourcegitcommit: 46e75903326c49a6c5cc576ee2b4f67f64a6d5ff
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/20/2021
ms.locfileid: "105769674"
---
# <a name="desktop-win32-code-samples"></a><span data-ttu-id="a00c4-103">Exemplos de código do Win32 para desktop</span><span class="sxs-lookup"><span data-stu-id="a00c4-103">Desktop Win32 code samples</span></span>

<span data-ttu-id="a00c4-104">Consulte também [exemplos de código](https://developer.microsoft.com/windows/samples/).</span><span class="sxs-lookup"><span data-stu-id="a00c4-104">Also see [Code samples](https://developer.microsoft.com/windows/samples/).</span></span>

## <a name="find-a-sample-for-the-api-youre-interested-in"></a><span data-ttu-id="a00c4-105">Encontre um exemplo para a API na qual você está interessado</span><span class="sxs-lookup"><span data-stu-id="a00c4-105">Find a sample for the API you're interested in</span></span>

<span data-ttu-id="a00c4-106">Você pode usar Microsoft Visual Studio para pesquisar o código-fonte de um repositório inteiro para ver se o uso de uma determinada API do Windows está sendo demonstrado.</span><span class="sxs-lookup"><span data-stu-id="a00c4-106">You can use Microsoft Visual Studio to search an entire repo's source code to see whether the usage of a particular Windows API is being demonstrated.</span></span>

* <span data-ttu-id="a00c4-107">Clone qualquer um dos repositórios listados nas seções abaixo (ou baixe o ZIP) em seu sistema de arquivos local.</span><span class="sxs-lookup"><span data-stu-id="a00c4-107">Clone any of the repos listed in the sections below (or download the ZIP) to your local file system.</span></span>
* <span data-ttu-id="a00c4-108">Em seguida, **Localize em arquivos** no Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="a00c4-108">Then **Find in Files** in Visual Studio.</span></span> <span data-ttu-id="a00c4-109">Defina **examinar na** pasta clonada ou baixada para e procure o nome da API na qual você está interessado.</span><span class="sxs-lookup"><span data-stu-id="a00c4-109">Set **Look in** to the folder you cloned or downloaded into, and search for the name of the API you're interested in.</span></span> <span data-ttu-id="a00c4-110">A verificação do **caso de correspondência** fornece os melhores resultados.</span><span class="sxs-lookup"><span data-stu-id="a00c4-110">Checking **Match case** gives best results.</span></span>
* <span data-ttu-id="a00c4-111">Tenha cuidado ao verificar **correspondência de palavra inteira** se a API puder ser chamada em várias formas &mdash; , por exemplo, **CreateMutex**, **createmutexa** e **CreateMutexW**.</span><span class="sxs-lookup"><span data-stu-id="a00c4-111">Be careful of checking **Match whole word** if the API can be called in various forms&mdash;for example, **CreateMutex**, **CreateMutexA**, and **CreateMutexW**.</span></span> <span data-ttu-id="a00c4-112">Nesse caso, pesquise **CreateMutex** com **Coincidir palavra inteira** desmarcada.</span><span class="sxs-lookup"><span data-stu-id="a00c4-112">In that case, search for **CreateMutex** with **Match whole word** unchecked.</span></span>

> [!NOTE]
> <span data-ttu-id="a00c4-113">Você pode instalar o [Visual Studio](https://visualstudio.microsoft.com/downloads/) sem despesas.</span><span class="sxs-lookup"><span data-stu-id="a00c4-113">You can install [Visual Studio](https://visualstudio.microsoft.com/downloads/) without expense.</span></span> <span data-ttu-id="a00c4-114">Uma Community Edition está disponível&mdash; é gratuita para alunos, colaboradores de software de código aberto e indivíduos.</span><span class="sxs-lookup"><span data-stu-id="a00c4-114">A Community edition is available&mdash;it's free for students, open-source contributors, and individuals.</span></span> <span data-ttu-id="a00c4-115">É claro que você pode fazer a mesma coisa com qualquer repositório de amostras.</span><span class="sxs-lookup"><span data-stu-id="a00c4-115">Of course you can do the same thing with any samples repo.</span></span>

## <a name="the-windows-classic-samples-repo"></a><span data-ttu-id="a00c4-116">O repositório de amostras clássicas do Windows</span><span class="sxs-lookup"><span data-stu-id="a00c4-116">The Windows classic samples repo</span></span>

<span data-ttu-id="a00c4-117">O repositório principal que contém aplicativos de exemplo do Windows usando a API do Win32 é o repositório de [exemplos clássico do Windows](https://github.com/Microsoft/Windows-classic-samples) .</span><span class="sxs-lookup"><span data-stu-id="a00c4-117">The main repo containing sample Windows apps using the Win32 API is the [Windows classic samples](https://github.com/Microsoft/Windows-classic-samples) repo.</span></span>

## <a name="directx-samples"></a><span data-ttu-id="a00c4-118">Exemplos do DirectX</span><span class="sxs-lookup"><span data-stu-id="a00c4-118">DirectX samples</span></span>

<span data-ttu-id="a00c4-119">Consulte o repositório [DirectX-Graphics-Samples](https://github.com/Microsoft/DirectX-Graphics-Samples) para exemplos de gráficos do DirectX 12 que demonstram como criar aplicativos com uso intensivo de gráficos para o Windows 10.</span><span class="sxs-lookup"><span data-stu-id="a00c4-119">See the [DirectX-Graphics-Samples](https://github.com/Microsoft/DirectX-Graphics-Samples) repo for DirectX 12 Graphics samples that demonstrate how to build graphics-intensive applications for Windows 10.</span></span>

<span data-ttu-id="a00c4-120">Consulte também [exemplos do DirectX](/windows/uwp/gaming/directx-samples).</span><span class="sxs-lookup"><span data-stu-id="a00c4-120">Also see [DirectX samples](/windows/uwp/gaming/directx-samples).</span></span>

## <a name="older-samples"></a><span data-ttu-id="a00c4-121">Amostras mais antigas</span><span class="sxs-lookup"><span data-stu-id="a00c4-121">Older samples</span></span>

<span data-ttu-id="a00c4-122">Você pode encontrar alguns aplicativos mais antigos de exemplo do Win32 no repositório de [exemplos do MSDN Galeria de código da Microsoft](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208.1%20desktop%20samples/%5BC%2B%2B%5D-Windows%208.1%20desktop%20samples) .</span><span class="sxs-lookup"><span data-stu-id="a00c4-122">You can find some older Win32 sample apps in the [MSDN Code Gallery Microsoft samples](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208.1%20desktop%20samples/%5BC%2B%2B%5D-Windows%208.1%20desktop%20samples) repo.</span></span>

## <a name="see-also"></a><span data-ttu-id="a00c4-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="a00c4-123">See also</span></span>

* [<span data-ttu-id="a00c4-124">Exemplos de código</span><span class="sxs-lookup"><span data-stu-id="a00c4-124">Code samples</span></span>](https://developer.microsoft.com/windows/samples/)
* [<span data-ttu-id="a00c4-125">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a00c4-125">Visual Studio</span></span>](https://visualstudio.microsoft.com/downloads/)
* [<span data-ttu-id="a00c4-126">Amostras clássicas do Windows</span><span class="sxs-lookup"><span data-stu-id="a00c4-126">Windows classic samples</span></span>](https://github.com/Microsoft/Windows-classic-samples)
* [<span data-ttu-id="a00c4-127">DirectX-Graphics-Samples</span><span class="sxs-lookup"><span data-stu-id="a00c4-127">DirectX-Graphics-Samples</span></span>](https://github.com/Microsoft/DirectX-Graphics-Samples)
* [<span data-ttu-id="a00c4-128">Exemplos do DirectX</span><span class="sxs-lookup"><span data-stu-id="a00c4-128">DirectX samples</span></span>](/windows/uwp/gaming/directx-samples)
* [<span data-ttu-id="a00c4-129">Exemplos da Galeria de código do MSDN da Microsoft</span><span class="sxs-lookup"><span data-stu-id="a00c4-129">MSDN Code Gallery Microsoft samples</span></span>](https://github.com/microsoftarchive/msdn-code-gallery-microsoft)
