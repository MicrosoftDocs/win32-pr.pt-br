---
title: Entendendo o Direct3D 12
description: Para escrever jogos e aplicativos 3D para Windows 10 e Windows 10 Mobile, você deve compreender os conceitos básicos da tecnologia do Direct3D 12 e como se preparar para usá-lo em seus jogos e aplicativos.
ms.assetid: DED7A434-FCD4-4F41-8B2C-E5AE6E48430F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1353c8c66fd401e364b9db302463f164f757c9ac
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548317"
---
# <a name="understanding-direct3d-12"></a><span data-ttu-id="8607a-103">Entendendo o Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="8607a-103">Understanding Direct3D 12</span></span>

<span data-ttu-id="8607a-104">Para escrever jogos e aplicativos 3D para Windows 10 e Windows 10 Mobile, você deve compreender os conceitos básicos da tecnologia do Direct3D 12 e como se preparar para usá-lo em seus jogos e aplicativos.</span><span class="sxs-lookup"><span data-stu-id="8607a-104">To write 3D games and apps for Windows 10 and Windows 10 Mobile, you must understand the basics of the Direct3D 12 technology, and how to prepare to use it in your games and apps.</span></span>

<span data-ttu-id="8607a-105">Use os tópicos desta seção para configurar e aprender sobre o ambiente no qual você programará seus aplicativos e jogos com o Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="8607a-105">Use the topics in this section to set up and learn about the environment in which you will program your apps and games with Direct3D 12.</span></span> <span data-ttu-id="8607a-106">Esse conteúdo também ajudará a portar seus aplicativos e jogos do Direct3D 11 para o Direct3D 12, para que você possa aproveitar os recursos e as eficiências do Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="8607a-106">This content will also help you to port your Direct3D 11 apps and games to Direct3D 12, so you can take advantage of Direct3D 12 features and efficiencies.</span></span>

<span data-ttu-id="8607a-107">Para programar com o Direct3D 12, você precisa destes componentes:</span><span class="sxs-lookup"><span data-stu-id="8607a-107">To program with Direct3D 12, you need these components:</span></span>

-   <span data-ttu-id="8607a-108">Uma plataforma de hardware com uma GPU compatível com o Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="8607a-108">A hardware platform with a Direct3D 12-compatible GPU</span></span>
-   <span data-ttu-id="8607a-109">[Exibir drivers](/previous-versions//ff569172(v=vs.85)) que dão suporte ao Windows Display Driver Model (WDDM) 2,0</span><span class="sxs-lookup"><span data-stu-id="8607a-109">[Display drivers](/previous-versions//ff569172(v=vs.85)) that support the Windows Display Driver Model (WDDM) 2.0</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8607a-110">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="8607a-110">In this section</span></span>



| <span data-ttu-id="8607a-111">Tópico</span><span class="sxs-lookup"><span data-stu-id="8607a-111">Topic</span></span>                                                                                                               | <span data-ttu-id="8607a-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="8607a-112">Description</span></span>                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8607a-113">Configuração do ambiente de programação do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="8607a-113">Direct3D 12 Programming Environment Setup</span></span>](directx-12-programming-environment-set-up.md)<br/>               | <span data-ttu-id="8607a-114">Descreve a instalação, as ferramentas e as bibliotecas com suporte que compõem um ambiente de desenvolvimento Direct3D 12 produtivo.</span><span class="sxs-lookup"><span data-stu-id="8607a-114">Describes the installation, tools and supported libraries that make up a productive Direct3D 12 development environment.</span></span> <br/>                              |
| [<span data-ttu-id="8607a-115">Criando um componente básico do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="8607a-115">Creating a Basic Direct3D 12 Component</span></span>](creating-a-basic-direct3d-12-component.md)<br/>                     | <span data-ttu-id="8607a-116">Este tópico descreve o fluxo de chamadas para criar um componente básico do Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="8607a-116">This topic describes the call flow to create a basic Direct3D 12 component.</span></span><br/>                                                                            |
| [<span data-ttu-id="8607a-117">Alterações importantes do Direct3D 11 para o Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="8607a-117">Important Changes from Direct3D 11 to Direct3D 12</span></span>](important-changes-from-directx-11-to-directx-12.md)<br/> | <span data-ttu-id="8607a-118">O Direct3D 12 representa um desvio significativo do modelo de programação do Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="8607a-118">Direct3D 12 represents a significant departure from the Direct3D 11 programming model.</span></span> <span data-ttu-id="8607a-119">O Direct3D 12 permite que os aplicativos fiquem mais próximos do hardware do que nunca.</span><span class="sxs-lookup"><span data-stu-id="8607a-119">Direct3D 12 lets apps get closer to hardware than ever before.</span></span> <br/> |
| [<span data-ttu-id="8607a-120">Níveis de recursos de hardware</span><span class="sxs-lookup"><span data-stu-id="8607a-120">Hardware Feature Levels</span></span>](hardware-feature-levels.md)<br/>                                                   | <span data-ttu-id="8607a-121">Descreve a funcionalidade dos 11 \_ 0 a 12 \_ 1 níveis de recursos de hardware.</span><span class="sxs-lookup"><span data-stu-id="8607a-121">Describes the functionality of the 11\_0 through 12\_1 hardware feature levels.</span></span><br/>                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="8607a-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8607a-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8607a-123">Guia de programação do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="8607a-123">Direct3D 12 Programming Guide</span></span>](directx-12-programming-guide.md)
</dt> </dl>

 

