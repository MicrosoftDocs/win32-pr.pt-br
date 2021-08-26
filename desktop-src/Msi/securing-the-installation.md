---
description: Adicione todas as propriedades Password da tabela CustomUserAccounts à propriedade MsiHiddenProperties na tabela Property.
ms.assetid: 682f534c-10a2-4260-b21d-7075d8c1620c
title: Proteger a instalação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 642170cc2ac4e84bebe5235e84328abe5039ede1bdb8fc2760bbd249ff5268de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040726"
---
# <a name="securing-the-installation"></a>Proteger a instalação

Adicione todas as propriedades Password da tabela CustomUserAccounts à propriedade [**MsiHiddenProperties**](msihiddenproperties.md) na [tabela Property](property-table.md). Adicione os nomes das ações personalizadas adiadas à **propriedade MsiHiddenProperties** também. Isso impedirá que o instalador registre os valores de propriedade confidenciais (as senhas) no log e garantirá que esses valores não sejam registrados quando as ações personalizadas adiadas usarem os valores como a propriedade CustomActionData.

Para que a senha do usuário seja disponibilizada no serviço Windows Installer, a propriedade password deve ser adicionada à propriedade [**SecureCustomProperties.**](securecustomproperties.md)

[Tabela de propriedades](property-table.md)



| Propriedade                                                 | Valor                                                        |
|----------------------------------------------------------|--------------------------------------------------------------|
| [**MsiHiddenProperties**](msihiddenproperties.md)       | TESTUSERPASSWORD; CreateAccount; RemoveAccount; RollbackAccount |
| [**SecureCustomProperties**](securecustomproperties.md) | TESTUSERPASSWORD                                             |



 

Isso conclui o exemplo.

 

 



