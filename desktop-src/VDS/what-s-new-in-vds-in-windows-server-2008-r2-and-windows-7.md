---
description: Saiba mais sobre as novas alterações do VDS (serviço de disco virtual) no Windows Server 2008 R2 e no Windows 7.
ms.assetid: 4ab37529-8d56-47a3-ad3d-0197cabd4f87
title: Novidades no VDS no Windows Server 2008 R2 e no Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9050b157e9ce3c78550fdcffbd688988b7eacf90
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119651"
---
# <a name="whats-new-in-vds-in-windows-server-2008-r2-and-windows-7"></a>Novidades no VDS no Windows Server 2008 R2 e no Windows 7

\[A partir do Windows 8 e do Windows Server 2012, a interface com do [serviço de disco virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

O Windows Server 2008 R2 e o Windows 7 apresentam as seguintes alterações ao VDS (serviço de disco virtual):

- [Novas interfaces VDS](#new-vds-interfaces)
- [Novas enumerações VDS](#new-vds-enumerations)
- [Novas estruturas do VDS](#new-vds-structures)
- [Modificações em enumerações VDS existentes](#modifications-to-existing-vds-enumerations)
- [Modificações nas estruturas VDS existentes](#modifications-to-existing-vds-structures)

## <a name="new-vds-interfaces"></a>Novas interfaces VDS

<dl>

[**IVdsDisk3**](/windows/desktop/api/Vds/nn-vds-ivdsdisk3)  
[**IVdsDiskPartitionMF2**](/windows/desktop/api/Vds/nn-vds-ivdsdiskpartitionmf2)  
[**IVdsDrive2**](/windows/desktop/api/Vds/nn-vds-ivdsdrive2)  
[**IVdsHwProviderStoragePools**](/windows/desktop/api/Vds/nn-vds-ivdshwproviderstoragepools)  
[**IVdsLun2**](/windows/desktop/api/Vds/nn-vds-ivdslun2)  
[**IVdsLunNumber**](/windows/desktop/api/Vds/nn-vds-ivdslunnumber)  
[**IVdsOpenVDisk**](/windows/desktop/api/Vds/nn-vds-ivdsopenvdisk)  
[**IVdsStoragePool**](/windows/desktop/api/Vds/nn-vds-ivdsstoragepool)  
[**IVdsSubSystem2**](/windows/desktop/api/Vds/nn-vds-ivdssubsystem2)  
[**IVdsSubSystemInterconnect**](/windows/desktop/api/Vds/nn-vds-ivdssubsysteminterconnect)  
[**IVdsVDisk**](/windows/desktop/api/Vds/nn-vds-ivdsvdisk)  
[**IVdsVdProvider**](/windows/desktop/api/Vds/nn-vds-ivdsvdprovider)  
[**IVdsVolume2**](/windows/desktop/api/Vds/nn-vds-ivdsvolume2)  
[**IVdsVolumeMF3**](/windows/desktop/api/Vds/nn-vds-ivdsvolumemf3)  


## <a name="new-vds-enumerations"></a>Novas enumerações VDS

<dl>

[**VDS_DISK_OFFLINE_REASON**](/windows/desktop/api/Vds/ne-vds-vds_disk_offline_reason)  
[**VDS_FORMAT_OPTION_FLAGS**](/windows/desktop/api/Vds/ne-vds-vds_format_option_flags)  
[**VDS_INTERCONNECT_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_interconnect_flag)  
[**VDS_RAID_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_raid_type)  
[**VDS_STORAGE_POOL_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_status)  
[**VDS_STORAGE_POOL_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_storage_pool_type)  
[**VDS_SUB_SYSTEM_SUPPORTED_RAID_TYPE_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_supported_raid_type_flag)  
[**VDS_VDISK_STATE**](/windows/desktop/api/Vds/ne-vds-vds_vdisk_state)  


## <a name="new-vds-structures"></a>Novas estruturas do VDS

<dl>

[**VDS_CREATE_VDISK_PARAMETERS**](/windows/desktop/api/Vds/ns-vds-vds_create_vdisk_parameters)  
[**VDS_DISK_FREE_EXTENT**](/windows/desktop/api/Vds/ns-vds-vds_disk_free_extent)  
[**VDS_DISK_PROP2**](/windows/desktop/api/Vds/ns-vds-vds_disk_prop2)  
[**VDS_DRIVE_PROP2**](/windows/desktop/api/Vds/ns-vds-vds_drive_prop2)  
[**VDS_HINTS2**](/windows/desktop/api/Vds/ns-vds-vds_hints2)  
[**VDS_POOL_ATTRIBUTES**](/windows/desktop/api/Vds/ns-vds-vds_pool_attributes)  
[**VDS_POOL_CUSTOM_ATTRIBUTES**](/windows/desktop/api/Vds/ns-vds-vds_pool_custom_attributes)  
[**VDS_STORAGE_POOL_DRIVE_EXTENT**](/windows/desktop/api/Vds/ns-vds-vds_storage_pool_drive_extent)  
[**VDS_STORAGE_POOL_PROP**](/windows/desktop/api/Vds/ns-vds-vds_storage_pool_prop)  
[**VDS_SUB_SYSTEM_PROP2**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_prop2)  
[**VDS_VDISK_PROPERTIES**](/windows/desktop/api/Vds/ns-vds-vds_vdisk_properties)  
[**VDS_VOLUME_PROP2**](/windows/desktop/api/Vds/ns-vds-vds_volume_prop)  


## <a name="modifications-to-existing-vds-enumerations"></a>Modificações em enumerações VDS existentes

[**VDS_ASYNC_OUTPUT_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_async_output_type) valores adicionados à enumeração:

 **VDS_ASYNCOUT_CREATE_VDISK**  
**VDS_ASYNCOUT_ATTACH_VDISK**  
**VDS_ASYNCOUT_COMPACT_VDISK**  
**VDS_ASYNCOUT_MERGE_VDISK**  
**VDS_ASYNCOUT_EXPAND_VDISK**  


[**VDS_CONTROLLER_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_controller_status) valor adicionado à enumeração:

**VDS_CS_REMOVED**  


[**VDS_DISK_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_disk_flag) valor adicionado à enumeração:

**VDS_DF_BOOT_FROM_DISK**  
**VDS_DF_CURRENT_READ_ONLY**  


[**VDS_DRIVE_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_drive_flag) valores adicionados à enumeração:

**VDS_DRF_ASSIGNED**  
**VDS_DRF_UNASSIGNED**  
**VDS_DRF_HOTSPARE_IN_USE**  
**VDS_DRF_HOTSPARE_STANDBY**  


[**VDS_DRIVE_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_drive_status) valor adicionado à enumeração:

**VDS_DRS_REMOVED**  


[**VDS_FILE_SYSTEM_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_file_system_type) valor adicionado à enumeração:

**VDS_FST_EXFAT**  


[**VDS_HEALTH**](/windows/desktop/api/Vds/ne-vds-vds_health) valores adicionados à enumeração:

**VDS_H_REPLACED**  
**VDS_H_PENDING_FAILURE**  
**VDS_H_DEGRADED**  


[**VDS_HWPROVIDER_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_hwprovider_type) valores adicionados à enumeração:

**VDS_HWT_SAS**  
**VDS_HWT_HYBRID**  


[**VDS_LUN_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_lun_flag) valores adicionados à enumeração:

**VDS_LF_READ_CACHE_ENABLED**  
**VDS_LF_WRITE_CACHE_ENABLED**  
**VDS_LF_MEDIA_SCAN_ENABLED**  
**VDS_LF_CONSISTENCY_CHECK_ENABLED**  
**VDS_LF_SNAPSHOT**  


[**VDS_LUN_PLEX_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_type) valores adicionados à enumeração:

**VDS_LPT_RAID2**  
**VDS_LPT_RAID3**  
**VDS_LPT_RAID4**  
**VDS_LPT_RAID5**  
**VDS_LPT_RAID6**  
**VDS_LPT_RAID03**  
**VDS_LPT_RAID05**  
**VDS_LPT_RAID10**  
**VDS_LPT_RAID15**  
**VDS_LPT_RAID30**  
**VDS_LPT_RAID50**  
**VDS_LPT_RAID53**  
**VDS_LPT_RAID60**  


[**VDS_LUN_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_lun_type) valores adicionados à enumeração:

**VDS_LT_RAID2**  
**VDS_LT_RAID3**  
**VDS_LT_RAID4**  
**VDS_LT_RAID5**  
**VDS_LT_RAID6**  
**VDS_LT_RAID01**  
**VDS_LT_RAID03**  
**VDS_LT_RAID05**  
**VDS_LT_RAID10**  
**VDS_LT_RAID15**  
**VDS_LT_RAID30**  
**VDS_LT_RAID50**  
**VDS_LT_RAID51**  
**VDS_LT_RAID53**  
**VDS_LT_RAID60**  
**VDS_LT_RAID61**  


[**VDS_OBJECT_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_object_type) valores adicionados à enumeração:

**VDS_OT_STORAGE_POOL**  
**VDS_OT_VDISK**  
**VDS_OT_OPEN_VDISK**  


[**VDS_PORT_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_port_status) valor adicionado à enumeração:

**VDS_DRS_REMOVED**  


[**VDS_PROVIDER_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_provider_flag) valores adicionados à enumeração:

**VDS_PF_SUPPORT_MIRROR**  
**VDS_PF_SUPPORT_RAID5**  


[**VDS_PROVIDER_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_provider_type) valores adicionados à enumeração:

**VDS_PT_VIRTUALDISK**  
**VDS_PT_MAX**  


[**VDS_SERVICE_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_service_flag) valores adicionados à enumeração:

**VDS_SVF_SUPPORT_MIRROR**  
**VDS_SVF_SUPPORT_RAID5**  


[**VDS_SUB_SYSTEM_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_sub_system_flag) valores adicionados à enumeração:

**VDS_SF_SUPPORTS_LUN_NUMBER**  
**VDS_SF_SUPPORTS_MIRRORED_CACHE**  
**VDS_SF_READ_CACHING_CAPABLE**  
**VDS_SF_WRITE_CACHING_CAPABLE**  
**VDS_SF_MEDIA_SCAN_CAPABLE**  
**VDS_SF_CONSISTENCY_CHECK_CAPABLE**  


[**VDS_TRANSITION_STATE**](/windows/desktop/api/Vds/ne-vds-vds_transition_state) valor adicionado à enumeração:

**VDS_TS_RESTRIPING**  


[**VDS_VERSION_SUPPORT_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_version_support_flag) valores adicionados à enumeração:

**VDS_VSF_2_0**  
**VDS_VSF_2_1**  
**VDS_VSF_3_0**  


[**VDS_VOLUME_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_volume_status) valor adicionado à enumeração:

**VDS_VS_OFFLINE**  


## <a name="modifications-to-existing-vds-structures"></a>Modificações nas estruturas VDS existentes

[**VDS_CONTROLLER_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification) estrutura adicionou valores de **ulEvent** :

VDS_NF_CONTROLLER_MODIFY  
VDS_NF_CONTROLLER_REMOVED  


A estrutura de [**VDS_DRIVE_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification) adicionou o valor **ulEvent** :

VDS_NF_DRIVE_REMOVED  


[**VDS_PORT_NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_port_notification) estrutura adicionou valores de **ulEvent** :

VDS_NF_PORT_MODIFY  
VDS_NF_PORT_REMOVED  


 

 
