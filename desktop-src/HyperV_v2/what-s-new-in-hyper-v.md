---
description: a versão 2 do provedor WMI do Hyper-V é nova para Windows 8 e Windows Server 2012.
ms.assetid: A91ACF7A-AFE6-45B6-960C-C4AAA0083735
title: O que há de novo no provedor WMI do Hyper-V
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbaab65c08031c291eb11e8f865b77e256e5600deba060e0f8176ec8d13c3714
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754926"
---
# <a name="whats-new-in-hyper-v-wmi-provider"></a>O que há de novo no provedor WMI do Hyper-V

a versão 2 do provedor WMI do Hyper-V é nova para Windows 8 e Windows Server 2012.

## <a name="windows-10-version-1709"></a>Windows 10, versão 1709

Novas classes:

-   [**\_Bateria Msvm**](msvm-battery.md)
-   [**Msvm \_ BatterySettingData**](msvm-batterysettingdata.md)
-   [**Msvm \_ PersistentMemoryController**](msvm-persistentmemorycontroller.md)

Propriedades novas:

-   [**Msvm \_ CollectionReferencePointExportJob**](msvm-collectionreferencepointexportjob.md): **ExportedGuestStateFilePaths**
-   [**Msvm \_ EthernetSwitchHardwareOffloadData**](msvm-ethernetswitchhardwareoffloaddata.md): **DefaultQueueVrssIndependentHostSpreading**, **DefaultQueueVrssExcludePrimaryProcessor**, **DefaultQueueVrssQueueSchedulingMode** e **DefaultQueueVrssMinQueuePairs**
-   [**Msvm \_ EthernetSwitchHardwareOffloadSettingData**](msvm-ethernetswitchhardwareoffloadsettingdata.md): **DefaultQueueVrssIndependentHostSpreading**, **DefaultQueueVrssExcludePrimaryProcessor**, **DefaultQueueVrssQueueSchedulingMode**, **DefaultQueueVrssMinQueuePairs**,
-   [**Msvm \_ EthernetSwitchPortOffloadData**](msvm-ethernetswitchportoffloaddata.md): **VrssVmbusChannelAffinityPolicy**, **VrssIndependentHostSpreading**, **VrssExcludePrimaryProcessor**, **VrssQueueSchedulingModes** e **VrssMinQueuePairs**
-   [**Msvm \_ VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md): **dataalignment**, **PmemAddressAbstractionType** e **IsPmemCompatible**
-   [**Msvm \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md): **DisableDifferentialOfIgnoredStorage** e **ExcludedVirtualHardDisks**
-   [**Msvm \_ VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md): **HypervisorRootSchedulerEnabled**
-   [**Msvm \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md): **CPUCappingMagnitude** e **CancelIfBlackoutThresholdExceeded**
-   [**Msvm \_ VirtualSystemReferencePointExportJob**](msvm-virtualsystemreferencepointexportjob.md): **ExportedGuestStateFilePath**
-   [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md): **arquitetura**, **AutomaticSnapshotsEnabled**, **IsAutomaticSnapshot**, **GuestStateFile** e **GuestStateDataRoot**

## <a name="windows-10-version-1703"></a>Windows 10, versão 1703

Novas classes:

-   [**Msvm \_ AssignableDeviceDismountSettingData**](msvm-assignabledevicedismountsettingdata.md)
-   [**Msvm \_ AssignableDeviceService**](msvm-assignabledeviceservice.md)
-   [**Msvm \_ CollectionReferencePointExportJob**](msvm-collectionreferencepointexportjob.md)
-   [**Msvm \_ EthernetSwitchHardwareOffloadSettingData**](msvm-ethernetswitchhardwareoffloadsettingdata.md)
-   [**Msvm \_ EthernetSwitchPortMigrationQosSettingData**](msvm-ethernetswitchportmigrationqossettingdata.md)
-   [**Msvm \_ EthernetSwitchPortRdmaSettingData**](msvm-ethernetswitchportrdmasettingdata.md)
-   [**Msvm \_ EthernetSwitchPortTeamMappingSettingData**](msvm-ethernetswitchportteammappingsettingdata.md)
-   [**Msvm \_ GpuPartition**](msvm-gpupartition.md)
-   [**Msvm \_ GpuPartitionSettingData**](msvm-gpupartitionsettingdata.md)
-   [**Msvm \_ NetworkConnectionDiagnosticInformation**](msvm-networkconnectiondiagnosticinformation.md)
-   [**Msvm \_ NetworkConnectionDiagnosticSettingData**](msvm-networkconnectiondiagnosticsettingdata.md)
-   [**Msvm \_ PartitionableGpu**](msvm-partitionablegpu.md)
-   [**Msvm \_ PciExpress**](msvm-pciexpress.md)
-   [**Msvm \_ PciExpressSettingData**](msvm-pciexpresssettingdata.md)
-   [**Msvm \_ SecurityElement**](msvm-securityelement.md)
-   [**Msvm \_ SecurityService**](msvm-securityservice.md)
-   [**Msvm \_ SecuritySettingData**](msvm-securitysettingdata.md)
-   [**Msvm \_ StorageSettingData**](msvm-storagesettingdata.md)
-   [**Msvm \_ SummaryInformationBase**](msvm-summaryinformationbase.md)
-   [**Msvm \_ SystemComponentSettingData**](msvm-systemcomponentsettingdata.md)
-   [**Msvm \_ VirtualSystemReferencePointExportJob**](msvm-virtualsystemreferencepointexportjob.md)
-   [**Msvm \_ VirtualSystemReferencePointSettingData**](msvm-virtualsystemreferencepointsettingdata.md)

Classes removidas:

-   [**Msvm \_ TPMSettingData**](msvm-tpmsettingdata.md)

Novos métodos:

-   [**Msvm \_ Classe CollectionSnapshotService**](msvm-collectionsnapshotservice.md) : [ **ApplySnapshot**](msvm-collectionsnapshotservice-applysnapshot.md)
-   [**Msvm \_ Classe VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) : [**AddSystemComponentSetting**](msvm-virtualsystemmanagementservice-addsystemcomponentsettings.md), [**DiagnoseNetworkConnection**](msvm-virtualsystemmanagementservice-diagnosenetworkconnection.md), [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md)e [**RemoveSystemComponentSettings**](msvm-virtualsystemmanagementservice-removesystemcomponentsettings.md)
-   [**Msvm \_ Classe VirtualSystemReferencePointService**](msvm-virtualsystemreferencepointservice.md) : [ **ImportReferencePointMetadata**](msvm-virtualsystemreferencepointservice-importreferencepointmetadata.md)

Propriedades novas:

-   [**Msvm \_ EthernetSwitchHardwareOffloadData**](msvm-ethernetswitchhardwareoffloaddata.md): **DefaultQueueVmmqQueuePairs**, **DefaultQueueVmmqEnabled** e **DefaultQueueVrssEnabled**
-   [**Msvm \_ EthernetSwitchPortOffloadData**](msvm-ethernetswitchportoffloaddata.md): **VmmqQueuePairs**, **VmmqEnabled** e **VrssEnabled**
-   [**Msvm \_ EthernetSwitchPortOffloadSettingData**](msvm-ethernetswitchportoffloadsettingdata.md): **VmmqQueuePairs**, **VmmqEnabled** e **VrssEnabled**
-   [**Msvm \_ GuestClusterInformation**](msvm-guestclusterinformation.md): **LastResourceMoveTime**
-   [**Msvm \_ KvpExchangeComponentSettingData**](msvm-kvpexchangecomponentsettingdata.md): **DisableHostKVPItems**
-   [**Msvm \_ MemorySettingData**](msvm-memorysettingdata.md): **SgxSize** e **SgxEnabled**
-   [**Msvm \_ Physical3dGraphicsProcessor**](msvm-physical3dgraphicsprocessor.md): **CompatibleForVirtualization** e **DriverModelVersion**
-   [**Msvm \_ ProcessorSettingData**](msvm-processorsettingdata.md): **HwThreadsPerCoreCpuGroupId**, **HideHypervisorPresent** e **ExposeVirtualizationExtensions**
-   [**Msvm \_ SettingsDefineCapabilities**](msvm-settingsdefinecapabilities.md): **SupportStatement**
-   [**Msvm \_ StorageAllocationSettingData**](msvm-storageallocationsettingdata.md): **WriteHardeningMethod**
-   [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md): **blindado**
-   [**Msvm \_ SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md): **AllowPacketDirect**
-   [**Msvm \_ VirtualSystemCollection**](msvm-virtualsystemcollection.md): **LastApplyConsistencyLevel**, **LastApplyVirtualMachineIds**, **LastApplyTime**, **FailedOverReplicationType**, **replicationmode** e **replicationstate**
-   [**Msvm \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md): **ExportForLiveMigration**
-   [**Msvm \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md): **AvoidRemovingVHDs** e **AllowOverwriteExistingFile**
-   [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md): **HighMmioGapSize**
-   [**Msvm \_ VirtualSystemSnapshotSettingData**](msvm-virtualsystemsnapshotsettingdata.md): **GuestBackupType**

