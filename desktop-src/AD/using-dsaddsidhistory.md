---
title: Usando DsAddSidHistory
description: Este tópico descreve como usar a função DsAddSidHistory.
ms.assetid: cbf4983c-551d-4771-870e-a192ed898eb7
ms.tgt_platform: multiple
keywords:
- Usando o DsAddSidHistory Active Directory
- Active Directory Active Directory , usando, Usando DsAddSidHistory
- DsAddSidHistory Active Directory, usando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afb37e09d5c7b337717f27b0e68ad17331ee27270da9e7b79a0d6bba791d2e5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118182520"
---
# <a name="using-dsaddsidhistory"></a>Usando DsAddSidHistory

A [**função DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) obtém o SID (identificador de segurança) da conta primária de uma entidade de segurança de um domínio (o domínio de origem) e adiciona-o ao atributo **sIDHistory** de uma entidade de segurança em outro domínio (destino) em uma floresta diferente. Quando o domínio de origem está Windows modo nativo 2000, essa função também recupera os valores **sIDHistory** da entidade de segurança de origem e os adiciona ao **sIDHistory** da entidade de segurança de destino.

Adicionar SIDs ao **sIDHistory** de uma entidade de segurança é uma operação sensível à segurança que efetivamente concede à entidade de segurança de destino acesso a todos os recursos acessíveis à entidade de segurança de origem, desde que existam confianças de domínios de recursos aplicáveis para o domínio de destino.

Em um modo nativo Windows 2000, um logon de usuário cria um token de acesso que contém os SIDs de grupo e SID da conta primária do usuário, bem como o **usuário sIDHistory** e **o sIDHistory** dos grupos dos quais o usuário é membro. Ter esses SIDs antigos (**valores sIDHistory)** no token do usuário concede ao usuário acesso aos recursos protegidos por ACLs (listas de controle de acesso) que contêm os SIDs antigos.

Essa operação facilita determinados Windows de implantação 2000. Em particular, ele dá suporte a um cenário no qual as contas em uma nova floresta do Windows 2000 são criadas para usuários e grupos que já existem em um ambiente de produção Windows NT 4.0. Ao colocar o SID da conta Windows NT 4.0 na conta do Windows 2000 **sIDHistory,** o acesso aos recursos de rede é preservado para o usuário que faz logon em sua nova conta do Windows 2000.

[**O DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) também dá suporte à migração de BDCs (controladores de domínio de backup) do Windows NT 4.0 (ou DCs e servidores membros em um domínio de modo nativo Windows 2000) para um domínio Windows 2000 como servidores membros. Essa migração requer a criação, no domínio de destino Windows 2000, de grupos locais de domínio que contêm, em **seu sIDHistory**, os SIDs primários dos grupos locais definidos no BDC (ou grupos locais de domínio referenciados em ACLs nos servidores Windows 2000) no domínio de origem. Ao criar um grupo local de destino que contém **o sIDHistory** e todos os membros do grupo local de origem, o acesso aos recursos de servidor migrados, protegidos por ACLs que referenciam o grupo local de origem, é mantido para todos os membros.

> [!Note]  
> O uso [**de DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) requer uma compreensão de suas implicações administrativas e de segurança mais amplas nesses e em outros cenários. Para obter mais informações, consulte o white paper "Planning Migration from Windows NT to Microsoft Windows 2000", fornecido como Dommig.doc nas Ferramentas de Suporte do Windows 2000. Esta documentação também pode ser encontrada no CD do produto em ferramentas \\ de \\ suporte.

 

## <a name="authorization-requirements"></a>Requisitos de autorização

[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) requer privilégios de administrador nos domínios de origem e destino. Especificamente, o chamador dessa API deve ser um membro do grupo Administradores de Domínio no domínio de destino. Uma verificação em código para essa associação é executada. Além disso, o chamador ou a conta fornecida no parâmetro *SrcDomainCreds,* se não **FOR NULL,** deve ser um membro do grupo Administradores ou Administradores de Domínio no domínio de origem.

## <a name="domain-and-trust-requirements"></a>Requisitos de domínio e confiança

[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) requer que o domínio de destino Windows no modo nativo 2000 ou posterior, porque somente esse tipo de domínio dá suporte ao atributo **sIDHistory.** O domínio de origem pode ser Windows NT 4.0 ou Windows 2000, modo misto ou nativo. Os domínios de origem e destino não devem estar na mesma floresta. Windows NT domínios 4.0 estão, por definição, não em uma floresta. Essa restrição entre florestas garante que SIDs duplicados, sejam eles exibidos como sids primários ou **valores sIDHistory,** não sejam criados na mesma floresta.

