---
title: Interfaces do Windows Virtual PC
description: As interfaces a seguir têm suporte do Windows Virtual PC.
ms.assetid: de003075-8609-4303-838e-da449b91dc8d
keywords:
- PC Virtual PC do Windows, interfaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4a505fab360214d92b844c282fe12722281770f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105794593"
---
# <a name="windows-virtual-pc-interfaces"></a>Interfaces do Windows Virtual PC

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

As interfaces a seguir têm suporte do Windows Virtual PC.



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
| [**IVMVirtualMachineCollection**](ivmvirtualmachinecollection.md)<br/>         | Define a coleção de VMs no Windows Virtual PC.<br/>                                               |
| [**IVMVirtualMachineEvents**](ivmvirtualmachineevents.md)<br/>                 | Define a interface de evento de saída para a interface [**IVMVirtualMachine**](ivmvirtualmachine.md) .<br/> |
| [**IVMVirtualNetwork**](ivmvirtualnetwork.md)<br/>                             | Define uma rede virtual.<br/>                                                                             |
| [**IVMVirtualNetworkCollection**](ivmvirtualnetworkcollection.md)<br/>         | Define uma coleção de objetos [**IVMVirtualNetwork**](ivmvirtualnetwork.md) .<br/>                        |
| [**IVMVirtualPC**](ivmvirtualpc.md)<br/>                                       | Define o objeto de aplicativo do Windows Virtual PC de nível superior.<br/>                                           |
| [**IVMVirtualPCEvents**](ivmvirtualpcevents.md)<br/>                           | Define a interface de evento de saída para a interface [**IVMVirtualPC**](ivmvirtualpc.md) .<br/>           |



 

## <a name="note-for-developers-on-64-bit-windows"></a>Observação para desenvolvedores em Windows de 64 bits

Nas edições de 64 bits do Windows, a biblioteca de tipos para o Windows Virtual PC está em um binário de 64 bits (VPC.exe) no diretório% WinDir% \\ System32. Esse diretório não é visível por padrão para processos de 32 bits; O WOW64 mapeia todo o acesso ao diretório% WinDir% \\ System32 para o diretório% windir% \\ SysWOW64 por padrão. O Visual Studio é um binário de 32 bits e, portanto, não pode abrir o arquivo neste local. Para gerar um assembly de interoperabilidade para o Windows Virtual PC, use TlbImp.exe, que vem com o Visual Studio e o SDK do Windows. Para gerar *Microsoft.VirtualPC.Interop.dll*, use a seguinte linha de comando:

**TlbImp.exe/out: * * * Microsoft.VirtualPC.Interop.dll* **/namespace: Microsoft. VirtualPC. Interop% WinDir% \\ System32 \\VPC.exe**

Outras soluções incluem copiar VPC.exe para um diretório diferente onde o compilador pode encontrá-lo, ou usar a ferramenta de OleView.exe da SDK do Windows para extrair um arquivo. idl da biblioteca de tipos no VPC.exe.

 

