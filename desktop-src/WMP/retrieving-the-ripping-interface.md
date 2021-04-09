---
title: Recuperar a interface de extração
description: Recuperar a interface de extração
ms.assetid: 760610eb-e356-4b50-b865-53557ba9b815
keywords:
- Windows Media Player, CD de CDs
- Modelo de objeto do Windows Media Player, cópia de CD
- modelo de objeto, cópia de CD
- Controle ActiveX do Windows Media Player, cópia de CD
- Controle ActiveX, cópia de CD
- Controle ActiveX móvel do Windows Media Player, cópia de CD
- Windows Media Player Mobile, CD-CDs
- CD de CDs, interface IWMPCdromRip
- copiando CDs, interface IWMPCdromRip
- Interface IWMPCdromRip
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 903fa285404700e35363a94239c79706e7af0e34
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "103823599"
---
# <a name="retrieving-the-ripping-interface"></a><span data-ttu-id="c355a-113">Recuperar a interface de extração</span><span class="sxs-lookup"><span data-stu-id="c355a-113">Retrieving the Ripping Interface</span></span>

<span data-ttu-id="c355a-114">Para enumerar as unidades de CD no computador do usuário, use a interface **IWMPCdromCollection** .</span><span class="sxs-lookup"><span data-stu-id="c355a-114">To enumerate the CD drives on the user's computer, use the **IWMPCdromCollection** interface.</span></span> <span data-ttu-id="c355a-115">Recupere um ponteiro para essa interface chamando [IWMPCore:: get \_ cdromCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection).</span><span class="sxs-lookup"><span data-stu-id="c355a-115">Retrieve a pointer to this interface by calling [IWMPCore::get\_cdromCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection).</span></span>

<span data-ttu-id="c355a-116">Usando os métodos [de \_ contagem](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromcollection-get_count) e [Item](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromcollection-item) de Get, você pode iterar a coleção para recuperar uma interface [IWMPCdrom](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom) para cada unidade de CD no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="c355a-116">By using the [get\_count](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromcollection-get_count) and [item](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromcollection-item) methods, you can iterate the collection to retrieve an [IWMPCdrom](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom) interface for each CD drive on the user's computer.</span></span>

<span data-ttu-id="c355a-117">A interface **IWMPCdrom** representa uma unidade de CD individual.</span><span class="sxs-lookup"><span data-stu-id="c355a-117">The **IWMPCdrom** interface represents an individual CD drive.</span></span> <span data-ttu-id="c355a-118">Antes de começar a copiar um CD, você deve primeiro chamar **QueryInterface** por meio de um ponteiro **IWMPCdrom** para recuperar a interface [IWMPCdromRip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip) .</span><span class="sxs-lookup"><span data-stu-id="c355a-118">Before you begin ripping a CD, you must first call **QueryInterface** through an **IWMPCdrom** pointer to retrieve the [IWMPCdromRip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip) interface.</span></span>

<span data-ttu-id="c355a-119">O exemplo de código a seguir demonstra como recuperar uma interface para copiar um CD de uma unidade específica:</span><span class="sxs-lookup"><span data-stu-id="c355a-119">The following code example demonstrates how to retrieve an interface for ripping a CD from a specific drive:</span></span>


```C++
HRESULT CMainDlg::GetCdromDriveCount (long &lDriveCount)
{
    HRESULT hr = m_spPlayer->get_cdromCollection(&m_spCdromCollection);

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
HRESULT CMainDlg::GetCdromRipInterface (long lIndex)
{
    // Get the IWMPCdrom interface.
    m_spCdrom.Release();
    HRESULT hr = m_spCdromCollection->item(lIndex, &m_spCdrom);
    if (SUCCEEDED(hr))
    {
        // Get the IWMPCdromRip interface.
        m_spCdromRip.Release();
        hr = m_spCdrom->QueryInterface(&m_spCdromRip);
    }

    return hr;
}

```



## <a name="related-topics"></a><span data-ttu-id="c355a-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c355a-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c355a-121">**Copiando um CD**</span><span class="sxs-lookup"><span data-stu-id="c355a-121">**Ripping a CD**</span></span>](ripping-a-cd.md)
</dt> <dt>

[<span data-ttu-id="c355a-122">**Iniciando o processo de RIP**</span><span class="sxs-lookup"><span data-stu-id="c355a-122">**Starting the Rip Process**</span></span>](starting-the-rip-process.md)
</dt> <dt>

[<span data-ttu-id="c355a-123">**Recuperando o status do RIP**</span><span class="sxs-lookup"><span data-stu-id="c355a-123">**Retrieving the Rip Status**</span></span>](retrieving-the-rip-status.md)
</dt> <dt>

[<span data-ttu-id="c355a-124">**Selecionando itens para copiar**</span><span class="sxs-lookup"><span data-stu-id="c355a-124">**Selecting Items for Ripping**</span></span>](selecting-items-for-ripping.md)
</dt> <dt>

[<span data-ttu-id="c355a-125">**Interface IWMPCdromCollection**</span><span class="sxs-lookup"><span data-stu-id="c355a-125">**IWMPCdromCollection Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> </dl>

 

 




