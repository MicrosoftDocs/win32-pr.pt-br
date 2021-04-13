---
description: A versão 1,5 do COM+ adiciona novos recursos projetados para aumentar a escalabilidade, a disponibilidade e a capacidade de gerenciamento gerais dos aplicativos COM+ para desenvolvedores e administradores de sistema.
ms.assetid: e7073ba5-6b19-4d94-8cc0-b4e16bb44afd
title: Novidades no COM+ 1,5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 994237002ea5d19c2cb00364f1064df38ed7271f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370476"
---
# <a name="whats-new-in-com-15"></a>O que há de novo no COM+ 1,5

A versão 1,5 do COM+ adiciona novos recursos projetados para aumentar a escalabilidade, a disponibilidade e a capacidade de gerenciamento gerais dos aplicativos COM+ para desenvolvedores e administradores de sistema.

O COM+ 1,5 está disponível a partir do Windows XP e do Windows Server 2003. Os novos recursos do COM+ 1,5 não estão disponíveis no Windows 2000.

## <a name="application-level-access-checks-enabled-by-default"></a>Application-Level verificações de acesso habilitadas por padrão

Como parte da segurança aprimorada do sistema, as verificações de acesso são habilitadas por padrão ao criar um aplicativo COM+. Em versões anteriores, as verificações de acesso foram desabilitadas por padrão no nível do aplicativo e habilitadas por padrão no nível do componente. A partir do Windows Server 2003, as verificações de acesso são habilitadas por padrão no nível do aplicativo e desabilitadas por padrão no nível do componente. Consulte [criando um novo aplicativo com+](creating-a-new-com--application.md), [habilitando verificações de acesso para um aplicativo](enabling-access-checks-for-an-application.md)e [habilitando verificações de acesso no nível do componente](enabling-access-checks-at-the-component-level.md) para obter mais informações e procedimentos sobre como alterar as configurações padrão.

## <a name="application-pooling"></a>Pool de aplicativos

Com a nova propriedade ConcurrentApps do objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) na coleção de [**aplicativos**](applications.md) , o pool de aplicativos com+ adiciona escalabilidade para processos de thread único e integra-se com o novo serviço de reciclagem de aplicativo com+. Consulte [pool de aplicativos com+](com--application-pooling.md) para obter informações detalhadas.

## <a name="application-recycling"></a>Reciclagem de aplicativos

A reciclagem de aplicativos aumenta significativamente a estabilidade geral dos seus aplicativos. Como o desempenho da maioria dos aplicativos pode ser prejudicado ao longo do tempo devido a fatores como vazamentos de memória, a dependência de código de terceiros e o uso de recursos não escalonáveis, a reciclagem de aplicativos COM+ fornece uma solução simples para desligar um processo associado a um aplicativo e reiniciá-lo. Consulte [reciclagem de aplicativos com+](com--application-recycling.md) para obter informações detalhadas. Consulte também "Configurando a reciclagem de processo" na ajuda da administração dos serviços de componentes para obter um procedimento passo a passo para configurar a reciclagem do processo.

## <a name="com-partitions"></a>Partições COM+

Nesta versão, o COM+ apresenta suporte para partições COM+, um recurso que permite que várias versões de aplicativos COM+ sejam instaladas e configuradas no mesmo computador. Esse recurso pode poupar o custo e o esforço demorado de usar vários servidores para gerenciar versões diferentes de um aplicativo. Em um único computador, cada partição atua, em vigor, como um servidor virtual. Depois de instalar o aplicativo em cada partição, você cria conjuntos de partições que mapeiam os usuários para os servidores lógicos. Consulte [partições com+](com--partitions.md) para obter informações detalhadas sobre como configurar e gerenciar partições com+. Consulte também "administrando partições de aplicativo" na ajuda da administração dos serviços de componentes para obter procedimentos passo a passo.

## <a name="com-services-without-components"></a>Serviços COM+ sem componentes

