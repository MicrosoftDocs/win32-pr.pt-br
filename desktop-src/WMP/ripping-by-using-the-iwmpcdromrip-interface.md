---
title: Copiando usando a interface IWMPCdromRip
description: Copiando usando a interface IWMPCdromRip
ms.assetid: 7622072e-82e1-4e31-ad80-ddc3473b5841
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
ms.openlocfilehash: 4fcf2e959d10385365075bb20e1c04c2d796ad2e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103823572"
---
# <a name="ripping-by-using-the-iwmpcdromrip-interface"></a><span data-ttu-id="a489a-113">Copiando usando a interface IWMPCdromRip</span><span class="sxs-lookup"><span data-stu-id="a489a-113">Ripping by Using the IWMPCdromRip Interface</span></span>

<span data-ttu-id="a489a-114">Esta seção descreve como usar a interface [IWMPCdromRip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip) para copiar música de um CD.</span><span class="sxs-lookup"><span data-stu-id="a489a-114">This section describes how to use the [IWMPCdromRip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip) interface to rip music from a CD.</span></span>

<span data-ttu-id="a489a-115">Copiar um CD usando a interface **IWMPCdromRip** tem o mesmo efeito que copiar música usando a interface do usuário do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="a489a-115">Ripping a CD by using the **IWMPCdromRip** interface has the same effect as ripping music by using the Windows Media Player user interface.</span></span> <span data-ttu-id="a489a-116">O conteúdo copiado é adicionado automaticamente à biblioteca de acordo com as preferências do usuário.</span><span class="sxs-lookup"><span data-stu-id="a489a-116">Ripped content is automatically added to the library according to the user's preferences.</span></span> <span data-ttu-id="a489a-117">Para obter mais informações sobre cópia de CD, consulte "copiando música de CDs" na ajuda do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="a489a-117">For more information about CD ripping, see "Ripping music from CDs" in Windows Media Player Help.</span></span>

<span data-ttu-id="a489a-118">Os exemplos de código nesta seção usam classes Active Template Library (ATL), como **CComPtr**.</span><span class="sxs-lookup"><span data-stu-id="a489a-118">The code examples in this section use Active Template Library (ATL) classes, such as **CComPtr**.</span></span>

## <a name="included-headers"></a><span data-ttu-id="a489a-119">Cabeçalhos incluídos</span><span class="sxs-lookup"><span data-stu-id="a489a-119">Included Headers</span></span>

<span data-ttu-id="a489a-120">Para usar o código nesta seção, inclua os seguintes cabeçalhos:</span><span class="sxs-lookup"><span data-stu-id="a489a-120">To use the code in this section, include the following headers:</span></span>


```C++
#include <atlbase.h>
#include <atlcom.h>
#include <atlwin.h>
#include <commctrl.h>
#include "wmp.h"
#include "wmpids.h"

```



## <a name="interface-pointers"></a><span data-ttu-id="a489a-121">Ponteiros de interface</span><span class="sxs-lookup"><span data-stu-id="a489a-121">Interface Pointers</span></span>

<span data-ttu-id="a489a-122">As interfaces do Windows Media Player são armazenadas nas seguintes variáveis de membro.</span><span class="sxs-lookup"><span data-stu-id="a489a-122">The interfaces for Windows Media Player are stored in the following member variables.</span></span>


```C++
// Player interface.
CComPtr<IWMPPlayer>             m_spPlayer;

// CDROM interfaces.
CComPtr<IWMPCdromCollection>    m_spCdromCollection;
CComPtr<IWMPCdrom>              m_spCdrom;
CComPtr<IWMPCdromRip>           m_spCdromRip;
CComPtr<IWMPPlaylist>           m_spPlaylist;

```



<span data-ttu-id="a489a-123">As seções a seguir descrevem como usar a interface IWMPCdromRip</span><span class="sxs-lookup"><span data-stu-id="a489a-123">The Following Sections Describe How to Use the IWMPCdromRip Interface</span></span>

-   [<span data-ttu-id="a489a-124">Recuperar a interface de extração</span><span class="sxs-lookup"><span data-stu-id="a489a-124">Retrieving the Ripping Interface</span></span>](retrieving-the-ripping-interface.md)
-   [<span data-ttu-id="a489a-125">Iniciando o processo de RIP</span><span class="sxs-lookup"><span data-stu-id="a489a-125">Starting the Rip Process</span></span>](starting-the-rip-process.md)
-   [<span data-ttu-id="a489a-126">Recuperando o status do RIP</span><span class="sxs-lookup"><span data-stu-id="a489a-126">Retrieving the Rip Status</span></span>](retrieving-the-rip-status.md)
-   [<span data-ttu-id="a489a-127">Selecionando itens para copiar</span><span class="sxs-lookup"><span data-stu-id="a489a-127">Selecting Items for Ripping</span></span>](selecting-items-for-ripping.md)

 

 




