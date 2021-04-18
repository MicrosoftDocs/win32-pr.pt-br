---
description: Com Monitor de Rede, a seleção de uma NIC por meio de programação é um processo de duas etapas. Primeiro, crie o BLOB de filtro chamando o método createBlob. Em seguida, selecione a NIC chamando o método GetNPPBlobFromUI.
ms.assetid: 0556b20a-307e-4bc3-a986-cfee96a8655d
title: Selecionando uma NIC usando GetNPPBlobFromUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb429a87d284a5a6a03a20357728c8bbcb5acac4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810295"
---
# <a name="selecting-a-nic-using-getnppblobfromui"></a><span data-ttu-id="ac870-105">Selecionando uma NIC usando GetNPPBlobFromUI</span><span class="sxs-lookup"><span data-stu-id="ac870-105">Selecting a NIC Using GetNPPBlobFromUI</span></span>

<span data-ttu-id="ac870-106">Com Monitor de Rede, a seleção de uma NIC por meio de programação é um processo de duas etapas.</span><span class="sxs-lookup"><span data-stu-id="ac870-106">With Network Monitor, selecting a NIC programmatically is a two-step process.</span></span> <span data-ttu-id="ac870-107">Primeiro, crie o BLOB de filtro chamando o método [**createBlob**](createblob.md) .</span><span class="sxs-lookup"><span data-stu-id="ac870-107">First, create the filter BLOB by calling the [**CreateBlob**](createblob.md) method.</span></span> <span data-ttu-id="ac870-108">Em seguida, selecione a NIC chamando o método [**GetNPPBlobFromUI**](getnppblobfromui.md) .</span><span class="sxs-lookup"><span data-stu-id="ac870-108">Then, select the NIC by calling the [**GetNPPBlobFromUI**](getnppblobfromui.md) method.</span></span>

<span data-ttu-id="ac870-109">Neste exemplo, um BLOB de filtro é usado para selecionar a NIC necessária:</span><span class="sxs-lookup"><span data-stu-id="ac870-109">In this example a filter BLOB is used to select the required NIC:</span></span>


```C++
DWORD rc;

// Call CreateBlob to create a filter blob.
///////////////////////////////////////////
HBLOB hFilterBlob;
rc = CreateBlob(&hFilterBlob);
if (FAILED (rc));
{
  // Failed creating filter BLOB. Add appropriate error handling.
}


// Call GetNPPBlobFromUI to retrieve the NPP Blob.
//////////////////////////////////////////////////
rc = GetNPPBlobFromUI(hwnd,
                      hFilterBlob,
                      &hBlob);
if (FAILED (rc));
{
  // Failed retrieving NPP BLOB. Add appropriate error handling.
}
```



 

 



