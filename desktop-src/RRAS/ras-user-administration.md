---
title: Administração de usuário RAS
description: Um servidor RAS usa um banco de dados de conta de usuário que contém informações sobre um conjunto de contas de usuário.
ms.assetid: b58767b0-9b76-4d43-953a-ea772643745e
keywords:
- Administração de RAS RRAS, administração do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 742bf3e357ef813a60c67f991b6e5829879d3e1a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105812878"
---
# <a name="ras-user-administration"></a>Administração de usuário RAS

Um servidor RAS usa um banco de dados de conta de usuário que contém informações sobre um conjunto de contas de usuário. As informações incluem os privilégios de RAS de um usuário, que são um conjunto de sinalizadores de bits que determinam como o servidor RAS responde quando o usuário chama para conectar. As funções de administração do servidor RAS localizam o banco de dados da conta de usuário e obtêm e definem os privilégios de RAS para contas de usuário.

Um servidor RAS pode fazer parte de um domínio do sistema operacional ou pode ser um computador autônomo que executa a versão do servidor ou Professional do sistema operacional. Para um servidor que faz parte de um domínio, o banco de dados da conta de usuário é armazenado no servidor que é o controlador de domínio primário (PDC). Um servidor autônomo armazena seu próprio banco de dados de conta de usuário local. Para obter o nome do servidor que armazena o banco de dados de conta de usuário usado por um servidor RAS especificado, você pode chamar a função [**MprAdminGetPDCServer**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver) . Você pode usar o nome do servidor de conta de usuário em uma chamada para a função [**NetQueryDisplayInformation**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) para enumerar os usuários em um banco de dados de conta de usuário. Você também pode usar o nome do servidor em chamadas para as funções [**MprAdminUserGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo) e [**MprAdminUserSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo) para obter e definir os privilégios de RAS para uma conta de usuário especificada.

As funções [**MprAdminUserGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo) e [**MprAdminUserSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo) usam a estrutura do [**usuário do RAS \_ \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_user_0) para especificar os privilégios RAS de um usuário e o número de telefone de retorno. Os privilégios de RAS indicam as seguintes informações:

-   Se o usuário pode fazer uma conexão remota com o servidor ou o domínio ao qual o servidor pertence.
-   Se o usuário estabelece uma conexão por meio de um retorno de chamada, no qual o servidor RAS desliga e, em seguida, chama o usuário para estabelecer a conexão.

Cada conta de usuário especifica um dos sinalizadores a seguir para indicar os privilégios de retorno de chamada do usuário.



| Valor                      | Significado                                                                                                                                                                                                                                                                        |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RASPRIV \_ Nocallback        | O servidor RAS não chama de volta o usuário para estabelecer uma conexão.                                                                                                                                                                                                          |
| RASPRIV \_ AdminSetCallback  | Quando o usuário chama, o servidor RAS desliga e chama um número de telefone de retorno predefinido armazenado no banco de dados da conta do usuário. O membro **szPhoneNumber** da estrutura do [**usuário do RAS \_ \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_user_0) contém o número de telefone de retorno do usuário.                       |
| RASPRIV \_ CallerSetCallback | Quando o usuário chama, o servidor RAS fornece a opção de especificar um número de telefone no qual chamar de volta o usuário. O usuário também pode optar por se conectar imediatamente sem a chamada de retorno. O membro **szPhoneNumber** contém um número padrão que o usuário pode substituir. |



 

 

 