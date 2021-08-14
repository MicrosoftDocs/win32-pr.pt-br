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

A classe de [**\_ chip CIM**](cim-chip.md) representa o tipo de hardware de circuito integrado, incluindo ASICs, processadores, chips de memória e assim por diante.

</dd> <dt>

[**\_CLUSTERINGSAP CIM**](cim-clusteringsap.md)
</dt> <dd>

A classe [**CIM \_ ClusteringSAP**](cim-clusteringsap.md) representa os pontos de acesso de um serviço de clustering.

</dd> <dt>

[**\_CLUSTERINGSERVICE CIM**](cim-clusteringservice.md)
</dt> <dd>

A classe [**CIM \_ ClusteringService**](cim-clusteringservice.md) representa a funcionalidade fornecida por um cluster. Por exemplo, a funcionalidade de failover pode ser modelada como um serviço de um cluster de failover.

</dd> <dt>

[**\_CLUSTERSERVICEACCESSBYSAP CIM**](cim-clusterserviceaccessbysap.md)
</dt> <dd>

A classe [**CIM \_ ClusterServiceAccessBySAP**](cim-clusterserviceaccessbysap.md) representa a relação entre um serviço de clustering e seus pontos de acesso.

</dd> <dt>

[**\_COLLECTEDCOLLECTIONS CIM**](cim-collectedcollections.md)
</dt> <dd>

A classe [**CIM \_ CollectedCollections**](cim-collectedcollections.md) é uma associação de agregação que representa uma coleção de elementos do sistema gerenciados (MSE) contidas em uma coleção de MSEs.

</dd> <dt>

[**\_COLLECTEDMSES CIM**](cim-collectedmses.md)
</dt> <dd>

A classe de associação [**CIM \_ CollectedMSEs**](cim-collectedmses.md) representa os membros do objeto GROUPING, uma classe [**CollectionOfMSEs**](cim-collectionofmses.md) .

</dd> <dt>

[**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md)
</dt> <dd>

O objeto [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) permite o agrupamento de objetos [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) com a finalidade de associar definições e configurações. É abstrato exigir mais definição e refinamento semântico em subclasses.

</dd> <dt>

[**\_COLLECTIONOFSENSORS CIM**](cim-collectionofsensors.md)
</dt> <dd>

A associação [**CIM \_ CollectionOfSensors**](cim-collectionofsensors.md) representa os sensores binários que compõem o sensor de multiestado.

</dd> <dt>

[**\_COLLECTIONSETTING CIM**](cim-collectionsetting.md)
</dt> <dd>

A classe [**CIM \_ CollectionSetting**](cim-collectionsetting.md) representa a associação entre um [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) e a classe de configuração definida para eles.

</dd> <dt>

[**\_COMPATIBLEPRODUCT CIM**](cim-compatibleproduct.md)
</dt> <dd>

A classe [**CIM \_ CompatibleProduct**](cim-compatibleproduct.md) representa uma associação entre produtos que indica se dois produtos referenciados são interoperáveis, como se eles podem ser instalados juntos ou se um pode ser o contêiner físico para o outro, e assim por diante.

</dd> <dt>

[**\_Componente CIM**](cim-component.md)
</dt> <dd>

A associação de [**\_ componente CIM**](cim-component.md) representa as partes de uma relação entre MSEs.

</dd> <dt>

[**\_Sistema de COMPUTERSYSTEM CIM**](cim-computersystem.md)
</dt> <dd>

Uma classe de [**\_ sistema CIM**](cim-computersystem.md) representa uma coleção especial de instâncias do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) . Esta coleção fornece recursos do computador e serve como um ponto de agregação para associar um ou mais dos seguintes elementos: sistema de arquivos, sistema operacional, processador e memória (armazenamento volátil e não volátil). Essa classe é derivada do [**\_ sistema CIM**](cim-system.md).

</dd> <dt>

[**\_COMPUTERSYSTEMDMA CIM**](cim-computersystemdma.md)
</dt> <dd>

A classe [**CIM \_ ComputerSystemDMA**](cim-computersystemdma.md) representa uma associação entre um sistema de computador e seus canais de DMA (acesso direto à memória) disponíveis.

</dd> <dt>

[**\_COMPUTERSYSTEMIRQ CIM**](cim-computersystemirq.md)
</dt> <dd>

A classe [**CIM \_ ComputerSystemIRQ**](cim-computersystemirq.md) representa uma associação entre um sistema de computador e suas IRQs (linhas de solicitação de interrupção) disponíveis.

</dd> <dt>

[**\_COMPUTERSYSTEMMAPPEDIO CIM**](cim-computersystemmappedio.md)
</dt> <dd>

A classe [**CIM \_ ComputerSystemMappedIO**](cim-computersystemmappedio.md) representa uma associação entre um sistema de computador e suas portas de e/s mapeadas de memória disponíveis.

</dd> <dt>

[**\_COMPUTERSYSTEMPACKAGE CIM**](cim-computersystempackage.md)
</dt> <dd>

A classe [**CIM \_ ComputerSystemPackage**](cim-computersystempackage.md) representa uma associação que define explicitamente a relação entre os sistemas de computador unitários e um ou mais pacotes físicos. A associação é semelhante à forma como os dispositivos lógicos são concretizados por elementos físicos.

</dd> <dt>

[**\_COMPUTERSYSTEMRESOURCE CIM**](cim-computersystemresource.md)
</dt> <dd>

A classe [**CIM \_ ComputerSystemResource**](cim-computersystemresource.md) representa uma associação entre um sistema de computador e seus recursos de sistema disponíveis.

</dd> <dt>

[**Configuração de CIM \_**](cim-configuration.md)
</dt> <dd>

O objeto de [**\_ configuração CIM**](cim-configuration.md) permite o agrupamento de conjuntos de parâmetros (definidos em objetos de [**\_ configuração CIM**](cim-setting.md) ) e dependências para um ou mais elementos do sistema gerenciado.

</dd> <dt>

[**CIM \_ conectado**](cim-connectedto.md)
</dt> <dd>

A classe [**CIM \_ conectadoto**](cim-connectedto.md) representa uma associação que indica que dois ou mais conectores físicos estão conectados.

</dd> <dt>

[**\_CONNECTORONPACKAGE CIM**](cim-connectoronpackage.md)
</dt> <dd>

A classe [**CIM \_ ConnectorOnPackage**](cim-connectoronpackage.md) representa uma associação que torna explícita a relação de confinamento entre conectores e pacotes. Os pacotes físicos contêm conectores e outros elementos físicos.

