---
description: As ações personalizadas ProcessAccounts e UninstallAccounts geram as ações personalizadas adiadas que criam, removem ou rebackam contas de usuário.
ms.assetid: 245b576b-96cc-4eab-8848-5ff78ba32873
title: Como fazer a tabela InstallExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ff6b8a551b141b5fc3f4d15318f2a6d98ff834cd33a572d542563adf55447b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118639167"
---
# <a name="authoring-the-installexecutesequence-table"></a>Como fazer a tabela InstallExecuteSequence

As ações personalizadas ProcessAccounts e UninstallAccounts geram as ações personalizadas adiadas que criam, removem ou rebackam contas de usuário. As ações personalizadas ProcessAccounts e UninstallAccounts devem ser inseridas na [tabela InstallExecuteSequence](installexecutesequence-table.md) a ser executada. Adicione as seguintes entradas à [tabela InstallExecuteSequence](installexecutesequence-table.md). Como essas ações personalizadas devem fazer parte da geração de script, ambas as ações personalizadas devem ser sequenciadas após a [ação InstallInitialize](installinitialize-action.md).

A condição em ProcessAccounts garante o seguinte. Consulte [Sintaxe de instrução condicional](conditional-statement-syntax.md).

-   ProcessAccounts será executado somente se o componente TestAccount estiver sendo instalado localmente no computador.
-   No momento, a Conta de Teste do componente não está instalada ou está instalada para ser executado na origem.

A condição em UninstallAccount garante o seguinte:

-   UninstallAccounts será executado somente se o componente TestAccount estiver instalado localmente no computador.
-   A Conta de Teste do componente está sendo removida ou instalada para ser executado da origem.

[Tabela InstallExecuteSequence](installexecutesequence-table.md)



| Ação            | Condição                                                           | Sequência |
|-------------------|---------------------------------------------------------------------|----------|
| ProcessAccounts   | VersionNT AND (? TestAccount=2 OR ? TestAccount=4) AND $TestAccount=3 | 1550     |
| UninstallAccounts | VersionNT E ? TestAccount=3 AND ($TestAccount=4 OR $TestAccount=2) | 1560     |



 

Continue a [Como autorizar a interface do usuário para entrada de senha.](authoring-the-user-interface-for-password-input.md)

 

 



