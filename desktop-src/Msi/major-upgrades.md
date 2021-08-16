---
description: Uma atualização importante é uma atualização abrangente de um produto que precisa de uma alteração da propriedade ProductCode.
ms.assetid: 0c8f2aad-b301-4404-9051-694d97db1a8d
title: Principais atualizações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d98c6364ca0a6d9622eaacdea6cd37a2cc2dd10b057405a99577acab5102f8f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118629152"
---
# <a name="major-upgrades"></a>Principais atualizações

Uma atualização importante é uma atualização abrangente de um produto que precisa de uma alteração da propriedade [**ProductCode**](productcode.md) .

Uma atualização principal típica remove uma versão anterior de um aplicativo e instala uma nova versão. Uma atualização importante pode reorganizar a árvore de componentes de recursos. Para obter mais informações, consulte [**ProductCode**](productcode.md) e [alterando o código do produto](changing-the-product-code.md).

durante uma atualização importante usando Windows Installer, o instalador pesquisa o computador do usuário em busca de aplicativos relacionados à atualização pendente e, quando detecta um, ele recupera a versão do aplicativo instalado do registro do sistema. Em seguida, o instalador usa informações no banco de dados de atualização para determinar se o aplicativo instalado deve ser atualizado.

Para habilitar os recursos de atualização do instalador, cada pacote deve ter uma propriedade [**UpgradeCode**](upgradecode.md) e uma [tabela de atualização](upgrade-table.md). Cada produto autônomo ou conjunto de produtos deve ter seu próprio **UpgradeCode**. Para obter mais informações sobre como usar o **UpgradeCode** , consulte a seção [usando um UpgradeCode](using-an-upgradecode.md). Cada registro na tabela de atualização fornece uma combinação do código de atualização, da versão do produto e das informações de idioma usadas para identificar um conjunto de produtos afetados pela atualização. Quando a [ação FindRelatedProducts](findrelatedproducts-action.md) detecta que um produto afetado está instalado no sistema, ele anexa o código do produto a uma propriedade na coluna actionproperty da tabela de atualização. A [ação RemoveExistingProducts](removeexistingproducts-action.md) e a [ação MigrateFeatureStates](migratefeaturestates-action.md) removem ou migram os produtos listados na lista actionproperty. Os autores de pacote também podem seguir o procedimento descrito no tópico: [preparando um aplicativo para atualizações principais futuras](preparing-an-application-for-future-major-upgrades.md).

Windows Os pacotes de atualização do instalador podem ser criados de forma que as principais atualizações não serão instaladas se o usuário já tiver uma versão mais recente do aplicativo instalada. Para obter mais informações sobre como criar um pacote que não será instalado em uma versão mais recente, consulte [impedindo a instalação de um pacote antigo em uma versão mais recente](preventing-an-old-package-from-installing-over-a-newer-version.md)

> [!Note]  
> Windows O instalador usa apenas os três primeiros campos da versão do produto. Consulte a propriedade [**ProductVersion**](productversion.md) para obter descrições desses campos. Se você incluir um quarto campo em sua versão do produto, o instalador ignorará o quarto campo.

 

O método recomendado para aplicar uma atualização principal instalando o pacote completo do produto atualizado. Para obter informações sobre como aplicar uma atualização principal instalando o produto, consulte [aplicando as principais atualizações instalando o produto](applying-major-upgrades-by-installing-the-product.md).

Uma atualização importante aplicada como um [pacote de patch](patch-packages.md) para o produto não pode ser sequenciada com outras atualizações e não é um [patch desinstalável](uninstallable-patches.md). para obter informações sobre como aplicar um pacote de patch de atualização importante a um pacote de Windows Installer, confira [aplicando as principais atualizações por meio da aplicação de patch na instalação Local do produto](applying-major-upgrades-by-patching-the-local-installation-of-the-product.md). O aplicativo de uma atualização principal usando um pacote de patch não é recomendado, em vez disso, aplique atualizações importantes instalando o produto completo.

> [!Note]  
> Se um aplicativo for instalado no [contexto de instalação](installation-context.md)por usuário, qualquer atualização importante para o aplicativo também deverá ser executada usando o contexto por usuário. Se um aplicativo estiver instalado no contexto de instalação por máquina, qualquer atualização importante para o aplicativo também deverá ser executada usando o contexto por máquina. o Windows Installer não instalará atualizações importantes no contexto de instalação.

 

Você pode condicionar ações personalizadas sequenciadas após [InstallValidate](installvalidate-action.md) para lidar com as principais atualizações usando a propriedade [**UPGRADINGPRODUCTCODE**](upgradingproductcode.md) :

-   Se você quiser que uma ação personalizada seja executada durante uma desinstalação do produto, mas não durante a remoção do produto por uma atualização principal, use essa condição.

    REMOVE = "ALL" e não [ **UPGRADINGPRODUCTCODE**](upgradingproductcode.md)

-   Se você quiser que uma ação personalizada seja executada somente durante uma atualização principal, use essa condição.

    [**UPGRADINGPRODUCTCODE**](upgradingproductcode.md)

 

 



