---
description: Atributos do gravador de coletor
ms.assetid: f27b9beb-f35f-400e-a337-50d9de21e91e
title: Atributos do gravador de coletor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e23dbca06c3ff1a4ac80b8e68413fdd0816d71a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091031"
---
# <a name="sink-writer-attributes"></a><span data-ttu-id="97d5a-103">Atributos do gravador de coletor</span><span class="sxs-lookup"><span data-stu-id="97d5a-103">Sink Writer Attributes</span></span>

<span data-ttu-id="97d5a-104">Os atributos a seguir podem ser usados para inicializar o gravador do coletor.</span><span class="sxs-lookup"><span data-stu-id="97d5a-104">The following attributes can be used to initialize the sink writer.</span></span>



| <span data-ttu-id="97d5a-105">Atributo</span><span class="sxs-lookup"><span data-stu-id="97d5a-105">Attribute</span></span>                                                                                  | <span data-ttu-id="97d5a-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="97d5a-106">Description</span></span>                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="97d5a-107">\_baixa \_ LATÊNCIA do MF</span><span class="sxs-lookup"><span data-stu-id="97d5a-107">MF\_LOW\_LATENCY</span></span>](mf-low-latency.md)                                                     | <span data-ttu-id="97d5a-108">Habilita o processamento de baixa latência.</span><span class="sxs-lookup"><span data-stu-id="97d5a-108">Enables low-latency processing.</span></span>                                                                                                                                                                                                    |
| [<span data-ttu-id="97d5a-109">\_conversores do MF ReadWrite \_ Disable \_</span><span class="sxs-lookup"><span data-stu-id="97d5a-109">MF\_READWRITE\_DISABLE\_CONVERTERS</span></span>](mf-readwrite-disable-converters.md)                  | <span data-ttu-id="97d5a-110">Habilita ou desabilita conversões de formato pelo gravador de coletor.</span><span class="sxs-lookup"><span data-stu-id="97d5a-110">Enables or disables format conversions by the sink writer.</span></span>                                                                                                                                                                         |
| [<span data-ttu-id="97d5a-111">MF \_ ReadWrite \_ habilitar \_ \_ transformações de hardware</span><span class="sxs-lookup"><span data-stu-id="97d5a-111">MF\_READWRITE\_ENABLE\_HARDWARE\_TRANSFORMS</span></span>](mf-readwrite-enable-hardware-transforms.md) | <span data-ttu-id="97d5a-112">Permite que o gravador de coletor use transformações de Media Foundation baseadas em hardware (MFTs).</span><span class="sxs-lookup"><span data-stu-id="97d5a-112">Enables the sink writer to use hardware-based Media Foundation transforms (MFTs).</span></span>                                                                                                                                                  |
| [<span data-ttu-id="97d5a-113">\_retorno de \_ \_ chamada assíncrono do gravador de coletor MF \_</span><span class="sxs-lookup"><span data-stu-id="97d5a-113">MF\_SINK\_WRITER\_ASYNC\_CALLBACK</span></span>](mf-sink-writer-async-callback.md)                     | <span data-ttu-id="97d5a-114">Contém um ponteiro para a interface de retorno de chamada do aplicativo para o gravador do coletor.</span><span class="sxs-lookup"><span data-stu-id="97d5a-114">Contains a pointer to the application's callback interface for the sink writer.</span></span>                                                                                                                                                    |
| [<span data-ttu-id="97d5a-115">\_limitação de \_ \_ desabilitação do gravador de coletor MF \_</span><span class="sxs-lookup"><span data-stu-id="97d5a-115">MF\_SINK\_WRITER\_DISABLE\_THROTTLING</span></span>](mf-sink-writer-disable-throttling.md)             | <span data-ttu-id="97d5a-116">Especifica se o gravador do coletor limita a taxa de dados de entrada.</span><span class="sxs-lookup"><span data-stu-id="97d5a-116">Specifies whether the sink writer limits the rate of incoming data.</span></span>                                                                                                                                                                |
| [<span data-ttu-id="97d5a-117">\_contêinertype de transcodificação MF \_</span><span class="sxs-lookup"><span data-stu-id="97d5a-117">MF\_TRANSCODE\_CONTAINERTYPE</span></span>](mf-transcode-containertype.md)                             | <span data-ttu-id="97d5a-118">Especifica o tipo de contêiner do arquivo de saída.</span><span class="sxs-lookup"><span data-stu-id="97d5a-118">Specifies the container type of the output file.</span></span>                                                                                                                                                                                   |
| [<span data-ttu-id="97d5a-119">\_Atributo de \_ desbloqueio de FIELDOFUSE MFT \_</span><span class="sxs-lookup"><span data-stu-id="97d5a-119">MFT\_FIELDOFUSE\_UNLOCK\_Attribute</span></span>](mft-fieldofuse-unlock-attribute.md)                  | <span data-ttu-id="97d5a-120">Contém um ponteiro [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) , que é usado para desbloquear um MFT com restrições de campo de uso.</span><span class="sxs-lookup"><span data-stu-id="97d5a-120">Contains an [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) pointer, which is used to unlock an MFT with field-of-use restrictions.</span></span> <span data-ttu-id="97d5a-121">Para obter mais informações, consulte [campo de restrições de uso](field-of-use-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="97d5a-121">For more information, see [Field of Use Restrictions](field-of-use-restrictions.md).</span></span> |
| [<span data-ttu-id="97d5a-122">\_Gerenciador de \_ D3D do gravador de coletor MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="97d5a-122">MF\_SINK\_WRITER\_D3D\_MANAGER</span></span>](mf-sink-writer-d3d-manager.md)                           | <span data-ttu-id="97d5a-123">Use esse atributo para fornecer um dispositivo Direct3D para qualquer codificador de vídeo ou coletores de mídia carregados pelo gravador de coletor.</span><span class="sxs-lookup"><span data-stu-id="97d5a-123">Use this attribute to provide a Direct3D device for any video encoders or media sinks loaded by the sink writer.</span></span>                                                                                                                   |



 

<span data-ttu-id="97d5a-124">Use esses atributos com os seguintes métodos e funções:</span><span class="sxs-lookup"><span data-stu-id="97d5a-124">Use these attributes with the following methods and functions:</span></span>

-   [<span data-ttu-id="97d5a-125">**IMFReadWriteClassFactory::CreateInstanceFromObject**</span><span class="sxs-lookup"><span data-stu-id="97d5a-125">**IMFReadWriteClassFactory::CreateInstanceFromObject**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromobject)
-   [<span data-ttu-id="97d5a-126">**IMFReadWriteClassFactory::CreateInstanceFromURL**</span><span class="sxs-lookup"><span data-stu-id="97d5a-126">**IMFReadWriteClassFactory::CreateInstanceFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromurl)
-   [<span data-ttu-id="97d5a-127">**MFCreateSinkWriterFromMediaSink**</span><span class="sxs-lookup"><span data-stu-id="97d5a-127">**MFCreateSinkWriterFromMediaSink**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [<span data-ttu-id="97d5a-128">**MFCreateSinkWriterFromURL**</span><span class="sxs-lookup"><span data-stu-id="97d5a-128">**MFCreateSinkWriterFromURL**</span></span>](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

<span data-ttu-id="97d5a-129">Para usar qualquer um desses atributos, primeiro chame [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) para criar um novo repositório de atributos.</span><span class="sxs-lookup"><span data-stu-id="97d5a-129">To use any of these attributes, first call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create a new attribute store.</span></span> <span data-ttu-id="97d5a-130">Em seguida, use a interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) para definir os atributos desejados no repositório de atributos.</span><span class="sxs-lookup"><span data-stu-id="97d5a-130">Then use the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface to set the desired attributes on the attribute store.</span></span> <span data-ttu-id="97d5a-131">Passe o ponteiro **IMFAttributes** para o parâmetro *pAttributes* de qualquer um dos métodos ou funções listados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="97d5a-131">Pass the **IMFAttributes** pointer to the *pAttributes* parameter of any of the methods or functions listed previously.</span></span>

## <a name="related-topics"></a><span data-ttu-id="97d5a-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="97d5a-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97d5a-133">**IMFSinkWriter**</span><span class="sxs-lookup"><span data-stu-id="97d5a-133">**IMFSinkWriter**</span></span>](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter)
</dt> <dt>

[<span data-ttu-id="97d5a-134">Atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="97d5a-134">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 



