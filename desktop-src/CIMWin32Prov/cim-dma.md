---
description: A classe CIM DMA representa o DMA (acesso direto à memória) da \_ arquitetura do computador.
ms.assetid: 101fa9f3-a403-487d-8482-b1e8e9f957d6
ms.tgt_platform: multiple
title: CIM_DMA classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DMA
- CIM_DMA.AddressSize
- CIM_DMA.Availability
- CIM_DMA.BurstMode
- CIM_DMA.ByteMode
- CIM_DMA.Caption
- CIM_DMA.ChannelTiming
- CIM_DMA.CreationClassName
- CIM_DMA.CSCreationClassName
- CIM_DMA.CSName
- CIM_DMA.Description
- CIM_DMA.DMAChannel
- CIM_DMA.InstallDate
- CIM_DMA.MaxTransferSize
- CIM_DMA.Name
- CIM_DMA.Status
- CIM_DMA.TransferWidths
- CIM_DMA.TypeCTiming
- CIM_DMA.WordMode
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 82519db788c063909b48aec26f77c131865e4752f69b63feb1daf5d2e9745092
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119924106"
---
# <a name="cim_dma-class"></a>Classe CIM \_ DMA

A **classe CIM \_ DMA** representa o DMA (acesso direto à memória) da arquitetura do computador.

