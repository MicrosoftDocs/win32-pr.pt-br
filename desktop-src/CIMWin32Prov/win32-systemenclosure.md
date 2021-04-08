---
description: Representa as propriedades que estão associadas a um compartimento de sistema físico.
ms.assetid: a8244dc0-a95e-4940-9b92-7820bdf14916
ms.tgt_platform: multiple
title: Classe Win32_SystemEnclosure
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemEnclosure
- Win32_SystemEnclosure.IsCompatible
- Win32_SystemEnclosure.AudibleAlarm
- Win32_SystemEnclosure.BreachDescription
- Win32_SystemEnclosure.CableManagementStrategy
- Win32_SystemEnclosure.Caption
- Win32_SystemEnclosure.ChassisTypes
- Win32_SystemEnclosure.CreationClassName
- Win32_SystemEnclosure.CurrentRequiredOrProduced
- Win32_SystemEnclosure.Depth
- Win32_SystemEnclosure.Description
- Win32_SystemEnclosure.HeatGeneration
- Win32_SystemEnclosure.Height
- Win32_SystemEnclosure.HotSwappable
- Win32_SystemEnclosure.InstallDate
- Win32_SystemEnclosure.LockPresent
- Win32_SystemEnclosure.Manufacturer
- Win32_SystemEnclosure.Model
- Win32_SystemEnclosure.Name
- Win32_SystemEnclosure.NumberOfPowerCords
- Win32_SystemEnclosure.OtherIdentifyingInfo
- Win32_SystemEnclosure.PartNumber
- Win32_SystemEnclosure.PoweredOn
- Win32_SystemEnclosure.Removable
- Win32_SystemEnclosure.Replaceable
- Win32_SystemEnclosure.SecurityBreach
- Win32_SystemEnclosure.SecurityStatus
- Win32_SystemEnclosure.SerialNumber
- Win32_SystemEnclosure.ServiceDescriptions
- Win32_SystemEnclosure.ServicePhilosophy
- Win32_SystemEnclosure.SKU
- Win32_SystemEnclosure.SMBIOSAssetTag
- Win32_SystemEnclosure.Status
- Win32_SystemEnclosure.Tag
- Win32_SystemEnclosure.TypeDescriptions
- Win32_SystemEnclosure.Version
- Win32_SystemEnclosure.VisibleAlarm
- Win32_SystemEnclosure.Weight
- Win32_SystemEnclosure.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c7f3b65f6435d8ff828aebf5310f9b21a2ea7f6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920555"
---
# <a name="win32_systemenclosure-class"></a>\_Classe Win32 SystemEnclosure

