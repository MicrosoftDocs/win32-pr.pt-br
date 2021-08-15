---
description: A tabela DrLocator contém as informações necessárias para encontrar um arquivo ou diretório pesquisando a árvore de diretórios.
ms.assetid: 2b779ff7-f410-4af0-899d-4432b015d526
title: Tabela DrLocator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe1765c7b8f5c38d5701c4c401eb333c7db6a7c403689b8c3100d55b5e51e28e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378320"
---
# <a name="drlocator-table"></a>Tabela DrLocator

A tabela DrLocator contém as informações necessárias para encontrar um arquivo ou diretório pesquisando a árvore de diretórios.

A tabela DrLocator tem as seguintes colunas.



| Coluna      | Tipo                         | Chave | Nullable |
|-------------|------------------------------|-----|----------|
| Assinatura\_ | [Identificador](identifier.md) | Y   | N        |
| Pai      | [Identificador](identifier.md) | Y   | Y        |
| Caminho        | [AnyPath](anypath.md)       | Y   | Y        |
| Profundidade       | [Inteiro](integer.md)       | N   | Y        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Assinatura\_
</dt> <dd>

A coluna \_ Assinatura é uma chave externa para a primeira coluna da tabela [Assinatura](signature-table.md). Esse campo pode representar uma assinatura de arquivo exclusiva listada na tabela Assinatura. Se o valor nesta coluna estiver ausente da tabela Assinatura, supõe-se que a pesquisa seja para um diretório apontado pela tabela DrLocator.

</dd> <dt>

<span id="Parent"></span><span id="parent"></span><span id="PARENT"></span>Pai
</dt> <dd>

Essa coluna é a assinatura do diretório pai do arquivo ou diretório na coluna \_ Assinatura. Se esse campo for nulo e a coluna Caminho não se expandir para um caminho completo, todas as unidades fixas do sistema do usuário serão pesquisadas usando o Caminho.

Esse campo é uma chave em uma das tabelas a seguir: [o RegLocator](reglocator-table.md), [o IniLocator,](inilocator-table.md)o [CompLocator](complocator-table.md)ou as tabelas DrLocator.

</dd> <dt>

<span id="Path"></span><span id="path"></span><span id="PATH"></span>Caminho
</dt> <dd>

A coluna Caminho contém o caminho no sistema do usuário. Esse é um caminho completo ou um subcaminho relativo abaixo do diretório especificado na coluna Pai. Confira as restrições no [tipo de dados AnyPath.](anypath.md)

</dd> <dt>

<span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>Profundidade
</dt> <dd>

A profundidade abaixo do caminho que o instalador pesquisa pelo arquivo ou diretório especificado na coluna \_ Assinatura. O valor usado no campo Profundidade é baseado em zero. Por exemplo, se o campo Caminho for c:/Arquivos de Programas/bin, a coluna Profundidade deverá ser definida como 0 ou superior, para detectar um arquivo localizado dentro do compartimento de pasta. Se o campo Profundidade estiver vazio, a profundidade será assumida como zero.

</dd> </dl>

## <a name="remarks"></a>Comentários

Esta tabela é usada com a [tabela AppSearch](appsearch-table.md).

As colunas dessa tabela geralmente não são localizadas. Se um autor decidir pesquisar produtos em vários idiomas, deverá haver uma entrada separada incluída na tabela para cada idioma.

Consulte [Procurando aplicativos, arquivos, entradas do Registro ou .ini de arquivo existentes.](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
</dl>

 

 



