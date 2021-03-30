---
title: Configurando a conta de usuário de um serviço
description: Seu instalador de serviço pode sugerir uma conta de logon padrão para uma instância de serviço e permitir que o administrador selecione a conta padrão ou especifique uma diferente.
ms.assetid: 37285c23-8922-4da5-9f0b-922ea5e5794e
ms.tgt_platform: multiple
keywords:
- Configurando o AD da conta de usuário de um serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 705fa16d8d2cce137755f4a5086716aaaef8046a
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103640376"
---
# <a name="setting-up-a-services-user-account"></a>Configurando a conta de usuário de um serviço

Seu instalador de serviço pode sugerir uma conta de logon padrão para uma instância de serviço e permitir que o administrador selecione a conta padrão ou especifique uma diferente. Se o administrador selecionar uma conta de usuário, em vez da conta LocalSystem, a conta deverá existir antes que você chame a função [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) para instalar uma instância do serviço em um servidor host. Para obter mais informações e um exemplo de código que pode ser usado para criar um novo objeto de usuário de domínio no Active Directory Domain Services, consulte [criando um usuário](creating-a-user.md).

O ideal é que cada instância de um serviço, seja um serviço replicável ou baseado em host, deva ter sua própria conta de usuário de domínio. O uso de contas separadas para cada instância de serviço é mais seguro do que ter várias instâncias que compartilham a mesma conta. Além disso, o uso de contas separadas torna possível auditar as atividades de cada instância de serviço.

Quando o instalador sugere uma conta de logon padrão, ele deve especificar o nome de uma nova conta a ser criada para a nova instância de serviço. O nome da conta pode ser composto dos mesmos elementos usados para compor um nome da entidade de serviço, como a classe de serviço, o computador host e o nome do serviço. Para saber mais, confira [Service Principal Names](service-principal-names.md) (Nomes da entidade de serviço). Normalmente, você cria a conta no contêiner usuários no domínio do computador host.

Você deve gerar uma senha para cada conta. Para obter mais informações sobre como escrever uma ferramenta que automatiza a tarefa de Atualizar senhas de conta de serviço, consulte [alterando a senha na conta de usuário de um serviço](changing-the-password-on-a-serviceampaposs-user-account.md).

 

 