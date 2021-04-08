---
description: A \_ classe de chassi CIM representa os elementos físicos que incluem outros elementos e fornece funcionalidade definíveis, como um desktop, nó de processamento, UPS, armazenamento em disco ou fita ou uma combinação desses.
ms.assetid: 4c55dbff-bc4a-4cc9-8f34-29636defaa56
ms.tgt_platform: multiple
title: Classe CIM_Chassis
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Chassis
- CIM_Chassis.Caption
- CIM_Chassis.Description
- CIM_Chassis.InstallDate
- CIM_Chassis.Name
- CIM_Chassis.Status
- CIM_Chassis.CreationClassName
- CIM_Chassis.Manufacturer
- CIM_Chassis.Model
- CIM_Chassis.OtherIdentifyingInfo
- CIM_Chassis.PartNumber
- CIM_Chassis.PoweredOn
- CIM_Chassis.SerialNumber
- CIM_Chassis.SKU
- CIM_Chassis.Tag
- CIM_Chassis.Version
- CIM_Chassis.Depth
- CIM_Chassis.Height
- CIM_Chassis.HotSwappable
- CIM_Chassis.Removable
- CIM_Chassis.Replaceable
- CIM_Chassis.Weight
- CIM_Chassis.Width
- CIM_Chassis.AudibleAlarm
- CIM_Chassis.BreachDescription
- CIM_Chassis.CableManagementStrategy
- CIM_Chassis.LockPresent
- CIM_Chassis.SecurityBreach
- CIM_Chassis.ServiceDescriptions
- CIM_Chassis.ServicePhilosophy
- CIM_Chassis.VisibleAlarm
- CIM_Chassis.ChassisTypes
- CIM_Chassis.CurrentRequiredOrProduced
- CIM_Chassis.HeatGeneration
- CIM_Chassis.NumberOfPowerCords
- CIM_Chassis.TypeDescriptions
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b1eb7f5e2733056cf48c1c9333453613ace699c6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089354"
---
# <a name="cim_chassis-class"></a>\_Classe de chassi CIM

