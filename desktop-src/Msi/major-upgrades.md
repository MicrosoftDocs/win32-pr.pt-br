---
description: Uma atualização importante é uma atualização abrangente de um produto que precisa de uma alteração da propriedade ProductCode.
ms.assetid: 0c8f2aad-b301-4404-9051-694d97db1a8d
title: Atualizações principais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d98c6364ca0a6d9622eaacdea6cd37a2cc2dd10b057405a99577acab5102f8f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118629152"
---
# <a name="major-upgrades"></a>Atualizações principais

Uma atualização importante é uma atualização abrangente de um produto que precisa de uma alteração da [**propriedade ProductCode.**](productcode.md)

Uma atualização principal típica remove uma versão anterior de um aplicativo e instala uma nova versão. Uma atualização importante pode reorganizar a árvore de componentes do recurso. Para obter mais informações, consulte [**ProductCode**](productcode.md) e [Alterando o código do produto](changing-the-product-code.md).

Durante uma atualização principal usando o Windows Installer, o instalador pesquisa no computador do usuário aplicativos relacionados à atualização pendente e, quando detecta um, ele recupera a versão do aplicativo instalado do registro do sistema. Em seguida, o instalador usa informações no banco de dados de atualização para determinar se o aplicativo instalado deve ser atualizado.

Para habilitar os recursos de atualização do instalador, cada pacote deve ter uma [**Propriedade UpgradeCode**](upgradecode.md) e uma [Tabela de Atualização](upgrade-table.md). Cada produto autônomo ou pacote de produtos deve ter seu **próprio UpgradeCode.** Para obter mais informações sobre como usar **o UpgradeCode,** consulte a seção [Usando um UpgradeCode](using-an-upgradecode.md). Cada registro na tabela Atualizar fornece uma combinação do código de atualização, da versão do produto e das informações de idioma usadas para identificar um conjunto de produtos afetados pela atualização. Quando a [Ação FindRelatedProducts](findrelatedproducts-action.md) detecta que um produto afetado está instalado no sistema, ele anexa o código do produto a uma propriedade na coluna ActionProperty da tabela Upgrade. A [ação RemoveExistingProducts](removeexistingproducts-action.md) e a [Ação MigrateFeatureStates](migratefeaturestates-action.md) removem ou migram os produtos listados na lista ActionProperty. Os autores de pacote também podem seguir o procedimento descrito no tópico: Preparando [um aplicativo para atualizações principais futuras.](preparing-an-application-for-future-major-upgrades.md)

Windows Os pacotes de atualização do instalador podem ser autorados de forma que as atualizações principais não serão instaladas se o usuário já tiver uma versão mais recente do aplicativo instalada. Para obter mais informações sobre como autor de um pacote que não será instalado em uma versão mais recente, consulte Impedindo que um pacote antigo seja instalado em uma [versão mais recente](preventing-an-old-package-from-installing-over-a-newer-version.md)

> [!Note]  
> Windows O instalador usa apenas os três primeiros campos da versão do produto. Consulte [**Propriedade ProductVersion**](productversion.md) para ver descrições desses campos. Se você incluir um quarto campo em sua versão do produto, o instalador ignorará o quarto campo.

 

O método recomendado para aplicar uma atualização principal instalando o pacote completo para o produto atualizado. Para obter informações sobre como aplicar uma atualização principal instalando o produto, consulte Aplicando atualizações [principais instalando o produto](applying-major-upgrades-by-installing-the-product.md).

Uma atualização importante aplicada como um [Pacote de Patch](patch-packages.md) para o produto não pode ser sequenciada com outras atualizações e não é um patch [desinstalável.](uninstallable-patches.md) Para obter informações sobre como aplicar um pacote de patch de atualização principal a um pacote do Windows Installer, consulte Aplicando atualizações principais aplicando [patches](applying-major-upgrades-by-patching-the-local-installation-of-the-product.md)na instalação local do produto . A aplicação de uma atualização principal usando um pacote de patch não é recomendada, em vez disso, aplique atualizações principais instalando o produto completo.

> [!Note]  
> Se um aplicativo estiver instalado no contexto de instalação por [usuário,](installation-context.md)qualquer atualização principal para o aplicativo também deverá ser executada usando o contexto por usuário. Se um aplicativo estiver instalado no contexto de instalação por computador, qualquer atualização principal para o aplicativo também deverá ser executada usando o contexto por computador. O Windows instalador não instalará atualizações principais no contexto de instalação.

 

Você pode condicionar ações personalizadas que são sequenciadas após [InstallValidate](installvalidate-action.md) para lidar com atualizações principais usando a [**propriedade UPGRADINGPRODUCTCODE:**](upgradingproductcode.md)

-   Se você quiser que uma ação personalizada seja executado durante uma desinstalação do produto, mas não durante a remoção do produto por uma atualização principal, use essa condição.

    REMOVE="ALL" E NOT [ **UPGRADINGPRODUCTCODE**](upgradingproductcode.md)

-   Se você quiser que uma ação personalizada seja executado somente durante uma atualização principal, use essa condição.

    [**UPGRADINGPRODUCTCODE**](upgradingproductcode.md)

 

 



