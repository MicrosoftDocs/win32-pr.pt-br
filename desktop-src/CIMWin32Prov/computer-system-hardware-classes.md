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
ms.openlocfilehash: d541071698c08510452faaf6bef0cd706dab66e5eaa77b5db121e522785c5c4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118420091"
---
# <a name="computer-system-hardware-classes"></a>Classes de hardware do sistema de computador

A categoria hardware do sistema de computador agrupa as classes que representam objetos relacionados ao hardware. Os exemplos incluem dispositivos de entrada, discos rígidos, placas de expansão, dispositivos de vídeo, dispositivos de rede e energia do sistema.

-   [Classes de dispositivo de resfriamento](#cooling-device-classes)
-   [Classes de dispositivo de entrada](#input-device-classes)
-   [Classes de Armazenamento em massa](#mass-storage-classes)
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
| [**\_PointingDevice Win32**](win32-pointingdevice.md) | Representa um dispositivo de entrada usado para apontar e selecionar regiões na exibição de um sistema de computador que executa o Windows. |



 

## <a name="mass-storage-classes"></a>Classes de Armazenamento em massa

as Classes na subcategoria Armazenamento em massa representam dispositivos de armazenamento como unidades de disco rígido, unidades de CD-ROM e unidades de fita.



| Classe                                                     | Descrição                                                                                  |
|-----------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**\_AutochkSetting Win32**](win32-autochksetting.md)     | Representa as configurações da operação de verificação automarca de um disco.                               |
| [**\_CDROMDrive Win32**](win32-cdromdrive.md)             | Representa uma unidade de CD-ROM em um sistema de computador que executa o Windows.                              |
| [**\_DiskDrive Win32**](win32-diskdrive.md)               | representa uma unidade de disco físico, como visto por um computador que executa o sistema operacional Windows. |
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
| [**\_Barramento Win32**](win32-bus.md)                                             | representa um barramento físico como visto por um sistema operacional Windows.<br/>                                                                                                                                               |
| [**\_CacheMemory Win32**](win32-cachememory.md)                             | Representa a memória cache (interna e externa) em um sistema de computador.<br/>                                                                                                                                          |
| [**\_ControllerHasHub Win32**](/previous-versions/windows/desktop/cimwin32a/win32-controllerhashub)             | Representa os hubs downstream do controlador USB (barramento serial universal).<br/>                                                                                                                                 |
| [**\_DeviceBus Win32**](win32-devicebus.md)                                 | Relaciona um barramento do sistema e um dispositivo lógico usando o barramento.<br/>                                                                                                                                                       |
| [**\_DeviceMemoryAddress Win32**](win32-devicememoryaddress.md)             | representa um endereço de memória do dispositivo em um sistema Windows.<br/>                                                                                                                                                        |
| [**\_DeviceSettings Win32**](win32-devicesettings.md)                       | Relaciona um dispositivo lógico e uma configuração que pode ser aplicada a ele.<br/>                                                                                                                                              |
| [**\_DMAChannel Win32**](win32-dmachannel.md)                               | Representa um canal de DMA (acesso direto à memória) em um sistema de computador que executa o Windows.<br/>                                                                                                                          |
| [**\_FloppyController Win32**](win32-floppycontroller.md)                   | Representa os recursos e a capacidade de gerenciamento de um controlador de unidade de disquete.<br/>                                                                                                                         |
| [**\_IDEController Win32**](win32-idecontroller.md)                         | Representa os recursos de um dispositivo de controlador IDE (Integrated Drive Electronics).<br/>                                                                                                                        |
| [**\_IDEControllerDevice Win32**](win32-idecontrollerdevice.md)             | Classe de associação que relaciona um controlador IDE e o dispositivo lógico.<br/>                                                                                                                                       |
| [**\_InfraredDevice Win32**](win32-infrareddevice.md)                       | Representa os recursos e o gerenciamento de um dispositivo de infravermelho.<br/>                                                                                                                                              |
| [**\_IRQResource Win32**](win32-irqresource.md)                             | representa um número de IRQ (linha de solicitação de interrupção) em um sistema de computador Windows.<br/>                                                                                                                                |
| [**\_MemoryArray Win32**](win32-memoryarray.md)                             | Representa as propriedades da matriz de memória e dos endereços mapeados do sistema de computador.<br/>                                                                                                                            |
| [**\_MemoryArrayLocation Win32**](win32-memoryarraylocation.md)             | Relaciona uma matriz de memória lógica e a matriz de memória física na qual ela existe.<br/>                                                                                                                             |
| [**\_MemoryDevice Win32**](win32-memorydevice.md)                           | Representa as propriedades do dispositivo de memória de um sistema de computador junto com seus endereços mapeados associados.<br/>                                                                                                     |
| [**\_MemoryDeviceArray Win32**](win32-memorydevicearray.md)                 | Relaciona um dispositivo de memória e a matriz de memória na qual ele reside.<br/>                                                                                                                                              |
| [**Win32 \_ MemoryDeviceLocation**](win32-memorydevicelocation.md)           | Classe de associação que relaciona um dispositivo de memória e a memória física em que ele existe.<br/>                                                                                                                     |
| [**Win32 \_ MotherboardDevice**](win32-motherboarddevice.md)                 | Representa um dispositivo que contém os componentes centrais do sistema de computador que executa Windows.<br/>                                                                                                               |
| [**Win32 \_ OnBoardDevice**](win32-onboarddevice.md)                         | Representa dispositivos de adaptador comuns integrados à placa-mãe (placa-mãe do sistema).<br/>                                                                                                                                   |
| [**Win32 \_ ParallelPort**](win32-parallelport.md)                           | Representa as propriedades de uma porta paralela em um sistema de computador executando Windows.<br/>                                                                                                                             |
| [**Win32 \_ PCMCIAController**](win32-pcmciacontroller.md)                   | Gerencia os recursos de um dispositivo de controlador PCMCIA (Adaptador de Placa de Memória do Computador Pessoal).<br/>                                                                                                      |
| [**Win32 \_ PhysicalMemory**](win32-physicalmemory.md)                       | Representa um dispositivo de memória física localizado em um computador, conforme disponível para o sistema operacional.<br/>                                                                                                                |
| [**Win32 \_ PhysicalMemoryArray**](win32-physicalmemoryarray.md)             | Representa detalhes sobre a memória física do sistema de computador.<br/>                                                                                                                                                |
| [**Win32 \_ PhysicalMemoryLocation**](win32-physicalmemorylocation.md)       | Relaciona uma matriz de memória física e sua memória física.<br/>                                                                                                                                                   |
| [**Win32 \_ PNPAllocatedResource**](win32-pnpallocatedresource.md)           | Representa uma associação entre dispositivos lógicos e recursos do sistema.<br/>                                                                                                                                        |
| [**Win32 \_ PNPDevice**](win32-pnpdevice.md)                                 | Relaciona um dispositivo (conhecido como Gerenciador de Configurações como um PNPEntity) e a função que ele executa.<br/>                                                                                                                |
| [**Win32 \_ PNPEntity**](win32-pnpentity.md)                                 | Representa as propriedades de um Plug and Play dispositivo.<br/>                                                                                                                                                           |
| [**Win32 \_ PortConnector**](win32-portconnector.md)                         | Representa portas de conexão físicas, como pin DB-25, Centronics e PS/2.<br/>                                                                                                                            |
| [**Win32 \_ PortResource**](win32-portresource.md)                           | Representa uma porta de E/S em um sistema de computador executando Windows.<br/>                                                                                                                                                   |
| [**Processador \_ Win32**](win32-processor.md)                                 | Representa um dispositivo capaz de interpretar uma sequência de instruções do computador em um sistema de computador executando Windows.<br/>                                                                                           |
| [**Win32 \_ SCSIController**](win32-scsicontroller.md)                       | Representa um pequeno controlador SCSI (interface do sistema de computador) em um sistema de computador executando Windows.<br/>                                                                                                           |
| [**Win32 \_ SCSIControllerDevice**](win32-scsicontrollerdevice.md)           | Relaciona um controlador SCSI e o dispositivo lógico (unidade de disco) conectado a ele.<br/>                                                                                                                                 |
| [**Win32 \_ SerialPort**](win32-serialport.md)                               | Representa uma porta serial em um sistema de computador executando Windows.<br/>                                                                                                                                                 |
| [**Win32 \_ SerialPortConfiguration**](win32-serialportconfiguration.md)     | Representa as configurações de transmissão de dados em uma Windows serial.<br/>                                                                                                                                        |
| [**Win32 \_ SerialPortSetting**](win32-serialportsetting.md)                 | Relaciona uma porta serial e suas definições de configuração.<br/>                                                                                                                                                          |
| [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md)                           | Representa os recursos e o gerenciamento de dispositivos lógicos relacionados à memória.<br/>                                                                                                                                  |
| [**Win32 \_ SoundDevice**](win32-sounddevice.md)                             | Representa as propriedades de um dispositivo de som em um sistema de computador executando Windows.<br/>                                                                                                                              |
| [**SystemBIOS do Win32 \_**](win32-systembios.md)                               | Relaciona um sistema de computador (incluindo dados como propriedades de inicialização, fusos horário, configurações de inicialização ou senhas administrativas) e um BIOS do sistema (serviços, idiomas e propriedades de gerenciamento do sistema).<br/> |
| [**Win32 \_ SystemDriverPNPEntity**](win32-systemdriverpnpentity.md)         | Relaciona um Plug and Play no sistema Windows computador e o driver que dá suporte ao Plug and Play dispositivo.<br/>                                                                                           |
| [**Win32 \_ SystemEnclosure**](win32-systemenclosure.md)                     | Representa as propriedades associadas a um compartimento do sistema físico.<br/>                                                                                                                                         |
| [**Win32 \_ SystemMemoryResource**](win32-systemmemoryresource.md)           | Representa um recurso de memória do sistema em um Windows sistema.<br/>                                                                                                                                                       |
| [**Win32 \_ SystemSlot**](win32-systemslot.md)                               | Representa pontos de conexão físicos, incluindo portas, slots de placa-mãe e periféricos e pontos de conexões proprietários.<br/>                                                                                  |
| [**Win32 \_ USBController**](win32-usbcontroller.md)                         | Gerencia os recursos de um controlador usb (barramento serial universal).<br/>                                                                                                                                           |
| [**Win32 \_ USBControllerDevice**](win32-usbcontrollerdevice.md)             | Relaciona um controlador USB e as instâncias [**\_ LogicalDevice cim**](cim-logicaldevice.md) conectadas a ele.<br/>                                                                                                    |
| [**Win32 \_ USBHub**](/previous-versions/windows/desktop/cimwin32a/win32-usbhub)                                 | Representa as características de gerenciamento de um hub USB.<br/>                                                                                                                                                        |



 

## <a name="networking-device-classes"></a>Classes de dispositivo de rede

A subcategoria Dispositivos de Rede grupos classes que representam o controlador de interface de rede, suas configurações e suas configurações.



| Classe                                                                           | Descrição                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ NetworkAdapter**](win32-networkadapter.md)                           | Representa um adaptador de rede em um sistema de computador executando Windows.<br/>                                                                                                                                          |
| [**Win32 \_ NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md) | Representa os atributos e comportamentos de um adaptador de rede. Não há garantia de que a classe seja suportada após a especificação de rede CIM da DMTF (Distributed Management Task Force).<br/> |
| [**Win32 \_ NetworkAdapterSetting**](win32-networkadaptersetting.md)             | Relaciona um adaptador de rede e suas definições de configuração.<br/>                                                                                                                                                   |



 

## <a name="power-classes"></a>Classes de energia

A subcategoria Power grupos classes que representam fontes de alimentação, baterias e eventos relacionados a esses dispositivos.



| Classe                                                             | Descrição                                                                                           |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**Bateria \_ win32**](win32-battery.md)                           | Representa uma bateria conectada ao sistema de computador.<br/>                                     |
| [**Win32 \_ CurrentProbe**](win32-currentprobe.md)                 | Representa as propriedades de um sensor de monitoramento atual (ammeter).<br/>                        |
| [**Win32 \_ PortableBattery**](win32-portablebattery.md)           | Representa as propriedades de uma bateria portátil, como uma usada para um computador de notebook.<br/> |
| [**Win32 \_ PowerManagementEvent**](win32-powermanagementevent.md) | Representa eventos de gerenciamento de energia resultantes de alterações de estado de energia.<br/>                     |
| [**Win32 \_ VoltageProbe**](win32-voltageprobe.md)                 | Representa as propriedades de um sensor de tensão (meter eletrônico).<br/>                      |



 

