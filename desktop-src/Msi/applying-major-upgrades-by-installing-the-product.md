---
description: Uma atualização importante pode ser aplicada instalando o novo pacote de instalação para o produto atualizado.
ms.assetid: f4fb28be-5ec0-4eac-9d4d-eccf5bd61ac4
title: Aplicando as principais atualizações instalando o produto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7619b2ae2b8e1f10cac2fcfae61dde0c6dbba5d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751659"
---
# <a name="applying-major-upgrades-by-installing-the-product"></a>Aplicando as principais atualizações instalando o produto

Uma atualização importante pode ser aplicada instalando o novo pacote de instalação para o produto atualizado. Como as atualizações principais recebem um código de produto diferente do produto original, a instalação da atualização deve ser tratada como uma instalação de um novo produto. A atualização pode ser simplesmente instalada como outro produto. Você pode fazer com que o novo pacote de instalação manipule a remoção do produto antigo, incluindo a [tabela de atualização](upgrade-table.md) e a ação [FindRelatedProducts](findrelatedproducts-action.md) e a [ação RemoveExistingProducts](removeexistingproducts-action.md).

**Para propagar uma atualização principal para os usuários atuais da linha de comando**

-   Na linha de comando, use: **msiexec/i \[** _caminho para o arquivo MSI atualizado_*_\]_*

**Para propagar uma atualização principal para os usuários atuais de um programa**

-   Em um programa, chame [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) e especifique o caminho para o arquivo MSI atualizado.

 

 



