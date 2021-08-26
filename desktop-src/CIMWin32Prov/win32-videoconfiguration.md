---
description: A classe \_ VideoConfiguration win32 não está ativa. Ele não retornará nenhuma instância, pois não há nenhum provedor que o retorne.
ms.assetid: 8dd15e8a-ff9b-4e75-bae9-8c80548301ab
ms.tgt_platform: multiple
title: Win32_VideoConfiguration classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_VideoConfiguration
- Win32_VideoConfiguration.Caption
- Win32_VideoConfiguration.Description
- Win32_VideoConfiguration.SettingID
- Win32_VideoConfiguration.ActualColorResolution
- Win32_VideoConfiguration.AdapterChipType
- Win32_VideoConfiguration.AdapterCompatibility
- Win32_VideoConfiguration.AdapterDACType
- Win32_VideoConfiguration.AdapterDescription
- Win32_VideoConfiguration.AdapterRAM
- Win32_VideoConfiguration.AdapterType
- Win32_VideoConfiguration.BitsPerPixel
- Win32_VideoConfiguration.ColorPlanes
- Win32_VideoConfiguration.ColorTableEntries
- Win32_VideoConfiguration.DeviceSpecificPens
- Win32_VideoConfiguration.DriverDate
- Win32_VideoConfiguration.HorizontalResolution
- Win32_VideoConfiguration.InfFilename
- Win32_VideoConfiguration.InfSection
- Win32_VideoConfiguration.InstalledDisplayDrivers
- Win32_VideoConfiguration.MonitorManufacturer
- Win32_VideoConfiguration.MonitorType
- Win32_VideoConfiguration.Name
- Win32_VideoConfiguration.PixelsPerXLogicalInch
- Win32_VideoConfiguration.PixelsPerYLogicalInch
- Win32_VideoConfiguration.RefreshRate
- Win32_VideoConfiguration.ScanMode
- Win32_VideoConfiguration.ScreenHeight
- Win32_VideoConfiguration.ScreenWidth
- Win32_VideoConfiguration.SystemPaletteEntries
- Win32_VideoConfiguration.VerticalResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7d951a8927458fa12398682ce63963dd71949d70e4db3a426dfc93ad14c78bf7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922616"
---
# <a name="win32_videoconfiguration-class"></a>Classe \_ VideoConfiguration do Win32

A **classe \_ VideoConfiguration win32** não está ativa. Ele não retornará nenhuma instância, pois não há nenhum provedor que o retorne.