## <a name="printing-classes"></a>Classes de impressão

A subcategoria Impressão grupos classes que representam impressoras, configurações de impressora e trabalhos de impressão.



| Classe                                                             | Descrição                                                                                                                              |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ DriverForDevice**](win32-driverfordevice.md)           | Relaciona uma impressora a um driver de impressora.<br/>                                                                                        |
| [**Impressora \_ Win32**](win32-printer.md)                           | Representa um dispositivo conectado a um sistema de computadores Windows que é capaz de reproduzir uma imagem visual em uma mídia.<br/> |
| [**Impressora \_ Win32Configuration**](win32-printerconfiguration.md) | Define a configuração de um dispositivo de impressora.<br/>                                                                               |
| [**Impressora \_ Win32Controller**](win32-printercontroller.md)       | Relaciona uma impressora e o dispositivo local ao qual a impressora está conectada.<br/>                                                     |
| [**Win32 \_ PrinterDriver**](win32-printerdriver.md)               | Representa os drivers para uma [**instância da Impressora Win32. \_**](win32-printer.md)<br/>                                                |
| [**Impressora \_ Win32DriverDll**](win32-printerdriverdll.md)         | Relaciona uma impressora local e seu arquivo de driver (não o próprio driver).<br/>                                                          |
| [**Impressora \_ Win32Conjunto**](win32-printersetting.md)             | Relaciona uma impressora e suas definições de configuração.<br/>                                                                             |
| [**Win32 \_ PrintJob**](win32-printjob.md)                         | Representa um trabalho de impressão gerado por um Windows baseado em dados.<br/>                                                              |
| [**Win32 \_ TCPIPPrinterPort**](win32-tcpipprinterport.md)         | Representa um ponto de acesso do serviço TCP/IP.<br/>                                                                                     |



 

