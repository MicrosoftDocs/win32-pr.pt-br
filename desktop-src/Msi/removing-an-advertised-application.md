---
description: Para remover um aplicativo que foi instalado no estado anunciado, basta desinstalá-lo usando MsiInstallProduct ou MsiConfigureProduct. Você também pode remover um aplicativo anunciado da linha de comando. Consulte Opções de linha de comando.
ms.assetid: 979928fc-d95b-4c4e-88bd-aa16fbced736
title: Removendo um aplicativo anunciado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6e8aba31dfd1538afc5585ada41b193c642950a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828868"
---
# <a name="removing-an-advertised-application"></a>Removendo um aplicativo anunciado

Para remover um aplicativo que foi instalado no estado anunciado, basta desinstalá-lo usando [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) ou [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta). Você também pode remover um aplicativo anunciado da linha de comando. Consulte [Opções de linha de comando](command-line-options.md).

Observe que talvez você não consiga remover um aplicativo anunciado se tiver criado o pacote de forma que a execução de uma instalação seja condicional na instrução **não instalada**. Um aplicativo anunciado não está instalado no computador do usuário e o instalador não define a propriedade [**instalada**](installed.md) . O pacote deve ser criado para que os aplicativos anunciados possam ser desinstalados.

 

 



