---
title: Interface IVMVirtualMachine (VPCCOMInterfaces. h)
description: Define a interface para uma máquina virtual.
ms.assetid: c1c243f2-0fb7-4249-8dc9-f0b70059e78f
keywords:
- Virtual PC de interface IVMVirtualMachine
- Virtual PC de interface IVMVirtualMachine, descrito
topic_type:
- apiref
api_name:
- IVMVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 006fe414a662c3d6d556aba68712aa0b428d9b5e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105788868"
---
# <a name="ivmvirtualmachine-interface"></a>Interface IVMVirtualMachine

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define a interface para uma máquina virtual. **IVMVirtualMachine** pode notificar clientes sobre eventos usando a interface de saída do [**IVMVirtualMachineEvents**](ivmvirtualmachineevents.md) . Os objetos **IVMVirtualMachine** são retornados de métodos [**IVMVirtualPC**](ivmvirtualpc.md) , como [**CreateVirtualMachine**](ivmvirtualpc-createvirtualmachine.md), [**RegisterVirtualMachine**](ivmvirtualpc-registervirtualmachine.md)e [**FindVirtualMachine**](ivmvirtualpc-findvirtualmachine.md). Você também pode recuperar um objeto **IVMVirtualMachine** do objeto [**IVMVirtualMachineCollection**](ivmvirtualmachinecollection.md) retornado da propriedade [**IVMVirtualPC:: VirtualMachines**](ivmvirtualpc-virtualmachines.md) .

## <a name="members"></a>Membros

A interface **IVMVirtualMachine** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMVirtualMachine** também tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **IVMVirtualMachine** tem esses métodos.



| Método                                                                           | Descrição                                                                                                |
|:---------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**AddDVDROMDrive**](ivmvirtualmachine-adddvdromdrive.md)                       | Adiciona uma nova unidade de CD ou DVD à máquina virtual.<br/>                                              |
| [**AddHardDiskConnection**](ivmvirtualmachine-addharddiskconnection.md)         | Adiciona uma nova conexão de disco rígido à máquina virtual.<br/>                                         |
| [**AddNetworkAdapter**](ivmvirtualmachine-addnetworkadapter.md)                 | Adiciona uma interface de rede à máquina virtual.<br/>                                                |
| [**AttachUSBDevice**](ivmvirtualmachine-attachusbdevice.md)                     | Anexa um dispositivo USB a uma máquina virtual.<br/>                                                     |
| [**DetachUSBDevice**](ivmvirtualmachine-detachusbdevice.md)                     | Libera um dispositivo USB de uma máquina virtual.<br/>                                                   |
| [**DiscardSavedState**](ivmvirtualmachine-discardsavedstate.md)                 | Descarta todas as informações de estado salvas de uma máquina virtual salva.<br/>                               |
| [**DiscardUndoDisks**](ivmvirtualmachine-discardundodisks.md)                   | Descarta os discos de desfazer virtuais.<br/>                                                                |
| [**Getactivavalue**](ivmvirtualmachine-getactivationvalue.md)               | Recupera o valor da configuração de ativação especificada para esta máquina virtual.<br/>               |
| [**GetConfigurationValue**](ivmvirtualmachine-getconfigurationvalue.md)         | Recupera o valor da definição de configuração especificada para esta máquina virtual.<br/>            |
| [**MergeUndoDisks**](ivmvirtualmachine-mergeundodisks.md)                       | Mescla os discos de desfazer virtuais.<br/>                                                                  |
| [**Pausar**](ivmvirtualmachine-pause.md)                                         | Pausa a máquina virtual.<br/>                                                                     |
| [**RemoveActivationValue**](ivmvirtualmachine-removeactivationvalue.md)         | Remove o valor da configuração de ativação especificada para esta máquina virtual.<br/>                 |
| [**RemoveConfigurationValue**](ivmvirtualmachine-removeconfigurationvalue.md)   | Remove o valor da definição de configuração especificada para esta máquina virtual.<br/>              |
| [**RemoveDVDROMDrive**](ivmvirtualmachine-removedvdromdrive.md)                 | Remove a unidade de CD ou DVD especificada da máquina virtual.<br/>                                 |
| [**RemoveHardDiskConnection**](ivmvirtualmachine-removeharddiskconnection.md)   | Remove a conexão de disco rígido especificada da máquina virtual.<br/>                            |
| [**RemoveNetworkAdapter**](ivmvirtualmachine-removenetworkadapter.md)           | Remove uma interface de rede da máquina virtual.<br/>                                           |
| [**Redefinir**](ivmvirtualmachine-reset.md)                                         | Redefine a máquina virtual.<br/>                                                                     |
| [**Retomar**](ivmvirtualmachine-resume.md)                                       | Retoma a máquina virtual.<br/>                                                                    |
| [**Salvar**](ivmvirtualmachine-save.md)                                           | Salva o estado da máquina virtual.<br/>                                                                |
| [**Setactivavalue**](ivmvirtualmachine-setactivationvalue.md)               | Define o valor da configuração de ativação especificada para esta máquina virtual.<br/>                    |
| [**Setconfigurationvalue**](ivmvirtualmachine-setconfigurationvalue.md)         | Define o valor da definição de configuração especificada para esta máquina virtual.<br/>                 |
| [**StartCommunicationChannel**](ivmvirtualmachine-startcommunicationchannel.md) | Configura um canal de comunicação entre o host e o convidado.<br/>                                         |
| [**Inicialização**](ivmvirtualmachine-startup.md)                                     | Inicia a máquina virtual no estado não inicializado ou salvo.<br/>                        |
| [**Startup2**](ivmvirtualmachine-startup2.md)                                   | Inicia a máquina virtual no estado não inicializado ou salvo, com opções avançadas.<br/> |
| [**Desativação**](ivmvirtualmachine-turnoff.md)                                     | Desativa a máquina virtual.<br/>                                                                  |



 

