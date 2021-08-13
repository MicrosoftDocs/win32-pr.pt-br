---
description: A tabela Assinatura contém as informações que identificam exclusivamente uma assinatura de arquivo. Para obter mais informações sobre assinaturas, consulte Assinaturas digitais e Windows Instalador.
ms.assetid: 4780356f-e02a-45d9-883c-4f84867dbdea
title: Tabela de assinatura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5ddda5c501b24e12498f356c10a1aa2a3549426daca5e4cc3c19c1f62ed04cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118624643"
---
# <a name="signature-table"></a>Tabela de assinatura

A tabela Assinatura contém as informações que identificam exclusivamente uma assinatura de arquivo. Para obter mais informações sobre assinaturas, [consulte Assinaturas digitais e Windows Instalador .](digital-signatures-and-windows-installer.md)

A tabela Assinatura tem as seguintes colunas.



| Coluna     | Tipo                               | Chave | Nullable |
|------------|------------------------------------|-----|----------|
| Assinatura  | [Identificador](identifier.md)       | Y   | N        |
| FileName   | [Text](text.md)                   | N   | N        |
| MinVersion | [Text](text.md)                   | N   | Y        |
| Maxversion | [Text](text.md)                   | N   | Y        |
| Minsize    | [DoubleInteger](doubleinteger.md) | N   | Y        |
| MaxSize    | [DoubleInteger](doubleinteger.md) | N   | Y        |
| Mindate    | [DoubleInteger](doubleinteger.md) | N   | Y        |
| Maxdate    | [DoubleInteger](doubleinteger.md) | N   | Y        |
| Idiomas  | [Text](text.md)                   | N   | Y        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>Assinatura
</dt> <dd>

A coluna Assinatura é uma assinatura de arquivo exclusiva.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Filename
</dt> <dd>

O nome do arquivo.

</dd> <dt>

<span id="MinVersion"></span><span id="minversion"></span><span id="MINVERSION"></span>MinVersion
</dt> <dd>

A versão mínima do arquivo, com uma comparação de idioma. Se esse campo for especificado, o arquivo deverá ter uma versão que seja pelo menos igual a MinVersion. Se o arquivo tiver uma versão igual ao valor do campo MinVersion, mas o idioma especificado na coluna Idiomas for diferente, o arquivo não atenderá aos critérios de filtro de assinatura.

> [!Note]  
> O idioma especificado na coluna Idiomas é usado na comparação e não há como ignorar o idioma. Se você quiser que um arquivo atender ao requisito de campo MinVersion, independentemente do idioma, deverá inserir um valor no campo MinVersion que seja um valor menor que o valor real. Por exemplo, se a versão mínima do filtro for 2.0.2600.1183, use 2.0.2600.1182 para encontrar o arquivo sem corresponder às informações de idioma.

 

</dd> <dt>

<span id="MaxVersion"></span><span id="maxversion"></span><span id="MAXVERSION"></span>Maxversion
</dt> <dd>

A versão máxima do arquivo. Se esse campo for especificado, o arquivo deverá ter uma versão que seja no máximo igual a MaxVersion.

</dd> <dt>

<span id="MinSize"></span><span id="minsize"></span><span id="MINSIZE"></span>Minsize
</dt> <dd>

O tamanho mínimo do arquivo. Se esse campo for especificado, o arquivo em inspeção deverá ter um tamanho que seja pelo menos igual a MinSize. Esse deve ser um número não negativo.

</dd> <dt>

<span id="MaxSize"></span><span id="maxsize"></span><span id="MAXSIZE"></span>Maxsize
</dt> <dd>

O tamanho máximo do arquivo. Se esse campo for especificado, o arquivo em inspeção deverá ter um tamanho que seja no máximo igual a MaxSize. Esse deve ser um número não negativo.

</dd> <dt>

<span id="MinDate"></span><span id="mindate"></span><span id="MINDATE"></span>Mindate
</dt> <dd>

A data e a hora mínimas de modificação do arquivo. Se esse campo for especificado, o arquivo em inspeção deverá ter uma data e hora de modificação que seja pelo menos igual a MinDate. Esse deve ser um número não negativo. O formato desse campo é dois valores empacotados de 16 bits do tipo **WORD.** O valor word de **ordem** alta especifica a data no formato de data do MS-DOS. O valor word de **ordem** baixa especifica a hora no formato de hora do MS-DOS. Um valor de 0 para o valor de hora representa meia-noite. Consulte a seção Comentários.

</dd> <dt>

