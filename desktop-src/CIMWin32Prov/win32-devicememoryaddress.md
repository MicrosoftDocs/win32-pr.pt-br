---
description: A classe WMI Win32 DeviceMemoryAddress representa um endereço de memória do dispositivo em um sistema de computador que \_ executa Windows.
ms.assetid: f0a70724-5ced-47fe-b17e-e153e65b80df
ms.tgt_platform: multiple
title: Win32_DeviceMemoryAddress classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 31d49baca4e11ce1908ba1d057819f216153f49353415c8b5465e70e3a607e00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119020244"
---
# <a name="win32_devicememoryaddress-class"></a>Classe Win32 \_ DeviceMemoryAddress

A classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ Win32 DeviceMemoryAddress** representa um endereço de memória do dispositivo em um sistema de computador que executa Windows.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4CF-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DeviceMemoryAddress : Win32_SystemMemoryResource
{
  string   Caption;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  uint64   EndingAddress;
  datetime InstallDate;
  string   MemoryType;
  string   Name;
  uint64   StartingAddress;
  string   Status;
};
```

## <a name="members"></a>Membros

A **classe Win32 \_ DeviceMemoryAddress** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe Win32 \_ DeviceMemoryAddress** tem essas propriedades.

<dl> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Legenda")
</dt> </dl>

Descrição curta do objeto uma cadeia de caracteres de uma linha.

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Chave CIM \_**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Nome da primeira classe concreta que aparece na cadeia de herança usada na criação de uma instância. Quando usada com as outras propriedades de chave da classe , a propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.

Essa propriedade é herdada de [**CIM \_ MemoryMappedIO.**](cim-memorymappedio.md)

</dd> <dt>

**CSCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nome da classe de criação do sistema de computador de definição de tela.

Essa propriedade é herdada de [**CIM \_ MemoryMappedIO.**](cim-memorymappedio.md)

</dd> <dt>

**CSName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Nome**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Chave \_ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Nome do sistema de computador de definição de tela.

Essa propriedade é herdada de [**CIM \_ MemoryMappedIO.**](cim-memorymappedio.md)

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")
</dt> </dl>

Descrição do objeto.

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**EndingAddress**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. E/S mapeada de memória DMTF \| \| 001.2")
</dt> </dl>

Endereço final da E/S mapeada em memória.

Essa propriedade é herdada de [**CIM \_ MemoryMappedIO.**](cim-memorymappedio.md)

Para obter mais informações sobre como **usar valores uint64** em scripts, consulte [Scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de dados: **datetime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Data de instalação")
</dt> </dl>

Data e hora em que o objeto foi instalado. Essa propriedade não requer um valor para indicar que o objeto está instalado.

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**MemoryType**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| SystemStructures \| CM PARTIAL RESOURCE \_ \_ \_ DESCRIPTOR \| Flags")
</dt> </dl>

Características do recurso de memória no sistema de computador executando Windows. Os valores são os seguintes.

<dt>

<span id="ReadWrite"></span><span id="readwrite"></span><span id="READWRITE"></span>

<span id="ReadWrite"></span><span id="readwrite"></span><span id="READWRITE"></span>**ReadWrite** ("ReadWrite")


</dt> <dd>

A memória pode ser lida e escrita.

</dd> <dt>

<span id="ReadOnly"></span><span id="readonly"></span><span id="READONLY"></span>

<span id="ReadOnly"></span><span id="readonly"></span><span id="READONLY"></span>**ReadOnly** ("ReadOnly")


</dt> <dd>

A memória é somente leitura.

</dd> <dt>

<span id="WriteOnly"></span><span id="writeonly"></span><span id="WRITEONLY"></span>

<span id="WriteOnly"></span><span id="writeonly"></span><span id="WRITEONLY"></span>**WriteOnly** ("WriteOnly")


</dt> <dd>

A memória só pode ser escrita.

</dd> <dt>

<span id="Prefetchable"></span><span id="prefetchable"></span><span id="PREFETCHABLE"></span>

<span id="Prefetchable"></span><span id="prefetchable"></span><span id="PREFETCHABLE"></span>**Prefetchable** ("Prefetchable")


</dt> <dd>

Um bloco de memória é copiado da memória principal para um buffer pequeno gerenciado pelo chipset de memória. As operações de leitura repetidas da mesma parte da memória são mais rápidas com memória pré-buscada.

</dd> <dt>

<span id="CombinedWrite"></span><span id="combinedwrite"></span><span id="COMBINEDWRITE"></span>

<span id="CombinedWrite"></span><span id="combinedwrite"></span><span id="COMBINEDWRITE"></span>**CombinedWrite** ("CombinedWrite")


</dt> <dd>

TBD

</dd> <dt>

<span id="Type24"></span><span id="type24"></span><span id="TYPE24"></span>

<span id="Type24"></span><span id="type24"></span><span id="TYPE24"></span>**Type24** ("Type24")


</dt> <dd>

TBD

</dd> <dt>

<span id="Cacheable"></span><span id="cacheable"></span><span id="CACHEABLE"></span>

<span id="Cacheable"></span><span id="cacheable"></span><span id="CACHEABLE"></span>**Armazenando em** cache ("em cache")


</dt> <dd>

TBD

</dd> <dt>

<span id="WindowDecode"></span><span id="windowdecode"></span><span id="WINDOWDECODE"></span>

<span id="WindowDecode"></span><span id="windowdecode"></span><span id="WINDOWDECODE"></span>**WindowDecode** ("WindowDecode")


</dt> <dd>

TBD

</dd> <dt>

<span id="Bar"></span><span id="bar"></span><span id="BAR"></span>

<span id="Bar"></span><span id="bar"></span><span id="BAR"></span>**Barra** ("Barra")


</dt> <dd>

TBD

</dd> </dl>

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Nome")
</dt> </dl>

Rótulo pelo qual o objeto é conhecido. Quando subclasse, a propriedade pode ser substituído para ser uma propriedade de chave.

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**StartingAddress**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Substitua**](/windows/desktop/WmiSdk/standard-qualifiers) ("StartingAddress"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. E/S mapeada de memória DMTF \| \| 001.1")
</dt> </dl>

Endereço inicial da E/S mapeada em memória. A propriedade do identificador de recurso de hardware deve ser definida com esse valor para construir a chave de recurso de E/S mapeada.

Essa propriedade é herdada de [**CIM \_ MemoryMappedIO.**](cim-memorymappedio.md)

Para obter mais informações sobre como **usar valores uint64** em scripts, consulte [Scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")
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

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **Win32 \_ DeviceMemoryAddress** é derivada de [**Win32 \_ SystemMemoryResource**](win32-systemmemoryresource.md).

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

[**\_SystemMemoryResource Win32**](win32-systemmemoryresource.md)
</dt> <dt>

[Classes de hardware do sistema de computador](computer-system-hardware-classes.md)
</dt> </dl>

 

