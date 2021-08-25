---
description: Permite que os usuários executem tarefas comuns como não administradores, chamados de usuários padrão e como administradores sem precisar alternar usuários, fazer logoff ou usar Executar como.
ms.assetid: 8a7ba726-c2a6-4b7b-b664-3c6fcfbfb221
title: Controle de conta de usuário (autorização)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da0092ed5d8de1c141ba4ee2ea31a498bd6954ba8401aafeb08e6a69b8d130f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906826"
---
# <a name="user-account-control-authorization"></a>Controle de conta de usuário (autorização)

O UAC (Controle de Conta de Usuário) permite que os usuários executem tarefas comuns como não administradores, chamados de usuários padrão e como administradores sem precisar alternar usuários, fazer logoff ou usar **Executar como**. O comportamento do UAC para a configuração "Nunca notificar" não desabilita mais o UAC. A configuração "Nunca notificar" fornece um token de divisão e sempre eleva automaticamente o privilégio necessário. Essa sutileza pode fazer com que seu aplicativo tenha problemas de compatibilidade. Você ainda pode desabilitar o UAC usando Políticas de Grupo ou definindo manualmente a chave do Registro.

**Windows Server 2008 R2, Windows 7, Windows Server 2008 e Windows Vista:** A configuração "Nunca notificar" desabilita o UAC.

Por exemplo, se você executar as etapas a seguir para alterar a configuração "Nunca notificar", obterá resultados diferentes ao tentar criar um arquivo em uma pasta que exija privilégios elevados. O Windows 8 é negar o acesso. O Windows 7 permite que você crie o arquivo File.txt aplicativo.

1.  Clique ou toque em **Iniciar.** Na caixa de pesquisa, digite "Alterar configurações de Controle de Conta de Usuário".
2.  Clique ou toque **em Alterar configurações de Controle de Conta de Usuário** para abri-lo.
3.  Mova o controle deslizante para **Nunca notificar**.
4.  Clique ou toque em **OK.**
5.  Reinicie seu computador.
6.  Clique ou toque **em Iniciar** e, em **seguida, em Executar**. Na caixa **Abrir,** digite "Cmd.exe". Observe que o título da janela não contém a cadeia de caracteres "Administrador".
7.  Digite "echo > %windir% \\ system32 \\File.txt".

O UAC foi adicionado Windows Server 2008 e Windows Vista. Uma conta de usuário padrão é sinônimo de uma conta de usuário no Windows XP. As contas de usuário que são membros do grupo administradores local executarão a maioria dos aplicativos como um usuário padrão.

Para obter informações sobre o UAC, consulte os tópicos a seguir.



| Tópico                                                                                                                                        | Descrição                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [Diretrizes para controle de conta de usuário no desenvolvimento de interface do usuário](https://msdn.microsoft.com/library/aa511445(l=en-us,v=MSDN.10).aspx)<br/> | Informações gerais sobre o UAC.<br/>                                                                                                     |
| [Desenvolvendo aplicativos que exigem privilégios de administrador](developing-applications-that-require-administrator-privilege.md)<br/>  | Modelos para desenvolver aplicativos que executam operações que exigem privilégio administrativo, mas que são executados como um usuário padrão.<br/> |
| [Referência de autorização](authorization-reference.md)<br/>                                                                            | Informações detalhadas sobre funções de autorização, interfaces, estruturas e outros elementos de programação.<br/>                        |



 

 

 