[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) requer uma confiança externa do domínio de origem para o domínio de destino nos casos listados na tabela a seguir.



| Caixa                                                                             | Descrição                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| O domínio de origem Windows 2000.<br/>                                    | O atributo **sIDHistory** de origem, disponível somente em domínios de origem Windows 2000, pode ser lido somente usando LDAP, o que requer essa confiança para proteção de integridade.<br/>                                                                                             |
| O domínio de origem Windows NT 4.0 e *SrcDomainCreds* é **NULL.**<br/> | A representação, necessária para dar suporte a operações de domínio de origem usando as credenciais do chamador, depende dessa confiança. A representação também requer que o controlador de domínio de destino tenha "Confiável para Delegação" habilitado por padrão em controladores de domínio.<br/> |



 

No entanto, não há nenhuma relação de confiança necessária entre os domínios de origem e de destino se o domínio de origem for Windows NT 4.0 e *SrcDomainCreds* não for **NULL.**

## <a name="source-domain-controller-requirements"></a>Requisitos do controlador de domínio de origem

[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) requer que o controlador de domínio, selecionado como o destino para operações no domínio de origem, seja o PDC em domínios do Windows NT 4.0 ou o pdc Emulator em domínios Windows 2000. A auditoria de domínio de origem é gerada por meio de operações de gravação, portanto, o PDC é necessário em domínios de origem do Windows NT 4.0 e a restrição somente PDC garante que as auditorias **de DsAddSidHistory** sejam geradas em um único computador. Isso reduz a necessidade de revisar os logs de auditoria de todos os DCs para monitorar o uso dessa operação.

> [!Note]  
> No Windows NT domínios de origem 4.0, o PDC (destino de operações no domínio de origem) deve estar executando o Sp4 (Service Pack 4) e posterior para garantir o suporte adequado à auditoria.

 

O valor do Registro a seguir deve ser criado como um valor REG DWORD e definido como 1 no controlador de domínio de origem para os DCs de origem \_ Windows NT 4.0 e Windows 2000.

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Control
            Lsa
               TcpipClientSupport
