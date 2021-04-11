---
title: Administração de conta de usuário RAS
description: Um servidor RAS do Windows NT 4,0 usa um banco de dados de conta de usuário que contém informações sobre um conjunto de contas de usuário.
ms.assetid: 653307f8-3b14-474a-9094-03a2d4c89092
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 521d090fc16e7d731525b79493119f3c604e043c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294142"
---
# <a name="ras-user-account-administration"></a>Administração de conta de usuário RAS

Um servidor RAS do Windows NT 4,0 usa um banco de dados de conta de usuário que contém informações sobre um conjunto de contas de usuário. As informações incluem os privilégios de RAS de um usuário, que são um conjunto de sinalizadores de bits que determinam como o servidor RAS responde quando o usuário chama para conectar. As funções de administração do servidor RAS permitem que você localize o banco de dados da conta de usuário e obtenha e defina os privilégios de RAS para contas de usuário.

Um servidor RAS do Windows NT 4,0 pode fazer parte de um domínio do Windows NT/Windows 2000 ou pode ser um servidor Windows NT autônomo ou uma estação de trabalho que não faz parte de um domínio. Para um servidor que faz parte de um domínio, o banco de dados da conta de usuário é armazenado no servidor que é o controlador de domínio primário (PDC). Um servidor autônomo armazena seu próprio banco de dados de conta de usuário local. Para obter o nome do servidor que armazena o banco de dados de conta de usuário usado por um servidor RAS especificado, você pode chamar a função [**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) . Você pode usar o nome do servidor de conta de usuário em uma chamada para a função [**NetQueryDisplayInformation**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) para enumerar os usuários em um banco de dados de conta de usuário. Você também pode usar o nome do servidor em chamadas para as funções [**RasAdminUserGetInfo**](rasadminusergetinfo.md) e [**RasAdminUserSetInfo**](rasadminusersetinfo.md) para obter e definir os privilégios de RAS para uma conta de usuário especificada.

As funções [**RasAdminUserGetInfo**](rasadminusergetinfo.md) e [**RasAdminUserSetInfo**](rasadminusersetinfo.md) usam a estrutura do [**usuário do RAS \_ \_ 0**](ras-user-0-str.md) para especificar os privilégios RAS de um usuário e o número de telefone de retorno. Os privilégios de RAS indicam as seguintes informações:

-   Se o usuário pode fazer uma conexão remota com o servidor ou o domínio ao qual o servidor pertence.
-   Se o usuário pode estabelecer uma conexão por meio de um retorno de chamada, no qual o servidor RAS desliga e, em seguida, chama o usuário para estabelecer a conexão.

Cada conta de usuário especifica um dos sinalizadores a seguir para indicar o privilégio de retorno de chamada do usuário.



| Valor                      | Significado                                                                                                                                                                                                                                                      |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RASPRIV \_ Nocallback        | O servidor RAS não chamará de volta o usuário para estabelecer uma conexão.                                                                                                                                                                                        |
| RASPRIV \_ AdminSetCallback  | Quando o usuário chama, o servidor RAS desliga e chama um número de telefone de retorno predefinido armazenado no banco de dados da conta do usuário. O membro **szPhoneNumber** da estrutura do [**usuário do RAS \_ \_ 0**](ras-user-0-str.md) contém o número de telefone de retorno do usuário. |
| RASPRIV \_ CallerSetCallback | Quando o usuário chama, o servidor RAS fornece a opção de especificar um número de telefone de retorno. O usuário também pode optar por se conectar imediatamente sem um retorno de chamada. O membro **szPhoneNumber** contém um número padrão que o usuário pode substituir.      |



 

 

 