Com o COM+ 1,5, você pode usar os serviços fornecidos pelo COM+ sem a necessidade de criar um componente para conter os métodos que chamam esses serviços. Isso beneficia muito os desenvolvedores que normalmente não usam componentes, mas desejam usar serviços COM+, como transações ou o controlador COM+. Usando serviços COM+ sem componentes, os desenvolvedores podem evitar a sobrecarga de criar um componente que é usado para acessar apenas os serviços COM+ de que precisam. Consulte [serviços com+ sem componentes](com--services-without-components.md) para obter informações detalhadas.

## <a name="com-soap-service"></a>Serviço SOAP COM+

Com o COM+ 1,5, agora você pode expor um aplicativo COM+ como um serviço Web XML. Você também pode usar um Web Service XML de modo transparente, seja implantado usando COM+ ou não, como um componente COM. Isso significa que você pode criar facilmente novos serviços Web XML fora dos aplicativos COM+ existentes e incorporar facilmente os serviços Web XML em novos aplicativos COM+. Consulte [serviço SOAP com+](com--soap-service.md) para obter informações detalhadas.

## <a name="configurable-isolation-levels"></a>Níveis de isolamento configuráveis

Os desenvolvedores de COM+ podem usar a nova propriedade TxIsolationLevel ou a ferramenta administrativa serviços de componentes para configurar o nível de isolamento de um aplicativo de acordo com a necessidade, ajudando a aumentar a simultaneidade, o desempenho e a escalabilidade. Essa flexibilidade permite que aqueles com a quantidade certa de experiência para obter cada último onça da produtividade de seus aplicativos. Consulte [Configurando níveis de isolamento da transação](configuring-transaction-isolation-levels.md) para obter informações detalhadas.

## <a name="creating-private-components"></a>Criando componentes privados

Em cenários em que você tem vários componentes auxiliares em um aplicativo que devem ser chamados apenas de outros componentes dentro desse aplicativo, esta versão do COM+ permite que você use uma nova propriedade, IsPrivateComponent, para marcar esses componentes como particulares. (Na versão anterior do COM+, todos os componentes tinham que ser públicos para terem acesso aos serviços COM+, o que significa que esses componentes poderiam ser ativados de outros aplicativos.) Um componente privado pode ser visto e ativado somente por outros componentes no mesmo aplicativo, dando a você mais controle sobre a funcionalidade a ser exposta. Você precisa apenas documentar e manter os componentes públicos, ao mesmo tempo em que faz uso de componentes privados que não podem ser acessados de fora do aplicativo, mas que ainda podem tirar proveito de todos os serviços COM+.

## <a name="dtc-security-settings"></a>Configurações de segurança do DTC

Várias novas configurações de segurança foram adicionadas ao Microsoft Coordenador de Transações Distribuídas (DTC), permitindo que você personalize seus níveis de segurança para gerenciar transações distribuídas. Consulte Considerações de segurança do DTC sobre essas configurações e como implementá-las.

Para facilitar a autenticação mútua, o DTC é restrito à execução na conta NetworkService. Consulte Gerenciando contas e privilégios para obter informações detalhadas.

Para recuperação com bancos de dados XA, é recomendável que a conta NetworkService seja fornecida às permissões e às funções necessárias para realizar essa recuperação. O método exato de fazer isso é específico para cada banco de dados. Consulte desabilitando transações distribuídas nativas e desabilitando transações TIP e XA para obter mais informações.

Para ajudar a fornecer um sistema mais seguro ao usar transações XA, as plataformas do Windows Server 2003 incluem uma nova entrada de registro para especificar arquivos DLL do XA. Ao atualizar para o Windows Server 2003, você pode trabalhar com transações XA como antes, criando uma entrada de registro em **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ MSDTC \\ XADLL**, em que o nome do valor é o nome da dll (no formato *DllName*. dll) e o valor é o caminho completo do arquivo dll. Você precisa criar uma entrada para cada arquivo DLL XA em uso. Se o computador que executa o DTC fizer parte de um cluster, a entrada do registro precisará ser feita para cada nó no cluster. Consulte Gerenciando transações XA para obter mais informações.

