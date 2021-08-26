---
description: Representa um dispositivo de memória física localizado em um sistema de computador e disponível para o sistema operacional.
ms.assetid: 34baca53-ab85-4e06-9853-71b904ede4ab
ms.tgt_platform: multiple
title: Classe Win32_PhysicalMemory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PhysicalMemory
- Win32_PhysicalMemory.Attributes
- Win32_PhysicalMemory.BankLabel
- Win32_PhysicalMemory.Capacity
- Win32_PhysicalMemory.Caption
- Win32_PhysicalMemory.ConfiguredClockSpeed
- Win32_PhysicalMemory.ConfiguredVoltage
- Win32_PhysicalMemory.CreationClassName
- Win32_PhysicalMemory.DataWidth
- Win32_PhysicalMemory.Description
- Win32_PhysicalMemory.DeviceLocator
- Win32_PhysicalMemory.FormFactor
- Win32_PhysicalMemory.HotSwappable
- Win32_PhysicalMemory.InstallDate
- Win32_PhysicalMemory.InterleaveDataDepth
- Win32_PhysicalMemory.InterleavePosition
- Win32_PhysicalMemory.Manufacturer
- Win32_PhysicalMemory.MaxVoltage
- Win32_PhysicalMemory.MemoryType
- Win32_PhysicalMemory.MinVoltage
- Win32_PhysicalMemory.Model
- Win32_PhysicalMemory.Name
- Win32_PhysicalMemory.OtherIdentifyingInfo
- Win32_PhysicalMemory.PartNumber
- Win32_PhysicalMemory.PositionInRow
- Win32_PhysicalMemory.PoweredOn
- Win32_PhysicalMemory.Removable
- Win32_PhysicalMemory.Replaceable
- Win32_PhysicalMemory.SerialNumber
- Win32_PhysicalMemory.SKU
- Win32_PhysicalMemory.SMBIOSMemoryType
- Win32_PhysicalMemory.Speed
- Win32_PhysicalMemory.Status
- Win32_PhysicalMemory.Tag
- Win32_PhysicalMemory.TotalWidth
- Win32_PhysicalMemory.TypeDetail
- Win32_PhysicalMemory.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5559de847cf15b60e3af27f8b092605b8ca8c3bfd874d27ebab7a0edda454d14
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119972206"
---
# <a name="win32_physicalmemory-class"></a>\_Classe Win32 PhysicalMemory

A [classe WMI](../wmisdk/retrieving-a-class.md) **\_ PhysicalMemory do Win32** representa um dispositivo de memória física localizado em um sistema de computador e disponível para o sistema operacional.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B93-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_PhysicalMemory : CIM_PhysicalMemory
{
  uint32   Attributes;
  string   BankLabel;
  uint64   Capacity;
  string   Caption;
  uint32   ConfiguredClockSpeed;
  uint32   ConfiguredVoltage;
  string   CreationClassName;
  uint16   DataWidth;
  string   Description;
  string   DeviceLocator;
  uint16   FormFactor;
  boolean  HotSwappable;
  datetime InstallDate;
  uint16   InterleaveDataDepth;
  uint32   InterleavePosition;
  string   Manufacturer;
  uint32   MaxVoltage;
  uint16   MemoryType;
  uint32   MinVoltage;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  uint32   PositionInRow;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  string   SerialNumber;
  string   SKU;
  uint32   SMBIOSMemoryType;
  uint32   Speed;
  string   Status;
  string   Tag;
  uint16   TotalWidth;
  uint16   TypeDetail;
  string   Version;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ PhysicalMemory** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ PhysicalMemory** tem essas propriedades.

<dl> <dt>

**Atributos**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| atributos do tipo SMBIOS 17 \| ")
</dt> </dl>

SMBIOS-Type 17-Attributes. Representa a classificação.

Esse valor é proveniente do membro **Attributes** da estrutura de **dispositivo de memória** nas informações de SMBIOS.

**Windows Server 2012 r2, Windows 8.1, Windows Server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** não há suporte para essa propriedade antes de Windows Server 2016 e Windows 10.

</dd> <dt>

**BankLabel**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Dispositivo de memória DMTF \| 2,4 ")
</dt> </dl>

Rotulado fisicamente o banco em que a memória está localizada.

Exemplos: "Bank 0", "Bank A"

Esse valor é proveniente do membro do **localizador de banco** da estrutura do **dispositivo de memória** nas informações do SMBIOS.

Essa propriedade é herdada do [**CIM \_ PhysicalMemory**](cim-physicalmemory.md).

</dd> <dt>

**Capacidade**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Dispositivo de memória DMTF \| 2,5 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" bytes ")
</dt> </dl>