Propriedades removidas:

-   [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md): **ParentPackage**

## <a name="windows-10"></a>Windows 10

Novas classes:

-   [**\_COLLECTEDMSES CIM**](cim-collectedmses.md)
-   [**\_Coleção CIM**](cim-collection.md)
-   [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md)
-   [**\_ELEMENTVIEW CIM**](cim-elementview.md)
-   [**\_MEMBEROFCOLLECTION CIM**](cim-memberofcollection.md)
-   [**\_TPM CIM**](cim-tpm.md)
-   [**Exibição de CIM \_**](cim-view.md)
-   [**Msvm \_ CollectedCollections**](msvm-collectedcollections.md)
-   [**Msvm \_ CollectedReferencePoints**](msvm-collectedreferencepoints.md)
-   [**Msvm \_ CollectedSnapshots**](msvm-collectedsnapshots.md)
-   [**Msvm \_ CollectedVirtualSystems**](msvm-collectedvirtualsystems.md)
-   [**Msvm \_ CollectionManagementService**](msvm-collectionmanagementservice.md)
-   [**Msvm \_ CollectionReferencePointExportSettingData**](msvm-collectionreferencepointexportsettingdata.md)
-   [**Msvm \_ CollectionReferencePointService**](msvm-collectionreferencepointservice.md)
-   [**Msvm \_ CollectionReferencePointSettingData**](msvm-collectionreferencepointsettingdata.md)
-   [**Msvm \_ CollectionSettingData**](msvm-collectionsettingdata.md)
-   [**Msvm \_ CollectionSnapshotExportSettingData**](msvm-collectionsnapshotexportsettingdata.md)
-   [**Msvm \_ CollectionSnapshotService**](msvm-collectionsnapshotservice.md)
-   [**Msvm \_ ComputerSystemSummaryInformation**](msvm-computersystemsummaryinformation.md)
-   [**Msvm \_ EthernetSwitchPortVfpSettingData**](msvm-ethernetswitchportvfpsettingdata.md)
-   [**Msvm \_ GuestClusterInformation**](msvm-guestclusterinformation.md)
-   [**Msvm \_ GuestCommunicationService**](msvm-guestcommunicationservice.md)
-   [**Msvm \_ GuestCommunicationServiceSettingData**](msvm-guestcommunicationservicesettingdata.md)
-   [**Msvm \_ GuestServiceInterfaceSettingDataComponent**](msvm-guestserviceinterfacesettingdatacomponent.md)
-   [**Msvm \_ managementcollection**](msvm-managementcollection.md)
-   [**Msvm \_ MoveUnmanagedVhd**](msvm-moveunmanagedvhd.md)
-   [**Msvm \_ ReferencePointCollection**](msvm-referencepointcollection.md)
-   [**Msvm \_ ReferencePointOfVirtualSystem**](msvm-referencepointofvirtualsystem.md)
-   [**Msvm \_ ReferencePointOfVirtualSystemCollection**](msvm-referencepointofvirtualsystemcollection.md)
-   [**Msvm \_ ResourceDependentOnResource**](msvm-resourcedependentonresource.md)
-   [**Msvm \_ SerialPortSettingData**](msvm-serialportsettingdata.md)
-   [**Msvm \_ ServiceOfVssComponent**](msvm-serviceofvsscomponent.md)
-   [**Msvm \_ instantâneocollection**](msvm-snapshotcollection.md)
-   [**Msvm \_ SnapshotOfVirtualSystemCollection**](msvm-snapshotofvirtualsystemcollection.md)
-   [**Msvm \_ StandaloneV2ElementConformsToProfile**](msvm-standalonev2elementconformstoprofile.md)
-   [**Msvm \_ SyntheticDisplayControllerSettingData**](msvm-syntheticdisplaycontrollersettingdata.md)
-   [**Msvm \_ SyntheticKeyboard**](msvm-synthetickeyboard.md)
-   [**TPM do Msvm \_**](msvm-tpm.md)
-   [**Msvm \_ TPMSettingData**](msvm-tpmsettingdata.md)
-   [**Msvm \_ VHDSetInformation**](msvm-vhdsetinformation.md)
-   [**Msvm \_ VHDSnapshotInformation**](msvm-vhdsnapshotinformation.md)
-   [**Msvm \_ VirtualEthernetSwitchNicTeamingMember**](msvm-virtualethernetswitchnicteamingmember.md)
-   [**Msvm \_ VirtualEthernetSwitchNicTeamingSettingData**](msvm-virtualethernetswitchnicteamingsettingdata.md)
-   [**Msvm \_ VirtualMachineToDisks**](msvm-virtualmachinetodisks.md)
-   [**Msvm \_ VirtualSystemCollection**](msvm-virtualsystemcollection.md)
-   [**Msvm \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md)
-   [**Msvm \_ VirtualSystemReferencePointExportSettingData**](msvm-virtualsystemreferencepointexportsettingdata.md)
-   [**Msvm \_ VirtualSystemReferencePointService**](msvm-virtualsystemreferencepointservice.md)
-   [**Msvm \_ VirtualSystemReferencePointSettingData**](msvm-virtualsystemreferencepointsettingdata.md)
-   [**Msvm \_ VirtualSystemSnapshotSettingData**](msvm-virtualsystemsnapshotsettingdata.md)
-   [**Msvm \_ VssService**](msvm-vssservice.md)

