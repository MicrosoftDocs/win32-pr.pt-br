---
title: Usando DsAddSidHistory
description: Este tópico descreve como usar a função DsAddSidHistory.
ms.assetid: cbf4983c-551d-4771-870e-a192ed898eb7
ms.tgt_platform: multiple
keywords:
- Usando o Active Directory DsAddSidHistory
- Active Directory Active Directory usando, Usando DsAddSidHistory
- DsAddSidHistory Active Directory, usando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6e987a55f7fe39a8e4705f6aca9e44189e0f7a2
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881840"
---
# <a name="using-dsaddsidhistory"></a>Usando DsAddSidHistory

A [**função DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) obtém o SID (identificador de segurança) da conta primária de uma entidade de segurança de um domínio (o domínio de origem) e adiciona-o ao atributo **sIDHistory** de uma entidade de segurança em outro domínio (destino) em uma floresta diferente. Quando o domínio de origem está no modo nativo Windows 2000, essa função também recupera os valores **sIDHistory** da entidade de segurança de origem e os adiciona ao **sIDHistory** da entidade de destino.

Adicionar SIDs ao **sIDHistory** de uma entidade de segurança é uma operação sensível à segurança que efetivamente concede à entidade de segurança de destino acesso a todos os recursos acessíveis à entidade de segurança de origem, desde que existam confianças de domínios de recursos aplicáveis para o domínio de destino.

Em um modo nativo Windows 2000, um logon de usuário cria um token de acesso que contém os SIDs de grupo e SID da conta primária do usuário, bem como o **usuário sIDHistory** e **o sIDHistory** dos grupos dos quais o usuário é membro. Ter esses SIDs antigos **(valores sIDHistory)** no token do usuário concede ao usuário acesso aos recursos protegidos por ACLs (listas de controle de acesso) que contêm os SIDs antigos.

Essa operação facilita determinados Windows de implantação 2000. Em particular, ele dá suporte a um cenário no qual as contas em uma nova floresta do Windows 2000 são criadas para usuários e grupos que já existem em um ambiente de produção Windows NT 4.0. Ao colocar o SID da conta do Windows NT 4.0 na conta do Windows 2000 **sIDHistory,** o acesso aos recursos de rede é preservado para o logon do usuário em sua nova conta do Windows 2000.

[**O DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) também dá suporte à migração de BDCs (controladores de domínio de backup) do Windows NT 4.0 (ou DCs e servidores membros em um domínio Windows 2000) para um domínio Windows 2000 como servidores membros. Essa migração requer a criação, no domínio do Windows 2000, de grupos locais de domínio que contêm, em **seu sIDHistory,** os SIDs primários dos grupos locais definidos no BDC (ou grupos locais de domínio referenciados em ACLs nos servidores Windows 2000) no domínio de origem. Ao criar um grupo local de destino que contém **o sIDHistory** e todos os membros do grupo local de origem, o acesso aos recursos de servidor migrados, protegidos por ACLs que referenciam o grupo local de origem, é mantido para todos os membros.

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

Um novo grupo local, " &lt; SrcDomainName $$$", deve ser criado no domínio de origem &gt; para fins de auditoria.

## <a name="auditing"></a>Auditoria

[**As operações DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) são auditadas para garantir que os administradores de domínio de origem e de destino sejam capazes de detectar quando essa função foi executado. A auditoria é obrigatória nos domínios de origem e de destino. **DsAddSidHistory** verifica se o Modo de Auditoria está em cada domínio e se a auditoria do Gerenciamento de Conta de eventos de Êxito/Falha está em. No domínio de destino, um evento de auditoria exclusivo "Adicionar Histórico de Sid" é gerado para cada operação **DsAddSidHistory bem-sucedida** ou com falha.

Eventos de auditoria exclusivos de auditoria "Adicionar Histórico de Sid" não estão disponíveis Windows NT sistemas 4.0. Para gerar eventos de auditoria que refletem inequivocamente o uso de [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) no domínio de origem, ele executa operações em um grupo especial cujo nome é o identificador exclusivo no log de auditoria. Um grupo local, " SrcDomainName $$$", cujo nome é composto pelo nome NetBIOS do domínio de origem anexado com três cifrões &lt; &gt; ($) (código ASCII = 0x24 e Unicode = U+0024), deve ser criado no controlador de domínio de origem antes de chamar **DsAddSidHistory**. Cada usuário de origem e grupo global que é um destino dessa operação é adicionado e removido da associação desse grupo. Isso gera eventos de auditoria Adicionar Membro e Excluir Membro no domínio de origem, que podem ser monitorados pesquisando eventos que referenciam o nome do grupo.