</dd> <dt>

[**\_Contêiner CIM**](cim-container.md)
</dt> <dd>

A classe de [**\_ contêiner CIM**](cim-container.md) representa uma associação entre um elemento físico contido e um que o contém. Um objeto recipiente deve ser um pacote físico.

</dd> <dt>

[**\_CONTROLLEDBY CIM**](cim-controlledby.md)
</dt> <dd>

O relacionamento [**CIM \_ ControlledBy**](cim-controlledby.md) indica quais dispositivos são incluídos no comando ou acessados por meio do dispositivo lógico do controlador.

</dd> <dt>

[**\_Controlador CIM**](cim-controller.md)
</dt> <dd>

A classe do [**\_ controlador CIM**](cim-controller.md) é uma classe pai para agrupar dispositivos diversos relacionados ao controle. Os exemplos de controladores são controladores SCSI, controladores USB e controladores seriais.

</dd> <dt>

[**\_COOLINGDEVICE CIM**](cim-coolingdevice.md)
</dt> <dd>

A classe [**CIM \_ CoolingDevice**](cim-coolingdevice.md) representa os recursos e o gerenciamento de dispositivos de resfriamento.

</dd> <dt>

[**CIM \_ CopyAction**](cim-copyfileaction.md)
</dt> <dd>

A classe [**CIM \_ CopyValue**](cim-copyfileaction.md) representa a movimentação ou a cópia de arquivos de um sistema de computador para um novo local.

</dd> <dt>

[**CIM \_ Createdirectoryaction**](cim-createdirectoryaction.md)
</dt> <dd>

A classe [**CIM \_ createdirectoryaction**](cim-createdirectoryaction.md) cria diretórios vazios para que os elementos de software sejam instalados localmente.

</dd> <dt>

[**\_CURRENTSENSOR CIM**](cim-currentsensor.md)
</dt> <dd>

A classe [**CIM \_ CurrentSensor**](cim-currentsensor.md) existe para compatibilidade com versões anteriores de definições de esquema CIM.

</dd> <dt>

[**DataFile de CIM \_**](cim-datafile.md)
</dt> <dd>

A classe de [**\_ DataFile do CIM**](cim-datafile.md) representa uma coleção nomeada de dados ou código executável. Somente as instâncias de arquivos em discos fixos locais serão retornadas

</dd> <dt>

[**\_Dependência CIM**](cim-dependency.md)
</dt> <dd>

A classe de [**\_ dependência CIM**](cim-dependency.md) representa uma associação que estabelece relações de dependência entre objetos.

</dd> <dt>

[**\_DEPENDENCYCONTEXT CIM**](cim-dependencycontext.md)
</dt> <dd>

O relacionamento [**CIM \_ DependencyContext**](cim-dependencycontext.md) associa uma classe de [**\_ dependência CIM**](cim-dependency.md) a um ou mais objetos de [**\_ configuração CIM**](cim-configuration.md) . Por exemplo, as dependências de um sistema de computador podem ser alteradas com base na rede à qual o sistema está anexado.

</dd> <dt>

[**\_DESKTOPMONITOR CIM**](cim-desktopmonitor.md)
</dt> <dd>

A classe [**CIM \_ DesktopMonitor**](cim-desktopmonitor.md) representa os recursos e o gerenciamento do dispositivo lógico do monitor de área de trabalho (CRT).

</dd> <dt>

[**\_DEVICEACCESSEDBYFILE CIM**](cim-deviceaccessedbyfile.md)
</dt> <dd>

A classe de associação [**CIM \_ DeviceAccessedByFile**](cim-deviceaccessedbyfile.md) especifica o dispositivo lógico acessado usando a classe de [**\_ dispositivo CIM**](cim-devicefile.md) referenciada.

</dd> <dt>

[**\_DEVICECONNECTION CIM**](cim-deviceconnection.md)
</dt> <dd>

A classe de associação [**CIM \_ DeviceConnection**](cim-deviceconnection.md) representa dois ou mais dispositivos conectados.

</dd> <dt>

[**\_DEVICEERRORCOUNTS CIM**](cim-deviceerrorcounts.md)
</dt> <dd>

A classe [**CIM \_ DeviceErrorCounts**](cim-deviceerrorcounts.md) é uma classe estatística que contém contadores relacionados a erros para um dispositivo lógico. Os tipos de erros são definidos por CCITT (REC X. 733) e ISO (IEC 10164-4).

</dd> <dt>

[**\_Dispositivo CIM**](cim-devicefile.md)
</dt> <dd>

A classe [**CIM \_ devicefile**](cim-devicefile.md) representa um tipo de arquivo lógico, que representa um dispositivo. Essa convenção é útil para sistemas operacionais que gerenciam dispositivos usando um modelo de e/s de fluxo de bytes. O dispositivo lógico associado a esse arquivo é especificado usando a relação de [**\_ DeviceAccessedByFile do CIM**](cim-deviceaccessedbyfile.md) .

</dd> <dt>

[**\_DEVICESAPIMPLEMENTATION CIM**](cim-devicesapimplementation.md)
</dt> <dd>

A classe [**CIM \_ DeviceSAPImplementation**](cim-devicesapimplementation.md) representa uma associação entre um ponto de acesso de serviço (SAP) e como ele é implementado. Quando muitos dispositivos lógicos são associados a um SAP, os elementos operam em conjunto para fornecer o ponto de acesso. Se houver implementações diferentes de um SAP, cada implementação resultará em instanciações individuais do objeto SAP.

</dd> <dt>

[**\_DEVICESERVICEIMPLEMENTATION CIM**](cim-deviceserviceimplementation.md)
</dt> <dd>

A classe [**CIM \_ DeviceServiceImplementation**](cim-deviceserviceimplementation.md) representa uma associação entre um serviço e como ele é implementado. Quando vários dispositivos são associados a um serviço, os elementos operam em conjunto para fornecer o serviço. Se houver implementações diferentes de um serviço, cada implementação resultará em instanciações individuais do objeto de serviço.

</dd> <dt>

[**\_DEVICESOFTWARE CIM**](cim-devicesoftware.md)
</dt> <dd>

O relacionamento [**CIM \_ DeviceSoftware**](cim-devicesoftware.md) identifica o software associado a um dispositivo, como drivers, configuração ou software de aplicativo ou firmware.

</dd> <dt>

[**\_Diretório CIM**](cim-directory.md)
</dt> <dd>

A classe de [**\_ diretório CIM**](cim-directory.md) representa um tipo de arquivo que agrupa logicamente os arquivos de dados que ele contém e fornece informações de caminho para os arquivos agrupados.

