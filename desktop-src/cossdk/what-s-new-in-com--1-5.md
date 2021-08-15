---
description: O COM+ versão 1.5 adiciona novos recursos projetados para aumentar a escalabilidade geral, a disponibilidade e a capacidade de gerenciamento de aplicativos COM+ para desenvolvedores e administradores do sistema.
ms.assetid: e7073ba5-6b19-4d94-8cc0-b4e16bb44afd
title: Novidades no COM+ 1.5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af0fd6705775e84f49d3a60afd7d89b7a5412b4a87fd5d04f202fadc77fd850d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118304877"
---
# <a name="whats-new-in-com-15"></a>Novidades no COM+ 1.5

O COM+ versão 1.5 adiciona novos recursos projetados para aumentar a escalabilidade geral, a disponibilidade e a capacidade de gerenciamento de aplicativos COM+ para desenvolvedores e administradores do sistema.

O COM+ 1.5 está disponível a partir do Windows XP e Windows Server 2003. Os novos recursos COM+ 1.5 não estão disponíveis no Windows 2000.

## <a name="application-level-access-checks-enabled-by-default"></a>Application-Level verificações de acesso habilitadas por padrão

Como parte da segurança aprimorada do sistema, as verificações de acesso são habilitadas por padrão ao criar um aplicativo COM+. Nas versões anteriores, as verificações de acesso eram desabilitadas por padrão no nível do aplicativo e habilitadas por padrão no nível do componente. A partir do Windows Server 2003, as verificações de acesso são habilitadas por padrão no nível do aplicativo e desabilitadas por padrão no nível do componente. Consulte Criando um novo [](enabling-access-checks-for-an-application.md)aplicativo [COM+,](creating-a-new-com--application.md)Habilitando verificações de acesso para um aplicativo e Habilitando verificações de acesso no nível do componente para obter mais informações e procedimentos sobre como alterar as configurações padrão. [](enabling-access-checks-at-the-component-level.md)

## <a name="application-pooling"></a>Pooling de Aplicativos

Com a nova propriedade ConcurrentApps do objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) na coleção Aplicativos, o Pool de Aplicativos COM+ adiciona escalabilidade para processos de thread único e integra-se ao novo serviço de Reciclagem de Aplicativos COM+. [](applications.md) Confira [Pool de Aplicativos COM+](com--application-pooling.md) para obter informações detalhadas.

## <a name="application-recycling"></a>Reciclagem de aplicativos

A reciclagem de aplicativos aumenta significativamente a estabilidade geral de seus aplicativos. Como o desempenho da maioria dos aplicativos pode ser degradado ao longo do tempo devido a fatores como vazamentos de memória, dependência de código de terceiros e uso de recursos não pode ser escalado, a reciclagem de aplicativos COM+ fornece uma solução simples para desligar normalmente um processo associado a um aplicativo e reiniciá-lo. Confira [Reciclagem de aplicativos COM+](com--application-recycling.md) para obter informações detalhadas. Consulte também "Configurando a reciclagem de processos" na Ajuda de Administração dos Serviços de Componentes para ver um procedimento passo a passo para configurar a reciclagem de processos.

## <a name="com-partitions"></a>Partições COM+

Nesta versão, o COM+ apresenta suporte para partições COM+, um recurso que permite que várias versões de aplicativos COM+ sejam instaladas e configuradas no mesmo computador. Esse recurso pode economizar o custo e o esforço demorado de usar vários servidores para gerenciar versões diferentes de um aplicativo. Em um único computador, cada partição atua, na verdade, como um servidor virtual. Depois de instalar o aplicativo em cada partição, você cria conjuntos de partições que mapeiam os usuários para os servidores lógicos. Consulte [Partições COM+ para](com--partitions.md) obter informações detalhadas sobre como configurar e gerenciar partições COM+. Consulte também "Administrando partições de aplicativo" na Ajuda de Administração dos Serviços de Componentes para ver os procedimentos passo a passo.

## <a name="com-services-without-components"></a>Serviços COM+ sem componentes

