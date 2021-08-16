---
description: A tabela TargetFiles \_ OptionalData contém informações sobre arquivos específicos em uma imagem de destino. Essa tabela é opcional no banco de dados de criação de patch (arquivo .pcp) e é usada pela função UiCreatePatchPackageEx.
ms.assetid: 577b1674-1e44-42e1-b011-c0fb561b514c
title: TargetFiles_OptionalData (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5664e2e21968cb3fee5ce3d606dd07008f2436c4b649a7bcefeebd77df9cf6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118623731"
---
# <a name="targetfiles_optionaldata-table-patchwizdll"></a>Tabela TargetFiles \_ OptionalData (Patchwiz.dll)

A tabela TargetFiles \_ OptionalData contém informações sobre arquivos específicos em uma imagem de destino. Essa tabela é opcional no banco de dados de criação de patch (arquivo .pcp) e é usada pela [função UiCreatePatchPackageEx.](uicreatepatchpackageex--patchwiz-dll-.md)

A tabela TargetFiles \_ OptionalData tem as seguintes colunas.



| Coluna        | Tipo | Chave | Nullable |
|---------------|------|-----|----------|
| Destino        | texto | Y   | N        |
| Ftk           | texto | Y   | N        |
| SymbolPaths   | texto |     | Y        |
| IgnoreOffsets | texto |     | Y        |
| IgnoreLengths | texto |     | Y        |
| RetainOffsets | texto |     | Y        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Target"></span><span id="target"></span><span id="TARGET"></span>Alvo
</dt> <dd>

Chave estrangeira para a coluna Destino da [Tabela TargetImages (Patchwiz.dll)](targetimages-table-patchwiz-dll-.md).

</dd> <dt>

<span id="FTK"></span><span id="ftk"></span>Ftk
</dt> <dd>

Chave estrangeira na tabela [Arquivo da](file-table.md) imagem de destino.

</dd> <dt>

<span id="SymbolPaths"></span><span id="symbolpaths"></span><span id="SYMBOLPATHS"></span>SymbolPaths
</dt> <dd>

O valor nesse campo é adicionado à lista delimitada por ponto e vírgula de pastas na coluna SymbolPaths da [tabela TargetImages (Patchwiz.dll)](targetimages-table-patchwiz-dll-.md) quando o patch é gerado e pode ser usado para adicionar arquivos de símbolo para um arquivo específico.

</dd> <dt>

<span id="IgnoreOffsets"></span><span id="ignoreoffsets"></span><span id="IGNOREOFFSETS"></span>IgnoreOffsets
</dt> <dd>

O valor nesse campo é uma lista delimitada por vírgulas de números de deslocamento de intervalo para os intervalos a serem ignorados no arquivo de destino. A ordem e o número dos intervalos na lista devem corresponder aos itens na coluna IgnoreLengths. Essa coluna é opcional.

Os valores podem ser decimais ou hexadecimais. [Patchwiz.dll](patchwiz-dll.md) trata o valor como hexadecimal se ele for prefixado por "0x". As colunas são colunas de cadeia de caracteres e Patchwiz.dll converterá os valores em ULONGs.

</dd> <dt>

<span id="IgnoreLengths"></span><span id="ignorelengths"></span><span id="IGNORELENGTHS"></span>IgnoreLengths
</dt> <dd>

O valor nesse campo é uma lista delimitada por vírgulas de comprimentos de intervalo em bytes para os intervalos a serem ignorados no arquivo de destino. A ordem e o número dos intervalos na lista devem corresponder aos itens na coluna IgnoreOffsets. Essa coluna é opcional.

Os valores podem ser decimais ou hexadecimais. [Patchwiz.dll](patchwiz-dll.md) trata o valor como hexadecimal se ele for prefixado por "0x". As colunas são colunas de cadeia de caracteres e Patchwiz.dll converterá os valores em ULONGs.

</dd> <dt>

<span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets
</dt> <dd>

O valor nesse campo é uma lista delimitada por vírgulas de números de deslocamento de intervalo para os intervalos a serem retidos no arquivo de destino. A ordem e o número dos intervalos na lista devem corresponder aos itens na coluna RetainOffsets do registro correspondente na tabela [FamilyFileRanges (Patchwiz.dll)](familyfileranges-table-patchwiz-dll-.md)

Os valores podem ser decimais ou hexadecimais. [Patchwiz.dll](patchwiz-dll.md) trata o valor como hexadecimal se ele for prefixado por "0x". As colunas são colunas de cadeia de caracteres e Patchwiz.dll converterá os valores em ULONGs.

</dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Corrigindo regiões selecionadas de um arquivo](patching-selected-regions-of-a-file.md)
</dt> </dl>

 

 