</dd> <dt>

[**\_Directoryaction do CIM**](cim-directoryaction.md)
</dt> <dd>

A classe abstrata do [**CIM \_ directoryaction**](cim-directoryaction.md) gerencia diretórios. A criação de diretório é tratada pela classe [**CIM \_ createdirectoryaction**](cim-createdirectoryaction.md) e a remoção de diretório é tratada pela classe [**CIM \_ RemoveDirectoryAction**](cim-removedirectoryaction.md) .

</dd> <dt>

[**\_DIRECTORYCONTAINSFILE CIM**](cim-directorycontainsfile.md)
</dt> <dd>

A classe [**CIM \_ DirectoryContainsFile**](cim-directorycontainsfile.md) representa uma associação entre um diretório e os arquivos contidos nesse diretório.

</dd> <dt>

[**\_DIRECTORYSPECIFICATION CIM**](cim-directoryspecification.md)
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

[**Cim \_ EsvasadoController**](cim-infraredcontroller.md)
</dt> <dd>

A [**classe \_ Cim DesaloqueadoController**](cim-infraredcontroller.md) representa as funcionalidades e o gerenciamento de um controlador com fio.

</dd> <dt>

[**CIM \_ InstalledOS**](cim-installedos.md)
</dt> <dd>

A [**classe de associação CIM \_ InstalledOS**](cim-installedos.md) representa um link entre o sistema de computador e o sistema operacional instalado. Um sistema operacional é instalado quando ele está na extensão de armazenamento do sistema de computador (por exemplo, copiado para uma unidade de disco ou baixado na memória).

</dd> <dt>

[**CIM \_ InstalledSoftwareElement**](cim-installedsoftwareelement.md)
</dt> <dd>

A [**classe CIM \_ InstalledSoftwareElement**](cim-installedsoftwareelement.md) associa um sistema de computador a um elemento de software instalado.

</dd> <dt>

[**CIM \_ IRQ**](cim-irq.md)
</dt> <dd>

A [**classe CIM \_ IRQ**](cim-irq.md) representa uma IRQ (linha de solicitação de interrupção) da arquitetura Intel.

</dd> <dt>

[**Trabalho \_ CIM**](cim-job.md)
</dt> <dd>

A [**classe De \_ trabalho CIM**](cim-job.md) representa uma unidade de trabalho para um sistema, como um trabalho de impressão. Um trabalho é diferente de um processo porque um trabalho pode ser agendado.

</dd> <dt>

[**JobDestination do CIM \_**](cim-jobdestination.md)
</dt> <dd>

A [**classe \_ JobDestination cim**](cim-jobdestination.md) representa o local em que um trabalho é enviado para processamento. Ele pode se referir a uma fila que contém zero ou mais trabalhos, como uma fila de impressão que contém trabalhos de impressão. Destinos de trabalho são hospedados em sistemas, semelhante à maneira como os serviços são hospedados em sistemas.

</dd> <dt>

[**\_JobDestinationJobs do CIM**](cim-jobdestinationjobs.md)
</dt> <dd>

A [**associação \_ JobDestinationJobs**](cim-jobdestinationjobs.md) do CIM descreve onde um trabalho é enviado para processamento (ou seja, para qual destino do trabalho).

</dd> <dt>

[**Teclado \_ CIM**](cim-keyboard.md)
</dt> <dd>

A [**classe \_ teclado CIM**](cim-keyboard.md) representa os recursos e o gerenciamento do dispositivo lógico do teclado.

</dd> <dt>

[**CIM \_ LinkHasConnector**](cim-linkhasconnector.md)
</dt> <dd>

A [**classe CIM \_ LinkHasConnector**](cim-linkhasconnector.md) associa cabos e links usados como conectores físicos, que conectam os elementos físicos. Essa associação define explicitamente a relação de conectores para [**CIM \_ PhysicalLink.**](cim-physicallink.md)

</dd> <dt>

[**CIM \_ LocalFileSystem**](cim-localfilesystem.md)
</dt> <dd>

A [**classe Cim \_ LocalFileSystem**](cim-localfilesystem.md) representa o armazenamento de arquivos controlado por um sistema de computador por meio de meios locais (por exemplo, acesso direto ao driver de dispositivo). O armazenamento de arquivos pode ser gerenciado diretamente pelo sistema de computador, sem a necessidade de outro computador atuar como um servidor de arquivos. No entanto, para um sistema de arquivos cluster, o sistema de arquivos é local e, portanto, é adiado para o cluster.

</dd> <dt>

[**Localização do CIM \_**](cim-location.md)
</dt> <dd>

A [**classe \_ Local CIM**](cim-location.md) representa a posição e o endereço de um elemento físico.

</dd> <dt>

[**CIM \_ LogicalDevice**](cim-logicaldevice.md)
</dt> <dd>

A [**classe \_ LogicalDevice cim**](cim-logicaldevice.md) representa uma entidade de hardware que pode ou não ser realizada em hardware físico.

</dd> <dt>

[**CIM \_ LogicalDisk**](cim-logicaldisk.md)
</dt> <dd>

A [**classe \_ LogicalDisk cim**](cim-logicaldisk.md) representa um intervalo contíguo de blocos lógicos que é identificável por um sistema de arquivos por meio do campo **DeviceID** (chave) do disco. Por exemplo, em um ambiente Windows, o **campo DeviceID** contém uma letra da unidade; em um UNIX, ele contém o caminho de acesso; e em um ambiente do NetWare, ele contém o nome do volume.

</dd> <dt>

[**CIM \_ LogicalDiskBasedOnPartition**](cim-logicaldiskbasedonpartition.md)
</dt> <dd>

A [**classe \_ LogicalDiskBasedOnPartition cim**](cim-logicaldiskbasedonpartition.md) associa um disco lógico à partição de disco na qual ele reside.

</dd> <dt>

[**CIM \_ LogicalDiskBasedOnVolumeSet**](cim-logicaldiskbasedonvolumeset.md)
</dt> <dd>

A [**associação \_ LogicalDiskBasedOnVolumeSet**](cim-logicaldiskbasedonvolumeset.md) cim relaciona discos lógicos com o volume no qual eles são encontrados. Os discos lógicos podem ser baseados em um único volume (por exemplo, exposto por um gerenciador de volume de software) ou em uma partição de disco.

</dd> <dt>

[**CIM \_ LogicalElement**](cim-logicalelement.md)
</dt> <dd>

