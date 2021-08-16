---
description: Se você estiver escrevendo um LTD para substituir o MSGina.dll (DLL) standard da Microsoft, talvez você queira fornecer algumas ou todas as funcionalidades PADRÃO DOIS.
ms.assetid: cd2ce7b7-6167-4451-9f6e-881676a2145c
title: MSGina.dll recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2acf5d1e7e9dccf9581b27ea2fef3deb1c2c8aa218a1b0a711b7015134e1d2d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117786745"
---
# <a name="msginadll-features"></a>MSGina.dll recursos

Se você estiver escrevendo um [*LTD*](../secgloss/g-gly.md) para substituir o MSGina.dll (DLL) standard da Microsoft, talvez você queira fornecer algumas ou todas as funcionalidades PADRÃO DOIS. Veja a seguir uma lista de recursos padrão e uma breve descrição de como eles são controlados.

> [!Note]  
> As DLLs DE VALOR são ignoradas no Windows Vista.

 

Os valores de chave do Registro controlam a disponibilidade ou o comportamento de muitos desses recursos PADRÃO DOIS. A menos que seja notado de outra forma, esses valores de chave pertencem à chave do Registro winlogon e têm um tipo de valor \[ REG \_ SZ \] . O caminho real da [*chave Winlogon*](../secgloss/w-gly.md) é:

**\\HKEY \_ LOCAL MACHINE Software Microsoft Windows NT \_ \\ \\ \\ \\ CurrentVersion \\ Winlogon**

-   **Caixa de diálogo Notificação Legal**

    Em alguns lugares, é legal que qualquer pessoa que tenha acesso a uma estação de trabalho faça logoff e comece a trabalhar, a menos que haja um aviso indicando que o sistema é somente para usuários autorizados. Além disso, muitos usuários querem mensagens específicas da empresa exibidas antes do logon normal. O PADRÃO DEIS usa dois valores de chave do Registro winlogon para permitir que um sistema ex display informações antes do logon. Se um dos valores de chave estiver presente e contiver uma cadeia de caracteres não nula, uma caixa de diálogo Aviso Legal será exibida antes da tela de boas-vindas. Esses nomes de valor de chave são mostrados na tabela a seguir.

    

    | Nome do valor da chave         | Sumário                                                            |
    |------------------------|---------------------------------------------------------------------|
    | **LegalNoticeCaption** | A cadeia de caracteres a ser exibida como a legenda da caixa de diálogo de aviso legal |
    | **LegalNoticeText**    | A cadeia de caracteres a ser exibida como a mensagem da caixa de diálogo de aviso legal |

    

     

-   **Exibir o sobrenome do usuário**

    Por padrão, a tela de logon exibe o nome do último usuário para fazer logon com êxito na estação de trabalho. Esse recurso é controlado pelo valor da chave do Registro **DontDisplayLastUserName.** Quando esse valor de chave é definido como um, o nome de usuário não é exibido na caixa de diálogo de logon.

