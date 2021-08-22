---
title: Configurando descompactores e descompactores
description: Configurando descompactores e descompactores
ms.assetid: 9cd63470-1591-4de0-b011-d7979539d936
keywords:
- VCM (gerenciador de compactação de vídeo), configurando os vcms
- VCM (gerenciador de compactação de vídeo), configurando os vcs
- Macro ICQueryConfigure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073a9ac7eb56c0870d7a08d8ed9fd221a2626bb6be83cc4683cd86c4bfa907db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144919"
---
# <a name="configuring-compressors-and-decompressors"></a>Configurando descompactores e descompactores

O exemplo a seguir usa a macro [**ICQueryConfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) para demonstrar como testar se uma caixa de diálogo dá suporte à caixa de diálogo de configuração e exibi-la, se isso acontecer.


```C++
// If the compressor handles a configuration dialog box, display it 
// using our application window as the parent window. 

if (ICQueryConfigure(hIC)) ICConfigure(hIC, hwndApp); 
 
```



O exemplo a seguir mostra como obter os dados de estado usando a [**macro ICGetState.**](/windows/desktop/api/Vfw/nf-vfw-icgetstate)


```C++
dwStateSize = ICGetStateSize(hIC);    // gets size of buffer required 
h = GlobalAlloc(GHND, dwStateSize);   // allocates buffer 
ICGetState(hIC, (LPVOID)lpData, dwStateSize);  // gets the state data 
 
// Store the state data as required. 
 
```



O exemplo a seguir mostra como restaurar dados de estado usando a [**macro ICSetState.**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) Os dados de estado restaurados por aplicativos não devem conter nenhuma alteração nos dados de estado obtidos de um driver.


```C++
ICSetState(hIC, (LPVOID)lpData, dwStateSize); // sets new state data 
 
```



 

 