> [!Note]  
> As operações [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) em grupos locais em um domínio de origem de modo misto do Windows NT 4.0 ou Windows 2000 não podem ser auditadas porque os grupos locais não podem ser membros de outro grupo local e, portanto, não podem ser adicionados ao grupo local especial " &lt; SrcDomainName &gt; $$$". Essa falta de auditoria não apresenta um problema de segurança para o domínio de origem, pois o acesso ao recurso de domínio de origem não é afetado por essa operação. Adicionar o SID de um grupo local de origem a um grupo local de destino não concede acesso aos recursos de origem, protegidos por esse grupo local, a nenhum usuário adicional. A adição de membros ao grupo local de destino não concede a eles acesso aos recursos de origem. Os membros adicionados recebem acesso somente aos servidores no domínio de destino migrados do domínio de origem, que podem ter recursos protegidos pelo SID do grupo local de origem.

 

## <a name="data-transmission-security"></a>Segurança de transmissão de dados

[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) impõe as seguintes medidas de segurança:

-   Chamadas de uma Windows 2000, as credenciais do chamador são usadas para autenticar e proteger a privacidade da chamada RPC para o controlador de domínio de destino. Se *SrcDomainCreds* não for **NULL,** a estação de trabalho e o DC de destino deverão dar suporte à criptografia de 128 bits para proteger a privacidade das credenciais. Se a criptografia de 128 bits não estiver disponível e *SrcDomainCreds* for fornecido, a chamada deverá ser feita no DC de destino.
-   O controlador de domínio de destino se comunica com o controlador de domínio de origem usando *SrcDomainCreds* ou as credenciais do chamador para autenticar mutuamente e proteger a integridade da leitura do SID da conta de origem (usando uma busca SAM) e **sIDHistory** (usando uma leitura LDAP).

## <a name="threat-models"></a>Modelos de ameaça

A tabela a seguir lista as possíveis ameaças associadas à chamada [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) e aborda as medidas de segurança pertinentes à ameaça específica.




| Ameaça potencial | Medida de segurança | 
|------------------|------------------|
| Man in the Middle Attack<br /> Um usuário não autorizado intercepta o <em>SID</em> de consulta da chamada de retorno do objeto de origem, substituindo o SID do objeto de origem por um SID arbitrário para inserção em um objeto de destino SIDhistory.<br /> | O <em>SID de lookup do objeto de</em> origem é um RPC autenticado, usando as credenciais de administrador do chamador, com proteção de mensagem de integridade do pacote. Isso garante que a chamada de retorno não possa ser modificada sem detecção. O controlador de domínio de destino cria um evento de auditoria exclusivo "Adicionar Histórico de SID" que reflete o SID adicionado à conta de <strong>destino sIDHistory</strong>.<br /> | 
| Domínio de origem do Troia<br /> Um usuário não autorizado cria um domínio de origem "Troia" em uma rede privada que tem o mesmo SID de domínio e alguns dos mesmos SIDs de conta que o domínio de origem legítimo. Em seguida, o usuário não autorizado tenta executar <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>DsAddSidHistory</strong></a> em um domínio de destino para obter o SID de uma conta de origem. Isso é feito sem a necessidade das credenciais do Administrador de Domínio de origem real e sem deixar uma trilha de auditoria no domínio de origem real. O método do usuário não autorizado para criar o domínio de origem do Troia De troia pode ser um dos seguintes:<ul><li>Obtenha uma cópia (backup do BDC) do domínio de origem SAM.</li><li>Crie um novo domínio, alterando o SID de domínio no disco para corresponder ao SID de domínio de origem legítimo e, em seguida, crie usuários suficientes para criar uma conta com o SID desejado.</li><li>Crie uma réplica BDC. Isso requer credenciais de administrador do domínio de origem. Em seguida, o usuário não autorizado leva a réplica para uma rede privada para implementar o ataque.</li></ul><br /> | Embora haja muitas maneiras para um usuário não autorizado recuperar ou criar um SID de objeto de origem desejado, o usuário não autorizado não pode usá-lo para atualizar o <strong>sIDHistory</strong> de uma conta sem ser membro do grupo administradores de domínio de destino. Como a verificação, no controlador de domínio de destino, para associação de Administrador de Domínio é em código, no DC de destino, não há nenhum método para fazer uma modificação de disco para alterar os dados de controle de acesso que protegem essa função. Uma tentativa de clonar uma conta de origem do Troia É auditada no domínio de destino. Esse ataque é atenuado com a reserva de associação no grupo Administradores de Domínio apenas para indivíduos altamente confiáveis.<br /> | 
| Modificação no disco do histórico de SID<br /> Um usuário sofisticado não autorizado, com credenciais de Administrador de Domínio e com acesso físico a um controlador de domínio no domínio de destino, pode modificar um valor <strong>sIDHistory</strong> da conta no disco.<br /> | Essa tentativa não está habilitada com o <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>uso de DsAddSidHistory.</strong></a> Esse ataque é atenuado impedindo o acesso físico aos controladores de domínio a todos, exceto administradores altamente confiáveis.<br /> | 
| Código não protegido usado para remover proteções<br /> Um usuário não autorizado ou administrador não autorizado com acesso físico ao código do Serviço de Diretório pode criar código não autorizado que:<ol><li>Remove a verificação de associação no grupo Administradores de Domínio no código.</li><li>Altera as chamadas no controlador de domínio de origem que aponta o SID para um LookupSidFromName que não é auditado.</li><li>Remove chamadas de log de auditoria.</li></ol><br /> | Alguém com acesso físico ao código DS e com conhecimento suficiente para criar código não autorizado tem a capacidade de modificar arbitrariamente o atributo <strong>sIDHistory</strong> de uma conta. A API <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>DsAddSidHistory</strong></a> não aumenta esse risco de segurança.<br /> | 
| Recursos vulneráveis a SIDs roubados<br /> Se um usuário não autorizado tiver êxito em usar um dos métodos descritos aqui para modificar uma conta <strong>sIDHistory</strong>e se os domínios de recursos de interesse confiarem no domínio de conta de usuário não autorizado, o usuário não autorizado poderá obter acesso não autorizado aos recursos do SID roubado, potencialmente sem deixar uma trilha de auditoria no domínio da conta do qual o SID foi roubado.<br /> | Os administradores de domínio de recursos protegem seus recursos configurando apenas as relações de confiança que fazem sentido de uma perspectiva de segurança. O uso <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>de DsAddSidHistory</strong></a> é restrito, no domínio de destino confiável, a membros do grupo Administradores de Domínio que já têm permissões amplas dentro do escopo de suas responsabilidades.<br /> | 
| Domínio de destino não está em operação<br /> Um usuário não autorizado cria um domínio Windows 2000 com uma conta cujo <strong>sIDHistory</strong> contém um SID que foi roubado de um domínio de origem. O usuário não autorizado usa essa conta para acesso não autorizado aos recursos.<br /> | O usuário não autorizado requer credenciais de Administrador para o domínio de origem para usar <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>DsAddSidHistory</strong></a>e deixa uma trilha de auditoria no controlador de domínio de origem. O domínio de destino não autorizado obtém acesso não autorizado somente em outros domínios que confiam no domínio não autorizado, o que requer privilégios de Administrador nesses domínios de recurso.<br /> | 




 