A **classe \_ VideoConfiguration do Win32** representa uma configuração de um subsistema de vídeo. Essa classe foi preterida em favor das propriedades contidas nas classes [**Win32 \_ VideoController,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md)e [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[DEPRECATED, UUID("{8502C4ED-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_VideoConfiguration : CIM_Setting
{
  string   Caption;
  string   Description;
  string   SettingID;
  uint32   ActualColorResolution;
  string   AdapterChipType;
  string   AdapterCompatibility;
  string   AdapterDACType;
  string   AdapterDescription;
  uint32   AdapterRAM;
  string   AdapterType;
  uint32   BitsPerPixel;
  uint32   ColorPlanes;
  uint32   ColorTableEntries;
  uint32   DeviceSpecificPens;
  datetime DriverDate;
  uint32   HorizontalResolution;
  string   InfFilename;
  string   InfSection;
  string   InstalledDisplayDrivers;
  string   MonitorManufacturer;
  string   MonitorType;
  string   Name;
  uint32   PixelsPerXLogicalInch;
  uint32   PixelsPerYLogicalInch;
  uint32   RefreshRate;
  string   ScanMode;
  uint32   ScreenHeight;
  uint32   ScreenWidth;
  uint32   SystemPaletteEntries;
  uint32   VerticalResolution;
};
```

## <a name="members"></a>Membros

A **classe \_ VideoConfiguration win32** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ VideoConfiguration win32** tem essas propriedades.

<dl> <dt>

**ActualColorResolution**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**PRETERIDO,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| COLORRES"), [**Unidades**](../wmisdk/standard-qualifiers.md) ("bits por pixel")
</dt> </dl>

Indica a profundidade de cor atual da exibição de vídeo.

Essa propriedade foi preterida em favor de uma(s) propriedade(s) correspondente contida no [**\_ VideoController win32,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e/ou [**CIM \_ VideoControllerResolution.**](cim-videocontrollerresolution.md)

</dd> <dt>

**AdapterChipType**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**PRETERIDO,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services Class \\ \\ \\ \\ Info \| ChipType")
</dt> </dl>

Contém o nome do chip do adaptador.

Exemplo: s3

Essa propriedade foi preterida em favor de uma(s) propriedade(s) correspondente contida no [**\_ VideoController win32,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e/ou [**CIM \_ VideoControllerResolution.**](cim-videocontrollerresolution.md)

</dd> <dt>

**AdapterCompatibility**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**PRETERIDO,**](../wmisdk/standard-wmi-qualifiers.md) [**chave**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Especifica o nome do fabricante do adaptador. Esse nome pode ser usado para comparar a compatibilidade desse dispositivo com as necessidades do sistema de computador.

Essa propriedade foi preterida em favor de uma(s) propriedade(s) correspondente contida no [**\_ VideoController win32,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e/ou [**CIM \_ VideoControllerResolution.**](cim-videocontrollerresolution.md)

</dd> <dt>

**AdapterDACType**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**PRETERIDO,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services Class \\ \\ \\ \\ Info \| DACType")
</dt> </dl>

Indica o nome do CHIP digital para análogo (DAC) usado no adaptador.

Essa propriedade foi preterida em favor de uma(s) propriedade(s) correspondente contida no [**\_ VideoController win32,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e/ou [**CIM \_ VideoControllerResolution.**](cim-videocontrollerresolution.md)

</dd> <dt>

**AdapterDescription**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**PRETERIDO,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Contém uma descrição ou um nome descritivo do adaptador de vídeo.

Essa propriedade foi preterida em favor de uma(s) propriedade(s) correspondente contida no [**\_ VideoController win32,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e/ou [**CIM \_ VideoControllerResolution.**](cim-videocontrollerresolution.md)

</dd> <dt>

**AdapterRAM**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**PRETERIDO,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services Class \\ \\ \\ \\ Info \| VideoMemory"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Indica o tamanho da memória do adaptador de vídeo.

Exemplo: 16777216

Essa propriedade foi preterida em favor de uma(s) propriedade(s) correspondente contida no [**\_ VideoController win32,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e/ou [**CIM \_ VideoControllerResolution.**](cim-videocontrollerresolution.md)

</dd> <dt>

**AdapterType**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**PRETERIDO,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| HARDWARE Description System \\ \\ \\ \\ \\ \\ DisplayController \\ \\ 0 \\ \\ Identifier")
</dt> </dl>

Indica o tipo de adaptador de vídeo.

Conjunto de caracteres: alfanumérico

Essa propriedade foi preterida em favor de uma(s) propriedade(s) correspondente contida no [**\_ VideoController win32,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e/ou [**CIM \_ VideoControllerResolution.**](cim-videocontrollerresolution.md)

</dd> <dt>

**Bitsperpixel**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**PRETERIDO,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Funções de contexto do dispositivo Win32API \| \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| BITSPIXEL")
</dt> </dl>

Indica o número real de bits por pixel que representam a exibição. Isso pode ser dimensionado para a configuração de vídeo atual (representada pela propriedade ActualColorResolution) do usuário.

Exemplo: 8

Essa propriedade foi preterida em favor de uma(s) propriedade(s) correspondente contida no [**\_ VideoController win32,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e/ou [**CIM \_ VideoControllerResolution.**](cim-videocontrollerresolution.md)

</dd> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Descrição textual curta do objeto atual.

Essa propriedade é herdada da [**Configuração cim \_**](cim-setting.md).

</dd> <dt>

**ColorPlanes**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**PRETERIDO,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| PLANES")
</dt> </dl>

Indica o número atual de planos de cores usados na exibição de vídeo. Um plano de cores é outra maneira de representar cores de pixel; em vez de atribuir um único valor RGB a cada pixel, os planos de cores separam o gráfico em cada um dos componentes de cor primária (vermelho-verde) e os armazenam em seus próprios planos. Isso permite maior profundidade de cor em sistemas de vídeo de 8 e 16 bits. Os sistemas gráficos atuais têm a bitwidth grande o suficiente para armazenar informações de profundidade de cor, tornando necessário apenas um plano de cores.

Example: 1

Essa propriedade foi preterida em favor de uma(s) propriedade(s) correspondente contida no [**\_ VideoController win32,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e/ou [**CIM \_ VideoControllerResolution.**](cim-videocontrollerresolution.md)

</dd> <dt>

**ColorTableEntries**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**PRETERIDO,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Funções de contexto do dispositivo Win32API \| \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| NUMCOLORS")
</dt> </dl>

Indica o número de índices de cores em uma tabela de cores para uma exibição de vídeo. Essa propriedade será usada se o dispositivo tiver uma profundidade de cor de não mais de 8 bits por pixel. Para dispositivos com profundidades de cor maiores, -1 é retornado.

Exemplo: 256

Essa propriedade foi preterida em favor de uma(s) propriedade(s) correspondente contida no [**\_ VideoController win32,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e/ou [**CIM \_ VideoControllerResolution.**](cim-videocontrollerresolution.md)

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descrição textual do objeto atual.

Essa propriedade é herdada da [**Configuração cim \_**](cim-setting.md).

</dd> <dt>

**DeviceSpecificPens**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**preterido**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funções de contexto de dispositivo win32api \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| NUMPENS")
</dt> </dl>

Indica o número atual de canetas específicas do dispositivo. Um valor de 0xFFFFFFFF significa que o dispositivo não dá suporte a canetas. As canetas são usadas para desenhar linhas e bordas de objetos poligonal.

Exemplo: 3

Essa propriedade foi preterida em favor de uma propriedade (s) correspondente contida no [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//ou [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**DriverDate**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**preterido**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| sistema \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \\ \\ AdapterDescription \| DriverDate")
</dt> </dl>

Indica a data e a hora em que o driver de vídeo atual foi instalado.

Essa propriedade foi preterida em favor de uma propriedade (s) correspondente contida no [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//ou [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**HorizontalResolution**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**preterido**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funções de contexto de dispositivo win32api \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| HORZRES")
</dt> </dl>

Indica o número atual de pixels na direção horizontal (eixo X) da exibição.

Exemplo: 1024

Essa propriedade foi preterida em favor de uma propriedade (s) correspondente contida no [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//ou [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**InfFilename**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**preterido**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| sistema \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \| InfPath")
</dt> </dl>

Especifica o caminho para o arquivo. inf do driver de vídeo.

exemplo: C: \\ Windows \\ System32 \\ Drivers

Essa propriedade foi preterida em favor de uma propriedade (s) correspondente contida no [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//ou [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**InfSection**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**preterido**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| sistema \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \| InfSection")
</dt> </dl>

Indica a seção do arquivo. inf onde residem as informações de vídeo do Win32.

Essa propriedade foi preterida em favor de uma propriedade (s) correspondente contida no [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//ou [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**InstalledDisplayDrivers**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**preterido**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| sistema \\ \\ CurrentControlSet \\ \\ Services \\ \\ Class \\ \\ Defaule \| drv")
</dt> </dl>

Indica o nome do driver de vídeo instalado.

Essa propriedade foi preterida em favor de uma propriedade (s) correspondente contida no [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//ou [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**MonitorManufacturer**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**preteridos**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Indica o nome do fabricante do dispositivo de vídeo.

Exemplo: NEC

Essa propriedade foi preterida em favor de uma propriedade (s) correspondente contida no [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//ou [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**Monitor**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**preterido**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry o \| sistema de descrição de hardware \\ \\ \\ \\ \\ \\ MonitorPeripheral \\ \\ 0 \| identificador")
</dt> </dl>

Indica o nome do modelo do dispositivo de vídeo.

Exemplo: NEC 5FGp

Essa propriedade foi preterida em favor de uma propriedade (s) correspondente contida no [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//ou [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**preterido**](../wmisdk/standard-wmi-qualifiers.md), [**chave**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Contém um nome de identificação para a classe de configuração de vídeo.

Essa propriedade foi preterida em favor de uma propriedade (s) correspondente contida no [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//ou [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**PixelsPerXLogicalInch**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**preterido**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funções de contexto de dispositivo win32api \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| LOGPIXELSX")
</dt> </dl>

Indica o número de pixels por polegada lógica ao longo do eixo X (direção horizontal) da exibição.

Essa propriedade foi preterida em favor de uma propriedade (s) correspondente contida no [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//ou [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**PixelsPerYLogicalInch**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**preterido**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funções de contexto de dispositivo win32api \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| LOGPIXELSY")
</dt> </dl>

Indica o número de pixels por polegada lógica ao longo do eixo Y (direção vertical) da exibição.

Essa propriedade foi preterida em favor de uma propriedade (s) correspondente contida no [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//ou [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**Taxa_de_atualização**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**preterido**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funções de contexto de dispositivo win32api \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| VREFRESH")
</dt> </dl>

Indica a taxa de atualização da configuração de vídeo. Um valor de 0 ou 1 indica que uma taxa padrão está sendo usada.

Exemplo: 72

Essa propriedade foi preterida em favor de uma propriedade (s) correspondente contida no [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//ou [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**Scanmode**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**preteridos**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| sistema \\ \\ CurrentControlSet \\ \\ Services \| Device0 \| DefaultSettings. entrelaçado")
</dt> </dl>

Indica se o dispositivo de vídeo está entrelaçado.

Essa propriedade foi preterida em favor de uma propriedade (s) correspondente contida no [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//ou [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

<dt>

<span id="Non_Interlaced"></span><span id="non_interlaced"></span><span id="NON_INTERLACED"></span>

**Não entrelaçado** ("não entrelaçado")


</dt> <dd></dd> <dt>

<span id="Interlaced"></span><span id="interlaced"></span><span id="INTERLACED"></span>

**Entrelaçado** ("entrelaçado")


</dt> <dd></dd> </dl>

</dd> <dt>

**ScreenHeight**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**preterido**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funções de contexto de dispositivo win32api \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| VERTSIZE"), [**unidades**](../wmisdk/standard-qualifiers.md) ("milímetros")
</dt> </dl>

Especifica a altura da tela física.

Essa propriedade foi preterida em favor de uma propriedade (s) correspondente contida no [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//ou [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**ScreenWidth**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**preterido**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funções de contexto de dispositivo win32api \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| HORZSIZE"), [**unidades**](../wmisdk/standard-qualifiers.md) ("milímetros")
</dt> </dl>

Especifica a largura da tela física.

Essa propriedade foi preterida em favor de uma propriedade (s) correspondente contida no [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e//ou [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md).

</dd> <dt>

**Settingid**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Identificador pelo qual o objeto atual é conhecido.

Essa propriedade é herdada da [**Configuração cim \_**](cim-setting.md).

</dd> <dt>

**SystemPaletteEntries**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**PRETERIDO,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| SIZEPALETTE")
</dt> </dl>

Iindica o número atual de entradas de índice de cores reservadas para uso do sistema. Esse valor só é válido para configurações de exibição que usam uma paleta indexada . Paletas indexadas não são usadas para profundidades de cor maiores que 8 bits por pixel. Se a profundidade da cor for maior que 8 bits por pixel, esse valor será definido como **NULL.**

Exemplo: 20

Essa propriedade foi preterida em favor de uma(s) propriedade(s) correspondente contida no [**\_ VideoController win32,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e/ou [**CIM \_ VideoControllerResolution.**](cim-videocontrollerresolution.md)

</dd> <dt>

**VerticalResolution**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**PRETERIDO,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Context Functions \| [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) \| VERTRES")
</dt> </dl>

Indica o número atual de pixels na direção vertical (eixo Y) da exibição.

Exemplo: 768

Essa propriedade foi preterida em favor de uma(s) propriedade(s) correspondente contida no [**\_ VideoController win32,**](win32-videocontroller.md) [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md) e/ou [**CIM \_ VideoControllerResolution.**](cim-videocontrollerresolution.md)

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | RAIZ \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Configuração cim \_**](cim-setting.md)
</dt> </dl>

 

 
