---
description: Insira registros para as cinco ações personalizadas de exemplo criadas na seção anterior para a tabela CustomAction. Para obter mais informações sobre como preencher a tabela CustomAction para esse tipo de ação personalizada, consulte tipo de ação personalizada 1.
ms.assetid: 56828105-bd72-426d-833f-f756c577c77f
title: Criando a tabela CustomAction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56fb7d8cf99a30200e6a5525e3516e2b888c1129
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921490"
---
# <a name="authoring-the-customaction-table"></a>Criando a tabela CustomAction

Insira registros para as cinco ações personalizadas de exemplo criadas na seção anterior para a [tabela CustomAction](customaction-table.md). Para obter mais informações sobre como preencher a tabela CustomAction para esse tipo de ação personalizada, consulte [tipo de ação personalizada 1](custom-action-type-1.md).

[Tabela CustomAction](customaction-table.md)



| Ação            | Tipo  | Fonte      | Destino                |
|-------------------|-------|-------------|-----------------------|
| ProcessAccounts   | 1     | Process.dll | ProcessUserAccounts   |
| UninstallAccounts | 1     | Process.dll | UninstallUserAccounts |
| CreateAccount     | 11265 | Create.dll  | CreateUserAccount     |
| RemoveAccount     | 11265 | Remove.dll  | RemoveUserAccount     |
| RollbackAccount   | 9473  | Remove.dll  | RemoveUserAccount     |



 

O código-fonte do C++ para as bibliotecas de vínculo dinâmico são fornecidos no SDK do Windows Installer. Use o Process. cpp para criar o arquivo Process.dll. Use Create. cpp para criar o arquivo Create.dll. Use remove. cpp para criar Remove.dll. Adicione esses arquivos da biblioteca de vínculo dinâmico à tabela binária.

[Tabela binária](binary-table.md)



| Name        | Dados            |
|-------------|-----------------|
| Process.dll | {*dados binários*} |
| Create.dll  | {*dados binários*} |
| Remove.dll  | {*dados binários*} |



 

Continue a [Adicionar uma tabela CustomUserAccounts personalizada](adding-a-custom-customuseraccounts-table.md).

 

 



