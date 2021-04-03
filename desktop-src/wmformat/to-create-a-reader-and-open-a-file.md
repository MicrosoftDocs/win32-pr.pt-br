---
title: Para criar um leitor e abrir um arquivo
description: Para criar um leitor e abrir um arquivo
ms.assetid: 82b194d6-7cb7-4b88-9ed7-944b8b43bc29
keywords:
- ASF (Advanced Systems Format), criando leitores
- ASF (formato de sistemas avançados), criando leitores
- Formato de sistema avançado (ASF), abertura de arquivos
- ASF (formato de sistemas avançados), abrindo arquivos
- leitores assíncronos, criando
- leitores assíncronos, abrindo arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8e714f51b56a7d9f3b18a774cd3b8c74bf05352
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "103640296"
---
# <a name="to-create-a-reader-and-open-a-file"></a><span data-ttu-id="68456-109">Para criar um leitor e abrir um arquivo</span><span class="sxs-lookup"><span data-stu-id="68456-109">To Create a Reader and Open a File</span></span>

<span data-ttu-id="68456-110">Antes de poder fazer qualquer trabalho com o leitor, você precisará criar um objeto leitor e carregar um arquivo para leitura.</span><span class="sxs-lookup"><span data-stu-id="68456-110">Before you can do any work with the reader, you will need to create a reader object and load a file for reading.</span></span> <span data-ttu-id="68456-111">Para inicializar o leitor e abrir um arquivo, execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="68456-111">To initialize the reader and open a file, perform the following steps.</span></span>

1.  <span data-ttu-id="68456-112">Crie um objeto leitor chamando a função [**WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader) .</span><span class="sxs-lookup"><span data-stu-id="68456-112">Create a reader object by calling the [**WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader) function.</span></span> <span data-ttu-id="68456-113">Você deve especificar o nível desejado de gerenciamento de direitos para o novo objeto de leitor.</span><span class="sxs-lookup"><span data-stu-id="68456-113">You must specify the desired level of rights management for the new reader object.</span></span> <span data-ttu-id="68456-114">Os modos disponíveis são listados no tipo de enumeração [**\_ direitos WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_rights) .</span><span class="sxs-lookup"><span data-stu-id="68456-114">The available modes are listed in the [**WMT\_RIGHTS**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_rights) enumeration type.</span></span>
2.  <span data-ttu-id="68456-115">Especifique um arquivo para ler chamando [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open).</span><span class="sxs-lookup"><span data-stu-id="68456-115">Specify a file to read by calling [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open).</span></span> <span data-ttu-id="68456-116">Você deve especificar uma interface de retorno de chamada de leitura para o leitor usar.</span><span class="sxs-lookup"><span data-stu-id="68456-116">You must specify a reader callback interface for the reader to use.</span></span> <span data-ttu-id="68456-117">Para obter mais informações sobre o retorno de chamada de leitor, consulte [para implementar mensagens de leitor no retorno de chamada OnStatus](to-implement-reader-messages-in-the-onstatus-callback.md).</span><span class="sxs-lookup"><span data-stu-id="68456-117">For more information about the reader callback, see [To Implement Reader Messages in the OnStatus Callback](to-implement-reader-messages-in-the-onstatus-callback.md).</span></span>
3.  <span data-ttu-id="68456-118">Aguarde até que o leitor Abra o arquivo.</span><span class="sxs-lookup"><span data-stu-id="68456-118">Wait for the reader to open the file.</span></span> <span data-ttu-id="68456-119">Quando você chama **Open** para carregar um arquivo, ele retorna quase imediatamente e continua o processamento em outro thread.</span><span class="sxs-lookup"><span data-stu-id="68456-119">When you call **Open** to load a file, it returns almost immediately and continues processing on another thread.</span></span> <span data-ttu-id="68456-120">Você deve aguardar a conclusão das operações, sinalizando um evento quando o retorno de chamada **OnStatus** receber a \_ mensagem de status WMT aberta.</span><span class="sxs-lookup"><span data-stu-id="68456-120">You should wait for operations to complete, by signaling an event when the **OnStatus** callback receives the WMT\_OPENED status message.</span></span>

<span data-ttu-id="68456-121">O leitor também dá suporte ao uso da interface com de **IStream** para abrir arquivos.</span><span class="sxs-lookup"><span data-stu-id="68456-121">The reader also supports the use of the **IStream** COM interface for opening files.</span></span> <span data-ttu-id="68456-122">Você pode implementar a interface **IStream** da maneira que escolher.</span><span class="sxs-lookup"><span data-stu-id="68456-122">You can implement the **IStream** interface any way you choose.</span></span> <span data-ttu-id="68456-123">Depois que o arquivo desejado for aberto em **IStream**, você poderá seguir as etapas listadas acima, exceto pelo fato de que você deve chamar [**IWMReaderAdvanced2:: OpenStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-openstream) em vez de **IWMReader:: Open** na etapa 2.</span><span class="sxs-lookup"><span data-stu-id="68456-123">After the desired file is opened in **IStream**, you can follow the steps listed above, except that you must call [**IWMReaderAdvanced2::OpenStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-openstream) instead of **IWMReader::Open** in step 2.</span></span>

## <a name="related-topics"></a><span data-ttu-id="68456-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="68456-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68456-125">**Interface IWMReader**</span><span class="sxs-lookup"><span data-stu-id="68456-125">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="68456-126">**Interface IWMReaderAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="68456-126">**IWMReaderAdvanced2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> <dt>

[<span data-ttu-id="68456-127">**Interface IWMStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="68456-127">**IWMStatusCallback Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback)
</dt> <dt>

[<span data-ttu-id="68456-128">**Lendo arquivos com o leitor assíncrono**</span><span class="sxs-lookup"><span data-stu-id="68456-128">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="68456-129">**Usando os métodos de retorno de chamada**</span><span class="sxs-lookup"><span data-stu-id="68456-129">**Using the Callback Methods**</span></span>](using-the-callback-methods.md)
</dt> </dl>

 

 




