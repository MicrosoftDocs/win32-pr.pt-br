---
title: Definindo System-Wide segurança usando DCOMCNFG
description: Quando você quiser que todos os aplicativos em um computador que não forneçam sua própria segurança compartilhem as mesmas configurações de segurança padrão, você definirá a segurança em todo o sistema.
ms.assetid: 23d1e222-c00b-497c-adc8-4ae14c5bdd98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7914fd3b1561900426e2928a5277cb845918e3b8d1b1ad1569ea8db0d112e218
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954366"
---
# <a name="setting-system-wide-security-using-dcomcnfg"></a>Definindo System-Wide segurança usando DCOMCNFG

Alterar as configurações de segurança em todo o sistema afetará todos os aplicativos de servidor COM que não configuram sua própria segurança em todo o processo. Isso pode impedir que esses aplicativos funcionam corretamente. Se você estiver alterando as configurações de segurança de todo o sistema para afetar as configurações de segurança de um aplicativo COM específico, deverá alterar as configurações de segurança em todo o processo para esse aplicativo COM específico. Para obter mais informações sobre como definir a segurança em todo o processo, consulte [Configurando a segurança em todo o processo.](setting-processwide-security.md)

Quando você quiser que todos os aplicativos em um computador que não forneçam sua própria segurança compartilhem as mesmas configurações de segurança padrão, você definirá a segurança em todo o sistema. Usar Dcomcnfg.exe facilita a definição de valores padrão no Registro que se aplicam a todos os aplicativos em um computador.

É importante entender que, se o cliente ou o servidor chamar explicitamente [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) para definir a segurança em todo o processo, as configurações padrão no Registro serão ignoradas e os parâmetros para **CoInitializeSecurity** serão usados em vez das configurações de segurança para o processo. Além disso, se você usar Dcomcnfg.exe para especificar configurações de segurança para um processo específico, as configurações padrão do computador serão substituídos pelas configurações do processo.

Ao habilenciar a segurança em todo o sistema, você deve definir o nível de autenticação como um valor diferente de Nenhum e definir permissões de início e acesso. Você tem a opção de definir o nível de representação padrão e também pode habilitar o acompanhamento de referência. Os tópicos a seguir fornecem procedimentos passo a passo:

