---
description: A tabela FamilyFileRanges contém informações sobre arquivos específicos de uma imagem atualizada com intervalos que nunca devem ser substituídos.
ms.assetid: 2e77605a-d909-4a17-977c-18281a96c36c
title: Tabela FamilyFileRanges (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2940d45d82efae3e61842ee0f6b4e46e3f77ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091135"
---
# <a name="familyfileranges-table-patchwizdll"></a>Tabela FamilyFileRanges (Patchwiz.dll)

A tabela FamilyFileRanges contém informações sobre arquivos específicos de uma imagem atualizada com intervalos que nunca devem ser substituídos. Essa tabela é opcional no banco de dados de criação de patches (arquivo. PCP) e é usada pela função [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) .

A tabela FamilyFileRanges tem as colunas a seguir.



| Coluna        | Tipo | Chave | Nullable |
|---------------|------|-----|----------|
| Família        | text | S   | N        |
| FTK           | text | S   | N        |
| RetainOffsets | text |     | N        |
| RetainLengths | text |     | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Family"></span><span id="family"></span><span id="FAMILY"></span>Parentes
</dt> <dd>

Chave estrangeira para a coluna família da [tabela ImageFamilies (Patchwiz.dll)](imagefamilies-table-patchwiz-dll-.md).

</dd> <dt>

<span id="FTK"></span><span id="ftk"></span>FTK
</dt> <dd>

Chave estrangeira nas [tabelas de arquivos](file-table.md) de todas as imagens atualizadas na família de imagens.

</dd> <dt>

<span id="RetainOffsets"></span><span id="retainoffsets"></span><span id="RETAINOFFSETS"></span>RetainOffsets
</dt> <dd>

O deslocamento dos intervalos que não podem ser substituídos. O valor nesse campo é uma lista dos números de deslocamento de intervalo para intervalos que não devem ser substituídos nos arquivos de destino. A ordem e o número dos intervalos na lista devem corresponder aos itens na coluna RetainLengths.

Os valores podem ser decimal ou hexadecimal. [Patchwiz.dll](patchwiz-dll.md) tratará o valor como hexadecimal se for prefixado por "0x". As colunas são colunas de cadeia de caracteres e Patchwiz.dll converterá os valores em ULONGs.

</dd> <dt>

<span id="RetainLengths"></span><span id="retainlengths"></span><span id="RETAINLENGTHS"></span>RetainLengths
</dt> <dd>

O comprimento em bytes dos intervalos que não podem ser substituídos. O valor nesse campo é uma lista de números de comprimento de intervalo para os intervalos a serem retidos nos arquivos de destino. A ordem e o número dos intervalos na lista devem corresponder aos itens na coluna RetainOffsets.

Os valores podem ser decimal ou hexadecimal. [Patchwiz.dll](patchwiz-dll.md) tratará o valor como hexadecimal se for prefixado por "0x". As colunas são colunas de cadeia de caracteres e Patchwiz.dll converterá os valores em ULONGs.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os deslocamentos e comprimentos inseridos em RetainOffsets e RetainLengths não devem especificar intervalos sobrepostos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aplicação de patch nas regiões selecionadas de um arquivo](patching-selected-regions-of-a-file.md)
</dt> </dl>

 

 



