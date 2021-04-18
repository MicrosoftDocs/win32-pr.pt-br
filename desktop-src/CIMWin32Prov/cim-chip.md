---
description: A \_ classe de chip CIM representa o tipo de hardware de circuito integrado, incluindo ASICs, processadores, chips de memória e assim por diante.
ms.assetid: 3c2b0023-5d02-49b9-90f5-d66eb8a103f0
ms.tgt_platform: multiple
title: Classe CIM_Chip
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Chip
- CIM_Chip.Caption
- CIM_Chip.Description
- CIM_Chip.InstallDate
- CIM_Chip.Name
- CIM_Chip.Status
- CIM_Chip.CreationClassName
- CIM_Chip.Manufacturer
- CIM_Chip.Model
- CIM_Chip.OtherIdentifyingInfo
- CIM_Chip.PartNumber
- CIM_Chip.PoweredOn
- CIM_Chip.SerialNumber
- CIM_Chip.SKU
- CIM_Chip.Tag
- CIM_Chip.Version
- CIM_Chip.HotSwappable
- CIM_Chip.Removable
- CIM_Chip.Replaceable
- CIM_Chip.FormFactor
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 953ae371edca42409246307b21aad69a02cf4a66
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457082"
---
# <a name="cim_chip-class"></a>\_Classe de chip CIM

A classe de **\_ chip CIM** representa o tipo de hardware de circuito integrado, incluindo ASICs, processadores, chips de memória e assim por diante.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[abstract, UUID("{FAF76B7A-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Chip : CIM_PhysicalComponent
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
  boolean  HotSwappable;
  boolean  Removable;
  boolean  Replaceable;
  uint16   FormFactor;
};
```

## <a name="members"></a>Membros

A classe de **\_ chip CIM** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe de **\_ chip CIM** tem essas propriedades.

<dl> <dt>

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

**FormFactor**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Fator forma de implementação para o chip. Os valores a seguir podem ser especificados.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outro** (1)


</dt> <dd></dd> <dt>

<span id="SIP"></span><span id="sip"></span>

**SIP** (2)


</dt> <dd></dd> <dt>

<span id="DIP"></span><span id="dip"></span>

**DIP** (3)


</dt> <dd></dd> <dt>

<span id="ZIP"></span><span id="zip"></span>

**Zip** (4)


</dt> <dd></dd> <dt>

<span id="SOJ"></span><span id="soj"></span>

**SOJ** (5)


</dt> <dd></dd> <dt>

<span id="Proprietary"></span><span id="proprietary"></span><span id="PROPRIETARY"></span>

**Proprietário** (6)


</dt> <dd></dd> <dt>

<span id="SIMM"></span><span id="simm"></span>

**SIMM** (7)


</dt> <dd></dd> <dt>

<span id="DIMM"></span><span id="dimm"></span>

**DIMM** (8)


</dt> <dd></dd> <dt>

<span id="TSOP"></span><span id="tsop"></span>

**TSOP** (9)


</dt> <dd></dd> <dt>

<span id="PGA"></span><span id="pga"></span>

**PGA** (10)


</dt> <dd></dd> <dt>

<span id="RIMM"></span><span id="rimm"></span>

**RIMM** (11)


</dt> <dd></dd> <dt>

<span id="SODIMM"></span><span id="sodimm"></span>

**SODIMM** (12)


</dt> <dd></dd> <dt>

<span id="SRIMM"></span><span id="srimm"></span>

**SRIMM** (13)


</dt> <dd></dd> <dt>

<span id="SMD"></span><span id="smd"></span>

**SMD** (14)


</dt> <dd></dd> <dt>

<span id="SSMP"></span><span id="ssmp"></span>

**SSMP** (15)


</dt> <dd></dd> <dt>

<span id="QFP"></span><span id="qfp"></span>

**QFP** (16)


</dt> <dd></dd> <dt>

<span id="TQFP"></span><span id="tqfp"></span>

**TQFP** (17)


</dt> <dd></dd> <dt>

<span id="SOIC"></span><span id="soic"></span>

**SOIC** (18)


</dt> <dd></dd> <dt>

<span id="LCC"></span><span id="lcc"></span>

**LCC** (19)


</dt> <dd></dd> <dt>

<span id="PLCC"></span><span id="plcc"></span>

**PLCC** (20)


</dt> <dd></dd> <dt>

<span id="BGA"></span><span id="bga"></span>

**BGA** (21)


</dt> <dd></dd> <dt>

<span id="FPBGA"></span><span id="fpbga"></span>

**FPBGA** (22)


</dt> <dd></dd> <dt>

<span id="LGA"></span><span id="lga"></span>

**LGA** (23)


</dt> <dd></dd> <dt>

<span id="FB-DIMM"></span><span id="fb-dimm"></span>

**FB-DIMM** (24)


</dt> <dd></dd> </dl>

</dd> <dt>

**HotSwappable**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se **for true**, o pacote poderá ser intercambiável. Um pacote físico pode ser intercambiável se o elemento puder ser substituído por um fisicamente diferente (mas equivalente) um enquanto o pacote que o contém está ativado. Por exemplo, um componente de ventilador pode ser projetado para ser intercambiável. Todos os componentes que podem ser intercambiáveis são inerentemente removíveis e substituíveis.

Essa propriedade é herdada do [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md).

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

Se for **true**, esse elemento será projetado para ser levado para dentro e para fora do contêiner físico no qual ele normalmente é encontrado, sem comprometer a função do empacotamento geral. Um pacote é considerado removível, mesmo que a energia precise ser desligada para executar a remoção. Se a energia puder ser ativada e o pacote for removido, o elemento será removível e poderá ser intercambiável. Por exemplo, um chip de processador atualizável é removível.

Essa propriedade é herdada do [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md).

</dd> <dt>

**Peças**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se for **true**, é possível substituir o elemento por um fisicamente diferente. Por exemplo, alguns sistemas de computador permitem que o chip do processador principal seja atualizado para uma classificação de clock mais alta. Nesse caso, diz-se que o processador é substituível. Todos os componentes removíveis são inerentemente substituíveis.

Essa propriedade é herdada do [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md).

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

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe de **\_ chip CIM** é derivada do [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md).

O WMI não implementa essa classe. Para obter mais informações sobre classes derivadas **do \_ chip CIM**, consulte [classes Win32](win32-provider.md).

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

[**\_PHYSICALCOMPONENT CIM**](cim-physicalcomponent.md)
</dt> </dl>

 