Com o COM+ 1.5, você pode usar os serviços fornecidos pelo COM+ sem a necessidade de criar um componente para conter os métodos que chamam esses serviços. Isso beneficia muito os desenvolvedores que normalmente não usam componentes, mas que querem usar serviços COM+, como transações ou o Rastreador COM+. Usando serviços COM+ sem componentes, os desenvolvedores podem evitar a sobrecarga de criar um componente que é usado para acessar apenas os serviços COM+ de que precisam. Consulte [Serviços COM+ sem componentes](com--services-without-components.md) para obter informações detalhadas.

## <a name="com-soap-service"></a>Serviço SOAP COM+

Com o COM+ 1.5, agora você pode expor um aplicativo COM+ como um serviço Web XML. Você também pode usar de forma transparente um serviço Web XML, seja implantado usando COM+ ou não, como um componente COM. Isso significa que você pode facilmente criar novos serviços Web XML de aplicativos COM+ existentes e incorporar facilmente serviços Web XML em novos aplicativos COM+. Consulte [Serviço SOAP COM+ para](com--soap-service.md) obter informações detalhadas.

## <a name="configurable-isolation-levels"></a>Níveis de isolamento configuráveis

Os desenvolvedores COM+ podem usar a nova propriedade TxIsolationLevel ou a ferramenta administrativa dos Serviços de Componentes para configurar o nível de isolamento de um aplicativo de acordo com a necessidade, ajudando a aumentar a simultatividade, o desempenho e a escalabilidade. Essa flexibilidade permite que aqueles com a quantidade certa de experiência recebam até a última onça de produtividade de seus aplicativos. Consulte [Configurando níveis de isolamento de transação](configuring-transaction-isolation-levels.md) para obter informações detalhadas.

## <a name="creating-private-components"></a>Criando componentes privados

Em cenários em que você tem vários componentes auxiliares em um aplicativo que devem ser chamados somente de outros componentes dentro desse aplicativo, esta versão do COM+ permite que você use uma nova propriedade, IsPrivateComponent, para marcar esses componentes como particulares. (Na versão anterior do COM+, todos os componentes tinham que ser públicos para ter acesso aos serviços COM+, o que significa que esses componentes podem ser ativados de outros aplicativos.) Um componente privado pode ser visto e ativado somente por outros componentes no mesmo aplicativo, dando a você mais controle sobre quais funcionalidades expor. Você precisa apenas documentar e manter os componentes públicos, fazendo uso de componentes privados que não podem ser acessados de fora do aplicativo, mas que ainda podem aproveitar todos os serviços COM+.

## <a name="dtc-security-settings"></a>Segurança do DTC Configurações

Várias novas configurações de segurança foram adicionadas para o DTC (Coordenador de Transações Distribuídas da Microsoft), permitindo que você personalize seus níveis de segurança para gerenciar transações distribuídas. Confira Considerações sobre segurança do DTC sobre essas configurações e como implementá-las.

Para facilitar a autenticação mútua, o DTC é restrito à execução na conta NetworkService. Consulte Gerenciando contas e privilégios para obter informações detalhadas.

Para recuperação com bancos de dados XA, é recomendável que a conta NetworkService tenha as permissões e as funções necessárias para executar essa recuperação. O método exato de fazer isso é específico para cada banco de dados. Consulte Desabilitando transações distribuídas nativas e desabilitando transações TIP e XA para obter mais informações.

Para ajudar a fornecer um sistema mais seguro ao usar transações XA, as plataformas Windows Server 2003 incluem uma nova entrada do Registro para especificar arquivos DLL XA. Ao atualizar para o Windows Server 2003, você pode trabalhar com transações XA como antes criando uma entrada do Registro em **HKEY \_ LOCAL MACHINE SOFTWARE Microsoft \_ \\ \\ \\ MSDTC \\ XADLL**, em que o nome do valor é o nome da DLL (no formato *dllname*.dll) e o valor é o caminho completo do arquivo DLL. Você precisa criar uma entrada para cada arquivo DLL XA em uso. Se o computador que executa o DTC faz parte de um cluster, a entrada do Registro precisa ser feita para cada nó no cluster. Consulte Gerenciando transações XA para obter mais informações.

