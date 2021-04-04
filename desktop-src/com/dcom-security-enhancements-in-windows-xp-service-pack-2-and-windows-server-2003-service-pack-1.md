---
title: Aprimoramentos de segurança DCOM no Windows XP Service Pack 2 e no Windows Server 2003 Service Pack 1
description: O Windows Server XP Service Pack 2 (SP2) e o Windows Server 2003 Service Pack 1 (SP1) apresentam configurações de segurança padrão aprimoradas para o DCOM (Distributed Component Object Model).
ms.assetid: 1917834c-5216-4ef3-a0c2-d8ca63cef53d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ad51807e27a9b97e8b05e467d8a84881c3993a
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104084927"
---
# <a name="dcom-security-enhancements-in-windows-xp-service-pack-2-and-windows-server-2003-service-pack-1"></a>Aprimoramentos de segurança DCOM no Windows XP Service Pack 2 e no Windows Server 2003 Service Pack 1

O Windows Server XP Service Pack 2 (SP2) e o Windows Server 2003 Service Pack 1 (SP1) apresentam configurações de segurança padrão aprimoradas para o DCOM (Distributed Component Object Model). Especificamente, eles apresentam direitos mais granulares que permitem que um administrador tenha controle independente sobre as permissões locais e remotas para iniciar, ativar e acessar servidores COM.

## <a name="what-does-dcom-do"></a>O que o DCOM faz?

O Microsoft Component Object Model (COM) é um sistema independente de plataforma, distribuído e orientado a objeto para a criação de componentes de software binários que podem interagir. O Distributed Component Object Model (DCOM) permite que os aplicativos sejam distribuídos entre locais que fazem mais sentido para você e para o aplicativo. O protocolo de conexão DCOM fornece suporte transparente para comunicação confiável, segura e eficiente entre os componentes COM.

## <a name="who-does-this-feature-apply-to"></a>A quem se aplica este recurso?

Se você usar somente COM para componentes COM em processo, esse recurso não se aplicará a você.

Esse recurso se aplicará a você se você tiver um aplicativo de servidor COM que atenda a um dos seguintes critérios:

-   A permissão de acesso para o aplicativo é menos estrita do que a permissão de inicialização, que é necessária para executar o aplicativo.
-   O aplicativo é geralmente ativado por um cliente COM remoto sem usar uma conta administrativa.
-   O aplicativo deve ser usado apenas localmente. Isso significa que você pode restringir seu aplicativo de servidor COM para que ele não seja acessível remotamente.

## <a name="what-new-functionality-is-added-to-this-feature-in-windows-xp-service-pack-2-and-windows-server-2003-service-pack-1"></a>Que nova funcionalidade é adicionada a esse recurso no Windows XP Service Pack 2 e no Windows Server 2003 Service Pack 1?

### <a name="computer-wide-restrictions"></a>Restrições em todo o computador

Foi feita uma alteração em COM para fornecer controles de acesso de todo o computador que regem o acesso a todas as solicitações de chamada, ativação ou inicialização no computador. A maneira mais simples de pensar sobre esses controles de acesso é como uma chamada [**AccessCheck**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck) adicional que é feita em uma ACL (lista de controle de acesso) de todo o computador em cada chamada, ativação ou inicialização de qualquer servidor com no computador. Se a **AccessCheck** falhar, a solicitação de chamada, ativação ou inicialização será negada. Isso é além de qualquer **AccessCheck** executada em relação às ACLs específicas do servidor. Na verdade, ele fornece um padrão de autorização mínimo que deve ser passado para acessar qualquer servidor COM no computador. Há uma ACL em todo o computador para permissões de inicialização para cobrir os direitos de ativação e inicialização e uma ACL em todo o computador para permissões de acesso para cobrir direitos de chamada. Eles podem ser configurados por meio do MMC (console de gerenciamento Microsoft) dos serviços de componentes.

