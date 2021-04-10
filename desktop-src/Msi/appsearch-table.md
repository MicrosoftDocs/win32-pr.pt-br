---
description: A tabela AppSearch contém as propriedades necessárias para pesquisar um arquivo que tenha uma assinatura de arquivo específica. A tabela AppSearch também pode ser usada para definir uma propriedade para o valor existente de um registro ou de uma entrada de arquivo. ini.
ms.assetid: d560096f-6baa-4fea-8786-f4e3d5ee6bf4
title: Tabela AppSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9419a768a51364b4f22444288e6728a87289aa0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169205"
---
# <a name="appsearch-table"></a>Tabela AppSearch

A tabela AppSearch contém as propriedades necessárias para pesquisar um arquivo que tenha uma assinatura de arquivo específica. A tabela AppSearch também pode ser usada para definir uma propriedade para o valor existente de um registro ou de uma entrada de arquivo. ini.

A tabela AppSearch tem as colunas a seguir.



| Coluna      | Tipo                         | Chave | Nullable |
|-------------|------------------------------|-----|----------|
| Propriedade    | [Identificador](identifier.md) | S   | N        |
| Signature\_ | [Identificador](identifier.md) | S   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Propriedade
</dt> <dd>

A execução da ação [AppSearch](appsearch-action.md) define essa propriedade como o local do arquivo indicado pela coluna de assinatura \_ . Essa propriedade será definida se a assinatura de arquivo existir no computador do usuário. As propriedades usadas nesta coluna devem ser propriedades [públicas](public-properties.md) e ter um identificador que não contenha letras minúsculas.

A propriedade listada no campo de propriedade pode ser inicializada na tabela de [Propriedades](property-table.md) ou em uma linha de comando. Se a ação [AppSearch](appsearch-action.md) localizar a assinatura, o instalador substituirá o valor da propriedade Initialized pelo valor encontrado. Se a assinatura não for encontrada, o valor da propriedade inicial será usado. Se a propriedade nunca foi inicializada, a propriedade só será definida se a assinatura for encontrada. Caso contrário, a propriedade será indefinida.

</dd> <dt>

<span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_
</dt> <dd>

A \_ coluna assinatura contém um identificador exclusivo chamado assinatura e também uma chave externa nas tabelas [RegLocator](reglocator-table.md), [IniLocator](inilocator-table.md), [CompLocator](complocator-table.md)e [DrLocator](drlocator-table.md) . Ao pesquisar um arquivo, o valor nessa coluna também deve ser uma chave estrangeira na tabela de [assinatura](signature-table.md) . Se o valor nessa coluna não estiver listado na tabela de assinatura, o instalador determinará que a pesquisa é para um diretório.

</dd> </dl>

## <a name="remarks"></a>Comentários

A ação [AppSearch](appsearch-action.md) em [*tabelas de sequência*](s-gly.md) processa as informações nesta tabela. Para obter informações sobre como usar *tabelas de sequência*, consulte [usando uma tabela de sequência](using-a-sequence-table.md).

A ação [AppSearch](appsearch-action.md) pesquisa assinaturas usando a tabela [CompLocator](complocator-table.md) primeiro, a tabela [RegLocator](reglocator-table.md) segundo, a tabela [IniLocator](inilocator-table.md) terceira e, por fim, a tabela [DrLocator](drlocator-table.md) . As assinaturas de arquivo são listadas na tabela de [assinatura](signature-table.md) . Uma assinatura que não está na tabela de assinatura denota um diretório e a ação define a propriedade como o caminho do diretório para essa assinatura.

Consulte [pesquisando aplicativos, arquivos, entradas de registro ou entradas de arquivo. ini existentes](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE52](ice52.md)  
[ICE88](ice88.md)  
</dl>

 

 