## <a name="low-memory-activation-gates"></a>Low-Memory portas de ativação

Com esta versão, o COM+ verifica automaticamente a memória antes de criar um servidor ou objeto COM+. Se o percentual de memória virtual disponível para o aplicativo ficar abaixo de um limite fixo, a ativação falhará antes que o objeto seja criado. Ao falhar nessas ativações que normalmente seriam executados, o [serviço COM+ Low-Memory Portas](com--low-memory-activation-gates.md) de Ativação aprimora muito a confiabilidade do sistema.

## <a name="moving-and-copying-com-components"></a>Movendo e copiando componentes COM

Com esta versão, o COM+ permite que você mova e copie seus componentes. Isso significa que você pode configurar uma única implementação física de um componente muitas vezes. Você obtém a reutilização de componentes em um nível binário em vez de no nível do código-fonte, o que resulta em menos código, custos de desenvolvimento menores e tempo de comercialização mais rápido. Consulte [Movendo componentes](moving-components.md) [e copiando componentes](copying-components.md) para obter informações detalhadas.

## <a name="network-access"></a>Acesso de rede

O acesso à rede COM+ está desabilitado por padrão no Windows Server 2003, o que significa que o COM+ pode ser usado somente localmente por padrão. Use o procedimento a seguir para habilitar o acesso COM+ à rede.

**Para habilitar o acesso COM+ de rede**

1.  No menu **Iniciar,** aponte para **Painel de Controle** e selecione **Adicionar ou Remover Programas**.

2.  Clique **em Adicionar/Remover componentes Windows .**

3.  Selecione **Servidor de Aplicativos** e clique em **Detalhes**.

4.  Marque a caixa ao lado de **Habilitar acesso COM+ à** rede e clique em **OK.**

5.  Clique **em Próximo** para concluir o assistente Windows Componentes.

6.  Clique **em Concluir** para fechar o assistente.

O acesso a transações de rede DTC é desabilitado por padrão Windows Server 2003. Nessas plataformas, o DTC pode executar apenas transações locais por padrão. Use o procedimento a seguir para habilitar o acesso DTC de rede.

> [!NOTE]
> Você também pode habilitar o acesso DTC de rede usando a ferramenta administrativa serviços de componentes ou programaticamente por meio da Biblioteca de Administração COM+. Para obter informações de procedimento, consulte "Configurando a segurança do DTC" na Ajuda de Administração dos Serviços de Componentes.

**Para habilitar o acesso DTC de rede**

1.  No menu **Iniciar,** aponte para **Painel de Controle** e selecione **Adicionar ou Remover Programas**.

2.  Clique **em Adicionar/Remover componentes Windows .**

3.  Selecione **Servidor de Aplicativos** e clique em **Detalhes**.

4.  Marque a caixa ao lado de **Habilitar acesso ao DTC de** rede e clique em **OK.**

5.  Clique **em Próximo** para concluir o assistente Windows Componentes.

6.  Clique **em Concluir** para fechar o assistente.

## <a name="pausing-and-disabling-applications"></a>Pausando e desabilitando aplicativos

Os aplicativos COM+ agora são mais gerenciáveis. Um administrador pode pausar e retomar aplicativos de servidor COM+, desabilitar e habilitar aplicativos de servidor ou biblioteca COM+, ou até mesmo componentes configurados individuais. Os recursos de pausa e desabilitação impedem futuras ativações sem afetar as instâncias de componente existentes. Consulte "Administrando aplicativos COM+ " na Ajuda de Administração dos Serviços de Componentes para obter mais informações.

## <a name="process-dumping"></a>Processo de despejo

