---
description: O exemplo a seguir mostra como Windows Instalador 3.0 e posterior pode ser usado para aplicar patches na ordem em que eles são autorados.
ms.assetid: 98771652-cec2-4371-8132-a741cf8431fb
title: Exemplo de a patch múltipla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b8d33d103bb27fde3b7fdc4ee46a0c5d946e73b6948513ea1b8fffb7bab30bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943363"
---
# <a name="multiple-patching-example"></a>Exemplo de a patch múltipla

O exemplo a seguir mostra como Windows Instalador 3.0 e posterior pode ser usado para aplicar patches na ordem em que eles são autorados.

## <a name="example"></a>Exemplo

Neste exemplo, há três patches, QFE1, QFE2 e ServicePack1, e cada um deles tem uma [tabela MsiPatchSequence.](msipatchsequence-table.md) Esses patches foram autorados para serem aplicados à versão 1.0 do aplicativo.



| Nome do patch   | Tipo de patch    | Número de Sequência |
|--------------|---------------|-----------------|
| QFE1         | Atualização pequena  | 1.1.0           |
| QFE2         | Atualização pequena  | 1.2.0           |
| ServicePack1 | Atualização secundária | 1.3.0           |



 

A [tabela MsiPatchSequence](msipatchsequence-table.md) de cada patch tem apenas um registro que contém a família de patch, o código do produto e o número de sequência. Todos os três patches são aplicados ao mesmo produto e pertencem à mesma família de patch, chamada AppPatch. Nenhum dos patches tem o **atributo msidbPatchSequenceSupersedeEarlier.**

[Tabela MsiPatchSequence](msipatchsequence-table.md) para a pequena [atualização](small-updates.md)QFE1. 

| PatchFamily | ProductCode                            | Sequência | Atributos |
|-------------|----------------------------------------|----------|------------|
| AppPatch    | {18A9233C-0B34-4127-A966-C257386270BC} | 1.1.0    |            |



 

[Tabela MsiPatchSequence](msipatchsequence-table.md) para a pequena [atualização](small-updates.md)QFE2. 

| PatchFamily | ProductCode                            | Sequência | Atributos |
|-------------|----------------------------------------|----------|------------|
| AppPatch    | {18A9233C-0B34-4127-A966-C257386270BC} | 1.2.0    |            |



 

[Tabela MsiPatchSequence para](msipatchsequence-table.md) atualização secundária do ServicePack1. [](minor-upgrades.md) 

| PatchFamily | ProductCode                            | Sequência | Atributos |
|-------------|----------------------------------------|----------|------------|
| AppPatch    | {18A9233C-0B34-4127-A966-C257386270BC} | 1.3.0    |            |



 

Se um usuário instalar a versão 1.0 do produto e, em seguida, aplicar o QFE2 e, em uma data posterior, decidir aplicar o QFE1, o instalador do Windows garantirá que a sequência efetiva do aplicativo de patch ao produto seja QFE1 aplicada antes do QFE2. Se o usuário aplicar ServicePack1, o QFE2 e o QFE1 serão aplicados juntos em uma data posterior, o instalador do Windows garantirá que a sequência efetiva do aplicativo de patch ao produto seja QFE1 antes do QFE2 e à frente do ServicePack1.

Se ServicePack1 tiver **msidbPatchSequenceSupersedeEarlier** definido na coluna Atributos de sua [tabela MsiPatchSequence,](msipatchsequence-table.md) isso significa que o service pack contém todas as alterações em QFE1 e QFE2. Nesse caso, QFE1 e QFE2 não são aplicados quando ServicePack1 é aplicado.

**Windows Instalador 2.0:** Sem suporte. Versões anteriores Windows Instalador 3.0 podem instalar apenas um patch por transação e os patches são aplicados na sequência fornecida. Para o exemplo anterior, se QFE2 for aplicado primeiro e, em seguida, QFE1 for aplicado, serão duas transações e os patches serão aplicados à versão 1.0 do aplicativo na sequência QFE2 seguida por QFE1. Se ServicePack1 for aplicado primeiro, O QFE1 ou QFE2 não poderá ser aplicado em uma transação posterior porque ServicePack1 é uma atualização secundária que altera a versão do aplicativo. QFE1 e QFE2 só podem ser aplicados à versão 1.0 do aplicativo.

 

 



