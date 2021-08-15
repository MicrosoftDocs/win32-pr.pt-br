---
description: Quando um aplicativo usa o API de Gerenciamento credenciais para solicitar credenciais, espera-se que o usuário insira informações que podem ser validadas, seja pelo sistema operacional ou pelo aplicativo.
ms.assetid: 53ed2eb4-2c29-48fd-b7fa-0c27bf155758
title: Formatos de nome de usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57c2d4a31904e1cdc6c08da596e2db24054389387ef90142001e7f0e6e520567
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915541"
---
# <a name="user-name-formats"></a>Formatos de nome de usuário

Quando um aplicativo usa o API de Gerenciamento credenciais para solicitar credenciais, espera-se que o usuário insira informações que podem ser validadas, seja pelo sistema operacional ou pelo aplicativo. O usuário pode especificar informações de credenciais de domínio em um dos seguintes formatos:

-   [Nome principal do usuário](#user-principal-name)
-   [Nome de logon de nível inferior](#down-level-logon-name)

## <a name="user-principal-name"></a>Nome UPN

[*O formato*](../secgloss/u-gly.md) UPN (nome UPN) é usado para especificar um nome no estilo da Internet, como <b>UserName@Example.Microsoft.com</b> . A tabela a seguir resume as partes de um UPN.



| Parte                                                        | Exemplo                                |
|-------------------------------------------------------------|----------------------------------------|
| Nome da conta de usuário. Também conhecido como o nome de logon.<br/> | *UserName*<br/>                  |
| Separador. Um literal de caractere, o sinal at (@).<br/> | @<br/>                           |
| Sufixo UPN. Também conhecido como o nome de domínio.<br/>       | *Example.Microsoft.com* <br/> |



 

Um UPN pode ser definido implicitamente ou explicitamente. Um UPN implícito é do formato <b>UserName@DNSDomainName.com</b> . Um UPN implícito sempre é associado à conta do usuário, mesmo que um UPN explícito não seja definido. Um UPN explícito é do formato , em que as cadeias de caracteres de nome e <i><b>Name@Suffix</b></i> sufixo são definidas explicitamente pelo administrador.

## <a name="down-level-logon-name"></a>Down-Level logon do Down-Level

O formato de nome de logon de nível inferior é usado para especificar um domínio e uma conta de usuário nesse domínio, por exemplo, <i><b>DOMAIN \\ UserName</b></i>. A tabela a seguir resume as partes de um nome de logon de nível inferior.



| Parte                                                           | Exemplo               |
|----------------------------------------------------------------|-----------------------|
| Nome de domínio NetBIOS.<br/>                                | *DOMAIN*<br/>   |
| Separador. Um literal de caractere, a faixa invertida ( \\ ).<br/> | **\\**<br/>     |
| Nome da conta de usuário. Também conhecido como o nome de logon.<br/>    | *UserName*<br/> |



 

 

 
