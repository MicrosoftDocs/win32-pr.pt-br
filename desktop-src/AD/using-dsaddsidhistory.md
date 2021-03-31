---
title: Usando DsAddSidHistory
description: Este tópico descreve como usar a função DsAddSidHistory.
ms.assetid: cbf4983c-551d-4771-870e-a192ed898eb7
ms.tgt_platform: multiple
keywords:
- Usando o DsAddSidHistory Active Directory
- Active Directory Active Directory, usando, usando DsAddSidHistory
- DsAddSidHistory Active Directory, usando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d45792dbd8c7a2bfa2dd047111a3ed165a2011e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634905"
---
# <a name="using-dsaddsidhistory"></a>Usando DsAddSidHistory

A função [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) Obtém o Sid (identificador de segurança) da conta primária de uma entidade de segurança de um domínio (o domínio de origem) e o adiciona ao atributo **SIDHistory** de uma entidade de segurança em outro domínio (destino) em uma floresta diferente. Quando o domínio de origem está no modo nativo do Windows 2000, essa função também recupera os valores de **SIDHistory** da entidade de segurança e os adiciona ao **SIDHistory** da entidade de segurança de destino.

A adição de SIDs ao **SIDHistory** de uma entidade de segurança é uma operação sensível à segurança que efetivamente concede ao acesso principal de destino a todos os recursos acessíveis à entidade de origem, desde que existam relações de confiança existentes nos domínios de recursos aplicáveis ao domínio de destino.

Em um domínio do Windows 2000 no modo nativo, um logon de usuário cria um token de acesso que contém o SID da conta primária do usuário e os SIDs de grupo, bem como o **SIDHistory** do usuário e o **SIDHistory** dos grupos dos quais o usuário é membro. Ter esses SIDs anteriores (valores de **SIDHistory** ) no token do usuário concede ao usuário acesso aos recursos protegidos pelas ACLs (listas de controle de acesso) que contêm os SIDs anteriores.

Esta operação facilita determinados cenários de implantação do Windows 2000. Em particular, ele dá suporte a um cenário no qual as contas em uma nova floresta do Windows 2000 são criadas para usuários e grupos que já existem em um ambiente de produção do Windows NT 4,0. Ao colocar o SID da conta do Windows NT 4,0 no **SIDHistory** da conta do Windows 2000, o acesso aos recursos de rede é preservado para o logon do usuário em sua nova conta do Windows 2000.

O [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) também dá suporte à migração de servidores de recursos dos BDCs (controladores de domínio de backup) do windows NT 4,0 (ou DCS e servidores membro em um domínio do Windows 2000 no modo nativo) para um domínio do Windows 2000 como servidores membro. Essa migração requer a criação, no domínio de destino do Windows 2000, de grupos locais de domínio que contêm, em seu **SIDHistory**, os SIDs primários dos grupos locais definidos no BDC (ou grupos locais de domínio referenciados em ACLs nos servidores Windows 2000) no domínio de origem. Ao criar um grupo local de destino contendo o **SIDHistory** e todos os membros do grupo local de origem, o acesso aos recursos migrados do servidor, protegidos por ACLs que fazem referência ao grupo local de origem, é mantido para todos os membros.

> [!Note]  
> O uso de [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) requer uma compreensão de suas implicações administrativas e de segurança mais amplas nesses e em outros cenários. Para obter mais informações, consulte a white paper "planejando a migração do Windows NT para o Microsoft Windows 2000", entregue como Dommig.doc nas ferramentas de suporte do Windows 2000. Esta documentação também pode ser encontrada no CD do produto em \\ ferramentas de suporte \\ .

 

## <a name="authorization-requirements"></a>Requisitos de autorização

O [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) requer privilégios de administrador nos domínios de origem e de destino. Especificamente, o chamador dessa API deve ser um membro do grupo de administradores de domínio no domínio de destino. Uma verificação embutida em código para essa associação é executada. Além disso, o chamador ou a conta fornecida no parâmetro *SrcDomainCreds* , se não for **NULL**, deve ser um membro do grupo Administradores ou administradores de domínio no domínio de origem.

