---
title: Usando coletores personalizados
description: Usando coletores personalizados
ms.assetid: 7151583a-c7ab-40b0-a7bf-ddd56f93b7aa
keywords:
- ASF (Advanced Systems Format), coletores personalizados
- ASF (formato de sistemas avançados), coletores personalizados
- ASF (Advanced Systems Format), coletores
- ASF (formato de sistemas avançados), coletores
- coletores, coletores personalizados
- coletores personalizados, sobre
- coletores de gravador, coletores personalizados
- coletores personalizados, interface IWMWriterSink
- IWMWriterSink
- coletores de gravador, interface IWMWriterSink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e324d654fa8c85d6145b0f4bf8f20de1f06e125f
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103640141"
---
# <a name="using-custom-sinks"></a><span data-ttu-id="5c8a2-113">Usando coletores personalizados</span><span class="sxs-lookup"><span data-stu-id="5c8a2-113">Using Custom Sinks</span></span>

<span data-ttu-id="5c8a2-114">Se você tiver uma necessidade de gravação especial, poderá criar seus próprios coletores de gravador.</span><span class="sxs-lookup"><span data-stu-id="5c8a2-114">If you have a special writing need, you can create your own writer sinks.</span></span> <span data-ttu-id="5c8a2-115">O gravador mantém uma comunicação unidirecional com um coletor fazendo chamadas para os métodos de [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink).</span><span class="sxs-lookup"><span data-stu-id="5c8a2-115">The writer maintains one-way communication with a sink by making calls to the methods of [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink).</span></span> <span data-ttu-id="5c8a2-116">Para criar seu próprio coletor, implemente a interface **IWMWriterSink** em uma classe em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5c8a2-116">To create your own sink, implement the **IWMWriterSink** interface in a class in your application.</span></span> <span data-ttu-id="5c8a2-117">Esse processo é muito semelhante à implementação de qualquer outra interface de retorno de chamada usada pelos objetos do SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="5c8a2-117">This process is very similar to implementing any other callback interface used by the objects of the Windows Media Format SDK.</span></span> <span data-ttu-id="5c8a2-118">Para obter mais informações sobre retornos de chamada, consulte [usando os métodos de retorno de chamada](using-the-callback-methods.md).</span><span class="sxs-lookup"><span data-stu-id="5c8a2-118">For more information about callbacks, see [Using the Callback Methods](using-the-callback-methods.md).</span></span>

<span data-ttu-id="5c8a2-119">O buffer recebido em [**IWMWriterSink:: Onheader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwritersink-onheader) deve ser gravado no início do arquivo e todos os buffers recebidos em [**OnDataUnit**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwritersink-ondataunit) devem ser gravados em sequência.</span><span class="sxs-lookup"><span data-stu-id="5c8a2-119">The buffer received in [**IWMWriterSink::OnHeader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwritersink-onheader) should be written to the beginning of the file, and all buffers received in [**OnDataUnit**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwritersink-ondataunit) should be written out sequentially.</span></span> <span data-ttu-id="5c8a2-120">O **Onheader** será chamado no início, mas pode ser chamado em outras ocasiões também e, se for, você deverá, se possível, substituir o cabeçalho original.</span><span class="sxs-lookup"><span data-stu-id="5c8a2-120">**OnHeader** will be called at the beginning but might be called at other times, too, and if it is, you should, if possible, overwrite the original header.</span></span> <span data-ttu-id="5c8a2-121">Se o seu aplicativo não puder fazer isso por algum motivo, simplesmente ignore as chamadas de **Onheader** subsequentes.</span><span class="sxs-lookup"><span data-stu-id="5c8a2-121">If your application is not able to do this for some reason, then simply ignore the subsequent **OnHeader** calls.</span></span>

<span data-ttu-id="5c8a2-122">Seu coletor personalizado deve comunicar seu status ao aplicativo de gravação fazendo chamadas para o método de retorno de chamada [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) .</span><span class="sxs-lookup"><span data-stu-id="5c8a2-122">Your custom sink should communicate its status to your writing application by making calls to the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback method.</span></span> <span data-ttu-id="5c8a2-123">Se você implementar o coletor como um objeto COM, talvez queira expor a interface [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) .</span><span class="sxs-lookup"><span data-stu-id="5c8a2-123">If you implement your sink as a COM object, you may want to expose the [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) interface.</span></span> <span data-ttu-id="5c8a2-124">No entanto, você pode passar o endereço do retorno de chamada **OnStatus** para o coletor e definir um contexto da maneira que desejar.</span><span class="sxs-lookup"><span data-stu-id="5c8a2-124">However, you can pass the address of the **OnStatus** callback to your sink and set a context in any way you like.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5c8a2-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5c8a2-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c8a2-126">**Trabalhando com coletores de gravador**</span><span class="sxs-lookup"><span data-stu-id="5c8a2-126">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 