A [classe WMI](../wmisdk/retrieving-a-class.md) **\_ SystemEnclosure do Win32** representa as propriedades que estão associadas a um compartimento de sistema físico.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B94-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_SystemEnclosure : CIM_Chassis
{
  boolean  AudibleAlarm;
  string   BreachDescription;
  string   CableManagementStrategy;
  string   Caption;
  uint16   ChassisTypes[];
  string   CreationClassName;
  sint16   CurrentRequiredOrProduced;
  real32   Depth;
  string   Description;
  uint16   HeatGeneration;
  real32   Height;
  boolean  HotSwappable;
  datetime InstallDate;
  boolean  LockPresent;
  string   Manufacturer;
  string   Model;
  string   Name;
  uint16   NumberOfPowerCords;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  uint16   SecurityBreach;
  uint16   SecurityStatus;
  string   SerialNumber;
  string   ServiceDescriptions[];
  uint16   ServicePhilosophy[];
  string   SKU;
  string   SMBIOSAssetTag;
  string   Status;
  string   Tag;
  string   TypeDescriptions[];
  string   Version;
  boolean  VisibleAlarm;
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ SystemEnclosure** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **Win32 \_ SystemEnclosure** tem esses métodos.



| Método           | Descrição                 |
|:-----------------|:----------------------------|
| **Iscompatível** | Não implementado.<br/> |



 

### <a name="properties"></a>Propriedades

A classe **Win32 \_ SystemEnclosure** tem essas propriedades.

<dl> <dt>

**AudibleAlarm**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se for **true**, o quadro será equipado com um alarme audível.

Essa propriedade é herdada do [**CIM \_ PhysicalFrame**](cim-physicalframe.md).

</dd> <dt>

**BreachDescription**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**SecurityBreach**")
</dt> </dl>

Cadeia de caracteres de forma livre que fornece mais informações se a propriedade **SecurityBreach** indicar que ocorreu um evento relacionado à segurança.

Essa propriedade é herdada do [**CIM \_ PhysicalFrame**](cim-physicalframe.md).

</dd> <dt>

**CableManagementStrategy**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Cadeia de caracteres de forma livre que contém informações sobre como os vários cabos são conectados e agrupados para o quadro. Com muitos cabos de rede, relacionados ao armazenamento e de energia, o gerenciamento de cabos pode ser um esforço complexo e desafiador. Essa propriedade contém informações para auxiliar no assembly e no serviço do quadro.

Essa propriedade é herdada do [**CIM \_ PhysicalFrame**](cim-physicalframe.md).

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

**ChassisTypes**
</dt> <dd> <dl> <dt>

Tipo de dados: a matriz **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("indexado"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Tabela global de contêiner físico DMTF \| 2,1 "), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ([**" \_ chassi CIM**](cim-chassis.md).**TypeDescriptions**")
</dt> </dl>

Matriz de tipos de chassi.

Esse valor é proveniente do membro de **tipo** do **compartimento do sistema ou** da estrutura do chassi nas informações do SMBIOS.

Essa propriedade é herdada [**do \_ chassi CIM**](cim-chassis.md).

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (2)


</dt> <dd></dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

**Área de trabalho** (3)


</dt> <dd></dd> <dt>

<span id="Low_Profile_Desktop"></span><span id="low_profile_desktop"></span><span id="LOW_PROFILE_DESKTOP"></span>

**Área de trabalho de baixo perfil** (4)


</dt> <dd></dd> <dt>

<span id="Pizza_Box"></span><span id="pizza_box"></span><span id="PIZZA_BOX"></span>

**Caixa de pizza** (5)


</dt> <dd></dd> <dt>

<span id="Mini_Tower"></span><span id="mini_tower"></span><span id="MINI_TOWER"></span>

**Mini-torre** (6)


</dt> <dd></dd> <dt>

<span id="Tower"></span><span id="tower"></span><span id="TOWER"></span>

**Torre** (7)


</dt> <dd></dd> <dt>

<span id="Portable"></span><span id="portable"></span><span id="PORTABLE"></span>

**Portátil** (8)


</dt> <dd></dd> <dt>

<span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>

**Laptop** (9)


</dt> <dd></dd> <dt>

<span id="Notebook"></span><span id="notebook"></span><span id="NOTEBOOK"></span>

**Notebook** (10)


</dt> <dd></dd> <dt>

<span id="Hand_Held"></span><span id="hand_held"></span><span id="HAND_HELD"></span>

**Mão suspensa** (11)


</dt> <dd></dd> <dt>

<span id="Docking_Station"></span><span id="docking_station"></span><span id="DOCKING_STATION"></span>

**Estação de encaixe** (12)


</dt> <dd></dd> <dt>

<span id="All_in_One"></span><span id="all_in_one"></span><span id="ALL_IN_ONE"></span>

**Tudo em um** (13)


</dt> <dd></dd> <dt>

<span id="Sub_Notebook"></span><span id="sub_notebook"></span><span id="SUB_NOTEBOOK"></span>

**Subnotebook** (14)


</dt> <dd></dd> <dt>

<span id="Space-Saving"></span><span id="space-saving"></span><span id="SPACE-SAVING"></span>

**Economia de espaço** (15)


</dt> <dd></dd> <dt>

<span id="Lunch_Box"></span><span id="lunch_box"></span><span id="LUNCH_BOX"></span>

**Caixa de almoço** (16)


</dt> <dd></dd> <dt>

<span id="Main_System_Chassis"></span><span id="main_system_chassis"></span><span id="MAIN_SYSTEM_CHASSIS"></span>

**Chassi do sistema principal** (17)


</dt> <dd></dd> <dt>

<span id="Expansion_Chassis"></span><span id="expansion_chassis"></span><span id="EXPANSION_CHASSIS"></span>

**Chassi de expansão** (18)


</dt> <dd></dd> <dt>

<span id="SubChassis"></span><span id="subchassis"></span><span id="SUBCHASSIS"></span>

**Subchassi** (19)


</dt> <dd></dd> <dt>

<span id="Bus_Expansion_Chassis"></span><span id="bus_expansion_chassis"></span><span id="BUS_EXPANSION_CHASSIS"></span>

**Chassi de expansão de barramento** (20)


</dt> <dd></dd> <dt>

<span id="Peripheral_Chassis"></span><span id="peripheral_chassis"></span><span id="PERIPHERAL_CHASSIS"></span>

**Chassi de periférico** (21)


</dt> <dd></dd> <dt>

<span id="Storage_Chassis"></span><span id="storage_chassis"></span><span id="STORAGE_CHASSIS"></span>

**Chassi de armazenamento** (22)


</dt> <dd></dd> <dt>

<span id="Rack_Mount_Chassis"></span><span id="rack_mount_chassis"></span><span id="RACK_MOUNT_CHASSIS"></span>

**Chassi de montagem em rack** (23)


</dt> <dd></dd> <dt>

<span id="Sealed-Case_PC"></span><span id="sealed-case_pc"></span><span id="SEALED-CASE_PC"></span>

**PC de caso lacrado** (24)

</dt> <dd></dd> <dt>

<span id="Tablet"></span><span id="tablet"></span><span id="TABLET"></span>

**Tablet** (30)

</dt> <dd></dd> <dt>

<span id="Convertible"></span><span id="Convertible"></span><span id="Convertible"></span>

**Conversível** (31)

</dt> <dd></dd> <dt>

<span id="Detachable"></span><span id="Detachable "></span><span id="Detachable "></span>

**Desanexável** (32)


</dt> <dd></dd> </dl>

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Nome da primeira classe concreta que aparece na cadeia de herança que é usada na criação de uma instância. Quando usado com as outras propriedades de chave da classe, essa propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.

Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).

