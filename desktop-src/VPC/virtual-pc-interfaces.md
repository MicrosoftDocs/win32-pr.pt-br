---
title: Windows Interfaces do Virtual PC
description: as interfaces a seguir têm suporte pelo Windows Virtual PC.
ms.assetid: de003075-8609-4303-838e-da449b91dc8d
keywords:
- Windows Virtual PC Virtual PC, interfaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 963574a5293a7c48b29096e3dbc563c0f2073c7a697f84a86fa0b5750feeabe9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119511756"
---
# <a name="windows-virtual-pc-interfaces"></a>Windows Interfaces do Virtual PC

\[Windows O Virtual PC não está mais disponível para uso a partir de Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

as interfaces a seguir têm suporte pelo Windows Virtual PC.



| Interface                                                                             | Descrição                                                                                                       |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [**IVMAccountant**](ivmaccountant.md)<br/>                                     | Fornece acesso a informações relacionadas à contabilidade para uma VM (máquina virtual).<br/>                          |
| [**IVMDisplay**](ivmdisplay.md)<br/>                                           | Controla as configurações de exibição de uma VM.<br/>                                                                 |
| [**IVMDVDDrive**](ivmdvddrive.md)<br/>                                         | Controla uma unidade de CD-ROM ou DVD-ROM em uma VM.<br/>                                                        |
| [**IVMDVDDriveCollection**](ivmdvddrivecollection.md)<br/>                     | Define a coleção de unidades de CD e DVD na VM.<br/>                                             |
| [**IVMDVDDriveEvents**](ivmdvddriveevents.md)<br/>                             | Define a interface de evento de saída para a interface [**IVMDVDDrive**](ivmdvddrive.md) .<br/>             |
| [**IVMFloppyDrive**](ivmfloppydrive.md)<br/>                                   | Controla uma unidade de disquete em uma VM.<br/>                                                                   |
| [**IVMFloppyDriveCollection**](ivmfloppydrivecollection.md)<br/>               | Define uma coleção de unidades de disquete na VM.<br/>                                                   |
| [**IVMFloppyDriveEvents**](ivmfloppydriveevents.md)<br/>                       | Define a interface de evento de saída para a interface [**IVMFloppyDrive**](ivmfloppydrive.md) .<br/>       |
| [**IVMGuestOS**](ivmguestos.md)<br/>                                           | Define o sistema operacional convidado em execução dentro de uma VM.<br/>                                                |
| [**IVMHardDisk**](ivmharddisk.md)<br/>                                         | Fornece acesso a uma imagem de disco rígido.<br/>                                                                  |
| [**IVMHardDiskConnection**](ivmharddiskconnection.md)<br/>                     | Define a conexão para um disco rígido dentro da VM.<br/>                                                  |
| [**IVMHardDiskConnectionCollection**](ivmharddiskconnectioncollection.md)<br/> | Define a coleção de conexões de disco rígido na VM.<br/>                                         |
| [**IVMHostInfo**](ivmhostinfo.md)<br/>                                         | Recupera informações sobre o computador host.<br/>                                                          |
| [**IVMKeyboard**](ivmkeyboard.md)<br/>                                         | Controla o dispositivo de teclado em uma VM.<br/>                                                              |
| [**IVMMouse**](ivmmouse.md)<br/>                                               | Controla o dispositivo de mouse em uma VM.<br/>                                                                 |
| [**IVMNetworkAdapter**](ivmnetworkadapter.md)<br/>                             | Serve como a interface para uma NIC (placa de interface de rede) virtual em uma VM.<br/>                         |
| [**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md)<br/>         | Define uma coleção de NICs virtuais em uma VM.<br/>                                                      |
| [**IVMParallelPort**](ivmparallelport.md)<br/>                                 | Define uma porta paralela dentro de uma VM.<br/>                                                                   |
| [**IVMParallelPortCollection**](ivmparallelportcollection.md)<br/>             | Define a coleção de portas paralelas na VM.<br/>                                                |
| [**IVMSerialPort**](ivmserialport.md)<br/>                                     | Define uma porta serial dentro de uma VM.<br/>                                                                     |
| [**IVMSerialPortCollection**](ivmserialportcollection.md)<br/>                 | Define a coleção de portas seriais na VM.<br/>                                                  |
| [**IVMTask**](ivmtask.md)<br/>                                                 | Usado para monitorar e controlar tarefas assíncronas para vários métodos.<br/>                                    |
| [**IVMTaskCollection**](ivmtaskcollection.md)<br/>                             | Define a coleção de objetos de tarefa em uma VM.<br/>                                                    |
| [**IVMUSBDevice**](ivmusbdevice.md)<br/>                                       | Define a interface para um dispositivo USB conectado ao sistema host.<br/>                                    |
| [**IVMUSBDeviceCollection**](ivmusbdevicecollection.md)<br/>                   | Define a coleção de dispositivos USB conectados ao sistema host.<br/>                                     |
| [**IVMVirtualMachine**](ivmvirtualmachine.md)<br/>                             | Define a interface para uma VM.<br/>                                                                        |
| [**IVMVirtualMachineCollection**](ivmvirtualmachinecollection.md)<br/>         | define a coleção de VMs dentro do Windows Virtual PC.<br/>                                               |
| [**IVMVirtualMachineEvents**](ivmvirtualmachineevents.md)<br/>                 | Define a interface de evento de saída para a interface [**IVMVirtualMachine**](ivmvirtualmachine.md) .<br/> |
| [**IVMVirtualNetwork**](ivmvirtualnetwork.md)<br/>                             | Define uma rede virtual.<br/>                                                                             |
| [**IVMVirtualNetworkCollection**](ivmvirtualnetworkcollection.md)<br/>         | Define uma coleção de objetos [**IVMVirtualNetwork**](ivmvirtualnetwork.md) .<br/>                        |
| [**IVMVirtualPC**](ivmvirtualpc.md)<br/>                                       | define o objeto de aplicativo Windows Virtual PC de nível superior.<br/>                                           |
| [**IVMVirtualPCEvents**](ivmvirtualpcevents.md)<br/>                           | Define a interface de evento de saída para a interface [**IVMVirtualPC**](ivmvirtualpc.md) .<br/>           |



 

## <a name="note-for-developers-on-64-bit-windows"></a>Observação para desenvolvedores em Windows de 64 bits

nas edições de 64 bits do Windows, a biblioteca de tipos para Windows Virtual PC está em um binário de 64 bits (VPC.exe) no diretório% WinDir% \\ System32. Esse diretório não é visível por padrão para processos de 32 bits; O WOW64 mapeia todo o acesso ao diretório% WinDir% \\ System32 para o diretório% windir% \\ SysWOW64 por padrão. Visual Studio é um binário de 32 bits e, portanto, não pode abrir o arquivo neste local. para gerar um assembly de interoperabilidade para Windows Virtual PC, use TlbImp.exe, que vem com Visual Studio e SDK do Windows. Para gerar *Microsoft.VirtualPC.Interop.dll*, use a seguinte linha de comando:

**TlbImp.exe/out:** _Microsoft.VirtualPC.Interop.dll_ **/namespace: Microsoft. VirtualPC. Interop% windir% \\ System32 \\VPC.exe**

outras soluções incluem copiar VPC.exe para um diretório diferente onde o compilador pode encontrá-lo, ou usar a ferramenta de OleView.exe da SDK do Windows para extrair um arquivo. idl da biblioteca de tipos no VPC.exe.

 

