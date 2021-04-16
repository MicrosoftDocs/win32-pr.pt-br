---
description: As ações personalizadas ProcessAccounts e UninstallAccounts geram as ações personalizadas adiadas que criam, removem ou rerecuperam contas de usuário.
ms.assetid: 245b576b-96cc-4eab-8848-5ff78ba32873
title: Criando a tabela InstallExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aa09895d5e5d2543b5594f4795734d26163a4f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768480"
---
# <a name="authoring-the-installexecutesequence-table"></a>Criando a tabela InstallExecuteSequence

As ações personalizadas ProcessAccounts e UninstallAccounts geram as ações personalizadas adiadas que criam, removem ou rerecuperam contas de usuário. As ações personalizadas ProcessAccounts e UninstallAccounts devem ser inseridas na [tabela InstallExecuteSequence](installexecutesequence-table.md) para serem executadas. Adicione as entradas a seguir à [tabela InstallExecuteSequence](installexecutesequence-table.md). Como essas ações personalizadas devem fazer parte da geração de script, ambas as ações personalizadas devem ser sequenciadas após a [ação InstallInitialize](installinitialize-action.md).

A condição em ProcessAccounts garante o seguinte. Consulte [sintaxe de instrução condicional](conditional-statement-syntax.md).

-   ProcessAccounts será executado somente se o componente TestAccount estiver sendo instalado localmente no computador.
-   A conta de teste de componente não está instalada no momento ou está instalada para ser executada a partir da origem.

A condição em UninstallAccount garante o seguinte:

-   UninstallAccounts será executado somente se o componente TestAccount estiver instalado localmente no computador.
-   A conta de teste de componente está sendo removida ou instalada para ser executada da origem.

[Tabela InstallExecuteSequence](installexecutesequence-table.md)



| Ação            | Condição                                                           | Sequência |
|-------------------|---------------------------------------------------------------------|----------|
| ProcessAccounts   | VersionNT e (? TestAccount = 2 ou? TestAccount = 4) e $TestAccount = 3 | 1550     |
| UninstallAccounts | VersionNT e? TestAccount = 3 e ($TestAccount = 4 ou $TestAccount = 2) | 1560     |



 

Continue a [criar a interface do usuário para entrada de senha](authoring-the-user-interface-for-password-input.md).

 

 



