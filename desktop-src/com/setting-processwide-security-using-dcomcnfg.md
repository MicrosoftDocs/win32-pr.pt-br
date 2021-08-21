---
title: Definindo Process-Wide segurança usando DCOMCNFG
description: Talvez você queira habilitar a segurança para um aplicativo específico se um aplicativo tiver necessidades de segurança diferentes daquelas exigidas por outros aplicativos no computador.
ms.assetid: 04a7f688-78a3-490a-bcfa-862824a05422
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5ace37c685748983d36b8a1e27a406fb8a81034d82ab793e77c4def960dfa2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118309101"
---
# <a name="setting-process-wide-security-using-dcomcnfg"></a>Definindo Process-Wide segurança usando DCOMCNFG

Talvez você queira habilitar a segurança para um aplicativo específico se um aplicativo tiver necessidades de segurança diferentes daquelas exigidas por outros aplicativos no computador. Por exemplo, você pode optar por usar configurações de todo o sistema para seus aplicativos que exigem um nível baixo de segurança ao definir um nível mais alto de segurança para um aplicativo específico.

No entanto, as configurações de segurança no Registro que se aplicam a um aplicativo específico às vezes não são usadas. Por exemplo, as configurações em todo o processo que você definir no Registro usando Dcomcnfg.exe serão substituídos se um cliente chamar [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket) para definir a segurança de um proxy de interface específico. Da mesma forma, se um cliente ou servidor (ou ambos) chamar [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) para definir a segurança de um processo, as configurações no Registro serão ignoradas e os parâmetros especificados para **CoInitializeSecurity** serão usados em vez disso.

Ao habilear a segurança de um aplicativo, várias configurações podem precisar ser modificadas. Isso inclui nível de autenticação, local, permissões de lançamento, permissões de acesso e identidade. Para procedimentos passo a passo, consulte o seguinte:

