---
description: A \_ classe WMI OnBoardDevice do Win32 representa dispositivos de adaptador comuns incorporados à placa-mãe (placa do sistema).
ms.assetid: 6fac38b4-7c04-4f64-997d-40bcbf767959
ms.tgt_platform: multiple
title: Classe Win32_OnBoardDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OnBoardDevice
- Win32_OnBoardDevice.Caption
- Win32_OnBoardDevice.CreationClassName
- Win32_OnBoardDevice.Description
- Win32_OnBoardDevice.DeviceType
- Win32_OnBoardDevice.Enabled
- Win32_OnBoardDevice.HotSwappable
- Win32_OnBoardDevice.InstallDate
- Win32_OnBoardDevice.Manufacturer
- Win32_OnBoardDevice.Model
- Win32_OnBoardDevice.Name
- Win32_OnBoardDevice.OtherIdentifyingInfo
- Win32_OnBoardDevice.PartNumber
- Win32_OnBoardDevice.PoweredOn
- Win32_OnBoardDevice.Removable
- Win32_OnBoardDevice.Replaceable
- Win32_OnBoardDevice.SerialNumber
- Win32_OnBoardDevice.SKU
- Win32_OnBoardDevice.Status
- Win32_OnBoardDevice.Tag
- Win32_OnBoardDevice.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a6ce10494c44f6eecd78e44d4bcf97d5e46da7d6281a5ef614a9e737acae68c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119972586"
---
# <a name="win32_onboarddevice-class"></a>\_Classe Win32 OnBoardDevice

