---
description: Com Monitor de Rede, a seleção de uma NIC por meio de programação é um processo de duas etapas. Primeiro, crie o BLOB de filtro chamando o método createBlob. Em seguida, selecione a NIC chamando o método GetNPPBlobFromUI.
ms.assetid: 0556b20a-307e-4bc3-a986-cfee96a8655d
title: Selecionando uma NIC usando GetNPPBlobFromUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3bd02ef5085bba511fb0d05844840eb92d85ef83c67f244ab321570fae4ad8c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128896"
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



 

 



