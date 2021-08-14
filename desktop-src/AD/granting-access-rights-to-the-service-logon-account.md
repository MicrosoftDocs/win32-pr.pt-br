---
title: Concedendo direitos de acesso à conta de logon de serviço
description: Uma consideração principal da instalação de uma instância de serviço é garantir que o serviço instalado possa acessar os recursos necessários.
ms.assetid: 5b756318-f621-4fce-af2b-71ccccbb4e3c
ms.tgt_platform: multiple
keywords:
- Concedendo direitos de acesso ao AD da conta de logon do serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d13d3e06432b3501961f65a3e27ca00a46f18197bef23d78e6f7ca0deec59b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118189075"
---
# <a name="granting-access-rights-to-the-service-logon-account"></a>Concedendo direitos de acesso à conta de logon de serviço

Uma consideração principal da instalação de uma instância de serviço é garantir que o serviço instalado possa acessar os recursos necessários. Para fazer isso, de definir ACEs nos descritores de segurança de objetos que o serviço deve acessar. Uma ACE pode conceder ou negar direitos de acesso a uma entidade de segurança especificada, como a conta de usuário do serviço ou a conta de computador para um serviço LocalSystem ou um grupo ao qual a conta do serviço pertence. Para obter mais informações sobre ACEs, descritores de segurança e controle de acesso, consulte [Controlando](controlling-access-to-objects-in-active-directory-domain-services.md) o acesso a objetos no Active Directory Domain Services e [Controle de Acesso](/windows/desktop/SecAuthZ/access-control).

Para obter mais informações e um exemplo de código que pode ser usado para definir uma ACE que permite que o serviço modifique seu ponto de conexão de serviço, consulte Habilitando a conta de serviço para acessar propriedades [SCP.](enabling-service-account-to-access-scp-properties.md)

Em alguns casos, você deve adicionar sua conta de usuário de serviço como membro de um ou mais grupos de segurança. Por exemplo, se você criar um grupo de administradores para seu serviço, poderá tornar o serviço um membro do grupo. Em seguida, você pode conceder direitos de acesso ao grupo em vez de concedi-los explicitamente à conta de serviço. Para obter mais informações sobre grupos de segurança, consulte [Gerenciando grupos](managing-groups.md).

 

 