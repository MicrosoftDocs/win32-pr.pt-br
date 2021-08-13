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

A tabela ExternalFiles contém informações sobre arquivos específicos que não fazem parte de uma imagem de destino regular. Esses arquivos podem existir em produtos que foram atualizados por outro produto, atualização ou patch. Essa tabela é opcional no banco de dados de criação de patches (arquivo. PCP) e é usada pela função [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) .

A tabela ExternalFiles tem as colunas a seguir.



| Coluna        | Tipo    | Chave | Nullable |
|---------------|---------|-----|----------|
| Família        | texto    | Y   | N        |
| FTK           | texto    | Y   | N        |
| FilePath      | texto    | Y   | N        |
| SymbolPaths   | texto    |     | Y        |
| IgnoreOffsets | texto    |     | Y        |
| IgnoreLengths | texto    |     | Y        |
| RetainOffsets | texto    |     | N        |
| Ordem         | Número inteiro |     | Y        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Parentes
</dt> <dd>

Chave estrangeira para a coluna família da [tabela ImageFamilies (Patchwiz.dll)](imagefamilies-table-patchwiz-dll-.md).

</dd> <dt>

<span id="FTK"></span><span id="ftk"></span>FTK
</dt> <dd>

Chave estrangeira na [tabela de arquivos](file-table.md) do .msi arquivo da imagem atualizada.

</dd> <dt>

<span id="FilePath"></span><span id="filepath"></span><span id="FILEPATH"></span>FilePath
</dt> <dd>

Caminho completo do arquivo externo, incluindo o nome do arquivo. O campo FilePath é usado para localizar o arquivo especificado na coluna FTK.

</dd> <dt>

<span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths
</dt> <dd>

O caminho completo pesquisou os arquivos de símbolo do arquivo especificado na coluna FTK.

</dd> <dt>

<span id="IgnoreOffsets"></span><span id="ignoreoffsets"></span><span id="IGNOREOFFSETS"></span>IgnoreOffsets
</dt> <dd>

O valor nesse campo é uma lista delimitada por vírgulas de números de deslocamento de intervalo para os intervalos a serem ignorados no arquivo externo. A ordem e o número dos intervalos na lista devem corresponder aos itens na coluna IgnoreLengths. Essa coluna é opcional.

Os valores podem ser decimal ou hexadecimal. [Patchwiz.dll](patchwiz-dll.md) tratará o valor como hexadecimal se for prefixado por "0x". As colunas são colunas de cadeia de caracteres e Patchwiz.dll converterá os valores em ULONGs.

</dd> <dt>

<span id="IgnoreLengths"></span><span id="ignorelengths"></span><span id="IGNORELENGTHS"></span>IgnoreLengths
</dt> <dd>

O valor nesse campo é uma lista delimitada por vírgulas de comprimentos de intervalo em bytes para que os intervalos sejam ignorados no arquivo externo. A ordem e o número dos intervalos na lista devem corresponder aos itens na coluna IgnoreOffsets. Essa coluna é opcional.

Os valores podem ser decimal ou hexadecimal. [Patchwiz.dll](patchwiz-dll.md) tratará o valor como hexadecimal se for prefixado por "0x". As colunas são colunas de cadeia de caracteres e Patchwiz.dll converterá os valores em ULONGs.

</dd> <dt>

<span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets
</dt> <dd>

O valor nesse campo é uma lista delimitada por vírgulas de números de deslocamento de intervalo para os intervalos a serem retidos no arquivo externo. A ordem e o número dos intervalos na lista devem corresponder aos itens na coluna RetainOffsets do registro correspondente na [tabela FamilyFileRanges (Patchwiz.dll)](familyfileranges-table-patchwiz-dll-.md).

Os valores podem ser decimal ou hexadecimal. [Patchwiz.dll](patchwiz-dll.md) tratará o valor como hexadecimal se for prefixado por "0x". As colunas são colunas de cadeia de caracteres e Patchwiz.dll converterá os valores em ULONGs.

</dd> <dt>

<span id="Order"></span><span id="order"></span><span id="ORDER"></span>Ordene
</dt> <dd>

Se duas ou mais versões forem especificadas para o mesmo arquivo externo, a tabela poderá conter vários registros com valores correspondentes nos campos FTK e Family. Nesse caso, o campo Order pode especificar a ordem dos arquivos externos a serem usados ao criar o patch. O pedido é do mais antigo para a versão mais recente.

</dd> </dl>

## <a name="remarks"></a>Comentários

Esta tabela aceita variáveis de ambiente como caminhos que começam com a versão 4,0 de Patchwiz.dll.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aplicação de patch nas regiões selecionadas de um arquivo](patching-selected-regions-of-a-file.md)
</dt> </dl>

 

 



