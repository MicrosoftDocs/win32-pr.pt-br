---
description: A tabela de assinatura contém as informações que identificam exclusivamente uma assinatura de arquivo. para obter mais informações sobre assinaturas, consulte assinaturas digitais e Windows Installer.
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

A tabela de assinatura contém as informações que identificam exclusivamente uma assinatura de arquivo. para obter mais informações sobre assinaturas [, consulte assinaturas digitais e Windows Installer](digital-signatures-and-windows-installer.md).

A tabela de assinatura tem as colunas a seguir.



| Coluna     | Tipo                               | Chave | Nullable |
|------------|------------------------------------|-----|----------|
| Assinatura  | [Identificador](identifier.md)       | Y   | N        |
| FileName   | [Text](text.md)                   | N   | N        |
| MinVersion | [Text](text.md)                   | N   | Y        |
| MaxVersion | [Text](text.md)                   | N   | Y        |
| MinSize    | [DoubleInteger](doubleinteger.md) | N   | Y        |
| MaxSize    | [DoubleInteger](doubleinteger.md) | N   | Y        |
| Lembre-se    | [DoubleInteger](doubleinteger.md) | N   | Y        |
| MaxDate    | [DoubleInteger](doubleinteger.md) | N   | Y        |
| Idiomas  | [Text](text.md)                   | N   | Y        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>Signature
</dt> <dd>

A coluna de assinatura é uma assinatura de arquivo exclusiva.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Nome do arquivo
</dt> <dd>

O nome do arquivo.

</dd> <dt>

<span id="MinVersion"></span><span id="minversion"></span><span id="MINVERSION"></span>MinVersion
</dt> <dd>

A versão mínima do arquivo, com uma comparação de idioma. Se esse campo for especificado, o arquivo deverá ter uma versão que seja pelo menos igual a MinVersion. Se o arquivo tiver uma versão igual ao valor do campo MinVersion, mas o idioma especificado na coluna idiomas for diferente, o arquivo não atenderá aos critérios do filtro de assinatura.

> [!Note]  
> O idioma especificado na coluna idiomas é usado na comparação e não há como ignorar o idioma. Se desejar que um arquivo atenda ao requisito de campo MinVersion independentemente da linguagem, você deverá inserir um valor no campo MinVersion que seja menor que o valor real. Por exemplo, se a versão mínima para o filtro for 2.0.2600.1183, use 2.0.2600.1182 para localizar o arquivo sem corresponder às informações de idioma.

 

</dd> <dt>

<span id="MaxVersion"></span><span id="maxversion"></span><span id="MAXVERSION"></span>MaxVersion
</dt> <dd>

A versão máxima do arquivo. Se esse campo for especificado, o arquivo deverá ter uma versão que seja, no máximo, igual a MaxVersion.

</dd> <dt>

<span id="MinSize"></span><span id="minsize"></span><span id="MINSIZE"></span>MinSize
</dt> <dd>

O tamanho mínimo do arquivo. Se esse campo for especificado, o arquivo em inspeção deverá ter um tamanho que seja, pelo menos, igual a MinSize. Este deve ser um número não negativo.

</dd> <dt>

<span id="MaxSize"></span><span id="maxsize"></span><span id="MAXSIZE"></span>MaxSize
</dt> <dd>

O tamanho máximo do arquivo. Se esse campo for especificado, o arquivo em inspeção deverá ter um tamanho que seja, no máximo, igual a MaxSize. Este deve ser um número não negativo.

</dd> <dt>

<span id="MinDate"></span><span id="mindate"></span><span id="MINDATE"></span>Lembre-se
</dt> <dd>

A data e a hora mínimas de modificação do arquivo. Se esse campo for especificado, o arquivo em inspeção deverá ter uma data e hora de modificação que seja, pelo menos, igual a. Este deve ser um número não negativo. O formato desse campo é dois valores de 16 bits empacotados do tipo **Word**. O valor de **palavra** de ordem superior especifica a data no formato de data do MS-dos. O valor de **palavra** de ordem inferior Especifica a hora no formato de hora do MS-dos. Um valor de 0 para o valor de hora representa meia-noite. Consulte a seção Comentários.

</dd> <dt>

<span id="MaxDate"></span><span id="maxdate"></span><span id="MAXDATE"></span>MaxDate
</dt> <dd>

