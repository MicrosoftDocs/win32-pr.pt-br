---
title: Definindo Process-Wide segurança usando DCOMCNFG
description: Talvez você queira habilitar a segurança para um aplicativo específico se um aplicativo tiver necessidades de segurança diferentes daqueles exigidos por outros aplicativos no computador.
ms.assetid: 04a7f688-78a3-490a-bcfa-862824a05422
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03174dd66e83a88724ff5d421d7b0dcb0c17699e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292884"
---
# <a name="setting-process-wide-security-using-dcomcnfg"></a>Definindo Process-Wide segurança usando DCOMCNFG

Talvez você queira habilitar a segurança para um aplicativo específico se um aplicativo tiver necessidades de segurança diferentes daqueles exigidos por outros aplicativos no computador. Por exemplo, você pode optar por usar configurações de todo o sistema para seus aplicativos que exigem um nível baixo de segurança ao definir um nível mais alto de segurança para um aplicativo específico.

No entanto, as configurações de segurança no registro que se aplicam a um aplicativo específico às vezes não são usadas. Por exemplo, as configurações de todo o processo que você definir no registro usando Dcomcnfg.exe serão substituídas se um cliente chamar [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) para definir a segurança para um determinado proxy de interface. Da mesma forma, se um cliente ou servidor (ou ambos) chamar [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) para definir a segurança para um processo, as configurações no registro serão ignoradas e os parâmetros especificados para **CoInitializeSecurity** serão usados em vez disso.

Ao habilitar a segurança para um aplicativo, várias configurações podem precisar ser modificadas. Isso inclui nível de autenticação, local, permissões de inicialização, permissões de acesso e identidade. Para obter os procedimentos passo a passo, consulte o seguinte:

