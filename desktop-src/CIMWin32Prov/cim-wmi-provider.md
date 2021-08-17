---
description: Essas classes WMI são declaradas em CimWin32. mof.
ms.assetid: 53122499-1CC0-4B48-AEA1-B70B7BBC3A99
ms.tgt_platform: multiple
title: Provedor WMI CIM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acb9a01e0771645cf6101171ce870be593181cb61d6118e627b9bf96b61994be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118420327"
---
# <a name="cim-wmi-provider"></a>Provedor WMI CIM

Essas classes WMI são declaradas em CimWin32. mof.

## <a name="in-this-section"></a>Nesta seção

<dl> <dt>

[**Ação de CIM \_**](cim-action.md)
</dt> <dd>

Uma classe de [**\_ ação CIM**](cim-action.md) é uma operação que faz parte de um processo para criar um elemento de software em seu estado seguinte ou para eliminar o elemento de software no estado atual.

</dd> <dt>

[**\_ACTIONSEQUENCE CIM**](cim-actionsequence.md)
</dt> <dd>

A associação [**CIM \_ ActionSequence**](cim-actionsequence.md) define uma série de operações que fazem a transição do elemento software (referenciado pela Associação [**\_ SoftwareElementActions do CIM**](cim-softwareelementactions.md) ) para seu próximo estado ou remove o elemento software de seu estado atual.

</dd> <dt>

[**\_ACTSASSPARE CIM**](cim-actsasspare.md)
</dt> <dd>

A associação [**CIM \_ ActsAsSpare**](cim-actsasspare.md) indica quais elementos podem ser sobressalentes ou substituir outros elementos agregados. Um sobressalente pode operar no modo "hot-standby", conforme especificado de acordo com o elemento.

</dd> <dt>

[**\_ADJACENTSLOTS CIM**](cim-adjacentslots.md)
</dt> <dd>

A associação [**CIM \_ AdjacentSlots**](cim-adjacentslots.md) descreve o layout dos slots em uma placa de adaptador ou placa de hospedagem. Informações, como a distância entre os slots e se elas são "compartilhadas" (se uma for populada, o outro slot não poderá ser usado), será transmitido como propriedades de associação.

</dd> <dt>

[**\_AGGREGATEPEXTENT CIM**](cim-aggregatepextent.md)
</dt> <dd>

A classe [**CIM \_ AggregatePExtent**](cim-aggregatepextent.md) fornece informações resumidas sobre blocos lógicos endereçáveis, que estão no mesmo grupo de redundância de armazenamento e localizados na mesma mídia física.

</dd> <dt>

[**\_AGGREGATEPSEXTENT CIM**](cim-aggregatepsextent.md)
</dt> <dd>

A classe [**CIM \_ AggregatePSExtent**](cim-aggregatepsextent.md) define o número de blocos lógicos endereçáveis em um único dispositivo de armazenamento, excluindo blocos lógicos mapeados como dados de verificação. Se os conjuntos de volumes forem definidos, os blocos lógicos estarão contidos em um único conjunto de volumes. Esse é um agrupamento alternativo para [**\_ ProtectedSpaceExtent CIM**](cim-protectedspaceextent.md), quando apenas informações resumidas são necessárias ou quando a configuração automática é usada.

</dd> <dt>

[**\_AGGREGATEREDUNDANCYCOMPONENT CIM**](cim-aggregateredundancycomponent.md)
</dt> <dd>

A classe [**CIM \_ AggregateRedundancyComponent**](cim-aggregateredundancycomponent.md) descreve a extensão física agregada em um grupo de redundância de armazenamento.

</dd> <dt>

[**\_ALARMDEVICE CIM**](cim-alarmdevice.md)
</dt> <dd>

A classe [**CIM \_ AlarmDevice**](cim-alarmdevice.md) é um dispositivo de alarme que emite indicações audíveis ou visíveis relacionadas a uma situação de problema.

</dd> <dt>

[**\_ALLOCATEDRESOURCE CIM**](cim-allocatedresource.md)
</dt> <dd>

A classe [**CIM \_ AllocatedResource**](cim-allocatedresource.md) representa uma associação entre dispositivos lógicos e recursos do sistema e indica que o recurso está atribuído ao dispositivo.

</dd> <dt>

[**\_APPLICATIONSYSTEM CIM**](cim-applicationsystem.md)
</dt> <dd>

A classe [**CIM \_ ApplicationSystem**](cim-applicationsystem.md) representa um sistema de aplicativo ou de software que dá suporte a uma função comercial específica que pode ser gerenciada como uma unidade independente. Esse sistema pode ser decomposto em seus componentes funcionais usando a classe [**CIM \_ SoftwareFeature**](cim-softwarefeature.md) . Os recursos de software para um determinado aplicativo ou sistema de software estão localizados usando a associação [**CIM \_ ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md) .

</dd> <dt>

[**\_APPLICATIONSYSTEMSOFTWAREFEATURE CIM**](cim-applicationsystemsoftwarefeature.md)
</dt> <dd>

A classe [**CIM \_ ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md) representa uma associação que identifica os recursos de software que compõem um sistema de aplicativos específico. Os recursos de software podem ser incluídos em produtos diferentes.

</dd> <dt>

[**\_ASSOCIATEDALARM CIM**](cim-associatedalarm.md)
</dt> <dd>

A dependência do [**CIM \_ AssociatedAlarm**](cim-associatedalarm.md) associa um alarme a um dispositivo lógico.

</dd> <dt>

[**\_ASSOCIATEDBATTERY CIM**](cim-associatedbattery.md)
</dt> <dd>

A dependência do [**CIM \_ AssociatedBattery**](cim-associatedbattery.md) associa uma bateria a um dispositivo lógico. Use essa associação para modelar baterias individuais que compõem uma fonte de alimentação ininterrupta (UPS).

</dd> <dt>

[**\_ASSOCIATEDCOOLING CIM**](cim-associatedcooling.md)
</dt> <dd>

A associação [**CIM \_ AssociatedCooling**](cim-associatedcooling.md) indica quando ventiladores ou outros dispositivos de resfriamento são específicos para um dispositivo (em vez de fornecer resfriamento de compartimento ou de gabinete).

</dd> <dt>

[**\_ASSOCIATEDMEMORY CIM**](cim-associatedmemory.md)
</dt> <dd>

A classe [**CIM \_ AssociateMemory**](cim-associatedmemory.md) associa a memória instalada ou associada, como memória de cache com um dispositivo lógico.

</dd> <dt>

[**\_ASSOCIATEDPROCESSORMEMORY CIM**](cim-associatedprocessormemory.md)
</dt> <dd>

A classe [**CIM \_ AssociatedProcessorMemory**](cim-associatedprocessormemory.md) associa o processador e a memória do sistema ou o cache de um processador.

</dd> <dt>

[**\_ASSOCIATEDSENSOR CIM**](cim-associatedsensor.md)
</dt> <dd>

A classe [**CIM \_ AssociatedSensor**](cim-associatedsensor.md) associa um sensor instalado a um dispositivo lógico. O sensor mede as propriedades de entrada e saída críticas e pode ser incluído no dispositivo ou instalado no próximo.

</dd> <dt>

[**\_ASSOCIATEDSUPPLYCURRENTSENSOR CIM**](cim-associatedsupplycurrentsensor.md)
</dt> <dd>

A classe [**CIM \_ AssociatedSupplyCurrentSensor**](cim-associatedsupplycurrentsensor.md) associa uma fonte de energia a um sensor atual (amperagem) que monitora sua frequência de entrada.

</dd> <dt>

[**\_ASSOCIATEDSUPPLYVOLTAGESENSOR CIM**](cim-associatedsupplyvoltagesensor.md)
</dt> <dd>

Associa uma fonte de energia a um sensor de tensão que monitora sua tensão de entrada.

</dd> <dt>

[**\_Baseado em CIM**](cim-basedon.md)
</dt> <dd>

A [**classe \_ com base em CIM**](cim-basedon.md) representa uma associação que descreve como as extensões de armazenamento podem ser montadas de extensões de nível inferior. Por exemplo, as extensões físicas incluem extensões de espaço protegido. Portanto, os conjuntos de volumes são montados de uma ou mais extensões de espaço físico ou protegido. A memória de cache pode ser definida de forma independente e realizada em um elemento físico, ou pode ser baseada em extensões de armazenamento voláteis ou não voláteis.

</dd> <dt>

[**\_Bateria CIM**](cim-battery.md)
</dt> <dd>

A classe de [**\_ bateria CIM**](cim-battery.md) representa os recursos e o gerenciamento do dispositivo lógico da bateria. Essa classe se aplica a baterias em sistemas de laptop e outras baterias internas e externas.

</dd> <dt>

[**\_BINARYSENSOR CIM**](cim-binarysensor.md)
</dt> <dd>

A classe [**CIM \_ BinarySensor**](cim-binarysensor.md) fornece uma saída booliana. As propriedades **CurrentState** e **PossibleStates** foram adicionadas para o sensor, tornando a **subclasse \_ BinarySensor CIM** não mais necessária, embora seja mantida para compatibilidade com versões anteriores. Um sensor binário pode ser criado instanciando-se um sensor com dois Estados possíveis.

</dd> <dt>

[**CIM \_ bioselement**](cim-bioselement.md)
</dt> <dd>

A classe [**CIM \_ bioselement**](cim-bioselement.md) representa o software de nível baixo que é carregado no armazenamento não volátil e usado para iniciar e configurar um sistema de computador.

</dd> <dt>

[**\_BIOSFEATURE CIM**](cim-biosfeature.md)
</dt> <dd>

representa os recursos do software de nível baixo que é usado para iniciar e configurar um sistema de computador.

</dd> <dt>

[**\_BIOSFEATUREBIOSELEMENTS CIM**](cim-biosfeaturebioselements.md)
</dt> <dd>

A classe [**CIM \_ BIOSFeatureBIOSElements**](cim-biosfeaturebioselements.md) associa um recurso do BIOS e seus elementos do BIOS agregados.

</dd> <dt>

[**\_BIOSLOADEDINNV CIM**](cim-biosloadedinnv.md)
</dt> <dd>

A classe [**CIM \_ BIOSLoadedInNV**](cim-biosloadedinnv.md) associa um elemento BIOS e o armazenamento não volátil no qual ele é carregado.

</dd> <dt>

[**\_BOOTOSFROMFS CIM**](cim-bootosfromfs.md)
</dt> <dd>

A classe [**CIM \_ BootOSFromFS**](cim-bootosfromfs.md) associa o sistema operacional e os sistemas de arquivos dos quais o sistema operacional é carregado. A associação é muitos-para-muitos; um sistema operacional distribuído pode depender de vários sistemas de arquivos para serem carregados de forma correta e completa.

</dd> <dt>

[**\_BOOTSAP CIM**](cim-bootsap.md)
</dt> <dd>

A classe [**CIM \_ BootSAP**](cim-bootsap.md) representa os pontos de acesso de um serviço de inicialização.

</dd> <dt>

[**\_DS CIM**](cim-bootservice.md)
</dt> <dd>

A classe [**CIM \_ DS**](cim-bootservice.md) representa a funcionalidade fornecida por um dispositivo ou software, ou por uma rede, para carregar um sistema operacional em um sistema de computador unitário.

</dd> <dt>

[**\_BOOTSERVICEACCESSBYSAP CIM**](cim-bootserviceaccessbysap.md)
</dt> <dd>

A classe [**CIM \_ BootServiceAccessBySAP**](cim-bootserviceaccessbysap.md) associa um serviço de inicialização e seus pontos de acesso.

</dd> <dt>

[**\_CACHEMEMORY CIM**](cim-cachememory.md)
</dt> <dd>

A classe [**CIM \_ CacheMemory**](cim-cachememory.md) define os recursos e o gerenciamento da memória cache.

</dd> <dt>

