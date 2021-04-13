---
title: Tarefas de manutenção da conta de logon
description: Este tópico descreve os problemas que pertencem a tarefas de manutenção de conta de logon.
ms.assetid: 528be433-58ef-400b-ba9a-d114f3f94ec6
ms.tgt_platform: multiple
keywords:
- AD de tarefas de manutenção da conta de logon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa0f11f69d9a974fd666871833029eda0e059329
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104365819"
---
# <a name="logon-account-maintenance-tasks"></a>Tarefas de manutenção da conta de logon

Este tópico descreve os problemas que pertencem a tarefas de manutenção de conta de logon.

Há dois problemas principais que se referem a tarefas de manutenção de conta de logon:

-   Atualizando a senha da conta para uma instância de serviço que é executada em uma conta de usuário. Para obter mais informações, consulte [alterando a senha na conta de usuário de um serviço](changing-the-password-on-a-serviceampaposs-user-account.md).
-   Tratamento de alterações na conta de logon de uma instância de serviço.

O segundo é um caso raro, mas pode acontecer. O sistema fornece a ferramenta administrativa de gerenciamento do computador que permite alterar para uma conta de logon de serviço. Além disso, outros aplicativos podem usar a função [**ChangeServiceConfig**](/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfiga) para especificar uma nova conta de logon para um serviço instalado. Por padrão, são necessários privilégios de administrador local para alterar uma conta de serviço. Se isso acontecer, ele poderia afetar o serviço de duas maneiras:

-   Se você tiver registrado os SPNs (nomes da entidade de serviço), eles serão registrados na conta errada.
-   Se você definir ACEs para conceder acesso ao serviço, elas agora concederão acesso à conta incorreta.

Uma abordagem é fazer com que o instalador de serviço armazene os SPNs registrados para cada instância de serviço no registro no computador host. Você pode usar a mesma chave do registro em HKEY \_ local \_ Machine que você usou para armazenar a cadeia de vinculação para o SCP de serviço. Quando o serviço é iniciado, ele chama a função [**QueryServiceConfig**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfiga) para determinar sua conta de logon e consulta o servidor de Active Directory para determinar se os SPNs estão registrados no objeto de diretório para essa conta. Se os SPNs não estiverem registrados ou estiverem registrados na conta errada, o serviço se recusará a iniciar e exibirá uma mensagem informando que um administrador de domínio deve executar o programa de configuração do serviço para atualizar as configurações de conta de logon. Lembre-se de que essa reconfiguração deve ser concluída por um administrador porque a conta de serviço não deve ter acesso para atualizar seu próprio SPN. Além disso, lembre-se de que os SPNs devem ser removidos da conta antiga, caso contrário, os SPNs serão inúteis para autenticação porque não são exclusivos na floresta.

 

 