-   [Definindo o nível de autenticação para um aplicativo](#setting-the-authentication-level-for-an-application)
-   [Configurando o local de um aplicativo](#setting-the-location-for-an-application)
-   [Definindo permissões de inicialização para um aplicativo](#setting-launch-permissions-for-an-application)
-   [Configurando permissões de acesso para um aplicativo](#setting-access-permissions-for-an-application)
-   [Definindo a identidade de um aplicativo](#setting-the-identity-for-an-application)
-   [Navegando no banco de dados do usuário](#browsing-the-user-database)
-   [Dcomcnfg.exe e aplicativos de 64 bits](#dcomcnfgexe-and-64-bit-applications)
-   [Tópicos relacionados](#related-topics)

## <a name="setting-the-authentication-level-for-an-application"></a>Definindo o nível de autenticação para um aplicativo

Para habilitar a segurança de um aplicativo, você deve definir um nível de autenticação diferente de nenhum. O nível de autenticação informa ao quanto a proteção de autenticação é necessária e pode variar de autenticar o cliente na primeira chamada de método para criptografar os Estados de parâmetros totalmente.

**Para definir o nível de autenticação de um aplicativo**

1.  Na página de propriedades **aplicativos** no Dcomcnfg.exe, selecione o aplicativo e clique no botão **Propriedades** (ou clique duas vezes no aplicativo selecionado).

2.  Na página **geral** , selecione um nível de autenticação diferente de **(nenhum)** na caixa de listagem **nível de autenticação** .

3.  Se você estiver definindo outras propriedades para este aplicativo, escolha o botão **aplicar** para aplicar o novo nível de autenticação. Clique em **OK** se você tiver terminado de definir as propriedades para este aplicativo e quiser aplicar as alterações.

## <a name="setting-the-location-for-an-application"></a>Configurando o local de um aplicativo

O local definido para seu aplicativo determina o computador no qual o aplicativo será executado. Você pode optar por executar o aplicativo no computador em que os dados estão localizados, no computador usado para definir o local ou em um computador especificado.

**Para definir o local de um aplicativo**

1.  Com Dcomcnfg.exe em execução, selecione o aplicativo na página **aplicativos** e escolha o botão **Propriedades** (ou clique duas vezes no aplicativo selecionado).

2.  Na página **local** , selecione uma ou mais caixas de seleção que correspondam aos locais em que você deseja que o aplicativo seja executado. Se você selecionar mais de uma caixa de seleção, COM usará a primeira que se aplica. Se Dcomcnfg.exe estiver sendo executado no computador servidor, sempre selecione **Executar aplicativo neste computador**.

3.  Se você estiver definindo outras propriedades para este aplicativo, escolha o botão **aplicar** para aplicar o novo local. Escolha **OK** se tiver terminado de definir as propriedades para este aplicativo e desejar aplicar as alterações.

## <a name="setting-launch-permissions-for-an-application"></a>Definindo permissões de inicialização para um aplicativo

Com Dcomcnfg.exe, você pode definir permissões de inicialização para controlar a lista de usuários que recebem ou negou permissão para iniciar um servidor específico. Você pode adicionar usuários ou grupos à lista, especificando se a permissão de acesso está sendo concedida ou negada. Você também pode remover usuários da lista.

**Para definir permissões de inicialização para um aplicativo**

1.  Com Dcomcnfg.exe em execução, selecione o aplicativo na página **aplicativos** e escolha o botão **Propriedades** (ou clique duas vezes no aplicativo selecionado).

2.  Na página de propriedades **segurança** , selecione o botão de opção **usar permissões de inicialização personalizadas** e escolha o botão **Editar** na mesma área.

3.  Para remover usuários ou grupos, selecione o usuário ou grupo que você deseja remover e escolha o botão **remover** . O usuário ou grupo selecionado não será mais exibido na caixa de listagem. Quando terminar de remover usuários e grupos, escolha **OK**.

4.  Se você quiser adicionar usuários ou grupos, escolha o botão **Adicionar** .

5.  Se você souber o nome de usuário totalmente qualificado que deseja adicionar, digite-o na caixa de texto **Adicionar nomes** . Se você não souber o nome de usuário, poderá procurar o banco de dados de usuário para localizá-lo (consulte navegando no banco de dados de usuário abaixo). Quando você localizar o nome de usuário, selecione o usuário ou grupo na caixa de listagem **nomes** e escolha o botão **Adicionar** .

6.  Na caixa de listagem **tipo de acesso** , selecione o tipo de acesso ( **permitir** inicialização ou **início de negação**). Para adicionar outros usuários que terão o tipo de acesso selecionado, repita a etapa 5. Quando terminar de adicionar usuários para o tipo de acesso selecionado, escolha o botão **OK** .

7.  Para adicionar usuários que terão um tipo diferente de acesso, repita as etapas 5 e 6. Caso contrário, escolha **OK** para aplicar as alterações.

## <a name="setting-access-permissions-for-an-application"></a>Configurando permissões de acesso para um aplicativo

Com o Dcomcnfg.exe, você pode gerenciar a lista de usuários com acesso concedido ou negado aos métodos de um servidor específico definindo permissões de acesso. Você pode adicionar usuários ou grupos à lista, especificando se a permissão de acesso está sendo concedida ou negada. Você também pode remover usuários da lista.

Ao definir permissões de acesso, você deve garantir que o sistema esteja incluído na lista de usuários que recebem acesso. Se você tiver concedido permissões de acesso a todos, o sistema estará incluído implicitamente.

O processo de configuração de permissões de acesso para um aplicativo é semelhante à definição de permissões de inicialização. As etapas são as seguintes.

**Para definir permissões de acesso para um aplicativo**

1.  Com Dcomcnfg.exe em execução, selecione o aplicativo na página **aplicativos** e escolha o botão **Propriedades** (ou clique duas vezes no aplicativo selecionado).

2.  Na página de propriedades **segurança** , selecione o botão de opção **usar permissões de acesso personalizadas** e escolha o botão **Editar** na mesma área.

3.  Para remover usuários ou grupos, selecione o usuário ou grupo que você deseja remover e escolha o botão **remover** . O usuário ou grupo selecionado não será mais exibido na caixa de listagem. Quando terminar de remover usuários e grupos, escolha **OK**.

4.  Se você quiser adicionar um usuário ou um grupo, escolha o botão **Adicionar** .

5.  Se você souber o nome de usuário totalmente qualificado que deseja adicionar, digite-o na caixa de texto **Adicionar nomes** . Se você não souber o nome de usuário, poderá procurar o banco de dados de usuário para localizá-lo. Quando você localizar o nome de usuário, selecione o usuário ou grupo na caixa de listagem **nomes** e escolha o botão **Adicionar** .

6.  Na caixa de listagem **tipo de acesso** , selecione o tipo de acesso ( **permitir** acesso ou **negar acesso**). Para adicionar outros usuários que terão o tipo de acesso selecionado, repita a etapa 5. Quando terminar de adicionar usuários para o tipo de acesso selecionado, escolha o botão **OK** .

7.  Para adicionar usuários que terão um tipo diferente de acesso, repita as etapas 5 e 6. Caso contrário, escolha **OK** para aplicar as alterações.

## <a name="setting-the-identity-for-an-application"></a>Definindo a identidade de um aplicativo

A identidade de um aplicativo é a conta usada para executar o aplicativo. A identidade pode ser a do usuário que está conectado no momento (o usuário interativo), a conta de usuário do processo do cliente que iniciou o servidor, um usuário especificado ou um serviço. Você pode usar Dcomcnfg.exe para escolher uma dessas identidades para o aplicativo. Para obter ajuda com a decisão de qual identidade deve ser definida para seu aplicativo, consulte [identidade do aplicativo](application-identity.md).

**Para definir a identidade de um aplicativo**

1.  Com Dcomcnfg.exe em execução, selecione o aplicativo na página **aplicativos** e escolha o botão **Propriedades** (ou clique duas vezes no aplicativo selecionado).

2.  Na página de propriedades **identidade** , selecione o botão de opção para a identidade desejada. Se você escolher **esse usuário**, deverá digitar o nome de usuário, a senha e a senha confirmada.

3.  Se você estiver definindo outras propriedades para este aplicativo, escolha o botão **aplicar** para aplicar a nova identidade. Escolha **OK** se tiver terminado de definir as propriedades para este aplicativo e desejar aplicar as alterações.

## <a name="browsing-the-user-database"></a>Navegando no banco de dados do usuário

Você procuraria o banco de dados de usuário em Dcomcnfg.exe quando precisar encontrar o nome de usuário totalmente qualificado para um usuário específico. Por exemplo, você pode procurar o banco de dados de usuário para localizar um usuário que você deseja adicionar para acessar ou iniciar permissões.

**Para procurar o banco de dados do usuário**

1.  Na caixa de listagem **nomes de lista** , selecione o domínio que contém o usuário ou grupo que você deseja adicionar.

2.  Para ver os usuários que pertencem ao domínio selecionado, escolha o botão **Mostrar usuários** .

3.  Para ver os membros de um grupo específico, selecione o grupo na caixa de listagem **nomes** e escolha o botão **Mostrar Membros** .

4.  Se você não conseguir localizar o usuário ou grupo que deseja adicionar, escolha o botão **Pesquisar** , que abre a caixa de diálogo **Localizar conta** . Selecione o domínio que você deseja pesquisar (ou selecione **Pesquisar tudo**), digite o nome de usuário que você deseja procurar e escolha o botão **Pesquisar** .

## <a name="dcomcnfgexe-and-64-bit-applications"></a>Dcomcnfg.exe e aplicativos de 64 bits

Em sistemas operacionais x64 do Windows XP para o Windows Server 2008, a versão de 64 bits do DCOMCNFG.EXE não configura corretamente os aplicativos DCOM de 32 bits para ativação remota. Esse comportamento faz com que os componentes que devem ser ativados remotamente sejam ativados localmente. Esse comportamento não ocorre no Windows 7 e no Windows Server 2008 R2 e em versões posteriores.

A solução alternativa é usar a versão de 32 bits do DCOMCNFG. Execute a versão de 32 bits do mmc.exe e carregue a versão de 32 bits do snap-in Serviços de componentes usando a linha de comando a seguir.

C: \\ Windows \\ SysWOW64>**MMC comexp. msc/32**

A versão de 32 bits dos serviços de componentes registra corretamente aplicativos DCOM de 32 bits para ativação remota.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Definindo Process-Wide segurança](setting-processwide-security.md)
</dt> </dl>

 

 




