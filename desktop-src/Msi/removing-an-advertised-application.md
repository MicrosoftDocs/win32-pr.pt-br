---
description: Para remover um aplicativo que foi instalado no estado anunciado, basta desinstalá-lo usando MsiInstallProduct ou MsiConfigureProduct. Você também pode remover um aplicativo anunciado da linha de comando. Consulte Opções de linha de comando.
ms.assetid: 979928fc-d95b-4c4e-88bd-aa16fbced736
title: Removendo um aplicativo anunciado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 880ce7d7de7ce7a8f9c9a20511f3f9d1b48ccdf34ffd2da51a71d226d0770b54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041576"
---
# <a name="removing-an-advertised-application"></a>Removendo um aplicativo anunciado

Para remover um aplicativo que foi instalado no estado anunciado, basta desinstalá-lo usando [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) ou [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta). Você também pode remover um aplicativo anunciado da linha de comando. Consulte [Opções de linha de comando](command-line-options.md).

Observe que talvez você não consiga remover um aplicativo anunciado se tiver criado o pacote de forma que a execução de uma instalação seja condicional na instrução **não instalada**. Um aplicativo anunciado não está instalado no computador do usuário e o instalador não define a propriedade [**instalada**](installed.md) . O pacote deve ser criado para que os aplicativos anunciados possam ser desinstalados.

 

 



