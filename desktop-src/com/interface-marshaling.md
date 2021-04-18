---
title: Empacotamento de interface
description: Empacotamento de interface
ms.assetid: 71069bd3-5f90-406a-be78-bb1af9b1c1c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5112b67e643fb95e1025fd4ed297043f81f576e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105789364"
---
# <a name="interface-marshaling"></a><span data-ttu-id="a131e-103">Empacotamento de interface</span><span class="sxs-lookup"><span data-stu-id="a131e-103">Interface Marshaling</span></span>

<span data-ttu-id="a131e-104">A menos que você saiba além de todas as dúvidas de que sua interface nunca será usada em limites de apartamento, thread ou processo, você precisa decidir como fornecer suporte de marshaling para suas interfaces.</span><span class="sxs-lookup"><span data-stu-id="a131e-104">Unless you know beyond all doubt that your interface will never be used across apartment, thread, or process boundaries, you need to decide how to provide marshaling support for your interfaces.</span></span> <span data-ttu-id="a131e-105">Há três maneiras de fornecer suporte ao marshaling:</span><span class="sxs-lookup"><span data-stu-id="a131e-105">There are three ways to provide marshaling support:</span></span>

-   <span data-ttu-id="a131e-106">Escreva seu próprio código de proxy/stub que chama o canal COM que, por sua vez, chama as bibliotecas de tempo de execução RPC.</span><span class="sxs-lookup"><span data-stu-id="a131e-106">Write your own proxy/stub code that calls the COM channel, which in turn calls the RPC run-time libraries.</span></span> <span data-ttu-id="a131e-107">Teoricamente, é possível fazer isso, mas na prática é quase impossível fazer isso sem uma quantidade significativa de esforço.</span><span class="sxs-lookup"><span data-stu-id="a131e-107">Theoretically, it is possible to do this, but in practice it is almost impossible to do without a significant amount of effort.</span></span>
-   <span data-ttu-id="a131e-108">Descreva suas interfaces em um arquivo IDL (linguagem de definição de interface) e use o compilador MIDL para gerar uma DLL de proxy/stub.</span><span class="sxs-lookup"><span data-stu-id="a131e-108">Describe your interfaces in an interface definition language (IDL) file and use the MIDL compiler to generate a proxy/stub DLL.</span></span> <span data-ttu-id="a131e-109">Esse método fornece o melhor desempenho e maior flexibilidade em termos de tipos de dados aceitáveis.</span><span class="sxs-lookup"><span data-stu-id="a131e-109">This method provides the best performance and the most flexibility in terms of acceptable data types.</span></span> <span data-ttu-id="a131e-110">Usando stubs de proxy gerados por MIDL, você pode controlar não apenas o gerenciamento de memória, mas até mesmo o marshaling e o desempacotamento de tipos de dados complexos em diferentes plataformas.</span><span class="sxs-lookup"><span data-stu-id="a131e-110">Using MIDL-generated proxy stubs, you can control not only memory management but even the marshaling and unmarshaling of complex data types across different platforms.</span></span>
-   <span data-ttu-id="a131e-111">Use MIDL para gerar uma biblioteca de tipos que o sistema usa para fornecer suporte de marshaling em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="a131e-111">Use MIDL to generate a type library that the system uses to provide marshaling support at run time.</span></span> <span data-ttu-id="a131e-112">Essa é a maneira mais fácil de implementar o suporte de marshaling.</span><span class="sxs-lookup"><span data-stu-id="a131e-112">This is the easiest way to implement marshaling support.</span></span> <span data-ttu-id="a131e-113">Tudo o que você precisa fazer é gerar uma biblioteca de tipos e registrá-la.</span><span class="sxs-lookup"><span data-stu-id="a131e-113">All you have to do is generate a type library and register it.</span></span> <span data-ttu-id="a131e-114">Suas interfaces devem ser compatíveis com a automação ( [**oleautomation**](/windows/desktop/Midl/oleautomation) ou [**Dual**](/windows/desktop/Midl/dual)), que coloca algumas restrições nos tipos de tipos de dados que você pode usar como parâmetros de método.</span><span class="sxs-lookup"><span data-stu-id="a131e-114">Your interfaces must be Automation-compatible (either [**oleautomation**](/windows/desktop/Midl/oleautomation) or [**dual**](/windows/desktop/Midl/dual)), which places some restrictions on the kinds of data types you can use as method parameters.</span></span> <span data-ttu-id="a131e-115">No entanto, na maioria dos casos, a vantagem de ter suas interfaces acessíveis a programas escritos em outras linguagens, como o Microsoft Visual Basic e o Java, supera as limitações dos tipos de dados.</span><span class="sxs-lookup"><span data-stu-id="a131e-115">However, in most cases, the advantage of having your interfaces accessible to programs written in other languages, such as Microsoft Visual Basic and Java, outweighs the limitations on data types.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a131e-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a131e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a131e-117">Comunicação entre objetos</span><span class="sxs-lookup"><span data-stu-id="a131e-117">Inter-Object Communication</span></span>](inter-object-communication.md)
</dt> </dl>

 

 