> [!IMPORTANT]
> As classes CIM (Distributed Management Task Force) do DMTF (Distributed Management Task Force) modelo CIM são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos esquemas de versão [do CIM 2.x.](https://dmtf.org/standards/cim/schemas)

 

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, UUID("{8502C523-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_DMA : CIM_SystemResource
{
  uint16   AddressSize;
  uint16   Availability;
  boolean  BurstMode;
  uint16   ByteMode;
  string   Caption;
  uint16   ChannelTiming;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  uint32   DMAChannel;
  datetime InstallDate;
  uint32   MaxTransferSize;
  string   Name;
  string   Status;
  uint16   TransferWidths[];
  uint16   TypeCTiming;
  uint16   WordMode;
};
```

## <a name="members"></a>Membros

A **classe CIM \_ DMA** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe CIM \_ DMA** tem essas propriedades.

<dl> <dt>

**AddressSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| System Resource DMA Info \| 001.3"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")
</dt> </dl>

Tamanho do endereço do canal DMA, em bits. Os valores permitidos são 8, 16, 32 e 64. Se for desconhecido, insira 0.

<dt>



  acima (0)


</dt> <dd></dd> <dt>



 (8)


</dt> <dd></dd> <dt>



 (16)


</dt> <dd></dd> <dt>



 (32)


</dt> <dd></dd> <dt>



 (64)


</dt> <dd></dd> </dl>

</dd> <dt>

**Disponibilidade**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| DMA \| 001.2")
</dt> </dl>

Disponibilidade do DMA.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outros** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)


</dt> <dd>

Desconhecido.

</dd> <dt>

<span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>

<span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Disponível** (3)


</dt> <dd>

Disponível.

</dd> <dt>

<span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>

<span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**Em Uso/Não Disponível** (4)


</dt> <dd>

Em uso (não disponível).

</dd> <dt>

<span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>

<span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**Em Uso e Disponível/Compartilhável** (5)


</dt> <dd>

Em uso, mas disponível (compartilhável).

</dd> </dl>

</dd> <dt>

**BurstMode**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| DMA \| 001.3")
</dt> </dl>

Se **TRUE**, o canal DMA dá suporte ao modo de estouro.

</dd> <dt>

**ByteMode**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| System Resource DMA Info \| 001.7")
</dt> </dl>

Indica se o DMA pode ser executado no modo contagem por byte.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outros** (1)


</dt> <dd>

Outros.

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)


</dt> <dd>

Desconhecido.

</dd> <dt>

<span id="Not_execute_in__count_by_byte__mode"></span><span id="not_execute_in__count_by_byte__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>

<span id="Not_execute_in__count_by_byte__mode"></span><span id="not_execute_in__count_by_byte__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**Não executar no modo 'contagem por byte'** (3)


</dt> <dd>

Não é possível executar no modo contagem por byte.

</dd> <dt>

<span id="Execute_in__count_by_byte__mode"></span><span id="execute_in__count_by_byte__mode"></span><span id="EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>

<span id="Execute_in__count_by_byte__mode"></span><span id="execute_in__count_by_byte__mode"></span><span id="EXECUTE_IN__COUNT_BY_BYTE__MODE"></span>**Executar no modo 'contagem por byte'** (4)


</dt> <dd>

Capaz de executar no modo contagem por byte.

</dd> </dl>

</dd> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Legenda")
</dt> </dl>

Descrição textual curta do objeto.

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**ChannelTiming**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| System Resource DMA Info \| 001.9")
</dt> </dl>

Tempo do canal DMA.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outros** (1)


</dt> <dd>

Outros.

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)


</dt> <dd>

Desconhecido.

</dd> <dt>

<span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>

<span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>**Compatível com ISA** (3)


</dt> <dd>

Compatível com ISA.

</dd> <dt>

<span id="Type_A"></span><span id="type_a"></span><span id="TYPE_A"></span>

<span id="Type_A"></span><span id="type_a"></span><span id="TYPE_A"></span>**Tipo A** (4)


</dt> <dd>

Digite A.

</dd> <dt>

<span id="Type_B"></span><span id="type_b"></span><span id="TYPE_B"></span>

<span id="Type_B"></span><span id="type_b"></span><span id="TYPE_B"></span>**Tipo B** (5)


</dt> <dd>

Tipo B.

</dd> <dt>

<span id="Type_F"></span><span id="type_f"></span><span id="TYPE_F"></span>

<span id="Type_F"></span><span id="type_f"></span><span id="TYPE_F"></span>**Tipo F** (6)


</dt> <dd>

Digite F.

</dd> </dl>

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Chave CIM \_**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Nome da classe ou subclasse usada na criação de uma instância. Quando usada com outras propriedades de chave da classe , essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.

</dd> <dt>

**CSCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Chave CIM \_**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Definindo o scoping do nome da classe de criação do sistema de computadores.

</dd> <dt>

**CSName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Name**"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Definindo o scoping do nome do sistema de computador.

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

**DMAChannel**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| DMA \| 1,1 ")
</dt> </dl>

Número do canal DMA. Esse número é parte do valor de chave do objeto.

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

**MaxTransferSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informações de DMA do recurso do sistema DMTF \| 1,4 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")
</dt> </dl>

Número máximo de bytes que podem ser transferidos por este canal DMA. Se for desconhecido, insira 0 (zero).

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

**Status**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")
</dt> </dl>

Indica o status atual do objeto.

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

**TransferWidths**
</dt> <dd> <dl> <dt>

Tipo de dados: a matriz **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informações de DMA do recurso do sistema DMTF \| 1,2 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")
</dt> </dl>

Matriz que indica todas as larguras de transferência, em bits, para as quais este canal DMA dá suporte. Os valores permitidos são 8, 16, 32, 64 e 128 bits. Se for desconhecido, insira 0 (zero).

<dt>



  acima (0)


</dt> <dd></dd> <dt>



 (8)


</dt> <dd></dd> <dt>



 (16)


</dt> <dd></dd> <dt>



 (32)


</dt> <dd></dd> <dt>



 (64)


</dt> <dd></dd> <dt>



 (128)


</dt> <dd></dd> </dl>

</dd> <dt>

**TypeCTiming**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informações de DMA do recurso do sistema DMTF \| 1,10 ")
</dt> </dl>

Indica se há suporte para o tempo de tipo C (intermitência).

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

<span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>

<span id="ISA_Compatible"></span><span id="isa_compatible"></span><span id="ISA_COMPATIBLE"></span>**Compatível com ISA** (3)


</dt> <dd>

Compatível com ISA.

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (4)


</dt> <dd>

Sem suporte.

</dd> <dt>

<span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span>

<span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span>**Com suporte** (5)


</dt> <dd>

Com suporte.

</dd> </dl>

</dd> <dt>

**WordMode**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informações de DMA do recurso do sistema DMTF \| 1,8 ")
</dt> </dl>

Indica se o DMA pode ser executado no modo de contagem por palavra.

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

<span id="Not_execute_in__count_by_word__mode"></span><span id="not_execute_in__count_by_word__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_WORD__MODE"></span>

<span id="Not_execute_in__count_by_word__mode"></span><span id="not_execute_in__count_by_word__mode"></span><span id="NOT_EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**Não executar no modo ' contagem por palavra '** (3)


</dt> <dd>

Não é possível executar no modo de contagem por palavra.

</dd> <dt>

<span id="Execute_in__count_by_word__mode"></span><span id="execute_in__count_by_word__mode"></span><span id="EXECUTE_IN__COUNT_BY_WORD__MODE"></span>

<span id="Execute_in__count_by_word__mode"></span><span id="execute_in__count_by_word__mode"></span><span id="EXECUTE_IN__COUNT_BY_WORD__MODE"></span>**Executar no modo ' contagem por palavra '** (4)


</dt> <dd>

Capaz de executar em modo de contagem por palavra.

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **CIM \_ DMA** é derivada do [**CIM \_ SystemResource**](cim-systemresource.md).

O WMI não implementa essa classe. Para classes derivadas do **\_ DMA do CIM**, consulte [classes Win32](win32-provider.md).

Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF. A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.

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

[**CIM \_ SystemResource**](cim-systemresource.md)
</dt> </dl>

 

