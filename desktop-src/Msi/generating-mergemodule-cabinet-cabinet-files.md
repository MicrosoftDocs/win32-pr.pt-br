---
description: Cada arquivo que é entregue ao pacote de instalação de destino pelo módulo de mesclagem deve ser armazenado dentro de um arquivo de gabinete inserido como um fluxo dentro do arquivo. msm. O nome desse gabinete é sempre MergeModule.CABinet.
ms.assetid: 884df249-977e-4e8e-8978-15331a7c1d8a
title: Gerando MergeModule.CABarquivos de gabinete inet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 962cf46b95db1fe186878d23a7cc7fcd1b91d3b2d202a85741eee7ef1c2bc7e7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649640"
---
# <a name="generating-mergemodulecabinet-cabinet-files"></a>Gerando MergeModule.CABarquivos de gabinete inet

Cada arquivo que é entregue ao pacote de instalação de destino pelo módulo de mesclagem deve ser armazenado dentro de um arquivo de gabinete inserido como um fluxo dentro do arquivo. msm. O nome desse gabinete é sempre MergeModule.CABinet.

Os nomes dos arquivos no MergeModule.CABinet devem corresponder às chaves primárias usadas na [tabela de arquivos](file-table.md) do módulo de mesclagem e devem aderir à Convenção descrita em [nomear chaves primárias em bancos de dados do módulo de mesclagem](naming-primary-keys-in-merge-module-databases.md).

O instalador ignora arquivos extras incluídos no MergeModule.CABinet que não estão listados na [tabela de arquivos](file-table.md)do módulo de mesclagem. Os números de sequência de arquivos especificados na tabela de arquivos não precisam ser consecutivos, mas eles devem seguir a mesma sequência que os arquivos armazenados dentro de MergeModule.CABinet. Para obter mais informações, consulte [criando tabelas de arquivos do módulo de mesclagem](authoring-merge-module-file-tables.md).

Isso significa que um único arquivo de gabinete pode conter todos os arquivos necessários para que um módulo de mesclagem ofereça suporte a vários idiomas. Todos os arquivos de idioma podem receber números de sequência exclusivos no gabinete e, em seguida, uma transformação de idioma pode ser usada para adicionar ou remover arquivos da tabela de arquivos para obter um módulo de mesclagem para um idioma específico. Para obter detalhes, consulte [criando módulos de mesclagem de vários idiomas](authoring-multiple-language-merge-modules.md).

MergeModule.CABo inet pode ser adicionado ao módulo de mesclagem abrindo uma [ \_ tabela de Fluxos](-streams-table.md)temporária. por exemplo, a ferramenta Msidb.exe fornecida com o SDK do Windows Installer pode ser usada para adicionar o MergeModule.CABinet ao módulo de mesclagem. Para obter mais informações, consulte [incluindo um arquivo de gabinete em uma instalação](including-a-cabinet-file-in-an-installation.md).

 

 



