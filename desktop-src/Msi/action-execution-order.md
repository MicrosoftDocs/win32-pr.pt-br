---
description: A ordem de execução da ação é determinada pela sequência de ações que foram criadas nas tabelas de sequência e pela ordem em que o instalador executa as tabelas de sequência.
ms.assetid: f4666f49-4ea1-42fb-b32d-ce77de79b212
title: Ordem de execução da ação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf28244d46ae5556d1b68cc3b7258297c69e11a8d526f3e7ca31a184e64c424e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118381836"
---
# <a name="action-execution-order"></a>Ordem de execução da ação

A ordem de execução da ação é determinada pela sequência de ações que foram criadas nas [*tabelas de sequência*](s-gly.md) e pela ordem em que o instalador executa as tabelas de sequência. Para obter detalhes, consulte as sequências de ação sugeridas em [usando uma tabela de sequência](using-a-sequence-table.md).

O instalador executa tabelas de sequência em resposta a uma solicitação de instalação, [anúncio](advertisement.md)ou [instalação administrativa](administrative-installation.md). Por exemplo, em resposta ao uso das [Opções de linha de comando](command-line-options.md)/I,/J ou/a, as ações de [instalação](install-action.md), [anúncio](advertise-action.md)e [administrador](admin-action.md) não são chamadas de dentro da sequência de ação. Em vez disso, essas ações de alto nível são passadas para o instalador quando o instalador é inicializado.

Se o instalador for aprovado na ação de instalação e o pacote de instalação tiver sido criado com uma interface do usuário, o instalador executará primeiro as ações na [tabela InstallUISequence](installuisequence-table.md) e executará as ações na [tabela InstallExecuteSequence](installexecutesequence-table.md) na ordem. Se o pacote não tiver nenhuma interface do usuário, o instalador executará as ações na tabela InstallExecuteSequence na ordem.

Se o instalador for aprovado na ação de administrador e o pacote de instalação tiver sido criado com uma interface do usuário, o instalador executará primeiro a [tabela AdminUISequence](adminuisequence-table.md) e executará a [tabela AdminExecuteSequence](adminexecutesequence-table.md). Se o pacote não tiver nenhuma interface do usuário, o instalador executará a tabela AdminExecute.

Se o instalador passar na ação de anúncio, o instalador executará a tabela [AdvtExecuteSequence](advtexecutesequence-table.md) .

> [!Note]  
> O instalador não usa a tabela [AdvtUISequence](advtuisequence-table.md) . A tabela AdvtUISequence não deve existir no banco de dados de instalação ou deve ser deixada em branco.

 

Quando o instalador executa uma tabela de sequência, ele executa ações na ordem dos números de sequência listados na coluna sequência. A ordem de ação é sempre linear sem ramificação ou looping. Os desenvolvedores de pacotes podem impedir condicionalmente que uma ação específica seja executada por meio da criação de uma expressão lógica na coluna condição. O instalador ignora a ação sempre que a condição é avaliada como falsa. Consulte [usando uma tabela de sequência](using-a-sequence-table.md) e [sintaxe de instrução condicional](conditional-statement-syntax.md).

Todas as tabelas de sequência têm as colunas a seguir.



| Coluna    | Descrição                                                                                                                                                                                                                                   |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ação    | A chave primária da tabela; o nome da ação deve ser exclusivo.                                                                                                                                                                                |
| Condição | Uma expressão booliana usada para determinar se a ação deve ser executada. A ação será executada se esse campo estiver em branco ou contiver uma expressão que seja avaliada como true. A ação não será executada se a expressão for avaliada como falsa. |
| Sequência  | Um número de sequência relativo usado para determinar a ordem na qual as ações são executadas.                                                                                                                                                         |



 

 

 