Essas ACLs em todo o computador fornecem uma maneira de substituir configurações de segurança fracas especificadas por um aplicativo específico por meio de [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ou configurações de segurança específicas do aplicativo. Isso fornece um padrão de segurança mínimo que deve ser passado, independentemente das configurações do servidor específico.

Essas ACLs são verificadas quando as interfaces expostas por RPCSs são acessadas. Isso fornece um método para controlar o acesso a esse serviço do sistema.

Essas ACLs fornecem um local centralizado onde um administrador pode definir a diretiva de autorização geral que se aplica a todos os servidores COM no computador.

> [!Note]  
> Alterar as configurações de segurança de todo o computador afetará todos os aplicativos de servidor COM e poderá impedi-lo de funcionar corretamente. Se houver aplicativos de servidor COM que tenham restrições menos rigorosas do que as restrições em todo o computador, reduzir as restrições de computador poderá expor esses aplicativos para acesso indesejado. Por outro lado, se você aumentar as restrições de todo o computador, alguns aplicativos de servidor COM podem não estar mais acessíveis chamando aplicativos.

 

Por padrão, as configurações de restrição de computador do Windows XP SP2 são:



| Permissão        | Administrador                                                                                             | Todos                                            | Anônima               |
|-------------------|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------|-------------------------|
| Inicializar<br/> | Inicialização local<br/> Ativação local<br/> Inicialização remota<br/> Ativação remota<br/> | Inicialização local<br/> Ativação local<br/> |                         |
| Access<br/> |                                                                                                           | Acesso local<br/> Acesso remoto<br/>    | Acesso local<br/> |



 

Por padrão, as configurações de restrição de computador do Windows Server 2003 SP 1 são as seguintes.



| Permissão        | Administrador                                                                                             | Usuários COM distribuídos (grupo interno)                                                                    | Todos                                            | Anônima                                        |
|-------------------|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------|--------------------------------------------------|
| Inicializar<br/> | Inicialização local<br/> Ativação local<br/> Inicialização remota<br/> Ativação remota<br/> | Inicialização local<br/> Ativação local<br/> Inicialização remota<br/> Ativação remota<br/> | Inicialização local<br/> Ativação local<br/> | N/D<br/>                                   |
| Access<br/> | N/D<br/>                                                                                            | Acesso local<br/> Acesso remoto<br/>                                                          | Acesso local<br/> Acesso remoto<br/>    | Acesso local<br/> Acesso remoto<br/> |



 

> [!Note]  
> Os usuários COM distribuídos são um novo grupo interno incluído no Windows Server 2003 SP1 para agilizar o processo de adição de usuários às configurações de restrição do computador DCOM. Esse grupo faz parte da ACL usada pelas configurações [MachineAccessRestriction](machineaccessrestriction.md) e [MachineLaunchRestriction](machinelaunchrestriction.md) , portanto, a remoção de usuários desse grupo afetará essas configurações.

 

### <a name="why-is-this-change-important-what-threats-does-it-help-mitigate"></a>Por que essas alterações são importantes? Quais ameaças elas ajudam a minimizar?

Muitos aplicativos COM incluem um código específico de segurança (por exemplo, a chamada de [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)), mas usam configurações fracas, muitas vezes permitindo acesso não autenticado ao processo. Atualmente, não há como um administrador substituir essas configurações para forçar mais segurança em versões anteriores do Windows.

A infraestrutura COM inclui as RPCSs, um serviço do sistema que é executado durante a inicialização do sistema e sempre é executado depois disso. Ele gerencia a ativação de objetos COM e a tabela de objetos em execução e fornece serviços auxiliares para a comunicação remota DCOM. Ele expõe as interfaces RPC que podem ser chamadas remotamente. Como alguns servidores COM permitem acesso remoto não autenticado, essas interfaces podem ser chamadas por qualquer pessoa, incluindo usuários não autenticados. Como resultado, RPCSs podem ser atacados por usuários mal-intencionados em computadores remotos não autenticados.

Em versões anteriores do Windows, não havia como um administrador entender o nível de exposição dos servidores COM em um computador. Um administrador tem uma ideia do nível de exposição, verificando sistematicamente as configurações de segurança definidas para todos os aplicativos COM registrados no computador, mas, Considerando que há cerca de 150 servidores COM em uma instalação padrão do Windows, essa tarefa era assustadora. Não havia como exibir as configurações de um servidor que incorpora segurança no software, sem revisar o código-fonte desse software.

Restrições em todo o computador DCOM atenuam esses três problemas. Ele também dá a um administrador a capacidade de desabilitar a ativação, a inicialização e as chamadas de DCOM de entrada.

### <a name="what-works-differently"></a>O que passou a funcionar de maneira diferente?

Por padrão, o grupo Everyone recebe permissões de inicialização local, ativação local e chamada de acesso local. Isso permite que todos os cenários locais funcionem sem modificação no software ou no sistema operacional.

Por padrão, no Windows XP SP2, o grupo Everyone recebe permissões de chamada de acesso remoto. No Windows Server 2003 SP1, os grupos Everyone e Anonymous recebem permissões de acesso remoto. Isso permite a maioria dos cenários de cliente COM, incluindo o caso comum em que um cliente COM passa uma referência local para um servidor remoto, em vigor, ligando o cliente a um servidor. No Windows XP SP2, isso pode desabilitar cenários que exigem chamadas de acesso remoto não autenticadas.

Também por padrão, somente os membros do grupo Administradores recebem permissões de ativação e inicialização remota. Isso desabilita ativações remotas por não administradores para servidores COM instalados.

### <a name="how-do-i-resolve-these-issues"></a>Como fazer resolver esses problemas?

Se você implementar um servidor COM e esperar oferecer suporte à ativação remota por um cliente COM não administrativo, deverá considerar se o risco associado à habilitação desse processo é aceitável ou se você deve modificar sua implementação para não exigir ativação remota por um cliente COM não administrativo ou chamadas remotas não autenticadas.

Se o risco for aceitável e você quiser habilitar a ativação remota por um cliente COM não administrativo ou chamadas remotas não autenticadas, será necessário alterar a configuração padrão para esse recurso.

> [!Note]  
> Alterar as configurações de segurança de todo o computador afetará todos os aplicativos de servidor COM e poderá impedi-lo de funcionar corretamente. Se houver aplicativos de servidor COM que tenham restrições menos rigorosas do que as restrições em todo o computador, reduzir as restrições de computador poderá expor esses aplicativos para acesso indesejado. Por outro lado, se você aumentar as restrições de todo o computador, alguns aplicativos de servidor COM podem não estar mais acessíveis chamando aplicativos.

 

Você pode alterar os parâmetros de configuração usando o MMC (console de gerenciamento Microsoft) dos serviços de componentes ou o registro do Windows.

Se você usar o snap-in do MMC dos serviços de componentes, essas configurações poderão ser definidas na guia **segurança com** da caixa de diálogo **Propriedades** do computador que você está gerenciando. A área **permissões de acesso** foi modificada para permitir que você defina limites de todo o computador, além das configurações padrão para servidores com. Além disso, você pode fornecer configurações de ACL separadas para acesso local e remoto em limites e padrões.

Na área **permissões de inicialização e ativação** , você pode controlar as permissões locais e remotas, bem como os limites de todo o computador e os padrões. Você pode especificar as permissões de ativação local e remota e de inicialização independentemente.

Como alternativa, você pode definir essas configurações de ACL usando o registro.

Essas ACLs são armazenadas no registro nos seguintes locais:

``` syntax
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole\MachineAccessRestriction=ACL
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole\MachineLaunchRestriction=ACL
```

Esses são valores nomeados do tipo REG \_ Binary que contêm dados que descrevem a ACL das entidades de segurança que podem acessar qualquer classe com ou objeto com no computador. Os direitos de acesso na ACL são:

``` syntax
COM_RIGHTS_EXECUTE 1
COM_RIGHTS_EXECUTE_LOCAL 2
COM_RIGHTS_EXECUTE_REMOTE 4
COM_RIGHTS_ACTIVATE_LOCAL 8
COM_RIGHTS_ACTIVATE_REMOTE 16
```

Essas ACLs podem ser criadas usando funções de segurança normais.

> [!Note]  
> Para fornecer compatibilidade com versões anteriores, uma ACL pode existir no formato usado antes do Windows XP SP2 e do Windows Server 2003 SP1, que usa apenas o direito de acesso COM direitos de COM \_ \_ , ou pode existir no novo formato usado no Windows XP SP2 e no windows Server 2003 SP1, que usa os direitos com, \_ \_ executados junto com uma combinação de \_ direitos COM \_ \_ , executar direitos de com e executar \_ \_ \_ controle remoto, os direitos com são \_ \_ ativados \_ e os direitos com são \_ \_ ativados \_ remotamente. Observe que \_ os direitos com \_ executam> devem estar sempre presentes; a ausência desse direito gera um descritor de segurança inválido. Observe também que você não deve misturar o formato antigo e o novo formato em uma única ACL; todas as ACEs (entradas de controle de acesso) devem conceder apenas o \_ direito de acesso de execução de direitos com \_ , ou todas elas devem conceder direitos com a serem \_ \_ executadas junto com uma combinação de direitos com, \_ executar direitos de com, executar \_ \_ \_ \_ \_ remotamente, \_ direitos com \_ \_ e direitos com \_ \_ Ativar \_ remotamente.

 

> [!Note]  
> Somente os usuários com direitos de administrador podem modificar essas configurações.

 

## <a name="what-existing-functionality-is-changing-in-windows-xp-service-pack-2-and-windows-server-2003-service-pack-1"></a>Qual funcionalidade existente está mudando no Windows XP Service Pack 2 e no Windows Server 2003 Service Pack 1?

### <a name="rpcss-runs-as-a-network-service"></a>RPCSs são executados como um serviço de rede

RPCSs é um serviço de chave para a infraestrutura de mapeador de ponto de extremidade RPC e DCOM. Esse serviço foi executado como sistema local em versões anteriores do Windows. Para reduzir a superfície de ataque do Windows e fornecer defesa profunda, a funcionalidade do RPCSs Service foi dividida em dois serviços. O serviço RPCSs com toda a funcionalidade original que não exigia privilégios de sistema local agora é executado na conta de serviço de rede. Um novo serviço DCOMLaunch que inclui a funcionalidade que exige privilégios do sistema local é executado na conta sistema local.

### <a name="why-is-this-change-important"></a>Por que essas alterações são importantes?

Essa alteração reduz a superfície de ataque e fornece defesa profunda para o serviço RPCSs porque uma elevação de privilégio no serviço RPCSs agora é limitada ao privilégio de serviço de rede.

### <a name="what-works-differently"></a>O que passou a funcionar de maneira diferente?

Essa alteração deve ser transparente para os usuários porque a combinação dos RPCSs e dos serviços DCOMLaunchs é equivalente ao serviço RPCSs anterior fornecido nas versões anteriores do Windows.

### <a name="more-specific-com-permissions"></a>Permissões COM mais específicas

Os aplicativos de servidor COM têm dois tipos de permissões: permissões de inicialização e permissões de acesso. As permissões de inicialização controlam a autorização para iniciar um servidor COM durante a ativação COM, se o servidor ainda não estiver em execução. Essas permissões são definidas como descritores de segurança que são especificados nas configurações do registro. Permissões de acesso controlam a autorização para chamar um servidor COM em execução. Essas permissões são definidas como descritores de segurança fornecidos para a infraestrutura COM por meio da API [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ou usando configurações do registro. As permissões de inicialização e de acesso permitem ou negam o acesso com base em entidades de segurança e não fazem distinção com o fato de o chamador ser local para o servidor ou remoto.

A primeira alteração distingue os direitos de acesso COM, com base na distância. As duas distâncias definidas são local e remota. Uma mensagem COM local chega por meio do protocolo LRPC (chamada de procedimento remoto) local, enquanto uma mensagem COM remota chega por meio de um protocolo de host RPC (chamada de procedimento remoto) como TCP (protocolo de controle de transmissão).

A ativação COM é o ato de obter um proxy de interface COM em um cliente chamando [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) ou uma de suas variantes. Como um efeito colateral desse processo de ativação, às vezes, um servidor COM deve ser iniciado para atender à solicitação do cliente. Uma ACL de permissões de inicialização declara quem tem permissão para iniciar um servidor COM. Uma ACL de permissões de acesso declara quem tem permissão para ativar um objeto COM ou chamar esse objeto depois que o servidor COM já estiver em execução.

A segunda alteração é que os direitos de chamada e ativação são separados para refletir para duas operações distintas e para mover o direito de ativação da ACL de permissão de acesso para a ACL de permissão de inicialização. Como a ativação e a inicialização estão relacionadas à aquisição de um ponteiro de interface, os direitos de acesso de ativação e inicialização logicamente pertencem a uma ACL. E como você sempre especifica as permissões de inicialização por meio da configuração (em comparação com as permissões de acesso, que geralmente são especificadas de forma programática), colocar os direitos de ativação na ACL de permissão de inicialização fornece ao administrador controle sobre a ativação.

As ACEs (entradas de controle de acesso) da permissão de inicialização são divididas em quatro direitos de acesso:

-   Inicialização local (LL)
-   Inicialização remota (RL)
-   Ativação local (LA)
-   Ativação remota (RA)

O descritor de segurança de permissão de acesso é dividido em dois direitos de acesso:

-   Chamadas de acesso local (LC)
-   Chamadas de acesso remoto (RC)

Isso permite que o administrador aplique configurações de segurança muito específicas. Por exemplo, você pode configurar um servidor COM para que ele aceite chamadas de acesso local de todos, enquanto aceita apenas chamadas de acesso remoto de administradores. Essas distinções podem ser especificadas por meio de alterações nos descritores de segurança de permissões COM.

### <a name="why-is-this-change-important-what-threats-does-it-help-mitigate"></a>Por que essas alterações são importantes? Quais ameaças elas ajudam a minimizar?

As versões anteriores do aplicativo de servidor COM não têm como restringir um aplicativo para que ele só possa ser usado localmente sem expor o aplicativo na rede por meio do DCOM. Quando um usuário tem acesso a um aplicativo de servidor COM, ele tem acesso para uso local e remoto.

Um aplicativo de servidor COM pode se expor a usuários não autenticados para implementar um cenário de retorno de chamada COM. Nesse cenário, o aplicativo também deve expor sua ativação a usuários não autenticados, o que pode não ser desejável.

As permissões COM precisas dão flexibilidade ao administrador para controlar a política de permissão COM de um computador. Essas permissões habilitam a segurança para os cenários descritos.

### <a name="what-works-differently-are-there-any-dependencies"></a>O que passou a funcionar de maneira diferente? Há alguma dependência?

Para fornecer compatibilidade COM versões anteriores, os descritores de segurança COM existentes são interpretados para permitir ou negar o acesso local e remoto simultaneamente. Ou seja, uma ACE (entrada de controle de acesso) permite local e remoto ou nega local e remoto.

Não há problemas de compatibilidade com versões anteriores para direitos de chamada ou inicialização. Há, no entanto, um problema de compatibilidade de direitos de ativação. Se, nos descritores de segurança existentes de um servidor COM, as permissões de inicialização configuradas forem mais restritivas do que as permissões de acesso e forem mais restritivas do que o mínimo necessário para cenários de ativação do cliente, a ACL de permissões de inicialização deverá ser modificada para conceder aos clientes autorizados as permissões de ativação apropriadas.

Para aplicativos COM que usam as configurações de segurança padrão, não há nenhum problema de compatibilidade. Para aplicativos que são iniciados dinamicamente usando a ativação COM, a maioria não tem problemas de compatibilidade, pois as permissões de inicialização já devem incluir qualquer pessoa que possa ativar um objeto. Caso contrário, esses aplicativos geram falhas de ativação mesmo antes de aplicar o Windows XP SP2 ou o Windows Server 2003 SP1, quando os chamadores sem permissão de inicialização tentarem ativar um objeto e o servidor COM ainda não estiver em execução.

Os aplicativos da maior preocupação de problemas de compatibilidade são aplicativos COM que já foram iniciados por algum outro mecanismo, como o Windows Explorer ou o Gerenciador de controle de serviços. Você também pode iniciar esses aplicativos por uma ativação COM anterior, que substitui as permissões de inicialização e acesso padrão e especifica permissões de inicialização mais restritivas do que as permissões de chamada. Para obter mais detalhes sobre como abordar esse problema de compatibilidade, consulte "Como fazer resolver esses problemas?" na próxima seção.

Se um sistema que é atualizado para o Windows XP SP2 ou o Windows Server 2003 SP1 for revertido para um estado anterior, qualquer ACE que tenha sido editada para permitir acesso local, acesso remoto ou ambos, será interpretado para permitir o acesso local e remoto. Qualquer ACE que foi editada para negar acesso local, acesso remoto ou ambos, é interpretado para negar acesso local e remoto. Sempre que você desinstala um service pack, você deve garantir que nenhuma Ace definida recentemente faça com que os aplicativos parem de funcionar.

### <a name="how-do-i-resolve-these-issues"></a>Como fazer resolver esses problemas?

Se você implementar um servidor COM e substituir as configurações de segurança padrão, confirme se a ACL de permissões de inicialização específica do aplicativo concede permissão de ativação aos usuários apropriados. Se não tiver, você deverá alterar sua ACL de permissão de inicialização específica do aplicativo para dar aos usuários apropriados direitos de ativação para que os aplicativos e componentes do Windows que usam DCOM não falhem. Essas permissões de inicialização específicas do aplicativo são armazenadas no registro.

As ACLs COM podem ser criadas ou modificadas usando funções de segurança normais.

## <a name="what-settings-are-added-or-changed-in-windows-xp-service-pack-2"></a>Quais configurações são adicionadas ou alteradas no Windows XP Service Pack 2?

> [!Caution]  
> O uso impróprio dessas configurações pode fazer com que aplicativos e componentes do Windows que usam DCOM falhem.

 

Na tabela a seguir, essas abreviações são usadas:

LL-início local

LA-ativação local

RL-inicialização remota

RA-ativação remota

LC-chamadas de acesso local

RC-chamadas de acesso remoto

ACL-lista de controle de acesso



| Nome da configuração                                                                                         | Local                                                                                                       | Valor padrão anterior                                                                                                                                                                     | Valor padrão                                                                                                                                                                                                                                                                                                                                                             | Valores possíveis                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MachineLaunchRestriction**<br/>                                                              | **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ OLE**<br/>                                                 | Everyone-LL, LA, RL, RA<br/> Modo<br/> LL, LA, RL, RA<br/> (Essa é uma nova chave do registro. Com base no comportamento existente, esses são os valores efetivos.)<br/> | Administrador: LL, LA, RL, RA<br/>                                                                                                                                                                                                                                                                                                                                  | LCA<br/>                                                                                                                                                                                                               |
| **MachineAccessRestriction**<br/>                                                              | **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ OLE**<br/>                                                 | Everyone-LC, RC<br/> Anônimo-LC, RC<br/> (Essa é uma nova chave do registro. Com base no comportamento existente, esses são os valores efetivos.)<br/>                            | Todos: LC, RC<br/> Anônimo: LC<br/>                                                                                                                                                                                                                                                                                                                      | LCA<br/>                                                                                                                                                                                                               |
| **CallFailureLoggingLevel**<br/>                                                               | **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ OLE**<br/>                                                 | Não aplicável.<br/>                                                                                                                                                                 | Esta chave do registro não está presente; no entanto, uma chave ou valor ausente é interpretado como 2.<br/> Esse evento não é registrado por padrão. Se você alterar esse valor para 1 para iniciar o registro dessas informações para ajudá-lo a solucionar um problema, certifique-se de monitorar o tamanho do seu log de eventos, pois esse é um evento que pode gerar um grande número de entradas.<br/> | 1-sempre registrar falhas no log de eventos durante uma chamada no processo do servidor COM.<br/> 2-nunca registrar em log as falhas do log de eventos durante uma chamada no processo do servidor de chamada.<br/>                                                  |
| **InvalidSecurityDescriptorLoggingLevel**<br/>                                                 | **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ OLE**<br/>                                                 | Não aplicável.<br/>                                                                                                                                                                 | Esta chave do registro não está presente; no entanto, uma chave ou valor ausente é interpretado como 1.<br/> Esse evento é registrado por padrão. Isso raramente deve ocorrer.<br/>                                                                                                                                                                                                    | 1-sempre registrar falhas no log de eventos quando a infraestrutura COM encontrar um descritor de segurança inválido.<br/> 2-nunca registra falhas no log de eventos quando a infraestrutura COM encontra um descritor de segurança inválido.<br/> |
| DCOM: restrições de inicialização de computador na sintaxe SDDL (Security Descriptor Definition Language)<br/> | (Objeto Política de Grupo) Configuração do computador \\ configurações do Windows \\ políticas locais \\ Opções de segurança<br/>  | Não aplicável.<br/>                                                                                                                                                                 | Não definido<br/>                                                                                                                                                                                                                                                                                                                                                    | Lista de controle de acesso no formato SDDL. A existência dessa política substitui os valores em MachineLaunchRestriction, anteriormente.<br/>                                                                                            |
| DCOM: restrições de acesso ao computador na sintaxe SDDL (Security Descriptor Definition Language)<br/> | (Objeto Política de Grupo) Configuração do computador \\ configurações do Windows \\ políticas locais \\ Opções de segurança<br/> | Não aplicável.<br/>                                                                                                                                                                 | Não definido<br/>                                                                                                                                                                                                                                                                                                                                                    | Lista de controle de acesso no formato SDDL. A existência dessa política substitui os valores em MachineAccessRestriction, anteriormente.<br/>                                                                                            |



 

## <a name="what-settings-are-added-or-changed-in-windows-server-2003-service-pack-1"></a>Quais configurações foram adicionadas ou alteradas no Windows Server 2003 Service Pack 1?

> [!Note]  
> O uso impróprio dessas configurações pode fazer com que aplicativos e componentes do Windows que usam DCOM falhem.

 

Na tabela a seguir, essas abreviações são usadas:

LL-início local

LA-ativação local

RL-inicialização remota

RA-ativação remota

LC-chamadas de acesso local

RC-chamadas de acesso remoto

ACL-lista de controle de acesso



| Nome da configuração                                                                                         | Local                                                                                                       | Valor padrão anterior                                                                                                                                                             | Valor padrão                                                                                                                                                                                                                                                                                                                                                             | Valores possíveis                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MachineLaunchRestriction**<br/>                                                              | **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ OLE**<br/>                                                 | Everyone: LL, LA, RL, RA<br/> Anônimo: LL, LA, RL, RA<br/> (Essa é uma nova chave do registro. Com base no comportamento existente, esses seriam os valores efetivos.)<br/> | Administrador: LL, LA, RL, RA<br/> Everyone: LL, LA<br/> Usuários COM distribuídos: LL, LA, RL, RA<br/>                                                                                                                                                                                                                                                     | LCA<br/>                                                                                                                                                                                                               |
| **MachineAccessRestriction**<br/>                                                              | **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ OLE**<br/>                                                 | Todos: LC, RC<br/> Anônimo: LC, RC<br/> (Essa é uma nova chave do registro. Com base no comportamento existente, esses seriam os valores efetivos.)<br/>                 | Todos: LC, RC<br/> Anônimo: LC, RC<br/>                                                                                                                                                                                                                                                                                                                  | LCA<br/>                                                                                                                                                                                                               |
| **CallFailureLoggingLevel**<br/>                                                               | **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ OLE**<br/>                                                 | Não aplicável.<br/>                                                                                                                                                         | Esta chave do registro não está presente; no entanto, uma chave ou valor ausente é interpretado como 2.<br/> Esse evento não é registrado por padrão. Se você alterar esse valor para 1 para iniciar o registro dessas informações para ajudá-lo a solucionar um problema, certifique-se de monitorar o tamanho do seu log de eventos, pois esse é um evento que pode gerar um grande número de entradas.<br/> | 1-sempre registrar falhas no log de eventos quando a infraestrutura COM encontrar um descritor de segurança inválido.<br/> 2-nunca registra falhas no log de eventos quando a infraestrutura COM encontra um descritor de segurança inválido.<br/> |
| **InvalidSecurityDescriptorLoggingLevel**<br/>                                                 | **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ OLE**<br/>                                                 | Não aplicável.<br/>                                                                                                                                                         | Esta chave do registro não está presente; no entanto, uma chave ou valor ausente é interpretado como 1.<br/> Esse evento é registrado por padrão. Isso raramente deve ocorrer.<br/>                                                                                                                                                                                                    | 1-sempre registrar falhas no log de eventos quando a infraestrutura COM encontrar um descritor de segurança inválido.<br/> 2-nunca registrar falhas no log de eventos quando a infraestrutura COM encontrar um descritor de segurança inválido.<br/>         |
| DCOM: restrições de inicialização de computador na sintaxe SDDL (Security Descriptor Definition Language)<br/> | (Objeto Política de Grupo) Configuração do computador \\ configurações do Windows \\ políticas locais \\ Opções de segurança<br/> | Não aplicável.<br/>                                                                                                                                                         | Não definido.<br/>                                                                                                                                                                                                                                                                                                                                                   | Lista de controle de acesso no formato SDDL. A existência dessa política substitui os valores em MachineLaunchRestriction, anteriormente.<br/>                                                                                            |
| DCOM: restrições de acesso ao computador na sintaxe SDDL (Security Descriptor Definition Language)<br/> | (Objeto Política de Grupo) Configuração do computador \\ configurações do Windows \\ políticas locais \\ Opções de segurança<br/> | Não aplicável.<br/>                                                                                                                                                         | Não definido.<br/>                                                                                                                                                                                                                                                                                                                                                   | Lista de controle de acesso no formato SDDL. A existência dessa política substitui os valores em MachineAccessRestriction, anteriormente.<br/>                                                                                            |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Segurança em COM](security-in-com.md)
</dt> </dl>

 

