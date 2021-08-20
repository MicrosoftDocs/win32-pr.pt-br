---
title: Configurando a conta de usuário de um serviço
description: O instalador do serviço pode sugerir uma conta de logon padrão para uma instância de serviço e permitir que o administrador selecione a conta padrão ou especifique outra.
ms.assetid: 37285c23-8922-4da5-9f0b-922ea5e5794e
ms.tgt_platform: multiple
keywords:
- Configurando o AD da conta de usuário de um serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f310ee97c68ded8c4086694302feccb5991d726e01f9addbeced21cc5b9acfdc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118183273"
---
# <a name="setting-up-a-services-user-account"></a>Configurando a conta de usuário de um serviço

O instalador do serviço pode sugerir uma conta de logon padrão para uma instância de serviço e permitir que o administrador selecione a conta padrão ou especifique outra. Se o administrador selecionar uma conta de usuário, em vez da conta LocalSystem, a conta deverá existir antes de você chamar a [**função CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) para instalar uma instância do serviço em um servidor host. Para obter mais informações e um exemplo de código que pode ser usado para criar um novo objeto de usuário de domínio no Active Directory Domain Services, consulte [Criando um usuário](creating-a-user.md).

O ideal é que cada instância de um serviço, seja um serviço baseado em host ou replicado, deve ter sua própria conta de usuário de domínio. Usar contas separadas para cada instância de serviço é mais seguro do que ter várias instâncias compartilhando a mesma conta. Além disso, o uso de contas separadas possibilita auditar as atividades de cada instância de serviço.

Quando o instalador sugere uma conta de logon padrão, ele deve especificar o nome de uma nova conta a ser criada para a nova instância de serviço. O nome da conta pode ser composto pelos mesmos elementos usados para compor um nome de entidade de serviço, como a classe de serviço, o computador host e o nome do serviço. Para saber mais, confira [Service Principal Names](service-principal-names.md) (Nomes da entidade de serviço). Normalmente, você cria a conta no contêiner Usuários no domínio do computador host.

Você deve gerar uma senha para cada conta. Para obter mais informações sobre como escrever uma ferramenta que automatiza a tarefa de atualização de senhas da conta de serviço, consulte Alterando a senha na conta de usuário [de um serviço](changing-the-password-on-a-serviceampaposs-user-account.md).

 

 