---
description: A API XAPO fornece a interface IXAPO e a classe CXAPOBase para a criação de novos tipos XAPO.
ms.assetid: 34f5c3d5-ee40-e304-7c97-d30c17621d26
title: 'Como: Criar um XAPO'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 549739462a0e76cbb437f0aa1403b099f72f5224
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172048"
---
# <a name="how-to-create-an-xapo"></a><span data-ttu-id="a10c5-103">Como: Criar um XAPO</span><span class="sxs-lookup"><span data-stu-id="a10c5-103">How to: Create an XAPO</span></span>

<span data-ttu-id="a10c5-104">A API XAPO fornece a interface [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) e a classe [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) para a criação de novos tipos XAPO.</span><span class="sxs-lookup"><span data-stu-id="a10c5-104">The XAPO API provides the [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) interface and the [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) class for building new XAPO types.</span></span> <span data-ttu-id="a10c5-105">A interface **IXAPO** contém todos os métodos que precisam ser implementados para criar um novo XAPO.</span><span class="sxs-lookup"><span data-stu-id="a10c5-105">The **IXAPO** interface contains all of the methods that need to be implemented to create a new XAPO.</span></span> <span data-ttu-id="a10c5-106">A classe **CXAPOBase** fornece uma implementação básica da interface **IXAPO** .</span><span class="sxs-lookup"><span data-stu-id="a10c5-106">The **CXAPOBase** class provides a basic implementation of the **IXAPO** interface.</span></span> <span data-ttu-id="a10c5-107">**CXAPOBase** implementa todos os métodos de interface **IXAPO** , exceto o método [**IXAPO::P modelos**](/windows/win32/api/xapo/nf-xapo-ixapo-process) , que é exclusivo para cada XAPO.</span><span class="sxs-lookup"><span data-stu-id="a10c5-107">**CXAPOBase** implements all of the **IXAPO** interface methods except the [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) method, which is unique to each XAPO.</span></span>

## <a name="to-create-a-new-static-xapo"></a><span data-ttu-id="a10c5-108">Para criar um novo XAPO estático</span><span class="sxs-lookup"><span data-stu-id="a10c5-108">To create a new static XAPO</span></span>

1.  <span data-ttu-id="a10c5-109">Derive uma nova classe XAPO da classe base [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) .</span><span class="sxs-lookup"><span data-stu-id="a10c5-109">Derive a new XAPO class from the [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) base class.</span></span>

    > [!Note]  
    > <span data-ttu-id="a10c5-110">XAPOs implemente a interface **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="a10c5-110">XAPOs implement the **IUnknown** interface.</span></span> <span data-ttu-id="a10c5-111">As interfaces [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) e [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) incluem os três métodos **IUnknown** : **QueryInterface**, **AddRef** e **Release**.</span><span class="sxs-lookup"><span data-stu-id="a10c5-111">The [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) and [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) interfaces include the three **IUnknown** methods: **QueryInterface**, **AddRef**, and **Release**.</span></span> <span data-ttu-id="a10c5-112">O [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) fornece implementações de todos os três métodos **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="a10c5-112">[**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) provides implementations of all three of the **IUnknown** methods.</span></span> <span data-ttu-id="a10c5-113">Uma nova instância de **CXAPOBase** terá uma contagem de referência de 1.</span><span class="sxs-lookup"><span data-stu-id="a10c5-113">A new instance of **CXAPOBase** will have a reference count of 1.</span></span> <span data-ttu-id="a10c5-114">Ele será destruído quando sua contagem de referência se tornar 0.</span><span class="sxs-lookup"><span data-stu-id="a10c5-114">It will be destroyed when its reference count becomes 0.</span></span> <span data-ttu-id="a10c5-115">Para permitir que o XAudio2 destrua uma instância de um XAPO quando ele não for mais necessário, chame **IUnknown:: Release** no XAPO depois que ele for adicionado a uma cadeia de efeito XAudio2.</span><span class="sxs-lookup"><span data-stu-id="a10c5-115">To allow XAudio2 to destroy an instance of an XAPO when it is no longer needed, call **IUnknown::Release** on the XAPO after it is added to an XAudio2 effect chain.</span></span> <span data-ttu-id="a10c5-116">Consulte [como: usar um XAPO no XAudio2](how-to--use-an-xapo-in-xaudio2.md) para obter mais informações sobre como usar um XAPO com XAudio2.</span><span class="sxs-lookup"><span data-stu-id="a10c5-116">See [How to: Use an XAPO in XAudio2](how-to--use-an-xapo-in-xaudio2.md) for more information about using an XAPO with XAudio2.</span></span>

     

