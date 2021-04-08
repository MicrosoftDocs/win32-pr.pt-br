---
description: Permite que os usuários executem tarefas comuns como não administradores, chamados de usuários padrão e como administradores sem precisar alternar usuários, fazer logoff ou usar Executar como.
ms.assetid: 8a7ba726-c2a6-4b7b-b664-3c6fcfbfb221
title: Controle de conta de usuário (autorização)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be7f3cd8f31dda8f1b15145bc4003fc9ede8782c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922451"
---
# <a name="user-account-control-authorization"></a>Controle de conta de usuário (autorização)

O UAC (controle de conta de usuário) permite que os usuários executem tarefas comuns como não administradores, chamados de usuários padrão e como administradores sem precisar alternar usuários, fazer logoff ou usar **Executar como**. O comportamento do UAC para a configuração "nunca notificar" não desabilita mais o UAC. A configuração "nunca notificar" fornece um token de divisão e sempre eleva automaticamente o privilégio necessário. Essa sutileza pode fazer com que seu aplicativo tenha problemas de compatibilidade. Você ainda pode desabilitar o UAC usando políticas de grupo ou definindo manualmente a chave do registro.

**Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** A configuração "nunca notificar" desabilita o UAC.

Por exemplo, se você executar as etapas a seguir para alterar a configuração "nunca notificar", obterá resultados diferentes ao tentar criar um arquivo em uma pasta que exija privilégios elevados. O comportamento do Windows 8 é negar o acesso. O comportamento do Windows 7 permite que você crie o arquivo de File.txt.

1.  Clique ou toque em **Iniciar**. Na caixa de pesquisa, digite "alterar configurações de controle de conta de usuário".
2.  Clique ou toque em **alterar configurações de controle de conta de usuário** para abri-lo.
3.  Mova o controle deslizante para **nunca notificar**.
4.  Clique ou toque em **OK**.
5.  Reinicie seu computador.
6.  Clique ou toque em **Iniciar** e em **executar**. Na caixa **abrir** , digite "Cmd.exe". Observe que o título da janela não contém a cadeia de caracteres "administrador".
7.  Digite "Echo >% windir% \\ system32 \\File.txt".

O UAC foi adicionado no Windows Server 2008 e no Windows Vista. Uma conta de usuário padrão é sinônimo de uma conta de usuário no Windows XP. As contas de usuário que são membros do grupo Administradores local executarão a maioria dos aplicativos como um usuário padrão.

Para obter informações sobre o UAC, consulte os tópicos a seguir.



| Tópico                                                                                                                                        | Descrição                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [Diretrizes para controle de conta de usuário no desenvolvimento de IU](https://msdn.microsoft.com/library/aa511445(l=en-us,v=MSDN.10).aspx)<br/> | Informações gerais sobre o UAC.<br/>                                                                                                     |
| [Desenvolvendo aplicativos que exigem privilégios de administrador](developing-applications-that-require-administrator-privilege.md)<br/>  | Modelos para desenvolvimento de aplicativos que executam operações que exigem privilégio administrativo, mas que são executados como um usuário padrão.<br/> |
| [Referência de autorização](authorization-reference.md)<br/>                                                                            | Informações detalhadas sobre funções de autorização, interfaces, estruturas e outros elementos de programação.<br/>                        |



 

 

 




