---
title: Tarefas de manutenção da conta de logon
description: Este tópico descreve os problemas que pertencem às tarefas de manutenção da conta de logon.
ms.assetid: 528be433-58ef-400b-ba9a-d114f3f94ec6
ms.tgt_platform: multiple
keywords:
- AD de Tarefas de Manutenção da Conta de Logon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09d026f37ad81d71691ac418ea49b1b0fda5e1d09fb3e4b6e2259083eb80ada9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186628"
---
# <a name="logon-account-maintenance-tasks"></a>Tarefas de manutenção da conta de logon

Este tópico descreve os problemas que pertencem às tarefas de manutenção da conta de logon.

Há dois problemas principais relacionados às tarefas de manutenção da conta de logon:

-   Atualizando a senha da conta para uma instância de serviço que é executado em uma conta de usuário. Para obter mais informações, [consulte Alterando a senha na conta de usuário de um serviço](changing-the-password-on-a-serviceampaposs-user-account.md).
-   Tratamento de alterações na conta de logon de uma instância de serviço.

O último é um caso raro, mas pode acontecer. O sistema fornece a ferramenta administrativa Gerenciamento do Computador que permite alterar para uma conta de logon de serviço. Além disso, outros aplicativos podem usar a [**função ChangeServiceConfig**](/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfiga) para especificar uma nova conta de logon para um serviço instalado. Por padrão, os privilégios de administrador local são necessários para alterar uma conta de serviço. Se isso acontecer, isso poderá afetar seu serviço de duas maneiras:

-   Se você registrou SPNs (nomes de entidade de serviço), eles serão registrados na conta errada.
-   Se você definir ACEs para conceder acesso ao serviço, eles agora concederão acesso à conta errada.

Uma abordagem é fazer com que o instalador de serviço armazene os SPNs registrados para cada instância de serviço no Registro no computador host. Você pode usar a mesma chave do Registro em HKEY LOCAL MACHINE que você usou para armazenar a cadeia de caracteres de associação \_ \_ para o SCP de serviço. Quando o serviço é iniciado, ele chama a função [**QueryServiceConfig**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfiga) para determinar sua conta de logon e, em seguida, consulta o servidor do Active Directory para determinar se os SPNs estão registrados no objeto de diretório para essa conta. Se os SPNs não estão registrados ou estão registrados na conta errada, o serviço se recusa a iniciar e exibe uma mensagem dizendo que um administrador de domínio deve executar o programa de configuração do serviço para atualizar as configurações da conta de logon. Esteja ciente de que essa reconfiguração deve ser concluída por um administrador porque a conta de serviço não deve ter acesso para atualizar seu próprio SPN. Além disso, esteja ciente de que os SPNs devem ser removidos da conta antiga, caso contrário, os SPNs serão inúteis para autenticação porque não são exclusivos na floresta.

 

 