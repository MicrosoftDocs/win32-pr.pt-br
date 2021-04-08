---
description: A categoria hardware do sistema de computador agrupa as classes que representam objetos relacionados ao hardware. Os exemplos incluem dispositivos de entrada, discos rígidos, placas de expansão, dispositivos de vídeo, dispositivos de rede e energia do sistema.
ms.assetid: 0b6cb410-166e-45cd-8dca-77a111b3cf62
ms.tgt_platform: multiple
title: Classes de hardware do sistema de computador
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a3681f78d882a3e977b9721bd70f0b852114c257
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920379"
---
# <a name="computer-system-hardware-classes"></a>Classes de hardware do sistema de computador

A categoria hardware do sistema de computador agrupa as classes que representam objetos relacionados ao hardware. Os exemplos incluem dispositivos de entrada, discos rígidos, placas de expansão, dispositivos de vídeo, dispositivos de rede e energia do sistema.

-   [Classes de dispositivo de resfriamento](#cooling-device-classes)
-   [Classes de dispositivo de entrada](#input-device-classes)
-   [Classes de armazenamento em massa](#mass-storage-classes)
-   [Classes de placa-mãe, controlador e porta](#motherboard-controller-and-port-classes)
-   [Classes de dispositivo de rede](#networking-device-classes)
-   [Classes de energia](#power-classes)
-   [Classes de impressão](#printing-classes)
-   [Classes de telefonia](#telephony-classes)
-   [Classes de vídeo e monitor](#video-and-monitor-classes)
-   [Tópicos relacionados](#related-topics)

## <a name="cooling-device-classes"></a>Classes de dispositivo de resfriamento

A subcategoria dispositivos de resfriamento agrupa classes que representam ventiladores instrumentados, investigações de temperatura e dispositivos de refrigeração.



| Classe                                                     | Descrição                                                                 |
|-----------------------------------------------------------|-----------------------------------------------------------------------------|
| [**\_Ventilador do Win32**](win32-fan.md)                           | Representa as propriedades de um dispositivo de ventilador no sistema de computador.           |
| [**\_HeatPipe Win32**](win32-heatpipe.md)                 | Representa as propriedades de um dispositivo de resfriamento de tubo de calor.                    |
| [**\_Refrigeração Win32**](win32-refrigeration.md)       | Representa as propriedades de um dispositivo de refrigeração.                        |
| [**\_TemperatureProbe Win32**](win32-temperatureprobe.md) | Representa as propriedades de um sensor de temperatura (termômetro eletrônico). |



 

## <a name="input-device-classes"></a>Classes de dispositivo de entrada

A subcategoria dispositivos de entrada agrupa as classes que representam teclados e dispositivos apontadores.



| Classe                                                 | Descrição                                                                                                         |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**\_Teclado Win32**](win32-keyboard.md)             | Representa um teclado instalado em um sistema de computador que executa o Windows.                                               |
| [**\_PointingDevice Win32**](win32-pointingdevice.md) | Representa um dispositivo de entrada usado para apontar e selecionar regiões na exibição de um sistema de computador executando o Windows. |



 

## <a name="mass-storage-classes"></a>Classes de armazenamento em massa

As classes na subcategoria de armazenamento em massa representam dispositivos de armazenamento como unidades de disco rígido, unidades de CD-ROM e unidades de fita.



| Classe                                                     | Descrição                                                                                  |
|-----------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**\_AutochkSetting Win32**](win32-autochksetting.md)     | Representa as configurações da operação de verificação automarca de um disco.                               |
| [**\_CDROMDrive Win32**](win32-cdromdrive.md)             | Representa uma unidade de CD-ROM em um sistema de computador que executa o Windows.                              |
| [**\_DiskDrive Win32**](win32-diskdrive.md)               | Representa uma unidade de disco físico, como visto por um computador que executa o sistema operacional Windows. |
| [**\_FloppyDrive Win32**](win32-floppydrive.md)           | Gerencia os recursos de uma unidade de disquete.                                             |
| [**\_PhysicalMedia Win32**](/previous-versions/windows/desktop/cimwin32a/win32-physicalmedia) | Representa qualquer tipo de documentação ou mídia de armazenamento.                                      |
| [**\_TapeDrive Win32**](win32-tapedrive.md)               | Representa uma unidade de fita em um sistema de computador que executa o Windows.                                |



 

## <a name="motherboard-controller-and-port-classes"></a>Classes de placa-mãe, controlador e porta

As classes de subcategoria de placa-mãe, controladores e portas que representam os dispositivos do sistema. Os exemplos incluem memória do sistema, memória de cache e controladores.



| Classe                                                                       | Descrição                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_1394Controller Win32**](win32-1394controller.md)                       | Representa os recursos e o gerenciamento de um controlador 1394.<br/>                                                                                                                                               |
| [**\_1394ControllerDevice Win32**](win32-1394controllerdevice.md)           | Relaciona o controlador de barramento serial de alta velocidade (IEEE 1394 Firewire) e a instância [**de \_ LogicalDevice CIM**](cim-logicaldevice.md) conectada a ele.<br/>                                                            |
| [**\_AllocatedResource Win32**](win32-allocatedresource.md)                 | Relaciona um dispositivo lógico a um recurso do sistema.<br/>                                                                                                                                                                 |
| [**\_AssociatedProcessorMemory Win32**](win32-associatedprocessormemory.md) | Relaciona um processador e sua memória de cache.<br/>                                                                                                                                                                      |
| [**Placa-base do Win32 \_**](win32-baseboard.md)                                 | Representa uma base (também conhecida como placa-mãe ou placa do sistema).<br/>                                                                                                                                          |
| [**\_BIOS Win32**](win32-bios.md)                                           | Representa os atributos dos serviços de entrada ou saída básicos (BIOS) do sistema de computador que estão instalados no computador.<br/>                                                                                   |
| [**\_Barramento Win32**](win32-bus.md)                                             | Representa um barramento físico como visto por um sistema operacional Windows.<br/>                                                                                                                                               |
| [**\_CacheMemory Win32**](win32-cachememory.md)                             | Representa a memória cache (interna e externa) em um sistema de computador.<br/>                                                                                                                                          |
| [**\_ControllerHasHub Win32**](/previous-versions/windows/desktop/cimwin32a/win32-controllerhashub)             | Representa os hubs downstream do controlador USB (barramento serial universal).<br/>                                                                                                                                 |
| [**\_DeviceBus Win32**](win32-devicebus.md)                                 | Relaciona um barramento do sistema e um dispositivo lógico usando o barramento.<br/>                                                                                                                                                       |
| [**\_DeviceMemoryAddress Win32**](win32-devicememoryaddress.md)             | Representa um endereço de memória do dispositivo em um sistema Windows.<br/>                                                                                                                                                        |
| [**\_DeviceSettings Win32**](win32-devicesettings.md)                       | Relaciona um dispositivo lógico e uma configuração que pode ser aplicada a ele.<br/>                                                                                                                                              |
| [**\_DMAChannel Win32**](win32-dmachannel.md)                               | Representa um canal de DMA (acesso direto à memória) em um sistema de computador executando o Windows.<br/>                                                                                                                          |
| [**\_FloppyController Win32**](win32-floppycontroller.md)                   | Representa os recursos e a capacidade de gerenciamento de um controlador de unidade de disquete.<br/>                                                                                                                         |
| [**\_IDEController Win32**](win32-idecontroller.md)                         | Representa os recursos de um dispositivo de controlador IDE (Integrated Drive Electronics).<br/>                                                                                                                        |
| [**\_IDEControllerDevice Win32**](win32-idecontrollerdevice.md)             | Classe de associação que relaciona um controlador IDE e o dispositivo lógico.<br/>                                                                                                                                       |
| [**\_InfraredDevice Win32**](win32-infrareddevice.md)                       | Representa os recursos e o gerenciamento de um dispositivo de infravermelho.<br/>                                                                                                                                              |
| [**\_IRQResource Win32**](win32-irqresource.md)                             | Representa um número de IRQ (linha de solicitação de interrupção) em um sistema de computador Windows.<br/>                                                                                                                                |
| [**\_MemoryArray Win32**](win32-memoryarray.md)                             | Representa as propriedades da matriz de memória e dos endereços mapeados do sistema de computador.<br/>                                                                                                                            |
| [**\_MemoryArrayLocation Win32**](win32-memoryarraylocation.md)             | Relaciona uma matriz de memória lógica e a matriz de memória física na qual ela existe.<br/>                                                                                                                             |
| [**\_MemoryDevice Win32**](win32-memorydevice.md)                           | Representa as propriedades do dispositivo de memória de um sistema de computador junto com seus endereços mapeados associados.<br/>                                                                                                     |
| [**\_MemoryDeviceArray Win32**](win32-memorydevicearray.md)                 | Relaciona um dispositivo de memória e a matriz de memória na qual ele reside.<br/>                                                                                                                                              |
| [**\_MemoryDeviceLocation Win32**](win32-memorydevicelocation.md)           | Classe de associação que relaciona um dispositivo de memória e a memória física na qual ele existe.<br/>                                                                                                                     |
| [**\_MotherboardDevice Win32**](win32-motherboarddevice.md)                 | Representa um dispositivo que contém os componentes centrais do sistema de computador que executa o Windows.<br/>                                                                                                               |
| [**\_OnBoardDevice Win32**](win32-onboarddevice.md)                         | Representa dispositivos de adaptador comum incorporados à placa-mãe (placa do sistema).<br/>                                                                                                                                   |
| [**\_ParallelPort Win32**](win32-parallelport.md)                           | Representa as propriedades de uma porta paralela em um sistema de computador que executa o Windows.<br/>                                                                                                                             |
| [**\_PCMCIAController Win32**](win32-pcmciacontroller.md)                   | Gerencia os recursos de um dispositivo de controlador PCMCIA (adaptador de interface de cartão de memória) do computador pessoal.<br/>                                                                                                      |
| [**\_PhysicalMemory Win32**](win32-physicalmemory.md)                       | Representa um dispositivo de memória física localizado em um computador como disponível para o sistema operacional.<br/>                                                                                                                |
| [**\_PhysicalMemoryArray Win32**](win32-physicalmemoryarray.md)             | Representa detalhes sobre a memória física do sistema do computador.<br/>                                                                                                                                                |
| [**\_PhysicalMemoryLocation Win32**](win32-physicalmemorylocation.md)       | Relaciona uma matriz de memória física e sua memória física.<br/>                                                                                                                                                   |
| [**\_PNPAllocatedResource Win32**](win32-pnpallocatedresource.md)           | Representa uma associação entre dispositivos lógicos e recursos do sistema.<br/>                                                                                                                                        |
| [**\_PNPDevice Win32**](win32-pnpdevice.md)                                 | Relaciona um dispositivo (conhecido para Configuration Manager como um PNPEntity) e a função que ele executa.<br/>                                                                                                                |
| [**\_PNPEntity Win32**](win32-pnpentity.md)                                 | Representa as propriedades de um dispositivo Plug and Play.<br/>                                                                                                                                                           |
| [**\_PortConnector Win32**](win32-portconnector.md)                         | Representa portas de conexão física, como DB-25 Pin masculino, Centronics e PS/2.<br/>                                                                                                                            |
| [**\_PortResource Win32**](win32-portresource.md)                           | Representa uma porta de e/s em um sistema de computador que executa o Windows.<br/>                                                                                                                                                   |
| [**\_Processador Win32**](win32-processor.md)                                 | Representa um dispositivo capaz de interpretar uma sequência de instruções de máquina em um sistema de computador executando o Windows.<br/>                                                                                           |
| [**\_SCSIController Win32**](win32-scsicontroller.md)                       | Representa um controlador de interface de sistema de computador pequeno (SCSI) em um sistema de computador executando o Windows.<br/>                                                                                                           |
| [**\_SCSIControllerDevice Win32**](win32-scsicontrollerdevice.md)           | Relaciona um controlador SCSI e o dispositivo lógico (unidade de disco) conectado a ele.<br/>                                                                                                                                 |
| [**SerialPort do Win32 \_**](win32-serialport.md)                               | Representa uma porta serial em um sistema de computador que executa o Windows.<br/>                                                                                                                                                 |
| [**\_SerialPortConfiguration Win32**](win32-serialportconfiguration.md)     | Representa as configurações de transmissão de dados em uma porta serial do Windows.<br/>                                                                                                                                        |
| [**\_SerialPortSetting Win32**](win32-serialportsetting.md)                 | Relaciona uma porta serial e suas definições de configuração.<br/>                                                                                                                                                          |
| [**\_SMBIOSMemory Win32**](win32-smbiosmemory.md)                           | Representa os recursos e o gerenciamento de dispositivos lógicos relacionados à memória.<br/>                                                                                                                                  |
| [**\_SoundDevice Win32**](win32-sounddevice.md)                             | Representa as propriedades de um dispositivo de som em um sistema de computador que executa o Windows.<br/>                                                                                                                              |
| [**\_SystemBIOS Win32**](win32-systembios.md)                               | Relaciona um sistema de computador (incluindo dados como propriedades de inicialização, fusos horários, configurações de inicialização ou senhas administrativas) e um BIOS do sistema (serviços, linguagens e propriedades de gerenciamento do sistema).<br/> |
| [**\_SystemDriverPNPEntity Win32**](win32-systemdriverpnpentity.md)         | Relaciona um dispositivo Plug and Play no sistema de computador Windows e o driver que dá suporte ao dispositivo Plug and Play.<br/>                                                                                           |
| [**\_SystemEnclosure Win32**](win32-systemenclosure.md)                     | Representa as propriedades associadas a um compartimento de sistema físico.<br/>                                                                                                                                         |
| [**\_SystemMemoryResource Win32**](win32-systemmemoryresource.md)           | Representa um recurso de memória do sistema em um sistema Windows.<br/>                                                                                                                                                       |
| [**\_SystemSlot Win32**](win32-systemslot.md)                               | Representa pontos de conexão física, incluindo portas, slots de placa-mãe e periféricos, e pontos de conexões proprietárias.<br/>                                                                                  |
| [**\_USBController Win32**](win32-usbcontroller.md)                         | Gerencia os recursos de um controlador USB (barramento serial universal).<br/>                                                                                                                                           |
| [**\_USBControllerDevice Win32**](win32-usbcontrollerdevice.md)             | Relaciona um controlador USB e as instâncias de [**\_ LogicalDevice CIM**](cim-logicaldevice.md) conectadas a ele.<br/>                                                                                                    |
| [**\_USBHub Win32**](/previous-versions/windows/desktop/cimwin32a/win32-usbhub)                                 | Representa as características de gerenciamento de um hub USB.<br/>                                                                                                                                                        |



 

## <a name="networking-device-classes"></a>Classes de dispositivo de rede

A subcategoria dispositivos de rede agrupa classes que representam o controlador de interface de rede, suas configurações e suas configurações.



| Classe                                                                           | Descrição                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Adaptador Win32**](win32-networkadapter.md)                           | Representa um adaptador de rede em um sistema de computador que executa o Windows.<br/>                                                                                                                                          |
| [**\_NetworkAdapterConfiguration Win32**](win32-networkadapterconfiguration.md) | Representa os atributos e comportamentos de um adaptador de rede. A classe não tem garantia de suporte após o Ratification da especificação de rede CIM da DMTF (Distributed Management Task Force).<br/> |
| [**\_NetworkAdapterSetting Win32**](win32-networkadaptersetting.md)             | Relaciona um adaptador de rede e suas definições de configuração.<br/>                                                                                                                                                   |



 

## <a name="power-classes"></a>Classes de energia

A subcategoria de energia agrupa as classes que representam fontes de alimentação, baterias e eventos relacionados a esses dispositivos.



| Classe                                                             | Descrição                                                                                           |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**\_Bateria Win32**](win32-battery.md)                           | Representa uma bateria conectada ao sistema de computador.<br/>                                     |
| [**\_CurrentProbe Win32**](win32-currentprobe.md)                 | Representa as propriedades de um sensor de monitoramento atual (ammeter).<br/>                        |
| [**\_PortableBattery Win32**](win32-portablebattery.md)           | Representa as propriedades de uma bateria portátil, como uma usada para um computador notebook.<br/> |
| [**\_PowerManagementEvent Win32**](win32-powermanagementevent.md) | Representa os eventos de gerenciamento de energia resultantes de alterações de estado de energia.<br/>                     |
| [**\_VoltageProbe Win32**](win32-voltageprobe.md)                 | Representa as propriedades de um sensor de tensão (voltímetro eletrônico).<br/>                      |



 

## <a name="printing-classes"></a>Classes de impressão

A subcategoria de impressão agrupa classes que representam impressoras, configurações de impressora e trabalhos de impressão.



| Classe                                                             | Descrição                                                                                                                              |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_DriverForDevice Win32**](win32-driverfordevice.md)           | Relaciona uma impressora a um driver de impressora.<br/>                                                                                        |
| [**\_Impressora Win32**](win32-printer.md)                           | Representa um dispositivo conectado a um sistema de computador executando o Windows que é capaz de reproduzir uma imagem visual em um meio.<br/> |
| [**\_PrinterConfiguration Win32**](win32-printerconfiguration.md) | Define a configuração de um dispositivo de impressora.<br/>                                                                               |
| [**\_PrinterController Win32**](win32-printercontroller.md)       | Relaciona uma impressora e o dispositivo local ao qual a impressora está conectada.<br/>                                                     |
| [**\_PrinterDriver Win32**](win32-printerdriver.md)               | Representa os drivers para uma instância de [**\_ impressora Win32**](win32-printer.md) .<br/>                                                |
| [**\_PrinterDriverDll Win32**](win32-printerdriverdll.md)         | Relaciona uma impressora local e seu arquivo de driver (não o próprio driver).<br/>                                                          |
| [**\_PrinterSetting Win32**](win32-printersetting.md)             | Relaciona uma impressora e suas definições de configuração.<br/>                                                                             |
| [**PrintJob do Win32 \_**](win32-printjob.md)                         | Representa um trabalho de impressão gerado por um aplicativo baseado no Windows.<br/>                                                              |
| [**\_TCPIPPrinterPort Win32**](win32-tcpipprinterport.md)         | Representa um ponto de acesso do serviço TCP/IP.<br/>                                                                                     |



 

## <a name="telephony-classes"></a>Classes de telefonia

A subcategoria de telefonia agrupa classes que representam dispositivos de modem "telefone antigo" e suas conexões seriais associadas.



| Classe                                                               | Descrição                                                                                                                                |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_POTSModem Win32**](win32-potsmodem.md)                         | Representa os serviços e as características de um modem de serviço de telefonia (POTS) simples em um sistema de computador executando o Windows.<br/> |
| [**\_POTSModemToSerialPort Win32**](win32-potsmodemtoserialport.md) | Relaciona um modem e a porta serial que o modem usa.<br/>                                                                             |



 

## <a name="video-and-monitor-classes"></a>Classes de vídeo e monitor

A subcategoria vídeo e monitores agrupa as classes que representam monitores, placas de vídeo e suas configurações associadas.



| Classe                                                                                 | Descrição                                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_DesktopMonitor Win32**](win32-desktopmonitor.md)                                 | Representa o tipo de monitor ou dispositivo de exibição conectado ao sistema de computador.<br/>                                                                                                                                                                                                                                                                                       |
| [**\_DisplayControllerConfiguration Win32**](win32-displaycontrollerconfiguration.md) | Representa as informações de configuração do adaptador de vídeo de um sistema de computador executando o Windows. Essa classe está obsoleta. No lugar dessa classe, use as propriedades nas classes [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md)e [CIM \_ VideoControllerResolution](cim-videocontrollerresolution.md) .<br/> |
| [**\_VideoController Win32**](win32-videocontroller.md)                               | Representa os recursos e a capacidade de gerenciamento do controlador de vídeo em um sistema de computador executando o Windows.<br/>                                                                                                                                                                                                                                                       |
| [**\_VideoSettings Win32**](win32-videosettings.md)                                   | Relaciona um controlador de vídeo e as configurações de vídeo que podem ser aplicadas a ele.<br/>                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Classes Win32](/previous-versions//aa394084(v=vs.85))
</dt> </dl>

 

