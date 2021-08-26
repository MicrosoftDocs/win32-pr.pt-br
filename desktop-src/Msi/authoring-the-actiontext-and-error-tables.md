---
description: As especificações de exemplo incluem o envio de mensagens ActionData quando uma ação personalizada cria ou remove uma conta de usuário e relata um erro se uma conta não pode ser criada.
ms.assetid: ee90fe3d-51f4-433b-a5ce-950a03e1d8fb
title: Como autor das tabelas ActionText e Error
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a7b89c8150e3767841fe914cf55fc7be8c92e8cecf8f54f8486993d955349be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045396"
---
# <a name="authoring-the-actiontext-and-error-tables"></a>Como autor das tabelas ActionText e Error

As especificações de exemplo incluem o envio de mensagens ActionData quando uma ação personalizada cria ou remove uma conta de usuário e relata um erro se uma conta não pode ser criada.

Insira as entradas a seguir na tabela ActionText para fornecer informações usadas pelas mensagens ActionText.

[Tabela ActionText](actiontext-table.md)



| Ação            | Descrição                                                       | Modelo                          |
|-------------------|-------------------------------------------------------------------|-----------------------------------|
| ProcessAccounts   | Gerando ações para criar contas de usuário no computador local. | Conta: \[ 1 \] , Atributos: \[ 2\] |
| CreateAccount     | Criando uma conta de usuário no computador local.                      | Conta: \[ 1\]                    |
| RemoveAccount     | Removendo a conta de usuário do computador local.                    | Conta: \[ 1\]                    |
| RollbackAccount   | Reverter a criação de contas de usuário no computador local. | Conta: \[ 1\]                    |
| UninstallAccounts | Gerando ações para remover contas de usuário no computador local. | Conta: \[ 1\]                    |



 

Insira as entradas a seguir na tabela Erro para fornecer informações usadas pelo relatório de erros.

[Tabela de erros](error-table.md)



| Erro | Mensagem                                                                        |
|-------|--------------------------------------------------------------------------------|
| 25001 | Não é possível criar a conta de usuário ' \[ 2 \] ' no computador local. Código de erro: \[ 3 \] . |
| 25002 | A conta de \[ usuário ' 2 \] ' já existe no computador local.                      |
| 25003 | Não é possível remover a conta de usuário ' \[ 2 \] ' no computador local. Código de erro: \[ 3 \] . |
| 25004 | A conta de \[ usuário ' 2 \] ' não existe no computador local.                      |



 

Continue a [autor da tabela InstallExecuteSequence](authoring-the-installexecutesequence-table.md).

 

 