<span id="MaxDate"></span><span id="maxdate"></span><span id="MAXDATE"></span>Maxdate
</dt> <dd>

A data máxima de criação do arquivo. Se esse campo for especificado, o arquivo em inspeção deverá ter uma data de criação que seja no máximo igual a MaxDate. Esse deve ser um número não negativo. O formato desse campo é dois valores empacotados de 16 bits do tipo **WORD.** O valor word de **ordem** alta especifica a data no formato de data do MS-DOS. O valor word de **ordem** baixa especifica a hora no formato de hora do MS-DOS. Um valor de 0 para o valor de hora representa meia-noite. Consulte a seção Comentários.

</dd> <dt>

<span id="Languages"></span><span id="languages"></span><span id="LANGUAGES"></span>Idiomas
</dt> <dd>

Os idiomas com suporte do arquivo.

</dd> </dl>

## <a name="remarks"></a>Comentários

Esta tabela é usada com a [tabela AppSearch](appsearch-table.md).

A assinatura é pesquisada usando a tabela [RegLocator](reglocator-table.md), a tabela [IniLocator](inilocator-table.md), a tabela [CompLocator](complocator-table.md)e a [tabela DrLocator](drlocator-table.md). As colunas dessa tabela geralmente não são localizadas. Se um autor decidir pesquisar produtos em vários idiomas, poderá haver uma entrada separada incluída na tabela para cada idioma.

A tabela Assinatura geralmente segue as regras Windows de versão do [arquivo do instalador.](file-versioning-rules.md) Os idiomas especificados na coluna Idiomas da tabela Assinatura não são avaliados, a menos que as versões de arquivo sejam equivalentes. A coluna Idiomas garantirá que um arquivo seja de um idioma específico se ele for da versão solicitada. Não há nenhum método disponível para ignorar a coluna Idiomas. Um valor NULL inserido na coluna Idiomas é tratado como um arquivo sem um idioma e não combina a assinatura de arquivo de um arquivo com um idioma que aparece na tabela Assinatura. O exemplo a seguir pesquisa uma versão específica do MSI.DLL.

[Tabela DrLocator](drlocator-table.md)

| Signature\_ | Pai | Caminho                  | Profundidade |
|-------------|--------|-----------------------|-------|
| MsiDll      | nulo | c: \\ Windows \\ System32 | 0     |



 

[Tabela AppSearch](appsearch-table.md)



| Propriedade | Signature\_ |
|----------|-------------|
| MSIDLL   | MsiDll      |



 

Tabela de assinatura



| Assinatura | FileName | MinVersion    | MaxVersion | MinSize | MaxSize | Lembre-se | MaxDate | Idiomas |
|-----------|----------|---------------|------------|---------|---------|---------|---------|-----------|
| MsiDll    | msi.dll  | 2.0.2600.1106 | nulo     | nulo  | nulo  | nulo  | nulo  | 0         |



 

nesse caso, e no Windows XP SP1, a [ação AppSearch](appsearch-action.md) define MSIDLL como c: \\ Windows \\ system32 \\msi.dll porque MSI.DLL é um arquivo de idioma neutro. Se o valor da coluna languages for alterado de 0 para 1033, a ação AppSearch falhará ao localizar o msi.dll correspondente e a propriedade MSIDLL será indefinida.

Você não pode usar a tabela de assinatura para consultar apenas os idiomas. Para pesquisar versões de idioma diferentes de um arquivo, você deve ter uma entrada separada na tabela de assinatura para cada versão de idioma. Se vários idiomas forem fornecidos na coluna idiomas, a pesquisa será para um arquivo que dá suporte a todos esses idiomas.

O formato das colunas mental e MaxDate são dois valores de 16 bits empacotados do tipo **Word**.

**Palavra** de data



| Bits | Conteúdo                                             |
|------|-----------------------------------------------------|
| 0 a 4  | Dia do mês (1-31)                             |
| 5-8  | Mês (1 = Janeiro, 2 = fevereiro e assim por diante)        |
| 9-15 | Deslocamento de ano de 1980 (adicione 1980 para obter o ano real) |



 

Hora da **palavra**



| Bits  | Conteúdo                     |
|-------|-----------------------------|
| 0 a 4   | Segundos dividido por 2        |
| 5-10  | Minutos (0-59)              |
| 11-15 | Hora (0-23 no relógio de 24 horas) |



 

A fórmula para calcular os valores de campo mentale e MaxDate é:

(Ano-1980) \* 512 + mês \* 32 + dia) \* 65536 + horas \* 2048 + minutos \* 32 + segundos/2

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

 

 



