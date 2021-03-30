---
title: Gravando fluxos de taxa de bits variáveis
description: Gravando fluxos de taxa de bits variáveis
ms.assetid: 9eccde59-8342-44ad-90e6-032db022d7c5
keywords:
- ASF (Advanced Systems Format), gravando fluxos de VBR
- ASF (formato de sistemas avançados), gravando fluxos de VBR
- taxa de bits variável (VBR), gravando fluxos
- VBR (taxa de bits variável), gravando fluxos
- fluxos, gravando VBR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6981cbae04085c4bf4f771d9dd29e30752427cdc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103640119"
---
# <a name="writing-variable-bit-rate-streams"></a><span data-ttu-id="5bc30-108">Gravando fluxos de taxa de bits variáveis</span><span class="sxs-lookup"><span data-stu-id="5bc30-108">Writing Variable Bit Rate Streams</span></span>

<span data-ttu-id="5bc30-109">Os fluxos de taxa de bits variável (VBR) são gravados da mesma forma que os fluxos de taxa de bits constante (CBR).</span><span class="sxs-lookup"><span data-stu-id="5bc30-109">Variable bit rate (VBR) streams are written the same way as constant bit rate (CBR) streams.</span></span> <span data-ttu-id="5bc30-110">A única diferença está no processamento realizado internamente pelo gravador e pelos codecs.</span><span class="sxs-lookup"><span data-stu-id="5bc30-110">The only difference is in the processing performed internally by the writer and the codecs.</span></span> <span data-ttu-id="5bc30-111">No entanto, a taxa de bits (restrita e irrestrita) baseada em taxas de bit requer uma passagem de pré-processamento no gravador.</span><span class="sxs-lookup"><span data-stu-id="5bc30-111">However, bit rate based VBR (both constrained and unconstrained) requires a preprocessing pass in the writer.</span></span>

<span data-ttu-id="5bc30-112">Você deve verificar o valor de retorno para a primeira chamada feita para [**IWMWriter:: WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) para cada fluxo.</span><span class="sxs-lookup"><span data-stu-id="5bc30-112">You should check the return value for the first call you make to [**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) for each stream.</span></span> <span data-ttu-id="5bc30-113">Se o código de erro retornado for \_ um número inválido de e/s do NS \_ \_ \_ , o fluxo exigirá uma passagem de pré-processamento.</span><span class="sxs-lookup"><span data-stu-id="5bc30-113">If the error code returned is NS\_E\_INVALID\_NUM\_PASSES, the stream requires a preprocessing pass.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5bc30-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5bc30-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5bc30-115">**Usando a codificação Two-Pass**</span><span class="sxs-lookup"><span data-stu-id="5bc30-115">**Using Two-Pass Encoding**</span></span>](using-two-pass-encoding.md)
</dt> <dt>

[<span data-ttu-id="5bc30-116">**Gravando arquivos ASF**</span><span class="sxs-lookup"><span data-stu-id="5bc30-116">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




