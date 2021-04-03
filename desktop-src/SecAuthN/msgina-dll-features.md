---
description: Se você estiver escrevendo uma GINA para substituir a DLL do Microsoft Standard GINA (MSGina.dll), talvez queira fornecer algumas ou todas as funcionalidades da GINA padrão.
ms.assetid: cd2ce7b7-6167-4451-9f6e-881676a2145c
title: Recursos de MSGina.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51833ab92e47dad01c13df004797e3ab3552b09a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829457"
---
# <a name="msginadll-features"></a>Recursos de MSGina.dll

Se você estiver escrevendo uma [*Gina*](../secgloss/g-gly.md) para substituir a DLL do Microsoft Standard GINA (MSGina.dll), talvez queira fornecer algumas ou todas as funcionalidades da Gina padrão. Veja a seguir uma lista de recursos padrão e uma breve descrição de como eles são controlados.

> [!Note]  
> As DLLs GINAs são ignoradas no Windows Vista.

 

Os valores de chave do registro controlam a disponibilidade ou o comportamento de muitos desses recursos padrão da GINA. Salvo indicação em contrário, esses valores de chave pertencem à chave do registro do Winlogon e têm um tipo de valor \[ reg \_ sz \] . O caminho real da chave do [*Winlogon*](../secgloss/w-gly.md) é:

**\\HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Winlogon**

-   **Caixa de diálogo notificação legal**

    Em alguns lugares, é legal que qualquer pessoa que tenha acesso a uma estação de trabalho faça logon e comece a trabalhar, a menos que haja um aviso indicando que o sistema é apenas para usuários autorizados. Além disso, muitos usuários desejam que as mensagens específicas da empresa sejam exibidas antes do logon normal. A GINA padrão usa dois valores de chave do registro do Winlogon para permitir que um sistema exiba informações antes do logon. Se o valor da chave estiver presente e contiver uma cadeia de caracteres não nula, uma caixa de diálogo de aviso legal será exibida antes da tela de boas-vindas usual. Esses nomes de valor de chave são mostrados na tabela a seguir.

    

    | Nome do valor da chave         | Sumário                                                            |
    |------------------------|---------------------------------------------------------------------|
    | **LegalNoticeCaption** | A cadeia de caracteres a ser exibida como a legenda da caixa de diálogo de aviso legal |
    | **LegalNoticeText**    | A cadeia de caracteres a ser exibida como a mensagem da caixa de diálogo de aviso legal |

    

     

-   **Exibir o último nome de usuário**

    Por padrão, a tela de logon exibe o nome do último usuário para fazer logon com êxito na estação de trabalho. Esse recurso é controlado pelo valor da chave do registro **DontDisplayLastUserName** . Quando esse valor de chave é definido como um, o nome de usuário não é exibido na caixa de diálogo de logon.

