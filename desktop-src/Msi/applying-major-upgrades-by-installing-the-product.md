---
description: Uma atualização importante pode ser aplicada instalando o novo pacote de instalação para o produto atualizado.
ms.assetid: f4fb28be-5ec0-4eac-9d4d-eccf5bd61ac4
title: Aplicando atualizações principais instalando o produto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79570051ddbff27b12a11e04e41c37f4babad96ff045bc408e00c2b7164b263a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045676"
---
# <a name="applying-major-upgrades-by-installing-the-product"></a>Aplicando atualizações principais instalando o produto

Uma atualização importante pode ser aplicada instalando o novo pacote de instalação para o produto atualizado. Como as atualizações principais têm um código de produto diferente do produto original, a instalação da atualização deve ser tratada como uma instalação de um novo produto. A atualização pode simplesmente ser instalada como outro produto. Você pode fazer com que o novo pacote de [](upgrade-table.md) instalação manipular a remoção do produto antigo incluindo a tabela Upgrade e a ação [FindRelatedProducts](findrelatedproducts-action.md) e [RemoveExistingProducts](removeexistingproducts-action.md).

**Para propagar uma atualização principal para os usuários atuais da linha de comando**

-   Na linha de comando, use: **caminho \[ msiexec /i** _para o arquivo msi atualizado_*_\]_*

**Para propagar uma atualização importante para usuários atuais de um programa**

-   Em um programa, chame [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) e especifique o caminho para o arquivo msi atualizado.

 

 



