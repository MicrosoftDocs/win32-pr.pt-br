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
# <a name="selecting-a-nic-using-getnppblobfromui"></a>Selecionando uma NIC usando GetNPPBlobFromUI

Com Monitor de Rede, a seleção de uma NIC por meio de programação é um processo de duas etapas. Primeiro, crie o BLOB de filtro chamando o método [**createBlob**](createblob.md) . Em seguida, selecione a NIC chamando o método [**GetNPPBlobFromUI**](getnppblobfromui.md) .

Neste exemplo, um BLOB de filtro é usado para selecionar a NIC necessária:


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



 

 