Capacidade total da memória física — em bytes.

Esse valor é proveniente da estrutura de **dispositivo de memória** nas informações de versão do SMBIOS. Para versões de SMBIOS 2,1 a 2,6, o valor é proveniente do membro de **tamanho** . Para o SMBIOS versão 2.7 +, o valor é proveniente do membro de **tamanho estendido** .

Essa propriedade é herdada do [**CIM \_ PhysicalMemory**](cim-physicalmemory.md).

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Breve descrição do objeto — uma cadeia de caracteres de uma linha.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**ConfiguredClockSpeed**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| tipo SMBIOS 17 de velocidade de clock de \| memória configurada")
</dt> </dl>

A velocidade de clock configurada do dispositivo de memória, em megahertz (MHz) ou 0, se a velocidade for desconhecida.

Esse valor é proveniente do membro da **velocidade do relógio da memória configurada** da estrutura do **dispositivo de memória** nas informações do SMBIOS.

**Windows Server 2012 r2, Windows 8.1, Windows Server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** não há suporte para essa propriedade antes de Windows Server 2016 e Windows 10.

</dd> <dt>

**ConfiguredVoltage**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 17 \| configurative Voltage")
</dt> </dl>

A tensão configurada para este dispositivo, em milivolts ou 0, se a tensão for desconhecida.

Esse valor é proveniente do membro de **tensão configurado** da estrutura do **dispositivo de memória** nas informações do SMBIOS.

**Windows Server 2012 r2, Windows 8.1, Windows Server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** não há suporte para essa propriedade antes de Windows Server 2016 e Windows 10.

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Nome da primeira classe concreta que aparece na cadeia de herança usada na criação de uma instância. Quando usado com as outras propriedades de chave da classe, a propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.

Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).

</dd> <dt>

**DataWidth**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Dispositivo de memória DMTF \| 2,8 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" bits ")
</dt> </dl>

Largura de dados da memória física — em bits. Uma largura de dados de 0 (zero) e uma largura total de 8 (oito) indica que a memória é usada unicamente para fornecer bits de correção de erro.

Esse valor é proveniente do membro de **largura de dados** da estrutura de **dispositivo de memória** nas informações de SMBIOS.

Essa propriedade é herdada do [**CIM \_ PhysicalMemory**](cim-physicalmemory.md).

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")
</dt> </dl>

Descrição de um objeto.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**DeviceLocator**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| localizador de dispositivo do tipo SMBIOS 17 \| ")
</dt> </dl>

Rótulo do soquete ou placa de circuito que contém a memória.

Exemplo: "SIMM 3"

Esse valor é proveniente do membro do **localizador de dispositivo** da estrutura de **dispositivo de memória** nas informações do SMBIOS.

</dd> <dt>

**FormFactor**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Dispositivo de memória DMTF \| 2,6 ")
</dt> </dl>

Fator forma de implementação para o chip.

Esse valor vem do membro de **fator forma** da estrutura do **dispositivo de memória** nas informações do SMBIOS.

Essa propriedade é herdada [**do \_ chip CIM**](cim-chip.md).

<dt>



  acima (0)


</dt> <dd>

Unknown

</dd> <dt>



 (1)


</dt> <dd>

Outro

</dd> <dt>



 (2)


</dt> <dd>

SIP

</dd> <dt>



 (3)


</dt> <dd>

DIP

</dd> <dt>



 (4)


</dt> <dd>

ZIP

</dd> <dt>



 (5)


</dt> <dd>

SOJ

</dd> <dt>



  (6)


</dt> <dd>

Proprietário

</dd> <dt>



 (7)


</dt> <dd>

Simm

</dd> <dt>



 (8)


</dt> <dd>

Dimm

</dd> <dt>



 (9)


</dt> <dd>

TSOP

</dd> <dt>



 (10)


</dt> <dd>

Pga

</dd> <dt>



 (11)


</dt> <dd>

Rimm

</dd> <dt>



 (12)


