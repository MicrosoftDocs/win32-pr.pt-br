---
title: Objeto de coletor de arquivo do gravador
description: Objeto de coletor de arquivo do gravador
ms.assetid: 93f44579-fb2d-498e-a271-5bc91d6f0321
keywords:
- SDK do Windows Media Format, objetos do coletor de arquivo do Writer
- ASF (Advanced Systems Format), objetos de coletor de arquivo do Writer
- ASF (formato de sistemas avançados), objetos do coletor de arquivo do gravador
- objetos, objetos do coletor de arquivo do gravador
- objetos do coletor de arquivo do gravador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82009e5be74cfc23e687001a2a81cd4546812af9
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104007246"
---
# <a name="writer-file-sink-object"></a><span data-ttu-id="0b586-108">Objeto de coletor de arquivo do gravador</span><span class="sxs-lookup"><span data-stu-id="0b586-108">Writer File Sink Object</span></span>

<span data-ttu-id="0b586-109">O objeto de coletor de arquivo do gravador é usado ao gravar a saída do Windows Media em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="0b586-109">The writer file sink object is used when writing Windows Media output to a file.</span></span>

<span data-ttu-id="0b586-110">O objeto de coletor de arquivo do gravador é criado pela função [**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink), que define um ponteiro para uma interface **IWMWriterFileSink** .</span><span class="sxs-lookup"><span data-stu-id="0b586-110">The writer file sink object is created by the function [**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink), which sets a pointer to an **IWMWriterFileSink** interface.</span></span> <span data-ttu-id="0b586-111">As outras interfaces do objeto de coletor de arquivo do gravador podem ser obtidas chamando o método **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="0b586-111">The other interfaces of the writer file sink object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="0b586-112">As interfaces a seguir têm suporte do objeto de coletor de arquivo do gravador.</span><span class="sxs-lookup"><span data-stu-id="0b586-112">The following interfaces are supported by the writer file sink object.</span></span>



| <span data-ttu-id="0b586-113">Interface</span><span class="sxs-lookup"><span data-stu-id="0b586-113">Interface</span></span>                                          | <span data-ttu-id="0b586-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="0b586-114">Description</span></span>                                                                                                                     |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0b586-115">**IWMRegisterCallback**</span><span class="sxs-lookup"><span data-stu-id="0b586-115">**IWMRegisterCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) | <span data-ttu-id="0b586-116">Permite que o aplicativo obtenha mensagens de status do objeto.</span><span class="sxs-lookup"><span data-stu-id="0b586-116">Enables the application to get status messages from the object.</span></span>                                                                 |
| [<span data-ttu-id="0b586-117">**IWMWriterFileSink**</span><span class="sxs-lookup"><span data-stu-id="0b586-117">**IWMWriterFileSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink)     | <span data-ttu-id="0b586-118">Abre um arquivo no qual o objeto gravador pode gravar dados.</span><span class="sxs-lookup"><span data-stu-id="0b586-118">Opens a file to which the writer object can write data.</span></span>                                                                         |
| [<span data-ttu-id="0b586-119">**IWMWriterFileSink2**</span><span class="sxs-lookup"><span data-stu-id="0b586-119">**IWMWriterFileSink2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink2)   | <span data-ttu-id="0b586-120">Fornece gerenciamento estendido de um objeto de coletor de arquivos.</span><span class="sxs-lookup"><span data-stu-id="0b586-120">Provides extended management of a file sink object.</span></span> <span data-ttu-id="0b586-121">Herda todos os métodos de **IWMWriterFileSink**.</span><span class="sxs-lookup"><span data-stu-id="0b586-121">Inherits all of the methods of **IWMWriterFileSink**.</span></span>                       |
| [<span data-ttu-id="0b586-122">**IWMWriterFileSink3**</span><span class="sxs-lookup"><span data-stu-id="0b586-122">**IWMWriterFileSink3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3)   | <span data-ttu-id="0b586-123">Fornece opções adicionais para gravar arquivos.</span><span class="sxs-lookup"><span data-stu-id="0b586-123">Provides additional options for writing files.</span></span> <span data-ttu-id="0b586-124">Herda todos os métodos de **IWMWriterFileSink** e **IWMWriterFileSink2**.</span><span class="sxs-lookup"><span data-stu-id="0b586-124">Inherits all of the methods of **IWMWriterFileSink** and **IWMWriterFileSink2**.</span></span> |
| [<span data-ttu-id="0b586-125">**IWMWriterSink**</span><span class="sxs-lookup"><span data-stu-id="0b586-125">**IWMWriterSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)             | <span data-ttu-id="0b586-126">Aloca memória, determina se o coletor está operando em tempo real e manipula várias funções de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="0b586-126">Allocates memory, determines whether the sink is operating in real time, and handles several callback functions.</span></span>                |



 

<span data-ttu-id="0b586-127">A interface de retorno de chamada a seguir deve ser implementada pelo aplicativo para acompanhar o progresso de um objeto de coletor de arquivo do gravador.</span><span class="sxs-lookup"><span data-stu-id="0b586-127">The following callback interface should be implemented by the application to track the progress of a writer file sink object.</span></span>



| <span data-ttu-id="0b586-128">Interface</span><span class="sxs-lookup"><span data-stu-id="0b586-128">Interface</span></span>                                      | <span data-ttu-id="0b586-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="0b586-129">Description</span></span>                                                                    |
|------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="0b586-130">**IWMStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="0b586-130">**IWMStatusCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | <span data-ttu-id="0b586-131">Necessário quando as informações de status devem ser comunicadas ao aplicativo host.</span><span class="sxs-lookup"><span data-stu-id="0b586-131">Required when status information must be communicated to the host application.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="0b586-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0b586-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b586-133">**Objetos**</span><span class="sxs-lookup"><span data-stu-id="0b586-133">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="0b586-134">**Trabalhando com coletores de gravador**</span><span class="sxs-lookup"><span data-stu-id="0b586-134">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 




