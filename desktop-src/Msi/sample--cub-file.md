---
description: 'Este exemplo ilustra o layout de um arquivo .file que contém dois ICEs. O instalador executa as ações personalizadas na sequência: ICE01 e ICE08.'
ms.assetid: 609cd16a-4421-4082-855d-229f5ba7117b
title: Arquivo .cú de exemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7aadbaca8bde7091f38d5ce8ccc39926ec6c595aa33e65e488136e89cccfc81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039656"
---
# <a name="sample-cub-file"></a>Arquivo .cú de exemplo

Este exemplo ilustra o layout de um arquivo .file que contém dois [ICEs](internal-consistency-evaluators-ices.md). O instalador executa as ações personalizadas na sequência: ICE01 e ICE08.

A ação personalizada ICE01 é um [Tipo de Ação Personalizada 1.](custom-action-type-1.md) É um ponto de entrada para uma DLL que é armazenada como um fluxo no arquivo .file. Esse fluxo é listado na tabela binária ice.dll.

A ação personalizada ICE08 é um [Tipo de Ação Personalizada 6.](custom-action-type-6.md) É um ponto de entrada para uma função no VBScript que é armazenada como um fluxo no arquivo .file. Esse fluxo é listado na Tabela Binária como ice.vbs.

[Tabela binária](binary-table.md)



| Nome    | Dados                               |
|---------|------------------------------------|
| ice.vbs | Dados binários não formatados de ice.vbs |
| ice.dll | Dados binários não formatados de ice.dll |



 

[Tabela CustomAction](customaction-table.md)



| Ação | Tipo | Fonte  | Destino |
|--------|------|---------|--------|
| ICE01  | 1    | ice.dll | ICE01  |
| ICE08  | 6    | ice.vbs | ICE02  |



 

\_Tabela ICESequence



| Ação | Condição | Sequência |
|--------|-----------|----------|
| ICE01  |           | 10       |
| ICE08  |           | 20       |



 

\_Tabela especial

ICE01 e ICE08 não exigem a inclusão de tabelas de processamento especiais. Quando o arquivo .file contém tabelas especiais, eles também devem ser incluídos na Tabela \_ de Validação.

[\_Tabela de validação](-validation-table.md)



| Tabela         | Coluna    | Nullable | Minvalue | MaxValue | Keytable | KeyColumn | Categoria                         | Definir | Descrição |
|---------------|-----------|----------|----------|----------|----------|-----------|----------------------------------|-----|-------------|
| Binário        | Nome      | N        |          |          |          |           | [Identificador](identifier.md)     |     |             |
| Binário        | Dados      | N        |          |          |          |           | [Binary](binary.md)             |     |             |
| CustomAction  | Ação    | N        |          |          |          |           | [Identificador](identifier.md)     |     |             |
| CustomAction  | Tipo      | N        |          |          |          |           | [Inteiro](integer.md)           |     |             |
| CustomAction  | Fonte    | Y        |          |          |          |           | [Customsource](customsource.md) |     |             |
| CustomAction  | Destino    | Y        |          |          |          |           | [Formatado](formatted.md)       |     |             |
| \_ICESequence | Ação    | N        |          |          |          |           | [Identificador](identifier.md)     |     |             |
| \_ICESequence | Condição | Y        |          |          |          |           | [Condição](condition.md)       |     |             |
| \_ICESequence | Sequência  | Y        |          |          |          |           | [Inteiro](integer.md)           |     |             |



 

 

 