A [**classe \_ LogicalElement cim**](cim-logicalelement.md) é a classe base para todos os componentes do sistema que representam componentes abstratos do sistema, como perfis, processos ou funcionalidades do sistema, na forma de dispositivos lógicos.

</dd> <dt>

[**CIM \_ LogicalFile**](cim-logicalfile.md)
</dt> <dd>

A [**classe \_ LogicalFile CIM**](cim-logicalfile.md) representa uma coleção nomeada de dados, que pode ser um código executável, localizado em um sistema de arquivos em uma extensão de armazenamento.

</dd> <dt>

[**CIM \_ LogicalIdentity**](cim-logicalidentity.md)
</dt> <dd>

A [**classe \_ LogicalIdentity cim**](cim-logicalidentity.md) é uma associação abstrata e genérica que indica que dois elementos lógicos representam aspectos diferentes da mesma entidade subjacente.

</dd> <dt>

[**CIM \_ CimOpticalDrive**](cim-magnetoopticaldrive.md)
</dt> <dd>

A [**classe CIM \_ LtdOpticalDrive**](cim-magnetoopticaldrive.md) representa os recursos e o gerenciamento de uma unidade de disco óptico, um subtipo do dispositivo de acesso à mídia.

</dd> <dt>

[**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)
</dt> <dd>

A [**classe CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) é a classe base para a hierarquia de elementos do sistema. Qualquer componente de sistema distinguível é um candidato para inclusão nesta classe.

</dd> <dt>

[**CIM \_ ManagementController**](cim-managementcontroller.md)
</dt> <dd>

A [**classe CIM \_ ManagementController**](cim-managementcontroller.md) está relacionada aos recursos e ao gerenciamento de um controlador de gerenciamento.

</dd> <dt>

[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)
</dt> <dd>

A [**classe CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md) representa a capacidade de acessar uma ou mais mídias e, em seguida, usar a mídia para armazenar e recuperar dados.

</dd> <dt>

[**CIM \_ MediaPresent**](cim-mediapresent.md)
</dt> <dd>

A [**associação CIM \_ MediaPresent**](cim-mediapresent.md) descreve uma relação em que uma extensão de armazenamento deve ser acessada por meio de um dispositivo de acesso à mídia.

</dd> <dt>

[**Memória \_ CIM**](cim-memory.md)
</dt> <dd>

A [**classe \_ Memória CIM**](cim-memory.md) representa os recursos e o gerenciamento de dispositivos lógicos relacionados à memória.

</dd> <dt>

[**Memória \_ CIMCapacidade**](cim-memorycapacity.md)
</dt> <dd>

A [**classe Cim \_ MemoryCapacity**](cim-memorycapacity.md) representa a memória que pode ser instalada em um elemento físico e suas configurações mínimas e máximas. Informações sobre a memória atualmente instalada e os requisitos mínimos e máximos de um elemento estão localizadas em instâncias da [**classe Cim \_ PhysicalMemory.**](cim-physicalmemory.md)

</dd> <dt>

[**CIM \_ MemoryCheck**](cim-memorycheck.md)
</dt> <dd>

A [**classe CIM \_ MemoryCheck**](cim-memorycheck.md) especifica uma condição para a quantidade mínima de memória que deve estar disponível em um sistema.

</dd> <dt>

[**CIM \_ MemoryMappedIO**](cim-memorymappedio.md)
</dt> <dd>

A [**classe CIM \_ MemoryMappedIO representa**](cim-memorymappedio.md) a E/S mapeada na memória da arquitetura do computador. Essa classe trata de recursos de E/S de memória e porta.

</dd> <dt>

[**CIM \_ MemoryOnCard**](cim-memoryoncard.md)
</dt> <dd>

A [**classe CIM \_ MemoryOnCard**](cim-memoryoncard.md) associa a memória física localizada em placas de hospedagem, cartões de adaptador e assim por diante. Essa associação define explicitamente a relação de memória com cartões.

</dd> <dt>

[**Memória \_ CIMWithMedia**](cim-memorywithmedia.md)
</dt> <dd>

A [**classe CIM \_ MemoryWithMedia**](cim-memorywithmedia.md) associa a memória física a uma mídia física e a seu corpo. A memória fornece identificação de mídia e armazena dados específicos do usuário.

</dd> <dt>

[**CIM \_ ModifySettingAction**](cim-modifysettingaction.md)
</dt> <dd>

A [**classe CIM \_ ModifySettingAction**](cim-modifysettingaction.md) representa as informações para modificar um arquivo de configuração específico, para uma entrada específica, com um valor específico.

</dd> <dt>

[**CIM \_ MonitorResolution**](cim-monitorresolution.md)
</dt> <dd>

A [**classe CIM \_ MonitorResolution**](cim-monitorresolution.md) representa a relação entre resoluções horizontais e verticais e a taxa de atualização e o modo de verificação para um monitor da área de trabalho. Os valores são especificados no objeto do controlador de vídeo.

</dd> <dt>

[**CIM \_ MonitorSetting**](cim-monitorsetting.md)
</dt> <dd>

A [**classe CIM \_ MonitorSetting**](cim-monitorsetting.md) associa a resolução do monitor ao monitor da área de trabalho ao qual ele se aplica.

</dd> <dt>

[**Montagem cim \_**](cim-mount.md)
</dt> <dd>

A [**classe \_ Montagem CIM**](cim-mount.md) representa uma associação entre um sistema de arquivos e um diretório ao qual ele está anexado.

</dd> <dt>

[**CIM \_ MultiStateSensor**](cim-multistatesensor.md)
</dt> <dd>

A [**classe CIM \_ MultiStateSensor**](cim-multistatesensor.md) representa um conjunto de vários membros de sensores binários em que cada sensor binário relata um resultado booliana.

</dd> <dt>

[**CIM \_ NetworkAdapter**](cim-networkadapter.md)
</dt> <dd>

A [**classe CIM \_ NetworkAdapter**](cim-networkadapter.md) é uma classe abstrata que define conceitos gerais de hardware de rede (por exemplo, endereço permanente ou velocidade de operação). As informações são transmitidas usando a [**associação CIM \_ DeviceSAPImplementation.**](cim-devicesapimplementation.md)

</dd> <dt>

[**CIM \_ NFS**](cim-nfs.md)
</dt> <dd>

A [**classe \_ CIM NFS**](cim-nfs.md) representa um sistema de arquivos remoto montado, usando o protocolo NFS (sistema de arquivos de rede), de um sistema de computador.

</dd> <dt>

[**CIM \_ NonVolatileStorage**](cim-nonvolatilestorage.md)
</dt> <dd>