-   [Definindo System-Wide nível de autenticação padrão](#setting-system-wide-default-authentication-level)
-   [Definindo System-Wide permissões de início](#setting-system-wide-launch-permissions)
-   [Definindo System-Wide permissões de acesso](#setting-system-wide-access-permissions)
-   [Definindo System-Wide nível de representação](#setting-system-wide-impersonation-level)
-   [Definindo System-Wide acompanhamento de referência](#setting-system-wide-reference-tracking)
-   [Habilitando e desabilitando o DCOM](#enabling-and-disabling-dcom)
-   [Tópicos relacionados](#related-topics)

## <a name="setting-system-wide-default-authentication-level"></a>Definindo System-Wide nível de autenticação padrão

O nível de autenticação é usado para dizer ao COM em qual nível você deseja que o cliente seja autenticado. Esses níveis oferecem vários níveis de proteção, desde nenhuma proteção até criptografia completa. Para habilitar a segurança de um computador, você precisa escolher um nível de autenticação diferente de Nenhum. Você pode escolher essa configuração usando Dcomcnfg.exe, concluindo as etapas a seguir.

**Para definir o nível de autenticação em todo o sistema**

1.  Execute Dcomcnfg.exe.

2.  Escolha a **guia Propriedades** Padrão.

3.  Na caixa **de listagem Nível de Autenticação** Padrão, escolha um valor diferente **de (Nenhum)**.

4.  Se você estiver definindo mais propriedades para o computador, clique no **botão Aplicar** para aplicar o novo nível de autenticação. Caso contrário, **clique em OK** para aplicar as alterações e sair Dcomcnfg.exe.

## <a name="setting-system-wide-launch-permissions"></a>Definindo System-Wide permissões de início

As permissões de lançamento definidas com Dcomcnfg.exe determinam uma lista de usuários, cada um dos quais tem permissão explicitamente concedida ou negada para iniciar qualquer servidor que não forneça suas próprias configurações de permissão de lançamento. Ao definir permissões de lançamento, você pode adicionar ou remover um ou mais usuários ou grupos dessa lista. Para cada usuário que você adicionar, você deve especificar se o usuário está sendo concedido ou negado permissão de lançamento.

**Para definir permissões de lançamento para um computador**

1.  Na página **de propriedades Segurança** Padrão Dcomcnfg.exe, escolha o botão **Editar** Padrão na área Permissões de **Início** Padrão.

2.  Para remover usuários ou grupos, selecione o usuário ou grupo que você deseja remover e escolha o **botão Remover.** O usuário ou grupo selecionado não aparecerá mais na caixa de listagem. Quando terminar de remover usuários e grupos, escolha **OK.**

3.  Se você quiser adicionar um usuário ou grupo, escolha o **botão** Adicionar.

4.  Se você sabe o nome de usuário totalmente qualificado que deseja adicionar, digite-o na **caixa de texto Adicionar** Nomes. Se você não sabe o nome de usuário, consulte Configurando a segurança do processo em todo o processo **usando DCOMCNFG** para encontrá-lo. Quando você tiver localizado o nome de usuário, selecione o usuário ou grupo na caixa **de** listagem Nomes e escolha o **botão** Adicionar.

5.  Na caixa **de listagem Tipo** de Acesso, selecione o tipo de acesso **(permitir iniciar** ou negar a **lançamento).** Para adicionar outros usuários que também terão o tipo de acesso selecionado, repita a etapa 4. Quando terminar de adicionar usuários para o tipo de acesso selecionado, escolha o **botão OK.**

6.  Para adicionar usuários que terão um tipo diferente de acesso, repita as etapas 4 e 5. Caso contrário, **escolha OK** para aplicar as alterações.

## <a name="setting-system-wide-access-permissions"></a>Definindo System-Wide permissões de acesso

Dcomcnfg.exe permite definir permissões de acesso para controlar a lista de usuários que têm acesso concedido ou negado aos métodos desses servidores que não fornecem suas próprias permissões de acesso. Você pode adicionar usuários ou grupos à lista, especificando se a permissão de acesso está sendo concedida ou negada. Você também pode remover usuários da lista.

Ao definir permissões de acesso, você deve garantir que SYSTEM seja incluído na lista de usuários que têm acesso concedido. Se você tiver concedido permissões de acesso a Todos, SYSTEM será incluído implicitamente.

O processo de configuração de permissões de acesso para um computador é semelhante à configuração de permissões de lançamento. As etapas a seguir devem ser realizadas.

**Para definir permissões de acesso para um computador**

1.  Na página **de propriedades Segurança** Padrão Dcomcnfg.exe, escolha o botão **Editar** Padrão na área **Permissões de** Acesso Padrão.

2.  Para remover usuários ou grupos, selecione o usuário ou grupo que você deseja remover e escolha o **botão Remover.** O usuário ou grupo selecionado não aparecerá mais na caixa de listagem. Quando terminar de remover usuários e grupos, escolha **OK.**

3.  Se você quiser adicionar um usuário ou um grupo, escolha o **botão** Adicionar.

4.  Se você sabe o nome de usuário totalmente qualificado que deseja adicionar, digite-o na **caixa de texto Adicionar** Nomes. Se você não sabe o nome de usuário, consulte Configurando a segurança em todo o processo [usando DCOMCNFG](setting-processwide-security-using-dcomcnfg.md) para encontrá-lo. Quando você tiver localizado o nome de usuário, selecione o usuário ou grupo na caixa **de** listagem Nomes e escolha o **botão** Adicionar.

5.  Na caixa **de listagem Tipo** de Acesso, selecione o tipo de acesso **(permitir acesso** ou negar **acesso**). Para adicionar outros usuários que terão o tipo de acesso selecionado, repita a etapa 4. Quando terminar de adicionar usuários para o tipo de acesso selecionado, escolha o **botão OK.**

6.  Para adicionar usuários que terão um tipo diferente de acesso, repita as etapas 4 e 5. Caso contrário, **escolha OK** para aplicar as alterações.

## <a name="setting-system-wide-impersonation-level"></a>Definindo System-Wide nível de representação

O nível de representação, definido pelo cliente, determina a quantidade de autoridade dada ao servidor para agir em nome do cliente. Por exemplo, quando o cliente tiver definido seu nível de representação para delegar, o servidor poderá acessar recursos locais e remotos como o cliente e o servidor poderá passar por vários limites do computador se a funcionalidade de desajuste estiver definida. Para ajudar a determinar qual nível de representação você deve escolher, consulte [Níveis de representação](impersonation-levels.md) e [Redução.](cloaking.md)

Definir o nível de representação padrão para todo o computador informa ao COM qual nível de representação usar quando um cliente específico no computador não especifica um nível de representação programaticamente usando [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ou [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket).

**Para definir o nível de representação para um computador**

1.  Com Dcomcnfg.exe em execução, escolha a **guia Propriedades** Padrão.

2.  Na caixa **de listagem Nível de** Representação Padrão, escolha o nível de representação que você deseja.

3.  Se você estiver definindo mais propriedades para o computador, escolha o **botão** Aplicar para aplicar o novo nível de representação. Caso contrário, **escolha OK** para aplicar as alterações e sair Dcomcnfg.exe.

## <a name="setting-system-wide-reference-tracking"></a>Definindo System-Wide de referência

Ao habilitar o acompanhamento de referência, você está solicitando que o COM faça verificações de segurança adicionais e mantenha o controle das informações que impedirão que os objetos sejam liberados muito cedo. Tenha em mente que essas verificações adicionais são caras. Para obter mais informações sobre o acompanhamento de referência, consulte [Acompanhamento de referência.](reference-tracking.md) Use as etapas a seguir para habilitar ou desabilitar o acompanhamento de referência.

**Para definir o acompanhamento de referência para um computador**

1.  Com Dcomcnfg.exe em execução, escolha a **guia Propriedades** Padrão.

2.  Para habilitar (ou desabilitar) o  acompanhamento de referência, marque (ou des) a caixa de seleção Fornecer segurança adicional para acompanhamento de referência próximo à parte inferior da página.

3.  Se você estiver definindo mais propriedades para o computador, escolha o **botão** Aplicar para aplicar a nova configuração. Caso contrário, **escolha OK** para aplicar as alterações e sair Dcomcnfg.exe.

## <a name="enabling-and-disabling-dcom"></a>Habilitando e desabilitando o DCOM

Quando um computador faz parte de uma rede, o protocolo de transmissão DCOM permite que objetos COM nesse computador se comuniquem com objetos COM em outros computadores. Você pode desabilitar o DCOM para um computador específico, mas fazer isso desabilitará toda a comunicação entre objetos nesse computador e objetos em outros computadores.

Desabilitar o DCOM em um computador não tem efeito sobre objetos COM locais. O COM ainda procura permissões de lançamento que você especificou. Se nenhuma permissão de lançamento tiver sido especificada, serão usadas permissões de lançamento padrão. Mesmo se você desabilitar o DCOM, se um usuário tiver acesso físico ao computador, ele poderá iniciar um servidor no computador, a menos que você de definir permissões de lançamento para não permitir.

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

 

 




