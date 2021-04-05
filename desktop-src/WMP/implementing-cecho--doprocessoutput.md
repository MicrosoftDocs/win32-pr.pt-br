---
title: Implementando CEcho DoProcessOutput
description: Implementando CEcho DoProcessOutput
ms.assetid: afd91022-4e2d-46a2-a0f4-cd2b558536d6
keywords:
- Plug-ins do Windows Media Player, método Echo DoProcessOutput de exemplo
- plug-ins, exemplo de método Echo DoProcessOutput
- plug-ins de processamento de sinal digital, Echo Sample DoProcessOutput Method
- Plug-ins do DSP, método Echo de exemplo DoProcessOutput
- Exemplo de plug-in do DSP de eco, método DoProcessOutput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ff40246a6a0ccda2b3f17b12924c44cb79fa4d9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006152"
---
# <a name="implementing-cechodoprocessoutput"></a><span data-ttu-id="8989d-108">Implementando CEcho::D oProcessOutput</span><span class="sxs-lookup"><span data-stu-id="8989d-108">Implementing CEcho::DoProcessOutput</span></span>

<span data-ttu-id="8989d-109">O método **DoProcessOutput** executa o processamento de sinal digital.</span><span class="sxs-lookup"><span data-stu-id="8989d-109">The **DoProcessOutput** method performs the digital signal processing.</span></span> <span data-ttu-id="8989d-110">Esse é o método que faz as alterações nos dados fornecidos pelo Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="8989d-110">This is the method that makes the changes to the data provided by Windows Media Player.</span></span> <span data-ttu-id="8989d-111">São os resultados desse método que você ouvirá como um efeito de eco quando o plug-in de exemplo de eco for concluído.</span><span class="sxs-lookup"><span data-stu-id="8989d-111">It is the results of this method that you will hear as an echo effect when your Echo sample plug-in is complete.</span></span>

<span data-ttu-id="8989d-112">Para este exemplo, o plug-in processará apenas áudio de 8 ou 16 bits.</span><span class="sxs-lookup"><span data-stu-id="8989d-112">For this sample, the plug-in will only process 8-bit or 16-bit audio.</span></span> <span data-ttu-id="8989d-113">Você precisará fazer algumas alterações no código de exemplo do assistente de plug-in para remover as seções que processam áudio de maior profundidade de bits.</span><span class="sxs-lookup"><span data-stu-id="8989d-113">You will need to make some changes to the plug-in wizard sample code to remove the sections that process higher bit depth audio.</span></span> <span data-ttu-id="8989d-114">No entanto, vale a pena estudar essas seções, pois você pode decidir adicionar sua própria implementação de eco para esses formatos.</span><span class="sxs-lookup"><span data-stu-id="8989d-114">It is worthwhile to study these sections, however, because you may decide to add your own echo implementation for those formats.</span></span>

<span data-ttu-id="8989d-115">As seções a seguir detalham as alterações que você precisa fazer no código:</span><span class="sxs-lookup"><span data-stu-id="8989d-115">The following sections detail the changes you need to make to the code:</span></span>

-   [<span data-ttu-id="8989d-116">Removendo o código para processar mais de 16 bits</span><span class="sxs-lookup"><span data-stu-id="8989d-116">Removing the Code to Process Greater than 16 Bits</span></span>](removing-the-code-to-process-greater-than-16-bits.md)
-   [<span data-ttu-id="8989d-117">Processando os dados de áudio</span><span class="sxs-lookup"><span data-stu-id="8989d-117">Processing the Audio Data</span></span>](processing-the-audio-data.md)
-   [<span data-ttu-id="8989d-118">Variáveis para executar o processamento</span><span class="sxs-lookup"><span data-stu-id="8989d-118">Variables to Perform Processing</span></span>](variables-to-perform-processing.md)
-   [<span data-ttu-id="8989d-119">Criando o efeito de eco</span><span class="sxs-lookup"><span data-stu-id="8989d-119">Creating the Echo Effect</span></span>](creating-the-echo-effect.md)

## <a name="related-topics"></a><span data-ttu-id="8989d-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8989d-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8989d-121">**O exemplo de eco**</span><span class="sxs-lookup"><span data-stu-id="8989d-121">**The Echo Sample**</span></span>](the-echo-sample.md)
</dt> </dl>

 

 




