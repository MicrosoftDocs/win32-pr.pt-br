---
title: Iniciando o processo de gravação
description: Iniciando o processo de gravação
ms.assetid: 91442bd2-1a68-465c-b865-63d309f33d55
keywords:
- Windows Media Player, gravação de CD
- Modelo de objeto do Windows Media Player, gravação de CD
- modelo de objeto, gravação de CD
- Controle ActiveX do Windows Media Player, gravação de CD
- Controle ActiveX, gravação de CD
- Controle ActiveX móvel do Windows Media Player, gravação de CD
- Windows Media Player Mobile, gravação de CD
- Gravação de CD, iniciando processo de gravação
- gravando CDs, iniciando o processo de gravação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4a35f473eebe35bffd48ac802dcfe79082689de
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103917004"
---
# <a name="starting-the-burn-process"></a><span data-ttu-id="a3f0e-112">Iniciando o processo de gravação</span><span class="sxs-lookup"><span data-stu-id="a3f0e-112">Starting the Burn Process</span></span>

<span data-ttu-id="a3f0e-113">Antes que a gravação possa começar, você deve atribuir uma lista de reprodução a ser gravada.</span><span class="sxs-lookup"><span data-stu-id="a3f0e-113">Before burning can begin, you must assign a playlist to be burned.</span></span> <span data-ttu-id="a3f0e-114">Use [IWMPCdromBurn::p UT \_ burnPlaylist](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_burnplaylist) para especificar uma lista de reprodução para gravação.</span><span class="sxs-lookup"><span data-stu-id="a3f0e-114">Use [IWMPCdromBurn::put\_burnPlaylist](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_burnplaylist) to specify a playlist for burning.</span></span>


```C++
HRESULT CMainDlg::PutPlaylist (void)
{
    // Specify the burn playlist.   
    HRESULT hr = m_spCdromBurn->put_burnPlaylist(m_spPlaylist);

    // Update the status information.
    if (SUCCEEDED(hr))
    {
        hr = m_spCdromBurn->refreshStatus();
    }

    return hr;
}

```



<span data-ttu-id="a3f0e-115">Para obter informações sobre como usar listas de reprodução, consulte [IWMPPlaylist](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist).</span><span class="sxs-lookup"><span data-stu-id="a3f0e-115">For information about using playlists, see [IWMPPlaylist](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist).</span></span>

<span data-ttu-id="a3f0e-116">Para iniciar a operação de gravação, chame [IWMPCdromBurn:: startBurn](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-startburn).</span><span class="sxs-lookup"><span data-stu-id="a3f0e-116">To start the burning operation, call [IWMPCdromBurn::startBurn](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-startburn).</span></span>


```C++
// Start burning.
hr = m_spCdromBurn->startBurn();

```



<span data-ttu-id="a3f0e-117">Você pode interromper a operação de gravação chamando [IWMPCdromBurn:: stopBurn](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-stopburn).</span><span class="sxs-lookup"><span data-stu-id="a3f0e-117">You can stop the burning operation by calling [IWMPCdromBurn::stopBurn](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-stopburn).</span></span>


```C++
// Stop burning.
hr = m_spCdromBurn->stopBurn();

```



## <a name="related-topics"></a><span data-ttu-id="a3f0e-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a3f0e-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3f0e-119">**Gravando um CD**</span><span class="sxs-lookup"><span data-stu-id="a3f0e-119">**Burning a CD**</span></span>](burning-a-cd.md)
</dt> <dt>

[<span data-ttu-id="a3f0e-120">**Recuperar a interface de gravação de CD**</span><span class="sxs-lookup"><span data-stu-id="a3f0e-120">**Retrieving the CD Burning Interface**</span></span>](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[<span data-ttu-id="a3f0e-121">**Apagando um CD regravável**</span><span class="sxs-lookup"><span data-stu-id="a3f0e-121">**Erasing a Rewritable CD**</span></span>](erasing-a-rewritable-cd.md)
</dt> <dt>

[<span data-ttu-id="a3f0e-122">**Recuperando a unidade e o status do disco**</span><span class="sxs-lookup"><span data-stu-id="a3f0e-122">**Retrieving the Drive and Disc Status**</span></span>](retrieving-the-drive-and-disc-status.md)
</dt> <dt>

[<span data-ttu-id="a3f0e-123">**Recuperando o status da gravação**</span><span class="sxs-lookup"><span data-stu-id="a3f0e-123">**Retrieving the Burn Status**</span></span>](retrieving-the-burn-status.md)
</dt> </dl>

 

 




