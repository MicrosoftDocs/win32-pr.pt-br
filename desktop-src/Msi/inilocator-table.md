---
description: A tabela IniLocator contém as informações necessárias para pesquisar um arquivo ou diretório usando um arquivo .ini ou para pesquisar uma entrada específica .ini em si. O .ini arquivo deve estar presente no diretório padrão Windows Microsoft.
ms.assetid: 5a3c6077-34ef-48c8-b4e6-ecb1deb40f96
title: Tabela IniLocator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5fae106340a953c59358c7c4108991d1510d49ea6d8940bcef72c538b7165ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946536"
---
# <a name="inilocator-table"></a>Tabela IniLocator

A tabela IniLocator contém as informações necessárias para pesquisar um arquivo ou diretório usando um arquivo .ini ou para pesquisar uma entrada específica .ini em si. O .ini arquivo deve estar presente no diretório padrão Windows Microsoft.

A tabela IniLocator tem as seguintes colunas.



| Coluna      | Tipo                         | Chave | Nullable |
|-------------|------------------------------|-----|----------|
| Assinatura\_ | [Identificador](identifier.md) | Y   | N        |
| FileName    | [FileName](text.md)         | N   | N        |
| Seção     | [Text](text.md)             | N   | N        |
| Chave         | [Text](text.md)             | N   | N        |
| Campo       | [Inteiro](integer.md)       | N   | Y        |
| Tipo        | [Inteiro](integer.md)       | N   | Y        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Assinatura\_
</dt> <dd>

Uma chave externa na primeira coluna da [tabela Assinatura](signature-table.md). A Assinatura \_ representa uma assinatura exclusiva e também é a chave externa na coluna um da tabela Assinatura. Se essa assinatura estiver presente na tabela Assinatura, a pesquisa será para um arquivo. Se essa chave estiver ausente da tabela Assinatura e o valor da coluna Type for **msidbLocatorTypeRawValue**, a pesquisa será pela entrada .ini especificada pela tabela IniLocator. Caso contrário, a pesquisa será para um diretório especificado pela tabela IniLocator.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Filename
</dt> <dd>

O nome .ini arquivo.

</dd> <dt>

<span id="Section"></span><span id="section"></span><span id="SECTION"></span>Seção
</dt> <dd>

Nome da seção no .ini arquivo.

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>Chave
</dt> <dd>

Valor da chave dentro da seção.

</dd> <dt>

<span id="Field"></span><span id="field"></span><span id="FIELD"></span>Campo
</dt> <dd>

O campo na linha .ini linha. Se Field for Null ou 0, a linha inteira será lida. Esse deve ser um número não negativo.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Tipo
</dt> <dd>

Um valor que determina se o valor .ini é um local de arquivo, um local de diretório ou um valor .ini bruto.

A tabela a seguir lista valores válidos. Se ausente, Type será definido como 1.



| Constante                      | Hexadecimal | Decimal | Descrição           |
|-------------------------------|-------------|---------|-----------------------|
| **msidbLocatorTypeDirectory** | 0x000       | 0       | Um local de diretório. |
| **msidbLocatorTypeFileName**  | 0x001       | 1       | Um local do arquivo.      |
| **msidbLocatorTypeRawValue**  | 0x002       | 2       | Um valor .ini bruto.     |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Esta tabela é usada com a [tabela AppSearch](appsearch-table.md).

As colunas dessa tabela geralmente não são localizadas. Se um autor decidir pesquisar produtos em vários idiomas, poderá haver uma entrada separada incluída na tabela para cada idioma.

O texto localizado associado para exibição de progresso ou registro em log é especificado na [tabela ActionText](actiontext-table.md).

Consulte [Procurando aplicativos, arquivos, entradas do Registro ou .ini de arquivo existentes.](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

 

 