A [**classe \_ Cim NonVolatileStorage**](cim-nonvolatilestorage.md) representa os recursos e o gerenciamento de armazenamento não volátil. A memória nãovolatile inclui o armazenamento de FLASH e ROM de forma nativa.

</dd> <dt>

[**CIM \_ NumericSensor**](cim-numericsensor.md)
</dt> <dd>

A [**classe \_ NUMERICSensor cim**](cim-numericsensor.md) representa um sensor numérico que retorna leituras numéricas e, opcionalmente, dá suporte a configurações de limites.

</dd> <dt>

[**Sistema operacional CIM \_**](cim-operatingsystem.md)
</dt> <dd>

A [**classe CIM \_ OperatingSystem**](cim-operatingsystem.md) representa um sistema operacional do computador, que é feito de software e firmware que torna o hardware de um sistema de computador acessível.

</dd> <dt>

[**CIM \_ OperatingSystemSoftwareFeature**](cim-operatingsystemsoftwarefeature.md)
</dt> <dd>

A [**classe CIM \_ OperatingSystemSoftwareFeature**](cim-operatingsystemsoftwarefeature.md) representa os recursos de software que comem o sistema operacional.

</dd> <dt>

[**CIM \_ OSProcess**](cim-osprocess.md)
</dt> <dd>

A [**classe CIM \_ OSProcess**](cim-osprocess.md) associa o sistema operacional e um ou mais processos em execução no contexto do sistema operacional.

</dd> <dt>

[**CIM \_ OSVersionCheck**](cim-osversioncheck.md)
</dt> <dd>

A [**classe CIM \_ OSVersionCheck**](cim-osversioncheck.md) especifica as versões do sistema operacional que podem dar suporte a um elemento de software.

</dd> <dt>

[**CIM \_ PackageAlarm**](cim-packagealarm.md)
</dt> <dd>

A [**associação \_ PackageAlarm cim**](/windows/desktop/SecCrypto/extendedproperties-newenum) representa a relação na qual um dispositivo de alarme é instalado como parte de um pacote. A instalação indica problemas com o ambiente do pacote– seu estado de segurança ou sua saúde geral.

</dd> <dt>

[**Package Cooling do CIM \_**](cim-packagecooling.md)
</dt> <dd>

A [**associação \_ Package Cooling cim**](cim-packagecooling.md) representa a relação na qual um dispositivo de resfriamento é instalado em um pacote, como um chassi ou rack, para auxiliar no resfriamento do pacote.

</dd> <dt>

[**CIM \_ PackagedComponent**](cim-packagedcomponent.md)
</dt> <dd>

A [**associação \_ Cim PackagedComponent**](cim-packagedcomponent.md) representa uma relação explícita na qual um componente normalmente é contido por um pacote físico, como um chassi ou cartão.

</dd> <dt>

[**CIM \_ PackageInChassis**](cim-packageinchassis.md)
</dt> <dd>

A [**associação \_ Cim PackageInChassis**](cim-packageinchassis.md) representa a relação na qual um chassi pode conter outros pacotes, como outros chassis e cartões.

</dd> <dt>

[**Pacote \_ CIMInSlot**](cim-packageinslot.md)
</dt> <dd>

A [**associação \_ Cim PackageInSlot**](cim-packageinslot.md) representa a relação entre as placas de dispositivo e o chassi no qual elas são montadas.

</dd> <dt>

[**CIM \_ PackageTempSensor**](cim-packagetempsensor.md)
</dt> <dd>

A [**associação \_ PackageTempSensor cim**](cim-packagetempsensor.md) representa a relação na qual um sensor de temperatura geralmente é instalado em um pacote, como um chassi ou um rack, para monitorar o ambiente do pacote.

</dd> <dt>

[**ParallelController do CIM \_**](cim-parallelcontroller.md)
</dt> <dd>

A [**associação \_ ParallelController**](cim-parallelcontroller.md) cim está relacionada aos recursos e ao gerenciamento do dispositivo lógico de porta paralela.

</dd> <dt>

[**CIM \_ ParticipatesInSet**](cim-participatesinset.md)
</dt> <dd>

A [**classe CIM \_ ParticipatesInSet**](cim-participatesinset.md) identifica elementos físicos que devem ser substituídos juntos.

</dd> <dt>

[**CIM \_ PCIController**](cim-pcicontroller.md)
</dt> <dd>

A [**classe CIM \_ PCIController**](cim-pcicontroller.md) representa as propriedades e o gerenciamento de um controlador PCI. As propriedades nessa classe e suas subclasses são definidas nas várias especificações de PCI publicadas pelo PCI SIG.

</dd> <dt>

[**CIM \_ PCMCIAController**](cim-pcmciacontroller.md)
</dt> <dd>

A [**classe CIM \_ PCMCIAController**](cim-pcmciacontroller.md) representa os recursos e o gerenciamento de um controlador PCMCIA (Associação Internacional de Cartão de Memória de Computador Pessoal).

</dd> <dt>

[**CIM \_ PCVideoController**](cim-pcvideocontroller.md)
</dt> <dd>

O [**\_ PCVideoController cim**](cim-pcvideocontroller.md) representa os recursos e o gerenciamento de um controlador de vídeo de computador pessoal, um subtipo de um controlador de vídeo.

</dd> <dt>

[**CIM \_ PExtentRedundancyComponent**](cim-pextentredundancycomponent.md)
</dt> <dd>

A [**classe CIM \_ PExtentRedundancyComponent**](cim-pextentredundancycomponent.md) representa as extensão físicas que participam de um grupo de redundância de armazenamento.

</dd> <dt>

[**CIM \_ PhysicalCapacity**](cim-physicalcapacity.md)
</dt> <dd>

A [**classe Cim \_ PhysicalCapacity**](cim-physicalcapacity.md) é uma classe abstrata que representa os requisitos mínimos e máximos de um elemento físico e sua capacidade de dar suporte a diferentes tipos de hardware. Por exemplo, requisitos mínimos e máximos de memória podem ser modelados como uma **subclasse de Cim \_ PhysicalCapacity**.

</dd> <dt>

[**CIM \_ PhysicalComponent**](cim-physicalcomponent.md)
</dt> <dd>

A [**classe \_ PhysicalComponent cim**](cim-physicalcomponent.md) representa um componente básico ou de baixo nível dentro de um pacote. Um elemento físico que não é um link, conector ou pacote é um descendente (ou membro) dessa classe.

</dd> <dt>

[**CIM \_ PhysicalConnector**](cim-physicalconnector.md)
</dt> <dd>