[**\_Placa CIM**](cim-card.md)
</dt> <dd>

A classe de [**\_ placa CIM**](cim-card.md) representa um tipo de contêiner físico que pode ser conectado a outro cartão ou placa de hospedagem, ou é uma placa de hospedagem/placa-mãe em um chassi. Essa classe inclui qualquer pacote que seja capaz de carregar sinais e fornecer um ponto de montagem para componentes físicos, como chips ou outros pacotes físicos, como outros cartões.

</dd> <dt>

[**\_CARDINSLOT CIM**](cim-cardinslot.md)
</dt> <dd>

A classe [**CIM \_ CardInSlot**](cim-cardinslot.md) associa uma placa de adaptador ao contêiner no qual ela é inserida.

</dd> <dt>

[**\_CARDONCARD CIM**](cim-cardoncard.md)
</dt> <dd>

A associação [**CIM \_ CardOnCard**](cim-cardoncard.md) descreve as relações sobre os cartões que podem ser conectados a placas-mãe/placas, daughtercards de um adaptador ou cartões que dão suporte a módulos especiais semelhantes a cartões.

</dd> <dt>

[**\_CDROMDRIVE CIM**](cim-cdromdrive.md)
</dt> <dd>

A classe [**CIM \_ CDROMDrive**](cim-cdromdrive.md) representa uma unidade de CD-ROM no computador.

</dd> <dt>

[**\_Chassi CIM**](cim-chassis.md)
</dt> <dd>

A classe de [**\_ chassi CIM**](cim-chassis.md) representa os elementos físicos que incluem outros elementos e fornece funcionalidade definíveis, como um desktop, nó de processamento, UPS, armazenamento em disco ou fita ou uma combinação desses.

</dd> <dt>

[**\_CHASSISINRACK CIM**](cim-chassisinrack.md)
</dt> <dd>

A associação de [**\_ ChassisInRack do CIM**](cim-chassisinrack.md) representa a relação de "contenção" entre um rack e um chassi que ele contém.

</dd> <dt>

[**Verificação de CIM \_**](cim-check.md)
</dt> <dd>

A classe de [**\_ verificação CIM**](cim-check.md) representa uma condição ou característica que deve ser verdadeira em um ambiente definido ou com escopo por uma instância de uma classe [**de \_ sistema CIM**](cim-computersystem.md) . As verificações associadas a um determinado elemento de software são organizadas em um dos dois grupos usando a propriedade **Phase** da Associação [**\_ SoftwareElementChecks do CIM**](cim-softwareelementchecks.md) .

</dd> <dt>

[**\_Chip CIM**](cim-chip.md)
</dt> <dd>

A [**classe \_ CIM Chip**](cim-chip.md) representa o tipo de hardware de circuito integrado, incluindo ASICs, processadores, chips de memória e assim por diante.

</dd> <dt>

[**\_Clusterings CIMSAP**](cim-clusteringsap.md)
</dt> <dd>

A [**classe CIM \_ ClusteringSAP**](cim-clusteringsap.md) representa os pontos de acesso de um serviço de clustering.

</dd> <dt>

[**CIM \_ ClusteringService**](cim-clusteringservice.md)
</dt> <dd>

A [**classe CIM \_ ClusteringService**](cim-clusteringservice.md) representa a funcionalidade fornecida por um cluster. Por exemplo, a funcionalidade de failover pode ser modelada como um serviço de um cluster de failover.

</dd> <dt>

[**Cluster \_ CIMServiceAccessBySAP**](cim-clusterserviceaccessbysap.md)
</dt> <dd>

A [**classe CIM \_ ClusterServiceAccessBySAP**](cim-clusterserviceaccessbysap.md) representa a relação entre um serviço de clustering e seus pontos de acesso.

</dd> <dt>

[**CIM \_ CollectedCollections**](cim-collectedcollections.md)
</dt> <dd>

A [**classe CIM \_ CollectedCollections**](cim-collectedcollections.md) é uma associação de agregação que representa uma coleção de MSE (Managed System Elements) contida em uma coleção de MSEs.

</dd> <dt>

[**CIM \_ CollectedMSEs**](cim-collectedmses.md)
</dt> <dd>

A [**classe de associação CIM \_ CollectedMSEs**](cim-collectedmses.md) representa os membros do objeto de agrupação, [**uma classe CollectionOfMSEs.**](cim-collectionofmses.md)

</dd> <dt>

[**Coleção \_ CIMOfMSEs**](cim-collectionofmses.md)
</dt> <dd>

O [**objeto \_ Cim CollectionOfMSEs**](cim-collectionofmses.md) permite o agrupamento de objetos [**Cim \_ ManagedSystemElement**](cim-managedsystemelement.md) com a finalidade de associar configurações e configurações. É abstrato exigir definição e refinamento semânticos em subclasses.

</dd> <dt>

[**Coleção \_ CIMOfSensors**](cim-collectionofsensors.md)
</dt> <dd>

A [**associação \_ Cim CollectionOfSensors**](cim-collectionofsensors.md) representa os sensores binários que comem o sensor de vários estados.

</dd> <dt>

[**Coleção \_ CIMConjunto**](cim-collectionsetting.md)
</dt> <dd>

A [**classe \_ CollectionSetting cim**](cim-collectionsetting.md) representa a associação entre uma Coleção [**\_ CIMOfMSEs**](cim-collectionofmses.md) e a classe de configuração definida para eles.

</dd> <dt>

[**CIM \_ CompatibleProduct**](cim-compatibleproduct.md)
</dt> <dd>

A [**classe CIM \_ CompatibleProduct**](cim-compatibleproduct.md) representa uma associação entre produtos que indica se dois produtos referenciados são interoperáveis, como se eles podem ser instalados juntos ou se um pode ser o contêiner físico para o outro e assim por diante.

</dd> <dt>

[**Componente \_ CIM**](cim-component.md)
</dt> <dd>

A [**associação do \_ componente CIM**](cim-component.md) representa as partes de uma relação entre MSEs.

</dd> <dt>

[**CIM \_ ComputerSystem**](cim-computersystem.md)
</dt> <dd>

Uma [**classe \_ COMPUTERSystem cim**](cim-computersystem.md) representa uma coleção especial de [**instâncias de \_ ManagedSystemElement**](cim-managedsystemelement.md) cim. Essa coleção fornece recursos de computador e serve como um ponto de agregação para associar um ou mais dos seguintes elementos: sistema de arquivos, sistema operacional, processador e memória (armazenamento volátil e não volátil). Essa classe é derivada do [**sistema CIM. \_**](cim-system.md)

</dd> <dt>

[**CIM \_ ComputerSystemDMA**](cim-computersystemdma.md)
</dt> <dd>

A [**classe CIM \_ ComputerSystemDMA**](cim-computersystemdma.md) representa uma associação entre um sistema de computador e seus canais de DMA (acesso direto à memória) disponíveis.

</dd> <dt>

[**CIM \_ ComputerSystemIRQ**](cim-computersystemirq.md)
</dt> <dd>

A [**classe CIM \_ ComputerSystemIRQ**](cim-computersystemirq.md) representa uma associação entre um sistema de computador e suas IRQs (linhas de solicitação de interrupção) disponíveis.

</dd> <dt>

[**CIM \_ ComputerSystemMappedIO**](cim-computersystemmappedio.md)
</dt> <dd>

A [**classe CIM \_ ComputerSystemMappedIO representa**](cim-computersystemmappedio.md) uma associação entre um sistema de computador e suas portas de E/S mapeadas em memória disponíveis.

</dd> <dt>

[**CIM \_ ComputerSystemPackage**](cim-computersystempackage.md)
</dt> <dd>

A [**classe CIM \_ ComputerSystemPackage**](cim-computersystempackage.md) representa uma associação que define explicitamente a relação entre sistemas de computador unitários e um ou mais pacotes físicos. A associação é semelhante à maneira como os dispositivos lógicos são realizados por elementos físicos.

</dd> <dt>

[**CIM \_ ComputerSystemResource**](cim-computersystemresource.md)
</dt> <dd>

A [**classe CIM \_ ComputerSystemResource**](cim-computersystemresource.md) representa uma associação entre um sistema de computador e seus recursos do sistema disponíveis.

</dd> <dt>

[**Configuração cim \_**](cim-configuration.md)
</dt> <dd>

O [**objeto \_ Configuração cim**](cim-configuration.md) permite o agrupamento de conjuntos de parâmetros (definidos em objetos de Configuração [**cim) \_**](cim-setting.md) e dependências para um ou mais elementos do sistema gerenciado.

</dd> <dt>

[**CIM \_ ConnectedTo**](cim-connectedto.md)
</dt> <dd>

A [**classe CIM \_ ConnectedTo**](cim-connectedto.md) representa uma associação que indica que dois ou mais conectores físicos estão conectados.

</dd> <dt>

[**CIM \_ ConnectorOnPackage**](cim-connectoronpackage.md)
</dt> <dd>

A [**classe CIM \_ ConnectorOnPackage**](cim-connectoronpackage.md) representa uma associação que torna explícita a relação de contenção entre conectores e pacotes. Os pacotes físicos contêm conectores, bem como outros elementos físicos.

</dd> <dt>

[**Contêiner \_ CIM**](cim-container.md)
</dt> <dd>

A [**classe \_ contêiner CIM**](cim-container.md) representa uma associação entre um elemento físico contido e um que contém. Um objeto que contém deve ser um pacote físico.

</dd> <dt>

[**CIM \_ ControlledBy**](cim-controlledby.md)
</dt> <dd>

A [**relação CIM \_ ControlledBy**](cim-controlledby.md) indica quais dispositivos são comandos ou acessados por meio do dispositivo lógico do controlador.

</dd> <dt>

[**Controlador \_ CIM**](cim-controller.md)
</dt> <dd>

A [**classe \_ controlador CIM**](cim-controller.md) é uma classe pai para agrupar diversos dispositivos relacionados ao controle. Exemplos de controladores são controladores SCSI, controladores USB e controladores seriais.

</dd> <dt>

[**CIM \_ CoolingDevice**](cim-coolingdevice.md)
</dt> <dd>

A [**classe CIM \_ CoolingDevice**](cim-coolingdevice.md) representa os recursos e o gerenciamento de dispositivos de resfriamento.

</dd> <dt>

[**CopyFileAction do CIM \_**](cim-copyfileaction.md)
</dt> <dd>

A [**classe \_ CopyFileAction cim**](cim-copyfileaction.md) representa a movimentação ou cópia de arquivos de um sistema de computador para um novo local.

</dd> <dt>

[**CIM \_ CreateDirectoryAction**](cim-createdirectoryaction.md)
</dt> <dd>

A [**classe CIM \_ CreateDirectoryAction**](cim-createdirectoryaction.md) cria diretórios vazios para que os elementos de software sejam instalados localmente.

</dd> <dt>

[**CIM \_ CurrentSensor**](cim-currentsensor.md)
</dt> <dd>

A [**classe \_ CurrentSensor cim**](cim-currentsensor.md) existe para compatibilidade com versões anteriores para definições de esquema CIM anteriores.

</dd> <dt>

[**CIM \_ DataFile**](cim-datafile.md)
</dt> <dd>

A [**classe CIM \_ DataFile**](cim-datafile.md) representa uma coleção nomeada de dados ou código executável. Somente instâncias de arquivos em discos fixos locais serão retornadas

</dd> <dt>

[**Dependência cim \_**](cim-dependency.md)
</dt> <dd>

A [**classe De \_ dependência CIM**](cim-dependency.md) representa uma associação que estabelece relações de dependência entre objetos.

</dd> <dt>

[**\_DependencyContext do CIM**](cim-dependencycontext.md)
</dt> <dd>

A [**relação \_ DependencyContext**](cim-dependencycontext.md) cim associa uma classe [**de \_ Dependência CIM**](cim-dependency.md) a um ou mais objetos de [**\_ Configuração cim.**](cim-configuration.md) Por exemplo, as dependências de um sistema de computador podem mudar com base na rede à qual o sistema está anexado.

