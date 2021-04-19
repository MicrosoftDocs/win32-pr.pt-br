---
description: As características de gerenciamento de um dispositivo USB.
ms.assetid: c0589346-7683-49c6-bd34-5ee38d71d00e
title: Classe CIM_USBDevice (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBDevice
- CIM_USBDevice.USBVersion
- CIM_USBDevice.ClassCode
- CIM_USBDevice.SubclassCode
- CIM_USBDevice.ProtocolCode
- CIM_USBDevice.USBVersionInBCD
- CIM_USBDevice.MaxPacketSize
- CIM_USBDevice.VendorID
- CIM_USBDevice.ProductID
- CIM_USBDevice.DeviceReleaseNumber
- CIM_USBDevice.Manufacturer
- CIM_USBDevice.Product
- CIM_USBDevice.SerialNumber
- CIM_USBDevice.NumberOfConfigs
- CIM_USBDevice.CurrentConfigValue
- CIM_USBDevice.CurrentAlternateSettings
- CIM_USBDevice.CommandTimeout
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4b43c57d69f0f9eb92293aa8fa1ff1aa1ebe96c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105775739"
---
# <a name="cim_usbdevice-class-hyper-v-management"></a>Classe CIM_USBDevice (gerenciamento do Hyper-V)

As características de gerenciamento de um dispositivo USB.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Device::USB")]
class CIM_USBDevice : CIM_LogicalDevice
{
  uint16   USBVersion;
  uint8    ClassCode;
  uint8    SubclassCode;
  uint8    ProtocolCode;
  uint16   USBVersionInBCD;
  uint8    MaxPacketSize;
  uint16   VendorID;
  uint16   ProductID;
  uint16   DeviceReleaseNumber;
  string   Manufacturer;
  string   Product;
  string   SerialNumber;
  uint8    NumberOfConfigs;
  uint8    CurrentConfigValue;
  uint8    CurrentAlternateSettings[];
  datetime CommandTimeout;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ UsbDevice** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **CIM \_ UsbDevice** tem esses métodos.



| Método                                               | Descrição                                   |
|:-----------------------------------------------------|:----------------------------------------------|
| [**Getdescriptor**](cim-usbdevice-getdescriptor.md) | Recupera um descritor de dispositivo USB.<br/> |



 

### <a name="properties"></a>Propriedades

A classe **CIM \_ UsbDevice** tem essas propriedades.

<dl> <dt>

**ClassCode**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("especificação de barramento serial universal. USB – se o \| descritor de dispositivo padrão \| bDeviceClass")
</dt> </dl>

O código de classe USB.

</dd> <dt>

**CommandTimeOut**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Um intervalo de tempo limite que é configurável por aplicativos de gerenciamento que dão suporte ao redirecionamento de USB. Quando o serviço de redirecionamento redireciona um comando de dispositivo USB para um dispositivo remoto e o dispositivo remoto não responde antes do intervalo de tempo limite, o serviço de redirecionamento emulará um evento de ejeção de mídia. Além disso, o serviço pode tentar novamente o comando ou tentar restabelecer a conexão com o dispositivo remoto.

</dd> <dt>

**CurrentAlternateSettings**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ UsbDevice**.**CurrentConfigValue**")
</dt> </dl>

Uma matriz que contém as configurações alternativas para cada interface na configuração atual do dispositivo.

</dd> <dt>

**CurrentConfigValue**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ UsbDevice**.**CurrentAlternateSettings**")
</dt> </dl>

A configuração selecionada no momento para o dispositivo. Se esse valor for zero, o dispositivo não será configurado.

</dd> <dt>

**DeviceReleaseNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("especificação de barramento serial universal. USB – se o \| descritor de dispositivo padrão \| bcdDevice")
</dt> </dl>

O número de liberação do dispositivo no formato BCD.

</dd> <dt>

**Manufacturer**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("especificação de barramento serial universal. USB – se o \| descritor de dispositivo padrão \| iManufacturer")
</dt> </dl>

A cadeia de caracteres do fabricante do dispositivo.

</dd> <dt>

**MaxPacketSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("especificação de barramento serial universal. USB – se o \| descritor de dispositivo padrão \| bMaxPacketSize")
</dt> </dl>

O tamanho máximo do pacote para o ponto de extremidade de USB zero.

</dd> <dt>

**NumberOfConfigs**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("especificação de barramento serial universal. USB – se o \| descritor de dispositivo padrão \| bNumConfigurations")
</dt> </dl>

O número de configurações de dispositivo que são definidas para o dispositivo.

</dd> <dt>

**Product**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("especificação de barramento serial universal. USB – se o \| descritor de dispositivo padrão \| iProduct")
</dt> </dl>

A cadeia de caracteres do produto do dispositivo.

</dd> <dt>

**ProductID**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("especificação de barramento serial universal. USB – se o \| descritor de dispositivo padrão \| idProduct")
</dt> </dl>

A ID do produto atribuída ao dispositivo pelo fabricante.

</dd> <dt>

**ProtocolCode**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("especificação de barramento serial universal. USB – se o \| descritor de dispositivo padrão \| bDeviceProtocol")
</dt> </dl>

O código do protocolo USB.

</dd> <dt>

**SerialNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("especificação de barramento serial universal. USB – se o \| descritor de dispositivo padrão \| iSerialNumber")
</dt> </dl>

O número de série do dispositivo.

</dd> <dt>

**SubclassCode**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("especificação de barramento serial universal. USB – se o \| descritor de dispositivo padrão \| bDeviceSubClass")
</dt> </dl>

O código de subclasse USB.

</dd> <dt>

**USBVersion**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A versão USB mais recente com suporte do dispositivo USB. A propriedade é expressa como um formato decimal codificado em binário (BCD) que contém um ponto decimal entre o 2º e o terceiro dígitos. Por exemplo, um valor de 0x201 indica que a versão 2, 1 tem suporte.

</dd> <dt>

**USBVersionInBCD**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("especificação de barramento serial universal. USB – se o \| descritor de dispositivo padrão \| bcdUSB")
</dt> </dl>

O número de especificação USB com o qual o dispositivo está em conformidade. Essa propriedade é formatada com o formato BCD.

</dd> <dt>

**VendorID**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("especificação de barramento serial universal. USB – se o \| descritor de dispositivo padrão \| idVendor")
</dt> </dl>

A ID do fornecedor atribuída ao dispositivo por USB.org.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_LOGICALDEVICE CIM**](cim-logicaldevice.md)
</dt> </dl>

 

