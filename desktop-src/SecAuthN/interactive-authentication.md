---
description: A autenticação é interativa quando um usuário é solicitado a fornecer informações de logon. A LSA (Autoridade de Segurança Local) executa uma autenticação interativa quando um usuário faz o login por meio da interface do usuário DOIS.
ms.assetid: 86a318fa-4d7c-4191-a309-d25b492dd915
title: Autenticação interativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 876f3aced39afba0d08a9643e14caae91336daf38a63f3855e76fe50136a16a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119482286"
---
# <a name="interactive-authentication"></a>Autenticação interativa

A autenticação é interativa quando um usuário é solicitado a fornecer informações de logon. A [*LSA (Autoridade*](../secgloss/l-gly.md) de Segurança Local) executa uma autenticação interativa quando um usuário faz o login por meio da interface do usuário [*DOIS.*](../secgloss/g-gly.md) A ilustração a seguir mostra as partes de uma autenticação interativa típica.

![autenticação interativa](images/lsaint3.png)

Um usuário sinaliza o sistema para iniciar a sequência de logon digitando a SAS [*(sequência*](../secgloss/s-gly.md) de atenção segura) CTRL+ALT+DEL. [*O Winlogon*](../secgloss/w-gly.md) recebe a SAS e chama o SEMPRE para exibir uma interface do usuário e obter os dados de logon do usuário, como um nome de usuário e uma senha.

Depois de obter os dados de logon, o SEMPRE chama a função [**LsaLogonUser**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalogonuser) para autenticar o usuário, especificando qual pacote de autenticação deve ser usado para avaliar os dados de logon.

O LSA chama o pacote de autenticação especificado e passa os dados de logon para ele. O pacote de autenticação examina os dados e determina se a autenticação foi bem-sucedida. O resultado da autenticação é retornado para o LSA e do LSA para o LTD.

O VISOR exibe o êxito ou a falha da autenticação para o usuário e retorna o resultado da autenticação para o Winlogon. Se a autenticação for bem-sucedida, a sessão de logon do usuário será iniciada e um conjunto de credenciais de [*logon*](../secgloss/c-gly.md) será salvo para referência futura.

> [!Note]  
> Em geral, um desenvolvedor que grava um PLAN personalizado para [](../secgloss/s-gly.md) aceitar dados de logon especializados, como um cartão inteligente ou dados de verificação retinal, também deve escrever um pacote de autenticação responsável por processar esses dados e determinar sua autenticidade.

 

Para obter mais informações sobre Winlogon e DRAAs, consulte [Winlogon e LTD.](winlogon-and-gina.md) Para obter mais informações sobre pacotes de autenticação, consulte [Criando pacotes de segurança personalizados.](creating-custom-security-packages.md)

 

 