</dd> <dt>

[**CIM \_ DesktopMonitor**](cim-desktopmonitor.md)
</dt> <dd>

A [**classe Cim \_ DesktopMonitor**](cim-desktopmonitor.md) representa os recursos e o gerenciamento do dispositivo lógico do CRT (monitor da área de trabalho).

</dd> <dt>

[**CIM \_ DeviceAccessedByFile**](cim-deviceaccessedbyfile.md)
</dt> <dd>

A [**classe de associação \_ DeviceAccessedByFile cim**](cim-deviceaccessedbyfile.md) especifica o dispositivo lógico acessado usando a classe [**DeviceFile CIM \_ referenciada.**](cim-devicefile.md)

</dd> <dt>

[**CIM \_ DeviceConnection**](cim-deviceconnection.md)
</dt> <dd>

A [**classe de associação \_ DeviceConnection cim**](cim-deviceconnection.md) representa dois ou mais dispositivos conectados.

</dd> <dt>

[**CIM \_ DeviceErrorCounts**](cim-deviceerrorcounts.md)
</dt> <dd>

A [**classe CIM \_ DeviceErrorCounts**](cim-deviceerrorcounts.md) é uma classe estatística que contém contadores relacionados a erros para um dispositivo lógico. Os tipos de erros são definidos por CCITT (Rec X.733) e ISO (IEC 10164-4).

</dd> <dt>

[**CIM \_ DeviceFile**](cim-devicefile.md)
</dt> <dd>

A [**classe \_ DeviceFile CIM**](cim-devicefile.md) representa um tipo de arquivo lógico, que representa um dispositivo. Essa convenção é útil para sistemas operacionais que gerenciam dispositivos usando um modelo de E/S de fluxo de byte. O dispositivo lógico associado a esse arquivo é especificado usando a relação [**\_ DeviceAccessedByFile cim.**](cim-deviceaccessedbyfile.md)

</dd> <dt>

[**CIM \_ DeviceSAPImplementation**](cim-devicesapimplementation.md)
</dt> <dd>

A [**classe CIM \_ DeviceSAPImplementation**](cim-devicesapimplementation.md) representa uma associação entre um SAP (ponto de acesso de serviço) e como ele é implementado. Quando muitos dispositivos lógicos estão associados a um SAP, os elementos operam em conjunto para fornecer o ponto de acesso. Se existirem implementações diferentes de um SAP, cada implementação resulta em instações individuais do objeto SAP.

</dd> <dt>

[**CIM \_ DeviceServiceImplementation**](cim-deviceserviceimplementation.md)
</dt> <dd>

A [**classe \_ DEVICEServiceImplementation cim**](cim-deviceserviceimplementation.md) representa uma associação entre um serviço e como ele é implementado. Quando vários dispositivos estão associados a um serviço, os elementos operam em conjunto para fornecer o serviço. Se existirem implementações diferentes de um serviço, cada implementação resulta em instações individuais do objeto de serviço.

</dd> <dt>

[**CIM \_ DeviceSoftware**](cim-devicesoftware.md)
</dt> <dd>

A [**relação CIM \_ DeviceSoftware**](cim-devicesoftware.md) identifica o software associado a um dispositivo, como drivers, configuração, software de aplicativo ou firmware.

</dd> <dt>

[**Diretório \_ CIM**](cim-directory.md)
</dt> <dd>

A [**classe \_ Cim Directory**](cim-directory.md) representa um tipo de arquivo que agrupa logicamente os arquivos de dados que ela contém e fornece informações de caminho para os arquivos agrupados.

</dd> <dt>

[**CIM \_ DirectoryAction**](cim-directoryaction.md)
</dt> <dd>

A [**classe \_ abstrata CIM DirectoryAction**](cim-directoryaction.md) gerencia diretórios. A criação de diretório é manipulada pela classe [**CIM \_ CreateDirectoryAction**](cim-createdirectoryaction.md) e a remoção de diretório é manipulada pela [**classe CIM \_ RemoveDirectoryAction.**](cim-removedirectoryaction.md)

</dd> <dt>

[**Diretório \_ CIMContainsFile**](cim-directorycontainsfile.md)
</dt> <dd>

A [**classe CIM \_ DirectoryContainsFile**](cim-directorycontainsfile.md) representa uma associação entre um diretório e arquivos contidos nesse diretório.

</dd> <dt>

[**CIM \_ DirectorySpecification**](cim-directoryspecification.md)
</dt> <dd>

A classe [**CIM \_ DirectorySpecification**](cim-directoryspecification.md) captura a estrutura de diretório principal de um elemento de software. Essa classe é usada para organizar os arquivos de um elemento de software em unidades gerenciáveis que podem ser realocadas em um sistema de computador.

</dd> <dt>

[**\_DIRECTORYSPECIFICATIONFILE CIM**](cim-directoryspecificationfile.md)
</dt> <dd>

A associação [**CIM \_ DirectorySpecificationFile**](cim-directoryspecificationfile.md) representa o diretório que contém o arquivo especificado referenciando a classe [**CIM \_ DirectorySpecification**](cim-directoryspecification.md) .

</dd> <dt>

[**\_DISCRETESENSOR CIM**](cim-discretesensor.md)
</dt> <dd>

A classe [**CIM \_ DiscreteSensor**](cim-discretesensor.md) tem um conjunto de valores de cadeia de caracteres legais que ele pode relatar. Os valores são enumerados na propriedade **PossibleValues** do sensor. Um sensor discreto sempre tem uma leitura atual que corresponde a um dos valores enumerados.

</dd> <dt>

[**\_DISKDRIVE CIM**](cim-diskdrive.md)
</dt> <dd>

A classe [**CIM \_ DiskDrive**](cim-diskdrive.md) representa uma unidade de disco físico, como visto pelo sistema operacional. Os recursos da unidade de disco correspondem às características lógica e de gerenciamento da unidade e, em alguns casos, podem não refletir as características físicas do dispositivo. Uma interface para uma unidade física é um membro dessa classe. No entanto, um objeto baseado em outro dispositivo lógico não é membro dessa classe.

</dd> <dt>

[**\_DISKETTEDRIVE CIM**](cim-diskettedrive.md)
</dt> <dd>

A classe [**CIM \_ DisketteDrive**](cim-diskettedrive.md) representa os recursos e o gerenciamento de uma unidade de disquete.

</dd> <dt>

[**\_DISKPARTITION CIM**](cim-diskpartition.md)
</dt> <dd>

A classe [**CIM \_ DiskPartition**](cim-diskpartition.md) representa um intervalo contíguo de blocos lógicos que é identificável pelo sistema operacional por meio dos campos tipo e subtipo da partição. As partições de disco devem ser realizadas diretamente pela mídia física (indicada pela Associação de [**\_ RealizesDiskPartition do CIM**](cim-realizesdiskpartition.md) ) ou criados em volumes de armazenamento.

</dd> <dt>

[**\_DISKSPACECHECK CIM**](cim-diskspacecheck.md)
</dt> <dd>

A classe [**CIM \_ DiskSpaceCheck**](cim-diskspacecheck.md) verifica a quantidade de espaço em disco disponível do sistema e especifica-o na propriedade **AvailableDiskSpace** . Os detalhes são comparados com o valor na propriedade **AvailableSpace** do objeto de [**sistema de \_ arquivos CIM**](cim-filesystem.md) que está associado ao objeto [**CIM \_ ComputerSystem**](cim-computersystem.md) , que descreve o ambiente do sistema. Quando o valor da propriedade **AvailableSpace** for maior ou igual ao valor especificado na propriedade **AvailableDiskSpace** , a condição será satisfeita.

</dd> <dt>

[**Exibição de CIM \_**](cim-display.md)
</dt> <dd>

A classe de [**\_ vídeo CIM**](cim-display.md) é uma classe pai para agrupar dispositivos de vídeo diversos.

</dd> <dt>

[**DMA de CIM \_**](cim-dma.md)
</dt> <dd>

A classe [**CIM \_ DMA**](cim-dma.md) representa o DMA (acesso direto à memória) da arquitetura do computador.

</dd> <dt>

[**CIM \_ encaixado**](cim-docked.md)
</dt> <dd>

A associação de [**\_ encaixe CIM**](cim-docked.md) representa a relação entre dois chassis. Por exemplo, um laptop (um tipo de chassi) pode ser encaixado em uma estação de encaixe (outro tipo de chassi). Essa relação típica é descrita explicitamente.

</dd> <dt>

[**\_ELEMENTCAPACITY CIM**](cim-elementcapacity.md)
</dt> <dd>

A classe [**CIM \_ ElementCapacity**](cim-elementcapacity.md) associa um objeto [**CIM \_ PhysicalCapacity**](cim-physicalcapacity.md) a um ou mais elementos físicos. Ele associa uma descrição dos requisitos mínimos e máximos de hardware (ou recursos) aos elementos físicos descritos.

</dd> <dt>

[**\_ELEMENTCONFIGURATION CIM**](cim-elementconfiguration.md)
</dt> <dd>

A associação [**CIM \_ ElementConfiguration**](cim-elementconfiguration.md) relaciona um objeto de [**\_ configuração CIM**](cim-configuration.md) a um ou mais elementos do sistema gerenciado. O objeto de **\_ configuração CIM** representa um determinado comportamento ou um estado funcional desejado para o [**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md)associado.

</dd> <dt>

[**\_ELEMENTSETTING CIM**](cim-elementsetting.md)
</dt> <dd>

A classe [**CIM \_ ElementSetting**](cim-elementsetting.md) representa a associação entre os elementos do sistema gerenciado e a classe de configuração definida para eles.

</dd> <dt>

[**\_ELEMENTSLINKED CIM**](cim-elementslinked.md)
</dt> <dd>

A associação [**CIM \_ ElementsLinked**](cim-elementslinked.md) representa os elementos físicos que são cabeados juntos por um link físico.

</dd> <dt>

[**\_ERRORCOUNTERSFORDEVICE CIM**](cim-errorcountersfordevice.md)
</dt> <dd>

A classe [**CIM \_ ErrorCountersForDevice**](cim-errorcountersfordevice.md) associa a classe [**CIM \_ DeviceErrorCounts**](cim-deviceerrorcounts.md) ao dispositivo lógico ao qual se aplica.

</dd> <dt>

[**\_EXECUTEPROGRAM CIM**](cim-executeprogram.md)
</dt> <dd>

A classe [**CIM \_ ExecuteProgram**](cim-executeprogram.md) representa os arquivos que podem ser executados no sistema onde o elemento de software está instalado.

</dd> <dt>

[**Exportação de CIM \_**](cim-export.md)
</dt> <dd>

A classe de [**\_ exportação CIM**](cim-export.md) representa uma associação entre um sistema de arquivos local e seus diretórios, o que indica que os diretórios especificados estão disponíveis para montagem. Ao exportar um sistema de arquivos inteiro, o diretório deve fazer referência ao diretório de nível superior do sistema de arquivos.

</dd> <dt>

[**\_EXTRACAPACITYGROUP CIM**](cim-extracapacitygroup.md)
</dt> <dd>

A classe [**CIM \_ ExtraCapacityGroup**](cim-extracapacitygroup.md) é derivada de um grupo de redundância que indica que os elementos agregados têm mais capacidade ou capacidade do que o necessário. Um exemplo desse tipo de redundância é a instalação de N + 1 fontes de alimentação ou ventiladores em um sistema.

</dd> <dt>

[**\_Ventilador CIM**](cim-fan.md)
</dt> <dd>

A classe de [**\_ ventilador CIM**](cim-fan.md) representa os recursos e o gerenciamento de um dispositivo de resfriamento de ventilador.

</dd> <dt>