</dd> <dt>

**CurrentRequiredOrProduced**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("amps às 120 volts")
</dt> </dl>

O atual é exigido pelo chassi em 120V. Se a energia for fornecida pelo chassi — como no caso de uma fonte de alimentação ininterrupta (UPS) — essa propriedade poderá indicar a amperagem produzida (como um número negativo).

Essa propriedade é herdada [**do \_ chassi CIM**](cim-chassis.md).

</dd> <dt>

**Profundidade**
</dt> <dd> <dl> <dt>

Tipo de dados: **real32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("polegadas")
</dt> </dl>

Profundidade do pacote físico — em polegadas.

Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")
</dt> </dl>

Descrição do objeto.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**HeatGeneration**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("BTU por hora")
</dt> </dl>

Quantidade de calor que é gerada pelo chassi em BTU/hora.

Essa propriedade é herdada [**do \_ chassi CIM**](cim-chassis.md).

</dd> <dt>

**Altura**
</dt> <dd> <dl> <dt>

Tipo de dados: **real32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("polegadas")
</dt> </dl>

Altura do pacote físico — em polegadas.

Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).

</dd> <dt>

**HotSwappable**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se for **true**, um pacote físico poderá ser trocado de maneira intercambiável (se for possível substituir o elemento por um fisicamente diferente, mas equivalente um, enquanto o pacote recipiente tiver energia aplicada a ele). Por exemplo, um pacote de unidade de disco inserido usando conectores de SCA é removível e pode ser intercambiável. Todos os pacotes que podem ser intercambiáveis são inerentemente removíveis e substituíveis.

Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")
</dt> </dl>

Data e hora em que o objeto foi instalado. Essa propriedade não requer um valor para indicar que o objeto está instalado.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**LockPresent**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se for **true**, o quadro será protegido com um bloqueio.

Essa propriedade é herdada do [**CIM \_ PhysicalFrame**](cim-physicalframe.md).

</dd> <dt>

**Manufacturer**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Nome da organização que produz o elemento físico.

Esse valor é proveniente do membro do **fabricante** do **compartimento do sistema ou** da estrutura do chassi nas informações do SMBIOS.

Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).

</dd> <dt>

**Modelo**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Nome pelo qual o elemento físico é conhecido.

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

Rótulo pelo qual o objeto é conhecido. Quando em uma subclasse, a propriedade pode ser substituída para ser uma propriedade de chave.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**NumberOfPowerCords**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de cabos de alimentação que devem ser conectados ao chassi para que todos os componentes operem.