-   **Logon automático**

    Esse recurso permite que um sistema faça logon automaticamente em um usuário sempre que o sistema é iniciado usando informações padrão e desabilitando a caixa de logon CTRL+ALT+DEL.

    Esse recurso usa os seguintes valores da chave Winlogon.

    

    | Valor                 | Sumário                                           |
    |-----------------------|----------------------------------------------------|
    | **AutoAdminLogon**    | 1                                                  |
    | **AutoLogonCount**    | O número de vezes para fazer um logon automático       |
    | **Defaultusername**   | O nome da conta de usuário                       |
    | **DefaultDomainName** | O nome do domínio em que a conta de usuário está |

    

     

    Se o valor da chave **AutoAdminLogon** estiver presente e contiver um, e o valor da chave **AutoLogonCount** não estiver presente, um logon automático ocorrerá sempre que o usuário atual for desligado ou o sistema for reiniciado. A conta que está sendo registrada é especificada usando os valores de chave **DefaultUserName** **e DefaultDomainName.** A senha da conta pode ser especificada de duas maneiras. Para computadores que executam um dos sistemas operacionais Windows Server 2003 ou Windows XP, a senha deve ser armazenada como um segredo usando a função [**LsaStorePrivateData.**](/windows/win32/api/ntsecapi/nf-ntsecapi-lsastoreprivatedata) Para obter detalhes, consulte [Protegendo a senha de logon automático](protecting-the-automatic-logon-password.md). A outra maneira de armazenar a senha é em texto não criptografado na **entrada DefaultPassword** da chave Winlogon; para fins de segurança, essa técnica deve ser evitada. Se você armazenar a senha usando a **função LsaStorePrivateData,** não forneça uma **entrada DefaultPassword** na chave Winlogon.

    Se o valor da chave **AutoAdminLogon** estiver presente e contiver um e se o valor da chave **AutoLogonCount** estiver presente e não for zero, **AutoLogonCount** determinará o número de logons automáticos que ocorrem. Sempre que o sistema for reiniciado, o valor de **AutoLogonCount** será decrementado em um até atingir zero. Quando **AutoLogonCount** atingir zero, nenhuma conta será registrada automaticamente, o valor da chave **AutoLogonCount** e o valor da chave **DefaultPassword,** se usados, serão excluídos do Registro e **AutoAdminLogon** será definido como zero.

    Há uma ressalva adicional ao uso **de AutoAdminLogon:** por padrão, MSGina.dll verifica o estado da chave SHIFT quando **AutoAdminLogon** é um. Se a tecla SHIFT for mantida para baixo durante o processo de inicialização, MSGina.dll ignorará o valor da chave **AutoAdminLogon** e solicitará ao usuário informações de identificação e autenticação interativamente. Esse é um recurso útil quando você está depurando um aplicativo dedicado. Para desabilitar o significado da tecla SHIFT, de definir o valor da chave **IgnoreShiftOverride** como um.

-   **Permitir desligamento não autenticado**

    Você pode configurar o [*VALOR PADRÃO*](../secgloss/g-gly.md) para incluir um **botão Desligar** na caixa de diálogo de logon. Isso permite que os usuários desliguem o sistema sem fazer logo on primeiro. O valor da chave a seguir controla se esse botão está incluído.

    

    | Valor                    | Descrição                                           |
    |--------------------------|-------------------------------------------------------|
    | **ShutdownWithoutLogon** | Um para incluir o botão; zero para excluir o botão |

    

     

-   **AtivaçãoUserinit.exe dados**

    Userinit.exe é um aplicativo que é executado pelo MSGina.dll quando o usuário fez logo on. Ele é executado no contexto do usuário recém-conectado [*e*](../secgloss/c-gly.md) na área de trabalho do aplicativo. Sua finalidade é configurar o ambiente do usuário, incluindo restaurar usos de rede, estabelecer configurações de perfil, como fontes e cores de tela, e executar scripts de logon. Depois de concluir essas tarefas, Userinit.exe executa os programas de shell de usuário. Os programas de shell herdam o ambiente que Userinit.exe configura. Os programas de shell específicos Userinit.exe executados são armazenados no valor da chave do **Shell** na chave do Registro do Winlogon.

    O valor da chave do **Shell** pode conter uma lista separada por vírgulas de programas a serem executados. Windows O Explorer é o programa de shell padrão e será executado se o valor da chave do **Shell** for nulo ou não estiver presente. Por padrão, o Windows Explorer é listado.

-   **Opções de segurança de logon**

    Quando conectado, se um usuário inserir uma SAS [*(sequência*](../secgloss/s-gly.md) de atenção segura), o usuário será apresentado com uma tela de opções de segurança. Entre as opções listadas estão:

    -   Desligue o sistema.
    -   Dê logoff.
    -   Altere a senha.
    -   Vá para a lista de tarefas.
    -   Bloqueie a estação de trabalho.

    Um DEVEIS de substituição pode fornecer opções semelhantes quando um evento SAS é recebido enquanto um usuário está conectado.

 

 