[**\_Arquivo de arquivos CIM**](cim-fileaction.md)
</dt> <dd>

A [**classe \_ fileaction do CIM**](cim-fileaction.md) permite que o autor Localize arquivos que já existem no computador de um usuário e, em seguida, mova ou copie esses arquivos para um novo local.

</dd> <dt>

[**Inespecificações de CIM \_**](cim-filespecification.md)
</dt> <dd>

A classe [**CIM \_ fileespecífication**](cim-filespecification.md) representa um arquivo que está ligado ou desligado do sistema. O arquivo está localizado no diretório identificado pela Associação de [**\_ DirectorySpecificationFile do CIM**](cim-directoryspecificationfile.md) . O método [**Invoke**](invoke-method-in-class-cim-filespecification.md) usa as informações para verificar a existência do arquivo. Observe que as propriedades com um valor **nulo** não são verificadas.

</dd> <dt>

[**Armazenamento de filecim \_**](cim-filestorage.md)
</dt> <dd>

A associação de [**\_ armazenamento**](cim-filestorage.md) de arquivo CIM vincula o sistema de arquivos e os arquivos lógicos endereçados por meio do sistema de arquivos.

</dd> <dt>

[**\_Sistema de arquivos CIM**](cim-filesystem.md)
</dt> <dd>

A [**classe \_ FileSystem do CIM**](cim-filesystem.md) representa um arquivo ou conjunto de dados local para um sistema de computador ou montado remotamente de um servidor de arquivos.

</dd> <dt>

[**\_FLATPANEL CIM**](cim-flatpanel.md)
</dt> <dd>

A classe [**CIM \_ FlatPanel**](cim-flatpanel.md) representa os recursos e o gerenciamento do dispositivo lógico do painel plano.

</dd> <dt>

[**\_FROMDIRECTORYACTION CIM**](cim-fromdirectoryaction.md)
</dt> <dd>

A associação [**CIM \_ FromDirectoryAction**](cim-fromdirectoryaction.md) identifica o diretório de origem para a ação de arquivo. Quando essa associação é usada, a suposição é que o diretório de origem foi criado por uma ação anterior. Essa associação não pode existir com uma associação de [**\_ FromDirectorySpecification CIM**](cim-fromdirectoryspecification.md) ; uma ação de arquivo só pode envolver um único diretório de origem.

</dd> <dt>

[**\_FROMDIRECTORYSPECIFICATION CIM**](cim-fromdirectoryspecification.md)
</dt> <dd>

A associação [**CIM \_ FromDirectorySpecification**](cim-fromdirectoryspecification.md) identifica o diretório de origem para a ação de arquivo. Quando essa associação é usada, a suposição é que o diretório de origem já existe. Essa associação não pode existir com uma associação de [**\_ FromDirectoryAction CIM**](cim-fromdirectoryaction.md) ; uma ação de arquivo só pode envolver um único diretório de origem.

</dd> <dt>

[**\_FRU CIM**](cim-fru.md)
</dt> <dd>

A classe de [**\_ FRU do CIM**](cim-fru.md) representa uma coleção de produtos e elementos físicos definidos pelo fornecedor que estão associados a uma FRU (unidade de substituição de campo) para oferecer suporte, manutenção ou atualização de um produto no local do cliente.

</dd> <dt>

[**\_FRUINCLUDESPRODUCT CIM**](cim-fruincludesproduct.md)
</dt> <dd>

A classe [**CIM \_ FRUIncludesProduct**](cim-fruincludesproduct.md) indica que uma FRU (unidade substituível de campo) pode ser composta por outros produtos.

</dd> <dt>

[**\_FRUPHYSICALELEMENTS CIM**](cim-fruphysicalelements.md)
</dt> <dd>

A classe [**CIM \_ FRUPhysicalElements**](cim-fruphysicalelements.md) representa os elementos físicos que compõem uma unidade de substituição de campo (FRU).

</dd> <dt>

[**\_HEATPIPE CIM**](cim-heatpipe.md)
</dt> <dd>

A classe [**CIM \_ HeatPipe**](cim-heatpipe.md) representa os recursos e o gerenciamento de um dispositivo de resfriamento de tubo de calor.

</dd> <dt>

[**\_HOSTEDACCESSPOINT CIM**](cim-hostedaccesspoint.md)
</dt> <dd>

A classe [**CIM \_ HostedAccessPoint**](cim-hostedaccesspoint.md) representa uma associação entre um SAP (ponto de acesso a serviços) e o sistema no qual ele é fornecido. Cada sistema pode hospedar muitos SAPs.

</dd> <dt>

[**\_HOSTEDBOOTSAP CIM**](cim-hostedbootsap.md)
</dt> <dd>

A classe [**CIM \_ HostedBootSAP**](cim-hostedbootsap.md) define o sistema de computador unitário de hospedagem para uma classe [**\_ BootSAP CIM**](cim-bootsap.md) . Como essa relação é subclasse do [**CIM \_ HostedAccessPoint**](cim-hostedaccesspoint.md), ela herda o esquema de escopo/nomenclatura definido para o [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md), em que um ponto de acesso é adiado para seu sistema de hospedagem. Nesse caso, o **CIM \_ BootSAP** deve adiar para sua classe de [**\_ UnitaryComputerSystem do CIM**](cim-unitarycomputersystem.md) de hospedagem.

</dd> <dt>

[**\_HOSTEDBOOTSERVICE CIM**](cim-hostedbootservice.md)
</dt> <dd>

A classe [**CIM \_ HostedBootService**](cim-hostedbootservice.md) associa um sistema de hospedagem e um serviço de inicialização. Como essa relação é subclasse de [**CIM \_ HostedService**](cim-hostedservice.md), ela herda o esquema de escopo/nomenclatura definido para o serviço, em que um serviço é adiado para seu sistema de hospedagem.

</dd> <dt>

[**\_HOSTEDFILESYSTEM CIM**](cim-hostedfilesystem.md)
</dt> <dd>

A associação [**CIM \_ HostedFileSystem**](cim-hostedfilesystem.md) representa um link entre o sistema de computador e o sistema de arquivos hospedado no sistema de computador.

</dd> <dt>

[**\_HOSTEDJOBDESTINATION CIM**](cim-hostedjobdestination.md)
</dt> <dd>

A classe [**CIM \_ HostedJobDestination**](cim-hostedjobdestination.md) representa uma associação entre um destino de trabalho e o sistema no qual ele reside. Um sistema pode hospedar muitas filas de trabalho. Destinos de trabalho adiados para o sistema de hospedagem.

</dd> <dt>

[**HostedService do CIM \_**](cim-hostedservice.md)
</dt> <dd>

A classe [**CIM \_ HostedService**](cim-hostedservice.md) representa uma associação entre um serviço e o sistema no qual a funcionalidade reside. Um sistema pode hospedar muitos serviços, o que adia para o sistema de hospedagem. O modelo não representa serviços hospedados em vários sistemas.

</dd> <dt>

[**\_INFRAREDCONTROLLER CIM**](cim-infraredcontroller.md)
</dt> <dd>

A classe [**CIM \_ InfraredController**](cim-infraredcontroller.md) representa os recursos e o gerenciamento de um controlador de infravermelho.

</dd> <dt>

[**\_INSTALLEDOS CIM**](cim-installedos.md)
</dt> <dd>

A classe de associação [**CIM \_ InstalledOS**](cim-installedos.md) representa um link entre o sistema de computador e o sistema operacional instalado. Um sistema operacional é instalado quando está na extensão de armazenamento de um sistema de computador (por exemplo, copiado para uma unidade de disco ou baixado para memória).

</dd> <dt>

[**\_INSTALLEDSOFTWAREELEMENT CIM**](cim-installedsoftwareelement.md)
</dt> <dd>

A classe [**CIM \_ InstalledSoftwareElement**](cim-installedsoftwareelement.md) associa um sistema de computador a um elemento de software instalado.

</dd> <dt>

[**IRQ de CIM \_**](cim-irq.md)
</dt> <dd>

A classe de [**\_ IRQ de CIM**](cim-irq.md) representa uma IRQ (linha de solicitação de interrupção) de arquitetura da Intel.

</dd> <dt>

[**Trabalho do CIM \_**](cim-job.md)
</dt> <dd>

A classe de [**\_ trabalho CIM**](cim-job.md) representa uma unidade de trabalho para um sistema, como um trabalho de impressão. Um trabalho é diferente de um processo porque um trabalho pode ser agendado.

</dd> <dt>

[**\_JOBDESTINATION CIM**](cim-jobdestination.md)
</dt> <dd>

A classe [**CIM \_ JobDestination**](cim-jobdestination.md) representa onde um trabalho é enviado para processamento. Ele pode se referir a uma fila que contém zero ou mais trabalhos, como uma fila de impressão que contém trabalhos de impressão. Os destinos de trabalho são hospedados em sistemas, de forma semelhante ao modo como os serviços são hospedados em sistemas.

</dd> <dt>

[**\_JOBDESTINATIONJOBS CIM**](cim-jobdestinationjobs.md)
</dt> <dd>

A associação [**CIM \_ JobDestinationJobs**](cim-jobdestinationjobs.md) descreve onde um trabalho é enviado para processamento (ou seja, para qual destino de trabalho).

</dd> <dt>

[**\_Teclado CIM**](cim-keyboard.md)
</dt> <dd>

A classe de [**\_ teclado CIM**](cim-keyboard.md) representa os recursos e o gerenciamento do dispositivo lógico do teclado.

</dd> <dt>

[**\_LINKHASCONNECTOR CIM**](cim-linkhasconnector.md)
</dt> <dd>

A classe [**CIM \_ LinkHasConnector**](cim-linkhasconnector.md) associa cabos e links usados como conectores físicos, que conectam os elementos físicos. Essa associação define explicitamente a relação de conectores [**para \_ PhysicalLink CIM**](cim-physicallink.md).

</dd> <dt>

[**\_LOCALFILESYSTEM CIM**](cim-localfilesystem.md)
</dt> <dd>

A classe [**CIM \_ LocalFileSystem**](cim-localfilesystem.md) representa o repositório de arquivos controlado por um sistema de computador por meio de meios locais (por exemplo, acesso direto ao driver de dispositivo). O armazenamento de arquivos pode ser gerenciado diretamente pelo sistema de computador, sem a necessidade de outro computador agir como um servidor de arquivos. No entanto, para um sistema de arquivos clusterizado, o sistema de arquivos é local e, portanto, é adiado para o cluster.

</dd> <dt>

[**Local do CIM \_**](cim-location.md)
</dt> <dd>

A classe de [**\_ local do CIM**](cim-location.md) representa a posição e o endereço de um elemento físico.

</dd> <dt>

[**\_LOGICALDEVICE CIM**](cim-logicaldevice.md)
</dt> <dd>

A classe [**CIM \_ LogicalDevice**](cim-logicaldevice.md) representa uma entidade de hardware que pode ou não ser realizada em hardware físico.

</dd> <dt>

[**\_LOGICALDISK CIM**](cim-logicaldisk.md)
</dt> <dd>

A classe de [**\_ LogicalDisk CIM**](cim-logicaldisk.md) representa um intervalo contíguo de blocos lógicos que é identificável por um sistema de arquivos por meio do campo **DeviceID** (chave) do disco. por exemplo, em um ambiente Windows, o campo **deviceid** contém uma letra da unidade; em um ambiente UNIX, ele contém o caminho de acesso; e em um ambiente do NetWare, ele contém o nome do volume.

</dd> <dt>

[**\_LOGICALDISKBASEDONPARTITION CIM**](cim-logicaldiskbasedonpartition.md)
</dt> <dd>

A classe [**CIM \_ LogicalDiskBasedOnPartition**](cim-logicaldiskbasedonpartition.md) associa um disco lógico à partição de disco na qual ele reside.

</dd> <dt>

