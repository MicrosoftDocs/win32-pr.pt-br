---
title: Iniciando o processo de RIP
description: Iniciando o processo de RIP
ms.assetid: 82ffc114-ddad-41be-af80-6c1bd29cb0d4
keywords:
- Windows Media Player, CD de CDs
- Modelo de objeto do Windows Media Player, cópia de CD
- modelo de objeto, cópia de CD
- Controle ActiveX do Windows Media Player, cópia de CD
- Controle ActiveX, cópia de CD
- Controle ActiveX móvel do Windows Media Player, cópia de CD
- Windows Media Player Mobile, CD-CDs
- CD de CDs, iniciando processo de RIP
- copiando CDs, iniciando processo RIP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2107b053abf8747d7add8fcedc26a2386ae5fd84
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "105811400"
---
# <a name="starting-the-rip-process"></a><span data-ttu-id="f2886-112">Iniciando o processo de RIP</span><span class="sxs-lookup"><span data-stu-id="f2886-112">Starting the Rip Process</span></span>

<span data-ttu-id="f2886-113">Depois de recuperar a interface de cópia de música conforme explicado na seção anterior, inicie o processo de cópia de CDs chamando [IWMPCdromRip:: startRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-startrip).</span><span class="sxs-lookup"><span data-stu-id="f2886-113">After you have retrieved the ripping interface as explained in the previous section, start the ripping process by calling [IWMPCdromRip::startRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-startrip).</span></span>


```C++
// Start ripping.
HRESULT hr = m_spCdromRip->startRip();

```



<span data-ttu-id="f2886-114">Você pode interromper a operação de cópia de CDs chamando [IWMPCdromRip:: stopRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-stoprip).</span><span class="sxs-lookup"><span data-stu-id="f2886-114">You can stop the ripping operation by calling [IWMPCdromRip::stopRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-stoprip).</span></span>


```C++
// Stop ripping.
HRESULT hr = m_spCdromRip->stopRip();

```



## <a name="related-topics"></a><span data-ttu-id="f2886-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f2886-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2886-116">**Copiando um CD**</span><span class="sxs-lookup"><span data-stu-id="f2886-116">**Ripping a CD**</span></span>](ripping-a-cd.md)
</dt> <dt>

[<span data-ttu-id="f2886-117">**Recuperar a interface de extração**</span><span class="sxs-lookup"><span data-stu-id="f2886-117">**Retrieving the Ripping Interface**</span></span>](retrieving-the-ripping-interface.md)
</dt> <dt>

[<span data-ttu-id="f2886-118">**Recuperando o status do RIP**</span><span class="sxs-lookup"><span data-stu-id="f2886-118">**Retrieving the Rip Status**</span></span>](retrieving-the-rip-status.md)
</dt> <dt>

[<span data-ttu-id="f2886-119">**Selecionando itens para copiar**</span><span class="sxs-lookup"><span data-stu-id="f2886-119">**Selecting Items for Ripping**</span></span>](selecting-items-for-ripping.md)
</dt> </dl>

 

 




