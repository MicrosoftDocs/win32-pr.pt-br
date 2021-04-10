---
description: Uma sessão de logon é uma sessão de computação que começa quando uma autenticação de usuário é bem-sucedida e termina quando o usuário faz logoff do sistema.
ms.assetid: 14f0f9e7-90ba-47d7-a8d5-06f9d2f1a7a1
title: Sessões de logon LSA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f32a4912218b68c25c5c23334f7b34ef875fa318
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170817"
---
# <a name="lsa-logon-sessions"></a>Sessões de logon LSA

Uma [*sessão de logon*](../secgloss/l-gly.md) é uma sessão de computação que começa quando uma autenticação de usuário é bem-sucedida e termina quando o usuário faz logoff do sistema.

Quando um usuário é autenticado com êxito, o pacote de autenticação cria uma sessão de logon e retorna informações para a LSA ( [*autoridade de segurança local*](../secgloss/l-gly.md) ) que é usada para criar um [*token*](../secgloss/t-gly.md) para o novo usuário. Esse token inclui, entre outras coisas, um [*identificador local exclusivo*](../secgloss/l-gly.md) (LUID) para a sessão de logon, chamado de [*ID de logon*](../secgloss/l-gly.md).

Quando um token é criado, a [*contagem de referência*](../secgloss/r-gly.md) para a sessão de logon é incrementada. A contagem de referência também é incrementada sempre que as cópias do token são criadas para a criação, representação ou outros usos do processo. Como os usos de token são concluídos e as cópias do token são excluídas, a contagem de referência para a sessão de logon é decrementada. Quando a contagem de referência chega a zero, a sessão de logon é excluída.

> [!Note]  
> Se a autenticação não for bem-sucedida, o [*pacote de autenticação*](../secgloss/a-gly.md) não deverá criar uma sessão de logon. Se o pacote de autenticação precisar criar uma sessão de logon antes de fazer uma determinação final da validade do usuário e se a autenticação falhar, o pacote de autenticação deverá excluir a sessão.

 

 

 
