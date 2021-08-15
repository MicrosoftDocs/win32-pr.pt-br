---
description: o arquivo de cabeçalho Winternl. h expõe protótipos de APIs de Windows internas. Não há biblioteca de importação associada, portanto os desenvolvedores devem usar a vinculação dinâmica em tempo de execução para chamar as funções descritas neste arquivo de cabeçalho.
ms.assetid: 11f09479-e04b-4e5e-bc46-a2d0daf13785
title: Chamando APIs internas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9c613b4f650709eb9764eff133c018be62768c58212b4dc7130149ce8b5173
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956125"
---
# <a name="calling-internal-apis"></a>Chamando APIs internas

o arquivo de cabeçalho Winternl. h expõe protótipos de APIs de Windows internas. Não há biblioteca de importação associada, portanto os desenvolvedores devem usar a vinculação dinâmica em tempo de execução para chamar as funções descritas neste arquivo de cabeçalho.

as funções e estruturas em Winternl. h são internas ao sistema operacional e estão sujeitas a alterações de uma versão do Windows para a próxima e, possivelmente, entre os service packs de cada versão. Para manter a compatibilidade do seu aplicativo, você deve usar as funções públicas equivalentes em vez disso. Mais informações estão disponíveis no arquivo de cabeçalho, Winternl. h, e a documentação para cada função.

Se você usar essas funções, poderá acessá-las por meio da vinculação dinâmica em tempo de execução usando [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress). Isso dá ao seu código uma oportunidade de responder normalmente se a função tiver sido alterada ou removida do sistema operacional. As alterações de assinatura, no entanto, podem não ser detectáveis.

 

 
