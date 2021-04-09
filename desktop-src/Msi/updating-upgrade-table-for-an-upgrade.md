---
description: Para aplicar uma atualização principal usando Windows Installer, o pacote de instalação do produto original deve especificar uma propriedade UpgradeCode, descrita em preparando um aplicativo para atualizações principais futuras, e o pacote de atualização deve ter uma tabela de atualização.
ms.assetid: 041f5bab-cb13-4e17-8465-484bcd3c6957
title: Atualizando a tabela de atualização para uma atualização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1b4c2cc2b650d49fb4ba40f97d69ed84911273
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091394"
---
# <a name="updating-upgrade-table-for-an-upgrade"></a>Atualizando a tabela de atualização para uma atualização

Para aplicar uma atualização principal usando Windows Installer, o pacote de instalação do produto original deve especificar uma propriedade [**UpgradeCode**](upgradecode.md) , descrita em [preparando um aplicativo para atualizações principais futuras](preparing-an-application-for-future-major-upgrades.md), e o pacote de atualização deve ter uma [tabela de atualização](upgrade-table.md).

Para obter mais informações sobre as principais atualizações, consulte [principais atualizações](major-upgrades.md) em [aplicação de patches e atualizações](patching-and-upgrades.md).

O pacote de instalação do MNP2000.msi foi atribuído a uma propriedade [**UpgradeCode**](upgradecode.md) , conforme descrito na seção [especificando propriedades](specifying-properties.md).

Windows Installer aplicará a atualização se o usuário já tiver instalado o 1,0 para versões 1,4 (inclusivo) do idioma inglês MNP2000. Windows Installer migra todas as configurações de recurso do produto original para o produto atualizado. O instalador remove os arquivos que pertencem aos produtos originais que não estão sendo usados pela atualização do produto.

Se sua cópia de MNP2001.msi não incluir uma [tabela de atualização](upgrade-table.md), use Orca ou outro editor de tabela, para importar uma tabela de atualização vazia para o banco de dados do Schema.msi. O SDK fornece uma cópia de Schema.msi. Use o editor de banco de dados para abrir MNP2001.msi e insira os dados a seguir na tabela de atualização vazia.



| UpgradeCode                            | VersionMin | VersionMax | Idioma | Atributos | Remover | Açãoproperty |
|----------------------------------------|------------|------------|----------|------------|--------|----------------|
| {908E378A-9551-4772-BF1D-5CFAF6FD9CB4} | 01.00.0000 | 01.40.0000 | 1046     | 769        |        | OLDAPPFOUND    |



 

[Continuar](updating-properties-for-an-upgrade.md)

 

 



