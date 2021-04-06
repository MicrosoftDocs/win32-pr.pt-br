---
description: As especificações de exemplo incluem o envio de mensagens ActionData quando uma ação personalizada cria ou remove uma conta de usuário e relata um erro se uma conta não puder ser criada.
ms.assetid: ee90fe3d-51f4-433b-a5ce-950a03e1d8fb
title: Criando as tabelas de erro e ActionText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e20646a90ca76c159a88bdd8a6d026ff10845da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828056"
---
# <a name="authoring-the-actiontext-and-error-tables"></a>Criando as tabelas de erro e ActionText

As especificações de exemplo incluem o envio de mensagens ActionData quando uma ação personalizada cria ou remove uma conta de usuário e relata um erro se uma conta não puder ser criada.

Insira as entradas a seguir na tabela ActionText para fornecer informações usadas pelas mensagens ActionText.

[Tabela ActionText](actiontext-table.md)



| Ação            | Descrição                                                       | Modelo                          |
|-------------------|-------------------------------------------------------------------|-----------------------------------|
| ProcessAccounts   | Gerando ações para criar contas de usuário no computador local. | Conta: \[ 1 \] , atributos: \[ 2\] |
| CreateAccount     | Criando conta de usuário no computador local.                      | Conta: \[ 1\]                    |
| RemoveAccount     | Removendo a conta de usuário do computador local.                    | Conta: \[ 1\]                    |
| RollbackAccount   | Reverter a criação de contas de usuário no computador local. | Conta: \[ 1\]                    |
| UninstallAccounts | Gerando ações para remover contas de usuário no computador local. | Conta: \[ 1\]                    |



 

Insira as entradas a seguir na tabela de erros para fornecer informações usadas pelo relatório de erros.

[Tabela de erros](error-table.md)



| Erro | Mensagem                                                                        |
|-------|--------------------------------------------------------------------------------|
| 25001 | Não é possível criar a conta de usuário ' \[ 2 \] ' no computador local. Código de erro: \[ 3 \] . |
| 25002 | A conta de usuário ' \[ 2 \] ' já existe no computador local.                      |
| 25003 | Não é possível remover a conta de usuário ' \[ 2 \] ' no computador local. Código de erro: \[ 3 \] . |
| 25004 | A conta de usuário ' \[ 2 \] ' não existe no computador local.                      |



 

Continue a [criar a tabela InstallExecuteSequence](authoring-the-installexecutesequence-table.md).

 

 



