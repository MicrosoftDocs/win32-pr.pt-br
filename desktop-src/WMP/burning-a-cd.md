---
title: Gravando um CD
description: Gravando um CD
ms.assetid: df55479e-d8a7-443d-bf2c-c988bfd0b1be
keywords:
- Windows Media Player, gravação de CD
- Modelo de objeto do Windows Media Player, gravação de CD
- modelo de objeto, gravação de CD
- Controle ActiveX do Windows Media Player, gravação de CD
- Controle ActiveX, gravação de CD
- Controle ActiveX móvel do Windows Media Player, gravação de CD
- Windows Media Player Mobile, gravação de CD
- Gravação de CD, sobre
- gravando CDs, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 007b7808ff375ab0673592d0d016f8e713321d1a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104084360"
---
# <a name="burning-a-cd"></a><span data-ttu-id="303db-112">Gravando um CD</span><span class="sxs-lookup"><span data-stu-id="303db-112">Burning a CD</span></span>

<span data-ttu-id="303db-113">Esta seção descreve como usar a interface [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) para gravar música em um CD.</span><span class="sxs-lookup"><span data-stu-id="303db-113">This section describes how to use the [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) interface to burn music to a CD.</span></span> <span data-ttu-id="303db-114">A interface **IWMPCdromBurn** fornece funcionalidade para gravar listas de reprodução em CDs como faixas de dados ou áudio, bem como apagar a CD-RWs.</span><span class="sxs-lookup"><span data-stu-id="303db-114">The **IWMPCdromBurn** interface provides functionality for burning playlists to CDs as either data or audio tracks, as well as erasing CD-RWs.</span></span>

<span data-ttu-id="303db-115">Uso de código</span><span class="sxs-lookup"><span data-stu-id="303db-115">Code Usage</span></span>

<span data-ttu-id="303db-116">Os exemplos de código nesta seção usam classes Active Template Library (ATL), como **CComPtr**.</span><span class="sxs-lookup"><span data-stu-id="303db-116">The code examples in this section use Active Template Library (ATL) classes, such as **CComPtr**.</span></span>

<span data-ttu-id="303db-117">Cabeçalhos incluídos</span><span class="sxs-lookup"><span data-stu-id="303db-117">Included Headers</span></span>

<span data-ttu-id="303db-118">Para usar o código nesta seção, inclua os seguintes cabeçalhos:</span><span class="sxs-lookup"><span data-stu-id="303db-118">To use the code in this section, include the following headers:</span></span>


```C++
#include <atlbase.h>
#include <atlcom.h>
#include <atlwin.h>
#include <commctrl.h>
#include "wmp.h"
#include "wmpids.h"

```



<span data-ttu-id="303db-119">Ponteiros de interface</span><span class="sxs-lookup"><span data-stu-id="303db-119">Interface Pointers</span></span>

<span data-ttu-id="303db-120">As interfaces do Windows Media Player são armazenadas nas seguintes variáveis de membro:</span><span class="sxs-lookup"><span data-stu-id="303db-120">The interfaces for Windows Media Player are stored in the following member variables:</span></span>


```C++
// Player interface.
CComPtr<IWMPPlayer>             m_spPlayer;

// CDROM interfaces.
CComPtr<IWMPCdromCollection>    m_spCdromCollection;
CComPtr<IWMPCdrom>              m_spCdrom;
CComPtr<IWMPCdromBurn>          m_spCdromBurn;
CComPtr<IWMPPlaylist>           m_spPlaylist;

```



<span data-ttu-id="303db-121">Os tópicos a seguir descrevem como usar a API de gravação de CD.</span><span class="sxs-lookup"><span data-stu-id="303db-121">The following topics describe how to use the CD burning API.</span></span>

-   [<span data-ttu-id="303db-122">Recuperar a interface de gravação de CD</span><span class="sxs-lookup"><span data-stu-id="303db-122">Retrieving the CD Burning Interface</span></span>](retrieving-the-cd-burning-interface.md)
-   [<span data-ttu-id="303db-123">Iniciando o processo de gravação</span><span class="sxs-lookup"><span data-stu-id="303db-123">Starting the Burn Process</span></span>](starting-the-burn-process.md)
-   [<span data-ttu-id="303db-124">Apagando um CD regravável</span><span class="sxs-lookup"><span data-stu-id="303db-124">Erasing a Rewritable CD</span></span>](erasing-a-rewritable-cd.md)
-   [<span data-ttu-id="303db-125">Recuperando a unidade e o status do disco</span><span class="sxs-lookup"><span data-stu-id="303db-125">Retrieving the Drive and Disc Status</span></span>](retrieving-the-drive-and-disc-status.md)
-   [<span data-ttu-id="303db-126">Recuperando o status da gravação</span><span class="sxs-lookup"><span data-stu-id="303db-126">Retrieving the Burn Status</span></span>](retrieving-the-burn-status.md)

## <a name="related-topics"></a><span data-ttu-id="303db-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="303db-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="303db-128">**Guia de controle do Player**</span><span class="sxs-lookup"><span data-stu-id="303db-128">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




