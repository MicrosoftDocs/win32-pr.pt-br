---
title: Diretrizes para aplicativos e serviços
description: para reduzir o número de reinicializações do sistema ao instalar e atender aplicativos no Windows Vista ou no Windows Server 2008, você deve observar as diretrizes a seguir para permitir que seu aplicativo ou serviço seja desligado corretamente e reiniciado.
ms.assetid: d0b9344f-05c6-4054-90b9-86942df50b3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1d4aa10da60ca5019a723ec996532ac5b60fdbfcdb7c322ff07ecbf8681f37b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010154"
---
# <a name="guidelines-for-applications-and-services"></a>Diretrizes para aplicativos e serviços

para reduzir o número de reinicializações do sistema ao instalar e atender aplicativos no Windows Vista ou no Windows Server 2008, você deve observar as diretrizes a seguir para permitir que seu aplicativo ou serviço seja desligado corretamente e reiniciado.

-   Seus aplicativos e serviços devem estar preparados para serem desligados e reiniciados pelo sistema quando for necessário instalar uma atualização. Normalmente, quando uma atualização é instalada, um aplicativo ou serviço precisa ser desligado porque atualmente ele contém um arquivo afetado em uso. Todos os aplicativos ou serviços que podem manter um arquivo em uso durante uma atualização devem estar preparados para desligar corretamente.
-   Seus aplicativos devem salvar dados do usuário e informações de estado necessárias após uma reinicialização e devem aderir às diretrizes descritas na seção [diretrizes para aplicativos](guidelines-for-applications.md).
-   Seus serviços devem aderir às diretrizes descritas na seção [diretrizes para serviços](guidelines-for-services.md).
-   O Gerenciador de reinicialização não encerra os [serviços críticos do sistema](critical-system-services.md); Portanto, esses serviços devem limitar o número de DLLs que dependem.

 

 




