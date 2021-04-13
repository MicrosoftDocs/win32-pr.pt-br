---
description: A autenticação é interativa quando um usuário é solicitado a fornecer informações de logon. A autoridade de segurança local (LSA) executa uma autenticação interativa quando um usuário faz logon por meio da interface de usuário da GINA.
ms.assetid: 86a318fa-4d7c-4191-a309-d25b492dd915
title: Autenticação interativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afeb09044f4b34f28c02cd0f03b3358a8158af65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297261"
---
# <a name="interactive-authentication"></a>Autenticação interativa

A autenticação é interativa quando um usuário é solicitado a fornecer informações de logon. A [*autoridade de segurança local*](../secgloss/l-gly.md) (LSA) executa uma autenticação interativa quando um usuário faz logon por meio da interface de usuário da [*Gina*](../secgloss/g-gly.md) . A ilustração a seguir mostra as partes de uma autenticação interativa típica.

![autenticação interativa](images/lsaint3.png)

Um usuário sinaliza o sistema para iniciar a sequência de logon digitando a SAS (sequência de [*atenção segura*](../secgloss/s-gly.md) ) Ctrl + Alt + Del. O [*Winlogon*](../secgloss/w-gly.md) recebe a SAS e chama a Gina para exibir uma interface do usuário e obter os dados de logon do usuário, como um nome de usuário e uma senha.

Depois de obter os dados de logon, o GINA chama a função [**LsaLogonUser**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalogonuser) para autenticar o usuário, especificando qual pacote de autenticação deve ser usado para avaliar os dados de logon.

O LSA chama o pacote de autenticação especificado e passa os dados de logon para ele. O pacote de autenticação examina os dados e determina se a autenticação é bem-sucedida. O resultado da autenticação é retornado para a LSA e da LSA para a GINA.

A GINA exibe o êxito ou a falha da autenticação para o usuário e retorna o resultado da autenticação para o Winlogon. Se a autenticação for realizada com sucesso, a sessão de logon do usuário será iniciada e um conjunto de [*credenciais*](../secgloss/c-gly.md) de logon será salvo para referência futura.

> [!Note]  
> Em geral, um desenvolvedor que escreve uma GINA personalizada para aceitar dados de logon especializados, como um [*cartão inteligente*](../secgloss/s-gly.md) ou dados de retina, também deve escrever um pacote de autenticação responsável por processar esses dados e determinar sua autenticidade.

 

Para obter mais informações sobre Winlogon e GINAs, consulte [Winlogon e Gina](winlogon-and-gina.md). Para obter mais informações sobre pacotes de autenticação, consulte [criando pacotes de segurança personalizados](creating-custom-security-packages.md).

 

 