## <a name="operational-constraints"></a>Restrições operacionais

Esta seção descreve as restrições operacionais do uso [**da função DsAddSidHistory.**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya)

O SID *de SrcPrincipal* ainda não deve existir na floresta de destino, seja como um SID de conta primária ou no **sIDHistory** de uma conta. A exceção é [**que DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) não gera um erro ao tentar adicionar um SID a **um sIDHistory** que contém um SID idêntico. Esse comportamento permite que **DsAddSidHistory** seja executado várias vezes com entrada idêntica, resultando em êxito e um estado final consistente para a facilidade de uso do desenvolvedor de ferramentas.

> [!Note]  
> A latência de replicação do Catálogo Global pode fornecer uma janela durante a qual os SIDs duplicados podem ser criados. No entanto, SIDs duplicados podem ser facilmente excluídos por um administrador.

 

*SrcPrincipal* e *DstPrincipal* devem ser um dos seguintes tipos:

-   Usuário
-   Grupo habilitado para segurança, incluindo:

    <dl> Grupo local  
    Grupo global  
    Grupo local de domínio (Windows somente no modo nativo 2000)  
    Grupo universal (Windows somente no modo nativo 2000)  
    </dl>

Os tipos de objeto *de SrcPrincipal* e *DstPrincipal* devem corresponder.

-   Se *SrcPrincipal* for um Usuário, *DstPrincipal* deverá ser um Usuário.
-   Se *SrcPrincipal* for um grupo local ou de domínio local, *DstPrincipal* deverá ser um grupo local de domínio.
-   Se *SrcPrincipal* for um Grupo Global ou Universal, *DstPrincipal* deverá ser um Grupo Global ou Universal.

*SrcPrincipal* e *DstPrincipal* não podem ser um dos seguintes tipos: ([**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) falha com um erro nesses casos)

-   Computador (estação de trabalho ou controlador de domínio)
-   Confiança entre domínios
-   Conta duplicada temporária (recurso praticamente nãoutilado, um legado de LANman)
-   Contas com SIDs bem conhecidos. SIDs bem conhecidos são idênticos em cada domínio; Portanto, adiá-los a **um sIDHistory** violaria o requisito de exclusividade do SID de uma floresta Windows 2000. Contas com SIDs bem conhecidos incluem os seguintes grupos locais:

    <dl> Operadores de conta  
    Administradores  
    Operadores de backup  
    Convidados  
    Operadores de impressão  
    Replicador  
    Operadores de servidor  
    Usuários  
    </dl>