```

Definir esse valor habilita chamadas RPC pelo transporte TCP. Isso é necessário porque, por padrão, as interfaces SAMRPC só podem ser remotas em pipes nomeados. O uso de pipes nomeados resulta em um sistema de gerenciamento de credenciais adequado para usuários conectados interativamente que fazem chamadas em rede, mas não é flexível para um processo do sistema que faz chamadas de rede com credenciais fornecidas pelo usuário. RPC sobre TCP é mais adequado para essa finalidade. Definir esse valor não diminui a segurança do sistema. Se esse valor for criado ou alterado, o controlador de domínio de origem deverá ser reiniciado para que essa configuração entre em vigor.

Um novo grupo local, " $$$", deve ser criado no domínio de origem <SrcDomainName> para fins de auditoria.

## <a name="auditing"></a>Auditoria

[**As operações DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) são auditadas para garantir que os administradores de domínio de origem e de destino sejam capazes de detectar quando essa função foi executado. A auditoria é obrigatória nos domínios de origem e de destino. **DsAddSidHistory** verifica se o Modo de Auditoria está em cada domínio e se a auditoria do Gerenciamento de Conta de eventos de Êxito/Falha está em. No domínio de destino, um evento de auditoria exclusivo "Adicionar Histórico de Sid" é gerado para cada operação **DsAddSidHistory bem-sucedida** ou com falha.

Os eventos de auditoria exclusivos de auditoria "Adicionar Histórico de Sid" não estão disponíveis Windows NT sistemas 4.0. Para gerar eventos de auditoria que refletem inequivocamente o uso de [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) no domínio de origem, ele executa operações em um grupo especial cujo nome é o identificador exclusivo no log de auditoria. Um grupo local, " $$$", cujo nome é composto pelo nome NetBIOS do domínio de origem anexado com três cifrões <SrcDomainName> ($) (código ASCII = 0x24 e Unicode = U+0024), deve ser criado no controlador de domínio de origem antes de chamar **DsAddSidHistory**. Cada usuário de origem e grupo global que é um destino dessa operação é adicionado e removido da associação desse grupo. Isso gera eventos de auditoria Adicionar Membro e Excluir Membro no domínio de origem, que podem ser monitorados pesquisando eventos que referenciam o nome do grupo.

> [!Note]  
> [**As operações DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) em grupos locais em um Windows NT 4.0 ou domínio de origem de modo misto do Windows 2000 não podem ser auditadas porque os grupos locais não podem ser membros de outro grupo local e, portanto, não podem ser adicionados ao grupo local especial " <SrcDomainName> $$$". Essa falta de auditoria não apresenta um problema de segurança para o domínio de origem, pois o acesso ao recurso de domínio de origem não é afetado por essa operação. Adicionar o SID de um grupo local de origem a um grupo local de destino não concede acesso aos recursos de origem, protegidos por esse grupo local, a nenhum usuário adicional. A adição de membros ao grupo local de destino não concede a eles acesso aos recursos de origem. Os membros adicionados recebem acesso somente aos servidores no domínio de destino migrados do domínio de origem, que podem ter recursos protegidos pelo SID do grupo local de origem.

 

## <a name="data-transmission-security"></a>Segurança de transmissão de dados

[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) impõe as seguintes medidas de segurança:

-   Chamadas de uma Windows 2000, as credenciais do chamador são usadas para autenticar e proteger a privacidade da chamada RPC para o controlador de domínio de destino. Se *SrcDomainCreds* não for **NULL,** a estação de trabalho e o DC de destino deverão dar suporte à criptografia de 128 bits para proteger a privacidade das credenciais. Se a criptografia de 128 bits não estiver disponível e *o SrcDomainCreds* for fornecido, a chamada deverá ser feita no DC de destino.
-   O controlador de domínio de destino se comunica com o controlador de domínio de origem usando *SrcDomainCreds* ou as credenciais do chamador para autenticar mutuamente e proteger a integridade da leitura do SID da conta de origem (usando uma busca SAM) e **sIDHistory** (usando uma leitura LDAP).

## <a name="threat-models"></a>Modelos de ameaça

A tabela a seguir lista as possíveis ameaças associadas à chamada [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) e aborda as medidas de segurança pertinentes à ameaça específica.



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
<td>Man in the Middle Attack<br/> Um usuário não autorizado intercepta o <em>SID</em> de consulta da chamada de retorno do objeto de origem, substituindo o SID do objeto de origem por um SID arbitrário para inserção em um objeto de destino SIDhistory.<br/></td>
<td>O <em>SID de lookup do objeto de</em> origem é um RPC autenticado, usando as credenciais de administrador do chamador, com proteção de mensagem de integridade do pacote. Isso garante que a chamada de retorno não possa ser modificada sem detecção. O controlador de domínio de destino cria um evento de auditoria adicionar histórico de SID exclusivo que reflete o SID adicionado à conta &quot; &quot; de destino <strong>sIDHistory</strong>.<br/></td>
</tr>
<tr class="even">
<td>Domínio de origem do Troia<br/> Um usuário não autorizado cria um domínio de origem de Troia Em uma rede privada que tem o mesmo SID de domínio e alguns dos mesmos SIDs de conta que o &quot; &quot; domínio de origem legítimo. Em seguida, o usuário não autorizado tenta executar <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>DsAddSidHistory</strong></a> em um domínio de destino para obter o SID de uma conta de origem. Isso é feito sem a necessidade das credenciais do Administrador de Domínio de origem real e sem deixar uma trilha de auditoria no domínio de origem real. O método do usuário não autorizado para criar o domínio de origem do Troia De troia pode ser um dos seguintes:
<ul>
<li>Obtenha uma cópia (backup do BDC) do domínio de origem SAM.</li>
<li>Crie um novo domínio, alterando o SID de domínio no disco para corresponder ao SID de domínio de origem legítimo e, em seguida, crie usuários suficientes para criar uma conta com o SID desejado.</li>
<li>Crie uma réplica BDC. Isso requer credenciais de administrador do domínio de origem. Em seguida, o usuário não autorizado leva a réplica para uma rede privada para implementar o ataque.</li>
</ul>
<br/></td>
<td>Embora haja muitas maneiras para um usuário não autorizado recuperar ou criar um SID de objeto de origem desejado, o usuário não autorizado não pode usá-lo para atualizar o <strong>sIDHistory</strong> de uma conta sem ser membro do grupo administradores de domínio de destino. Como a verificação, no controlador de domínio de destino, para associação de Administrador de Domínio é em código, no DC de destino, não há nenhum método para fazer uma modificação de disco para alterar os dados de controle de acesso que protegem essa função. Uma tentativa de clonar uma conta de origem do Troia É auditada no domínio de destino. Esse ataque é atenuado com a reserva de associação no grupo Administradores de Domínio apenas para indivíduos altamente confiáveis.<br/></td>
</tr>
<tr class="odd">
<td>Modificação no disco do histórico de SID<br/> Um usuário sofisticado não autorizado, com credenciais de Administrador de Domínio e com acesso físico a um controlador de domínio no domínio de destino, pode modificar um valor <strong>sIDHistory</strong> da conta no disco.<br/></td>
<td>Essa tentativa não está habilitada com o <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>uso de DsAddSidHistory.</strong></a> Esse ataque é mitigado ao impedir o acesso físico a controladores de domínio a todos, exceto administradores altamente confiáveis.<br/></td>
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
<td>Domínio de destino não autorizado<br/> um usuário não autorizado cria um domínio Windows 2000 com uma conta cujo <strong>sIDHistory</strong> contém um SID que foi roubado de um domínio de origem. O usuário não autorizado usa essa conta para acesso não autorizado aos recursos.<br/></td>
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
    grupo de domínio local (somente Windows modo nativo do 2000)  
    grupo Universal (somente Windows modo nativo de 2000)  
    </dl>

Os tipos de objeto de *SrcPrincipal* e *DstPrincipal* devem corresponder.

-   Se *SrcPrincipal* for um usuário, *DstPrincipal* deverá ser um usuário.
-   Se *SrcPrincipal* for um grupo local ou de domínio, *DstPrincipal* deverá ser um grupo de domínio local.
-   Se *SrcPrincipal* for um grupo global ou universal, *DstPrincipal* deverá ser um grupo global ou universal.

*SrcPrincipal* e *DstPrincipal* não podem ser um dos seguintes tipos: ([**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) falha com um erro nesses casos)

-   Computador (estação de trabalho ou controlador de domínio)
-   Confiança entre domínios
-   Conta duplicada temporária (um recurso virtualmente não utilizado, um herdado do LANman)
-   Contas com SIDs bem conhecidos. SIDs bem conhecidos são idênticos em todos os domínios; portanto, adicioná-los a um **sIDHistory** violaria o requisito de exclusividade de SID de uma floresta Windows 2000. As contas com SIDs bem conhecidos incluem os seguintes grupos locais:

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

o procedimento a seguir mostra como habilitar a auditoria de eventos de gerenciamento de usuário/grupo em um domínio Windows 2000 ou Windows Server 2003 de origem ou de destino.

**para habilitar a auditoria de eventos de gerenciamento de usuário/grupo em um domínio de origem ou de destino Windows 2000 ou Windows Server 2003**

1.  No snap-in Active Directory usuários e computadores do MMC, selecione o contêiner controladores de domínio de domínio de destino.
2.  Clique com o botão direito do mouse em **controladores de domínio** e escolha **Propriedades**.
3.  Clique na guia **política de grupo** .
4.  Selecione a **política controladores de domínio padrão** e clique em **Editar**.
5.  em **configuração do computador \\ Windows Configurações \\ segurança Configurações \\ política de \\ auditoria de políticas locais**, clique duas vezes em gerenciamento de conta de **auditoria**.
6.  Na janela **Gerenciamento de conta de auditoria** , selecione auditoria de **êxito** e de **falha** . As atualizações de política entram em vigor após uma reinicialização ou após uma atualização.
7.  Verifique se a auditoria está habilitada exibindo a diretiva de auditoria efetiva no snap-in do Política de Grupo MMC.

o procedimento a seguir mostra como habilitar a auditoria de eventos de gerenciamento de usuário/grupo em um domínio Windows NT 4,0.

**para habilitar a auditoria de eventos de gerenciamento de usuário/grupo em um domínio Windows NT 4,0**

1.  No **Gerenciador de usuários para domínios**, clique no menu **políticas** e selecione **auditoria**.
2.  Selecione **auditar esses eventos**.
3.  Para o **Gerenciamento de usuários e grupos**, verifique **êxito e falha**.

o procedimento a seguir mostra como habilitar a auditoria de eventos de gerenciamento de usuário/grupo em um domínio de origem Windows NT 4,0, Windows 2000 ou Windows Server 2003.

**para habilitar a auditoria de eventos de gerenciamento de usuário/grupo em um domínio de origem Windows NT 4,0, Windows 2000 ou Windows Server 2003**

1.  No **Gerenciador de usuários para domínios**, clique no menu **usuário** e selecione **novo grupo local**.
2.  Insira um nome de grupo composto pelo nome NetBIOS do domínio de origem acrescentado com três sinais de dólar ($), por exemplo, FABRIKAM $ $ $. O campo descrição deve indicar que esse grupo é usado para auditar o uso de operações de clonagem ou [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) . Verifique se não há membros no grupo. Clique em **OK**.

A operação [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) falhará se a auditoria de origem e de destino não estiver habilitada conforme descrito aqui.

## <a name="set-up-trust-if-required"></a>Configurar confiança se necessário

Se uma das seguintes opções for verdadeira, uma relação de confiança deverá ser estabelecida do domínio de origem para o domínio de destino (isso deve ocorrer em uma floresta diferente):

-   o domínio de origem é Windows Server 2003.
-   o domínio de origem é Windows NT 4,0 e *SrcDomainCreds* é **nulo**.

 

 





