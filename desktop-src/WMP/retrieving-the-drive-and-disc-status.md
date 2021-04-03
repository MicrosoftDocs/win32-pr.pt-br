---
title: Recuperando a unidade e o status do disco
description: Recuperando a unidade e o status do disco
ms.assetid: 5e3e6107-d2bc-450c-a86e-5d3ef7b3092a
keywords:
- Windows Media Player, gravação de CD
- Modelo de objeto do Windows Media Player, gravação de CD
- modelo de objeto, gravação de CD
- Controle ActiveX do Windows Media Player, gravação de CD
- Controle ActiveX, gravação de CD
- Controle ActiveX móvel do Windows Media Player, gravação de CD
- Windows Media Player Mobile, gravação de CD
- Gravação de CD, recuperando a unidade e o status do disco
- gravando CDs, recuperando a unidade e o status do disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eab66581c336f642fd53b22f81949847d0a1c89
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103823573"
---
# <a name="retrieving-the-drive-and-disc-status"></a><span data-ttu-id="45985-112">Recuperando a unidade e o status do disco</span><span class="sxs-lookup"><span data-stu-id="45985-112">Retrieving the Drive and Disc Status</span></span>

<span data-ttu-id="45985-113">Antes de iniciar uma operação de gravação de CD, você deve garantir que a unidade de CD-ROM selecionada dê suporte à operação que você deseja executar.</span><span class="sxs-lookup"><span data-stu-id="45985-113">Before starting a CD burning operation, you must ensure that the selected CD-ROM drive supports the operation you want to perform.</span></span> <span data-ttu-id="45985-114">Por exemplo, você deve verificar se um CD pode ser apagado antes de chamar [IWMPCdromBurn:: Erase](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-erase).</span><span class="sxs-lookup"><span data-stu-id="45985-114">For instance, you must check that a CD is capable of being erased before calling [IWMPCdromBurn::erase](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-erase).</span></span> <span data-ttu-id="45985-115">O código a seguir mostra um exemplo de como usar [IWMPCdromBurn:: IsAvailable](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-isavailable) para determinar se há suporte para uma operação:</span><span class="sxs-lookup"><span data-stu-id="45985-115">The following code shows an example of using [IWMPCdromBurn::isAvailable](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-isavailable) to determine whether an operation is supported:</span></span>


```C++
VARIANT_BOOL vbResult;
    
// Check whether this drive can burn CDs.
CComBSTR bstrItem;
HRESULT hr = bstrItem.Append("Burn");
if (SUCCEEDED(hr))
{
    hr = m_spCdromBurn->isAvailable(bstrItem, &vbResult);
}
if (SUCCEEDED(hr))
{
    if (VARIANT_TRUE == vbResult)
    {
        // The current drive can burn CDs.
    }
}

```



## <a name="related-topics"></a><span data-ttu-id="45985-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="45985-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45985-117">**Gravando um CD**</span><span class="sxs-lookup"><span data-stu-id="45985-117">**Burning a CD**</span></span>](burning-a-cd.md)
</dt> <dt>

[<span data-ttu-id="45985-118">**Recuperar a interface de gravação de CD**</span><span class="sxs-lookup"><span data-stu-id="45985-118">**Retrieving the CD Burning Interface**</span></span>](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[<span data-ttu-id="45985-119">**Iniciando o processo de gravação**</span><span class="sxs-lookup"><span data-stu-id="45985-119">**Starting the Burn Process**</span></span>](starting-the-burn-process.md)
</dt> <dt>

[<span data-ttu-id="45985-120">**Apagando um CD regravável**</span><span class="sxs-lookup"><span data-stu-id="45985-120">**Erasing a Rewritable CD**</span></span>](erasing-a-rewritable-cd.md)
</dt> <dt>

[<span data-ttu-id="45985-121">**Recuperando o status da gravação**</span><span class="sxs-lookup"><span data-stu-id="45985-121">**Retrieving the Burn Status**</span></span>](retrieving-the-burn-status.md)
</dt> </dl>

 

 