## <a name="domain-and-trust-requirements"></a>Requisitos de domínio e confiança

[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) exige que o domínio de destino esteja no modo nativo do Windows 2000 ou posterior, pois somente esse tipo de domínio dá suporte ao atributo **SIDHistory** . O domínio de origem pode ser o Windows NT 4,0 ou Windows 2000, modo misto ou nativo. Os domínios de origem e de destino não devem estar na mesma floresta. Os domínios do Windows NT 4,0 são por definição que não estão em uma floresta. Essa restrição entre florestas garante que SIDs duplicados, sejam exibidos como SIDs primários ou valores de **SIDHistory** , não sejam criados na mesma floresta.

O [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) requer uma relação de confiança externa do domínio de origem para o domínio de destino nos casos listados na tabela a seguir.



| Caixa                                                                             | Descrição                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| O domínio de origem é o Windows 2000.<br/>                                    | O atributo **SIDHistory** de origem, disponível somente em domínios de origem do Windows 2000, pode ser somente leitura usando LDAP, o que exige essa relação de confiança para a proteção de integridade.<br/>                                                                                             |
| O domínio de origem é o Windows NT 4,0 e o *SrcDomainCreds* é **nulo**.<br/> | A representação, necessária para dar suporte às operações de domínio de origem usando as credenciais do chamador, depende dessa relação de confiança. A representação também exige que o controlador de domínio de destino tenha "confiável para delegação" habilitada por padrão em controladores de domínio.<br/> |



 

No entanto, não há nenhuma relação de confiança necessária entre os domínios de origem e de destino se o domínio de origem for Windows NT 4,0 e *SrcDomainCreds* não for **nulo**.

## <a name="source-domain-controller-requirements"></a>Requisitos do controlador de domínio de origem

[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) requer que o controlador de domínio, selecionado como o destino para operações no domínio de origem, seja o PDC em domínios do windows NT 4,0 ou o emulador de PDC em domínios do Windows 2000. A auditoria de domínio de origem é gerada por meio de operações de gravação, portanto, o PDC é necessário em domínios de origem do Windows NT 4,0 e a restrição somente PDC garante que as auditorias **DsAddSidHistory** sejam geradas em um único computador. Isso reduz a necessidade de examinar os logs de auditoria de todos os DCs para monitorar o uso dessa operação.

> [!Note]  
> Em domínios de origem do Windows NT 4,0, o PDC (destino de operações no domínio de origem) deve estar executando o Service Pack 4 (SP4) e posterior para garantir o suporte adequado à auditoria.

 

O valor do registro a seguir deve ser criado como um \_ valor reg DWORD e definido como 1 no controlador de domínio de origem para os DCS de origem do Windows NT 4,0 e do windows 2000.

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Control
            Lsa
               TcpipClientSupport