2.  <span data-ttu-id="a10c5-117">Substitua a implementação da classe [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) do método [**IXAPO:: LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) .</span><span class="sxs-lookup"><span data-stu-id="a10c5-117">Override the [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) class implementation of the [**IXAPO::LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) method.</span></span>

    <span data-ttu-id="a10c5-118">A substituição de [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) permite que informações sobre o formato dos dados de áudio sejam armazenados para uso em [**IXAPO::P modelos**](/windows/win32/api/xapo/nf-xapo-ixapo-process).</span><span class="sxs-lookup"><span data-stu-id="a10c5-118">Overriding [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) allows information about the format of audio data to be stored for use in [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process).</span></span>

3.  <span data-ttu-id="a10c5-119">Implemente o método [**IXAPO::P modelos**](/windows/win32/api/xapo/nf-xapo-ixapo-process) .</span><span class="sxs-lookup"><span data-stu-id="a10c5-119">Implement the [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) method.</span></span>

    <span data-ttu-id="a10c5-120">XAudio2 chama o método [**IXAPO::P modelos**](/windows/win32/api/xapo/nf-xapo-ixapo-process) sempre que um XAPO precisa processar dados de áudio.</span><span class="sxs-lookup"><span data-stu-id="a10c5-120">XAudio2 calls the [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) method whenever an XAPO needs to process audio data.</span></span> <span data-ttu-id="a10c5-121">O **processo** contém a massa do código para um XAPO.</span><span class="sxs-lookup"><span data-stu-id="a10c5-121">**Process** contains the bulk of the code for an XAPO.</span></span>

## <a name="implementing-the-process-method"></a><span data-ttu-id="a10c5-122">Implementando o método Process</span><span class="sxs-lookup"><span data-stu-id="a10c5-122">Implementing the Process Method</span></span>

<span data-ttu-id="a10c5-123">O método [**IXAPO::P modelos**](/windows/win32/api/xapo/nf-xapo-ixapo-process) aceita buffers de fluxo para dados de áudio de entrada e saída.</span><span class="sxs-lookup"><span data-stu-id="a10c5-123">The [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) method accepts stream buffers for input and output audio data.</span></span> <span data-ttu-id="a10c5-124">Um XAPO típico esperará um buffer de fluxo de entrada e um buffer de fluxo de saída.</span><span class="sxs-lookup"><span data-stu-id="a10c5-124">A typical XAPO will expect one input stream buffer and one output stream buffer.</span></span> <span data-ttu-id="a10c5-125">Você deve basear o processamento de dados do buffer de fluxo de entrada no formato especificado na função [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) e quaisquer sinalizadores passados para a função **process** com o buffer de fluxo de entrada.</span><span class="sxs-lookup"><span data-stu-id="a10c5-125">You should base the processing of data from the input stream buffer on the format specified in the [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) function and any flags passed to the **Process** function with the input stream buffer.</span></span> <span data-ttu-id="a10c5-126">Copie os dados de buffer de fluxo de entrada processados para o buffer de fluxo de saída.</span><span class="sxs-lookup"><span data-stu-id="a10c5-126">Copy the processed input stream buffer data to the output stream buffer.</span></span> <span data-ttu-id="a10c5-127">Defina o parâmetro BufferFlags do buffer de fluxo de saída como o [**\_ buffer XAPO \_ válido**](/windows/desktop/api/xapo/ne-xapo-xapo_buffer_flags) ou o **buffer XAPO é \_ \_ silencioso**.</span><span class="sxs-lookup"><span data-stu-id="a10c5-127">Set the output stream buffer's BufferFlags parameter as either [**XAPO\_BUFFER\_VALID**](/windows/desktop/api/xapo/ne-xapo-xapo_buffer_flags) or **XAPO\_BUFFER\_SILENT**.</span></span>

<span data-ttu-id="a10c5-128">O exemplo a seguir demonstra uma implementação de [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) e de [**processo**](/windows/win32/api/xapo/nf-xapo-ixapo-process) que simplesmente copia dados de um buffer de entrada para um buffer de saída.</span><span class="sxs-lookup"><span data-stu-id="a10c5-128">The following example demonstrates a [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) and [**Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) implementation that simply copies data from an input buffer to an output buffer.</span></span> <span data-ttu-id="a10c5-129">No entanto, não haverá processamento se o buffer de entrada estiver marcado com o [**\_ buffer XAPO \_ silencioso**](/windows/desktop/api/xapo/ne-xapo-xapo_buffer_flags).</span><span class="sxs-lookup"><span data-stu-id="a10c5-129">However, there is no processing if the input buffer is marked with [**XAPO\_BUFFER\_SILENT**](/windows/desktop/api/xapo/ne-xapo-xapo_buffer_flags).</span></span>