</dt> <dd>

Sodimm

</dd> <dt>



 (13)


</dt> <dd>

SRIMM

</dd> <dt>



 (14)


</dt> <dd>

Smd

</dd> <dt>



 (15)


</dt> <dd>

SSMP

</dd> <dt>



 (16)


</dt> <dd>

QFP

</dd> <dt>



 (17)


</dt> <dd>

TQFP

</dd> <dt>



 (18)


</dt> <dd>

SOIC

</dd> <dt>



 (19)


</dt> <dd>

Lcc

</dd> <dt>



 (20)


</dt> <dd>

YORKC

</dd> <dt>



 (21)


</dt> <dd>

Bga

</dd> <dt>



 (22)


</dt> <dd>

FPBGA

</dd> <dt>



 (23)


</dt> <dd>

LGA

</dd> </dl>

</dd> <dt>

**HotSwappable**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se **TRUE**, esse componente de mídia física poderá ser substituído por um fisicamente diferente, mas equivalente, enquanto o pacote que o contém tem a potência aplicada. Por exemplo, um componente de ventilador pode ser projetado para ser trocado por hot-swapp. Todos os componentes que podem ser trocados por hot-swapp são inerentemente removíveis e substituíveis.

Essa propriedade é herdada de [**Cim \_ PhysicalComponent.**](cim-physicalcomponent.md)

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de dados: **datetime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Data de instalação")
</dt> </dl>

Data e hora em que o objeto é instalado. Essa propriedade não precisa de um valor para indicar que o objeto está instalado.

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**InterleaveDataDepth**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 20 \| Interleaved Data Depth")
</dt> </dl>

Número máximo de inteiros de 16 bits sem sinal de linhas consecutivas de dados que são acessadas em uma única transferência intercalada do dispositivo de memória. Se o valor for 0 (zero), a memória não será intercalada.

</dd> <dt>

**InterleavePosition**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. Endereços mapeados do dispositivo de memória DMTF \| \| 001.7")
</dt> </dl>

Posição da memória física em uma intercalação. Por exemplo, em uma intercalação 2:1, um valor de "1" indica que a memória está na posição "even".

Essa propriedade é herdada [**de CIM \_ PhysicalMemory.**](cim-physicalmemory.md)

<dt>

0
</dt> <dd>

Não intercalado

</dd> <dt>

1
</dt> <dd>

Primeira posição

</dd> <dt>

2
</dt> <dd>

Segunda posição

</dd> </dl>

</dd> <dt>

**Fabricante**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Nome da organização responsável por produzir o elemento físico.

Esse valor vem do membro **Fabricante** da estrutura **dispositivo de** memória nas informações do SMBIOS.

