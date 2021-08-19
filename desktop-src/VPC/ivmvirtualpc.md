---
title: Interface IVMVirtualPC (VPCCOMInterfaces. h)
description: define o objeto de aplicativo Windows Virtual PC de nível superior. todos os outros objetos de interface do Virtual PC Windows são recuperados por meio desse objeto.
ms.assetid: 519d3f1b-0a72-4c67-a2d9-124fda6c8b7a
keywords:
- Virtual PC de interface IVMVirtualPC
- Virtual PC de interface IVMVirtualPC, descrito
topic_type:
- apiref
api_name:
- IVMVirtualPC
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69dd5eec832e95b2b93ff0fb0bee026428a937fa277f86ff14ef672bc66e0dd6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124646"
---
# <a name="ivmvirtualpc-interface"></a>Interface IVMVirtualPC

\[Windows O Virtual PC não está mais disponível para uso a partir de Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

define o objeto de aplicativo Windows Virtual PC de nível superior. todos os outros objetos de interface do Virtual PC Windows são recuperados por meio desse objeto.

O **IVMVirtualPC** pode notificar os clientes sobre eventos usando a interface de saída do [**IVMVirtualPCEvents**](ivmvirtualpcevents.md) .

## <a name="members"></a>Membros

A interface **IVMVirtualPC** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMVirtualPC** também tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **IVMVirtualPC** tem esses métodos.



| Método                                                                                      | Descrição                                                                                              |
|:--------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [**CreateDifferencingVirtualHardDisk**](ivmvirtualpc-createdifferencingvirtualharddisk.md) | Cria um disco rígido virtual diferencial.<br/>                                                     |
| [**CreateDynamicVirtualHardDisk**](ivmvirtualpc-createdynamicvirtualharddisk.md)           | Cria um disco rígido virtual de redimensionamento dinâmico.<br/>                                             |
| [**CreateFixedVirtualHardDisk**](ivmvirtualpc-createfixedvirtualharddisk.md)               | Cria um disco rígido virtual de tamanho fixo.<br/>                                                       |
| [**CreateFloppyDiskImage**](ivmvirtualpc-createfloppydiskimage.md)                         | Cria um arquivo de imagem de disquete.<br/>                                                             |
| [**CreateVirtualMachine**](ivmvirtualpc-createvirtualmachine.md)                           | Cria uma nova configuração de máquina virtual e recupera o objeto de máquina virtual.<br/>         |
| [**DeleteVirtualMachine**](ivmvirtualpc-deletevirtualmachine.md)                           | Exclui uma configuração de máquina virtual.<br/>                                                      |
| [**FindVirtualMachine**](ivmvirtualpc-findvirtualmachine.md)                               | Recupera um objeto de máquina virtual que corresponde à configuração solicitada.<br/>                  |
| [**FindVirtualNetwork**](ivmvirtualpc-findvirtualnetwork.md)                               | Recupera um objeto de rede virtual que corresponde ao nome solicitado.<br/>                           |
| [**GetConfigurationValue**](ivmvirtualpc-getconfigurationvalue.md)                         | Recupera o valor da definição de configuração especificada.<br/>                                   |
| [**GetDVDFiles**](ivmvirtualpc-getdvdfiles.md)                                             | Recupera uma matriz de arquivos de DVD conhecidos.<br/>                                                        |
| [**GetFloppyDiskFiles**](ivmvirtualpc-getfloppydiskfiles.md)                               | Recupera uma matriz de arquivos de disquete virtual conhecidos.<br/>                                        |
| [**GetFloppyDiskImageType**](ivmvirtualpc-getfloppydiskimagetype.md)                       | Recupera o tipo de um arquivo de imagem de disquete existente.<br/>                                     |
| [**GetHardDisk**](ivmvirtualpc-getharddisk.md)                                             | Recupera um objeto correspondente a um arquivo de imagem de disco existente.<br/>                             |
| [**GetHardDiskFiles**](ivmvirtualpc-getharddiskfiles.md)                                   | Recupera uma matriz de arquivos de disco rígido virtual conhecidos.<br/>                                          |
| [**GetVirtualMachineFiles**](ivmvirtualpc-getvirtualmachinefiles.md)                       | Recupera uma matriz de arquivos de configuração de máquina virtual conhecidos.<br/>                              |
| [**RegisterVirtualMachine**](ivmvirtualpc-registervirtualmachine.md)                       | Registra uma configuração de máquina virtual existente e recupera o objeto de máquina virtual.<br/> |
| [**RemoveConfigurationValue**](ivmvirtualpc-removeconfigurationvalue.md)                   | Remove o valor da definição de configuração especificada.<br/>                                     |
| [**Setconfigurationvalue**](ivmvirtualpc-setconfigurationvalue.md)                         | Define o valor da definição de configuração especificada.<br/>                                        |
| [**UnregisterVirtualMachine**](ivmvirtualpc-unregistervirtualmachine.md)                   | Cancela o registro de uma configuração de máquina virtual sem excluir o arquivo de configuração.<br/>          |



 

### <a name="properties"></a>Propriedades

A interface **IVMVirtualPC** tem essas propriedades.



| Propriedade                                                                                   | Tipo de acesso           | Descrição                                                                                                                                           |
|:-------------------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DefaultVMConfigurationPath**](ivmvirtualpc-defaultvmconfigurationpath.md)<br/>   | Leitura/gravação<br/> | O diretório padrão a ser procurado por arquivos de configuração de máquina virtual disponíveis.<br/>                                                    |
| [**HostInfo**](ivmvirtualpc-hostinfo.md)<br/>                                       | Somente leitura<br/>  | Informações sobre o computador físico.<br/>                                                                                                   |
| [**MaximumFloppyDrivesPerVM**](ivmvirtualpc-maximumfloppydrivespervm.md)<br/>       | Somente leitura<br/>  | O número máximo de unidades de disquete por máquina virtual.<br/>                                                                                   |
| [**MaximumMemoryPerVM**](ivmvirtualpc-maximummemorypervm.md)<br/>                   | Somente leitura<br/>  | A quantidade máxima permitida de memória física por máquina virtual, em megabytes.<br/>                                                       |
| [**MaximumNetworkAdaptersPerVM**](ivmvirtualpc-maximumnetworkadapterspervm.md)<br/> | Somente leitura<br/>  | O número máximo de interfaces de rede por máquina virtual.<br/>                                                                             |
| [**MaximumNumberOfIDEBuses**](ivmvirtualpc-maximumnumberofidebuses.md)<br/>         | Somente leitura<br/>  | O número máximo de barramentos permitidos para o IDE.<br/>                                                                                               |
| [**MaximumParallelPortsPerVM**](ivmvirtualpc-maximumparallelportspervm.md)<br/>     | Somente leitura<br/>  | O número máximo de portas paralelas por máquina virtual.<br/>                                                                                  |
| [**MaximumSerialPortsPerVM**](ivmvirtualpc-maximumserialportspervm.md)<br/>         | Somente leitura<br/>  | O número máximo de portas seriais por máquina virtual.<br/>                                                                                    |
| [**MinimumMemoryPerVM**](ivmvirtualpc-minimummemorypervm.md)<br/>                   | Somente leitura<br/>  | A quantidade mínima permitida de memória física por máquina virtual, em megabytes.<br/>                                                       |
| [**Nome**](ivmvirtualpc-name.md)<br/>                                               | Somente leitura<br/>  | o nome do aplicativo de Windows Virtual PC.<br/>                                                                                            |
| [**SearchPaths**](ivmvirtualpc-searchpaths.md)<br/>                                 | Leitura/gravação<br/> | os caminhos do sistema de arquivos que são usados para localizar arquivos associados a Windows Virtual PC.<br/>                                                      |
| [**SuggestedMaximumMemoryPerVM**](ivmvirtualpc-suggestedmaximummemorypervm.md)<br/> | Somente leitura<br/>  | A quantidade máxima permitida de memória física por máquina virtual sugerida, em megabytes, para evitar condições de memória insuficiente no host.<br/> |
| [**Tarefas**](ivmvirtualpc-tasks.md)<br/>                                             | Somente leitura<br/>  | Uma coleção de tarefas.<br/>                                                                                                                     |
| [**UnconnectedNetworkAdapters**](ivmvirtualpc-unconnectednetworkadapters.md)<br/>   | Somente leitura<br/>  | Uma coleção enumerável de interfaces de rede não conectadas.<br/>                                                                                |
| [**Uptime**](ivmvirtualpc-uptime.md)<br/>                                           | Somente leitura<br/>  | O número de segundos que o Windows aplicativo de computador virtual está em execução.<br/>                                                                 |
| [**USBDeviceCollection**](ivmvirtualpc-usbdevicecollection.md)<br/>                 | Somente leitura<br/>  | Uma coleção enumerável de todos os dispositivos USB conectados ao host.<br/>                                                                         |
| [**Versão**](ivmvirtualpc-version.md)<br/>                                         | Somente leitura<br/>  | A versão desta instância do Windows Virtual PC.<br/>                                                                                        |
| [**VirtualMachines**](ivmvirtualpc-virtualmachines.md)<br/>                         | Somente leitura<br/>  | Uma coleção enumerável de máquinas virtuais.<br/>                                                                                              |
| [**VirtualNetworks**](ivmvirtualpc-virtualnetworks.md)<br/>                         | Somente leitura<br/>  | Uma coleção enumerável de redes virtuais.<br/>                                                                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMVirtualPC é definido como \_ 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



 