## <a name="telephony-classes"></a>Classes de telefonia

A subcategoria Telefonia grupos classes que representam dispositivos de modem "telefone antigo sem-valor" e suas conexões seriais associadas.



| Classe                                                               | Descrição                                                                                                                                |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ POTSModem**](win32-potsmodem.md)                         | Representa os serviços e as características de um modem DOLS (Plain Old Telephone Service) em um sistema de computador que executa Windows.<br/> |
| [**Win32 \_ POTSModemToSerialPort**](win32-potsmodemtoserialport.md) | Relaciona um modem e a porta serial que o modem usa.<br/>                                                                             |



 

## <a name="video-and-monitor-classes"></a>Classes de vídeo e monitor

As classes de subcategoria Vídeo e Monitores que representam monitores, placas de vídeo e suas configurações associadas.



| Classe                                                                                 | Descrição                                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md)                                 | Representa o tipo de monitor ou dispositivo de exibição anexado ao sistema de computador.<br/>                                                                                                                                                                                                                                                                                       |
| [**Win32 \_ DisplayControllerConfiguration**](win32-displaycontrollerconfiguration.md) | Representa as informações de configuração do adaptador de vídeo de um sistema de computador executando Windows. Essa classe está obsoleta. No lugar dessa classe, use as propriedades nas classes [**Win32 \_ VideoController,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md)e [CIM \_ VideoControllerResolution.](cim-videocontrollerresolution.md)<br/> |
| [**VideoController do Win32 \_**](win32-videocontroller.md)                               | Representa os recursos e a capacidade de gerenciamento do controlador de vídeo em um sistema de computador executando Windows.<br/>                                                                                                                                                                                                                                                       |
| [**VideoSettings do Win32 \_**](win32-videosettings.md)                                   | Relaciona um controlador de vídeo e configurações de vídeo que podem ser aplicadas a ele.<br/>                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Win32 Classes](/previous-versions//aa394084(v=vs.85))
</dt> </dl>

 