Essa propriedade é herdada [**do \_ chassi CIM**](cim-chassis.md).

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Dados adicionais, além das informações de marca do ativo, que podem ser usados para identificar um elemento físico. Um exemplo são os dados de código de barras associados a um elemento que também tem uma marca de ativo. Lembre-se de que, se apenas os dados de código de barras estiverem disponíveis e for exclusivo ou puderem ser usados como uma chave de elemento, essa propriedade será **NULL** e os dados de código de barras usados como a chave de classe, na propriedade Tag.

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

Número de peça atribuído pela organização que produz ou fabrica o elemento físico.

Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).

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

Se for **true**, um pacote físico será removível (se for projetado para ser levado para dentro e para fora do contêiner físico no qual ele normalmente é encontrado, sem encontrar a função do empacotamento geral). Um pacote ainda poderá ser removível se a potência precisar ser "desativada" para executar a remoção. Se o pacote puder ser removido enquanto a energia estiver ATIVAda, o elemento será removível e poderá ser intercambiável. Por exemplo, uma bateria extra em um laptop é removível, assim como um pacote de unidade de disco que é inserido usando conectores do aplicativo de configuração de servidor (SCA). No entanto, o último pode ser intercambiável. Uma exibição de laptop não é removível, nem uma fonte de alimentação não redundante. A remoção desses componentes afetaria a função do empacotamento geral ou é impossível devido à forte integração do pacote.

Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).

</dd> <dt>

**Peças**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se **for true**, esse componente de mídia física poderá ser substituído por um fisicamente diferente. Por exemplo, alguns sistemas de computador permitem que o chip do processador principal seja atualizado para uma classificação de clock mais alta. Nesse caso, diz-se que o processador é substituível. Outro exemplo é um pacote de fornecimento de energia montado em trilhos deslizantes. Todos os pacotes removíveis são inerentemente substituíveis.

Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).

</dd> <dt>

**SecurityBreach**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Tabela global de contêiner físico DMTF \| 2,12 "), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**BreachDescription**")
</dt> </dl>

Status de uma violação física do quadro.

Essa propriedade é herdada do [**CIM \_ PhysicalFrame**](cim-physicalframe.md).

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (2)


</dt> <dd></dd> <dt>

<span id="No_Breach"></span><span id="no_breach"></span><span id="NO_BREACH"></span>

**Sem violação** (3)


</dt> <dd></dd> <dt>

<span id="Breach_Attempted"></span><span id="breach_attempted"></span><span id="BREACH_ATTEMPTED"></span>

**Tentativa de violação** (4)


</dt> <dd></dd> <dt>

<span id="Breach_Successful"></span><span id="breach_successful"></span><span id="BREACH_SUCCESSFUL"></span>

**Violação bem-sucedida** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**SecurityStatus**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("status de segurança do SMBIOS \| tipo 3 \| ")
</dt> </dl>

Configuração de segurança para entrada externa, por exemplo, um teclado, para um computador.

Esse valor é proveniente do membro de **status de segurança** do **compartimento do sistema ou** da estrutura do chassi nas informações do SMBIOS.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (2)


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Nenhum** (3)


</dt> <dd></dd> <dt>

<span id="External_interface_locked_out"></span><span id="external_interface_locked_out"></span><span id="EXTERNAL_INTERFACE_LOCKED_OUT"></span>

**Interface externa bloqueada** (4)


</dt> <dd></dd> <dt>

<span id="External_interface_enabled"></span><span id="external_interface_enabled"></span><span id="EXTERNAL_INTERFACE_ENABLED"></span>

**Interface externa habilitada** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**SerialNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Número alocado pelo fabricante usado para identificar o elemento físico.

Esse valor é proveniente do membro de **número de série** do **compartimento do sistema ou** da estrutura do chassi nas informações do SMBIOS.

Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).

</dd> <dt>

