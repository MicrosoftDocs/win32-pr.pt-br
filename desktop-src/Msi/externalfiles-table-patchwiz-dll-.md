---
description: A tabela ExternalFiles contém informações sobre arquivos específicos que não fazem parte de uma imagem de destino regular.
ms.assetid: c75591c2-5266-4a99-8104-53815f6550e2
title: Tabela ExternalFiles (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2573556e8e4e00cf9004b83520468724ad1c959704cf8be32769a7ee41e24ebf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118636873"
---
# <a name="externalfiles-table-patchwizdll"></a>Tabela ExternalFiles (Patchwiz.dll)

A tabela ExternalFiles contém informações sobre arquivos específicos que não fazem parte de uma imagem de destino regular. Esses arquivos podem existir em produtos que foram atualizados por outro produto, atualização ou patch. Essa tabela é opcional no banco de dados de criação de patch (arquivo .pcp) e é usada pela [função UiCreatePatchPackageEx.](uicreatepatchpackageex--patchwiz-dll-.md)

A tabela ExternalFiles tem as seguintes colunas.



| Coluna        | Tipo    | Chave | Nullable |
|---------------|---------|-----|----------|
| Família        | texto    | Y   | N        |
| Ftk           | texto    | Y   | N        |
| FilePath      | texto    | Y   | N        |
| SymbolPaths   | texto    |     | Y        |
| IgnoreOffsets | texto    |     | Y        |
| IgnoreLengths | texto    |     | Y        |
| RetainOffsets | texto    |     | N        |
| Ordem         | Número inteiro |     | Y        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Família
</dt> <dd>

Chave estrangeira para a coluna Família da [tabela ImageFamilies (Patchwiz.dll)](imagefamilies-table-patchwiz-dll-.md).

</dd> <dt>

<span id="FTK"></span><span id="ftk"></span>Ftk
</dt> <dd>

Chave estrangeira [na tabela Arquivo](file-table.md) do .msi da imagem atualizada.

</dd> <dt>

<span id="FilePath"></span><span id="filepath"></span><span id="FILEPATH"></span>Filepath
</dt> <dd>

Caminho completo do arquivo externo, incluindo o nome do arquivo. O campo FilePath é usado para localizar o arquivo especificado na coluna FTK.

</dd> <dt>

<span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths
</dt> <dd>

Caminho completo pesquisado por arquivos de símbolo do arquivo especificado na coluna FTK.

</dd> <dt>

<span id="IgnoreOffsets"></span><span id="ignoreoffsets"></span><span id="IGNOREOFFSETS"></span>IgnoreOffsets
</dt> <dd>

O valor nesse campo é uma lista delimitada por vírgulas de números de deslocamento de intervalo para os intervalos a serem ignorados no arquivo externo. A ordem e o número dos intervalos na lista devem corresponder aos itens na coluna IgnoreLengths. Essa coluna é opcional.

Os valores podem ser decimais ou hexadecimais. [Patchwiz.dll](patchwiz-dll.md) trata o valor como hexadecimal se ele for prefixado por "0x". As colunas são colunas de cadeia de caracteres e Patchwiz.dll converterá os valores em ULONGs.

</dd> <dt>

<span id="IgnoreLengths"></span><span id="ignorelengths"></span><span id="IGNORELENGTHS"></span>IgnoreLengths
</dt> <dd>

O valor nesse campo é uma lista delimitada por vírgulas de comprimentos de intervalo em bytes para os intervalos a serem ignorados no arquivo externo. A ordem e o número dos intervalos na lista devem corresponder aos itens na coluna IgnoreOffsets. Essa coluna é opcional.

Os valores podem ser decimais ou hexadecimais. [Patchwiz.dll](patchwiz-dll.md) trata o valor como hexadecimal se ele for prefixado por "0x". As colunas são colunas de cadeia de caracteres e Patchwiz.dll converterá os valores em ULONGs.

</dd> <dt>

<span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets
</dt> <dd>

O valor nesse campo é uma lista delimitada por vírgulas de números de deslocamento de intervalo para os intervalos a serem retidos no arquivo Externo. A ordem e o número dos intervalos na lista devem corresponder aos itens na coluna RetainOffsets do registro correspondente na Tabela [FamilyFileRanges (Patchwiz.dll).](familyfileranges-table-patchwiz-dll-.md)

Os valores podem ser decimais ou hexadecimais. [Patchwiz.dll](patchwiz-dll.md) trata o valor como hexadecimal se ele for prefixado por "0x". As colunas são colunas de cadeia de caracteres e Patchwiz.dll converterá os valores em ULONGs.

</dd> <dt>

<span id="Order"></span><span id="order"></span><span id="ORDER"></span>Ordem
</dt> <dd>

Se duas ou mais versões são especificadas para o mesmo arquivo externo, a tabela pode conter vários registros com valores correspondentes nos campos FTK e Family. Nesse caso, o campo Ordem pode especificar a ordem de arquivos externos a ser usado ao criar o patch. O pedido é da versão mais antiga para a mais recente.

</dd> </dl>

## <a name="remarks"></a>Comentários

Esta tabela aceita variáveis de ambiente como caminhos começando com a versão 4.0 do Patchwiz.dll.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Corrigindo regiões selecionadas de um arquivo](patching-selected-regions-of-a-file.md)
</dt> </dl>

 

 