A classe de **\_ chassi CIM** representa os elementos físicos que incluem outros elementos e fornece funcionalidade definíveis, como um desktop, nó de processamento, UPS, armazenamento em disco ou fita ou uma combinação desses.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[abstract, UUID("{FAF76B72-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Chassis : CIM_PhysicalFrame
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  string   Manufacturer;
  string   Model;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  string   SerialNumber;
  string   SKU;
  string   Tag;
  string   Version;
  real32   Depth;
  real32   Height;
  boolean  HotSwappable;
  boolean  Removable;
  boolean  Replaceable;
  real32   Weight;
  real32   Width;
  boolean  AudibleAlarm;
  string   BreachDescription;
  string   CableManagementStrategy;
  boolean  LockPresent;
  uint16   SecurityBreach;
  string   ServiceDescriptions[];
  uint16   ServicePhilosophy[];
  boolean  VisibleAlarm;
  uint16   ChassisTypes[];
  sint16   CurrentRequiredOrProduced;
  uint16   HeatGeneration;
  uint16   NumberOfPowerCords;
  string   TypeDescriptions[];
};
```

## <a name="members"></a>Membros

A classe de **\_ chassi CIM** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe de **\_ chassi CIM** tem esses métodos.



| Método                                                           | Descrição                                                                                                                                      |
|:-----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Iscompatível**](iscompatible-method-in-class-cim-chassis.md) | Verifica se o elemento físico referenciado pode ser contido ou inserido no pacote físico. Não implementado pelo WMI.<br/> |



 

### <a name="properties"></a>Propriedades

A classe de **\_ chassi CIM** tem essas propriedades.

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

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**SecurityBreach**")
</dt> </dl>

Cadeia de caracteres de forma livre que fornece mais informações se a propriedade **SecurityBreach** indicar que ocorreu uma violação ou algum outro evento relacionado à segurança.

Essa propriedade é herdada do [**CIM \_ PhysicalFrame**](cim-physicalframe.md).

</dd> <dt>

**CableManagementStrategy**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Cadeia de caracteres de forma livre que contém informações sobre como os vários cabos são conectados e agrupados para o quadro. Com muitos cabos de rede, relacionados ao armazenamento e de energia, o gerenciamento de cabos pode ser um esforço complexo e desafiador. Essa propriedade de cadeia de caracteres contém informações para auxiliar no assembly e no serviço do quadro.

Essa propriedade é herdada do [**CIM \_ PhysicalFrame**](cim-physicalframe.md).

</dd> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Uma breve descrição textual do objeto.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**ChassisTypes**
</dt> <dd> <dl> <dt>

Tipo de dados: a matriz **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Tabela global de contêiner físico DMTF \| 2,1 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ chassi CIM**.**TypeDescriptions**")
</dt> </dl>

Enumeração, matriz com valor inteiro que indica o tipo de chassi.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)


</dt> <dd>

Outros.

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)


</dt> <dd>

Desconhecido.

</dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**Área de trabalho** (3)


</dt> <dd>

Desktop.

</dd> <dt>

<span id="Low_Profile_Desktop"></span><span id="low_profile_desktop"></span><span id="LOW_PROFILE_DESKTOP"></span>

<span id="Low_Profile_Desktop"></span><span id="low_profile_desktop"></span><span id="LOW_PROFILE_DESKTOP"></span>**Área de trabalho de baixo perfil** (4)


</dt> <dd>

Área de trabalho de baixo perfil.

</dd> <dt>

<span id="Pizza_Box"></span><span id="pizza_box"></span><span id="PIZZA_BOX"></span>

<span id="Pizza_Box"></span><span id="pizza_box"></span><span id="PIZZA_BOX"></span>**Caixa de pizza** (5)


</dt> <dd>

Caixa de pizza.

</dd> <dt>

<span id="Mini_Tower"></span><span id="mini_tower"></span><span id="MINI_TOWER"></span>

<span id="Mini_Tower"></span><span id="mini_tower"></span><span id="MINI_TOWER"></span>**Mini-torre** (6)


</dt> <dd>

Mini-torre.

</dd> <dt>

<span id="Tower"></span><span id="tower"></span><span id="TOWER"></span>

<span id="Tower"></span><span id="tower"></span><span id="TOWER"></span>**Torre** (7)


</dt> <dd>

Torre.

</dd> <dt>

<span id="Portable"></span><span id="portable"></span><span id="PORTABLE"></span>

<span id="Portable"></span><span id="portable"></span><span id="PORTABLE"></span>**Portátil** (8)


</dt> <dd>

Portátil.

</dd> <dt>

<span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>

<span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>**Laptop** (9)


</dt> <dd>

Laptop.

</dd> <dt>

<span id="Notebook"></span><span id="notebook"></span><span id="NOTEBOOK"></span>

<span id="Notebook"></span><span id="notebook"></span><span id="NOTEBOOK"></span>**Notebook** (10)


</dt> <dd>

D430.

</dd> <dt>

<span id="Hand_Held"></span><span id="hand_held"></span><span id="HAND_HELD"></span>

<span id="Hand_Held"></span><span id="hand_held"></span><span id="HAND_HELD"></span>**Mão suspensa** (11)


</dt> <dd>

Mão.

</dd> <dt>

<span id="Docking_Station"></span><span id="docking_station"></span><span id="DOCKING_STATION"></span>

<span id="Docking_Station"></span><span id="docking_station"></span><span id="DOCKING_STATION"></span>**Estação de encaixe** (12)


</dt> <dd>

Estação de encaixe.

</dd> <dt>

<span id="All_in_One"></span><span id="all_in_one"></span><span id="ALL_IN_ONE"></span>

<span id="All_in_One"></span><span id="all_in_one"></span><span id="ALL_IN_ONE"></span>**Tudo em um** (13)


</dt> <dd>

Tudo-em-um.

</dd> <dt>

<span id="Sub_Notebook"></span><span id="sub_notebook"></span><span id="SUB_NOTEBOOK"></span>

<span id="Sub_Notebook"></span><span id="sub_notebook"></span><span id="SUB_NOTEBOOK"></span>**Subnotebook** (14)


</dt> <dd>

Subnotebook.

</dd> <dt>

<span id="Space-Saving"></span><span id="space-saving"></span><span id="SPACE-SAVING"></span>

<span id="Space-Saving"></span><span id="space-saving"></span><span id="SPACE-SAVING"></span>**Economia de espaço** (15)


</dt> <dd>

Economia de espaço.

</dd> <dt>

<span id="Lunch_Box"></span><span id="lunch_box"></span><span id="LUNCH_BOX"></span>

<span id="Lunch_Box"></span><span id="lunch_box"></span><span id="LUNCH_BOX"></span>**Caixa de almoço** (16)


</dt> <dd>

Caixa de almoço.

</dd> <dt>

<span id="Main_System_Chassis"></span><span id="main_system_chassis"></span><span id="MAIN_SYSTEM_CHASSIS"></span>

<span id="Main_System_Chassis"></span><span id="main_system_chassis"></span><span id="MAIN_SYSTEM_CHASSIS"></span>**Chassi do sistema principal** (17)


</dt> <dd>

Chassi do sistema principal.

</dd> <dt>

<span id="Expansion_Chassis"></span><span id="expansion_chassis"></span><span id="EXPANSION_CHASSIS"></span>

<span id="Expansion_Chassis"></span><span id="expansion_chassis"></span><span id="EXPANSION_CHASSIS"></span>**Chassi de expansão** (18)


</dt> <dd>

Chassi de expansão.

</dd> <dt>

<span id="SubChassis"></span><span id="subchassis"></span><span id="SUBCHASSIS"></span>

<span id="SubChassis"></span><span id="subchassis"></span><span id="SUBCHASSIS"></span>**Subchassi** (19)


</dt> <dd>

Subchassi.

</dd> <dt>

<span id="Bus_Expansion_Chassis"></span><span id="bus_expansion_chassis"></span><span id="BUS_EXPANSION_CHASSIS"></span>

<span id="Bus_Expansion_Chassis"></span><span id="bus_expansion_chassis"></span><span id="BUS_EXPANSION_CHASSIS"></span>**Chassi de expansão de barramento** (20)


</dt> <dd>

Chassi de expansão de barramento.

</dd> <dt>

<span id="Peripheral_Chassis"></span><span id="peripheral_chassis"></span><span id="PERIPHERAL_CHASSIS"></span>

<span id="Peripheral_Chassis"></span><span id="peripheral_chassis"></span><span id="PERIPHERAL_CHASSIS"></span>**Chassi de periférico** (21)


</dt> <dd>

Chassi periférico.

</dd> <dt>

<span id="Storage_Chassis"></span><span id="storage_chassis"></span><span id="STORAGE_CHASSIS"></span>

<span id="Storage_Chassis"></span><span id="storage_chassis"></span><span id="STORAGE_CHASSIS"></span>**Chassi de armazenamento** (22)


</dt> <dd>

Chassi de armazenamento.

</dd> <dt>

<span id="Rack_Mount_Chassis"></span><span id="rack_mount_chassis"></span><span id="RACK_MOUNT_CHASSIS"></span>

<span id="Rack_Mount_Chassis"></span><span id="rack_mount_chassis"></span><span id="RACK_MOUNT_CHASSIS"></span>**Chassi de montagem em rack** (23)


</dt> <dd>

Chassi de montagem de rack.

</dd> <dt>

<span id="Sealed-Case_PC"></span><span id="sealed-case_pc"></span><span id="SEALED-CASE_PC"></span>

<span id="Sealed-Case_PC"></span><span id="sealed-case_pc"></span><span id="SEALED-CASE_PC"></span>**PC de caso lacrado** (24)


</dt> <dd>

Computador com casos lacrados.

</dd> </dl>

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nome da classe ou subclasse usada na criação de uma instância. Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.

Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).

</dd> <dt>

**CurrentRequiredOrProduced**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("amps às 120 volts")
</dt> </dl>

Atualmente exigido pelo chassi às 120 volts. Se a energia for fornecida pelo chassi (como no caso de um UPS), essa propriedade poderá indicar a amperagem produzida, como um número negativo.

</dd> <dt>

**Profundidade**
</dt> <dd> <dl> <dt>

Tipo de dados: **real32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("polegadas")
</dt> </dl>

Profundidade do pacote físico, em polegadas.

Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")
</dt> </dl>

Uma descrição textual do objeto.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**HeatGeneration**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("BTU por hora")
</dt> </dl>

Quantidade de calor gerada pelo chassi em BTU/hora.

</dd> <dt>

**Altura**
</dt> <dd> <dl> <dt>

Tipo de dados: **real32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("polegadas")
</dt> </dl>

Altura do pacote físico, em polegadas.

Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).

</dd> <dt>

**HotSwappable**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se **for true**, o pacote poderá ser intercambiável. Um pacote físico pode ser intercambiável se o elemento puder ser substituído por um fisicamente diferente (mas equivalente) um enquanto o pacote que o contém está ativado. Por exemplo, um componente de ventilador pode ser projetado para ser intercambiável. Todos os componentes que podem ser intercambiáveis são inerentemente removíveis e substituíveis.

Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")
</dt> </dl>

Indica quando o objeto foi instalado. A falta de um valor não indica que o objeto não está instalado.

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

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nome da organização responsável por produzir o elemento físico. Para obter mais informações, consulte a propriedade **Vendor** do [**\_ produto CIM**](cim-product.md).

Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).

</dd> <dt>

**Modelo**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Nome pelo qual o elemento físico é geralmente conhecido.

Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")
</dt> </dl>

Rótulo pelo qual o objeto é conhecido. Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**NumberOfPowerCords**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de cabos de alimentação que devem ser conectados ao chassi para que todos os componentes possam operar.

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Dados adicionais, além das informações de marca do ativo, que podem ser usados para identificar um elemento físico. Um exemplo são dados de código de barras associados a um elemento, que também tem uma marca de ativo. Observe que, se apenas os dados de código de barras estiverem disponíveis e for exclusivo e puderem ser usados como uma chave de elemento, essa propriedade será nula e os dados de código de barras seriam usados como a chave de classe na propriedade de **marca** .

Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).

</dd> <dt>

**PartNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Número de peça atribuído pela organização responsável por produzir ou fabricar o elemento físico.

Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).

</dd> <dt>

**Ligado**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se **for true**, o elemento físico será ligado. Caso contrário, ele estará desativado no momento.

Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).

</dd> <dt>

**Removível**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se for **true**, o pacote será projetado para ser levado para dentro e para fora do contêiner físico no qual ele normalmente é encontrado, sem comprometer a função do empacotamento geral. Um pacote é considerado removível, mesmo que a energia precise ser desligada para executar a remoção. Se a energia puder ser ativada e o pacote for removido, o elemento será removível e poderá ser intercambiável. Por exemplo, um chip de processador atualizável é removível.

Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).

</dd> <dt>

**Peças**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se for **true**, é possível substituir o elemento por um fisicamente diferente. Por exemplo, alguns sistemas de computador permitem que o chip do processador principal seja atualizado para uma classificação de clock mais alta. Nesse caso, diz-se que o processador é substituível. Todos os componentes removíveis são inerentemente substituíveis.

Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).

</dd> <dt>

**SecurityBreach**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Tabela global de contêiner físico DMTF \| 2,12 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**BreachDescription**")
</dt> </dl>

Indica se uma violação física do quadro foi tentada, mas malsucedida, ou se foi bem-sucedida.

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

**SerialNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Número alocado pelo fabricante usado para identificar o elemento físico.

Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).

</dd> <dt>

**ServiceDescriptions**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ CIM PhysicalFrame**](cim-physicalframe.md).**Infilosofia**")
</dt> </dl>

Cadeias de caracteres de forma livre que fornecem explicações detalhadas para entradas na matriz de **unifilosofia** .

> [!Note]  
> Cada entrada dessa matriz está relacionada à entrada na matriz de **unifilosofia** que está localizada no mesmo índice.

 

Essa propriedade é herdada do [**CIM \_ PhysicalFrame**](cim-physicalframe.md).

</dd> <dt>

**Infilosofia**
</dt> <dd> <dl> <dt>

Tipo de dados: a matriz **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ CIM PhysicalFrame**](cim-physicalframe.md).**ServiceDescriptions**")
</dt> </dl>

Indica se o quadro é atendido de cima, para frente, para trás ou para o lado; e se ele tem bandejas deslizantes ou lados removíveis e se o quadro é móvel (por exemplo, com cilindros).

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

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Número de unidade de manutenção de estoque para este elemento físico.

Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")
</dt> </dl>

Cadeia de caracteres que indica o status atual do objeto. O status operacional e não operacional pode ser definido. O status operacional pode incluir "OK", "degradado" e "Pred falha". "Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).

O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço". O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo. Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.

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

Qualificadores: [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Identifica exclusivamente o elemento físico e serve como a chave do elemento. Essa propriedade pode conter informações, como a marca de ativo ou os dados de número de série. A chave para [**o \_ físico do CIM**](cim-physicalelement.md) é colocada muito alta na hierarquia de objetos para identificar de forma independente o hardware ou a entidade, independentemente do posicionamento físico nos gabinetes, adaptadores e assim por diante. Por exemplo, um componente removível que pode ser intercambiável pode ser extraído de seu pacote recipiente (escopo) e estar temporariamente não utilizado. O objeto ainda continua existindo e pode até ser inserido em um contêiner de escopo diferente. A chave para um elemento físico é uma cadeia de caracteres arbitrária que é definida independentemente do posicionamento ou da hierarquia orientada por local.

Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).

</dd> <dt>

**TypeDescriptions**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ chassi CIM**.**ChassisTypes**")
</dt> </dl>

Matriz de cadeias de caracteres de forma livre que fornece informações sobre as entradas da matriz **ChassisTypes** .

> [!Note]  
> Cada entrada de matriz está relacionada à entrada na propriedade **ChassisTypes** , que está localizada no mesmo índice.

 

</dd> <dt>

**Versão**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Indica a versão do elemento físico.

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

Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("libras")
</dt> </dl>

Peso do pacote físico, em libras.

Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).

</dd> <dt>

**Largura**
</dt> <dd> <dl> <dt>

Tipo de dados: **real32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("polegadas")
</dt> </dl>

Largura do pacote físico, em polegadas.

Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe de **\_ chassi CIM** é derivada do [**CIM \_ PhysicalFrame**](cim-physicalframe.md).

O WMI não implementa essa classe. Para obter mais informações sobre classes derivadas **do \_ chassi CIM**, consulte [classes Win32](win32-provider.md).

Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF. A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.

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

[**\_PHYSICALFRAME CIM**](cim-physicalframe.md)
</dt> </dl>

 