### <a name="properties"></a>Propriedades

A interface **IVMVirtualMachine** tem essas propriedades.



| Propriedade                                                                            | Tipo de acesso           | Descrição                                                                                                                                    |
|:------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**Apoio**](ivmvirtualmachine-accountant.md)<br/>                       | Somente leitura<br/>  | Um contador para esta máquina virtual.<br/>                                                                                             |
| [**AttachedDriveTypes**](ivmvirtualmachine-attacheddrivetypes.md)<br/>       | Somente leitura<br/>  | Uma matriz que indica o tipo de unidade anexado a cada local na máquina virtual.<br/>                                             |
| [**BaseBoardSerialNumber**](ivmvirtualmachine-baseboardserialnumber.md)<br/> | Leitura/gravação<br/> | O número de série da placa base.<br/>                                                                                                       |
| [**BIOSGUID**](ivmvirtualmachine-biosguid.md)<br/>                           | Leitura/gravação<br/> | O GUID do BIOS.<br/>                                                                                                                      |
| [**BIOSSerialNumber**](ivmvirtualmachine-biosserialnumber.md)<br/>           | Leitura/gravação<br/> | O número de série do BIOS.<br/>                                                                                                             |
| [**ChassisAssetTag**](ivmvirtualmachine-chassisassettag.md)<br/>             | Leitura/gravação<br/> | A marca do ativo do chassi.<br/>                                                                                                              |
| [**ChassisSerialNumber**](ivmvirtualmachine-chassisserialnumber.md)<br/>     | Leitura/gravação<br/> | O número de série do chassi.<br/>                                                                                                          |
| [**Configid**](ivmvirtualmachine-configid.md)<br/>                           | Somente leitura<br/>  | O identificador exclusivo para a máquina virtual.<br/>                                                                                      |
| [**Monitor**](ivmvirtualmachine-display.md)<br/>                             | Somente leitura<br/>  | A exibição de vídeo para a máquina virtual.<br/>                                                                                          |
| [**DVDROMDrives**](ivmvirtualmachine-dvdromdrives.md)<br/>                   | Somente leitura<br/>  | Uma coleção enumerável de unidades de CD e DVD conectadas à máquina virtual.<br/>                                                      |
| [**Arquivo**](ivmvirtualmachine-file.md)<br/>                                   | Somente leitura<br/>  | O caminho totalmente qualificado do arquivo. VMC para a configuração da máquina virtual.<br/>                                                    |
| [**FloppyDrives**](ivmvirtualmachine-floppydrives.md)<br/>                   | Somente leitura<br/>  | Uma coleção enumerável de unidades de disquete conectadas à máquina virtual.<br/>                                                          |
| [**GuestOS**](ivmvirtualmachine-guestos.md)<br/>                             | Somente leitura<br/>  | O sistema operacional convidado para esta máquina virtual.<br/>                                                                                |
| [**HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md)<br/>     | Somente leitura<br/>  | Uma coleção enumerável de conexões de disco rígido.<br/>                                                                                  |
| [**Has3DNow**](ivmvirtualmachine-has3dnow.md)<br/>                           | Somente leitura<br/>  | Indica se o processador dá suporte ao conjunto de instruções 3DNow.<br/>                                                                 |
| [**HasMMX**](ivmvirtualmachine-hasmmx.md)<br/>                               | Somente leitura<br/>  | Indica se o processador dá suporte ao conjunto de instruções MMX.<br/>                                                                   |
| [**HasSSE**](ivmvirtualmachine-hassse.md)<br/>                               | Somente leitura<br/>  | Indica se o processador dá suporte ao conjunto de instruções SSE.<br/>                                                                   |
| [**HasSSE2**](ivmvirtualmachine-hassse2.md)<br/>                             | Somente leitura<br/>  | Indica se o processador dá suporte ao conjunto de instruções SSE2.<br/>                                                                  |
| [**Teclado**](ivmvirtualmachine-keyboard.md)<br/>                           | Somente leitura<br/>  | O dispositivo de teclado para a máquina virtual.<br/>                                                                                        |
| [**Memória**](ivmvirtualmachine-memory.md)<br/>                               | Leitura/gravação<br/> | A quantidade de memória física na máquina virtual, em megabytes.<br/>                                                                 |
| [**Mouse**](ivmvirtualmachine-mouse.md)<br/>                                 | Somente leitura<br/>  | O dispositivo de mouse para a máquina virtual.<br/>                                                                                           |
| [**Nome**](ivmvirtualmachine-name.md)<br/>                                   | Leitura/gravação<br/> | O nome da configuração da máquina virtual.<br/>                                                                                      |
| [**Adaptadores**](ivmvirtualmachine-networkadapters.md)<br/>             | Somente leitura<br/>  | Uma coleção enumerável de NICs anexadas à máquina virtual.<br/>                                                                   |
| [**Observações**](ivmvirtualmachine-notes.md)<br/>                                 | Leitura/gravação<br/> | As observações para a máquina virtual.<br/>                                                                                                  |
| [**ParallelPorts**](ivmvirtualmachine-parallelports.md)<br/>                 | Somente leitura<br/>  | Uma coleção enumerável de portas paralelas.<br/>                                                                                         |
| [**ProcessorSpeed**](ivmvirtualmachine-processorspeed.md)<br/>               | Somente leitura<br/>  | A velocidade do processador, em megahertz (MHz).<br/>                                                                                     |
| [**RdpPipeName**](ivmvirtualmachine-rdppipename.md)<br/>                     | Somente leitura<br/>  | Nome da conexão RDP chamada pipe usado para vídeo e entrada.<br/>                                                                     |
| [**SavedStateFilePath**](ivmvirtualmachine-savedstatefilepath.md)<br/>       | Somente leitura<br/>  | O caminho completo para o arquivo de estado salvo.<br/>                                                                                              |
| [**SerialPorts**](ivmvirtualmachine-serialports.md)<br/>                     | Somente leitura<br/>  | Uma coleção enumerável de portas seriais.<br/>                                                                                           |
| [**ShutdownActionOnQuit**](ivmvirtualmachine-shutdownactiononquit.md)<br/>   | Leitura/gravação<br/> | A ação a ser executada nesta máquina virtual se estiver em execução quando o Windows Virtual PC for encerrado.<br/>                                |
| [**Status**](ivmvirtualmachine-state.md)<br/>                                 | Somente leitura<br/>  | O estado atual da máquina virtual.<br/>                                                                                           |
| [**Executado**](ivmvirtualmachine-undoable.md)<br/>                           | Leitura/gravação<br/> | Indica se as unidades de desfazer estão habilitadas para discos rígidos conectados à máquina virtual.<br/>                                      |
| [**Desfazeraction**](ivmvirtualmachine-undoaction.md)<br/>                       | Leitura/gravação<br/> | A ação padrão a ser executada em todas as unidades de desfazer quando a máquina virtual é desligada de dentro do sistema operacional convidado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine é definido como f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



 

