---
description: Se essa política do sistema for definida como 1, o instalador não armazenará arquivos de reversão durante a instalação e desabilitará a reversão da instalação.
ms.assetid: 01747de6-7478-4403-ba36-8ff1abc2b70f
title: DisableRollback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7f0ce15e618880f021e04adf7d2146a97f6ed65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921062"
---
# <a name="disablerollback"></a>DisableRollback

Se essa [política do sistema](system-policy.md) for definida como 1, o instalador não armazenará arquivos de reversão durante a instalação e desabilitará a reversão da instalação. Por padrão, a reversão está habilitada. Os administradores são aconselhados a não usar essa política, a menos que seja absolutamente essencial. Para obter mais informações, consulte [Rollback Installation](rollback-installation.md).

## <a name="registry-key"></a>Chave do Registro

Para desabilitar a reversão para instalações por usuário, defina **DisableRollback** como 1 na seguinte chave do registro:

**HKEY \_ \_** Políticas de software de usuário atuais \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

Para desabilitar a reversão para instalações por computador, defina **DisableRollback** como 1 na seguinte chave do registro.

**HKEY \_ \_** Políticas de \\ **software** do computador local \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de Dados

**REG \_ DWORD**

 

 



