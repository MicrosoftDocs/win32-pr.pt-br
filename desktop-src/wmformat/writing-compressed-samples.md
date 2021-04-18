---
title: Gravando amostras compactadas
description: Gravando amostras compactadas
ms.assetid: f85ca719-1b9d-404f-b2b1-c9e3524e4bc6
keywords:
- ASF (Advanced Systems Format), gravando amostras compactadas
- ASF (formato de sistemas avançados), gravando amostras compactadas
- ASF (Advanced Systems Format), passando amostras compactadas
- ASF (formato de sistemas avançados), passando amostras compactadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0c43fed30aa89e83c157479257e78fbab4acd98
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104453848"
---
# <a name="writing-compressed-samples"></a><span data-ttu-id="b4426-107">Gravando amostras compactadas</span><span class="sxs-lookup"><span data-stu-id="b4426-107">Writing Compressed Samples</span></span>

<span data-ttu-id="b4426-108">Para alguns fluxos de áudio ou vídeo, talvez você queira passar exemplos que já foram compactados em vez de passar dados brutos.</span><span class="sxs-lookup"><span data-stu-id="b4426-108">For some audio or video streams, you may want to pass samples that are already compressed instead of passing raw data.</span></span> <span data-ttu-id="b4426-109">Esse recurso é usado para copiar um fluxo existente ou para escrever amostras compactadas com um codec de terceiros.</span><span class="sxs-lookup"><span data-stu-id="b4426-109">This feature is used to copy an existing stream or to write samples compressed with a third-party codec.</span></span> <span data-ttu-id="b4426-110">O processo de gravar um exemplo compactado é idêntico a escrever um exemplo descompactado, exceto pelo fato de que você usa [**IWMWriterAdvanced:: WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) em vez de [**IWMWriter:: WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample).</span><span class="sxs-lookup"><span data-stu-id="b4426-110">The process of writing a compressed sample is identical to writing an uncompressed sample, except that you use [**IWMWriterAdvanced::WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) instead of [**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample).</span></span> <span data-ttu-id="b4426-111">Para obter mais informações sobre como escrever amostras descompactadas, consulte [para escrever exemplos](to-write-samples.md).</span><span class="sxs-lookup"><span data-stu-id="b4426-111">For more information about writing uncompressed samples, see [To Write Samples](to-write-samples.md).</span></span>

<span data-ttu-id="b4426-112">Quando você escreve amostras compactadas, para perfis de CBR, o gravador descartará alguns exemplos, se necessário, para manter o conteúdo dentro dos valores de janela de buffer e taxa de bits especificados.</span><span class="sxs-lookup"><span data-stu-id="b4426-112">When you write compressed samples, for CBR profiles, the writer will drop some samples, if necessary, to keep the content within the specified bit rate and buffer window values.</span></span> <span data-ttu-id="b4426-113">Para a VBR, o gravador não descartará amostras, mas não há como garantir que os valores de taxa de bits e de janela de buffer estejam corretos.</span><span class="sxs-lookup"><span data-stu-id="b4426-113">For VBR, the writer will not drop samples, but there is no way to be sure that the bit rate and buffer window values will be correct.</span></span>

<span data-ttu-id="b4426-114">Se você estiver copiando um fluxo de um arquivo para outro, sempre deverá copiar o objeto de configuração de fluxo do perfil do arquivo original para o perfil do novo arquivo.</span><span class="sxs-lookup"><span data-stu-id="b4426-114">If you are copying a stream from one file to another, you should always copy the stream configuration object from the profile of the original file to the profile of the new file.</span></span> <span data-ttu-id="b4426-115">Isso garante que você tenha a taxa de bits e as informações de janela de buffer corretas.</span><span class="sxs-lookup"><span data-stu-id="b4426-115">This ensures that you have the correct bit rate and buffer window information.</span></span> <span data-ttu-id="b4426-116">Se você copiar um fluxo compactado para um fluxo que tenha uma janela de buffer inferior definida, os exemplos serão removidos durante a gravação do arquivo.</span><span class="sxs-lookup"><span data-stu-id="b4426-116">If you copy a compressed stream to a stream that has a lower buffer window set, samples will be dropped during file writing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b4426-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b4426-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4426-118">**Gravando arquivos ASF**</span><span class="sxs-lookup"><span data-stu-id="b4426-118">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




