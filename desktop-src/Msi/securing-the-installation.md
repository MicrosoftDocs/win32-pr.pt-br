---
description: Adicione todas as propriedades de senha da tabela CustomUserAccounts à propriedade MsiHiddenProperties na tabela de propriedades.
ms.assetid: 682f534c-10a2-4260-b21d-7075d8c1620c
title: Protegendo a instalação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: add5211327508dbbf6531c48c3d2ae40f095375d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922901"
---
# <a name="securing-the-installation"></a>Protegendo a instalação

Adicione todas as propriedades de senha da tabela CustomUserAccounts à propriedade [**MsiHiddenProperties**](msihiddenproperties.md) na [tabela de propriedades](property-table.md). Adicione os nomes das ações personalizadas adiadas à propriedade **MsiHiddenProperties** também. Isso impedirá que o instalador grave os valores de propriedade confidenciais (as senhas) no log e garantirá que esses valores não sejam registrados quando as ações personalizadas adiadas usarem os valores como a propriedade CustomActionData.

Para que a senha do usuário esteja disponível no serviço Windows Installer, a propriedade password deve ser adicionada à propriedade [**SecureCustomProperties**](securecustomproperties.md) .

[Tabela de propriedades](property-table.md)



| Propriedade                                                 | Valor                                                        |
|----------------------------------------------------------|--------------------------------------------------------------|
| [**MsiHiddenProperties**](msihiddenproperties.md)       | TESTUSERPASSWORD; CreateAccount; RemoveAccount; RollbackAccount |
| [**SecureCustomProperties**](securecustomproperties.md) | TESTUSERPASSWORD                                             |



 

Isso conclui o exemplo.

 

 