Classe removida:

-   [**Msvm \_ ResourcePoolComponent**](msvm-resourcepoolcomponent.md)
-   [**Msvm \_ ResourcePoolRegistration**](msvm-resourcepoolregistration.md)
-   [**Msvm \_ ResourcePoolSettingData**](msvm-resourcepoolsettingdata.md)
-   [**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)
-   [**Msvm \_ VirtualizationComponentRegistration**](msvm-virtualizationcomponentregistration.md)

Propriedades novas:

-   [**Msvm \_ BootSourceSettingData**](msvm-bootsourcesettingdata.md): **OptionalData**
-   [**Msvm \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md): **LastKnownSwitchName** e **CompartmentGuid**
-   [**Msvm \_ EthernetSwitchHardwareOffloadData**](msvm-ethernetswitchhardwareoffloaddata.md): **PacketDirectInUse**
-   [**Msvm \_ EthernetSwitchPortOffloadSettingData**](msvm-ethernetswitchportoffloadsettingdata.md): **PacketDirectModerationInterval**, **PacketDirectModerationCount**, **PacketDirectNumProcs**,
-   [**Msvm \_ EthernetSwitchPortSecuritySettingData**](msvm-ethernetswitchportsecuritysettingdata.md): **EnableFixSpeed10G** e **reservado**
-   [**Msvm \_ GuestServiceInterfaceComponentSettingData**](msvm-guestserviceinterfacecomponentsettingdata.md): **DefaultEnabledStatePolicy**
-   [**Msvm \_ ProcessorSettingData**](msvm-processorsettingdata.md): **EnableHostResourceProtection**
-   [**Msvm \_ StorageAllocationSettingData**](msvm-storageallocationsettingdata.md): **StorageQoSPolicyID**, **cachingmode** e **snapshotid**
-   [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md): **InstanceId**, **version**, **ThumbnailImageHeight**, **ThumbnailImageWidth** e **HostComputerSystemName**
-   [**Msvm \_ Synthetic3DDisplayControllerSettingData**](msvm-synthetic3ddisplaycontrollersettingdata.md): **VRAMSizeBytes**
-   [**Msvm \_ VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md): **TeamingEnabled** e **PacketDirectEnabled**
-   [**Msvm \_ VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md): **ParentTimestamp** e **ParentIdentifier**
-   [**Msvm \_ VirtualHardDiskState**](msvm-virtualharddiskstate.md): **carimbo de data/hora**
-   [**Msvm \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md): **BackupIntent** e **DifferentialBackupBase**
-   [**Msvm \_ VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md): **DefaultVirtualHardDiskCachingMode**
-   [**Msvm \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md): **RemoveSourceUnmanagedVhds** e **UnmanagedVhds**
-   [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md): **userinstantâneotype**, **GuestControlledCacheTypes**, **LockOnDisconnect**, **ParentPackage**, **AutomaticCriticalErrorActionTimeout**, **AutomaticCriticalErrorAction**, **consolemode** e **SecureBootTemplateId**

