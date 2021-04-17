---
description: Os autores de pacotes de instalação devem incluir a atualização de informações em seus arquivos. msi para garantir que seu pacote de instalação possa aproveitar a funcionalidade completa de atualização disponível com o Microsoft Windows Installer.
ms.assetid: 88bb2709-a1bf-4140-a145-ae6bee85dde1
title: Preparando um aplicativo para atualizações principais futuras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1e0dc9ccbee10becc39274e91d2fedeb3707028
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748143"
---
# <a name="preparing-an-application-for-future-major-upgrades"></a>Preparando um aplicativo para atualizações principais futuras

Os autores de pacotes de instalação devem incluir a atualização de informações em seus arquivos. msi para garantir que seu pacote de instalação possa aproveitar a funcionalidade completa de atualização disponível com o Microsoft Windows Installer.

Cada aplicativo, ou conjunto de aplicativos, deve ser atribuído a uma propriedade [**UpgradeCode**](upgradecode.md) , uma propriedade [**ProductVersion**](productversion.md) e uma propriedade [**ProductLanguage**](productlanguage.md) . A propriedade [**UpgradeCode**](upgradecode.md) indica uma família de aplicativos relacionados que consiste em versões diferentes e versões de idioma diferentes do mesmo produto. Para obter mais informações sobre como usar a propriedade [**UpgradeCode**](upgradecode.md) , consulte [usando um UpgradeCode](using-an-upgradecode.md).

**Preparando um aplicativo para atualizações principais futuras**

1.  Determine um novo valor de código de pacote para o aplicativo. Para obter mais informações sobre códigos de pacote, consulte [Package codes](package-codes.md). Insira o novo código do pacote na propriedade [**Resumo do número de revisão**](revision-number-summary.md) do fluxo de informações de [Resumo](summary-information-stream.md).
2.  Determine uma nova propriedade [**ProductCode**](productcode.md) para o aplicativo. Consulte [alterando o código do produto](changing-the-product-code.md) para obter mais informações. Insira o [**ProductCode**](productcode.md) e seu valor na [tabela de propriedades](property-table.md).
3.  Determine a versão do aplicativo e a propriedade [**ProductVersion**](productversion.md) . O [**ProductVersion**](productversion.md) deve aumentar com cada nova versão do aplicativo. Observe que o instalador usa apenas os três primeiros campos da versão do produto. Se você incluir um quarto campo em sua versão do produto, o instalador ignorará o quarto campo. Insira [**ProductVersion**](productversion.md) e seu valor na tabela de propriedades.
4.  Determine o idioma do pacote e a propriedade [**ProductLanguage**](productlanguage.md) . O valor dessa propriedade deve ser um identificador de idioma numérico (LANGid). Insira [**ProductLanguage**](productlanguage.md) e seu valor na [tabela de propriedades](property-table.md). Observe que a [ação FindRelatedProducts](findrelatedproducts-action.md) usa o idioma retornado por [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa). Para que o FindRelatedProducts funcione corretamente, o autor do pacote deve ter certeza de que a propriedade [**ProductLanguage**](productlanguage.md) está definida na tabela de propriedades para um idioma que também está listado na propriedade [**Summary do modelo**](template-summary.md) .
5.  Se você estiver criando um pacote de instalação para a primeira versão do seu produto, use um novo [**UpgradeCode**](upgradecode.md). Se o seu pacote for destinado a uma versão mais recente de um produto existente, ou for a mesma versão de um produto existente em um idioma diferente, use o mesmo [**UpgradeCode**](upgradecode.md) que o produto existente. Dois produtos com o mesmo [**ProductVersion**](productversion.md) e o mesmo [**ProductLanguage**](productlanguage.md) podem ter o mesmo [**UpgradeCode**](upgradecode.md), a menos que um seja uma [pequena atualização](small-updates.md) do outro.
6.  O [**UpgradeCode**](upgradecode.md) tem o formato de um [GUID](guid.md). Insira o GUID [**UpgradeCode**](upgradecode.md) na tabela de propriedades.

Para obter mais informações, consulte [impedindo que um pacote antigo seja instalado em uma versão mais recente](preventing-an-old-package-from-installing-over-a-newer-version.md).

 

 