-   **Logon automático**

    Esse recurso permite que um sistema faça logon de um usuário automaticamente toda vez que o sistema é iniciado usando informações padrão e desabilitando a caixa de logon CTRL + ALT + DEL.

    Esse recurso usa os seguintes valores da chave Winlogon.

    

    | Valor                 | Sumário                                           |
    |-----------------------|----------------------------------------------------|
    | **AutoAdminLogon**    | 1                                                  |
    | **AutoLogonCount**    | O número de vezes para fazer um logon automático       |
    | **DefaultUserName**   | O nome da conta de usuário                       |
    | **DefaultDomainName** | O nome do domínio no qual a conta de usuário está |

    

     

    Se o valor da chave **AutoAdminLogon** estiver presente e contiver um, e o valor da chave **AutoLogonCount** não estiver presente, um logon automático ocorrerá sempre que o usuário atual fizer logoff ou o sistema for reiniciado. A conta na qual está sendo feito logon é especificada usando os valores de chave **DefaultUserName** e **DefaultDomainName** . A senha da conta pode ser especificada de uma das duas maneiras. Para computadores que executam um dos sistemas operacionais Windows Server 2003 ou Windows XP, a senha deve ser armazenada como um segredo usando a função [**LsaStorePrivateData**](/windows/win32/api/ntsecapi/nf-ntsecapi-lsastoreprivatedata) . Para obter detalhes, consulte [protegendo a senha de logon automático](protecting-the-automatic-logon-password.md). A outra maneira de armazenar a senha está em texto não criptografado na entrada **DefaultPassword** da chave Winlogon; para fins de segurança, essa técnica deve ser evitada. Se você armazenar a senha usando a função **LsaStorePrivateData** , não forneça uma entrada **DefaultPassword** na chave Winlogon.

    Se o valor da chave **AutoAdminLogon** estiver presente e contiver um, e se o valor da chave **AutoLogonCount** estiver presente e não for zero, **AutoLogonCount** determinará o número de logons automáticos que ocorrerem. Cada vez que o sistema é reiniciado, o valor de **AutoLogonCount** será decrementado em um até chegar a zero. Quando **AutoLogonCount** chega a zero, nenhuma conta será conectada automaticamente, o valor da chave **AutoLogonCount** e o valor da chave **DefaultPassword** , se usado, serão excluídos do registro e o **AutoAdminLogon** será definido como zero.

    Há uma limitação adicional ao uso de **AutoAdminLogon**: por padrão, MSGina.dll verifica o estado da tecla Shift quando o **AutoAdminLogon** é um. Se a tecla SHIFT for mantida durante o processo de inicialização, MSGina.dll ignorará o valor da chave **AutoAdminLogon** e solicitará ao usuário informações de identificação e autenticação interativamente. Esse é um recurso útil quando você está depurando um aplicativo dedicado. Para desabilitar o significado da tecla SHIFT, defina o valor da chave **IgnoreShiftOverride** como um.

-   **Permitir desligamento não autenticado**

    Você pode configurar a [*Gina*](../secgloss/g-gly.md) padrão para incluir um botão de **desligamento** na caixa de diálogo de logon. Isso permite que os usuários encerrem o sistema sem primeiro fazer logon. O valor de chave a seguir controla se esse botão está incluído.

    

    | Valor                    | Descrição                                           |
    |--------------------------|-------------------------------------------------------|
    | **ShutdownWithoutLogon** | Um para incluir o botão; zero para excluir o botão |

    

     

-   **Ativação deUserinit.exe**

    Userinit.exe é um aplicativo executado pelo MSGina.dll quando o usuário fez logon. Ele é executado no [*contexto*](../secgloss/c-gly.md) do usuário conectado recentemente e na área de trabalho do aplicativo. Sua finalidade é configurar o ambiente do usuário, incluindo a restauração de usos de rede, o estabelecimento de configurações de perfil, como fontes e cores de tela, e a execução de scripts de logon. Depois de concluir essas tarefas, Userinit.exe executará os programas do shell do usuário. Os programas do Shell herdam o ambiente que o Userinit.exe configura. Os programas de shell específicos que Userinit.exe executado são armazenados no valor de chave do **shell** na chave do registro do Winlogon.

    O valor da chave do **shell** pode conter uma lista separada por vírgulas de programas a serem executados. O Windows Explorer é o programa de shell padrão e será executado se o valor da chave do **shell** for nulo ou não estiver presente. Por padrão, o Windows Explorer está listado.

-   **Opções de segurança conectadas**

    Quando conectado, se um usuário inserir uma [*seqüência de atenção segura*](../secgloss/s-gly.md) (SAS), será apresentada uma tela de opções de segurança ao usuário. Entre as opções listadas estão:

    -   Desligue o sistema.
    -   Dê logoff.
    -   Altere a senha.
    -   Vá para a lista de tarefas.
    -   Bloquear a estação de trabalho.

    Uma GINA de substituição pode fornecer opções semelhantes quando um evento SAS é recebido enquanto um usuário faz logon.

 

 