Novos métodos:

-   [**Msvm \_ Classe imagens**](msvm-imagemanagementservice.md) : [**ConvertVirtualHardDiskToVHDSet**](msvm-imagemanagementservice-convertvirtualharddisktovhdset.md), [**DeleteVHDSnapshot**](msvm-imagemanagementservice-deletevhdsnapshot.md), [**FindMountedStorageImageInstance**](msvm-imagemanagementservice-findmountedstorageimageinstance.md), [**GetVHDSetInformation**](msvm-imagemanagementservice-getvhdsetinformation.md), [**GetVHDSnapshotInformation**](msvm-imagemanagementservice-getvhdsnapshotinformation.md), [**GetVirtualDiskChanges**](msvm-imagemanagementservice-getvirtualdiskchanges.md), [**OptimizeVHDSet**](msvm-imagemanagementservice-optimizevhdset.md)e [**SetVHDSnapshotInformation**](msvm-imagemanagementservice-setvhdsnapshotinformation.md)
-   [**Msvm \_ Classe ShutdownComponent**](msvm-shutdowncomponent.md) : [ **InitiateReboot**](msvm-shutdowncomponent-initiatereboot.md)
-   [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md): [**AddBootSourceSettings**](msvm-virtualsystemmanagementservice-addbootsourcesettings.md), [**AddGuestServiceSettings**](msvm-virtualsystemmanagementservice-addguestservicesettings.md), [**DefinePlannedSystem**](msvm-virtualsystemmanagementservice-defineplannedsystem.md), [**ModifyGuestServiceSettings**](msvm-virtualsystemmanagementservice-modifyguestservicesettings.md), [**RemoveBootSourceSettings**](msvm-virtualsystemmanagementservice-removebootsourcesettings.md), [**RemoveGuesServiceSettings**](msvm-virtualsystemmanagementservice-removeguestservicesettings.md), [**SetInitialMachineConfigurationData**](msvm-virtualsystemmanagementservice-setinitialmachineconfigurationdata.md)e [**UpgradeSystemVersion**](msvm-virtualsystemmanagementservice-upgradesystemversion.md)
-   [**Msvm \_ Classe VirtualSystemSnapshotService**](msvm-virtualsystemsnapshotservice.md) : [ **ConvertToReferencePoint**](msvm-virtualsystemsnapshotservice-converttoreferencepoint.md)

## <a name="windows-81-and-windows-server-2012-r2"></a>Windows 8.1 e Windows Server 2012 R2

Windows 8.1 e Windows Server 2012 R2 incluem uma nova funcionalidade para a versão 2 do provedor WMI do Hyper-V.