Se *SrcPrincipal* tiver um RID (identificador relativo) e um prefixo específico de domínio, ou seja, Administradores de Domínio, Usuários de Domínio e Computadores de Domínio, *DstPrincipal* deverá ter o mesmo RID conhecido para que [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) tenha êxito. Contas com RIDs conhecidos incluem os seguintes usuários e grupos globais:

-   Administrador
-   Convidado
-   Administradores de domínio
-   Convidados de domínio
-   Usuários de domínio

## <a name="setting-the-registry-value"></a>Definindo o valor do Registro

O procedimento a seguir mostra como definir o valor do Registro TcpipClientSupport.

**Para definir o valor do Registro TcpipClientSupport**

1.  Crie o valor do Registro a seguir como um valor REG DWORD no controlador de domínio de origem e \_ de definido seu valor como 1.

    **HKEY \_ LOCAL \_ MACHINE \\ SYSTEM \\ CurrentControlSet \\ Control \\ Lsa \\ TcpipClientSupport**

2.  Em seguida, reinicie o controlador de domínio de origem. Esse valor do Registro faz com que o SAM escute em TCP/IP. [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) falhará se esse valor não estiver definido no controlador de domínio de origem.

## <a name="enabling-auditing-of-usergroup-management-events"></a>Habilitando a auditoria de eventos de gerenciamento de usuários/grupos

O procedimento a seguir mostra como habilitar a auditoria de eventos de gerenciamento de usuário/grupo em um domínio de origem ou destino Windows 2000 ou Windows Server 2003.

**Para habilitar a auditoria de eventos de gerenciamento de usuário/grupo em um Windows 2000 ou Windows Server 2003 de origem ou de destino**

1.  No snap-in Usuários e Computadores do Active Directory MMC, selecione o contêiner Controladores de Domínio do domínio de destino.
2.  Clique com o botão **direito do mouse em Controladores de** Domínio e escolha **Propriedades**.
3.  Clique na **Política de Grupo** guia.
4.  Selecione a **Política de Controladores de Domínio Padrão** e clique em **Editar**.
5.  Em **Configuração do \\ Computador Windows Configurações Segurança Configurações Política de \\ \\ Auditoria \\** de Políticas Locais , clique duas vezes em **Audit Account Management**.
6.  Na janela **Gerenciamento de Conta de** Auditoria, selecione Auditoria de Êxito **e** Falha.  As atualizações de política entre em vigor após uma reinicialização ou após a atualização.
7.  Verifique se a auditoria está habilitada exibindo a política de auditoria efetiva Política de Grupo snap-in do MMC.

O procedimento a seguir mostra como habilitar a auditoria de eventos de gerenciamento de usuário/grupo em um domínio Windows NT 4.0.

**Para habilitar a auditoria de eventos de gerenciamento de usuário/grupo em um domínio Windows NT 4.0**

1.  No **Gerenciador de Usuários para Domínios**, clique no menu **Políticas** e selecione **Auditar**.
2.  Selecione **Auditar esses eventos.**
3.  Para **Gerenciamento de Usuários e Grupos**, marque Êxito e **Falha.**

O procedimento a seguir mostra como habilitar a auditoria de eventos de gerenciamento de Usuário/Grupo em um domínio de origem do Windows NT 4.0, Windows 2000 ou Windows Server 2003.

**Para habilitar a auditoria de eventos de gerenciamento de usuário/grupo em um domínio de origem Windows NT 4.0, Windows 2000 ou Windows Server 2003**

1.  No **Gerenciador de Usuários para Domínios**, clique **no** menu Usuário e selecione Novo **Grupo Local**.
2.  Insira um nome de grupo composto pelo domínio de origem Nome NetBIOS anexado com três cifrões ($), por exemplo, FABRIKAM$$$$. O campo de descrição deve indicar que esse grupo é usado para auditar o uso [**de DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) ou operações de clonagem. Verifique se não há membros no grupo. Clique em **OK**.

A [**operação DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) falhará se a auditoria de origem e destino não estiver habilitada, conforme descrito aqui.

## <a name="set-up-trust-if-required"></a>Configurar a confiança se necessário

Se um dos seguintes for true, uma relação de confiança deverá ser estabelecida do domínio de origem para o domínio de destino (isso deve ocorrer em uma floresta diferente):

-   O domínio de origem Windows Server 2003.
-   O domínio de origem Windows NT 4.0 e *SrcDomainCreds* é **NULL.**

 

 





