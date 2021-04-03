---
title: Enumerando coletores
description: Enumerando coletores
ms.assetid: 1b635cd8-6bdd-4592-bfb5-bcdcf7818e18
keywords:
- ASF (Advanced Systems Format), enumerando coletores
- ASF (formato de sistemas avançados), enumerando coletores
- ASF (Advanced Systems Format), coletores
- ASF (formato de sistemas avançados), coletores
- coletores, enumerando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff35124a8c88108082544b270aa4d9813ff67ea9
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/21/2020
ms.locfileid: "103640281"
---
# <a name="enumerating-sinks"></a><span data-ttu-id="0c8e5-108">Enumerando coletores</span><span class="sxs-lookup"><span data-stu-id="0c8e5-108">Enumerating Sinks</span></span>

<span data-ttu-id="0c8e5-109">O gravador pode ter muitos coletores associados a ele.</span><span class="sxs-lookup"><span data-stu-id="0c8e5-109">The writer can have many sinks associated with it.</span></span> <span data-ttu-id="0c8e5-110">Você pode enumerar os coletores que foram adicionados ao gravador usando [**IWMWriterAdvanced:: GetSinkCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsinkcount) e [**IWMWriterAdvanced:: getsink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsink).</span><span class="sxs-lookup"><span data-stu-id="0c8e5-110">You can enumerate the sinks that have been added to the writer by using [**IWMWriterAdvanced::GetSinkCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsinkcount) and [**IWMWriterAdvanced::GetSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getsink).</span></span>

<span data-ttu-id="0c8e5-111">O código de exemplo na [obtenção de mensagens de erro de um coletor demonstra a enumeração do](getting-error-messages-from-a-sink.md) coletor.</span><span class="sxs-lookup"><span data-stu-id="0c8e5-111">The example code in the [Getting Error Messages from a Sink](getting-error-messages-from-a-sink.md) demonstrates sink enumeration.</span></span>

> [!Note]  
> <span data-ttu-id="0c8e5-112">Ao enumerar coletores, o coletor de arquivo padrão criado em resposta a uma chamada para [**IWMWriter:: SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename) será enumerado junto com outros coletores que você adicionou.</span><span class="sxs-lookup"><span data-stu-id="0c8e5-112">When enumerating sinks, the default file sink created in response to a call to [**IWMWriter::SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename) will be enumerated along with any other sinks you have added.</span></span> <span data-ttu-id="0c8e5-113">Se você estiver usando apenas o coletor de arquivos padrão, poderá acessá-lo chamando **getsink** para o índice de coletor 0.</span><span class="sxs-lookup"><span data-stu-id="0c8e5-113">If you are using only the default file sink, you can access it by calling **GetSink** for sink index 0.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="0c8e5-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0c8e5-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c8e5-115">**Interface IWMWriterAdvanced**</span><span class="sxs-lookup"><span data-stu-id="0c8e5-115">**IWMWriterAdvanced Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[<span data-ttu-id="0c8e5-116">**Trabalhando com coletores de gravador**</span><span class="sxs-lookup"><span data-stu-id="0c8e5-116">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 