-   [Definindo o nível de autenticação para um aplicativo](#setting-the-authentication-level-for-an-application)
-   [Definindo o local de um aplicativo](#setting-the-location-for-an-application)
-   [Definindo permissões de início para um aplicativo](#setting-launch-permissions-for-an-application)
-   [Definindo permissões de acesso para um aplicativo](#setting-access-permissions-for-an-application)
-   [Definindo a identidade de um aplicativo](#setting-the-identity-for-an-application)
-   [Navegando no banco de dados do usuário](#browsing-the-user-database)
-   [Dcomcnfg.exe aplicativos de 64 bits e de 64 bits](#dcomcnfgexe-and-64-bit-applications)
-   [Tópicos relacionados](#related-topics)

## <a name="setting-the-authentication-level-for-an-application"></a>Definindo o nível de autenticação para um aplicativo

Para habilitar a segurança de um aplicativo, você deve definir um nível de autenticação diferente de Nenhum. O nível de autenticação informa ao COM quanto a proteção de autenticação é necessária e pode variar de autenticar o cliente na primeira chamada de método para criptografar totalmente os estados do parâmetro.

**Para definir o nível de autenticação de um aplicativo**

1.  Na página **de** propriedades Aplicativos Dcomcnfg.exe, selecione o  aplicativo e clique no botão Propriedades (ou clique duas vezes no aplicativo selecionado).

2.  Na página **Geral,** selecione um nível de autenticação diferente **de (Nenhum)** na caixa **de listagem Nível** de Autenticação.

3.  Se você estiver definindo outras propriedades para esse aplicativo, escolha o **botão Aplicar** para aplicar o novo nível de autenticação. Clique **em OK** se tiver concluído a configuração de propriedades para este aplicativo e desejar aplicar as alterações.

## <a name="setting-the-location-for-an-application"></a>Definindo o local de um aplicativo

O local definido para seu aplicativo determina o computador no qual o aplicativo será executado. Você pode optar por executar seu aplicativo no computador em que os dados estão localizados, no computador que você usa para definir o local ou em um computador especificado.

**Para definir o local de um aplicativo**

1.  Com Dcomcnfg.exe em execução, selecione o  aplicativo na  página Aplicativos e escolha o botão Propriedades (ou clique duas vezes no aplicativo selecionado).

2.  Na página **Local,** marque uma ou mais caixas de seleção que correspondem aos locais em que você deseja que o aplicativo seja executado. Se você marcar mais de uma caixa de seleção, o COM usará o primeiro que se aplicar. Se Dcomcnfg.exe estiver sendo executado no computador servidor, sempre selecione Executar **Aplicativo neste computador.**

3.  Se você estiver definindo outras propriedades para esse aplicativo, escolha **o botão Aplicar** para aplicar o novo local. Escolha **OK** se tiver concluído a configuração de propriedades para este aplicativo e desejar aplicar as alterações.

## <a name="setting-launch-permissions-for-an-application"></a>Definindo permissões de início para um aplicativo

Com Dcomcnfg.exe, você pode definir permissões de lançamento para controlar a lista de usuários que têm permissão concedida ou negada para iniciar um servidor específico. Você pode adicionar usuários ou grupos à lista, especificando se a permissão de acesso está sendo concedida ou negada. Você também pode remover usuários da lista.

**Para definir permissões de lançamento para um aplicativo**

1.  Com Dcomcnfg.exe em execução, selecione o  aplicativo na  página Aplicativos e escolha o botão Propriedades (ou clique duas vezes no aplicativo selecionado).

2.  Na página **Propriedade** de segurança, selecione o botão de opção Usar permissões de lançamento **personalizadas** e escolha o **botão Editar** na mesma área.

3.  Para remover usuários ou grupos, selecione o usuário ou grupo que você deseja remover e escolha o **botão Remover.** O usuário ou grupo selecionado não aparecerá mais na caixa de listagem. Quando terminar de remover usuários e grupos, escolha **OK.**

4.  Se você quiser adicionar usuários ou grupos, escolha o **botão** Adicionar.

5.  Se você sabe o nome de usuário totalmente qualificado que deseja adicionar, digite-o na **caixa de texto Adicionar** Nomes. Se você não sabe o nome de usuário, pode procurar o banco de dados do usuário para encontrá-lo (consulte Navegando no Banco de Dados do Usuário abaixo). Quando você tiver localizado o nome de usuário, selecione o usuário ou grupo na caixa **de** listagem Nomes e escolha o **botão** Adicionar.

6.  Na caixa **de listagem Tipo** de Acesso, selecione o tipo de acesso **(permitir iniciar** ou negar a **lançamento).** Para adicionar outros usuários que terão o tipo de acesso selecionado, repita a etapa 5. Quando terminar de adicionar usuários para o tipo de acesso selecionado, escolha o **botão OK.**

7.  Para adicionar usuários que terão um tipo diferente de acesso, repita as etapas 5 e 6. Caso contrário, **escolha OK** para aplicar as alterações.

## <a name="setting-access-permissions-for-an-application"></a>Definindo permissões de acesso para um aplicativo

Com Dcomcnfg.exe, você pode gerenciar a lista de usuários que têm acesso concedido ou negado aos métodos de um servidor específico definindo permissões de acesso. Você pode adicionar usuários ou grupos à lista, especificando se a permissão de acesso está sendo concedida ou negada. Você também pode remover usuários da lista.

Ao definir permissões de acesso, você deve garantir que SYSTEM seja incluído na lista de usuários que têm acesso concedido. Se você tiver concedido permissões de acesso a Todos, SYSTEM será incluído implicitamente.

O processo de definição de permissões de acesso para um aplicativo é semelhante à configuração de permissões de lançamento. As etapas são as seguintes.

**Para definir permissões de acesso para um aplicativo**

1.  Com Dcomcnfg.exe em execução, selecione o  aplicativo na  página Aplicativos e escolha o botão Propriedades (ou clique duas vezes no aplicativo selecionado).

2.  Na página **Propriedade** de segurança, selecione o botão de opção Usar permissões **de acesso personalizadas** e escolha o **botão Editar** na mesma área.

3.  Para remover usuários ou grupos, selecione o usuário ou grupo que você deseja remover e escolha o **botão Remover.** O usuário ou grupo selecionado não aparecerá mais na caixa de listagem. Quando terminar de remover usuários e grupos, escolha **OK.**

4.  Se você quiser adicionar um usuário ou um grupo, escolha o **botão** Adicionar.

5.  Se você sabe o nome de usuário totalmente qualificado que deseja adicionar, digite-o na **caixa de texto Adicionar** Nomes. Se você não sabe o nome de usuário, pode procurar o banco de dados de usuário para encontrá-lo. Quando você tiver localizado o nome de usuário, selecione o usuário ou grupo na caixa **de** listagem Nomes e escolha o **botão** Adicionar.

6.  Na caixa **de listagem Tipo** de Acesso, selecione o tipo de acesso **(permitir acesso** ou negar **acesso**). Para adicionar outros usuários que terão o tipo de acesso selecionado, repita a etapa 5. Quando terminar de adicionar usuários para o tipo de acesso selecionado, escolha o **botão OK.**

7.  Para adicionar usuários que terão um tipo diferente de acesso, repita as etapas 5 e 6. Caso contrário, **escolha OK** para aplicar as alterações.

## <a name="setting-the-identity-for-an-application"></a>Definindo a identidade de um aplicativo

A identidade de um aplicativo é a conta usada para executar o aplicativo. A identidade pode ser a do usuário que está conectado no momento (o usuário interativo), a conta de usuário do processo do cliente que iniciou o servidor, um usuário especificado ou um serviço. Você pode usar Dcomcnfg.exe para escolher uma dessas identidades para o aplicativo. Para saber mais sobre qual identidade definir para seu aplicativo, confira [Identidade do Aplicativo.](application-identity.md)

**Para definir a identidade de um aplicativo**

1.  Com Dcomcnfg.exe em execução, selecione o  aplicativo na  página Aplicativos e escolha o botão Propriedades (ou clique duas vezes no aplicativo selecionado).

2.  Na página **de propriedades** Identidade, selecione o botão de opção para a identidade que você deseja. Se você escolher **Este Usuário**, deverá digitar o nome de usuário, a senha e a senha confirmada.

3.  Se você estiver definindo outras propriedades para esse aplicativo, escolha o **botão Aplicar** para aplicar a nova identidade. Escolha **OK** se tiver concluído a configuração de propriedades para este aplicativo e desejar aplicar as alterações.

## <a name="browsing-the-user-database"></a>Navegando no banco de dados do usuário

Você procuraria o banco de dados de usuário Dcomcnfg.exe quando precisar encontrar o nome de usuário totalmente qualificado para um usuário específico. Por exemplo, você pode procurar o banco de dados de usuário para localizar um usuário que deseja adicionar para permissões de acesso ou de lançamento.

**Para procurar o banco de dados do usuário**

1.  Na caixa **de listagem Nomes** de Lista de , selecione o domínio que contém o usuário ou grupo que você deseja adicionar.

2.  Para ver os usuários que pertencem ao domínio selecionado, escolha o **botão Mostrar** Usuários.

3.  Para ver os membros de um grupo específico, selecione o grupo na caixa de **listagem** Nomes e escolha o **botão Mostrar** Membros.

4.  Se você não conseguir localizar o usuário ou grupo que deseja adicionar, escolha o **botão** Pesquisar, que abrirá a caixa de **diálogo** Localizar Conta. Selecione o domínio que você deseja pesquisar (ou selecione **Pesquisar Tudo**), digite o nome de usuário que você deseja procurar e escolha o **botão** Pesquisar.

## <a name="dcomcnfgexe-and-64-bit-applications"></a>Dcomcnfg.exe aplicativos de 64 bits e de 64 bits

em sistemas operacionais x64 do Windows XP para o Windows Server 2008, a versão de 64 bits do DCOMCNFG.EXE não configura corretamente os aplicativos DCOM de 32 bits para ativação remota. Esse comportamento faz com que os componentes que devem ser ativados remotamente sejam ativados localmente. esse comportamento não ocorre no Windows 7 e no Windows Server 2008 R2 e em versões posteriores.

A solução alternativa é usar a versão de 32 bits do DCOMCNFG. Execute a versão de 32 bits do mmc.exe e carregue a versão de 32 bits do snap-in Serviços de componentes usando a linha de comando a seguir.

C: \\ Windows \\ SysWOW64>**MMC comexp. msc/32**

A versão de 32 bits dos serviços de componentes registra corretamente aplicativos DCOM de 32 bits para ativação remota.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Definindo Process-Wide segurança](setting-processwide-security.md)
</dt> </dl>

 

 