[**\_LOGICALDISKBASEDONVOLUMESET CIM**](cim-logicaldiskbasedonvolumeset.md)
</dt> <dd>

A associação de [**\_ LogicalDiskBasedOnVolumeSet do CIM**](cim-logicaldiskbasedonvolumeset.md) relaciona discos lógicos com o volume no qual eles são encontrados. Discos lógicos podem ser baseados em um único volume (por exemplo, exposto por um Gerenciador de volume de software) ou uma partição de disco.

</dd> <dt>

[**CIM \_ LogicalElement**](cim-logicalelement.md)
</dt> <dd>

A classe [**CIM \_ LogicalElement**](cim-logicalelement.md) é a classe base para todos os componentes do sistema que representam componentes do sistema abstratos, como perfis, processos ou recursos do sistema, na forma de dispositivos lógicos.

</dd> <dt>

[**CIM \_ LogicalFile**](cim-logicalfile.md)
</dt> <dd>

A classe [**CIM \_ LogicalFile**](cim-logicalfile.md) representa uma coleção nomeada de dados, que pode ser código executável, que está localizada em um sistema de arquivos em uma extensão de armazenamento.

</dd> <dt>

[**\_LOGICALIDENTITY CIM**](cim-logicalidentity.md)
</dt> <dd>

A classe [**CIM \_ LogicalIdentity**](cim-logicalidentity.md) é uma associação abstrata e genérica que indica que dois elementos lógicos representam diferentes aspectos da mesma entidade subjacente.

</dd> <dt>

[**\_MAGNETOOPTICALDRIVE CIM**](cim-magnetoopticaldrive.md)
</dt> <dd>

A classe [**CIM \_ MagnetoOpticalDrive**](cim-magnetoopticaldrive.md) representa os recursos e o gerenciamento de uma unidade magneto-óptica, um subtipo do dispositivo de acesso à mídia.

</dd> <dt>

[**\_MANAGEDSYSTEMELEMENT CIM**](cim-managedsystemelement.md)
</dt> <dd>

A classe [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) é a classe base para a hierarquia de elementos do sistema. Qualquer componente de sistema diferencial é um candidato para inclusão nessa classe.

</dd> <dt>

[**\_MANAGEMENTCONTROLLER CIM**](cim-managementcontroller.md)
</dt> <dd>

A classe [**CIM \_ ManagementController**](cim-managementcontroller.md) está relacionada aos recursos e ao gerenciamento de um controlador de gerenciamento.

</dd> <dt>

[**\_MEDIAACCESSDEVICE CIM**](cim-mediaaccessdevice.md)
</dt> <dd>

A classe [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md) representa a capacidade de acessar uma ou mais mídias e, em seguida, usar a mídia para armazenar e recuperar dados.

</dd> <dt>

[**\_MEDIAPRESENT CIM**](cim-mediapresent.md)
</dt> <dd>

A associação [**CIM \_ MediaPresent**](cim-mediapresent.md) descreve uma relação em que uma extensão de armazenamento deve ser acessada por meio de um dispositivo de acesso à mídia.

</dd> <dt>

[**\_Memória CIM**](cim-memory.md)
</dt> <dd>

A classe de [**\_ memória CIM**](cim-memory.md) representa os recursos e o gerenciamento de dispositivos lógicos relacionados à memória.

</dd> <dt>

[**\_MEMORYCAPACITY CIM**](cim-memorycapacity.md)
</dt> <dd>

A classe [**CIM \_ MemoryCapacity**](cim-memorycapacity.md) representa a memória que pode ser instalada em um elemento físico e suas configurações mínimas e máximas. Informações sobre a memória que está atualmente instalada e os requisitos mínimos e máximos de um elemento estão localizados em instâncias da classe [**CIM \_ PhysicalMemory**](cim-physicalmemory.md) .

</dd> <dt>

[**\_MEMORYCHECK CIM**](cim-memorycheck.md)
</dt> <dd>

A classe [**CIM \_ MemoryCheck**](cim-memorycheck.md) especifica uma condição para a quantidade mínima de memória que deve estar disponível em um sistema.

</dd> <dt>

[**\_MEMORYMAPPEDIO CIM**](cim-memorymappedio.md)
</dt> <dd>

A classe [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md) representa e/s mapeada pela memória da arquitetura do computador. Essa classe trata da memória e dos recursos de e/s de porta.

</dd> <dt>

[**\_MEMORYONCARD CIM**](cim-memoryoncard.md)
</dt> <dd>

A classe [**CIM \_ MemoryOnCard**](cim-memoryoncard.md) associa a memória física localizada em placas de hospedagem, placas de adaptador e assim por diante. Essa associação define explicitamente a relação de memória para os cartões.

</dd> <dt>

[**\_MEMORYWITHMEDIA CIM**](cim-memorywithmedia.md)
</dt> <dd>

A classe [**CIM \_ MemoryWithMedia**](cim-memorywithmedia.md) associa a memória física a uma mídia física e a seu cartucho. A memória fornece a identificação de mídia e armazena dados específicos do usuário.

</dd> <dt>

[**\_MODIFYSETTINGACTION CIM**](cim-modifysettingaction.md)
</dt> <dd>

A classe [**CIM \_ ModifySettingAction**](cim-modifysettingaction.md) representa as informações para modificar um arquivo de configuração específico, para uma entrada específica, com um valor específico.

</dd> <dt>

[**\_MONITORRESOLUTION CIM**](cim-monitorresolution.md)
</dt> <dd>

A classe [**CIM \_ MonitorResolution**](cim-monitorresolution.md) representa a relação entre as resoluções horizontal e vertical e a taxa de atualização e o modo de verificação para um monitor de desktop. Os valores são especificados no objeto do controlador de vídeo.

</dd> <dt>

[**\_MONITORSETTING CIM**](cim-monitorsetting.md)
</dt> <dd>

A classe [**CIM \_ MonitorSetting**](cim-monitorsetting.md) associa a resolução do monitor ao monitor de área de trabalho ao qual se aplica.

</dd> <dt>

[**Montagem de CIM \_**](cim-mount.md)
</dt> <dd>

A classe de [**\_ montagem CIM**](cim-mount.md) representa uma associação entre um sistema de arquivos e um diretório ao qual ele está anexado.

</dd> <dt>

[**\_MULTISTATESENSOR CIM**](cim-multistatesensor.md)
</dt> <dd>

A classe [**CIM \_ MultiStateSensor**](cim-multistatesensor.md) representa um conjunto de vários membros de sensores binários em que cada sensor binário relata um resultado booliano.

</dd> <dt>

[**\_Adaptador CIM**](cim-networkadapter.md)
</dt> <dd>

A classe [**CIM \_ adaptador**](cim-networkadapter.md) é uma classe abstrata que define os conceitos gerais de hardware de rede (por exemplo, endereço permanente ou velocidade de operação). As informações são transmitidas usando a associação [**CIM \_ DeviceSAPImplementation**](cim-devicesapimplementation.md) .

</dd> <dt>

[**\_NFS CIM**](cim-nfs.md)
</dt> <dd>

A classe [**CIM \_ NFS**](cim-nfs.md) representa um sistema de arquivos remoto que é montado, usando o protocolo NFS (sistema de arquivos de rede), de um sistema de computador.

</dd> <dt>

[**\_NONVOLATILESTORAGE CIM**](cim-nonvolatilestorage.md)
</dt> <dd>

A classe [**CIM \_ NonVolatileStorage**](cim-nonvolatilestorage.md) representa os recursos e o gerenciamento do armazenamento não volátil. A memória não volátil inclui, nativamente, o armazenamento flash e ROM.

</dd> <dt>

[**\_NUMERICSENSOR CIM**](cim-numericsensor.md)
</dt> <dd>

A classe [**CIM \_ NumericSensor**](cim-numericsensor.md) representa um sensor numérico que retorna leituras numéricas e, opcionalmente, dá suporte a configurações de limites.

</dd> <dt>

[**Sistema \_ operacional CIM**](cim-operatingsystem.md)
</dt> <dd>

A classe [**CIM \_ OperatingSystem**](cim-operatingsystem.md) representa um sistema operacional de computador, que é composto por software e firmware que tornam o hardware de um sistema de computador utilizável.

</dd> <dt>

[**\_OPERATINGSYSTEMSOFTWAREFEATURE CIM**](cim-operatingsystemsoftwarefeature.md)
</dt> <dd>

A classe [**CIM \_ OperatingSystemSoftwareFeature**](cim-operatingsystemsoftwarefeature.md) representa os recursos de software que compõem o sistema operacional.

</dd> <dt>

[**\_OSPROCESS CIM**](cim-osprocess.md)
</dt> <dd>

A classe [**CIM \_ OSProcess**](cim-osprocess.md) associa o sistema operacional e um ou mais processos em execução no contexto do sistema operacional.

</dd> <dt>

[**\_OSVERSIONCHECK CIM**](cim-osversioncheck.md)
</dt> <dd>

A classe [**CIM \_ OSVersionCheck**](cim-osversioncheck.md) especifica as versões do sistema operacional que podem dar suporte a um elemento de software.

</dd> <dt>

[**\_PACKAGEALARM CIM**](cim-packagealarm.md)
</dt> <dd>

A associação [**CIM \_ PackageAlarm**](/windows/desktop/SecCrypto/extendedproperties-newenum) representa a relação na qual um dispositivo de alarme é instalado como parte de um pacote. A instalação indica problemas com o ambiente do pacote — seu estado de segurança ou sua integridade geral.

</dd> <dt>

[**\_PACKAGECOOLING CIM**](cim-packagecooling.md)
</dt> <dd>

A associação [**CIM \_ PackageCooling**](cim-packagecooling.md) representa a relação na qual um dispositivo de resfriamento é instalado em um pacote, como um chassi ou rack, para auxiliar na resfriamento do pacote.

</dd> <dt>

[**\_PACKAGEDCOMPONENT CIM**](cim-packagedcomponent.md)
</dt> <dd>

A associação [**CIM \_ PackagedComponent**](cim-packagedcomponent.md) representa uma relação explícita na qual um componente é normalmente contido por um pacote físico, como um chassi ou cartão.

</dd> <dt>

[**\_PACKAGEINCHASSIS CIM**](cim-packageinchassis.md)
</dt> <dd>

A associação [**CIM \_ PackageInChassis**](cim-packageinchassis.md) representa a relação na qual um chassi pode conter outros pacotes, como outros chassis e cartões.

</dd> <dt>

[**\_PACKAGEINSLOT CIM**](cim-packageinslot.md)
</dt> <dd>

A associação [**CIM \_ PackageInSlot**](cim-packageinslot.md) representa a relação entre os cartões de dispositivo e o chassi no qual eles são montados.

</dd> <dt>

[**\_PACKAGETEMPSENSOR CIM**](cim-packagetempsensor.md)
</dt> <dd>

A associação [**CIM \_ PackageTempSensor**](cim-packagetempsensor.md) representa a relação na qual um sensor de temperatura é frequentemente instalado em um pacote, como um chassi ou um rack, para monitorar o ambiente do pacote.

</dd> <dt>

[**\_PARALLELCONTROLLER CIM**](cim-parallelcontroller.md)
</dt> <dd>

A associação de [**\_ ParallelController CIM**](cim-parallelcontroller.md) está relacionada aos recursos e ao gerenciamento do dispositivo lógico de porta paralela.

</dd> <dt>

[**\_PARTICIPATESINSET CIM**](cim-participatesinset.md)
</dt> <dd>

A classe [**CIM \_ ParticipatesInSet**](cim-participatesinset.md) identifica os elementos físicos que devem ser substituídos juntos.

</dd> <dt>

[**\_PCICONTROLLER CIM**](cim-pcicontroller.md)
</dt> <dd>

A classe [**CIM \_ PCIController**](cim-pcicontroller.md) representa as propriedades e o gerenciamento de um controlador PCI. As propriedades nessa classe e suas subclasses são definidas nas várias especificações de PCI publicadas pelo SIG de PCI.

