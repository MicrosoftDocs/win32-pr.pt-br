---
description: Uma tabela de arquivos é necessária em cada módulo de mesclagem e deve ter um registro para cada arquivo que está sendo entregue ao pacote de instalação de destino pelo módulo de mesclagem.
ms.assetid: 436933c7-6e5d-4b4e-9147-c60a26871dbe
title: Criando tabelas de arquivos do módulo de mesclagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e2687ed69c1a0362f96db896a5fdf4237ac4681
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010914"
---
# <a name="authoring-merge-module-file-tables"></a>Criando tabelas de arquivos do módulo de mesclagem

Uma [tabela de arquivos](file-table.md) é necessária em cada módulo de mesclagem e deve ter um registro para cada arquivo que está sendo entregue ao pacote de instalação de destino pelo módulo de mesclagem. Quando o módulo de mesclagem é mesclado em um arquivo. msi, cada arquivo na tabela de arquivos do módulo de mesclagem é armazenado dentro de um [*arquivo de gabinete*](c-gly.md) no arquivo. msm. O nome do gabinete em um módulo de mesclagem é sempre o seguinte: MergeModule.CABinet.

Para obter mais informações, consulte [gerando MergeModule.CABarquivos de gabinete inet](generating-mergemodule-cabinet-cabinet-files.md).

-   Como os arquivos de um módulo de mesclagem são sempre armazenados dentro de um arquivo de gabinete, não é necessário definir os sinalizadores de bit **msidbFileAttributesNoncompressed** ou **MsidbFileAttributesCompressed** na coluna Attributes da [tabela File](file-table.md).
-   Os nomes dos arquivos no MergeModule.CABinet devem corresponder à chave primária na [tabela de arquivos](file-table.md)do módulo de mesclagem.

    A coluna arquivo é a chave primária da [tabela de arquivos](file-table.md) e as entradas nesse campo devem seguir a Convenção descrita em [nomear chaves primárias em bancos de dados do módulo de mesclagem](naming-primary-keys-in-merge-module-databases.md).

-   Os números de sequência de arquivos são especificados na coluna sequência da [tabela de arquivos](file-table.md).

    Os arquivos devem ser listados na [tabela de arquivos](file-table.md) do módulo de mesclagem na mesma sequência em que são armazenados MergeModule.CABinet. Os números de sequência de arquivos não precisam ser consecutivos, mas eles devem seguir a mesma sequência que os arquivos armazenados no gabinete. Por exemplo, o primeiro, o segundo e o terceiro arquivos armazenados no gabinete podem ter os números de sequência 100, 200 e 300.

-   O instalador ignora arquivos extras incluídos no MergeModule.CABinet que não estão listados na tabela de [arquivos](file-table.md).

    Um arquivo de gabinete pode conter todos os arquivos necessários para um módulo de mesclagem que dá suporte a vários idiomas usando transformações. Todos os arquivos de idioma podem receber um número de sequência exclusivo no gabinete e, em seguida, uma transformação pode adicionar ou remover arquivos da [tabela de arquivos](file-table.md) quando necessário para um idioma específico. Para obter mais informações, consulte [criando módulos de mesclagem de vários idiomas](authoring-multiple-language-merge-modules.md).

Para obter mais informações, consulte [File Table](file-table.md).

 

 