-   As propriedades **IOPSAllocationUnits**, **IOPSLimit**, **IOPSReservation** e **PersistentReservationsSupported** foram adicionadas na classe Msvm [**\_ StorageAllocationSettingData**](msvm-storageallocationsettingdata.md) .
-   A propriedade **VirtualDiskId** foi adicionada à classe [**\_ VirtualHardDiskSettingData Msvm**](msvm-virtualharddisksettingdata.md) .
-   Informações sobre o QoS de armazenamento foram adicionadas à propriedade **OperationalStatus** das classes [**Msvm \_ LogicalDisk**](msvm-logicaldisk.md) e [**Msvm \_ ResourcePool**](msvm-resourcepool.md) .
-   [**Msvm \_ Classe StorageAlert**](msvm-storagealert.md)
-   A propriedade **ClusterMonitored** foi adicionada às classes [**Msvm \_ EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) e [**Msvm \_ SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md) .
-   As propriedades **EnableCompression** e **EnableSmbTransport** foram adicionadas à classe [**Msvm \_ VirtualSystemMigrationServiceSettingData**](msvm-virtualsystemmigrationservicesettingdata.md) .
-   A propriedade **EnableCompression** foi adicionada à classe [**\_ VirtualSystemMigrationSettingData Msvm**](msvm-virtualsystemmigrationsettingdata.md) . A propriedade **TransportType** inclui informações sobre a migração dinâmica.
-   [**Msvm \_ Classe CopyFileToGuestJob**](msvm-copyfiletoguestjob.md)
-   [**Msvm \_ Classe CopyFileToGuestSettingData**](msvm-copyfiletoguestsettingdata.md)
-   [**Msvm \_ Classe GuestFileService**](msvm-guestfileservice.md)
-   [**Msvm \_ Classe GuestService**](msvm-guestservice.md)
-   [**Msvm \_ Classe GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md)
-   [**Msvm \_ Classe GuestServiceInterfaceComponentSettingData**](msvm-guestserviceinterfacecomponentsettingdata.md)
-   [**Msvm \_ Classe RegisteredGuestService**](msvm-registeredguestservice.md)
-   A propriedade **EnhancedSessionModeEnabled** foi adicionada à classe [**\_ VirtualSystemManagementServiceSettingData Msvm**](msvm-virtualsystemmanagementservicesettingdata.md) .
-   A propriedade **EnhancedModeState** e o método [**InjectNonMaskableInterrupt**](injectnonmaskableinterrupt-msvm-computersystem.md) foram adicionados à classe [**Msvm \_ ComputerSystem**](msvm-computersystem.md) .
-   As propriedades **BootSourceOrder**, **LowMmioGapSize**, **NetworkBootPreferredProtocol**, **PauseAfterBootFailure** , **SecureBootEnabled** e **VirtualSystemSubType** foram adicionadas na classe Msvm [**\_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) .
-   [**Msvm \_ Classe BootSourceSettingData**](msvm-bootsourcesettingdata.md)
-   [**Msvm \_ Classe BootSourceComponent**](msvm-bootsourcecomponent.md)
-   [**Msvm \_ Classe LogicalIdentity**](msvm-logicalidentity.md)
-   [**Msvm \_ Classe CompatibilityVector**](msvm-compatibilityvector.md)
-   O método [**GetSystemCompatibilityVectors**](getsystemcompatibilityvectors-msvm-virtualsystemmigrationservice.md) foi adicionado à classe [**\_ VirtualSystemMigrationService Msvm**](msvm-virtualsystemmigrationservice.md) .
-   As propriedades **ReplicationStateEx**, **ReplicationHealthEx**, **EnhancedSessionModeState**, **VirtualSwitchNames** e **VirtualSystemSubType** foram adicionadas à classe Msvm [**\_ SummaryInformation**](msvm-summaryinformation.md) . As propriedades **replicationstate** e **ReplicationHealth** são preteridas e substituídas pelas propriedades **ReplicationStateEx** e **ReplicationHealthEx** .
-   A propriedade **PnpDevicePath** foi adicionada à classe [**\_ MountedStorageImage Msvm**](msvm-mountedstorageimage.md) .
-   As propriedades **AllowedHashAlgorithms** e **TrustedIssuerCertificateHashes** foram adicionadas à classe [**Msvm \_ TerminalServiceSettingData**](msvm-terminalservicesettingdata.md) .

Windows 8.1 e Windows Server 2012 R2 incluem novas funcionalidades para replicação de máquina virtual e recuperação de failover.

