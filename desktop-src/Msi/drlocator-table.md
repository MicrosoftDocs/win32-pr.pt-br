---
description: A tabela DrLocator contém as informações necessárias para localizar um arquivo ou diretório pesquisando a árvore de diretórios.
ms.assetid: 2b779ff7-f410-4af0-899d-4432b015d526
title: Tabela DrLocator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78df5a5af83a18a14027b88033e977b2c63d2027
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752459"
---
# <a name="drlocator-table"></a>Tabela DrLocator

A tabela DrLocator contém as informações necessárias para localizar um arquivo ou diretório pesquisando a árvore de diretórios.

A tabela DrLocator tem as colunas a seguir.



| Coluna      | Tipo                         | Chave | Nullable |
|-------------|------------------------------|-----|----------|
| Signature\_ | [Identificador](identifier.md) | S   | N        |
| Pai      | [Identificador](identifier.md) | S   | S        |
| Caminho        | [AnyPath](anypath.md)       | S   | S        |
| Profundidade       | [Inteiro](integer.md)       | N   | S        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_
</dt> <dd>

A \_ coluna de assinatura é uma chave externa para a primeira coluna da [tabela de assinatura](signature-table.md). Esse campo pode representar uma assinatura de arquivo exclusiva listada na tabela de assinatura. Se o valor nessa coluna estiver ausente da tabela de assinatura, a pesquisa será considerada para um diretório apontado pela tabela DrLocator.

</dd> <dt>

<span id="Parent"></span><span id="parent"></span><span id="PARENT"></span>Primária
</dt> <dd>

Essa coluna é a assinatura do diretório pai do arquivo ou diretório na coluna de assinatura \_ . Se esse campo for nulo e a coluna de caminho não expandir para um caminho completo, todas as unidades fixas do sistema do usuário serão pesquisadas usando o caminho.

Esse campo é uma chave em uma das tabelas a seguir: as tabelas [RegLocator](reglocator-table.md), [IniLocator](inilocator-table.md), [CompLocator](complocator-table.md)ou DrLocator.

</dd> <dt>

<span id="Path"></span><span id="path"></span><span id="PATH"></span>Multi-Path
</dt> <dd>

A coluna Path contém o caminho no sistema do usuário. Este é um caminho completo ou um subcaminho relativo abaixo do diretório especificado na coluna pai. Consulte as restrições no tipo de dados [AnyPath](anypath.md) .

</dd> <dt>

<span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>Detalhado
</dt> <dd>

A profundidade abaixo do caminho que o instalador pesquisa pelo arquivo ou diretório especificado na \_ coluna assinatura. O valor usado no campo profundidade baseia-se em zero. Por exemplo, se o campo caminho for c:/Arquivos de programas/bin, a coluna profundidade deverá ser definida como 0 ou maior para detectar um arquivo localizado dentro da pasta bin. Se o campo de profundidade estiver vazio, presume-se que a profundidade seja zero.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa tabela é usada com a [tabela AppSearch](appsearch-table.md).

As colunas desta tabela geralmente não são localizadas. Se um autor decidir procurar produtos em vários idiomas, deverá haver uma entrada separada incluída na tabela para cada idioma.

Consulte [pesquisando aplicativos, arquivos, entradas de registro ou entradas de arquivo. ini existentes](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
</dl>

 

 



