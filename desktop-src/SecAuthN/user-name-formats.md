---
description: Quando um aplicativo usa a API de gerenciamento de credenciais para solicitar credenciais, espera-se que o usuário insira informações que podem ser validadas pelo sistema operacional ou pelo aplicativo.
ms.assetid: 53ed2eb4-2c29-48fd-b7fa-0c27bf155758
title: Formatos de nome de usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1fb99a9e6064cd3883a8d71c1e76ca853d88661
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749759"
---
# <a name="user-name-formats"></a>Formatos de nome de usuário

Quando um aplicativo usa a API de gerenciamento de credenciais para solicitar credenciais, espera-se que o usuário insira informações que podem ser validadas pelo sistema operacional ou pelo aplicativo. O usuário pode especificar informações de credenciais de domínio em um dos seguintes formatos:

-   [Nome principal do usuário](#user-principal-name)
-   [Nome de logon de nível inferior](#down-level-logon-name)

## <a name="user-principal-name"></a>Nome UPN

O formato UPN ( [*nome principal do usuário*](../secgloss/u-gly.md) ) é usado para especificar um nome de estilo de Internet, como <b>UserName@Example.Microsoft.com</b> . A tabela a seguir resume as partes de um UPN.



| Parte                                                        | Exemplo                                |
|-------------------------------------------------------------|----------------------------------------|
| Nome da conta de usuário. Também conhecido como o nome de logon.<br/> | *UserName*<br/>                  |
| Caractere. Um literal de caractere, o sinal de arroba (@).<br/> | @<br/>                           |
| Sufixo UPN. Também conhecido como o nome de domínio.<br/>       | *Example.Microsoft.com* <br/> |



 

Um UPN pode ser definido implicitamente ou explicitamente. Um UPN implícito está no formato <b>UserName@DNSDomainName.com</b> . Um UPN implícito sempre é associado à conta do usuário, mesmo que um UPN explícito não esteja definido. Um UPN explícito é do formulário <i><b>Name@Suffix</b></i> , onde as cadeias de caracteres de nome e sufixo são explicitamente definidas pelo administrador.

## <a name="down-level-logon-name"></a>Nome de logon do Down-Level

O formato de nome de logon de nível inferior é usado para especificar um domínio e uma conta de usuário nesse domínio, por exemplo, <i><b>domínio \\ username</b></i>. A tabela a seguir resume as partes de um nome de logon de nível inferior.



| Parte                                                           | Exemplo               |
|----------------------------------------------------------------|-----------------------|
| Nome de domínio NetBIOS.<br/>                                | *DOMAIN*<br/>   |
| Caractere. Um literal de caractere, a barra invertida ( \\ ).<br/> | **\\**<br/>     |
| Nome da conta de usuário. Também conhecido como o nome de logon.<br/>    | *UserName*<br/> |



 

 

 
