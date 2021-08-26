---
description: A \_ classe de rack CIM representa um rack (um quadro físico ou compartimento) no qual os chassis são armazenados. Normalmente, um rack representa o compartimento; todos os componentes em funcionamento são empacotados no chassi.
ms.assetid: 1e0273ce-2a09-4f75-a82e-d0555d6a831e
ms.tgt_platform: multiple
title: Classe CIM_Rack
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Rack
- CIM_Rack.AudibleAlarm
- CIM_Rack.BreachDescription
- CIM_Rack.CableManagementStrategy
- CIM_Rack.Caption
- CIM_Rack.CountryDesignation
- CIM_Rack.CreationClassName
- CIM_Rack.Depth
- CIM_Rack.Description
- CIM_Rack.Height
- CIM_Rack.HotSwappable
- CIM_Rack.InstallDate
- CIM_Rack.LockPresent
- CIM_Rack.Manufacturer
- CIM_Rack.Model
- CIM_Rack.Name
- CIM_Rack.OtherIdentifyingInfo
- CIM_Rack.PartNumber
- CIM_Rack.PoweredOn
- CIM_Rack.Removable
- CIM_Rack.Replaceable
- CIM_Rack.SecurityBreach
- CIM_Rack.SerialNumber
- CIM_Rack.ServiceDescriptions
- CIM_Rack.ServicePhilosophy
- CIM_Rack.SKU
- CIM_Rack.Status
- CIM_Rack.Tag
- CIM_Rack.TypeOfRack
- CIM_Rack.Version
- CIM_Rack.VisibleAlarm
- CIM_Rack.Weight
- CIM_Rack.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a16c6d0f3594f4fe3b322b5561edf679ded259091f22eade7d831c63fee8f780
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921086"
---
# <a name="cim_rack-class"></a>\_Classe de rack CIM