A data de criação máxima do arquivo. Se esse campo for especificado, o arquivo em inspeção deverá ter uma data de criação que seja, no máximo, igual a MaxDate. Este deve ser um número não negativo. O formato desse campo é dois valores de 16 bits empacotados do tipo **Word**. O valor de **palavra** de ordem superior especifica a data no formato de data do MS-dos. O valor de **palavra** de ordem inferior Especifica a hora no formato de hora do MS-dos. Um valor de 0 para o valor de tempo representa meia-noite. Consulte a seção Comentários.

</dd> <dt>

<span id="Languages"></span><span id="languages"></span><span id="LANGUAGES"></span>Idiomas
</dt> <dd>

Os idiomas com suporte no arquivo.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa tabela é usada com a [tabela AppSearch](appsearch-table.md).

A assinatura é pesquisada usando a [tabela RegLocator](reglocator-table.md), a [tabela IniLocator](inilocator-table.md), a [tabela CompLocator](complocator-table.md)e a [tabela DrLocator](drlocator-table.md). As colunas desta tabela geralmente não são localizadas. Se um autor decidir procurar produtos em vários idiomas, poderá haver uma entrada separada incluída na tabela para cada idioma.

a tabela de assinatura geralmente segue as Windows Installer [regras de controle de versão do arquivo](file-versioning-rules.md). Os idiomas especificados na coluna idiomas da tabela de assinatura não são avaliados, a menos que as versões de arquivo sejam equivalentes. A coluna idiomas garantirá que um arquivo seja de um idioma específico se for da versão solicitada. Não há nenhum método disponível para ignorar a coluna de idiomas. Um valor nulo inserido na coluna idiomas é tratado como um arquivo sem idioma e não corresponde à assinatura de arquivo de um arquivo com uma linguagem que aparece na tabela de assinatura. O exemplo a seguir pesquisa uma versão específica do MSI.DLL.

[Tabela DrLocator](drlocator-table.md)

| Assinatura\_ | Pai | Caminho                  | Profundidade |
|-------------|--------|-----------------------|-------|
| MsiDll      | {null} | c: \\ windows \\ system32 | 0     |



 

[Tabela AppSearch](appsearch-table.md)



| Propriedade | Assinatura\_ |
|----------|-------------|
| MSIDLL   | MsiDll      |



 

Tabela de assinatura



| Assinatura | FileName | MinVersion    | Maxversion | Minsize | MaxSize | Mindate | Maxdate | Idiomas |
|-----------|----------|---------------|------------|---------|---------|---------|---------|-----------|
| MsiDll    | msi.dll  | 2.0.2600.1106 | {null}     | {null}  | {null}  | {null}  | {null}  | 0         |



 

Nesse caso, e no Windows XP SP1, a ação [AppSearch](appsearch-action.md) define MSIDLL como c: \\ windows system32msi.dll porque MSI.DLL é um arquivo neutro em \\ \\ idioma. Se o valor da coluna Idiomas for alterado de 0 para 1033, a ação AppSearch não encontrará o valor correspondente msi.dll e a propriedade MSIDLL será indefinida.

Você não pode usar a tabela Assinatura para consultar apenas idiomas. Para pesquisar versões de idioma diferentes de um arquivo, você deve ter uma entrada separada na tabela Assinatura para cada versão do idioma. Se vários idiomas são fornecidos na coluna Idiomas, a pesquisa é para um arquivo que dá suporte a todos esses idiomas.

O formato das colunas MinDate e MaxDate são dois valores empacotados de 16 bits do **tipo WORD.**

Palavra de **data**



| Bits | Conteúdo                                             |
|------|-----------------------------------------------------|
| 0–4  | Dia do mês (1-31)                             |
| 5-8  | Mês (1 = janeiro, 2 = fevereiro e assim por diante)        |
| 9-15 | Deslocamento de ano de 1980 (adicionar 1980 para obter o ano real) |



 

Time **WORD**



| Bits  | Conteúdo                     |
|-------|-----------------------------|
| 0–4   | Segundos divididos por 2        |
| 5-10  | Minutos (0-59)              |
| 11-15 | Hora(0 a 23 no relógio de 24 horas) |



 

A fórmula para calcular os valores de campo MinDate e MaxDate é:

( (Year - 1980) \* 512 + Month \* 32 + Day ) \* 65536 + Hours \* 2048 + Minutes \* 32 + Seconds/2

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

 

 



