---
title: Para forçar a inserção de Key-Frame
description: Para forçar a inserção de Key-Frame
ms.assetid: 456482da-aaa2-41f8-93f7-c0fa5abe7dd2
keywords:
- ASF (Advanced Systems Format), forçando inserções de quadros-chave
- ASF (formato de sistemas avançados), forçando inserções de quadros-chave
- ASF (Advanced Systems Format), inserções de quadro-chave
- ASF (formato de sistemas avançados), inserções de quadros-chave
- quadros chave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23006eef1e51d8bc63f2d55cac22e09a2052d83e
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104453883"
---
# <a name="to-force-key-frame-insertion"></a><span data-ttu-id="90bf2-108">Para forçar a inserção de Key-Frame</span><span class="sxs-lookup"><span data-stu-id="90bf2-108">To Force Key-Frame Insertion</span></span>

<span data-ttu-id="90bf2-109">O codec Windows Media Video 9 dá suporte à inserção forçada de quadros-chave.</span><span class="sxs-lookup"><span data-stu-id="90bf2-109">The Windows Media Video 9 codec supports forced key-frame insertion.</span></span> <span data-ttu-id="90bf2-110">Ao passar um exemplo para o gravador, você pode especificar que ele deve ser codificado como um [*quadro-chave*](wmformat-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="90bf2-110">When you pass a sample to the writer, you can specify that it must be encoded as a [*key frame*](wmformat-glossary.md).</span></span>

<span data-ttu-id="90bf2-111">Para forçar a inserção de quadro-chave para um exemplo, execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="90bf2-111">To force key-frame insertion for a sample, perform the following steps.</span></span>

1.  <span data-ttu-id="90bf2-112">Aloque um buffer para manter o exemplo e recupere um ponteiro para a interface [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) que contém o buffer chamando [**IWMWriter:: AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample).</span><span class="sxs-lookup"><span data-stu-id="90bf2-112">Allocate a buffer to hold the sample, and retrieve a pointer to the [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) interface containing the buffer by calling [**IWMWriter::AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample).</span></span>
2.  <span data-ttu-id="90bf2-113">Recupere o local e o tamanho do buffer criado na etapa 1 chamando [**INSSBuffer:: GetBufferAndLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbufferandlength).</span><span class="sxs-lookup"><span data-stu-id="90bf2-113">Retrieve the location and size of the buffer created in step 1 by calling [**INSSBuffer::GetBufferAndLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbufferandlength).</span></span>
3.  <span data-ttu-id="90bf2-114">Copie os dados de exemplo para o local do buffer, certificando-se de que o exemplo passado caiba no buffer alocado.</span><span class="sxs-lookup"><span data-stu-id="90bf2-114">Copy your sample data to the buffer location, making sure that the sample passed will fit in the allocated buffer.</span></span> <span data-ttu-id="90bf2-115">Dependendo da origem de seus exemplos, você pode usar uma variedade de funções para copiar os dados.</span><span class="sxs-lookup"><span data-stu-id="90bf2-115">Depending upon the source of your samples, you can use a variety of functions to copy the data.</span></span> <span data-ttu-id="90bf2-116">Por exemplo, se você estiver copiando um fluxo de um arquivo AVI, poderá usar a função AVI, **AVIStreamRead**.</span><span class="sxs-lookup"><span data-stu-id="90bf2-116">For example, if you are copying a stream from an AVI file, you can use the AVI function, **AVIStreamRead**.</span></span>
4.  <span data-ttu-id="90bf2-117">Atualize a quantidade de dados usados no buffer para refletir o tamanho real do exemplo chamando [**INSSBuffer:: SetLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-setlength).</span><span class="sxs-lookup"><span data-stu-id="90bf2-117">Update the amount of data used in the buffer to reflect the actual size of the sample by calling [**INSSBuffer::SetLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-setlength).</span></span>
5.  <span data-ttu-id="90bf2-118">Obtenha um ponteiro para a interface [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) chamando **INSSBuffer:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="90bf2-118">Obtain a pointer to the [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) interface by calling **INSSBuffer::QueryInterface**.</span></span>
6.  <span data-ttu-id="90bf2-119">Defina o exemplo como um quadro-chave forçado chamando o método [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) para definir a \_ Propriedade OutputCleanPoint do WM SampleExtensionGUID \_ .</span><span class="sxs-lookup"><span data-stu-id="90bf2-119">Set the sample as a forced key frame by calling the [**INSSBuffer3::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) method to set the WM\_SampleExtensionGUID\_OutputCleanPoint property.</span></span> <span data-ttu-id="90bf2-120">Esta propriedade é um valor booliano; Defina-o como **true**.</span><span class="sxs-lookup"><span data-stu-id="90bf2-120">This property is a Boolean value; set it to **TRUE**.</span></span>
7.  <span data-ttu-id="90bf2-121">Passe a interface de buffer para o gravador junto com o número de entrada e o tempo de amostra usando o método [**IWMWriter:: WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) .</span><span class="sxs-lookup"><span data-stu-id="90bf2-121">Pass the buffer interface to the writer along with the input number and sample time by using the [**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="90bf2-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="90bf2-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90bf2-123">**IWMWriter::WriteSample**</span><span class="sxs-lookup"><span data-stu-id="90bf2-123">**IWMWriter::WriteSample**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample)
</dt> <dt>

[<span data-ttu-id="90bf2-124">**Para escrever exemplos**</span><span class="sxs-lookup"><span data-stu-id="90bf2-124">**To Write Samples**</span></span>](to-write-samples.md)
</dt> <dt>

[<span data-ttu-id="90bf2-125">**Codificação de taxa de bits variável (VBR)**</span><span class="sxs-lookup"><span data-stu-id="90bf2-125">**Variable Bit Rate (VBR) Encoding**</span></span>](variable-bit-rate--vbr--encoding.md)
</dt> <dt>

[<span data-ttu-id="90bf2-126">**Gravando arquivos ASF**</span><span class="sxs-lookup"><span data-stu-id="90bf2-126">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




