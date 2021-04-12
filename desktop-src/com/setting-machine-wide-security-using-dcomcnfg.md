---
title: Definindo System-Wide segurança usando DCOMCNFG
description: Quando desejar que todos os aplicativos em um computador que não fornecem sua própria segurança compartilhem as mesmas configurações de segurança padrão, você definirá a segurança em todo o sistema.
ms.assetid: 23d1e222-c00b-497c-adc8-4ae14c5bdd98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7feaaf356263a48c2c93eb9b3b3764b7352cd39
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364214"
---
# <a name="setting-system-wide-security-using-dcomcnfg"></a>Definindo System-Wide segurança usando DCOMCNFG

Alterar as configurações de segurança de todo o sistema afetará todos os aplicativos de servidor COM que não definem sua própria segurança em todo o processo. Isso pode impedir que esses aplicativos funcionem corretamente. Se você estiver alterando as configurações de segurança de todo o sistema para afetar as configurações de segurança de um determinado aplicativo COM, em vez disso, deverá alterar as configurações de segurança de todo o processo para esse aplicativo COM específico. Para obter mais informações sobre como definir a segurança de todo o processo, consulte [definindo a segurança de todo o processo](setting-processwide-security.md).

Quando desejar que todos os aplicativos em um computador que não fornecem sua própria segurança compartilhem as mesmas configurações de segurança padrão, você definirá a segurança em todo o sistema. O uso de Dcomcnfg.exe facilita a definição de valores padrão no registro que se aplicam a todos os aplicativos em um computador.

É importante entender que, se o cliente ou o servidor chamar explicitamente [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) para definir a segurança em todo o processo, as configurações padrão no registro serão ignoradas e os parâmetros para **CoInitializeSecurity** serão usados em vez das configurações de segurança para o processo. Além disso, se você usar Dcomcnfg.exe para especificar configurações de segurança para um processo específico, as configurações padrão do computador serão substituídas pelas configurações do processo.

Ao habilitar a segurança em todo o sistema, você deve definir o nível de autenticação para um valor diferente de nenhum e deve definir as permissões de inicialização e acesso. Você tem a opção de definir o nível de representação padrão e também pode habilitar o controle de referência. Os tópicos a seguir fornecem procedimentos passo a passo:

-   [Definindo System-Wide nível de autenticação padrão](#setting-system-wide-default-authentication-level)
-   [Definindo System-Wide permissões de inicialização](#setting-system-wide-launch-permissions)
-   [Configurando permissões de acesso de System-Wide](#setting-system-wide-access-permissions)
-   [Definindo System-Wide nível de representação](#setting-system-wide-impersonation-level)
-   [Definindo System-Wide acompanhamento de referência](#setting-system-wide-reference-tracking)
-   [Habilitando e desabilitando o DCOM](#enabling-and-disabling-dcom)
-   [Tópicos relacionados](#related-topics)

## <a name="setting-system-wide-default-authentication-level"></a>Definindo System-Wide nível de autenticação padrão

O nível de autenticação é usado para informar ao COM em qual nível você deseja que o cliente seja autenticado. Esses níveis oferecem vários níveis de proteção, de nenhuma proteção à criptografia completa. Para habilitar a segurança de um computador, você precisa escolher um nível de autenticação diferente de nenhum. Você pode escolher essa configuração, usando Dcomcnfg.exe, concluindo as etapas a seguir.

**Para definir o nível de autenticação com base em todo o sistema**

1.  Execute Dcomcnfg.exe.

2.  Escolha a guia **propriedades padrão** .

3.  Na caixa de listagem **nível de AuthenticationÂ de DefaultÂ** , escolha um valor diferente de **(nenhum)**.

4.  Se você estiver configurando mais propriedades para o computador, clique no botão **aplicar** para aplicar o novo nível de autenticação. Caso contrário, clique em **OK** para aplicar as alterações e sair Dcomcnfg.exe.

## <a name="setting-system-wide-launch-permissions"></a>Definindo System-Wide permissões de inicialização

As permissões de inicialização definidas com Dcomcnfg.exe determinam uma lista de usuários, sendo que cada um deles tem permissão explicitamente concedida ou negada para iniciar qualquer servidor que não forneça suas próprias configurações de permissão de inicialização. Ao definir permissões de inicialização, você pode adicionar ou remover um ou mais usuários ou grupos dessa lista. Para cada usuário que você adicionar, você deve especificar se a permissão de inicialização do usuário está sendo concedida ou negada.

**Para definir permissões de inicialização para um computador**

1.  Na página de propriedades de **segurança padrão** no Dcomcnfg.exe, escolha o botão **Editar padrão** na área **permissões de inicialização padrão** .

2.  Para remover usuários ou grupos, selecione o usuário ou grupo que você deseja remover e escolha o botão **remover** . O usuário ou grupo selecionado não será mais exibido na caixa de listagem. Quando terminar de remover usuários e grupos, escolha **OK**.

3.  Se você quiser adicionar um usuário ou grupo, escolha o botão **Adicionar** .

4.  Se você souber o nome de usuário totalmente qualificado que deseja adicionar, digite-o na caixa de texto **Adicionar nomes** . Se você não souber o nome de usuário, consulte **definindo a segurança do processwide usando DCOMCNFG** para localizá-lo. Quando você localizar o nome de usuário, selecione o usuário ou grupo na caixa de listagem **nomes** e escolha o botão **Adicionar** .

5.  Na caixa de listagem **tipo de acesso** , selecione o tipo de acesso ( **permitir** inicialização ou **início de negação**). Para adicionar outros usuários que também terão o tipo de acesso selecionado, repita a etapa 4. Quando terminar de adicionar usuários para o tipo de acesso selecionado, escolha o botão **OK** .

6.  Para adicionar usuários que terão um tipo diferente de acesso, repita as etapas 4 e 5. Caso contrário, escolha **OK** para aplicar as alterações.

## <a name="setting-system-wide-access-permissions"></a>Configurando permissões de acesso de System-Wide

Dcomcnfg.exe permite que você defina permissões de acesso para controlar a lista de usuários com acesso concedido ou negado aos métodos desses servidores que não fornecem suas próprias permissões de acesso. Você pode adicionar usuários ou grupos à lista, especificando se a permissão de acesso está sendo concedida ou negada. Você também pode remover usuários da lista.

Ao definir permissões de acesso, você deve garantir que o sistema esteja incluído na lista de usuários que recebem acesso. Se você tiver concedido permissões de acesso a todos, o sistema estará incluído implicitamente.

O processo de configuração de permissões de acesso para um computador é semelhante à definição de permissões de inicialização. As etapas a seguir devem ser executadas.

**Para definir permissões de acesso para um computador**

1.  Na página de propriedades de **segurança padrão** no Dcomcnfg.exe, escolha o botão **Editar padrão** na área **permissões de acesso padrão** .

2.  Para remover usuários ou grupos, selecione o usuário ou grupo que você deseja remover e escolha o botão **remover** . O usuário ou grupo selecionado não será mais exibido na caixa de listagem. Quando terminar de remover usuários e grupos, escolha **OK**.

3.  Se você quiser adicionar um usuário ou um grupo, escolha o botão **Adicionar** .

4.  Se você souber o nome de usuário totalmente qualificado que deseja adicionar, digite-o na caixa de texto **Adicionar nomes** . Se você não souber o nome de usuário, consulte [definindo a segurança de todo o processo usando DCOMCNFG](setting-processwide-security-using-dcomcnfg.md) para localizá-lo. Quando você localizar o nome de usuário, selecione o usuário ou grupo na caixa de listagem **nomes** e escolha o botão **Adicionar** .

5.  Na caixa de listagem **tipo de acesso** , selecione o tipo de acesso ( **permitir** acesso ou **negar acesso**). Para adicionar outros usuários que terão o tipo de acesso selecionado, repita a etapa 4. Quando terminar de adicionar usuários para o tipo de acesso selecionado, escolha o botão **OK** .

6.  Para adicionar usuários que terão um tipo diferente de acesso, repita as etapas 4 e 5. Caso contrário, escolha **OK** para aplicar as alterações.

## <a name="setting-system-wide-impersonation-level"></a>Definindo System-Wide nível de representação

O nível de representação, definido pelo cliente, determina a quantidade de autoridade atribuída ao servidor para atuar em nome do cliente. Por exemplo, quando o cliente tiver definido seu nível de representação como delegado, o servidor poderá acessar recursos locais e remotos como o cliente, e o servidor poderá encobrir vários limites de computador se o recurso de encobrimento estiver definido. Para ajudar a determinar qual nível de representação deve ser escolhido, consulte [níveis de representação](impersonation-levels.md) e [encobrimento](cloaking.md).

Definir o nível de representação padrão para todo o computador informa ao COM qual nível de representação usar quando um cliente específico no computador não especifica um nível de representação programaticamente usando [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ou [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket).

**Para definir o nível de representação de um computador**

1.  Com Dcomcnfg.exe em execução, escolha a guia **propriedades padrão** .

2.  Na caixa de listagem **nível de representação padrão** , escolha o nível de representação desejado.

3.  Se você estiver configurando mais propriedades para o computador, escolha o botão **aplicar** para aplicar o novo nível de representação. Caso contrário, escolha **OK** para aplicar as alterações e sair Dcomcnfg.exe.

## <a name="setting-system-wide-reference-tracking"></a>Definindo System-Wide acompanhamento de referência

Quando você habilita o acompanhamento de referência, está solicitando que o COM faça verificações de segurança adicionais e mantenha o controle das informações que impedirão que os objetos sejam lançados muito cedo. Tenha em mente que essas verificações adicionais são caras. Para obter mais informações sobre o acompanhamento de referência, consulte [acompanhamento de referência](reference-tracking.md). Use as etapas a seguir para habilitar ou desabilitar o acompanhamento de referência.

**Para definir o acompanhamento de referência para um computador**

1.  Com Dcomcnfg.exe em execução, escolha a guia **propriedades padrão** .

2.  Para habilitar (ou desabilitar) o acompanhamento de referência, marque (ou desmarque) a caixa de seleção **fornecer segurança adicional para acompanhamento de referência** , próxima à parte inferior da página.

3.  Se você estiver configurando mais propriedades para o computador, escolha o botão **aplicar** para aplicar a nova configuração. Caso contrário, escolha **OK** para aplicar as alterações e sair Dcomcnfg.exe.

## <a name="enabling-and-disabling-dcom"></a>Habilitando e desabilitando o DCOM

Quando um computador faz parte de uma rede, o protocolo de transmissão DCOM permite que objetos COM nesse computador se comuniquem com objetos COM em outros computadores. Você pode desabilitar o DCOM para um computador específico, mas isso desabilitará toda a comunicação entre objetos nesse computador e objetos em outros computadores.

Desabilitar o DCOM em um computador não tem nenhum efeito sobre objetos COM locais. COM ainda procura permissões de inicialização que você especificou. Se nenhuma permissão de inicialização tiver sido especificada, as permissões de inicialização padrão serão usadas. Mesmo que você desabilite o DCOM, se um usuário tiver acesso físico ao computador, ele poderá iniciar um servidor no computador, a menos que você defina as permissões de inicialização para não permiti-lo.

> [!Note]  
> Se você desabilitar o DCOM em um computador remoto, não poderá acessar remotamente esse computador posteriormente para reabilitar o DCOM. Para reabilitar o DCOM, você precisará de acesso físico a esse computador.

 

**Para habilitar (ou desabilitar) manualmente o DCOM para um computador**

1.  Execute Dcomcnfg.exe.

2.  Escolha a guia **Propriedades do DefaultÂ** .

3.  Marque (ou desmarque) a caixa de seleção **habilitar COMÂ distribuído neste computador** .

4.  Se você estiver configurando mais propriedades para o computador, clique no botão **aplicar** para habilitar (ou desabilitar) DCOM. Caso contrário, clique em **OK** para aplicar as alterações e sair Dcomcnfg.exe.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Definindo a segurança de todo o processo](setting-processwide-security.md)
</dt> </dl>

 

 




