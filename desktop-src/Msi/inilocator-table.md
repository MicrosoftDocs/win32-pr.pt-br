---
description: A tabela IniLocator contém as informações necessárias para pesquisar um arquivo ou diretório usando um arquivo. ini ou para procurar uma própria entrada. ini em particular. O arquivo. ini deve estar presente no diretório padrão do Microsoft Windows.
ms.assetid: 5a3c6077-34ef-48c8-b4e6-ecb1deb40f96
title: Tabela IniLocator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89583a2d69fd88dd4b5624920e2374aa7e203103
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105747977"
---
# <a name="inilocator-table"></a>Tabela IniLocator

A tabela IniLocator contém as informações necessárias para pesquisar um arquivo ou diretório usando um arquivo. ini ou para procurar uma própria entrada. ini em particular. O arquivo. ini deve estar presente no diretório padrão do Microsoft Windows.

A tabela IniLocator tem as colunas a seguir.



| Coluna      | Tipo                         | Chave | Nullable |
|-------------|------------------------------|-----|----------|
| Signature\_ | [Identificador](identifier.md) | S   | N        |
| FileName    | [FileName](text.md)         | N   | N        |
| Seção     | [Text](text.md)             | N   | N        |
| Chave         | [Text](text.md)             | N   | N        |
| Campo       | [Inteiro](integer.md)       | N   | Y        |
| Tipo        | [Inteiro](integer.md)       | N   | S        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signature\_
</dt> <dd>

Uma chave externa na primeira coluna da tabela de [assinatura](signature-table.md). A assinatura \_ representa uma assinatura exclusiva e também é a chave externa na coluna um da tabela de assinatura. Se essa assinatura estiver presente na tabela de assinatura, a pesquisa será para um arquivo. Se essa chave estiver ausente da tabela de assinatura e o valor da coluna de tipo for **msidbLocatorTypeRawValue**, a pesquisa será para a entrada. ini especificada pela tabela IniLocator. Caso contrário, a pesquisa será para um diretório especificado pela tabela IniLocator.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Nome do arquivo
</dt> <dd>

O nome do arquivo. ini.

</dd> <dt>

<span id="Section"></span><span id="section"></span><span id="SECTION"></span>Section
</dt> <dd>

Nome da seção dentro do arquivo. ini.

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Chaves
</dt> <dd>

Valor da chave na seção.

</dd> <dt>

<span id="Field"></span><span id="field"></span><span id="FIELD"></span>Campo
</dt> <dd>

O campo na linha. ini. Se o campo for nulo ou 0, a linha inteira será lida. Este deve ser um número não negativo.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Escreva
</dt> <dd>

Um valor que determina se o valor de. ini é um local de arquivo, um local de diretório ou um valor RAW. ini.

A tabela a seguir lista os valores válidos. Se estiver ausente, o tipo será definido como 1.



| Constante                      | Hexadecimal | Decimal | Descrição           |
|-------------------------------|-------------|---------|-----------------------|
| **msidbLocatorTypeDirectory** | 0x000       | 0       | Um local do diretório. |
| **msidbLocatorTypeFileName**  | 0x001       | 1       | Um local de arquivo.      |
| **msidbLocatorTypeRawValue**  | 0x002       | 2       | Um valor RAW. ini.     |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa tabela é usada com a [tabela AppSearch](appsearch-table.md).

As colunas desta tabela geralmente não são localizadas. Se um autor decidir procurar produtos em vários idiomas, poderá haver uma entrada separada incluída na tabela para cada idioma.

O texto localizado associado para exibição de progresso ou registro em log está especificado na [tabela ActionText](actiontext-table.md).

Consulte [pesquisando aplicativos, arquivos, entradas de registro ou entradas de arquivo. ini existentes](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

 

 



