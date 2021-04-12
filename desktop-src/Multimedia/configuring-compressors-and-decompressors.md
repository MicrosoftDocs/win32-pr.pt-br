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
# <a name="configuring-compressors-and-decompressors"></a><span data-ttu-id="099ae-106">Configurando compactadores e descompactadores</span><span class="sxs-lookup"><span data-stu-id="099ae-106">Configuring Compressors and Decompressors</span></span>

<span data-ttu-id="099ae-107">O exemplo a seguir usa a macro [**ICQueryConfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) para demonstrar como testar se um compressor dá suporte à caixa de diálogo de configuração e exibi-la se ela existir.</span><span class="sxs-lookup"><span data-stu-id="099ae-107">The following example uses the [**ICQueryConfigure**](/windows/desktop/api/Vfw/nf-vfw-icqueryconfigure) macro to demonstrate how to test whether a compressor supports the configuration dialog box and to display it if it does.</span></span>


```C++
// If the compressor handles a configuration dialog box, display it 
// using our application window as the parent window. 

if (ICQueryConfigure(hIC)) ICConfigure(hIC, hwndApp); 
 
```



<span data-ttu-id="099ae-108">O exemplo a seguir mostra como obter os dados de estado usando a macro [**ICGetState**](/windows/desktop/api/Vfw/nf-vfw-icgetstate) .</span><span class="sxs-lookup"><span data-stu-id="099ae-108">The following example shows how to obtain the state data using the [**ICGetState**](/windows/desktop/api/Vfw/nf-vfw-icgetstate) macro.</span></span>


```C++
dwStateSize = ICGetStateSize(hIC);    // gets size of buffer required 
h = GlobalAlloc(GHND, dwStateSize);   // allocates buffer 
ICGetState(hIC, (LPVOID)lpData, dwStateSize);  // gets the state data 
 
// Store the state data as required. 
 
```



<span data-ttu-id="099ae-109">O exemplo a seguir mostra como restaurar dados de estado usando a macro [**ICSetState**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) .</span><span class="sxs-lookup"><span data-stu-id="099ae-109">The following example shows how to restore state data using the [**ICSetState**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) macro.</span></span> <span data-ttu-id="099ae-110">Os dados de estado restaurados por aplicativos não devem conter nenhuma alteração nos dados de estado obtidos de um driver.</span><span class="sxs-lookup"><span data-stu-id="099ae-110">State data restored by applications should not contain any changes to the state data obtained from a driver.</span></span>


```C++
ICSetState(hIC, (LPVOID)lpData, dwStateSize); // sets new state data 
 
```



 

 




