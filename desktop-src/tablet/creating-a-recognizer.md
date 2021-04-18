---
description: Se você optar por fazer isso, seu aplicativo poderá fornecer suas próprias implementações de reconhecedor. Esta seção descreve os requisitos para criar um reconhecedor de aplicativo personalizado para seu aplicativo que você pode usar com a API da plataforma Tablet PC.
ms.assetid: 502ef3fb-ba45-4f8b-bbd5-19c24e313439
title: Criando um reconhecedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bc71f56dc7095c6c72d18b36c3a12caa493ec9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763910"
---
# <a name="creating-a-recognizer"></a><span data-ttu-id="ddf85-104">Criando um reconhecedor</span><span class="sxs-lookup"><span data-stu-id="ddf85-104">Creating a Recognizer</span></span>

<span data-ttu-id="ddf85-105">Se você optar por fazer isso, seu aplicativo poderá fornecer suas próprias implementações de reconhecedor.</span><span class="sxs-lookup"><span data-stu-id="ddf85-105">If you choose to do so, your application can provide its own recognizer implementations.</span></span> <span data-ttu-id="ddf85-106">Esta seção descreve os requisitos para criar um reconhecedor de aplicativo personalizado para seu aplicativo que você pode usar com a API da plataforma Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="ddf85-106">This section describes the requirements for creating a custom application recognizer for your application that you can use with the Tablet PC Platform API.</span></span>

> [!Note]  
> <span data-ttu-id="ddf85-107">Os reconhecedores de aplicativos personalizados não são usados pelo painel de entrada do Tablet PC ou pelo diário do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="ddf85-107">Custom application recognizers are not used by the Tablet PC Input Panel or Microsoft Windows Journal.</span></span> <span data-ttu-id="ddf85-108">Esses acessórios usam apenas os reconhecedores com os quais foram testados.</span><span class="sxs-lookup"><span data-stu-id="ddf85-108">These accessories use only recognizers with which they have been tested.</span></span>

 

<span data-ttu-id="ddf85-109">As seções a seguir detalham a implementação de um reconhecedor personalizado:</span><span class="sxs-lookup"><span data-stu-id="ddf85-109">The following sections detail the implementation of a custom recognizer:</span></span>

-   [<span data-ttu-id="ddf85-110">Arquitetura da API de reconhecimento</span><span class="sxs-lookup"><span data-stu-id="ddf85-110">Recognition API Architecture</span></span>](recognition-api-architecture.md)
-   <span data-ttu-id="ddf85-111">[APIs de reconhecimento necessárias](/previous-versions//ms701664(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ddf85-111">[Required Recognition APIs](/previous-versions//ms701664(v=vs.85))</span></span>
-   [<span data-ttu-id="ddf85-112">HRECOGNIZER e HRECOCONTEXT</span><span class="sxs-lookup"><span data-stu-id="ddf85-112">HRECOGNIZER and HRECOCONTEXT</span></span>](hrecognizer-and-hrecocontext.md)
-   [<span data-ttu-id="ddf85-113">Estrutura malha do reconhecedor</span><span class="sxs-lookup"><span data-stu-id="ddf85-113">Recognizer Lattice Structure</span></span>](recognizer-lattice-structure.md)
-   [<span data-ttu-id="ddf85-114">Registrando a DLL do reconhecedor</span><span class="sxs-lookup"><span data-stu-id="ddf85-114">Registering Your Recognizer DLL</span></span>](registering-your-recognizer-dll.md)
-   [<span data-ttu-id="ddf85-115">Considerações de Threading do reconhecedor</span><span class="sxs-lookup"><span data-stu-id="ddf85-115">Recognizer Threading Considerations</span></span>](recognizer-threading-considerations.md)
-   [<span data-ttu-id="ddf85-116">Sequência de chamada típica</span><span class="sxs-lookup"><span data-stu-id="ddf85-116">Typical Calling Sequence</span></span>](typical-calling-sequence.md)
-   [<span data-ttu-id="ddf85-117">Modelo de exemplo de DLL do Recognizer</span><span class="sxs-lookup"><span data-stu-id="ddf85-117">Recognizer DLL Sample Template</span></span>](recognizer-dll-sample-template.md)
-   [<span data-ttu-id="ddf85-118">Valores de intervalo Unicode de gestos</span><span class="sxs-lookup"><span data-stu-id="ddf85-118">Unicode Range Values of Gestures</span></span>](unicode-range-values-of-gestures.md)
-   [<span data-ttu-id="ddf85-119">APIs do Recognizer</span><span class="sxs-lookup"><span data-stu-id="ddf85-119">Recognizer APIs</span></span>](recognizer-apis.md)

 

 
