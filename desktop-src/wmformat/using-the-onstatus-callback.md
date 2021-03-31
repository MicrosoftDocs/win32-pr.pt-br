---
title: Usando o retorno de chamada OnStatus
description: Usando o retorno de chamada OnStatus
ms.assetid: 598e2d13-709b-42a3-ae06-b8c7d208ca9e
keywords:
- SDK do Windows Media Format, método de retorno de chamada OnStatus
- SDK do Windows Media Format, interface IWMStatusCallback
- Método de retorno de chamada OnStatus, sobre
- IWMStatusCallback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56e96b8d7fd75fd8a1d97a56c8b09304c51d0238
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103916970"
---
# <a name="using-the-onstatus-callback"></a><span data-ttu-id="305bc-107">Usando o retorno de chamada OnStatus</span><span class="sxs-lookup"><span data-stu-id="305bc-107">Using the OnStatus Callback</span></span>

<span data-ttu-id="305bc-108">O método de retorno de chamada [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) é chamado por vários objetos no SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="305bc-108">The [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback method is called by several objects in the Windows Media Format SDK.</span></span> <span data-ttu-id="305bc-109">**OnStatus** recebe mensagens que representam as alterações no status das operações do SDK.</span><span class="sxs-lookup"><span data-stu-id="305bc-109">**OnStatus** receives messages that represent changes in the status of SDK operations.</span></span>

<span data-ttu-id="305bc-110">Para usar o método de retorno de chamada **OnStatus** , você deve implementar uma classe em seu aplicativo que herde da interface [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) .</span><span class="sxs-lookup"><span data-stu-id="305bc-110">To use the **OnStatus** callback method, you must implement a class in your application that inherits from the [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) interface.</span></span> <span data-ttu-id="305bc-111">Inclua o código para sua versão do **OnStatus** na classe.</span><span class="sxs-lookup"><span data-stu-id="305bc-111">Include code for your version of **OnStatus** in the class.</span></span> <span data-ttu-id="305bc-112">Vários exemplos de implementações de **OnStatus** podem ser encontrados nos exemplos incluídos neste SDK.</span><span class="sxs-lookup"><span data-stu-id="305bc-112">Several examples of **OnStatus** implementations can be found in the samples included with this SDK.</span></span> <span data-ttu-id="305bc-113">Para obter mais informações sobre os exemplos, consulte [aplicativos de exemplo](sample-applications.md).</span><span class="sxs-lookup"><span data-stu-id="305bc-113">For more information about the samples, see [Sample Applications](sample-applications.md).</span></span>

<span data-ttu-id="305bc-114">Você deve associar sua implementação do retorno de chamada de status com vários objetos do Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="305bc-114">You must associate your implementation of the status callback with various objects of the Windows Media Format SDK.</span></span> <span data-ttu-id="305bc-115">Cada objeto tem uma maneira diferente de fazer essa associação.</span><span class="sxs-lookup"><span data-stu-id="305bc-115">Each object has a different way of making this association.</span></span> <span data-ttu-id="305bc-116">Para obter uma lista dos métodos que associam objetos específicos, consulte a página de referência do **IWMStatusCallback** .</span><span class="sxs-lookup"><span data-stu-id="305bc-116">For a list of the methods that associate specific objects, see the **IWMStatusCallback** reference page.</span></span>

<span data-ttu-id="305bc-117">As mensagens de status que podem ser recebidas por **OnStatus** são definidas no tipo de enumeração [**\_ status WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) .</span><span class="sxs-lookup"><span data-stu-id="305bc-117">The status messages that can be received by **OnStatus** are defined in the [**WMT\_STATUS**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) enumeration type.</span></span>

<span data-ttu-id="305bc-118">Você pode escolher quais mensagens interceptar e quais ignorar.</span><span class="sxs-lookup"><span data-stu-id="305bc-118">You can choose which messages to trap and which to ignore.</span></span> <span data-ttu-id="305bc-119">No entanto, responder a algumas mensagens de status é necessário para determinados recursos.</span><span class="sxs-lookup"><span data-stu-id="305bc-119">However, responding to some status messages is required for certain features.</span></span> <span data-ttu-id="305bc-120">Por exemplo, ao usar o leitor assíncrono, o método [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) abre um arquivo de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="305bc-120">For example, when using the asynchronous reader, the [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) method opens a file asynchronously.</span></span> <span data-ttu-id="305bc-121">A única maneira de saber quando o arquivo foi aberto é interceptar a \_ mensagem aberta MWT.</span><span class="sxs-lookup"><span data-stu-id="305bc-121">The only way to tell when the file has been opened is to trap the MWT\_OPENED message.</span></span> <span data-ttu-id="305bc-122">Normalmente, as mensagens às quais você responde são notificações sobre a conclusão de tarefas assíncronas.</span><span class="sxs-lookup"><span data-stu-id="305bc-122">Typically, the messages you respond to are notifications of the completion of asynchronous tasks.</span></span>

## <a name="related-topics"></a><span data-ttu-id="305bc-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="305bc-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="305bc-124">**Usando os métodos de retorno de chamada**</span><span class="sxs-lookup"><span data-stu-id="305bc-124">**Using the Callback Methods**</span></span>](using-the-callback-methods.md)
</dt> </dl>

 

 