Essa propriedade é herdada de [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**MaxVoltage**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Tipo 17 \| Tensão máxima")
</dt> </dl>

A tensão operacional máxima para esse dispositivo, em milivolts ou 0, se a tensão for desconhecida.

Esse valor vem do **membro de tensão** Máxima da estrutura **dispositivo de** memória nas informações do SMBIOS.

**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 e Windows Vista:** Essa propriedade não é suportada antes Windows Server 2016 e Windows 10.

</dd> <dt>

**MemoryType**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. Dispositivo de memória DMTF \| \| 002.9")
</dt> </dl>

Tipo de memória física. Esse é um valor CIM mapeado para o valor SMBIOS. A **propriedade SMBIOSMemoryType** contém o tipo de memória SMBIOS bruto.

Esse valor vem do membro **Tipo de** Memória da estrutura **dispositivo de** memória nas informações do SMBIOS.

Essa propriedade é herdada [**de CIM \_ PhysicalMemory.**](cim-physicalmemory.md)

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outros** (1)


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

<span id="DRAM"></span><span id="dram"></span>**DRAM** (2)


</dt> <dd></dd> <dt>

<span id="Synchronous_DRAM"></span><span id="synchronous_dram"></span><span id="SYNCHRONOUS_DRAM"></span>

<span id="Synchronous_DRAM"></span><span id="synchronous_dram"></span><span id="SYNCHRONOUS_DRAM"></span>**DRAM síncrona** (3)


</dt> <dd></dd> <dt>

<span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>

<span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>**DRAM de cache** (4)


</dt> <dd></dd> <dt>

<span id="EDO"></span><span id="edo"></span>

<span id="EDO"></span><span id="edo"></span>**Edo** (5)


</dt> <dd></dd> <dt>

<span id="EDRAM"></span><span id="edram"></span>

<span id="EDRAM"></span><span id="edram"></span>**EDRAM** (6)


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

<span id="VRAM"></span><span id="vram"></span>**VRAM** (7)


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

<span id="SRAM"></span><span id="sram"></span>**SRAM** (8)


</dt> <dd></dd> <dt>

<span id="RAM"></span><span id="ram"></span>

<span id="RAM"></span><span id="ram"></span>**RAM** (9)


</dt> <dd></dd> <dt>

<span id="ROM"></span><span id="rom"></span>

<span id="ROM"></span><span id="rom"></span>**ROM** (10)


</dt> <dd></dd> <dt>

<span id="Flash"></span><span id="flash"></span><span id="FLASH"></span>

<span id="Flash"></span><span id="flash"></span><span id="FLASH"></span>**Flash** (11)


</dt> <dd></dd> <dt>

<span id="EEPROM"></span><span id="eeprom"></span>

<span id="EEPROM"></span><span id="eeprom"></span>**EEPROM** (12)


</dt> <dd></dd> <dt>

<span id="FEPROM"></span><span id="feprom"></span>

<span id="FEPROM"></span><span id="feprom"></span>**FEPROM** (13)


</dt> <dd></dd> <dt>

<span id="EPROM"></span><span id="eprom"></span>

<span id="EPROM"></span><span id="eprom"></span>**(14** )


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

<span id="CDRAM"></span><span id="cdram"></span>**CDRAM** (15)


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

<span id="3DRAM"></span><span id="3dram"></span>**3DRAM** (16)


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

<span id="SDRAM"></span><span id="sdram"></span>**SDRAM** (17)


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

<span id="SGRAM"></span><span id="sgram"></span>**SGRAM** (18)


</dt> <dd></dd> <dt>

<span id="RDRAM"></span><span id="rdram"></span>

<span id="RDRAM"></span><span id="rdram"></span>**RDRAM** (19)


</dt> <dd></dd> <dt>

<span id="DDR"></span><span id="ddr"></span>

<span id="DDR"></span><span id="ddr"></span>**DDR** (20)


</dt> <dd></dd> <dt>

<span id="DDR2"></span><span id="ddr2"></span>

<span id="DDR2"></span><span id="ddr2"></span>**DDR2** (21)


</dt> <dd>

DDR2 — pode não estar disponível.

</dd> <dt>

<span id="DDR2_FB-DIMM"></span><span id="ddr2_fb-dimm"></span>

<span id="DDR2_FB-DIMM"></span><span id="ddr2_fb-dimm"></span>**DDR2 FB-DIMM** (22)


</dt> <dd>

O DDR2 – FB-DIMM, pode não estar disponível.

</dd> <dt>

24
</dt> <dd>

DDR3 — pode não estar disponível.

</dd> <dt>

25
</dt> <dd>

FBD2

</dt> <dd></dd> <dt>

<span id="DDR4"></span><span id="DDR4"></span>**DDR4** (26)

</dd> </dl>

</dd> <dt>

**MinVoltage**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("tipo de SMBIOS \| 20 de \| Voltagem mínima")
</dt> </dl>

A tensão operacional mínima para este dispositivo, em milivolts ou 0, se a tensão for desconhecida.

Esse valor é proveniente do membro de **tensão mínima** da estrutura do **dispositivo de memória** nas informações do SMBIOS.

**Windows Server 2012 r2, Windows 8.1, Windows Server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** não há suporte para essa propriedade antes de Windows Server 2016 e Windows 10.

</dd> <dt>

**Modelo**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Nome do elemento físico.

Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")
</dt> </dl>

Rótulo do objeto. Quando em uma subclasse, a propriedade pode ser substituída para ser uma propriedade de chave.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Dados adicionais, além das informações de marca do ativo, que podem ser usados para identificar um elemento físico. Um exemplo são os dados de código de barras associados a um elemento que também tem uma marca de ativo. Se apenas os dados de código de barras estiverem disponíveis e exclusivos ou puderem ser usados como uma chave de elemento, essa propriedade será **NULL** e os dados de código de barras serão usados como a chave de classe na propriedade de marca.

Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).