-   [**Msvm \_ Classe replicationprovider**](msvm-replicationprovider.md)
-   [**Msvm \_ Classe ReplicationRelationship**](msvm-replicationrelationship.md)
-   Os métodos [**ChangeReplicationModeToPrimary**](changereplicationmodetoprimary-msvm-replicationservice.md), [**GetReplicationStatisticsEx**](getreplicationstatisticsex-msvm-replicationservice.md), [**InitiateFailback**](initiatefailback-msvm-replicationservice.md), [**RemoveReplicationRelationshipEx**](removereplicationrelationshipex-msvm-replicationservice.md)e [**ResetReplicationStatisticsEx**](resetreplicationstatisticsex-msvm-replicationservice.md) foram adicionados à classe Msvm [**\_ ReplicationService**](msvm-replicationservice.md) . Os métodos **GetReplicationStatisticsEx**, **RemoveReplicationRelationshipEx** e **ResetReplicationStatisticsEx** substituem os métodos [**GetReplicationStatistics**](getreplicationstatistics-msvm-replicationservice.md), [**RemoveReplicationRelationship**](removereplicationrelationship-msvm-replicationservice.md)e [**ResetReplicationStatistics**](resetreplicationstatistics-msvm-replicationservice.md) .
-   A classe [**Msvm \_ SystemReplicationRelationship**](msvm-systemreplicationrelationship.md) mostra uma associação entre uma máquina virtual e muitos relacionamentos de replicação.
-   As propriedades **AdditionalSettings** e **replicationprovider** foram adicionadas à classe [**\_ ReplicationSettingData Msvm**](msvm-replicationsettingdata.md) .
-   Informações sobre o provedor host-to-host foram adicionadas aos métodos [**CreateReplicationRelationship**](createreplicationrelationship-msvm-replicationservice.md) e [**ModifyReplicationSettings**](modifyreplicationsettings-msvm-replicationservice.md) da classe [**Msvm \_ ReplicationService**](msvm-replicationservice.md) .
-   O método [**RequestReplicationStateChangeEx**](msvm-requestreplicationstatechangeex-computersystem.md) foi adicionado à classe [**Msvm \_ ComputerSystem**](msvm-computersystem.md) e substitui o método [**RequestReplicationStateChange**](msvm-computersystem-requestreplicationstatechange.md) . A propriedade **InstanceId** agora pode indicar a replicação estendida. Para obter mais informações sobre a replicação estendida, consulte [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md).
-   [**Msvm \_**](msvm-replicationsettingdata.md) As instâncias ReplicationSettingData e [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) têm uma relação 1:1 que você pode representar com uma associação [**Msvm \_ SettingsDefineState**](msvm-settingsdefinestate.md) .

    | [**Msvm \_**](msvm-settingsdefinestate.md) Nome da propriedade SettingsDefineState | Valor                                                                                                |
    |-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
    | **Managedelement**                                                          | Representa o objeto [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md)          |
    | **SettingData**                                                             | Representa o objeto [**Msvm \_ ReplicationSettingData**](msvm-replicationsettingdata.md) associado |

    

     

-   [**Msvm \_ ReplicationSettingData**](msvm-replicationsettingdata.md) pode diferenciar entre instâncias de configuração para relação de replicação com base na propriedade **InstanceId** ou **ReplicationRelationship** . Portanto, esses métodos que lidam com uma relação única não alteraram sua assinatura:

    -   [**Msvm \_ ReplicationService::CreateReplicationRelationship**](createreplicationrelationship-msvm-replicationservice.md)
    -   [**Msvm \_ ReplicationService::ModifyReplicationSettings**](modifyreplicationsettings-msvm-replicationservice.md)
    -   [**Msvm \_ ReplicationService::Resync**](resynchronize-msvm-replicationservice.md)
    -   [**Msvm \_ ReplicationService::StartReplication**](startreplication-msvm-replicationservice.md)

-   Embora você possa usar [**GetReplicationStatistics,**](getreplicationstatistics-msvm-replicationservice.md) [**RemoveReplicationRelationship**](removereplicationrelationship-msvm-replicationservice.md)e [**RequestReplicationStateChange**](msvm-computersystem-requestreplicationstatechange.md) sempre para a relação primária, recomendamos que você use [**GetReplicationStatisticsEx,**](getreplicationstatisticsex-msvm-replicationservice.md) [**RemoveReplicationRelationshipEx**](removereplicationrelationshipex-msvm-replicationservice.md)e [**RequestReplicationStateChangeEx**](msvm-requestreplicationstatechangeex-computersystem.md) porque eles podem processar a relação de replicação primária e estendida. Para obter mais informações sobre a replicação estendida, consulte [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md).
-   Embora essas propriedades da classe [**Msvm \_ ComputerSystem**](msvm-computersystem.md) continuem indicando o status da relação de replicação primária, em vez disso, use essas propriedades de um objeto [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) para determinar o status atual da relação de replicação primária e estendida.

    | Nome da propriedade                                | Type        |
    |----------------------------------------------|-------------|
    | **ReplicationState**                         | Uint16 (RO) |
    | **Replicationhealth**                        | Uint16 (RO) |
    | **LastReplicationTime**                      | Datetime    |
    | **FailedOverReplicationType**                | Uint16      |
    | **LastApplicationConsistentReplicationTime** | Datetime    |
    | **LastReplicationType**                      | Uint16      |

    

     

 

 



