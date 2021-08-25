---
description: Para aplicar uma atualização principal usando o instalador do Windows, o pacote de instalação do produto original deve especificar uma Propriedade UpgradeCode, descrita em Preparando um aplicativo para atualizações principais futuras, e o pacote de atualização deve ter uma tabela upgrade.
ms.assetid: 041f5bab-cb13-4e17-8465-484bcd3c6957
title: Atualizando a tabela de atualização para uma atualização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba65db43019c09e27824c54265244c65b900e4f3c94dacd24405e7fac2e0272a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809746"
---
# <a name="updating-upgrade-table-for-an-upgrade"></a>Atualizando a tabela de atualização para uma atualização

Para aplicar uma atualização principal usando o instalador do Windows, o pacote de instalação do produto original deve especificar uma propriedade [**UpgradeCode,**](upgradecode.md) descrita em Preparando um aplicativo para atualizações principais [futuras](preparing-an-application-for-future-major-upgrades.md)e o pacote de atualização deve ter uma tabela upgrade [.](upgrade-table.md)

Para obter mais informações sobre atualizações principais, consulte [Atualizações principais](major-upgrades.md) em [Patching e Atualizações](patching-and-upgrades.md).

O pacote de instalação do MNP2000.msi foi atribuído a uma propriedade [**UpgradeCode,**](upgradecode.md) conforme descrito na seção [Especificando propriedades](specifying-properties.md).

Windows O instalador aplicará a atualização se o usuário já tiver instalado as versões 1.0 a 1.4 (inclusive) do idioma inglês MNP2000. Windows O instalador migra todas as configurações de recurso do produto original para o produto atualizado. O instalador remove os arquivos que pertencem aos produtos originais que não estão sendo usados pela atualização do produto.

Se a cópia do MNP2001.msi não incluir uma Tabela de [atualização,](upgrade-table.md)use Orca ou outro editor de tabela para importar uma tabela De atualização vazia para o banco de dados do Schema.msi. O SDK fornece uma cópia de Schema.msi. Use o editor de banco de dados para MNP2001.msi e insira os dados a seguir na tabela De atualização vazia.



| Upgradecode                            | VersionMin | VersionMax | Idioma | Atributos | Remover | ActionProperty |
|----------------------------------------|------------|------------|----------|------------|--------|----------------|
| {908E378A-9551-4772-BF1D-5CFAF6FD9CB4} | 01.00.0000 | 01.40.0000 | 1046     | 769        |        | OLDAPPFOUND    |



 

[Continuar](updating-properties-for-an-upgrade.md)

 

 