</dd> <dt>

**PartNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Número de peça atribuído pela organização responsável por produzir ou fabricar o elemento físico.

Esse valor é proveniente do membro de **número de peça** da estrutura de **dispositivo de memória** nas informações de SMBIOS.

Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).

</dd> <dt>

**PositionInRow**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Endereços mapeados do dispositivo de memória DMTF \| 1,6 ")
</dt> </dl>

Posição da memória física em uma linha. Por exemplo, se usar dispositivos de memória de 2 8 bits para formar uma linha de 16 bits, um valor de 2 (dois) significa que essa memória é o segundo dispositivo — 0 (zero) é um valor inválido para essa propriedade.

Essa propriedade é herdada do [**CIM \_ PhysicalMemory**](cim-physicalmemory.md).

</dd> <dt>

**Ligado**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se **for true**, o elemento físico será ligado.

Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).

</dd> <dt>

**Removível**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se for **true**, um componente físico será removível (se for projetado para ser colocado dentro e fora do contêiner físico no qual ele é normalmente encontrado, sem encontrar a função do empacotamento geral). Um componente ainda poderá ser removível se a energia precisar ser "desativada" para executar a remoção. Se a energia puder ser "ativada" e o componente for removido, o elemento será removível e poderá ser intercambiável. Por exemplo, um chip de processador atualizável é removível.

Essa propriedade é herdada do [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md).

</dd> <dt>

**Peças**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se **for true**, esse componente de mídia física poderá ser substituído por um fisicamente diferente. Por exemplo, alguns sistemas de computador permitem que o chip do processador principal seja atualizado para uma classificação de clock mais alta. Nesse caso, diz-se que o processador é substituível. Todos os componentes removíveis são inerentemente substituíveis.

Essa propriedade é herdada do [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md).

</dd> <dt>

**SerialNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

O número alocado pelo fabricante para identificar o elemento físico.

Esse valor é proveniente do membro de **número de série** da estrutura de **dispositivo de memória** nas informações de SMBIOS.

Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).

</dd> <dt>

**SKU**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Número de unidade de manutenção de estoque do elemento físico.

Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).

</dd> <dt>

**SMBIOSMemoryType**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("tipo de memória do SMBIOS \| tipo 17 \| \_ ")
</dt> </dl>

O tipo de memória do SMBIOS bruto. O valor da propriedade **memorytype** é um valor CIM que é mapeado para o valor SMBIOS.

**Windows Server 2012 r2, Windows 8.1, Windows Server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** não há suporte para essa propriedade antes de Windows Server 2016 e Windows 10.

</dd> <dt>

**Rápida**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("nanossegundos")
</dt> </dl>

Velocidade da memória física — em nanossegundos.

Esse valor é proveniente do membro **Speed** da estrutura do **dispositivo de memória** nas informações do SMBIOS.

Essa propriedade é herdada do [**CIM \_ PhysicalMemory**](cim-physicalmemory.md).

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")
</dt> </dl>

Status atual do objeto. Vários status de operação e não operacional podem ser definidos. Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo). Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço". O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo. Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

