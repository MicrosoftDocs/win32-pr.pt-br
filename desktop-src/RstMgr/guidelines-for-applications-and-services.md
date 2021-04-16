---
title: Diretrizes para aplicativos e serviços
description: Para reduzir o número de reinicializações do sistema ao instalar e atender aplicativos no Windows Vista ou no Windows Server 2008, você deve observar as diretrizes a seguir para permitir que seu aplicativo ou serviço seja desligado corretamente e reiniciado.
ms.assetid: d0b9344f-05c6-4054-90b9-86942df50b3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaf2963c03432a8b016f01316b79b387754f1459
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105750205"
---
# <a name="guidelines-for-applications-and-services"></a>Diretrizes para aplicativos e serviços

Para reduzir o número de reinicializações do sistema ao instalar e atender aplicativos no Windows Vista ou no Windows Server 2008, você deve observar as diretrizes a seguir para permitir que seu aplicativo ou serviço seja desligado corretamente e reiniciado.

-   Seus aplicativos e serviços devem estar preparados para serem desligados e reiniciados pelo sistema quando for necessário instalar uma atualização. Normalmente, quando uma atualização é instalada, um aplicativo ou serviço precisa ser desligado porque atualmente ele contém um arquivo afetado em uso. Todos os aplicativos ou serviços que podem manter um arquivo em uso durante uma atualização devem estar preparados para desligar corretamente.
-   Seus aplicativos devem salvar dados do usuário e informações de estado necessárias após uma reinicialização e devem aderir às diretrizes descritas na seção [diretrizes para aplicativos](guidelines-for-applications.md).
-   Seus serviços devem aderir às diretrizes descritas na seção [diretrizes para serviços](guidelines-for-services.md).
-   O Gerenciador de reinicialização não encerra os [serviços críticos do sistema](critical-system-services.md); Portanto, esses serviços devem limitar o número de DLLs que dependem.

 

 