## <a name="low-memory-activation-gates"></a>Low-Memory Gates de ativação

Com esta versão, o COM+ verifica a memória automaticamente antes de criar um servidor ou objeto COM+. Se a porcentagem de memória virtual disponível para o aplicativo ficar abaixo de um limite fixo, a ativação falhará antes de o objeto ser criado. Ao falhar com essas ativações que normalmente seriam executadas, o serviço [COM+ Low-Memory ativação de entradas](com--low-memory-activation-gates.md) melhora muito a confiabilidade do sistema.

## <a name="moving-and-copying-com-components"></a>Movendo e copiando componentes COM

Com esta versão, o COM+ permite que você mova e copie seus componentes. Isso significa que você pode configurar uma única implementação física de um componente muitas vezes diferentes. Você obtém reutilização de componentes em um nível binário em vez de no nível de código-fonte, o que resulta em menos código, menores custos de desenvolvimento e tempo de colocação no mercado mais rápido. Consulte [movendo componentes](moving-components.md) e [copiando componentes](copying-components.md) para obter informações detalhadas.

## <a name="network-access"></a>Acesso de rede

O acesso à rede COM+ é desabilitado por padrão no Windows Server 2003, o que significa que COM+ pode ser usado somente localmente por padrão. Use o procedimento a seguir para habilitar o acesso de COM+ de rede.

**Para habilitar o acesso de COM+ de rede**

1.  No menu **Iniciar** , aponte para **painel de controle** e, em seguida, selecione **Adicionar ou remover programas**.

2.  Clique em **Adicionar ou remover componentes do Windows**.

3.  Selecione **Servidor de Aplicativos** e clique em **Detalhes**.

4.  Marque a caixa ao lado de **habilitar acesso de com+ de rede** e clique em **OK**.

5.  Clique em **Avançar** para concluir o assistente de componentes do Windows.

6.  Clique em **concluir** para fechar o assistente.

O acesso às transações de rede do DTC está desabilitado por padrão no Windows Server 2003. Nessas plataformas, o DTC pode executar apenas transações locais por padrão. Use o procedimento a seguir para habilitar o acesso DTC de rede.

> [!NOTE]
> Você também pode habilitar o acesso DTC de rede usando a ferramenta administrativa serviços de componentes ou programaticamente por meio da biblioteca de administração COM+. Para obter informações de procedimento, consulte "Configurando a segurança do DTC" na ajuda da administração de serviços de componentes.

**Para habilitar o acesso DTC de rede**

1.  No menu **Iniciar** , aponte para **painel de controle** e, em seguida, selecione **Adicionar ou remover programas**.

2.  Clique em **Adicionar ou remover componentes do Windows**.

3.  Selecione **Servidor de Aplicativos** e clique em **Detalhes**.

4.  Marque a caixa ao lado de **habilitar acesso DTC de rede** e clique em **OK**.

5.  Clique em **Avançar** para concluir o assistente de componentes do Windows.

6.  Clique em **concluir** para fechar o assistente.

## <a name="pausing-and-disabling-applications"></a>Pausando e desabilitando aplicativos

Os aplicativos COM+ agora são mais gerenciáveis. Um administrador pode pausar e retomar aplicativos do servidor COM+ ou desabilitar e habilitar aplicativos de biblioteca ou servidor COM+, ou até mesmo componentes individuais configurados. Os recursos de pausa e desativação impedem ativações futuras sem afetar as instâncias de componentes existentes. Consulte "administrando aplicativos COM+" na ajuda da administração de serviços de componentes para obter mais informações.

## <a name="process-dumping"></a>Despejo de processo

Não é fácil solucionar problemas de aplicativos em um ambiente de produção. Como coletar informações sobre um problema sem perturbar os processos em execução? O COM+ agora fornece uma solução por meio de seu novo recurso de despejo de processo. Esse recurso permite que o administrador do sistema despeje todo o estado de um processo sem encerrá-lo. Consulte "administrando a ferramenta de despejo de processo para depurar aplicativos COM+" na ajuda da administração de serviços de componentes para obter mais informações.

