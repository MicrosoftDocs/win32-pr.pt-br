---
title: Extensões ADSI
description: Uma extensão ADSI é um objeto COM especial que permite que um desenvolvedor estenda um objeto ADSI.
ms.assetid: 3e40e702-089a-4d2a-806c-cd5b29d11bfd
ms.tgt_platform: multiple
keywords:
- Extensões ADSI
- ADSI ADSI, usando extensões
- ADSI de extensões
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a3852e64ad282c11ecd17c6b13904738ee7f46a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004883"
---
# <a name="adsi-extensions"></a><span data-ttu-id="edfea-106">Extensões ADSI</span><span class="sxs-lookup"><span data-stu-id="edfea-106">ADSI Extensions</span></span>

<span data-ttu-id="edfea-107">Uma extensão ADSI é um objeto COM especial que permite que um desenvolvedor estenda um objeto ADSI.</span><span class="sxs-lookup"><span data-stu-id="edfea-107">An ADSI extension is a special COM object that enable a developer to extend an ADSI object.</span></span> <span data-ttu-id="edfea-108">Cada extensão é associada a uma classe especificada no diretório.</span><span class="sxs-lookup"><span data-stu-id="edfea-108">Each extension is associated with a specified class in the directory.</span></span> <span data-ttu-id="edfea-109">Com esse modelo de extensão, os desenvolvedores podem adicionar métodos para fornecer um significado mais dinâmico a um objeto.</span><span class="sxs-lookup"><span data-stu-id="edfea-109">With this extension model, developers can add methods to give more dynamic meaning to an object.</span></span> <span data-ttu-id="edfea-110">Em um modelo de programação de diretório tradicional, um objeto é acessado obtendo e configurando os atributos de objeto.</span><span class="sxs-lookup"><span data-stu-id="edfea-110">In a traditional directory programming model, an object is accessed by getting and setting the object attributes.</span></span> <span data-ttu-id="edfea-111">Usando extensões ADSI, você pode adicionar mais recursos a um objeto de diretório.</span><span class="sxs-lookup"><span data-stu-id="edfea-111">Using ADSI extensions, you can add more features to a directory object.</span></span>

<span data-ttu-id="edfea-112">Esta seção aborda os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="edfea-112">This section discusses the following topics:</span></span>

-   [<span data-ttu-id="edfea-113">Benefícios do uso de extensões ADSI</span><span class="sxs-lookup"><span data-stu-id="edfea-113">Benefits of Using ADSI Extensions</span></span>](benefits-of-using-adsi-extensions.md)
-   [<span data-ttu-id="edfea-114">Arquitetura de extensão ADSI</span><span class="sxs-lookup"><span data-stu-id="edfea-114">ADSI Extension Architecture</span></span>](adsi-extension-architecture.md)
-   [<span data-ttu-id="edfea-115">Como a ADSI integra extensões</span><span class="sxs-lookup"><span data-stu-id="edfea-115">How ADSI Integrates Extensions</span></span>](adsi-and-extensions.md)
-   [<span data-ttu-id="edfea-116">O que um cliente vê?</span><span class="sxs-lookup"><span data-stu-id="edfea-116">What Does a Client See?</span></span>](what-does-a-client-see.md)
-   [<span data-ttu-id="edfea-117">Obtendo interfaces ADSI de sua extensão</span><span class="sxs-lookup"><span data-stu-id="edfea-117">Getting ADSI Interfaces From Your Extension</span></span>](getting-adsi-interfaces-from-your-extension.md)
-   [<span data-ttu-id="edfea-118">Bibliotecas de tipos de extensão ADSI</span><span class="sxs-lookup"><span data-stu-id="edfea-118">ADSI Extension Type Libraries</span></span>](adsi-extension-type-libraries.md)
-   [<span data-ttu-id="edfea-119">Suporte de associação antecipada</span><span class="sxs-lookup"><span data-stu-id="edfea-119">Early Binding Support</span></span>](early-binding-support.md)
-   [<span data-ttu-id="edfea-120">Suporte à ligação tardia</span><span class="sxs-lookup"><span data-stu-id="edfea-120">Late Binding Support</span></span>](late-binding-support.md)
-   [<span data-ttu-id="edfea-121">Interface IADsExtension</span><span class="sxs-lookup"><span data-stu-id="edfea-121">IADsExtension Interface</span></span>](iadsextension-interface.md)
-   [<span data-ttu-id="edfea-122">Suporte a interfaces duplas ou de expedição</span><span class="sxs-lookup"><span data-stu-id="edfea-122">Supporting Dual or Dispatch Interfaces</span></span>](supporting-dual-or-dispatch-interfaces.md)
-   [<span data-ttu-id="edfea-123">Revisitando regras de agregação com com extensões ADSI</span><span class="sxs-lookup"><span data-stu-id="edfea-123">Revisiting COM Aggregation Rules with ADSI Extensions</span></span>](revisiting-com-aggregation-rules-with-adsi-extensions.md)
-   [<span data-ttu-id="edfea-124">Resolução de vários componentes de agregação com suporte para a mesma interface</span><span class="sxs-lookup"><span data-stu-id="edfea-124">Resolution of Multiple Aggregation Components Supporting the Same Interface</span></span>](resolution-of-multiple-aggregation-components-supporting-the-same-interface.md)
-   [<span data-ttu-id="edfea-125">Resolução de conflitos de nome de função/Propriedade em automação em extensões</span><span class="sxs-lookup"><span data-stu-id="edfea-125">Resolution of Function/Property Name Conflicts in Automation in Extensions</span></span>](resolution-of-functionproperty-name-conflicts-in-automation-in-extensions.md)

 

 