A classe de **\_ rack CIM** representa um rack (um quadro físico ou compartimento) no qual os chassis são armazenados. Normalmente, um rack representa o compartimento; todos os componentes em funcionamento são empacotados no chassi.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, UUID("{FAF76B71-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Rack : CIM_PhysicalFrame
{
  boolean  AudibleAlarm;
  string   BreachDescription;
  string   CableManagementStrategy;
  string   Caption;
  string   CountryDesignation;
  string   CreationClassName;
  real32   Depth;
  string   Description;
  real32   Height;
  boolean  HotSwappable;
  datetime InstallDate;
  boolean  LockPresent;
  string   Manufacturer;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  uint16   SecurityBreach;
  string   SerialNumber;
  string   ServiceDescriptions[];
  uint16   ServicePhilosophy[];
  string   SKU;
  string   Status;
  string   Tag;
  uint16   TypeOfRack;
  string   Version;
  boolean  VisibleAlarm;
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a>Membros

A classe de **\_ rack CIM** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe de **\_ rack CIM** tem esses métodos.



| Método                                                        | Descrição                                                                                                                                      |
|:--------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Iscompatível**](iscompatible-method-in-class-cim-rack.md) | Verifica se o elemento físico referenciado pode ser contido ou inserido no pacote físico. Não implementado pelo WMI.<br/> |



 

### <a name="properties"></a>Propriedades

A classe de **\_ rack CIM** tem essas propriedades.

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

Cadeia de caracteres de forma livre que fornecerá informações se a propriedade **SecurityBreach** indicar que ocorreu uma violação ou algum outro evento relacionado à segurança.

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

Breve descrição textual do objeto.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**CountryDesignation**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ rack CIM**.**TypeOfRack**")
</dt> </dl>

País ou região para o qual o rack foi projetado. As cadeias de caracteres de código de país ou região são definidas por ISO/IEC 3166. O tipo de rack é especificado na propriedade **TypeOfRack** .

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

Descrição textual do objeto.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Altura**
</dt> <dd> <dl> <dt>

Tipo de dados: **real32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("altura"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("EUA")
</dt> </dl>

Altura do pacote físico, usando a unidade de medida "U". Um "U" é uma unidade de medida padrão para a altura de um rack, ou componente montável em rack, e é igual a 1,75 polegadas ou 4,445 centímetros.

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

Data e hora em que o objeto foi instalado. Essa propriedade não precisa de um valor para indicar que o objeto está instalado.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**LockPresent**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se for **true**, o quadro será protegido com um bloqueio.

Essa propriedade é herdada de [**CIM \_ PhysicalFrame.**](cim-physicalframe.md)

</dd> <dt>

**Fabricante**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nome da organização que produziu o elemento físico. Para obter mais informações, consulte **a propriedade Vendor** do produto [**CIM \_**](cim-product.md).

Essa propriedade é herdada de [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**Modelo**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Nome pelo qual o elemento físico é geralmente conhecido.

Essa propriedade é herdada de [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Nome")
</dt> </dl>

Rótulo pelo qual o objeto é conhecido. Quando subclasse, essa propriedade pode ser substituído para ser uma propriedade de chave.

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Dados adicionais, além das informações de marca de ativo, que podem ser usados para identificar um elemento físico. Um exemplo são dados de código de barras associados a um elemento que também tem uma marca de ativo. Essa propriedade é herdada de [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

> [!Note]  
> Se apenas os dados de código de barras estão disponíveis e são exclusivos e podem ser usados como uma chave de elemento, essa propriedade seria nula e os dados de código de barra seriam usados como a chave de classe na propriedade **Tag.**

 

</dd> <dt>

**PartNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Número da parte atribuído pela organização que produziu ou fabricou o elemento físico.

Essa propriedade é herdada de [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**PoweredOn**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se **TRUE**, o elemento físico será ligado.

Essa propriedade é herdada de [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**Removível**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se **TRUE**, esse elemento foi projetado para ser levado para dentro e para fora do contêiner físico no qual normalmente é encontrado, sem prejudicar a função do empacotamento geral. Um pacote é considerado removível mesmo se a energia deve estar "desligada" para executar a remoção. Se a energia puder ser "on" e o pacote removido, o elemento será removível e poderá ser trocado por hot-swapp. Por exemplo, uma bateria extra em um laptop é removível, assim como um pacote de unidade de disco inserido usando conectores SCA; no entanto, o último pode ser trocado por hot-swapp. A exibição de um laptop não é removível, nem uma fonte de alimentação não redundante. A remoção desses componentes afeta a função do empacotamento geral ou é impossível devido à integração rígida do pacote.

Essa propriedade é herdada de [**CIM \_ PhysicalPackage.**](cim-physicalpackage.md)

</dd> <dt>

**Substituível**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se **TRUE**, é possível substituir o elemento por um fisicamente diferente. Por exemplo, alguns sistemas de computador permitem que o chip do processador principal seja atualizado para uma classificação de relógio mais alta. Nesse caso, diz-se que o processador é substituível. Todos os componentes removíveis são inerentemente substituíveis.

Essa propriedade é herdada de [**CIM \_ PhysicalPackage.**](cim-physicalpackage.md)

</dd> <dt>

**SecurityBreach**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Tabela Global do Contêiner Físico DMTF \| \| 002.12"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**BreachDescription**")
</dt> </dl>

Indica se uma violação física do quadro foi tentada, mas malsucedida ou tentada e bem-sucedida. Essa propriedade é herdada de [**CIM \_ PhysicalFrame.**](cim-physicalframe.md)

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outros** (1)


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

**Serialnumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Número alocado pelo fabricante usado para identificar o rack.

Essa propriedade é herdada de [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**Servicedescriptions**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **de cadeia de** caracteres
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**ServicePhyphy**")
</dt> </dl>

Cadeias de caracteres de forma livre que fornecem explicações detalhadas para entradas na **matriz ServicePhyphy.** Observe que cada entrada da matriz está relacionada à entrada em **ServicePhyphy** que está localizada no mesmo índice.

Essa propriedade é herdada de [**CIM \_ PhysicalFrame.**](cim-physicalframe.md)

</dd> <dt>

**ServicePhy**
</dt> <dd> <dl> <dt>

Tipo de dados: **matriz uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**ServiceDescriptions**")
</dt> </dl>

Indica se o quadro é atendido na parte superior, frontal, traseira ou lateral; e se ele tem bandejas deslizantes ou lados removíveis e se o quadro pode ser movido (por exemplo, com rolos).

Essa propriedade é herdada de [**CIM \_ PhysicalFrame.**](cim-physicalframe.md)

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outros** (1)


</dt> <dd></dd> <dt>

<span id="Service_From_Top"></span><span id="service_from_top"></span><span id="SERVICE_FROM_TOP"></span>

**Serviço do início** (2)


</dt> <dd></dd> <dt>

<span id="Service_From_Front"></span><span id="service_from_front"></span><span id="SERVICE_FROM_FRONT"></span>

**Serviço do Front** (3)


</dt> <dd></dd> <dt>

<span id="Service_From_Back"></span><span id="service_from_back"></span><span id="SERVICE_FROM_BACK"></span>

**Serviço de voltar** (4)


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

**Movêvel** (8)


</dt> <dd></dd> </dl>

</dd> <dt>

**SKU**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Número de unidade de manutenção de estoque para o elemento físico.

Essa propriedade é herdada de [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")
</dt> </dl>

Status atual do objeto. Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

Os valores incluem o seguinte:

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Erro** ("Erro")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Degradado** ("Degradado")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** ("Desconhecido")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Pred Fail** ("Pred Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Iniciando** ("Iniciando")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Parando** ("Parando")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Serviço** ("Serviço")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Stressed** ("Stressed")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**NonRecover** ("NonRecover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Sem contato** ("Sem contato")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Perda de vírgula** ("comm perdida")


</dt> <dd></dd> </dl>

</dd> <dt>

**Tag**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**\_ Chave CIM,**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Cadeia de caracteres arbitrária que identifica exclusivamente o elemento físico e serve como a chave do elemento. Essa propriedade pode conter informações, como dados de marca de ativo ou número de série. A chave para [**Cim \_ PhysicalElement**](cim-physicalelement.md) é colocada muito alta na hierarquia de objetos para identificar independentemente o hardware ou a entidade, independentemente do posicionamento físico em gabinetes (ou em) gabinetes, adaptadores e assim por diante. Por exemplo, um componente removível que pode ser trocado por hot-swapp pode ser retirado de seu pacote de contenção (scoping) e ser temporariamente não usada. O objeto ainda continua a existir e pode até mesmo ser inserido em um contêiner de scoping diferente. A chave para um elemento físico é uma cadeia de caracteres arbitrária definida independentemente do posicionamento ou da hierarquia orientada à localização.

Essa propriedade é herdada de [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**TypeOfRack**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Rack**.**CountryDesignation**")
</dt> </dl>

Tipo de rack.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Standard_19_Inch"></span><span id="standard_19_inch"></span><span id="STANDARD_19_INCH"></span>

<span id="Standard_19_Inch"></span><span id="standard_19_inch"></span><span id="STANDARD_19_INCH"></span>**Standard 19 Polegadas** (1)


</dt> <dd>

Padrão de 19 polegadas

</dd> <dt>

<span id="Telco"></span><span id="telco"></span><span id="TELCO"></span>

<span id="Telco"></span><span id="telco"></span><span id="TELCO"></span>**Telco** (2)


</dt> <dd></dd> <dt>

<span id="Equipment_Shelf"></span><span id="equipment_shelf"></span><span id="EQUIPMENT_SHELF"></span>

<span id="Equipment_Shelf"></span><span id="equipment_shelf"></span><span id="EQUIPMENT_SHELF"></span>**Prateleira do equipamento** (3)


</dt> <dd></dd> <dt>

<span id="Non-Standard"></span><span id="non-standard"></span><span id="NON-STANDARD"></span>

<span id="Non-Standard"></span><span id="non-standard"></span><span id="NON-STANDARD"></span>**Não Padrão** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**Versão**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Versão do elemento físico.

Essa propriedade é herdada de [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**VisibleAlarm**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se **TRUE**, o equipamento incluirá um alarme visível.

Essa propriedade é herdada de [**CIM \_ PhysicalFrame.**](cim-physicalframe.md)

</dd> <dt>

**Weight**
</dt> <dd> <dl> <dt>

Tipo de dados: **real32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("quilogramas")
</dt> </dl>

Peso do pacote físico, em quilogramas.

Essa propriedade é herdada de [**CIM \_ PhysicalPackage.**](cim-physicalpackage.md)

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

Essa propriedade é herdada de [**CIM \_ PhysicalPackage.**](cim-physicalpackage.md)

</dd> </dl>

## <a name="remarks"></a>Comentários

A **classe \_ Cim Rack** é derivada de CIM [**\_ PhysicalFrame.**](cim-physicalframe.md)

O WMI não implementa essa classe.

Esta documentação é derivada das descrições da classe CIM publicadas pelo DMTF. A Microsoft pode ter feito alterações para corrigir erros secundários, estar em conformidade com os padrões de documentação do SDK da Microsoft ou fornecer mais informações.

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

[**CIM \_ PhysicalFrame**](cim-physicalframe.md)
</dt> </dl>

 