```

Definir esse valor habilita chamadas RPC no transporte TCP. Isso é necessário porque, por padrão, as interfaces SAMRPC são remotas somente em pipes nomeados. O uso de pipes nomeados resulta em um sistema de gerenciamento de credenciais adequado para usuários conectados interativamente, fazendo chamadas em rede, mas não é flexível para um processo do sistema que faz chamadas de redes com credenciais fornecidas pelo usuário. RPC sobre TCP é mais adequado para essa finalidade. A definição desse valor não diminui a segurança do sistema. Se esse valor for criado ou alterado, o controlador de domínio de origem deverá ser reiniciado para que essa configuração entre em vigor.

Um novo grupo local, " <SrcDomainName> $ $ $", deve ser criado no domínio de origem para fins de auditoria.

## <a name="auditing"></a>Auditoria

As operações [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) são auditadas para garantir que os administradores de domínio de origem e de destino sejam capazes de detectar quando essa função foi executada. A auditoria é obrigatória nos domínios de origem e de destino. **DsAddSidHistory** verifica se o modo de auditoria está ativado em cada domínio e se a auditoria de gerenciamento de conta de eventos de êxito/falha está ativada. No domínio de destino, um evento de auditoria exclusivo "Adicionar histórico SID" é gerado para cada operação de **DsAddSidHistory** bem-sucedida ou com falha.

Os eventos de auditoria exclusivos do "Adicionar histórico SID" não estão disponíveis em sistemas Windows NT 4,0. Para gerar eventos de auditoria que refletem inequivocamente o uso de [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) em relação ao domínio de origem, ele executa operações em um grupo especial cujo nome é o identificador exclusivo no log de auditoria. Um grupo local, " <SrcDomainName> $ $ $", cujo nome é composto pelo nome NetBIOS do domínio de origem acrescentado com três sinais de dólar ($) (código ASCII = 0x24 e Unicode = U + 0024), deve ser criado no controlador de domínio de origem antes de chamar **DsAddSidHistory**. Cada usuário de origem e grupo global que é um destino dessa operação é adicionado e removido da associação deste grupo. Isso gera eventos de auditoria Adicionar membro e excluir membro no domínio de origem, que pode ser monitorado pesquisando eventos que fazem referência ao nome do grupo.

> [!Note]  
> As operações [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) em grupos locais em um domínio de origem de modo misto do windows NT 4,0 ou do Windows 2000 não podem ser auditadas porque os grupos locais não podem se tornar membros de outro grupo local e, portanto, não podem ser adicionados ao <SrcDomainName> grupo local "$ $ $" especial. Essa falta de auditoria não apresenta um problema de segurança para o domínio de origem, pois o acesso ao recurso do domínio de origem não é afetado por essa operação. A adição do SID de um grupo local de origem a um grupo local de destino não concede acesso aos recursos de origem, protegidos por esse grupo local, a qualquer usuário adicional. Adicionar membros ao grupo local de destino não concede a eles acesso aos recursos de origem. Os membros adicionados recebem acesso somente aos servidores no domínio de destino migrados do domínio de origem, que podem ter recursos protegidos pelo SID do grupo local de origem.

 

## <a name="data-transmission-security"></a>Segurança de transmissão de dados

O [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) impõe as seguintes medidas de segurança:

-   Chamado de uma estação de trabalho do Windows 2000, as credenciais do chamador são usadas para autenticar e proteger a chamada RPC para o controlador de domínio de destino. Se *SrcDomainCreds* não for **NULL**, tanto a estação de trabalho quanto o DC de destino deverão oferecer suporte à criptografia de 128 bits para privacidade-proteger as credenciais. Se a criptografia de 128 bits não estiver disponível e *SrcDomainCreds* forem fornecidas, a chamada deverá ser feita no DC de destino.
-   O controlador de domínio de destino se comunica com o controlador de domínio de origem usando *SrcDomainCreds* ou as credenciais do chamador para autenticar mutuamente e proteger a leitura do Sid da conta de origem (usando uma pesquisa Sam) e **SIDHistory** (usando uma leitura LDAP).

## <a name="threat-models"></a>Modelos de ameaça

A tabela a seguir lista as possíveis ameaças associadas à chamada [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) e resolve as medidas de segurança pertinentes à ameaça específica.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Ameaça potencial</th>
<th>Medida de segurança</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Homem no ataque do meio<br/> Um usuário não autorizado intercepta o <em>Sid de pesquisa da chamada de retorno do objeto de origem</em> , substituindo o SID do objeto de origem por um SID arbitrário para inserção em um objeto de destino SIDhistory.<br/></td>
<td>O <em>Sid de pesquisa do objeto de origem</em> é um RPC autenticado, usando as credenciais de administrador do chamador, com proteção de mensagem de integridade de pacote. Isso garante que a chamada de retorno não pode ser modificada sem detecção. O controlador de domínio de destino cria um evento exclusivo de &quot; auditoria de histórico de SID &quot; que reflete o Sid adicionado ao <strong>SIDHistory</strong>da conta de destino.<br/></td>
</tr>
<tr class="even">
<td>Domínio de origem do cavalo de Troia<br/> Um usuário não autorizado cria um &quot; domínio de origem do cavalo &quot; de Troia em uma rede privada que tem o mesmo SID de domínio e alguns dos mesmos SIDs de conta que o domínio de origem legítimo. Em seguida, o usuário não autorizado tenta executar <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>DsAddSidHistory</strong></a> em um domínio de destino para obter o Sid de uma conta de origem. Isso é feito sem a necessidade de credenciais de administrador de domínio de origem real e sem deixar uma trilha de auditoria no domínio de origem real. O método do usuário não autorizado para criar o domínio de origem do cavalo de Troia pode ser um dos seguintes:
<ul>
<li>Obtenha uma cópia (backup do BDC) do SAM do domínio de origem.</li>
<li>Crie um novo domínio, alterando o SID do domínio no disco para corresponder ao SID do domínio de origem legítimo e, em seguida, crie usuários suficientes para criar uma instância de uma conta com o SID desejado.</li>
<li>Crie uma réplica do BDC. Isso requer credenciais de administrador de domínio de origem. Em seguida, o usuário não autorizado leva a réplica para uma rede privada para implementar o ataque.</li>
</ul>
<br/></td>
<td>Embora haja várias maneiras de um usuário não autorizado recuperar ou criar um SID de objeto de origem desejado, o usuário não autorizado não pode usá-lo para atualizar o <strong>SIDHistory</strong> de uma conta sem ser membro do grupo de administradores de domínio de destino. Como a verificação, no controlador de domínio de destino, para a associação de administrador de domínio é embutida em código, no DC de destino, não há nenhum método para fazer uma modificação no disco para alterar os dados de controle de acesso que protegem essa função. Uma tentativa de clonar uma conta de origem do cavalo de Troia é auditada no domínio de destino. Esse ataque é mitigado ao reservar a associação no grupo de administradores de domínio apenas para indivíduos altamente confiáveis.<br/></td>
</tr>
<tr class="odd">
<td>Modificação no disco do histórico de SID<br/> Um usuário não autorizado sofisticado, com credenciais de administrador de domínio e com acesso físico a um DC no domínio de destino, pode modificar um valor de <strong>SIDHistory</strong> de conta no disco.<br/></td>
<td>Essa tentativa não é habilitada pelo uso de <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>DsAddSidHistory</strong></a>. Esse ataque é mitigado ao impedir o acesso físico a controladores de domínio a todos, exceto administradores altamente confiáveis.<br/></td>
</tr>
<tr class="even">
<td>Código não autorizado usado para remover proteções<br/> Um usuário não autorizado ou um administrador não autorizado com acesso físico ao código do serviço de diretório poderia criar um código não autorizado que:
<ol>
<li>Remove a verificação de associação no grupo Administradores de domínio no código.</li>
<li>Altera as chamadas no controlador de domínio de origem que aponta o SID para um LookupSidFromName que não é auditado.</li>
<li>Remove as chamadas de log de auditoria.</li>
</ol>
<br/></td>
<td>Alguém com acesso físico ao código DS e com conhecimento suficiente para criar código não autorizado tem a capacidade de modificar arbitrariamente o atributo <strong>SIDHistory</strong> de uma conta. A API <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>DsAddSidHistory</strong></a> não aumenta esse risco de segurança.<br/></td>
</tr>
<tr class="odd">
<td>Recursos vulneráveis a SIDs roubados<br/> Se um usuário não autorizado tiver tido êxito no uso de um dos métodos descritos aqui para modificar um <strong>SIDHistory</strong>de conta e se os domínios de recursos de interesse confiarem no domínio de conta de usuário não autorizado, o usuário não autorizado poderá obter acesso não autorizado aos recursos do Sid roubado, potencialmente sem deixar uma trilha de auditoria no domínio da conta do qual o Sid foi roubado.<br/></td>
<td>Os administradores de domínio de recursos protegem seus recursos Configurando apenas as relações de confiança que fazem sentido de uma perspectiva de segurança. O uso de <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>DsAddSidHistory</strong></a> é restrito, no domínio de destino confiável, aos membros do grupo de administradores de domínio que já têm permissões amplas dentro do escopo de suas responsabilidades.<br/></td>
</tr>
<tr class="even">
<td>Domínio de destino não autorizado<br/> Um usuário não autorizado cria um domínio do Windows 2000 com uma conta cujo <strong>SIDHistory</strong> contém um SID que foi roubado de um domínio de origem. O usuário não autorizado usa essa conta para acesso não autorizado aos recursos.<br/></td>
<td>O usuário não autorizado requer credenciais de administrador para o domínio de origem a fim de usar o <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>DsAddSidHistory</strong></a>e deixa uma trilha de auditoria no controlador de domínio de origem. O domínio de destino invasor obtém acesso não autorizado somente em outros domínios que confiam no domínio não autorizado, o que exige privilégios de administrador nesses domínios de recurso.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="operational-constraints"></a>Restrições operacionais

Esta seção descreve as restrições operacionais do uso da função [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) .

O SID de *SrcPrincipal* já não deve existir na floresta de destino, seja como um SID de conta primária ou no **SIDHistory** de uma conta. A exceção é que [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) não gera um erro ao tentar adicionar um SID a um **SIDHistory** que contém um SID idêntico. Esse comportamento permite que o **DsAddSidHistory** seja executado várias vezes com entrada idêntica, resultando em êxito e em um estado final consistente, para a facilidade de uso do desenvolvedor de ferramentas.

> [!Note]  
> A latência de replicação de catálogo global pode fornecer uma janela durante a qual SIDs duplicados podem ser criados. No entanto, os SIDs duplicados podem ser facilmente excluídos por um administrador.

 

*SrcPrincipal* e *DstPrincipal* devem ser um dos seguintes tipos:

-   Usuário
-   Grupo habilitado para segurança, incluindo:

    <dl> Grupo local  
    Grupo global  
    Grupo de domínio local (somente no modo nativo do Windows 2000)  
    Grupo universal (somente no modo nativo do Windows 2000)  
    </dl>

Os tipos de objeto de *SrcPrincipal* e *DstPrincipal* devem corresponder.

-   Se *SrcPrincipal* for um usuário, *DstPrincipal* deverá ser um usuário.
-   Se *SrcPrincipal* for um grupo local ou de domínio, *DstPrincipal* deverá ser um grupo de domínio local.
-   Se *SrcPrincipal* for um grupo global ou universal, *DstPrincipal* deverá ser um grupo global ou universal.

*SrcPrincipal* e *DstPrincipal* não podem ser um dos seguintes tipos: ([**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) falha com um erro nesses casos)

-   Computador (estação de trabalho ou controlador de domínio)
-   Confiança entre domínios
-   Conta duplicada temporária (um recurso virtualmente não utilizado, um herdado do LANman)
-   Contas com SIDs bem conhecidos. SIDs bem conhecidos são idênticos em todos os domínios; Portanto, adicioná-los a um **SIDHistory** violaria o requisito de exclusividade de Sid de uma floresta do Windows 2000. As contas com SIDs bem conhecidos incluem os seguintes grupos locais:

    <dl> Operadores de conta  
    Administradores  
    Operadores de backup  
    Convidados  
    Operadores de impressão  
    Replicador  
    Operadores de servidor  
    Usuários  
    </dl>

Se *SrcPrincipal* tiver um RID (identificador relativo) bem conhecido e um prefixo específico de domínio, ou seja, administradores de domínio, usuários de domínio e computadores de domínio, o *DstPrincipal* deverá ter o mesmo RID conhecido para que o [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) seja bem sucedido. As contas com RIDs bem conhecidos incluem os seguintes usuários e grupos globais:

-   Administrador
-   Convidado
-   Administradores de domínio
-   Convidados do domínio
-   Usuários de domínio

## <a name="setting-the-registry-value"></a>Definindo o valor do registro

O procedimento a seguir mostra como definir o valor de Registro TcpipClientSupport.

**Para definir o valor de Registro TcpipClientSupport**

1.  Crie o seguinte valor de registro como um \_ valor de reg DWORD no controlador de domínio de origem e defina seu valor como 1.

    **HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Control \\ LSA \\ TcpipClientSupport**

2.  Em seguida, reinicie o controlador de domínio de origem. Esse valor de registro faz com que o SAM escute no TCP/IP. [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) falhará se esse valor não estiver definido no controlador de domínio de origem.

## <a name="enabling-auditing-of-usergroup-management-events"></a>Habilitando a auditoria de eventos de gerenciamento de usuário/grupo

O procedimento a seguir mostra como habilitar a auditoria de eventos de gerenciamento de usuário/grupo em um domínio de origem ou de destino do Windows 2000 ou do Windows Server 2003.

**Para habilitar a auditoria de eventos de gerenciamento de usuário/grupo em um domínio de origem ou de destino do Windows 2000 ou do Windows Server 2003**

1.  No snap-in Active Directory usuários e computadores do MMC, selecione o contêiner controladores de domínio de domínio de destino.
2.  Clique com o botão direito do mouse em **controladores de domínio** e escolha **Propriedades**.
3.  Clique na guia **política de grupo** .
4.  Selecione a **política controladores de domínio padrão** e clique em **Editar**.
5.  Em **configuração do computador \\ configurações do Windows \\ configurações de segurança \\ políticas locais \\ política de auditoria**, clique duas vezes em gerenciamento de conta de **auditoria**.
6.  Na janela **Gerenciamento de conta de auditoria** , selecione auditoria de **êxito** e de **falha** . As atualizações de política entram em vigor após uma reinicialização ou após uma atualização.
7.  Verifique se a auditoria está habilitada exibindo a diretiva de auditoria efetiva no snap-in do Política de Grupo MMC.

O procedimento a seguir mostra como habilitar a auditoria de eventos de gerenciamento de usuário/grupo em um domínio do Windows NT 4,0.

**Para habilitar a auditoria de eventos de gerenciamento de usuário/grupo em um domínio do Windows NT 4,0**

1.  No **Gerenciador de usuários para domínios**, clique no menu **políticas** e selecione **auditoria**.
2.  Selecione **auditar esses eventos**.
3.  Para o **Gerenciamento de usuários e grupos**, verifique **êxito e falha**.

O procedimento a seguir mostra como habilitar a auditoria de eventos de gerenciamento de usuário/grupo em um domínio de origem do Windows NT 4,0, Windows 2000 ou Windows Server 2003.

**Para habilitar a auditoria de eventos de gerenciamento de usuário/grupo em um domínio de origem do Windows NT 4,0, Windows 2000 ou Windows Server 2003**

1.  No **Gerenciador de usuários para domínios**, clique no menu **usuário** e selecione **novo grupo local**.
2.  Insira um nome de grupo composto pelo nome NetBIOS do domínio de origem acrescentado com três sinais de dólar ($), por exemplo, FABRIKAM $ $ $. O campo descrição deve indicar que esse grupo é usado para auditar o uso de operações de clonagem ou [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) . Verifique se não há membros no grupo. Clique em **OK**.

A operação [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) falhará se a auditoria de origem e de destino não estiver habilitada conforme descrito aqui.

## <a name="set-up-trust-if-required"></a>Configurar confiança se necessário

Se uma das seguintes opções for verdadeira, uma relação de confiança deverá ser estabelecida do domínio de origem para o domínio de destino (isso deve ocorrer em uma floresta diferente):

-   O domínio de origem é o Windows Server 2003.
-   O domínio de origem é o Windows NT 4,0 e o *SrcDomainCreds* é **nulo**.

 

 





