---
title: Para criar um leitor síncrono e abrir um arquivo
description: Para criar um leitor síncrono e abrir um arquivo
ms.assetid: 6349d05e-20db-4ce8-83fd-cad4cec666f2
keywords:
- ASF (Advanced Systems Format), criando leitores
- ASF (formato de sistemas avançados), criando leitores
- Formato de sistema avançado (ASF), abertura de arquivos
- ASF (formato de sistemas avançados), abrindo arquivos
- leitores síncronos, criando
- leitores síncronos, abrindo arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e222c046a685885fa9e17baa52d0161176551ff3
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "105797902"
---
# <a name="to-create-a-synchronous-reader-and-open-a-file"></a><span data-ttu-id="3ed64-109">Para criar um leitor síncrono e abrir um arquivo</span><span class="sxs-lookup"><span data-stu-id="3ed64-109">To Create a Synchronous Reader and Open a File</span></span>

<span data-ttu-id="3ed64-110">Antes de poder fazer qualquer trabalho com o leitor síncrono, você precisará criar um objeto leitor síncrono e carregar um arquivo para leitura.</span><span class="sxs-lookup"><span data-stu-id="3ed64-110">Before you can do any work with the synchronous reader, you will need to create a synchronous reader object and load a file for reading.</span></span> <span data-ttu-id="3ed64-111">Para inicializar o leitor síncrono e abrir um arquivo, execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="3ed64-111">To initialize the synchronous reader and open a file, perform the following steps.</span></span>

1.  <span data-ttu-id="3ed64-112">Crie um objeto leitor síncrono chamando a função [**WMCreateSyncReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader) .</span><span class="sxs-lookup"><span data-stu-id="3ed64-112">Create a synchronous reader object by calling the [**WMCreateSyncReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader) function.</span></span> <span data-ttu-id="3ed64-113">Você deve especificar o nível desejado de gerenciamento de direitos para o novo objeto de leitor.</span><span class="sxs-lookup"><span data-stu-id="3ed64-113">You must specify the desired level of rights management for the new reader object.</span></span> <span data-ttu-id="3ed64-114">Os modos disponíveis são listados no tipo de enumeração **\_ direitos WMT** .</span><span class="sxs-lookup"><span data-stu-id="3ed64-114">The available modes are listed in the **WMT\_RIGHTS** enumeration type.</span></span>
2.  <span data-ttu-id="3ed64-115">Especifique um arquivo para ler chamando [**IWMSyncReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-open).</span><span class="sxs-lookup"><span data-stu-id="3ed64-115">Specify a file to read by calling [**IWMSyncReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-open).</span></span>

<span data-ttu-id="3ed64-116">O leitor síncrono também dá suporte ao uso da interface com de **IStream** para abrir arquivos.</span><span class="sxs-lookup"><span data-stu-id="3ed64-116">The synchronous reader also supports the use of the **IStream** COM interface for opening files.</span></span> <span data-ttu-id="3ed64-117">Você pode implementar a interface **IStream** da maneira que escolher.</span><span class="sxs-lookup"><span data-stu-id="3ed64-117">You can implement the **IStream** interface any way you choose.</span></span> <span data-ttu-id="3ed64-118">Depois que o arquivo desejado for aberto em **IStream**, você poderá seguir as etapas listadas acima, exceto pelo fato de que você deve chamar [**IWMSyncReader:: OpenStream**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-openstream) em vez de **IWMSyncReader:: Open** na etapa 2.</span><span class="sxs-lookup"><span data-stu-id="3ed64-118">After the desired file is opened in **IStream**, you can follow the steps listed above, except that you must call [**IWMSyncReader::OpenStream**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-openstream) instead of **IWMSyncReader::Open** in step 2.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3ed64-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3ed64-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ed64-120">**Interface IWMSyncReader**</span><span class="sxs-lookup"><span data-stu-id="3ed64-120">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="3ed64-121">**Lendo arquivos com o leitor síncrono**</span><span class="sxs-lookup"><span data-stu-id="3ed64-121">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