A [classe WMI](../wmisdk/retrieving-a-class.md) **\_ OnBoardDevice do Win32** representa dispositivos de adaptador comuns incorporados à placa-mãe (placa do sistema).

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{AEECF151-D0EA-11d2-ABFC-00805F538618}"), AMENDMENT]
class Win32_OnBoardDevice : CIM_PhysicalComponent
{
  string   Caption;
  string   CreationClassName;
  string   Description;
  uint16   DeviceType;
  boolean  Enabled;
  boolean  HotSwappable;
  datetime InstallDate;
  string   Manufacturer;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  string   SerialNumber;
  string   SKU;
  string   Status;
  string   Tag;
  string   Version;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ OnBoardDevice** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ OnBoardDevice** tem essas propriedades.

<dl> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Breve descrição do objeto.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Nome da primeira classe concreta a ser exibida na cadeia de herança usada na criação de uma instância. Quando usado com as outras propriedades de chave da classe, a propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.

Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) ("Descrição"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Descrição do SMBIOS \| tipo 10 \| ")
</dt> </dl>

Descrição do objeto.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**DeviceType**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| tipo de dispositivo SMBIOS tipo 10 \| ")
</dt> </dl>

Tipo de dispositivo que está sendo representado.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (2)


</dt> <dd></dd> <dt>

<span id="Video"></span><span id="video"></span><span id="VIDEO"></span>

**Vídeo** (3)


</dt> <dd></dd> <dt>

<span id="SCSI_Controller"></span><span id="scsi_controller"></span><span id="SCSI_CONTROLLER"></span>

**Controlador SCSI** (4)


</dt> <dd></dd> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

**Ethernet** (5)


</dt> <dd></dd> <dt>

<span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>

**Token ring** (6)


</dt> <dd></dd> <dt>

<span id="Sound"></span><span id="sound"></span><span id="SOUND"></span>

**Som** (7)


</dt> <dd></dd> </dl>

</dd> <dt>

**Habilitada**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| tipo 10 \| status do dispositivo n")
</dt> </dl>

Se for **true**, o dispositivo integrado estará disponível para uso.

</dd> <dt>

**HotSwappable**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se for **true**, um pacote físico poderá ser trocado de maneira intercambiável (se for possível substituir o elemento por um fisicamente diferente, mas equivalente um, enquanto o pacote recipiente tiver energia aplicada a ele). Por exemplo, um pacote de unidade de disco inserido usando conectores de SCA é removível e pode ser intercambiável. Todos os pacotes que podem ser intercambiáveis são inerentemente removíveis e substituíveis.

Essa propriedade é herdada do [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")
</dt> </dl>

Data e hora em que o objeto foi instalado. Essa propriedade não precisa de um valor para indicar que o objeto está instalado.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Manufacturer**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Nome da organização responsável por produzir o elemento físico.

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

Nome pelo qual o elemento físico é geralmente conhecido.

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

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Dados adicionais, além das informações de marca do ativo, que podem ser usados para identificar um elemento físico. Um exemplo são os dados de código de barras associados a um elemento que também tem uma marca de ativo. Observe que, se apenas os dados de código de barras estiverem disponíveis e for exclusivo ou puderem ser usados como uma chave de elemento, essa propriedade será **NULL** e os dados de código de barras serão usados como a chave de classe na propriedade de marca.

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

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se **TRUE**, um pacote físico será removível (se ele for projetado para ser levado para dentro e para fora do contêiner físico no qual normalmente é encontrado, sem prejudicar a função do empacotamento geral). Um pacote ainda poderá ser removível se a energia tiver que estar "desligada" para executar a remoção. Se a energia puder ser "on" e o pacote for removido, o elemento será removível e poderá ser trocado a quente. Por exemplo, uma bateria extra em um laptop é removível, assim como um pacote de unidade de disco inserido usando conectores SCA. No entanto, o último pode ser trocado por hot-swapp. A exibição de um laptop não é removível, nem uma fonte de alimentação não rereduente. Remover esses componentes afetaria a função do empacotamento geral ou seria impossível devido à integração rígida do pacote.

Essa propriedade é herdada de [**Cim \_ PhysicalComponent.**](cim-physicalcomponent.md)

</dd> <dt>

**Substituível**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se **TRUE**, um pacote físico será substituível (se for possível substituir, FRU ou atualizar, o elemento por um fisicamente diferente). Por exemplo, alguns sistemas de computador permitem que o chip do processador principal seja atualizado para uma classificação de relógio mais alta. Nesse caso, diz-se que o processador é substituível. Outro exemplo é um pacote de fonte de alimentação montado em trilhos deslizantes. Todos os pacotes removíveis são inerentemente substituíveis.

Essa propriedade é herdada de [**Cim \_ PhysicalComponent.**](cim-physicalcomponent.md)

</dd> <dt>

**Serialnumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Número alocado pelo fabricante usado para identificar o elemento físico.

Essa propriedade é herdada de [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**SKU**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)
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

Qualificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")
</dt> </dl>

Status atual do objeto. Vários status operacionais e não operacionais podem ser definidos. Os status operacionais incluem: "OK", "Degradado" e "Pred Fail" (um elemento, como uma unidade de disco rígido habilitada para SMART, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo). Os status nãooperacionais incluem: "Error", "Starting", "Stopping" e "Service". O último, "Serviço", pode ser aplicado durante o espelhamento de um disco, o recarregamento de uma lista de permissões de usuário ou outro trabalho administrativo. Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros estados.

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

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

Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("Tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Identificador exclusivo do dispositivo na placa conectado ao sistema.

Essa propriedade é herdada de [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

Exemplo: "Dispositivo a placa 1"

</dd> <dt>

**Versão**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Versão do elemento físico.

Essa propriedade é herdada de [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> </dl>

## <a name="remarks"></a>Comentários

A **classe Win32 \_ OnBoardDevice** é derivada de [**CIM \_ PhysicalComponent.**](cim-physicalcomponent.md)

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

[**CIM \_ PhysicalComponent**](cim-physicalcomponent.md)
</dt> <dt>

[Classes de hardware do sistema de computador](computer-system-hardware-classes.md)
</dt> </dl>

 

 