Não é fácil solucionar problemas de aplicativos em um ambiente de produção. Como você coleta informações sobre um problema sem atrapalhar os processos em execução? O COM+ agora fornece uma solução por meio de seu novo recurso de despejo de processo. Esse recurso permite que o administrador do sistema despeja todo o estado de um processo sem finalização. Consulte "Administrando a Ferramenta de Despejo de Processo para depurar aplicativos COM+ " na Ajuda de Administração de Serviços de Componentes para obter mais informações.

## <a name="process-initialization"></a>Inicialização do processo

Muitos aplicativos de servidor precisam fazer inicialização e limpeza específicas quando são iniciados e desligados. ao executar o Windows Server 2003, você pode criar uma classe que implementa a interface [**IProcessInitializer**](/windows/desktop/api/ComSvcs/nn-comsvcs-iprocessinitializer) . Quando o processo é iniciado, ele chama [**IProcessInitializer:: Startup**](/windows/desktop/api/ComSvcs/nf-comsvcs-iprocessinitializer-startup) e, ao desligar, ele chama [**IProcessInitializer:: Shutdown**](/windows/desktop/api/ComSvcs/nf-comsvcs-iprocessinitializer-shutdown). Isso dá ao seu componente a oportunidade de realizar tarefas necessárias, como inicializar conexões, arquivos e caches.

## <a name="running-com-applications-as-nt-services"></a>Executando aplicativos COM+ como serviços NT

Os desenvolvedores do COM+ agora podem usar a ferramenta administrativa serviços de componentes para configurar e implementar um aplicativo de servidor COM+ como um serviço NT. Isso significa que o servidor poderá ser iniciado automaticamente ou reiniciado se seu aplicativo sempre precisar ser executado; que seu aplicativo COM+ possa ser executado como a conta do sistema local se precisar executar operações privilegiadas; e que os serviços dependentes de seu aplicativo agora podem ser iniciados automaticamente. Consulte [aplicativos com+ em execução como aplicativos de serviço](com--applications-running-as-service-applications.md) para obter informações detalhadas.

## <a name="side-by-side-assemblies"></a>Assemblies lado a lado

Assemblies SxS (lado a lado) permitem que os aplicativos especifiquem qual versão de uma DLL de sistema ou componente COM clássico usar, como MDAC, MFS, MSVCRT ou MSXML. por exemplo, se um aplicativo ASP depender de MSXML versão 2,0, você poderá garantir que esse aplicativo ainda use MSXML versão 2,0 mesmo depois que os service packs forem aplicados ao servidor. ou seja, mesmo quando uma nova versão do MSXML está instalada no computador, a versão 2,0 permanece e é usada pelo seu aplicativo.

Para configurar assemblies SxS, você precisa saber o caminho para a DLL e que o arquivo de manifesto COM+ existe em cada diretório virtual que precisa usar a DLL. O manifesto COM+ é um arquivo XML que tem informações sobre onde uma DLL está instalada. O manifesto é usado para criar um contexto de ativação para o aplicativo. Os contextos de ativação permitem que um aplicativo carregue uma versão de DLL específica, uma instância de objeto COM ou uma versão de janela personalizada. Você pode usar a ferramenta administrativa serviços de componentes ou a Propriedade ApplicationDirectory para inserir o caminho completo do diretório raiz do aplicativo que contém um arquivo de manifesto do assembly SxS válido. Para obter mais informações, consulte [aplicativos isolados e assemblies lado a lado](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal).

## <a name="windows-error-reporting"></a>Relatório de Erros do Windows

o COM+ 1,5 inclui suporte para o componente Relatório de Erros do Windows (WER), disponível a partir do Windows XP. O WER permite que os usuários notifiquem a Microsoft de falhas de aplicativo, falhas de kernel e aplicativos sem resposta. Essas notificações permitem que as equipes de atendimento ao cliente da Microsoft resolvam os problemas técnicos com mais eficiência. além disso, o componente Relatório de Erros do Windows permite que os desenvolvedores do COM+ recebam informações que podem ser usadas para aprimorar seus aplicativos. Para obter mais informações, consulte [Relatório de erros do Windows](/windows/desktop/wer/windows-error-reporting).

 

 