## <a name="process-initialization"></a>Inicialização do processo

Muitos aplicativos de servidor precisam fazer inicialização e limpeza específicas quando são iniciados e desligados. Ao executar no Windows Server 2003, você pode criar uma classe que implementa a interface [**IProcessInitializer**](/windows/desktop/api/ComSvcs/nn-comsvcs-iprocessinitializer) . Quando o processo é iniciado, ele chama [**IProcessInitializer:: Startup**](/windows/desktop/api/ComSvcs/nf-comsvcs-iprocessinitializer-startup) e, ao desligar, ele chama [**IProcessInitializer:: Shutdown**](/windows/desktop/api/ComSvcs/nf-comsvcs-iprocessinitializer-shutdown). Isso dá ao seu componente a oportunidade de realizar tarefas necessárias, como inicializar conexões, arquivos e caches.

## <a name="running-com-applications-as-nt-services"></a>Executando aplicativos COM+ como serviços NT

Os desenvolvedores do COM+ agora podem usar a ferramenta administrativa serviços de componentes para configurar e implementar um aplicativo de servidor COM+ como um serviço NT. Isso significa que o servidor poderá ser iniciado automaticamente ou reiniciado se seu aplicativo sempre precisar ser executado; que seu aplicativo COM+ possa ser executado como a conta do sistema local se precisar executar operações privilegiadas; e que os serviços dependentes de seu aplicativo agora podem ser iniciados automaticamente. Consulte [aplicativos com+ em execução como aplicativos de serviço](com--applications-running-as-service-applications.md) para obter informações detalhadas.

## <a name="side-by-side-assemblies"></a>Assemblies lado a lado

Os assemblies SxS (lado a lado) permitem que os aplicativos especifiquem qual versão de uma DLL do sistema ou o componente COM clássico usar, como MDAC, MFS, MSVCRT ou MSXML. Por exemplo, se um aplicativo ASP depender da versão 2,0 do MSXML, você poderá garantir que esse aplicativo ainda use a versão 2,0 do MSXML mesmo depois que os Service Packs forem aplicados ao servidor. Ou seja, mesmo quando uma nova versão do MSXML está instalada no computador, a versão 2,0 permanece e é usada pelo seu aplicativo.

Para configurar assemblies SxS, você precisa saber o caminho para a DLL e que o arquivo de manifesto COM+ existe em cada diretório virtual que precisa usar a DLL. O manifesto COM+ é um arquivo XML que tem informações sobre onde uma DLL está instalada. O manifesto é usado para criar um contexto de ativação para o aplicativo. Os contextos de ativação permitem que um aplicativo carregue uma versão de DLL específica, uma instância de objeto COM ou uma versão de janela personalizada. Você pode usar a ferramenta administrativa serviços de componentes ou a Propriedade ApplicationDirectory para inserir o caminho completo do diretório raiz do aplicativo que contém um arquivo de manifesto do assembly SxS válido. Para obter mais informações, consulte [aplicativos isolados e assemblies lado a lado](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal).

## <a name="windows-error-reporting"></a>Relatório de Erros do Windows

O COM+ 1,5 inclui suporte para o componente Relatório de Erros do Windows (WER), disponível a partir do Windows XP. O WER permite que os usuários notifiquem a Microsoft de falhas de aplicativo, falhas de kernel e aplicativos sem resposta. Essas notificações permitem que as equipes de atendimento ao cliente da Microsoft resolvam os problemas técnicos com mais eficiência. Além disso, o componente Relatório de Erros do Windows permite que os desenvolvedores do COM+ recebam informações que podem ser usadas para aprimorar seus aplicativos. Para obter mais informações, consulte [Relatório de erros do Windows](/windows/desktop/wer/windows-error-reporting).

 

 