Os valores possíveis são.

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Erro** ("erro")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Degradado** ("degradado")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** ("desconhecido")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Falha de Pred** ("Pred Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Iniciando** ("Iniciando")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Parando** ("parando")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Serviço** ("serviço")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Sob estresse** ("sob estresse")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

Não **recuperar** ("Recover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Sem contato** ("sem contato")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Perda de comunicação** ("perda de comunicação")


</dt> <dd></dd> </dl>

</dd> <dt>

**Tag**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**override**](../wmisdk/standard-qualifiers.md) ("tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Identificador exclusivo para o dispositivo de memória física que é representado por uma instância do **Win32 \_ PhysicalMemory**. Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).

Exemplo: "memória física 1"

</dd> <dt>

**TotalWidth**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Dispositivo de memória DMTF \| 2,7 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" bits ")
</dt> </dl>

Largura total, em bits, da memória física, incluindo bits de verificação ou correção de erro. Se não houver nenhum bit de correção de erro, o valor nessa propriedade deverá corresponder ao que é especificado para a propriedade **datalargura** .

Esse valor é proveniente do membro de **largura total** da estrutura de **dispositivo de memória** nas informações de SMBIOS.

Essa propriedade é herdada do [**CIM \_ PhysicalMemory**](cim-physicalmemory.md).

</dd> <dt>

**TypeDetail**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("tipo de SMBIOS- \| \| detalhe de tipo 17")
</dt> </dl>

Tipo de memória física representada.

Esse valor é proveniente do membro de **detalhes de tipo** da estrutura do **dispositivo de memória** nas informações do SMBIOS.

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reservado** (1)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (2)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (4)


</dt> <dd></dd> <dt>

<span id="Fast-paged"></span><span id="fast-paged"></span><span id="FAST-PAGED"></span>

<span id="Fast-paged"></span><span id="fast-paged"></span><span id="FAST-PAGED"></span>**Com página rápida** (8)


</dt> <dd></dd> <dt>

<span id="Static_column"></span><span id="static_column"></span><span id="STATIC_COLUMN"></span>

<span id="Static_column"></span><span id="static_column"></span><span id="STATIC_COLUMN"></span>**Coluna estática** (16)


</dt> <dd></dd> <dt>

<span id="Pseudo-static"></span><span id="pseudo-static"></span><span id="PSEUDO-STATIC"></span>

<span id="Pseudo-static"></span><span id="pseudo-static"></span><span id="PSEUDO-STATIC"></span>**Pseudo-estático** (32)


</dt> <dd></dd> <dt>

<span id="RAMBUS"></span><span id="rambus"></span>

<span id="RAMBUS"></span><span id="rambus"></span>**Rambus** (64)


</dt> <dd></dd> <dt>

<span id="Synchronous"></span><span id="synchronous"></span><span id="SYNCHRONOUS"></span>

<span id="Synchronous"></span><span id="synchronous"></span><span id="SYNCHRONOUS"></span>**Síncrono** (128)


</dt> <dd></dd> <dt>

<span id="CMOS"></span><span id="cmos"></span>

<span id="CMOS"></span><span id="cmos"></span>**CMOS** (256)


</dt> <dd></dd> <dt>

<span id="EDO"></span><span id="edo"></span>

<span id="EDO"></span><span id="edo"></span>**Edo** (512)


</dt> <dd></dd> <dt>

<span id="Window_DRAM"></span><span id="window_dram"></span><span id="WINDOW_DRAM"></span>

<span id="Window_DRAM"></span><span id="window_dram"></span><span id="WINDOW_DRAM"></span>**DRAM de janela** (1024)


</dt> <dd></dd> <dt>

<span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>

<span id="Cache_DRAM"></span><span id="cache_dram"></span><span id="CACHE_DRAM"></span>**DRAM de cache** (2048)


</dt> <dd></dd> <dt>

<span id="Non-volatile"></span><span id="non-volatile"></span><span id="NON-VOLATILE"></span>

<span id="Non-volatile"></span><span id="non-volatile"></span><span id="NON-VOLATILE"></span>**Não volátil** (4096)


</dt> <dd>

Não volátil

</dd> </dl>

</dd> <dt>

**Versão**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Versão do elemento físico.

Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **Win32 \_ PhysicalMemory** é derivada de [**CIM \_ PhysicalMemory**](cim-physicalmemory.md).

## <a name="examples"></a>Exemplos

As [informações do computador get-ComputerInfo-Query de computadores locais/remotos-(WMI) exemplo do](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell na galeria do TechNet usam várias chamadas para hardware e software, incluindo **Win32 \_ PhysicalMemory**, para exibir informações sobre um sistema local ou remoto.

A amostra do PowerShell de [relatório do servidor](https://Gallery.TechNet.Microsoft.Com/Server-Report-7b4ac2fb) na galeria do TechNet usa várias chamadas para hardware e software, incluindo **Win32 \_ PhysicalMemory**, para coletar informações do servidor e publicar no documento do Word.

O exemplo de código do PowerShell a seguir recupera informações sobre a memória física do computador local.


```PowerShell
function get-WmiMemoryFormFactor {
param ([uint16] $char)

If ($char -ge 0 -and  $char  -le 22) {

switch ($char) {
0     {"00-Unknown"}
1     {"01-Other"}
2     {"02-SiP"}
3     {"03-DIP"}
4     {"04-ZIP"}
5     {"05-SOJ"}
6     {"06-Proprietary"}
7     {"07-SIMM"}
8     {"08-DIMM"}
9     {"09-TSOPO"}
10     {"10-PGA"}
11     {"11-RIM"}
12     {"12-SODIMM"}
13     {"13-SRIMM"}
14     {"14-SMD"}
15     {"15-SSMP"}
16     {"16-QFP"}
17     {"17-TQFP"}
18     {"18-SOIC"}
19     {"19-LCC"}
20     {"20-PLCC"}
21     {"21-FPGA"}
22     {"22-LGA"}
}
}

else {"{0} - undefined value" -f $char
}

Return
}

# Helper function to return memory Interleave  Position

function get-WmiInterleavePosition {
param ([uint32] $char)

If ($char -ge 0 -and  $char -le 2) {

switch ($char) {
0     {"00-Non-Interleaved"}
1     {"01-First Position"}
2     {"02-Second Position"}
}
}

else {"{0} - undefined value" -f $char
}

Return
}


# Helper function to return Memory Tupe
function get-WmiMemoryType {
param ([uint16] $char)

If ($char -ge 0 -and  $char  -le 20) {

switch ($char) {
0     {"00-Unknown"}
1     {"01-Other"}
2     {"02-DRAM"}
3     {"03-Synchronous DRAM"}
4     {"04-Cache DRAM"}
5     {"05-EDO"}
6     {"06-EDRAM"}
7     {"07-VRAM"}
8     {"08-SRAM"}
9     {"09-ROM"}
10     {"10-ROM"}
11     {"11-FLASH"}
12     {"12-EEPROM"}
13     {"13-FEPROM"}
14     {"14-EPROM"}
15     {"15-CDRAM"}
16     {"16-3DRAM"}
17     {"17-SDRAM"}
18     {"18-SGRAM"}
19     {"19-RDRAM"}
20     {"20-DDR"}
}

}

else {"{0} - undefined value" -f $char
}

Return
}


# Get the object
$memory = Get-WMIObject Win32_PhysicalMemory

#  Format and Print
"System has {0} memory sticks:" -f $memory.count

Foreach ($stick in $memory) {

# Do some conversions
$cap=$stick.capacity/1mb
$ff=get-WmiMemoryFormFactor($stick.FormFactor)
$ilp=get-WmiInterleavePosition($stick.InterleavePosition)
$mt=get-WMIMemoryType($stick.MemoryType)

# print details of each stick
"BankLabel            {0}"  -f $stick.banklabel
"Capacity (MB)        {0}"  -f $cap
"Caption              {0}"  -f $stick.Caption
"CreationClassName    {0}"  -f $stick.creationclassname
"DataWidth            {0}"  -f $stick.DataWidth
"Description          {0}"  -f $stick.Description
"DeviceLocator        {0}"  -f $stick.DeviceLocator
"FormFactor           {0}"  -f $ff
"HotSwappable         {0}"  -f $stick.HotSwappable
"InstallDate          {0}"  -f $stick.InstallDate
"InterleaveDataDepth  {0}"  -f $stick.InterleaveDataDepth
"InterleavePosition   {0}"  -f $ilp
"Manufacturer         {0}"  -f $stick.Manufacturer
"MemoryType           {0}"  -f $mt
"Model                {0}"  -f $stick.Model
"Name                 {0}"  -f $stick.Name
"OtherIdentifyingInfo {0}"  -f $stick.OtherIdentifyingInfo
"PartNumber           {0}"  -f $stick.PartNumber
"PositionInRow        {0}"  -f $stick.PositionInRow
"PoweredOn            {0}"  -f $stick.PoweredOn
"Removable            {0}"  -f $stick.Removable
"Replaceable          {0}"  -f $stick.Replaceable
"SerialNumber         {0}"  -f $stick.SerialNumber
"SKU                  {0}"  -f $stick.SKU 
"Speed                {0}"  -f $stick.Speed 
"Status               {0}"  -f $stick.Status
"Tag                  {0}"  -f $stick.Tag
"TotalWidth           {0}"  -f $stick.TotalWidth 
"TypeDetail           {0}"  -f $stick.TypeDetail
"Version              {0}"  -f $stick.Version
""
}
"-----"
```



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

[**CIM \_ PhysicalMemory**](cim-physicalmemory.md)
</dt> <dt>

[Classes de hardware do sistema de computador](computer-system-hardware-classes.md)
</dt> </dl>

 

 