</dd> <dt>

[**\_PCMCIACONTROLLER CIM**](cim-pcmciacontroller.md)
</dt> <dd>

A classe [**CIM \_ PCMCIAController**](cim-pcmciacontroller.md) representa os recursos e o gerenciamento de um controlador de PCMCIA (Associação Internacional de cartão de memória) do computador pessoal.

</dd> <dt>

[**\_PCVIDEOCONTROLLER CIM**](cim-pcvideocontroller.md)
</dt> <dd>

O [**\_ PCVideoController CIM**](cim-pcvideocontroller.md) representa os recursos e o gerenciamento de um controlador de vídeo de computador pessoal, um subtipo de um controlador de vídeo.

</dd> <dt>

[**\_PEXTENTREDUNDANCYCOMPONENT CIM**](cim-pextentredundancycomponent.md)
</dt> <dd>

A classe [**CIM \_ PExtentRedundancyComponent**](cim-pextentredundancycomponent.md) representa as extensões físicas que participam de um grupo de redundância de armazenamento.

</dd> <dt>

[**\_PHYSICALCAPACITY CIM**](cim-physicalcapacity.md)
</dt> <dd>

A classe [**CIM \_ PhysicalCapacity**](cim-physicalcapacity.md) é uma classe abstrata que representa os requisitos mínimos e máximos de um elemento físico e sua capacidade de dar suporte a diferentes tipos de hardware. Por exemplo, os requisitos mínimos e máximos de memória podem ser modelados como uma subclasse de **\_ PhysicalCapacity CIM**.

</dd> <dt>

[**\_PHYSICALCOMPONENT CIM**](cim-physicalcomponent.md)
</dt> <dd>

A classe [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md) representa um componente básico ou de baixo nível em um pacote. Um elemento físico que não é um link, um conector ou um pacote é um descendente (ou membro) dessa classe.

</dd> <dt>

[**\_PHYSICALCONNECTOR CIM**](cim-physicalconnector.md)
</dt> <dd>

A classe [**CIM \_ PhysicalConnector**](cim-physicalconnector.md) representa qualquer elemento físico que é usado para se conectar a outros elementos. Qualquer objeto que possa se conectar e transmitir sinais ou potência entre dois ou mais elementos físicos é um descendente (ou membro) dessa classe.

</dd> <dt>

[**Físico do CIM \_**](cim-physicalelement.md)
</dt> <dd>

As subclasses do [**CIM \_ PhysicalElement**](cim-physicalelement.md) definem qualquer componente de um sistema que tenha uma identidade física distinta. As instâncias dessa classe podem ser definidas em termos de rótulos que podem ser fisicamente anexados ao objeto.

</dd> <dt>

[**\_PHYSICALELEMENTLOCATION CIM**](cim-physicalelementlocation.md)
</dt> <dd>

A classe [**CIM \_ PhysicalElementLocation**](cim-physicalelementlocation.md) associa um elemento físico a um objeto de [**\_ local CIM**](cim-location.md) para fins de inventário ou substituição.

</dd> <dt>

[**\_PHYSICALEXTENT CIM**](cim-physicalextent.md)
</dt> <dd>

A classe [**CIM \_ PhysicalExtent**](cim-physicalextent.md) representa uma implementação de RAID SCC. Ele define os endereços de bloco endereçáveis consecutivos em um único dispositivo de armazenamento que são tratados como uma única extensão de armazenamento na mesma classe [**CIM \_ StorageRedundancyGroup**](cim-storageredundancygroup.md) . Uma alternativa, quando a configuração automática é usada, é instanciar ou estender a classe [**CIM \_ AggregatePExtent**](cim-aggregatepextent.md) .

</dd> <dt>

[**\_PHYSICALFRAME CIM**](cim-physicalframe.md)
</dt> <dd>

A classe [**CIM \_ PhysicalFrame**](cim-physicalframe.md) é uma classe pai de rack, chassi e outros compartimentos de quadro, pois são definidos em classes de extensão. Propriedades como **VisibleAlarm** e **AudibleAlarm** e dados relacionados a violações de segurança são incluídos nessa classe pai.

</dd> <dt>

[**\_PHYSICALLINK CIM**](cim-physicallink.md)
</dt> <dd>

A classe [**CIM \_ PhysicalLink**](cim-physicallink.md) representa o cabeamento dos elementos físicos.

</dd> <dt>

[**\_PHYSICALMEDIA CIM**](cim-physicalmedia.md)
</dt> <dd>

A classe [**CIM \_ PhysicalMedia**](cim-physicalmedia.md) representa tipos de mídia de documentação e armazenamento, como fitas, CD ROMs e assim por diante.

</dd> <dt>

[**\_PHYSICALMEMORY CIM**](cim-physicalmemory.md)
</dt> <dd>

A classe [**CIM \_ PhysicalMemory**](cim-physicalmemory.md) representa dispositivos de memória de nível baixo, como Simms, DIMMs, chips de memória bruta e assim por diante.

</dd> <dt>

[**\_PHYSICALPACKAGE CIM**](cim-physicalpackage.md)
</dt> <dd>

A classe [**CIM \_ PhysicalPackage**](cim-physicalpackage.md) representa os elementos físicos que contêm ou hospedam outros componentes. Os exemplos são um compartimento de rack ou uma placa de adaptador.

</dd> <dt>

[**\_POINTINGDEVICE CIM**](cim-pointingdevice.md)
</dt> <dd>

A classe [**CIM \_ PointingDevice**](cim-pointingdevice.md) representa um dispositivo que aponta para regiões na exibição. Qualquer dispositivo que manipule um ponteiro ou aponta para regiões em uma exibição Visual é membro dessa classe. Por exemplo, um mouse, uma caneta, um touch pad ou um Tablet.

</dd> <dt>

[**\_POTSMODEM CIM**](cim-potsmodem.md)
</dt> <dd>

A classe [**CIM \_ POTSModem**](cim-potsmodem.md) representa um dispositivo que traduz dados binários em modulações de onda para transmissão baseada em som conectando-se à rede do sistema de telefonia antigo (POTS).

</dd> <dt>

[**Fonte de \_ alimentação CIM**](cim-powersupply.md)
</dt> <dd>

A classe [**CIM \_ powersupply**](cim-powersupply.md) representa os recursos e o gerenciamento do dispositivo lógico da fonte de energia.

</dd> <dt>

[**\_Impressora CIM**](cim-printer.md)
</dt> <dd>

A classe de [**\_ impressora CIM**](cim-printer.md) representa os recursos e o gerenciamento do dispositivo lógico da impressora.

</dd> <dt>

[**\_Processo CIM**](cim-process.md)
</dt> <dd>

A classe de [**\_ processo CIM**](cim-process.md) representa uma única instância de um programa em execução. Um usuário normalmente vê um processo como um aplicativo ou uma tarefa.

</dd> <dt>

[**\_PROCESSEXECUTABLE CIM**](cim-processexecutable.md)
</dt> <dd>

A classe [**CIM \_ ProcessExecutable**](cim-processexecutable.md) representa um vínculo entre um processo e um arquivo de dados e indica que o arquivo participa da execução do processo.

</dd> <dt>

[**\_Processador CIM**](cim-processor.md)
</dt> <dd>

A classe de [**\_ processador CIM**](cim-processor.md) representa os recursos e o gerenciamento do dispositivo lógico do processador.

</dd> <dt>

[**\_PROCESSTHREAD CIM**](cim-processthread.md)
</dt> <dd>

A classe [**CIM \_ ProcessThread**](cim-processthread.md) representa um link entre um processo e os threads em execução no contexto do processo.

</dd> <dt>

[**\_Produto CIM**](cim-product.md)
</dt> <dd>

A classe de [**\_ produto CIM**](cim-product.md) é uma classe concreta que representa uma coleção de elementos físicos, recursos de software e outros produtos, adquiridos como uma unidade. A aquisição implica um contrato entre o fornecedor e o consumidor, o que pode ter implicações no licenciamento, suporte e garantia do produto.

</dd> <dt>

[**\_PRODUCTFRU CIM**](cim-productfru.md)
</dt> <dd>

A classe [**CIM \_ ProductFRU**](cim-productfru.md) representa uma associação entre o produto e uma unidade de substituição de campo (FRU), que fornece informações sobre os componentes do produto que foram ou estão sendo substituídos.

</dd> <dt>

[**\_PRODUCTPARENTCHILD CIM**](cim-productparentchild.md)
</dt> <dd>

A associação [**CIM \_ ProductParentChild**](cim-productparentchild.md) define uma hierarquia pai-filho entre os produtos. Por exemplo, um produto pode ser agrupado com outros produtos.

</dd> <dt>

[**\_PRODUCTPHYSICALELEMENTS CIM**](cim-productphysicalelements.md)
</dt> <dd>

A classe [**CIM \_ ProductPhysicalElements**](cim-productphysicalelements.md) representa os elementos físicos que compõem um produto.

</dd> <dt>

[**\_PRODUCTPRODUCTDEPENDENCY CIM**](cim-productproductdependency.md)
</dt> <dd>

A classe [**CIM \_ ProductProductDependency**](cim-productproductdependency.md) representa uma associação entre dois produtos, que indica que um deve ser instalado ou ausente para que o outro funcione. Isso é conceitualmente equivalente à associação [**de \_ ServiceServiceDependency do CIM**](cim-serviceservicedependency.md) .

</dd> <dt>

[**\_PRODUCTSOFTWAREFEATURES CIM**](cim-productsoftwarefeatures.md)
</dt> <dd>

A associação [**CIM \_ ProductSoftwareFeatures**](cim-productsoftwarefeatures.md) identifica os recursos de software para um produto específico.

</dd> <dt>

[**\_PRODUCTSUPPORT CIM**](cim-productsupport.md)
</dt> <dd>

A classe [**CIM \_ ProductSupport**](cim-productsupport.md) representa uma associação entre produto e acesso de suporte que transmite como o suporte é obtido para o produto. Vários tipos de suporte estão disponíveis para um produto; o mesmo objeto de suporte pode fornecer assistência para vários produtos.

</dd> <dt>

[**\_PROTECTEDSPACEEXTENT CIM**](cim-protectedspaceextent.md)
</dt> <dd>

A classe [**CIM \_ ProtectedSpaceExtent**](cim-protectedspaceextent.md) representa endereços de bloco lógico endereçáveis, que são tratados como uma única extensão de armazenamento, mas estão localizados em uma única extensão física.

</dd> <dt>

[**\_PSEXTENTBASEDONPEXTENT CIM**](cim-psextentbasedonpextent.md)
</dt> <dd>

A classe [**CIM \_ PSExtentBasedOnPExtent**](cim-psextentbasedonpextent.md) associa extensões de espaço protegidas que se baseiam em uma extensão física.

</dd> <dt>

[**\_Rack CIM**](cim-rack.md)
</dt> <dd>

A classe de [**\_ rack CIM**](cim-rack.md) representa um rack (um quadro físico ou compartimento) no qual os chassis são armazenados. Normalmente, um rack representa o compartimento; todos os componentes em funcionamento são empacotados no chassi.

</dd> <dt>

[**O CIM \_ percebe**](cim-realizes.md)
</dt> <dd>

O [**CIM \_ percebe**](cim-realizes.md) que a classe representa a associação que define o mapeamento entre um dispositivo lógico e o componente físico que implementa o dispositivo.

</dd> <dt>

[**\_REALIZESAGGREGATEPEXTENT CIM**](cim-realizesaggregatepextent.md)
</dt> <dd>

A associação [**CIM \_ RealizesAggregatePExtent**](cim-realizesaggregatepextent.md) representa a relação na qual a classe [**CIM \_ AggregatePExtent**](cim-aggregatepextent.md) é realizada em uma mídia física.

</dd> <dt>