A [**classe \_ Cim PhysicalConnector**](cim-physicalconnector.md) representa qualquer elemento físico usado para se conectar a outros elementos. Qualquer objeto que possa se conectar e transmitir sinais ou energia entre dois ou mais elementos físicos é um descendente (ou membro) dessa classe.

</dd> <dt>

[**CIM \_ PhysicalElement**](cim-physicalelement.md)
</dt> <dd>

As [**subclasses CIM \_ PhysicalElement**](cim-physicalelement.md) definem qualquer componente de um sistema que tenha uma identidade física distinta. Instâncias dessa classe podem ser definidas em termos de rótulos que podem ser fisicamente anexados ao objeto .

</dd> <dt>

[**CIM \_ PhysicalElementLocation**](cim-physicalelementlocation.md)
</dt> <dd>

A [**classe \_ CIM PhysicalElementLocation**](cim-physicalelementlocation.md) associa um elemento físico a um objeto [**Local CIM \_**](cim-location.md) para fins de inventário ou substituição.

</dd> <dt>

[**CIM \_ PhysicalExtent**](cim-physicalextent.md)
</dt> <dd>

A [**classe \_ Cim PhysicalExtent**](cim-physicalextent.md) representa uma implementação raid SCC. Ele define os endereços de bloco enderecáveis consecutivos em um único dispositivo de armazenamento que são tratados como uma única extensão de armazenamento na mesma [**classe CIM \_ StorageRedundancyGroup.**](cim-storageredundancygroup.md) Uma alternativa, quando a configuração automática é usada, é insinuar ou estender a [**classe \_ AGGREGATEPExtent cim.**](cim-aggregatepextent.md)

</dd> <dt>

[**CIM \_ PhysicalFrame**](cim-physicalframe.md)
</dt> <dd>

A [**classe CIM \_ PhysicalFrame**](cim-physicalframe.md) é uma classe pai de rack, chassi e outros compartimentos de quadro conforme eles são definidos em classes de extensão. Propriedades como **VisibleAlarm** e **VisibleAlarm** e dados relacionados a violações de segurança são incluídos nessa classe pai.

</dd> <dt>

[**CIM \_ PhysicalLink**](cim-physicallink.md)
</dt> <dd>

A [**classe \_ Cim PhysicalLink**](cim-physicallink.md) representa o cabeamento de elementos físicos.

</dd> <dt>

[**CIM \_ PhysicalMedia**](cim-physicalmedia.md)
</dt> <dd>

A [**classe CIM \_ PhysicalMedia**](cim-physicalmedia.md) representa tipos de documentação e mídia de armazenamento, como fitas, ROMs de CD e assim por diante.

</dd> <dt>

[**CIM \_ PhysicalMemory**](cim-physicalmemory.md)
</dt> <dd>

A [**classe \_ Cim PhysicalMemory**](cim-physicalmemory.md) representa dispositivos de memória de baixo nível, comoLF, DIMMs, chips de memória brutos e assim por diante.

</dd> <dt>

[**CIM \_ PhysicalPackage**](cim-physicalpackage.md)
</dt> <dd>

A [**classe \_ Cim PhysicalPackage**](cim-physicalpackage.md) representa elementos físicos que contêm ou hospedam outros componentes. Exemplos são um compartimento de rack ou uma placa de adaptador.

</dd> <dt>

[**CIM \_ PointingDevice**](cim-pointingdevice.md)
</dt> <dd>

A [**classe CIM \_ PointingDevice**](cim-pointingdevice.md) representa um dispositivo que aponta para regiões na exibição. Qualquer dispositivo que manipula um ponteiro ou aponta para regiões em uma exibição visual é um membro dessa classe. Por exemplo, um mouse, caneta, painel de toque ou tablet.

</dd> <dt>

[**CIM \_ POTSModem**](cim-potsmodem.md)
</dt> <dd>

A [**classe CIM \_ POTSModem**](cim-potsmodem.md) representa um dispositivo que converte dados binários em modulares de onda para transmissão baseada em som conectando-se à rede DOLS (Plain Old Telephone System).

</dd> <dt>

[**CIM \_ PowerSupply**](cim-powersupply.md)
</dt> <dd>

A [**classe CIM \_ PowerSupply**](cim-powersupply.md) representa os recursos e o gerenciamento do dispositivo lógico de fonte de alimentação.

</dd> <dt>

[**Impressora \_ CIM**](cim-printer.md)
</dt> <dd>

A [**\_ classe Impressora CIM**](cim-printer.md) representa os recursos e o gerenciamento do dispositivo lógico da impressora.

</dd> <dt>

[**Processo \_ CIM**](cim-process.md)
</dt> <dd>

A [**classe \_ Processo CIM**](cim-process.md) representa uma única instância de um programa em execução. Um usuário normalmente vê um processo como um aplicativo ou tarefa.

</dd> <dt>

[**CIM \_ ProcessExecutable**](cim-processexecutable.md)
</dt> <dd>

A [**classe CIM \_ ProcessExecutable**](cim-processexecutable.md) representa um vínculo entre um processo e um arquivo de dados e indica que o arquivo participa da execução do processo.

</dd> <dt>

[**Processador \_ CIM**](cim-processor.md)
</dt> <dd>

A [**classe \_ processador CIM**](cim-processor.md) representa os recursos e o gerenciamento do dispositivo lógico do processador.

</dd> <dt>

[**Processo \_ CIMThread**](cim-processthread.md)
</dt> <dd>

A [**classe \_ PROCESSThread cim**](cim-processthread.md) representa um link entre um processo e os threads em execução no contexto do processo.

</dd> <dt>

[**Produto \_ CIM**](cim-product.md)
</dt> <dd>

A [**classe \_ Produto CIM**](cim-product.md) é uma classe concreta que representa uma coleção de elementos físicos, recursos de software e, outros produtos, adquiridos como uma unidade. A aquisição implica um contrato entre o fornecedor e o consumidor, que pode ter implicações no licenciamento, no suporte e na garantia do produto.

</dd> <dt>

[**CIM \_ ProductFRU**](cim-productfru.md)
</dt> <dd>

A [**classe Cim \_ ProductFRU**](cim-productfru.md) representa uma associação entre o produto e uma UNIDADE substituível por campo (FRU), que fornece informações sobre os componentes do produto que foram ou estão sendo substituídos.

</dd> <dt>

[**CIM \_ ProductParentChild**](cim-productparentchild.md)
</dt> <dd>

