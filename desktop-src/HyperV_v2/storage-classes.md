---
description: 'Os objetos de armazenamento são separados em três tipos: controladores, unidades e mídia.'
ms.assetid: CF38F6E8-A43D-4A97-8055-6B17E323524C
title: Classes de armazenamento
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90c46efc17b3df5e1a509cec3565c6aaa7b65ff06d189951b100ac06d93a957e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829666"
---
# <a name="storage-classes"></a>Classes de armazenamento

Os objetos de armazenamento são separados em três tipos: controladores, unidades e mídia.

Há dois controladores, um controlador IDE emulado e um controlador SCSI sintético. Ambos os controladores dão suporte ao anexo de unidades que hospedam a mídia.

Veja a seguir as classes WMI de virtualização relacionadas ao armazenamento. Também há suporte para mídia de disquete sintética. Não há suporte para a anexação a uma unidade de disquete física.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                      | Descrição                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Msvm \_ AffectedStorageJobElement**](msvm-affectedstoragejobelement.md)<br/>       | Representa a associação entre um trabalho e os elementos gerenciados que podem ser afetados pela sua execução.<br/>                                                                                               |
| [**Msvm \_ com base em**](msvm-basedon.md)<br/>                                           | Uma associação que descreve como as extensões de armazenamento podem ser montadas de extensões de nível inferior.<br/>                                                                                                           |
| [**Msvm \_ ControlledBy**](msvm-controlledby.md)<br/>                                 | Associa um dispositivo de armazenamento ao controlador de armazenamento que possui o dispositivo.<br/>                                                                                                                          |
| [**Msvm \_ DiskDrive**](msvm-diskdrive.md)<br/>                                       | Representa uma unidade de disco rígido dentro de uma máquina virtual.<br/>                                                                                                                                              |
| [**Msvm \_ DisketteController**](msvm-diskettecontroller.md)<br/>                     | Representa o controlador de disquete na máquina virtual.<br/>                                                                                                                                               |
| [**Msvm \_ DisketteDrive**](msvm-diskettedrive.md)<br/>                               | Representa uma unidade de disquete dentro da máquina virtual.<br/>                                                                                                                                                  |
| [**Msvm \_ DVDDrive**](msvm-dvddrive.md)<br/>                                         | Representa uma unidade de DVD dentro de uma máquina virtual.<br/>                                                                                                                                                    |
| [**Msvm \_ IDEController**](msvm-idecontroller.md)<br/>                               | Representa um controlador IDE.<br/>                                                                                                                                                                          |
| [**Msvm \_ imagens**](msvm-imagemanagementservice.md)<br/>             | Gerencia os arquivos de mídia virtual (. VHD,. vhdx,. ISO ou. VFD) para uma máquina virtual.<br/>                                                                                                                    |
| [**\_LogicalDisk Msvm**](msvm-logicaldisk.md)<br/>                                   | Representa a mídia da unidade de armazenamento e é usada para preencher as unidades de armazenamento.<br/>                                                                                                                             |
| [**Msvm \_ MediaPresent**](msvm-mediapresent.md)<br/>                                 | Associa uma unidade de armazenamento à mídia inserida na unidade.<br/>                                                                                                                                     |
| [**Msvm \_ MountedStorageImage**](msvm-mountedstorageimage.md)<br/>                   | Fornece informações detalhadas sobre uma imagem de armazenamento montada manualmente.<br/>                                                                                                                                  |
| [**Msvm \_ ProtocolControllerForUnit**](msvm-protocolcontrollerforunit.md)<br/>       | Essa associação indica que uma subclasse de dispositivo lógico (por exemplo, um volume de armazenamento) é conectada por meio de um controlador de protocolo específico.<br/>                                                       |
| [**Msvm \_ SCSIProtocolController**](msvm-scsiprotocolcontroller.md)<br/>             | Representa um controlador SCSI sintético.<br/>                                                                                                                                                                |
| [**Msvm \_ StorageAlert**](msvm-storagealert.md)<br/>                                 | Representa um evento que é gerado cada vez que a propriedade **OperationalStatus** da classe [**Msvm \_ ResourcePool**](msvm-resourcepool.md) ou [**Msvm \_ LogicalDisk**](msvm-logicaldisk.md) é alterada.<br/> |
| [**Msvm \_ StorageAllocationSettingData**](msvm-storageallocationsettingdata.md)<br/> | Representa as configurações especificamente relacionadas à alocação do armazenamento virtual.<br/>                                                                                                                         |
| [**Msvm \_ StorageJob**](msvm-storagejob.md)<br/>                                     | representa um trabalho de operação de armazenamento criado pelo serviço de gerenciamento de imagens Microsoft Hyper-V.<br/>                                                                                                          |
| [**Msvm \_ VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md)<br/>     | Fornece dados de configuração para um disco rígido virtual.<br/>                                                                                                                                                         |
| [**Msvm \_ VirtualHardDiskState**](msvm-virtualharddiskstate.md)<br/>                 | Fornece informações de estado para uma imagem de disco rígido virtual existente.<br/>                                                                                                                                    |



 

 

 