[**\_REALIZESDISKPARTITION CIM**](cim-realizesdiskpartition.md)
</dt> <dd>

A classe [**CIM \_ RealizesDiskPartition**](cim-realizesdiskpartition.md) representa uma partição de disco em uma mídia física que modela a criação de partições em uma unidade SCSI ou IDE bruto.

</dd> <dt>

[**\_REALIZESPEXTENT CIM**](cim-realizespextent.md)
</dt> <dd>

A associação [**CIM \_ RealizesPExtent**](cim-realizespextent.md) representa a relação na qual as extensões físicas são realizadas em uma mídia física. Além disso, o endereço inicial da extensão física na mídia física é especificado.

</dd> <dt>

[**Reinicialização de CIM \_**](cim-rebootaction.md)
</dt> <dd>

A classe [**CIM \_ rebootaction**](cim-rebootaction.md) causa uma reinicialização do sistema onde o elemento de software é instalado.

</dd> <dt>

[**\_REDUNDANCYCOMPONENT CIM**](cim-redundancycomponent.md)
</dt> <dd>

A classe [**CIM \_ RedundancyComponent**](cim-redundancycomponent.md) associa um grupo de redundância composto por elementos do sistema gerenciado e indica que, juntos, os elementos fornecem redundância. Todos os elementos agregados em um grupo de redundância devem ser instanciações da mesma classe de objeto.

</dd> <dt>

[**\_REDUNDANCYGROUP CIM**](cim-redundancygroup.md)
</dt> <dd>

A classe [**CIM \_ RedundancyGroup**](cim-redundancygroup.md) representa uma coleção de elementos de sistema gerenciados, que indica que os componentes agregados, juntos, fornecem redundância. Todos os elementos agregados em um grupo de redundância devem ser instanciações da mesma classe de objeto.

</dd> <dt>

[**\_Refrigeração CIM**](cim-refrigeration.md)
</dt> <dd>

A classe de [**\_ refrigeração CIM**](cim-refrigeration.md) representa os recursos e o gerenciamento de um dispositivo de resfriamento de refrigeração.

</dd> <dt>

[**\_RELATEDSTATISTICS CIM**](cim-relatedstatistics.md)
</dt> <dd>

A associação [**CIM \_ RelatedStatistics**](cim-relatedstatistics.md) representa hierarquias e dependências de classes [**\_ StatisticalInformation do CIM**](cim-statisticalinformation.md) relacionadas.

</dd> <dt>

[**\_REMOTEFILESYSTEM CIM**](cim-remotefilesystem.md)
</dt> <dd>

A classe [**CIM \_ RemoteFileSystem**](cim-remotefilesystem.md) representa um sistema de arquivos remoto que é acessado por meio de um serviço relacionado à rede. Nesse caso, o armazenamento de arquivos é hospedado por um computador, que atua como um servidor de arquivos.

</dd> <dt>

[**\_REMOVEDIRECTORYACTION CIM**](cim-removedirectoryaction.md)
</dt> <dd>

A classe [**CIM \_ RemoveDirectoryAction**](cim-removedirectoryaction.md) remove diretórios de elementos de software.

</dd> <dt>

[**\_RemoveFile CIM**](cim-removefileaction.md)
</dt> <dd>

A classe [**CIM \_ removeaction**](cim-removefileaction.md) desinstala arquivos.

</dd> <dt>

[**Replacement do CIM \_**](cim-replacementset.md)
</dt> <dd>

A classe de conjunto de [**\_ substituição CIM**](cim-replacementset.md) agrega elementos físicos que devem ser substituídos juntos. Por exemplo, ao substituir um cartão de memória, os chips de memória do componente também podem ser removidos e substituídos. Ou, essa associação pode ser usada para substituir ou atualizar um conjunto de chips de memória.

</dd> <dt>

[**\_RESIDESONEXTENT CIM**](cim-residesonextent.md)
</dt> <dd>

A classe [**CIM \_ ResidesOnExtent**](cim-residesonextent.md) representa uma associação entre um sistema de arquivos e a extensão de armazenamento onde ele está localizado. Normalmente, um sistema de arquivos reside em um disco lógico.

</dd> <dt>

[**\_RUNNINGOS CIM**](cim-runningos.md)
</dt> <dd>

A classe [**CIM \_ RunningOS**](cim-runningos.md) representa o sistema operacional em execução no momento. No máximo, um sistema operacional pode ser executado a qualquer momento em um sistema de computador; o sistema de computador pode não estar inicializado no momento ou seu sistema operacional pode ser desconhecido.

</dd> <dt>

[**\_SAPSAPDEPENDENCY CIM**](cim-sapsapdependency.md)
</dt> <dd>

A classe [**CIM \_ SAPSAPDependency**](cim-sapsapdependency.md) é uma associação entre dois SAPs (pontos de acesso ao serviço), o que indica que o segundo SAP é necessário para que o primeiro SAP se conecte ao seu serviço.

</dd> <dt>

[**\_Scanner CIM**](cim-scanner.md)
</dt> <dd>

O [**\_ scanner CIM**](cim-scanner.md) representa os recursos e o gerenciamento do dispositivo lógico do scanner.

</dd> <dt>

[**\_SCSICONTROLLER CIM**](cim-scsicontroller.md)
</dt> <dd>

A classe [**CIM \_ SCSIController**](cim-scsicontroller.md) representa os recursos e o gerenciamento do dispositivo lógico do controlador SCSI.

</dd> <dt>

[**\_SCSIINTERFACE CIM**](cim-scsiinterface.md)
</dt> <dd>

representa uma relação de [**\_ ControlledBy CIM**](cim-controlledby.md) que indica quais dispositivos são acessados por meio de um controlador SCSI e as características de acesso.

</dd> <dt>

[**\_Sensor CIM**](cim-sensor.md)
</dt> <dd>

A classe de [**\_ sensor CIM**](cim-sensor.md) representa um dispositivo de hardware capaz de medir as características de uma propriedade física (por exemplo, as características de temperatura ou voltagem de um sistema de computador unitário).

</dd> <dt>

[**\_SERIALCONTROLLER CIM**](cim-serialcontroller.md)
</dt> <dd>

A classe [**CIM \_ SerialController**](cim-serialcontroller.md) representa os recursos e o gerenciamento do dispositivo lógico da porta serial.

</dd> <dt>

[**\_SERIALINTERFACE CIM**](cim-serialinterface.md)
</dt> <dd>

A classe [**CIM \_ SerialInterface**](cim-serialinterface.md) representa um relacionamento [**CIM \_ ControlledBy**](cim-controlledby.md) que indica quais dispositivos são acessados por meio do controlador serial e as características do acesso.

</dd> <dt>

[**\_Serviço CIM**](cim-service.md)
</dt> <dd>

A classe de [**\_ serviço CIM**](cim-service.md) representa um elemento lógico que contém informações para representar e gerenciar a funcionalidade fornecida por um dispositivo ou recurso de software. Um serviço é um objeto de finalidade geral para configurar e gerenciar a implementação da funcionalidade; Ela não é a funcionalidade propriamente dita.

</dd> <dt>

[**\_SERVICEACCESSBYSAP CIM**](cim-serviceaccessbysap.md)
</dt> <dd>

A classe de associação [**CIM \_ ServiceAccessBySAP**](cim-serviceaccessbysap.md) representa os pontos de acesso de um serviço. por exemplo, uma impressora pode ser acessada pelos SAPs (pontos de acesso ao serviço) do NetWare, do Macintosh ou do Windows, que são potencialmente hospedados em sistemas diferentes.

</dd> <dt>

[**\_SERVICEACCESSPOINT CIM**](cim-serviceaccesspoint.md)
</dt> <dd>

A classe [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md) representa a capacidade de usar ou invocar um serviço. Os pontos de acesso representam serviços que estão disponíveis para uso por outras entidades.

</dd> <dt>

[**\_SERVICESAPDEPENDENCY CIM**](cim-servicesapdependency.md)
</dt> <dd>

A classe [**CIM \_ ServiceSAPDependency**](cim-servicesapdependency.md) representa uma associação entre um serviço e um ponto de acesso de serviço (SAP), que indica que o SAP referenciado é usado pelo serviço para fornecer sua funcionalidade.

</dd> <dt>

[**\_SERVICESERVICEDEPENDENCY CIM**](cim-serviceservicedependency.md)
</dt> <dd>

A classe [**CIM \_ ServiceServiceDependency**](cim-serviceservicedependency.md) representa uma associação entre dois serviços.

</dd> <dt>

[**Configuração de CIM \_**](cim-setting.md)
</dt> <dd>

A classe de [**\_ configuração CIM**](cim-setting.md) representa parâmetros operacionais e relacionados à configuração para um ou mais elementos do sistema gerenciado.

</dd> <dt>

[**\_SETTINGCHECK CIM**](cim-settingcheck.md)
</dt> <dd>

A classe [**CIM \_ SettingCheck**](cim-settingcheck.md) especifica as informações necessárias para verificar um arquivo de configuração específico em busca de uma entrada específica que contenha um valor igual ao valor especificado. Todas as comparações são consideradas não diferenciando maiúsculas de minúsculas.

</dd> <dt>

[**\_SETTINGCONTEXT CIM**](cim-settingcontext.md)
</dt> <dd>

A classe [**CIM \_ SettingContext**](cim-settingcontext.md) associa objetos de configuração a objetos de configuração.

</dd> <dt>

[**\_Slot CIM**](cim-slot.md)
</dt> <dd>

A classe de [**\_ slot CIM**](cim-slot.md) representa conectores nos quais os pacotes são inseridos.

</dd> <dt>

[**\_SLOTINSLOT CIM**](cim-slotinslot.md)
</dt> <dd>

A relação de [**\_ SlotInSlot do CIM**](cim-slotinslot.md) representa a capacidade de um adaptador especial estender a estrutura de slot existente para permitir que cartões incompatíveis sejam conectados a um quadro ou placa de hospedagem.

</dd> <dt>

[**\_Software CIM**](cim-softwareelement.md)
</dt> <dd>

A classe [**CIM \_ softwareelement**](cim-softwareelement.md) decompõe um objeto [**CIM \_ SoftwareFeature**](cim-softwarefeature.md) em um conjunto de partes individuais gerenciáveis ou implantáveis para uma plataforma específica. A plataforma de um elemento de software é identificada exclusivamente por sua arquitetura de hardware e sistema operacional subjacentes.

</dd> <dt>

[**\_SOFTWAREELEMENTACTIONS CIM**](cim-softwareelementactions.md)
</dt> <dd>

A associação [**CIM \_ SoftwareElementActions**](cim-softwareelementactions.md) identifica as ações para um elemento de software.

</dd> <dt>

[**\_SOFTWAREELEMENTCHECKS CIM**](cim-softwareelementchecks.md)
</dt> <dd>

A classe de associação [**CIM \_ SoftwareElementChecks**](cim-softwareelementchecks.md) relaciona um elemento de software com informações de condição ou local que um recurso pode exigir.

</dd> <dt>

[**\_SOFTWAREELEMENTVERSIONCHECK CIM**](cim-softwareelementversioncheck.md)
</dt> <dd>

A classe [**CIM \_ SoftwareElementVersionCheck**](cim-softwareelementversioncheck.md) representa um tipo de elemento de software que deve existir no ambiente.

</dd> <dt>

[**\_SOFTWAREFEATURE CIM**](cim-softwarefeature.md)
</dt> <dd>

A classe [**CIM \_ SoftwareFeature**](cim-softwarefeature.md) representa uma função ou um recurso específico de um produto ou sistema de aplicativos.

</dd> <dt>

[**\_SOFTWAREFEATURESAPIMPLEMENTATION CIM**](cim-softwarefeaturesapimplementation.md)
</dt> <dd>

A classe [**CIM \_ SoftwareFeatureSAPImplementation**](cim-softwarefeaturesapimplementation.md) representa uma associação entre um ponto de acesso de serviço (SAP) e como ele é implementado no software.

