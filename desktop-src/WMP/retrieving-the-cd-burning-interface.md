---
title: Recuperar a interface de gravação de CD
description: Recuperar a interface de gravação de CD
ms.assetid: d52f7b27-a327-4656-8dc2-0b075264d295
keywords:
- Windows Media Player, gravação de CD
- Modelo de objeto do Windows Media Player, gravação de CD
- modelo de objeto, gravação de CD
- Controle ActiveX do Windows Media Player, gravação de CD
- Controle ActiveX, gravação de CD
- Controle ActiveX móvel do Windows Media Player, gravação de CD
- Windows Media Player Mobile, gravação de CD
- Gravação de CD, recuperando a interface IWMPCdromCollection
- gravando CDs, recuperando a interface IWMPCdromCollection
- Interface IWMPCdromCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b63763f9dd99bbaf88ae099edb53ba072cd1a25e
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104007229"
---
# <a name="retrieving-the-cd-burning-interface"></a><span data-ttu-id="dc197-113">Recuperar a interface de gravação de CD</span><span class="sxs-lookup"><span data-stu-id="dc197-113">Retrieving the CD Burning Interface</span></span>

<span data-ttu-id="dc197-114">Para enumerar as unidades de CD no computador do usuário, use a interface **IWMPCdromCollection** .</span><span class="sxs-lookup"><span data-stu-id="dc197-114">To enumerate the CD drives on the user's computer, use the **IWMPCdromCollection** interface.</span></span> <span data-ttu-id="dc197-115">Você recupera um ponteiro para essa interface chamando [IWMPCore:: get \_ cdromCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection).</span><span class="sxs-lookup"><span data-stu-id="dc197-115">You retrieve a pointer to this interface by calling [IWMPCore::get\_cdromCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection).</span></span>

<span data-ttu-id="dc197-116">Usando os métodos **de \_ contagem** e **Item** de Get, você pode iterar a coleção para recuperar um ponteiro de interface [IWMPCdrom](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom) para cada unidade de CD no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="dc197-116">By using the **get\_count** and **item** methods, you can iterate the collection to retrieve an [IWMPCdrom](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom) interface pointer for each CD drive on the user's computer.</span></span>

<span data-ttu-id="dc197-117">A interface **IWMPCdrom** representa uma unidade de CD individual.</span><span class="sxs-lookup"><span data-stu-id="dc197-117">The **IWMPCdrom** interface represents an individual CD drive.</span></span> <span data-ttu-id="dc197-118">Antes de começar a gravar um CD, você deve primeiro chamar **QueryInterface** por meio de um ponteiro **IWMPCdrom** para recuperar um ponteiro para a interface [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) .</span><span class="sxs-lookup"><span data-stu-id="dc197-118">Before you begin burning a CD, you must first call **QueryInterface** through an **IWMPCdrom** pointer to retrieve a pointer to the [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) interface.</span></span>

<span data-ttu-id="dc197-119">O exemplo de código a seguir demonstra como recuperar uma interface para gravar um CD em uma unidade específica:</span><span class="sxs-lookup"><span data-stu-id="dc197-119">The following code example demonstrates how to retrieve an interface for burning a CD to a specific drive:</span></span>


```C++
HRESULT CMainDlg::GetCdromDriveCount (long &lDriveCount)
{
    hr = m_spPlayer->get_cdromCollection(&m_spCdromCollection);

    // Get the number of CDROM drives.
    if (SUCCEEDED(hr))
    {
        hr = m_spCdromCollection->get_count(&lDriveCount);
    }

    return hr;
}

// lIndex refers to the index of the current drive,
// which must be less than the value retrieved by
// GetCdromDriveCount above.
HRESULT CMainDlg::GetCdromBurnInterface (long lIndex)
{
    // Get the IWMPCdrom interface.
    m_spCdrom.Release();
    HRESULT hr = m_spCdromCollection->item(lIndex, &m_spCdrom);
    if (SUCCEEDED(hr))
    {
        // Get the IWMPCdromBurn interface.
        m_spCdromBurn.Release();
        hr = m_spCdrom->QueryInterface(&m_spCdromBurn);
    }

    return hr;
}

```



## <a name="related-topics"></a><span data-ttu-id="dc197-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dc197-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc197-121">**Gravando um CD**</span><span class="sxs-lookup"><span data-stu-id="dc197-121">**Burning a CD**</span></span>](burning-a-cd.md)
</dt> <dt>

[<span data-ttu-id="dc197-122">**Iniciando o processo de gravação**</span><span class="sxs-lookup"><span data-stu-id="dc197-122">**Starting the Burn Process**</span></span>](starting-the-burn-process.md)
</dt> <dt>

[<span data-ttu-id="dc197-123">**Apagando um CD regravável**</span><span class="sxs-lookup"><span data-stu-id="dc197-123">**Erasing a Rewritable CD**</span></span>](erasing-a-rewritable-cd.md)
</dt> <dt>

[<span data-ttu-id="dc197-124">**Recuperando a unidade e o status do disco**</span><span class="sxs-lookup"><span data-stu-id="dc197-124">**Retrieving the Drive and Disc Status**</span></span>](retrieving-the-drive-and-disc-status.md)
</dt> <dt>

[<span data-ttu-id="dc197-125">**Recuperando o status da gravação**</span><span class="sxs-lookup"><span data-stu-id="dc197-125">**Retrieving the Burn Status**</span></span>](retrieving-the-burn-status.md)
</dt> <dt>

[<span data-ttu-id="dc197-126">**Interface IWMPCdromCollection**</span><span class="sxs-lookup"><span data-stu-id="dc197-126">**IWMPCdromCollection Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> </dl>

 

 