A [**associação CIM \_ ProductParentChild**](cim-productparentchild.md) define uma hierarquia pai-filho entre produtos. Por exemplo, um produto pode ser empacotado com outros produtos.

</dd> <dt>

[**CIM \_ ProductPhysicalElements**](cim-productphysicalelements.md)
</dt> <dd>

A [**classe CIM \_ ProductPhysicalElements**](cim-productphysicalelements.md) representa os elementos físicos que comem um produto.

</dd> <dt>

[**CIM \_ ProductProductDependency**](cim-productproductdependency.md)
</dt> <dd>

A [**classe CIM \_ ProductProductDependency**](cim-productproductdependency.md) representa uma associação entre dois produtos, que indica que um deve ser instalado ou ausente para que o outro funcione. Isso é conceitualmente equivalente à associação [**CIM \_ ServiceServiceDependency.**](cim-serviceservicedependency.md)

</dd> <dt>

[**CIM \_ ProductSoftwareFeatures**](cim-productsoftwarefeatures.md)
</dt> <dd>

A [**associação CIM \_ ProductSoftwareFeatures**](cim-productsoftwarefeatures.md) identifica os recursos de software para um produto específico.

</dd> <dt>

[**CIM \_ ProductSupport**](cim-productsupport.md)
</dt> <dd>

A [**classe CIM \_ ProductSupport**](cim-productsupport.md) representa uma associação entre o produto e o acesso de suporte que transmite como o suporte é obtido para o produto. Vários tipos de suporte estão disponíveis para um produto; O mesmo objeto de suporte pode fornecer assistência para vários produtos.

</dd> <dt>

[**CIM \_ ProtectedSpaceExtent**](cim-protectedspaceextent.md)
</dt> <dd>

A [**classe CIM \_ ProtectedSpaceExtent**](cim-protectedspaceextent.md) representa endereços de bloco lógico enderecáveis, que são tratados como uma única extensão de armazenamento, mas estão localizados em uma única extensão física.

</dd> <dt>

[**CIM \_ PSExtentBasedOnPExtent**](cim-psextentbasedonpextent.md)
</dt> <dd>

A [**classe CIM \_ PSExtentBasedOnPExtent**](cim-psextentbasedonpextent.md) associa as extensão de espaço protegida baseadas em uma extensão física.

</dd> <dt>

[**CIM \_ Rack**](cim-rack.md)
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

A classe [**CIM \_ Statistics**](cim-statistics.md) representa uma associação que relaciona os elementos do sistema gerenciado aos grupos estatísticos que se aplicam a eles.

</dd> <dt>

[**\_STORAGEDEFECT CIM**](cim-storagedefect.md)
</dt> <dd>

A agregação [**CIM \_ StorageDefect**](cim-storagedefect.md) coleta os erros de armazenamento para uma extensão de armazenamento.

</dd> <dt>

[**\_STORAGEERROR CIM**](cim-storageerror.md)
</dt> <dd>

A classe [**CIM \_ StorageError**](cim-storageerror.md) representa blocos de mídia ou espaço de memória que são mapeados fora de uso devido a erros. A chave da classe é a propriedade **StartingAddress** dos bytes em erro.

</dd> <dt>

[**\_STORAGEEXTENT CIM**](cim-storageextent.md)
</dt> <dd>

A classe [**CIM \_ StorageExtent**](cim-storageextent.md) representa os recursos e o gerenciamento de várias mídias que existem para armazenar dados e permitir a recuperação de dados. Essa classe pai pode representar os vários componentes de RAID (hardware ou software) ou uma extensão lógica bruta na parte superior da mídia física.

</dd> <dt>

[**\_STORAGEREDUNDANCYGROUP CIM**](cim-storageredundancygroup.md)
</dt> <dd>

A classe [**CIM \_ StorageRedundancyGroup**](cim-storageredundancygroup.md) representa informações de redundância relacionadas ao armazenamento em massa.

</dd> <dt>

[**\_SUPPORTACCESS CIM**](cim-supportaccess.md)
</dt> <dd>

A classe [**CIM \_ SupportAccess**](cim-supportaccess.md) define como obter assistência para um produto.

</dd> <dt>

[**\_SWAPSPACECHECK CIM**](cim-swapspacecheck.md)
</dt> <dd>

A classe [**CIM \_ SwapSpaceCheck**](cim-swapspacecheck.md) especifica a quantidade de espaço de permuta que deve estar disponível no sistema.

</dd> <dt>

[**\_Sistema CIM**](cim-system.md)
</dt> <dd>

A classe de [**\_ sistema CIM**](cim-system.md) agrega um conjunto enumerável de elementos do sistema gerenciado. A agregação funciona como um todo funcional. Em qualquer subclasse específica do sistema, há uma lista bem definida de classes de elementos do sistema gerenciado cujas instâncias devem ser agregadas.

</dd> <dt>

[**\_SYSTEMCOMPONENT CIM**](cim-systemcomponent.md)
</dt> <dd>

uma classe de associação de modelo CIM (CIM) que estabelece relações entre um sistema e os elementos do sistema gerenciado dos quais ele é composto.

</dd> <dt>

[**\_SYSTEMDEVICE CIM**](cim-systemdevice.md)
</dt> <dd>

A associação [**CIM \_ SystemDevice**](cim-systemdevice.md) representa uma relação explícita na qual os dispositivos lógicos podem ser agregados por um sistema.

</dd> <dt>

[**\_SYSTEMRESOURCE CIM**](cim-systemresource.md)
</dt> <dd>

A classe [**CIM \_ SystemResource**](cim-systemresource.md) representa uma entidade gerenciada pelo BIOS ou um sistema operacional que está disponível para uso por software e dispositivos lógicos.

</dd> <dt>

[**\_Tacômetro CIM**](cim-tachometer.md)
</dt> <dd>

A classe do [**\_ tacômetro CIM**](cim-tachometer.md) existe para compatibilidade com versões anteriores de definições de esquema CIM.

</dd> <dt>

[**\_TAPEDRIVE CIM**](cim-tapedrive.md)
</dt> <dd>

A classe [**CIM \_ TapeDrive**](cim-tapedrive.md) representa uma unidade de fita no sistema. As unidades de fita são basicamente diferenciadas, pois só podem ser acessadas sequencialmente.

</dd> <dt>

[**\_Sensor CIM**](cim-temperaturesensor.md)
</dt> <dd>

A classe [**CIM \_ sensor**](cim-temperaturesensor.md) existe para compatibilidade com versões anteriores de definições de esquema CIM.

</dd> <dt>

[**\_Thread CIM**](cim-thread.md)
</dt> <dd>

