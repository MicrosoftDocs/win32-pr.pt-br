---
description: 'Este exemplo ilustra o layout de um arquivo. Cub contendo duas ICEs. O instalador executa as ações personalizadas na sequência: ICE01 e ICE08.'
ms.assetid: 609cd16a-4421-4082-855d-229f5ba7117b
title: Arquivo. Cub de exemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e937b779e2a620ffc17cf936e37f74867f3dfdd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920866"
---
# <a name="sample-cub-file"></a>Arquivo. Cub de exemplo

Este exemplo ilustra o layout de um arquivo. Cub contendo duas [ICES](internal-consistency-evaluators-ices.md). O instalador executa as ações personalizadas na sequência: ICE01 e ICE08.

A ação personalizada ICE01 é um [tipo de ação personalizada 1](custom-action-type-1.md). É um ponto de entrada para uma DLL que é armazenada como um fluxo no arquivo. cub. Esse fluxo é listado na tabela binária ice.dll.

A ação personalizada ICE08 é um [tipo de ação personalizada 6](custom-action-type-6.md). É um ponto de entrada para uma função no VBScript que é armazenada como um fluxo no arquivo. cub. Esse fluxo é listado na tabela binária como ice.vbs.

[Tabela binária](binary-table.md)



| Name    | Dados                               |
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

ICE01 e ICE08 não exigem a inclusão de tabelas de processamento especiais. Quando o arquivo. Cub contém tabelas especiais, elas também devem ser incluídas na \_ tabela de validação.

[\_Tabela de validação](-validation-table.md)



| Tabela         | Coluna    | Nullable | MinValue | MaxValue | KeyTable | KeyColumn | Categoria                         | Definir | Descrição |
|---------------|-----------|----------|----------|----------|----------|-----------|----------------------------------|-----|-------------|
| Binário        | Name      | N        |          |          |          |           | [Identificador](identifier.md)     |     |             |
| Binário        | Dados      | N        |          |          |          |           | [Binary](binary.md)             |     |             |
| CustomAction  | Ação    | N        |          |          |          |           | [Identificador](identifier.md)     |     |             |
| CustomAction  | Tipo      | N        |          |          |          |           | [Inteiro](integer.md)           |     |             |
| CustomAction  | Fonte    | S        |          |          |          |           | [CustomSource](customsource.md) |     |             |
| CustomAction  | Destino    | S        |          |          |          |           | [Binário](formatted.md)       |     |             |
| \_ICESequence | Ação    | N        |          |          |          |           | [Identificador](identifier.md)     |     |             |
| \_ICESequence | Condição | S        |          |          |          |           | [Condição](condition.md)       |     |             |
| \_ICESequence | Sequência  | S        |          |          |          |           | [Inteiro](integer.md)           |     |             |



 

 

 



