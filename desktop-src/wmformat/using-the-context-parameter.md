---
title: Usando o parâmetro context
description: Usando o parâmetro context
ms.assetid: 50e37c36-0ce1-4abd-bb25-f18bb164fdeb
keywords:
- SDK do Windows Media Format, parâmetro de contexto
- SDK do Windows Media Format, parâmetro pvContext
- parâmetro pvContext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 084d7ac0f58d3f3e19ae6b1d6f990a1867988bcd
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104084344"
---
# <a name="using-the-context-parameter"></a><span data-ttu-id="c3cc2-106">Usando o parâmetro context</span><span class="sxs-lookup"><span data-stu-id="c3cc2-106">Using the Context Parameter</span></span>

<span data-ttu-id="c3cc2-107">Alguns dos retornos de chamada usados pelo Windows Media Format SDK usam um parâmetro chamado *pvContext*.</span><span class="sxs-lookup"><span data-stu-id="c3cc2-107">Some of the callbacks used by the Windows Media Format SDK take a parameter called *pvContext*.</span></span> <span data-ttu-id="c3cc2-108">Os objetos de chamada passam pelo valor especificado no método que iniciou a ação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="c3cc2-108">The calling objects pass along the value you specify in the method that began the asynchronous action.</span></span> <span data-ttu-id="c3cc2-109">Por exemplo, ao chamar [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open), você pode passar um valor para *pvContext*.</span><span class="sxs-lookup"><span data-stu-id="c3cc2-109">For example, when you call [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open), you can pass a value for *pvContext*.</span></span> <span data-ttu-id="c3cc2-110">Quando o método [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) é chamado pelo objeto Reader para notificar seu aplicativo de que o arquivo foi aberto, ele passará qualquer valor usado em sua chamada para **Open** como o parâmetro *pvContext* de **OnStatus**.</span><span class="sxs-lookup"><span data-stu-id="c3cc2-110">When the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) method is called by the reader object to notify your application that the file has been opened, it will pass whatever value you used in your call to **Open** as the *pvContext* parameter of **OnStatus**.</span></span> <span data-ttu-id="c3cc2-111">Esse parâmetro de contexto é fornecido para seu uso e você pode usá-lo da maneira que desejar.</span><span class="sxs-lookup"><span data-stu-id="c3cc2-111">This context parameter is provided for your use and you can use it in any way you like.</span></span>

<span data-ttu-id="c3cc2-112">O parâmetro *pvContext* é usado com mais frequência quando vários objetos precisam compartilhar o mesmo retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="c3cc2-112">The *pvContext* parameter is most often used when multiple objects need to share the same callback.</span></span> <span data-ttu-id="c3cc2-113">Por exemplo, vários objetos usam o método [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) .</span><span class="sxs-lookup"><span data-stu-id="c3cc2-113">For example, several objects use the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) method.</span></span> <span data-ttu-id="c3cc2-114">Você pode usar *pvContext* para permitir que os diferentes objetos compartilhem uma implementação de **OnStatus** passando um valor diferente para *pvContext* em sua chamada original.</span><span class="sxs-lookup"><span data-stu-id="c3cc2-114">You can use *pvContext* to enable the different objects to share one implementation of **OnStatus** by passing a different value for *pvContext* on your original call.</span></span> <span data-ttu-id="c3cc2-115">Em sua implementação de **OnStatus**, você pode ramificar a lógica de manipulação de mensagens com base no valor de *pvContext*.</span><span class="sxs-lookup"><span data-stu-id="c3cc2-115">In your implementation of **OnStatus**, you can branch the message handling logic based on the value of *pvContext*.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c3cc2-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c3cc2-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3cc2-117">**Usando os métodos de retorno de chamada**</span><span class="sxs-lookup"><span data-stu-id="c3cc2-117">**Using the Callback Methods**</span></span>](using-the-callback-methods.md)
</dt> </dl>

 

 