**ServiceDescriptions**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("indexado"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ([**" \_ CIM PhysicalFrame**](cim-physicalframe.md).**Infilosofia**")
</dt> </dl>

Matriz de explicações mais detalhadas para qualquer uma das entradas na matriz de **unifilosofia** . Lembre-se de que cada entrada dessa matriz está relacionada à entrada no **perfilosofia** que está localizada no mesmo índice.

Essa propriedade é herdada do [**CIM \_ PhysicalFrame**](cim-physicalframe.md).

</dd> <dt>

**Infilosofia**
</dt> <dd> <dl> <dt>

Tipo de dados: a matriz **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("indexado"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ([**" \_ CIM PhysicalFrame**](cim-physicalframe.md).**ServiceDescriptions**")
</dt> </dl>

Matriz que inclui se o quadro é atendido de cima, para frente, para trás ou para o lado, se o quadro tem bandejas deslizantes ou lados removíveis e se o quadro é móvel, por exemplo, com os cilindros.

Essa propriedade é herdada do [**CIM \_ PhysicalFrame**](cim-physicalframe.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outro** (1)


</dt> <dd></dd> <dt>

<span id="Service_From_Top"></span><span id="service_from_top"></span><span id="SERVICE_FROM_TOP"></span>

**Serviço da parte superior** (2)


</dt> <dd></dd> <dt>

<span id="Service_From_Front"></span><span id="service_from_front"></span><span id="SERVICE_FROM_FRONT"></span>

**Serviço da frente** (3)


</dt> <dd></dd> <dt>

<span id="Service_From_Back"></span><span id="service_from_back"></span><span id="SERVICE_FROM_BACK"></span>

**Serviço de volta** (4)


</dt> <dd></dd> <dt>

<span id="Service_From_Side"></span><span id="service_from_side"></span><span id="SERVICE_FROM_SIDE"></span>

**Serviço do lado** (5)


</dt> <dd></dd> <dt>

<span id="Sliding_Trays"></span><span id="sliding_trays"></span><span id="SLIDING_TRAYS"></span>

**Bandejas deslizantes** (6)


</dt> <dd></dd> <dt>

<span id="Removable_Sides"></span><span id="removable_sides"></span><span id="REMOVABLE_SIDES"></span>

**Lados removíveis** (7)


</dt> <dd></dd> <dt>

<span id="Moveable"></span><span id="moveable"></span><span id="MOVEABLE"></span>

**Móvel** (8)


</dt> <dd></dd> </dl>

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

**SMBIOSAssetTag**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("marca de ativo do SMBIOS \| tipo 3 \| ")
</dt> </dl>

Número da marca do ativo do compartimento do sistema.

Esse valor é proveniente do membro de **número de marca de ativo** do compartimento do **sistema ou** da estrutura do chassi nas informações do SMBIOS.

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

Os valores incluem o seguinte:

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

Identificador exclusivo do compartimento do sistema.

Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).

Exemplo: "compartimento do sistema 1"

</dd> <dt>

**TypeDescriptions**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("indexado"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ([**" \_ chassi CIM**](cim-chassis.md).**ChassisTypes**")
</dt> </dl>

Matriz de mais informações sobre as entradas de matriz **ChassisTypes** . Lembre-se de que cada entrada dessa matriz está relacionada à entrada em **ChassisTypes** que está localizada no mesmo índice.

Essa propriedade é herdada [**do \_ chassi CIM**](cim-chassis.md).

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

Esse valor é proveniente do membro da **versão** do **compartimento do sistema ou** da estrutura do chassi nas informações do SMBIOS.

Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).

</dd> <dt>

**VisibleAlarm**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se **for true**, o equipamento incluirá um alarme visível.

Essa propriedade é herdada do [**CIM \_ PhysicalFrame**](cim-physicalframe.md).

</dd> <dt>

**Weight**
</dt> <dd> <dl> <dt>

Tipo de dados: **real32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("libras")
</dt> </dl>

Peso do pacote físico em libras.

Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).

</dd> <dt>

**Largura**
</dt> <dd> <dl> <dt>

Tipo de dados: **real32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("polegadas")
</dt> </dl>

Largura do pacote físico em polegadas.

Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **Win32 \_ SystemEnclosure** é derivada do [**\_ chassi CIM**](cim-chassis.md).

## <a name="examples"></a>Exemplos

O exemplo de [coleta de ativos de sistema multithread com](https://Gallery.TechNet.Microsoft.Com/Multithreaded-System-Asset-856a8f7c) PowerShell do PowerShell na galeria do TechNet usa várias classes, incluindo **Win32 \_ SystemEnclosure**, para recuperar dados de um sistema.

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

[**\_Chassi CIM**](cim-chassis.md)
</dt> <dt>

[Classes de hardware do sistema de computador](computer-system-hardware-classes.md)
</dt> <dt>

[Tarefas do WMI: hardware do computador](../wmisdk/wmi-tasks--computer-hardware.md)
</dt> </dl>

 

 