</dd> <dt>

[**\_SOFTWAREFEATURESERVICEIMPLEMENTATION CIM**](cim-softwarefeatureserviceimplementation.md)
</dt> <dd>

A classe [**CIM \_ SoftwareFeatureServiceImplementation**](cim-softwarefeatureserviceimplementation.md) representa uma associação entre um serviço e como ele é implementado no software.

</dd> <dt>

[**\_SOFTWAREFEATURESOFTWAREELEMENTS CIM**](cim-softwarefeaturesoftwareelements.md)
</dt> <dd>

A associação [**CIM \_ SoftwareFeatureSoftwareElements**](cim-softwarefeaturesoftwareelements.md) identifica os elementos de software que compõem um recurso de software específico.

</dd> <dt>

[**Telespare CIM \_**](cim-sparegroup.md)
</dt> <dd>

A classe de [**\_ Spar sobressalente CIM**](cim-sparegroup.md) é derivada da classe [**CIM \_ RedundancyGroup**](cim-redundancygroup.md) e indica que um ou mais dos elementos agregados podem ser resobrados.

</dd> <dt>

[**\_STATISTICALINFORMATION CIM**](cim-statisticalinformation.md)
</dt> <dd>

A classe [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md) é uma classe raiz para a coleção arbitrária de dados estatísticos ou métricas aplicáveis a um ou mais elementos do sistema gerenciados.

</dd> <dt>

[**Estatísticas de CIM \_**](cim-statistics.md)
</dt> <dd>

A classe Cim Statistics representa uma associação que relaciona elementos do sistema gerenciado aos grupos [**\_ estatísticos**](cim-statistics.md) que se aplicam a eles.

</dd> <dt>

[**CIM \_ StorageDefect**](cim-storagedefect.md)
</dt> <dd>

A [**agregação Cim \_ StorageDefect**](cim-storagedefect.md) coleta os erros de armazenamento para uma extensão de armazenamento.

</dd> <dt>

[**CIM \_ StorageError**](cim-storageerror.md)
</dt> <dd>

A [**classe CIM \_ StorageError**](cim-storageerror.md) representa blocos de espaço de mídia ou memória mapeados fora de uso devido a erros. A chave da classe é a **propriedade StartingAddress** dos bytes em erro.

</dd> <dt>

[**CIM \_ StorageExtent**](cim-storageextent.md)
</dt> <dd>

A [**classe CIM \_ StorageExtent**](cim-storageextent.md) representa os recursos e o gerenciamento das várias mídias existentes para armazenar dados e permitir a recuperação de dados. Essa classe pai pode representar os vários componentes do RAID (hardware ou software) ou uma extensão lógica bruta sobre a mídia física.

</dd> <dt>

[**CIM \_ StorageRedundancyGroup**](cim-storageredundancygroup.md)
</dt> <dd>

A [**classe CIM \_ StorageRedundancyGroup**](cim-storageredundancygroup.md) representa informações de redundância relacionadas ao armazenamento em massa.

</dd> <dt>

[**Suporte \_ CIMAccess**](cim-supportaccess.md)
</dt> <dd>

A [**classe CIM \_ SupportAccess**](cim-supportaccess.md) define como obter assistência para um produto.

</dd> <dt>

[**CIM \_ SwapSpaceCheck**](cim-swapspacecheck.md)
</dt> <dd>

A [**classe CIM \_ SwapSpaceCheck**](cim-swapspacecheck.md) especifica a quantidade de espaço de permuta que deve estar disponível no sistema.

</dd> <dt>

[**Sistema \_ CIM**](cim-system.md)
</dt> <dd>

A [**classe \_ Sistema CIM**](cim-system.md) agrega um conjunto enumerável de elementos do sistema gerenciado. A agregação opera como um todo funcional. Em qualquer subclasse específica do sistema, há uma lista bem definida de classes de elemento do sistema gerenciado cujas instâncias devem ser agregadas.

</dd> <dt>

[**CIM \_ SystemComponent**](cim-systemcomponent.md)
</dt> <dd>

uma modelo CIM de associação CIM (modelo CIM) que estabelece relações entre um sistema e os elementos do sistema gerenciado dos quais ele é composto.

</dd> <dt>

[**CIM \_ SystemDevice**](cim-systemdevice.md)
</dt> <dd>

A [**associação \_ Cim SystemDevice**](cim-systemdevice.md) representa uma relação explícita na qual os dispositivos lógicos podem ser agregados por um sistema.

</dd> <dt>

[**CIM \_ SystemResource**](cim-systemresource.md)
</dt> <dd>

A [**classe CIM \_ SystemResource**](cim-systemresource.md) representa uma entidade gerenciada pelo BIOS ou um sistema operacional que está disponível para uso por dispositivos lógicos e de software.

</dd> <dt>

[**CIM \_ Tachometer**](cim-tachometer.md)
</dt> <dd>

A [**classe CIM \_ Tachometer**](cim-tachometer.md) existe para compatibilidade com versões anteriores com definições de esquema CIM anteriores.

</dd> <dt>

[**CIM \_ TapeDrive**](cim-tapedrive.md)
</dt> <dd>

A [**classe \_ TapeDrive CIM**](cim-tapedrive.md) representa uma unidade de fita no sistema. As unidades de fita são diferenciadas principalmente porque só podem ser acessadas sequencialmente.

</dd> <dt>

[**CIM \_ TemperatureSensor**](cim-temperaturesensor.md)
</dt> <dd>

A [**classe \_ TemperatureSensor cim**](cim-temperaturesensor.md) existe para compatibilidade com versões anteriores com definições de esquema CIM anteriores.

</dd> <dt>

[**CIM \_ Thread**](cim-thread.md)
</dt> <dd>

A [**classe \_ Thread CIM**](cim-thread.md) representa a capacidade de executar unidades de um processo ou tarefa, em paralelo. Um processo pode ter muitos threads, cada um deles é fraco para o processo.

</dd> <dt>

[**CIM \_ ToDirectoryAction**](cim-todirectoryaction.md)
</dt> <dd>

A [**associação CIM \_ ToDirectoryAction**](cim-todirectoryaction.md) identifica o diretório de destino para a ação do arquivo.

</dd> <dt>

[**CIM \_ ToDirectorySpecification**](cim-todirectoryspecification.md)
</dt> <dd>

A [**associação CIM \_ ToDirectorySpecification**](cim-todirectoryspecification.md) identifica o diretório de destino para a ação do arquivo.

</dd> <dt>

[**CIM \_ UninterruptiblePowerSupply**](cim-uninterruptiblepowersupply.md)
</dt> <dd>

A [**classe CIM \_ UninterruptiblePowerSupply**](cim-uninterruptiblepowersupply.md) representa os recursos e o gerenciamento de uma fonte de alimentação ininterrupta (UPS).

</dd> <dt>

[**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md)
</dt> <dd>

A [**classe CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md) representa uma área de trabalho, móvel, computador de rede, servidor ou outro tipo de sistema de computador de nó único.

</dd> <dt>

[**CIM \_ USBController**](cim-usbcontroller.md)
</dt> <dd>

A [**classe CIM \_ USBController**](cim-usbcontroller.md) representa os recursos e o gerenciamento de um controlador USB.

</dd> <dt>

[**CIM \_ USBControllerHasHub**](cim-usbcontrollerhashub.md)
</dt> <dd>

A [**classe CIM \_ USBControllerHasHub**](cim-usbcontrollerhashub.md) define os hubs que são downstream do controlador USB.

</dd> <dt>

[**CIM \_ USBDevice**](cim-usbdevice.md)
</dt> <dd>

A [**classe CIM \_ USBDevice**](cim-usbdevice.md) representa as características de gerenciamento de um dispositivo USB.

</dd> <dt>

[**CIM \_ USBHub**](cim-usbhub.md)
</dt> <dd>

A [**classe CIM \_ USBHub**](cim-usbhub.md) representa os recursos e o gerenciamento de um hub USB.

</dd> <dt>

[**CIM \_ UserDevice**](cim-userdevice.md)
</dt> <dd>

A [**classe \_ UserDevice cim**](cim-userdevice.md) é uma classe pai da qual outras classes, como Teclado [**CIM \_**](cim-keyboard.md) ou [**Cim \_ DesktopMonitor,**](cim-desktopmonitor.md)descendem. Os dispositivos de usuário são dispositivos lógicos que permitem ao usuário do sistema de computador inserir, exibir ou ouvir dados.

</dd> <dt>

[**CIM \_ VersionCompatibilityCheck**](cim-versioncompatibilitycheck.md)
</dt> <dd>

A [**classe CIM \_ VersionCompatibilityCheck**](cim-versioncompatibilitycheck.md) especifica se é permitido criar o próximo estado de um elemento de software.

</dd> <dt>

[**CIM \_ VideoBIOSElement**](cim-videobioselement.md)
</dt> <dd>

A [**classe CIM \_ VideoBIOSElement**](cim-videobioselement.md) representa o software de baixo nível carregado no armazenamento não volátil e usado para configurar e acessar o controlador de vídeo e a exibição de um sistema de computador.

</dd> <dt>

[**CIM \_ VideoBIOSFeature**](cim-videobiosfeature.md)
</dt> <dd>

A [**classe CIM \_ VideoBIOSFeature**](cim-videobiosfeature.md) representa os recursos do software de baixo nível usado para configurar e acessar o controlador de vídeo e a exibição de um sistema de computador.

</dd> <dt>

[**CIM \_ VideoBIOSFeatureVideoBIOSElements**](cim-videobiosfeaturevideobioselements.md)
</dt> <dd>

A [**classe CIM \_ VideoBIOSFeatureVideoBIOSElements**](cim-videobiosfeaturevideobioselements.md) associa um recurso de BIOS de vídeo e seus elementos BIOS de vídeo agregados.

</dd> <dt>

[**CIM \_ VideoController**](cim-videocontroller.md)
</dt> <dd>

A [**classe CIM \_ VideoController**](cim-videocontroller.md) representa os recursos e o gerenciamento do controlador de vídeo.

</dd> <dt>

[**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)
</dt> <dd>

A [**classe CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md) representa os vários modos de vídeo que um controlador de vídeo pode dar suporte.

</dd> <dt>

[**CIM \_ VideoSetting**](cim-videosetting.md)
</dt> <dd>

A [**classe CIM \_ VideoSetting**](cim-videosetting.md) associa o objeto de configuração [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md) ao controlador ao qual ele se aplica.

</dd> <dt>

[**CIM \_ VolatileStorage**](cim-volatilestorage.md)
</dt> <dd>

A [**classe CIM \_ VolatileStorage**](cim-volatilestorage.md) representa os recursos e o gerenciamento do armazenamento volátil.

</dd> <dt>

[**CIM \_ VoltageSensor**](cim-voltagesensor.md)
</dt> <dd>

A [**classe CIM \_ VoltageSensor**](cim-voltagesensor.md) existe para compatibilidade com versões anteriores de definições de esquema CIM. Com adições às classes [**Cim \_ Sensor**](cim-sensor.md) e [**CIM \_ NumericSensor**](cim-numericsensor.md) na versão 2.2, não é mais necessário.

</dd> <dt>

[**CIM \_ VolumeSet**](cim-volumeset.md)
</dt> <dd>

A [**classe CIM \_ VolumeSet**](cim-volumeset.md) representa um intervalo contíguo de blocos lógicos apresentados ao ambiente operacional para leitura e escrita de dados do usuário.

</dd> <dt>

[**CIM \_ WORMDrive**](cim-wormdrive.md)
</dt> <dd>

A [**classe CIM \_ WORMDrive**](cim-wormdrive.md) representa os recursos e o gerenciamento de uma unidade WORM, um subtipo do dispositivo de acesso à mídia.

</dd> </dl>

 

 
