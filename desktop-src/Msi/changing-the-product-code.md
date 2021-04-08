---
description: O código do produto é um GUID que é a principal identificação de um aplicativo ou produto. Consulte códigos de produto.
ms.assetid: 4de84885-587d-405f-ba85-d62e09e8ba92
title: Alterando o código do produto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0272f1901ef60342f01f4db091e7a4e62b28e30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010912"
---
# <a name="changing-the-product-code"></a>Alterando o código do produto

O código do produto é um GUID que é a principal identificação de um aplicativo ou produto. Consulte [códigos de produto](product-codes.md).

Uma atualização que atende às diretrizes a seguir geralmente não requer uma alteração do código do produto e pode ser tratada como uma [pequena atualização](small-updates.md), ou se a versão for alterada, como uma [atualização secundária](minor-upgrades.md):

-   A atualização pode ampliar ou reduzir a árvore de componentes de recursos, mas não deve reorganizar a hierarquia existente de recursos e componentes descritos pelas tabelas [Feature](feature-table.md) e [FeatureComponents](featurecomponents-table.md) . Ele pode adicionar um novo recurso à árvore de componentes de recurso existente. Se ele remover um recurso pai, ele também deverá remover todos os recursos filho do recurso removido.
-   A atualização pode adicionar um novo componente a um recurso novo ou existente.
-   A atualização não deve alterar o código de componente de nenhum componente. Consequentemente, uma pequena atualização ou uma atualização secundária nunca deve alterar o nome do arquivo de chave de um componente, pois isso exigiria alterar o código do componente.
-   A atualização não deve alterar o nome do arquivo. msi do pacote de instalação. Em vez disso, como ele modifica o pacote, ele deve alterar o código do pacote. Observe que isso significa que a atualização pode alterar as tabelas, ações personalizadas e caixas de diálogo no arquivo. msi sem alterar o nome do arquivo.
-   A atualização pode adicionar, remover ou modificar os arquivos, as chaves do registro ou os atalhos de componentes que não são compartilhados por dois ou mais recursos. Se a atualização modificar um arquivo com versão, a versão desse arquivo deverá ser incrementada na tabela de [arquivos](file-table.md). Se a atualização remover recursos, ela também deverá atualizar as tabelas [RemoveFile](removefile-table.md) e [RemoveRegistry](removeregistry-table.md) para remover arquivos não utilizados, chaves do registro ou atalhos que já foram instalados.
-   A atualização de um componente que é compartilhado por dois ou mais recursos deve ser compatível retroativamente com todos os aplicativos e recursos que usam o componente. A atualização pode modificar o recurso de um componente compartilhado, como arquivos, entradas de registro e atalhos, desde que as alterações sejam compatíveis com versões anteriores. Não é recomendável que a atualização adicione ou remova arquivos, entradas do registro ou atalhos de um componente compartilhado.
-   Uma pequena atualização é fornecida como um [pacote de patches](patch-packages.md)Windows Installer. (Um CD-ROM completo do produto normalmente não é fornecido com uma pequena atualização).

O código do produto deve ser alterado se qualquer uma das seguintes opções for verdadeira para a atualização:

-   As instalações coexistentes de produtos originais e atualizados no mesmo sistema devem ser possíveis.
-   O nome do arquivo. msi foi alterado.
-   O código de componente de um componente existente foi alterado.
-   Um componente é removido de um recurso existente.
-   Um recurso existente foi feito em um filho de um recurso existente.
-   Um recurso filho existente foi removido de seu recurso pai.

Observe que a adição de um novo recurso filho, que consiste inteiramente em novos componentes, a um recurso existente não exige a alteração do código do produto.

Novos recursos filho podem ser criados incluindo msidbFeatureAttributesFollowParent e msidbFeatureAttributesUIDisallowAbsent no campo atributos da [tabela de recursos](feature-table.md). Se a atualização secundária apenas adicionar novos recursos filho, reinstale = ALL será suficiente para forçar a instalação dos novos recursos filho. Para obter mais informações, consulte [controlando Estados de seleção de recursos](controlling-feature-selection-states.md).

Um novo recurso filho pode estar oculto do usuário. Para sincronizar o estado de instalação de um novo recurso filho com seu recurso pai, defina os bits msidbFeatureAttributesFollowParent e msidbFeatureAttributesUIDisallowAbsent para o recurso filho.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre propriedades](about-properties.md)
</dt> <dt>

[Usando propriedades](using-properties.md)
</dt> <dt>

[Referência de propriedade](property-reference.md)
</dt> </dl>

 

 