```
STDMETHOD(LockForProcess) (UINT32 InputLockedParameterCount,
          const XAPO_LOCKFORPROCESS_BUFFER_PARAMETERS* pInputLockedParameters,
          UINT32 OutputLockedParameterCount,
          const XAPO_LOCKFORPROCESS_BUFFER_PARAMETERS* pOutputLockedParameters)
{
    assert(!IsLocked());
    assert(InputLockedParameterCount == 1);
    assert(OutputLockedParameterCount == 1);
    assert(pInputLockedParameters != NULL);
    assert(pOutputLockedParameters != NULL);
    assert(pInputLockedParameters[0].pFormat != NULL);
    assert(pOutputLockedParameters[0].pFormat != NULL);


    m_uChannels = pInputLockedParameters[0].pFormat->nChannels;
    m_uBytesPerSample = (pInputLockedParameters[0].pFormat->wBitsPerSample >> 3);

    return CXAPOBase::LockForProcess(
        InputLockedParameterCount,
        pInputLockedParameters,
        OutputLockedParameterCount,
        pOutputLockedParameters);
}
STDMETHOD_(void, Process)(UINT32 InputProcessParameterCount,
           const XAPO_PROCESS_BUFFER_PARAMETERS* pInputProcessParameters,
           UINT32 OutputProcessParameterCount,
           XAPO_PROCESS_BUFFER_PARAMETERS* pOutputProcessParameters,
           BOOL IsEnabled)
{
    assert(IsLocked());
    assert(InputProcessParameterCount == 1);
    assert(OutputProcessParameterCount == 1);
    assert(NULL != pInputProcessParameters);
    assert(NULL != pOutputProcessParameters);


    XAPO_BUFFER_FLAGS inFlags = pInputProcessParameters[0].BufferFlags;
    XAPO_BUFFER_FLAGS outFlags = pOutputProcessParameters[0].BufferFlags;

    // assert buffer flags are legitimate
    assert(inFlags == XAPO_BUFFER_VALID || inFlags == XAPO_BUFFER_SILENT);
    assert(outFlags == XAPO_BUFFER_VALID || outFlags == XAPO_BUFFER_SILENT);

    // check input APO_BUFFER_FLAGS
    switch (inFlags)
    {
    case XAPO_BUFFER_VALID:
        {
            void* pvSrc = pInputProcessParameters[0].pBuffer;
            assert(pvSrc != NULL);

            void* pvDst = pOutputProcessParameters[0].pBuffer;
            assert(pvDst != NULL);

            memcpy(pvDst,pvSrc,pInputProcessParameters[0].ValidFrameCount * m_uChannels * m_uBytesPerSample);
            break;
        }

    case XAPO_BUFFER_SILENT:
        {
            // All that needs to be done for this case is setting the
            // output buffer flag to XAPO_BUFFER_SILENT which is done below.
            break;
        }

    }

    // set destination valid frame count, and buffer flags
    pOutputProcessParameters[0].ValidFrameCount = pInputProcessParameters[0].ValidFrameCount; // set destination frame count same as source
    pOutputProcessParameters[0].BufferFlags     = pInputProcessParameters[0].BufferFlags;     // set destination buffer flags same as source

}
```



<span data-ttu-id="a10c5-130">Ao escrever um método de [**processo**](/windows/win32/api/xapo/nf-xapo-ixapo-process) , é importante observar que os dados de áudio XAudio2 são intercalados.</span><span class="sxs-lookup"><span data-stu-id="a10c5-130">When writing a [**Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) method, it is important to note XAudio2 audio data is interleaved.</span></span> <span data-ttu-id="a10c5-131">Isso significa que os dados de cada canal são adjacentes a um número de exemplo específico.</span><span class="sxs-lookup"><span data-stu-id="a10c5-131">This means data from each channel is adjacent for a particular sample number.</span></span> <span data-ttu-id="a10c5-132">Por exemplo, se houver uma onda de 4 canais tocando em uma voz de origem XAudio2, os dados de áudio serão uma amostra do canal 0, uma amostra do canal 1, uma amostra do canal 2, uma amostra do canal 3 e, em seguida, a próxima amostra dos canais 0, 1, 2, 3 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="a10c5-132">For example, if there is a 4-channel wave playing into an XAudio2 source voice, the audio data is a sample of channel 0, a sample of channel 1, a sample of channel 2, a sample of channel 3, and then the next sample of channels 0, 1, 2, 3, and so on.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a10c5-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a10c5-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a10c5-134">Efeitos de áudio</span><span class="sxs-lookup"><span data-stu-id="a10c5-134">Audio Effects</span></span>](audio-effects.md)
</dt> <dt>

[<span data-ttu-id="a10c5-135">Visão geral do XAPO</span><span class="sxs-lookup"><span data-stu-id="a10c5-135">XAPO Overview</span></span>](xapo-overview.md)
</dt> </dl>

 

 