A classe de [**\_ thread CIM**](cim-thread.md) representa a capacidade de executar unidades de um processo ou tarefa, em paralelo. Um processo pode ter muitos threads, cada um dos quais é fraco para o processo.

</dd> <dt>

[**CIM \_ Todirectoryaction**](cim-todirectoryaction.md)
</dt> <dd>

A associação [**CIM \_ todirectoryaction**](cim-todirectoryaction.md) identifica o diretório de destino para a ação de arquivo.

</dd> <dt>

[**\_TODIRECTORYSPECIFICATION CIM**](cim-todirectoryspecification.md)
</dt> <dd>

A associação [**CIM \_ ToDirectorySpecification**](cim-todirectoryspecification.md) identifica o diretório de destino para a ação de arquivo.

</dd> <dt>

[**\_UNINTERRUPTIBLEPOWERSUPPLY CIM**](cim-uninterruptiblepowersupply.md)
</dt> <dd>

A classe [**CIM \_ UninterruptiblePowerSupply**](cim-uninterruptiblepowersupply.md) representa os recursos e o gerenciamento de uma fonte de energia ininterrupta (UPS).

</dd> <dt>

[**\_UNITARYCOMPUTERSYSTEM CIM**](cim-unitarycomputersystem.md)
</dt> <dd>

A classe [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md) representa um computador desktop, móvel, de rede, servidor ou outro tipo de sistema de computador de nó único.

</dd> <dt>

[**\_USBCONTROLLER CIM**](cim-usbcontroller.md)
</dt> <dd>

A classe [**CIM \_ USBController**](cim-usbcontroller.md) representa os recursos e o gerenciamento de um controlador USB.

</dd> <dt>

[**\_USBCONTROLLERHASHUB CIM**](cim-usbcontrollerhashub.md)
</dt> <dd>

A classe [**CIM \_ USBControllerHasHub**](cim-usbcontrollerhashub.md) define os hubs que são DOWNSTREAM do controlador USB.

</dd> <dt>

[**\_USBDEVICE CIM**](cim-usbdevice.md)
</dt> <dd>

A classe [**CIM \_ UsbDevice**](cim-usbdevice.md) representa as características de gerenciamento de um dispositivo USB.

</dd> <dt>

[**CIM \_ USBHub**](cim-usbhub.md)
</dt> <dd>

A classe [**CIM \_ USBHub**](cim-usbhub.md) representa os recursos e o gerenciamento de um hub USB.

</dd> <dt>

[**Userdevice do CIM \_**](cim-userdevice.md)
</dt> <dd>

A classe [**CIM \_ userdevice**](cim-userdevice.md) é uma classe pai da qual outras classes, como o [**CIM \_ Keyboard**](cim-keyboard.md) ou [**CIM \_ DesktopMonitor**](cim-desktopmonitor.md), descendem. Os dispositivos de usuário são dispositivos lógicos que permitem que o usuário de um sistema de computador insira, exiba ou Ouça dados.

</dd> <dt>

[**\_VERSIONCOMPATIBILITYCHECK CIM**](cim-versioncompatibilitycheck.md)
</dt> <dd>

A classe [**CIM \_ VersionCompatibilityCheck**](cim-versioncompatibilitycheck.md) especifica se é permitido criar o próximo estado de um elemento de software.

</dd> <dt>

[**\_VIDEOBIOSELEMENT CIM**](cim-videobioselement.md)
</dt> <dd>

A classe [**CIM \_ VideoBIOSElement**](cim-videobioselement.md) representa o software de nível baixo que é carregado no armazenamento não volátil e usado para configurar e acessar o controlador de vídeo de um sistema de computador e exibi-lo.

</dd> <dt>

[**\_VIDEOBIOSFEATURE CIM**](cim-videobiosfeature.md)
</dt> <dd>

A classe [**CIM \_ VideoBIOSFeature**](cim-videobiosfeature.md) representa os recursos do software de baixo nível usado para configurar e acessar o controlador de vídeo de um sistema de computador e exibir o.

</dd> <dt>

[**\_VIDEOBIOSFEATUREVIDEOBIOSELEMENTS CIM**](cim-videobiosfeaturevideobioselements.md)
</dt> <dd>

A classe [**CIM \_ VideoBIOSFeatureVideoBIOSElements**](cim-videobiosfeaturevideobioselements.md) associa um recurso de BIOS de vídeo e seus elementos de BIOS de vídeo agregados.

</dd> <dt>

[**\_VIDEOCONTROLLER CIM**](cim-videocontroller.md)
</dt> <dd>

A classe [**CIM \_ VideoController**](cim-videocontroller.md) representa os recursos e o gerenciamento do controlador de vídeo.

</dd> <dt>

[**\_VIDEOCONTROLLERRESOLUTION CIM**](cim-videocontrollerresolution.md)
</dt> <dd>

A classe [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md) representa os vários modos de vídeo aos quais um controlador de vídeo pode dar suporte.

</dd> <dt>

[**\_VIDEOSETTING CIM**](cim-videosetting.md)
</dt> <dd>

A classe [**CIM \_ VideoSetting**](cim-videosetting.md) associa o objeto de configuração [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md) ao controlador ao qual ele se aplica.

</dd> <dt>

[**\_VOLATILESTORAGE CIM**](cim-volatilestorage.md)
</dt> <dd>

A classe [**CIM \_ VolatileStorage**](cim-volatilestorage.md) representa os recursos e o gerenciamento do armazenamento volátil.

</dd> <dt>

[**\_Voltagem CIM**](cim-voltagesensor.md)
</dt> <dd>

A classe [**CIM \_ voltagem**](cim-voltagesensor.md) existe para compatibilidade com versões anteriores de definições de esquema CIM. Com adições às classes [**do \_ sensor CIM**](cim-sensor.md) e do [**cim \_ NumericSensor**](cim-numericsensor.md) na versão 2,2, ela não é mais necessária.

</dd> <dt>

[**\_Volumeset CIM**](cim-volumeset.md)
</dt> <dd>

A classe [**CIM \_ volumeset**](cim-volumeset.md) representa um intervalo contíguo de blocos lógicos apresentados ao ambiente operacional para leitura e gravação de dados do usuário.

</dd> <dt>

[**\_WORMDRIVE CIM**](cim-wormdrive.md)
</dt> <dd>

A classe [**CIM \_ WORMDrive**](cim-wormdrive.md) representa os recursos e o gerenciamento de uma unidade de worm, um subtipo do dispositivo de acesso à mídia.

</dd> </dl>

 

 
