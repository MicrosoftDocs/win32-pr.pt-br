---
title: Usando os métodos de retorno de chamada
description: Usando os métodos de retorno de chamada
ms.assetid: 098cb90b-8c21-4692-a4f9-bacce042520a
keywords:
- SDK do Windows Media Format, métodos de retorno de chamada
- Windows Media Format SDK, métodos chamados de forma assíncrona
- métodos de retorno de chamada
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d39201c101c9031a7157f79f6c12ec88f07decfc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103640125"
---
# <a name="using-the-callback-methods"></a><span data-ttu-id="d5530-106">Usando os métodos de retorno de chamada</span><span class="sxs-lookup"><span data-stu-id="d5530-106">Using the Callback Methods</span></span>

<span data-ttu-id="d5530-107">Várias interfaces no SDK do Windows Media Format contêm métodos que são chamados de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="d5530-107">Several interfaces in the Windows Media Format SDK contain methods that are called asynchronously.</span></span> <span data-ttu-id="d5530-108">A maioria desses métodos usa funções de retorno de chamada para passar informações para o aplicativo de controle.</span><span class="sxs-lookup"><span data-stu-id="d5530-108">Most of these methods use callback functions to pass information to the controlling application.</span></span>

<span data-ttu-id="d5530-109">As seções a seguir descrevem alguns dos problemas gerais relacionados ao uso de métodos de retorno de chamada com o SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="d5530-109">The following sections describe some of the general issues regarding the use of callback methods with the Windows Media Format SDK.</span></span>



| <span data-ttu-id="d5530-110">Seção</span><span class="sxs-lookup"><span data-stu-id="d5530-110">Section</span></span>                                                                          | <span data-ttu-id="d5530-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="d5530-111">Description</span></span>                                                                                                                                                                                          |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d5530-112">Usando o retorno de chamada OnStatus</span><span class="sxs-lookup"><span data-stu-id="d5530-112">Using the OnStatus Callback</span></span>](using-the-onstatus-callback.md)                   | <span data-ttu-id="d5530-113">Descreve como implementar o método de retorno de chamada [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) , que é usado por vários objetos para aconselhar aplicativos de andamento da operação do SDK.</span><span class="sxs-lookup"><span data-stu-id="d5530-113">Describes how to implement the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback method, which is used by several objects to advise applications of SDK operation progress.</span></span> |
| [<span data-ttu-id="d5530-114">Usando eventos com chamadas assíncronas</span><span class="sxs-lookup"><span data-stu-id="d5530-114">Using Events with Asynchronous Calls</span></span>](using-events-with-asynchronous-calls.md) | <span data-ttu-id="d5530-115">Descreve uma técnica comum para lidar com chamadas de método assíncrono em um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d5530-115">Describes a common technique to handle asynchronous method calls in an application.</span></span>                                                                                                                  |
| [<span data-ttu-id="d5530-116">Usando o parâmetro context</span><span class="sxs-lookup"><span data-stu-id="d5530-116">Using the Context Parameter</span></span>](using-the-context-parameter.md)                   | <span data-ttu-id="d5530-117">Apresenta o parâmetro *pvContext* , compartilhado por vários retornos de chamada e seus métodos de chamada, e explica como usá-lo.</span><span class="sxs-lookup"><span data-stu-id="d5530-117">Introduces the *pvContext* parameter, shared by several callbacks and their calling methods, and explains how to use it.</span></span>                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="d5530-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d5530-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5530-119">**Guia de programação**</span><span class="sxs-lookup"><span data-stu-id="d5530-119">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 




