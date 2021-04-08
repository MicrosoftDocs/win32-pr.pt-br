---
description: A tabela PatchSequence é usada para gerar a tabela MsiPatchSequence em um patch. A tabela requer a versão do PATCHWIZ.DLL que está disponível com Windows Installer&\# 160; 3.0.
ms.assetid: bdeccb3b-57c0-4424-9602-348b8048fd46
title: Tabela PatchSequence (PATCHWIZ.DLL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 382e940d3c0cb6c7be2c8360ab98f2afaf13c799
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837303"
---
# <a name="patchsequence-table-patchwizdll"></a>Tabela PatchSequence (PATCHWIZ.DLL)

A tabela PatchSequence é usada para gerar a [tabela MsiPatchSequence](msipatchsequence-table.md) em um patch. A tabela requer a versão do [PATCHWIZ.DLL](patchwiz-dll.md) que está disponível com o Windows Installer 3,0.

A tabela a seguir identifica as colunas da tabela PatchSequence.



| Coluna      | Tipo       | Chave | Nullable |
|-------------|------------|-----|----------|
| PatchFamily | Identificador | S   | N        |
| Destino      | Texto       | S   | S        |
| Sequência    | Versão    |     | S        |
| Substituir   | Integer    |     | S        |



 

### <a name="columns"></a>Colunas

<dl> <dt>

<span id="PatchFamily"></span><span id="patchfamily"></span><span id="PATCHFAMILY"></span>PatchFamily
</dt> <dd>

O identificador que indica as famílias de sequência às quais esse patch pertence.

Os valores nas colunas Target e PatchFamily juntas definem a chave primária da tabela. Um patch que pertence a várias famílias de sequência ou tem sequências diferentes dependendo do código do produto do destino, pode ter uma linha para cada emparelhamento. Esse valor é usado para preencher a coluna PatchFamily da [tabela MsiPatchSequence](msipatchsequence-table.md) que pertence ao patch.

</dd> <dt>

<span id="Target"></span><span id="target"></span><span id="TARGET"></span>Alvo
</dt> <dd>

A coluna de destino é usada para filtrar o PatchFamily por código de produto.

Um valor nulo nesta coluna indica que esse PatchFamily se aplica a todos os destinos do patch. Se essa coluna contiver uma chave estrangeira para a [tabela TargetImages](targetimages-table-patchwiz-dll-.md), o código do produto da imagem especificada será recuperado e usado para popular o valor do código do produto na linha do novo patch da [tabela MsiPatchSequence](msipatchsequence-table.md). Se essa coluna contiver um GUID, o GUID será usado para preencher o valor do código do produto da linha na tabela MsiPatchSequence.

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Ordem
</dt> <dd>

O valor na coluna sequence é usado para preencher a coluna sequence da [tabela MsiPatchSequence](msipatchsequence-table.md) do novo arquivo de patch.

Se o valor for NULL, um número de sequência será gerado automaticamente.

</dd> <dt>

<span id="Supersede"></span><span id="supersede"></span><span id="SUPERSEDE"></span>Substituir
</dt> <dd>

Um valor de **msidbPatchSequenceSupersedeEarlier** ou 1 neste campo indica que esse patch substitui [as pequenas atualizações](small-updates.md) anteriores nas famílias de sequência às quais esse patch pertence.

O valor nessa coluna é usado para definir a coluna atributos da linha do novo patch na [tabela MsiPatchSequence](msipatchsequence-table.md) .

</dd> </dl>

### <a name="remarks"></a>Comentários

Disponível a partir do Windows Installer 3,0.

 

 



