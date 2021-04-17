---
description: Você pode instalar produtos inteiros com o Windows Installer functions. As etapas a seguir descrevem como instalar um produto.
ms.assetid: 03cc7abc-63bd-4a01-a05c-9f7928de8827
title: Instalando um aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cf312e7394c4fcbca699f6e032e315a42356c1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755082"
---
# <a name="installing-an-application"></a>Instalando um aplicativo

Você pode instalar produtos inteiros com o Windows Installer functions. As etapas a seguir descrevem como instalar um produto.

**Para instalar um produto**

1.  Execute um produto por meio de sua sequência de instalação ou desinstalação chamando a função [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) .
2.  Especifique o nível de instalação chamando a função [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta) .

    Você pode usar os parâmetros da função [**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta) para definir o estado da instalação. Por exemplo, você pode definir o estado para instalar localmente ou instalar a partir da origem. Você pode definir o intervalo de recursos do produto a ser incluído definindo o nível.

Para obter mais informações sobre a instalação de um aplicativo, consulte [mecanismo](installation-mechanism.md)de [resiliência](resiliency.md) e instalação.

 

 



