---
title: Administração de usuário ras
description: Um servidor RAS usa um banco de dados de conta de usuário que contém informações sobre um conjunto de contas de usuário.
ms.assetid: b58767b0-9b76-4d43-953a-ea772643745e
keywords:
- Ras Administration RRAS , user administration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7860e4916a9cf6138ebb6c201e9301feacbe332649036e7eb18075df621512a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028636"
---
# <a name="ras-user-administration"></a>Administração de usuário ras

Um servidor RAS usa um banco de dados de conta de usuário que contém informações sobre um conjunto de contas de usuário. As informações incluem os privilégios RAS de um usuário, que são um conjunto de sinalizadores de bits que determinam como o servidor RAS responde quando o usuário chama para se conectar. As funções de administração do servidor RAS localizam o banco de dados de conta de usuário e obter e definir os privilégios ras para contas de usuário.

Um servidor RAS pode fazer parte de um domínio do sistema operacional ou pode ser um computador autônomo que executa o servidor ou a versão profissional do sistema operacional. Para um servidor que faz parte de um domínio, o banco de dados da conta de usuário é armazenado no servidor que é o PDC (controlador de domínio primário). Um servidor autônomo armazena seu próprio banco de dados de conta de usuário local. Para obter o nome do servidor que armazena o banco de dados de conta de usuário usado por um servidor RAS especificado, você pode chamar a [**função MprAdminGetPDCServer.**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver) Em seguida, você pode usar o nome do servidor de conta de usuário em uma chamada para a função [**NetQueryDisplayInformation**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) para enumerar os usuários em um banco de dados de conta de usuário. Você também pode usar o nome do servidor em chamadas para as funções [**MprAdminUserGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo) e [**MprAdminUserSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo) para obter e definir os privilégios ras para uma conta de usuário especificada.

As funções [**MprAdminUserGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo) e [**MprAdminUserSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo) usam a estrutura [**RAS USER \_ \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_user_0) para especificar os privilégios RAS de um usuário e o número de telefone de retorno de chamada. Os privilégios ras indicam as seguintes informações:

-   Se o usuário pode fazer uma conexão remota com o servidor ou o domínio ao qual o servidor pertence.
-   Se o usuário estabelece uma conexão por meio de uma chamada de volta, na qual o servidor RAS trava e, em seguida, chama de volta ao usuário para estabelecer a conexão.

Cada conta de usuário especifica um dos sinalizadores a seguir para indicar os privilégios de retorno de chamada do usuário.



| Valor                      | Significado                                                                                                                                                                                                                                                                        |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RASPRIV \_ NoCallback        | O servidor RAS não chama de volta o usuário para estabelecer uma conexão.                                                                                                                                                                                                          |
| RASPRIV \_ AdminSetCallback  | Quando o usuário chama, o servidor RAS desliga e chama um número de telefone de retorno de chamada predefinido armazenado no banco de dados da conta de usuário. O **membro szPhoneNumber** da estrutura [**RAS USER \_ \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_user_0) contém o número de telefone de retorno de chamada do usuário.                       |
| RASPRIV \_ CallerSetCallback | Quando o usuário chama, o servidor RAS fornece a opção de especificar um número de telefone no qual chamar o usuário de volta. O usuário também pode optar por se conectar imediatamente sem a chamada de volta. O **membro szPhoneNumber** contém um número padrão que o usuário pode substituir. |



 

 

 