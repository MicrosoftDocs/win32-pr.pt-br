---
description: A \_ classe WMI DisplayControllerConfiguration do Win32 representa as informações de configuração do adaptador de vídeo de um sistema de computador executando o Windows.
ms.assetid: 36ebd840-5e8c-411a-828d-38972fe956e2
ms.tgt_platform: multiple
title: Classe Win32_DisplayControllerConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DisplayControllerConfiguration
- Win32_DisplayControllerConfiguration.Caption
- Win32_DisplayControllerConfiguration.Description
- Win32_DisplayControllerConfiguration.SettingID
- Win32_DisplayControllerConfiguration.BitsPerPixel
- Win32_DisplayControllerConfiguration.ColorPlanes
- Win32_DisplayControllerConfiguration.DeviceEntriesInAColorTable
- Win32_DisplayControllerConfiguration.DeviceSpecificPens
- Win32_DisplayControllerConfiguration.HorizontalResolution
- Win32_DisplayControllerConfiguration.Name
- Win32_DisplayControllerConfiguration.RefreshRate
- Win32_DisplayControllerConfiguration.ReservedSystemPaletteEntries
- Win32_DisplayControllerConfiguration.SystemPaletteEntries
- Win32_DisplayControllerConfiguration.VerticalResolution
- Win32_DisplayControllerConfiguration.VideoMode
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8e64f99cb4d4715d9b7a0eb88bd2e7629feed853
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089464"
---
# <a name="win32_displaycontrollerconfiguration-class"></a>\_Classe Win32 DisplayControllerConfiguration

A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ DisplayControllerConfiguration do Win32** representa as informações de configuração do adaptador de vídeo de um sistema de computador executando o Windows.

Essa classe está obsoleta. No lugar dessa classe, você deve usar as propriedades nas classes [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md)e [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md) .

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[DEPRECATED, Dynamic, Provider("CIMWin32"), UUID("{8502C4E5-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DisplayControllerConfiguration : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  uint32 BitsPerPixel;
  uint32 ColorPlanes;
  uint32 DeviceEntriesInAColorTable;
  uint32 DeviceSpecificPens;
  uint32 HorizontalResolution;
  string Name;
  sint32 RefreshRate;
  uint32 ReservedSystemPaletteEntries;
  uint32 SystemPaletteEntries;
  uint32 VerticalResolution;
  string VideoMode;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ DisplayControllerConfiguration** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ DisplayControllerConfiguration** tem essas propriedades.

<dl> <dt>

**BitsPerPixel**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**preterido**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| funções de contexto de dispositivo win32api \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| BITSPIXEL")
</dt> </dl>

O número de bits usados para representar a cor nessa configuração ou os bits em cada pixel.

Exemplo: 8

</dd> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Breve descrição textual do objeto atual.

Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).

</dd> <dt>

**ColorPlanes**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| funções de contexto de dispositivo win32api planos de \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| ")
</dt> </dl>

Número atual de planos de cores usados na configuração de exibição. Um plano de cores é outra maneira de representar cores de pixel. Em vez de atribuir um único valor RGB a cada pixel, os planos de cores separam o gráfico em cada um dos componentes de cor primária (vermelho, verde, azul) e os armazena em seus próprios planos. Isso permite mais profundidades de cor em sistemas de vídeo de 8 e 16 bits. Os sistemas gráficos presentes têm o bitwidth grande o suficiente para armazenar informações de profundidade de cor, o que significa que apenas um plano de cores é necessário.

Example: 1

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descrição textual do objeto atual.

Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).

</dd> <dt>

**DeviceEntriesInAColorTable**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**preterido**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| funções de contexto de dispositivo win32api \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| NUMCOLORS")
</dt> </dl>

Número de índices de cores em uma tabela de cores de um dispositivo de vídeo (se o dispositivo tiver uma profundidade de cor de no máximo 8 bits por pixel). Para dispositivos com mais profundidades de cor,-1 é retornado.

Exemplo: 256

</dd> <dt>

**DeviceSpecificPens**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**preterido**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| funções de contexto de dispositivo win32api \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| NUMPENS")
</dt> </dl>

Número atual de canetas específicas do dispositivo. Um valor de 0xFFFFFFFF significa que o dispositivo não dá suporte a canetas. As canetas são propriedades lógicas que podem ser atribuídas pelo controlador de vídeo para exibir dispositivos e são usadas para desenhar linhas, bordas de polígonos e texto.

Exemplo: 3

</dd> <dt>

**HorizontalResolution**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**preterido**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| funções de contexto de dispositivo win32api \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| HORZRES"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")
</dt> </dl>

Número atual de pixels na direção horizontal (eixo x) da exibição.

Exemplo: 1024

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**preterido**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

Nome do adaptador usado nesta configuração.

</dd> <dt>

**Taxa_de_atualização**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**preterido**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| funções de contexto de dispositivo win32api \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| HORZRESVREFRESH"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hertz")
</dt> </dl>

Taxa de atualização do adaptador de vídeo. Um valor de 0 (zero) ou 1 (um) indica que uma taxa padrão está sendo usada. Um valor de-1 indica que uma taxa ideal está sendo usada.

Exemplo: 72

</dd> <dt>

**ReservedSystemPaletteEntries**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**preterido**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| funções de contexto de dispositivo win32api \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| NUMRESERVED")
</dt> </dl>

Número atual de entradas de índice de cor reservadas para uso do sistema. Esse valor só é válido para configurações de exibição que usam uma paleta indexada. As paletas indexadas não são usadas para profundidades de cor maiores que 8 bits por pixel. Se a profundidade de cor tiver mais de 8 bits por pixel, esse valor será definido como **nulo**.

Exemplo: 20

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Identificador pelo qual o objeto atual é conhecido.

Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).

</dd> <dt>

**SystemPaletteEntries**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**preterido**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| funções de contexto de dispositivo win32api \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| NUMRESERVED")
</dt> </dl>

Número atual de entradas de índice de cor reservadas para uso do sistema. Esse valor só é válido para configurações de exibição que usam uma paleta indexada. As paletas indexadas não são usadas para profundidades de cor maiores que 8 bits por pixel. Se a profundidade de cor tiver mais de 8 bits por pixel, esse valor será definido como **nulo**.

Exemplo: 20

</dd> <dt>

**VerticalResolution**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**preterido**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| funções de contexto de dispositivo win32api \| [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) \| VERTRES"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")
</dt> </dl>

Número atual de pixels na direção vertical (eixo y) da exibição.

Exemplo: 768

</dd> <dt>

**Videomode**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

Descrição legível pelo usuário da atual resolução de tela e configuração de cor da exibição.

Exemplo: "1024 768 com 256 cores"

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **Win32 \_ DisplayControllerConfiguration** é derivada da [**\_ configuração de CIM**](cim-setting.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Configuração de CIM \_**](cim-setting.md)
</dt> <dt>

[Classes de hardware do sistema de computador](computer-system-hardware-classes.md)
</dt> </dl>

 

