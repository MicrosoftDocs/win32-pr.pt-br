---
title: Configurando compactadores e descompactadores
description: Configurando compactadores e descompactadores
ms.assetid: 9cd63470-1591-4de0-b011-d7979539d936
keywords:
- VCM (Gerenciador de compactação de vídeo), configurando os compactadores
- VCM (Gerenciador de compactação de vídeo), configurando os compactadores
- Macro ICQueryConfigure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88d388a52047a1aea7936cc494dafc0d1a2d6dec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363923"
---
# <a name="configuring-compressors-and-decompressors"></a>Configurando compactadores e descompactadores

O exemplo a seguir usa a macro [**ICQueryConfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) para demonstrar como testar se um compressor dá suporte à caixa de diálogo de configuração e exibi-la se ela existir.


```C++
// If the compressor handles a configuration dialog box, display it 
// using our application window as the parent window. 

if (ICQueryConfigure(hIC)) ICConfigure(hIC, hwndApp); 
 
```



O exemplo a seguir mostra como obter os dados de estado usando a macro [**ICGetState**](/windows/desktop/api/Vfw/nf-vfw-icgetstate) .


```C++
dwStateSize = ICGetStateSize(hIC);    // gets size of buffer required 
h = GlobalAlloc(GHND, dwStateSize);   // allocates buffer 
ICGetState(hIC, (LPVOID)lpData, dwStateSize);  // gets the state data 
 
// Store the state data as required. 
 
```



O exemplo a seguir mostra como restaurar dados de estado usando a macro [**ICSetState**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) . Os dados de estado restaurados por aplicativos não devem conter nenhuma alteração nos dados de estado obtidos de um driver.


```C++
ICSetState(hIC, (LPVOID)lpData, dwStateSize); // sets new state data 
 
```



 

 




