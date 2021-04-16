---
description: O exemplo a seguir mostra como Windows Installer 3,0 e posterior podem ser usados para aplicar patches na ordem em que são criados.
ms.assetid: 98771652-cec2-4371-8132-a741cf8431fb
title: Exemplo de vários patches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2d10274531ac4906ef61a49caee9ccbcde98bbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754351"
---
# <a name="multiple-patching-example"></a>Exemplo de vários patches

O exemplo a seguir mostra como Windows Installer 3,0 e posterior podem ser usados para aplicar patches na ordem em que são criados.

## <a name="example"></a>Exemplo

Neste exemplo, há três patches, QFE1, QFE2 e ServicePack1, e cada um deles tem uma tabela [MsiPatchSequence](msipatchsequence-table.md) . Esses patches foram criados para serem aplicados à versão 1,0 do aplicativo.



| Nome do patch   | Tipo de patch    | Número de Sequência |
|--------------|---------------|-----------------|
| QFE1         | Pequena atualização  | 1.1.0           |
| QFE2         | Pequena atualização  | 1.2.0           |
| ServicePack1 | Atualização secundária | 1.3.0           |



 

A tabela [MsiPatchSequence](msipatchsequence-table.md) de cada patch tem apenas um registro que contém a família de patches, o código do produto e o número de sequência. Os três patches são todos aplicados ao mesmo produto e pertencem à mesma família de patches, chamada AppPatch. Nenhum dos patches tem o atributo **msidbPatchSequenceSupersedeEarlier** .

[Tabela MsiPatchSequence](msipatchsequence-table.md) para a [atualização pequena](small-updates.md)do QFE1. 

| PatchFamily | ProductCode                            | Sequência | Atributos |
|-------------|----------------------------------------|----------|------------|
| AppPatch    | {18A9233C-0B34-4127-A966-C257386270BC} | 1.1.0    |            |



 

[Tabela MsiPatchSequence](msipatchsequence-table.md) para a [atualização pequena](small-updates.md)do QFE2. 

| PatchFamily | ProductCode                            | Sequência | Atributos |
|-------------|----------------------------------------|----------|------------|
| AppPatch    | {18A9233C-0B34-4127-A966-C257386270BC} | 1.2.0    |            |



 

[Tabela MsiPatchSequence](msipatchsequence-table.md) para [atualização secundária](minor-upgrades.md)ServicePack1. 

| PatchFamily | ProductCode                            | Sequência | Atributos |
|-------------|----------------------------------------|----------|------------|
| AppPatch    | {18A9233C-0B34-4127-A966-C257386270BC} | 1.3.0    |            |



 

Se um usuário instalar a versão 1,0 do produto e, em seguida, aplicar QFE2 e, em uma data posterior, decidir aplicar QFE1, Windows Installer garantirá que a sequência efetiva do aplicativo de patch para o produto seja QFE1 aplicada à frente do QFE2. Se o usuário aplicar ServicePack1, o aplicará QFE2 e QFE1 juntos em uma data posterior, Windows Installer garantirá que a sequência efetiva do aplicativo de patch para o produto seja QFE1 à frente de QFE2 e à frente de ServicePack1.

Se ServicePack1 tiver **msidbPatchSequenceSupersedeEarlier** definido na coluna Attributes de sua tabela [MsiPatchSequence](msipatchsequence-table.md) , isso significará que o Service Pack contém todas as alterações em QFE1 e QFE2. Nesse caso, QFE1 e QFE2 não são aplicados quando ServicePack1 é aplicado.

**Windows Installer 2,0:** Sem suporte. Versões anteriores a Windows Installer 3,0 podem instalar apenas um patch por transação e os patches são aplicados na sequência em que são fornecidos. Para o exemplo anterior, se QFE2 for aplicado primeiro e, em seguida, QFE1 for aplicado, ou seja, duas transações e os patches serão aplicados à versão 1,0 do aplicativo na sequência QFE2 seguida por QFE1. Se ServicePack1 for aplicado primeiro, QFE1 ou QFE2 não poderão ser aplicados em uma transação posterior porque ServicePack1 é uma atualização secundária que altera a versão do aplicativo. QFE1 e QFE2 só podem ser aplicados à versão 1,0 do aplicativo.

 

 



