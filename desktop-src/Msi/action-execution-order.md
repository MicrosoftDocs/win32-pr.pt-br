---
description: A ordem de execução da ação é determinada pela sequência de ações que foram feitas nas tabelas de sequência e pela ordem em que o instalador executa as tabelas de sequência.
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

A ordem de execução da ação é determinada pela sequência [](s-gly.md) de ações que foram feitas nas tabelas de sequência e pela ordem em que o instalador executa as tabelas de sequência. Para obter detalhes, consulte as sequências de ação sugeridas em [Usando uma tabela de sequência.](using-a-sequence-table.md)

O instalador executa tabelas de sequência em resposta a uma solicitação para uma instalação, [anúncio](advertisement.md)ou [uma instalação administrativa](administrative-installation.md). Por exemplo, em resposta ao uso das opções de linha de comando /I, /J ou [/A,](command-line-options.md)as ações [INSTALL,](install-action.md) [ADVERTISE](advertise-action.md)e [ADMIN](admin-action.md) não são chamadas de dentro da sequência de ação. Essas ações de alto nível são passadas para o instalador quando o instalador é inicializado.

Se o instalador receber a ação INSTALL e o pacote de instalação tiver sido autor com uma interface do usuário, o instalador primeiro executará as ações na tabela [InstallUISequence](installuisequence-table.md) e, em seguida, executará as ações na tabela [InstallExecuteSequence](installexecutesequence-table.md) na ordem. Se o pacote não tiver nenhuma interface do usuário, o instalador executará as ações na tabela InstallExecuteSequence na ordem.

Se o instalador for aprovado na ação ADMIN e o pacote de instalação tiver sido autor com uma interface do usuário, o instalador primeiro executa a tabela [AdminUISequence](adminuisequence-table.md) e, em seguida, executa a tabela [AdminExecuteSequence](adminexecutesequence-table.md). Se o pacote não tiver nenhuma interface do usuário, o instalador executa a tabela AdminExecute.

Se o instalador for passado para a ação ADVERTISE, o instalador executa a [tabela AdvtExecuteSequence.](advtexecutesequence-table.md)

> [!Note]  
> O instalador não usa a [tabela AdvtUISequence.](advtuisequence-table.md) A tabela AdvtUISequence não deve existir no banco de dados de instalação ou deve ser deixada vazia.

 

Quando o instalador executa uma tabela de sequência, ele executa ações na ordem dos números de sequência listados na coluna Sequência. A ordem de ação é sempre linear sem ramificação ou loop. Os desenvolvedores de pacotes podem impedir condicionalmente que uma ação específica seja executada por meio da adoção de uma expressão lógica na coluna Condição. O instalador ignora a ação sempre que a condição é avaliada como False. Consulte [Usando uma tabela de sequência e](using-a-sequence-table.md) sintaxe de [instrução condicional](conditional-statement-syntax.md).

Todas as tabelas de sequência têm as seguintes colunas.



| Coluna    | Descrição                                                                                                                                                                                                                                   |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ação    | A chave primária para a tabela; o nome da ação deve ser exclusivo.                                                                                                                                                                                |
| Condição | Uma expressão booliana usada para determinar se a ação deve ser tomada. A ação será executada se esse campo estiver em branco ou contiver uma expressão que seja avaliada como True. A ação não será executada se a expressão for avaliada como False. |
| Sequência  | Um número de sequência relativo usado para determinar a ordem em que as ações são executadas.                                                                                                                                                         |



 

 

 



