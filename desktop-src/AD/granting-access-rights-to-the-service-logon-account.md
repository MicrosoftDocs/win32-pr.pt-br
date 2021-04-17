---
title: Concedendo direitos de acesso à conta de logon do serviço
description: Uma consideração principal da instalação de uma instância de serviço é garantir que o serviço instalado possa acessar os recursos necessários.
ms.assetid: 5b756318-f621-4fce-af2b-71ccccbb4e3c
ms.tgt_platform: multiple
keywords:
- Concedendo direitos de acesso ao AD da conta de logon do serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f4ea5b85e6158109338b881eeb3f59d74a3910
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "105769120"
---
# <a name="granting-access-rights-to-the-service-logon-account"></a>Concedendo direitos de acesso à conta de logon do serviço

Uma consideração principal da instalação de uma instância de serviço é garantir que o serviço instalado possa acessar os recursos necessários. Para fazer isso, defina ACEs nos descritores de segurança de objetos que o serviço deve acessar. Uma ACE pode conceder ou negar direitos de acesso a uma entidade de segurança especificada, como a conta de usuário de serviço ou a conta de computador para um serviço LocalSystem ou um grupo ao qual a conta do serviço pertence. Para obter mais informações sobre ACEs, descritores de segurança e controle de acesso, consulte [controlando o acesso a objetos no Active Directory Domain Services](controlling-access-to-objects-in-active-directory-domain-services.md) e [controle de acesso](/windows/desktop/SecAuthZ/access-control).

Para obter mais informações e um exemplo de código que pode ser usado para definir uma ACE que permite ao serviço modificar seu ponto de conexão de serviço, consulte [habilitando a conta de serviço para acessar as propriedades do SCP](enabling-service-account-to-access-scp-properties.md).

Em alguns casos, você deve adicionar sua conta de usuário de serviço como um membro de um ou mais grupos de segurança. Por exemplo, se você criar um grupo de administradores para seu serviço, poderá fazer com que o serviço seja um membro do grupo. Você pode conceder direitos de acesso ao grupo em vez de concedê-los explicitamente para a conta de serviço. Para obter mais informações sobre grupos de segurança, consulte [Managing groups](managing-groups.md).

 

 