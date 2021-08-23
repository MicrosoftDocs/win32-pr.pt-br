---
description: Insira registros para as cinco ações personalizadas de exemplo criadas na seção anterior para a Tabela CustomAction. Para obter mais informações sobre como preencher a tabela CustomAction para esse tipo de ação personalizada, consulte Tipo de ação personalizada 1.
ms.assetid: 56828105-bd72-426d-833f-f756c577c77f
title: Como fazer a tabela CustomAction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b618da6e88718aa59483b3b25c007ff0b41eb89f6e1dc18a7eb31563632dc54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066076"
---
# <a name="authoring-the-customaction-table"></a>Como fazer a tabela CustomAction

Insira registros para as cinco ações personalizadas de exemplo criadas na seção anterior para a [Tabela CustomAction](customaction-table.md). Para obter mais informações sobre como popular a tabela CustomAction para esse tipo de ação personalizada, consulte [Custom Action Type 1](custom-action-type-1.md).

[Tabela CustomAction](customaction-table.md)



| Ação            | Tipo  | Fonte      | Destino                |
|-------------------|-------|-------------|-----------------------|
| ProcessAccounts   | 1     | Process.dll | ProcessUserAccounts   |
| UninstallAccounts | 1     | Process.dll | UninstallUserAccounts |
| CreateAccount     | 11265 | Create.dll  | CreateUserAccount     |
| RemoveAccount     | 11265 | Remove.dll  | RemoveUserAccount     |
| RollbackAccount   | 9473  | Remove.dll  | RemoveUserAccount     |



 

O código-fonte do C++ para as bibliotecas de vínculo dinâmico é fornecido no SDK Windows Installer. Use Process.cpp para criar o arquivo Process.dll. Use Create.cpp para criar o arquivo Create.dll. Use Remove.cpp para criar Remove.dll. Adicione esses arquivos de biblioteca de vínculo dinâmico à tabela Binária.

[Tabela binária](binary-table.md)



| Nome        | Dados            |
|-------------|-----------------|
| Process.dll | {*dados binários*} |
| Create.dll  | {*dados binários*} |
| Remove.dll  | {*dados binários*} |



 

Continue [adicionando uma tabela CustomUserAccounts personalizada.](adding-a-custom-customuseraccounts-table.md)

 

 



