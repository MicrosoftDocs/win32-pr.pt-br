---
description: A \_ classe CIM SerialInterface representa um \_ relacionamento CIM ControlledBy que indica quais dispositivos são acessados por meio do controlador serial e as características do acesso.
ms.assetid: bebc304a-c2b7-41c7-b24a-8f450ee3c4bb
ms.tgt_platform: multiple
title: Classe CIM_SerialInterface
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SerialInterface
- CIM_SerialInterface.NegotiatedDataWidth
- CIM_SerialInterface.NegotiatedSpeed
- CIM_SerialInterface.AccessState
- CIM_SerialInterface.NumberOfHardResets
- CIM_SerialInterface.NumberOfSoftResets
- CIM_SerialInterface.Dependent
- CIM_SerialInterface.Antecedent
- CIM_SerialInterface.FlowControlInfo
- CIM_SerialInterface.NumberOfStopBits
- CIM_SerialInterface.ParityInfo
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1df787ff64798f412035a72e6db6d7b01b4b9b0a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826342"
---
# <a name="cim_serialinterface-class"></a>\_Classe CIM SerialInterface

A classe **CIM \_ SerialInterface** representa um relacionamento [**CIM \_ ControlledBy**](cim-controlledby.md) que indica quais dispositivos são acessados por meio do controlador serial e as características do acesso.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, UUID("{8B309BDA-E3D4-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_SerialInterface : CIM_ControlledBy
{
  uint32                   NegotiatedDataWidth;
  uint64                   NegotiatedSpeed;
  uint16                   AccessState;
  uint32                   NumberOfHardResets;
  uint32                   NumberOfSoftResets;
  CIM_LogicalDevice    REF Dependent;
  CIM_SerialController REF Antecedent;
  uint16                   FlowControlInfo;
  uint16                   NumberOfStopBits;
  uint16                   ParityInfo;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ SerialInterface** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ SerialInterface** tem essas propriedades.

<dl> <dt>

**Accessstate**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se o controlador está ativando ou acessando ativamente o dispositivo. Essas informações são necessárias quando um dispositivo lógico pode ser acessado ou acessado por meio de vários controladores.

Essa propriedade é herdada do [**CIM \_ ControlledBy**](cim-controlledby.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

**Ativo** (1)


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

**Inativo** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ SerialController**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Um [**\_ SerialController CIM**](cim-serialcontroller.md) que descreve o controlador serial.

</dd> <dt>

**Depende**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ LogicalDevice CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")
</dt> </dl>

Um [**\_ LogicalDevice CIM**](cim-logicaldevice.md) que descreve o dispositivo lógico.

</dd> <dt>

**FlowControlInfo**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica o controle de fluxo para dados transmitidos.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span id="None"></span><span id="none"></span><span id="NONE"></span>**Nenhum** (2)


</dt> <dd></dd> <dt>

<span id="XonXoff"></span><span id="xonxoff"></span><span id="XONXOFF"></span>

<span id="XonXoff"></span><span id="xonxoff"></span><span id="XONXOFF"></span>**XOnXOff** (3)


</dt> <dd></dd> <dt>

<span id="RTS_CTS"></span><span id="rts_cts"></span>

<span id="RTS_CTS"></span><span id="rts_cts"></span>**RTS/CTS** (4)


</dt> <dd></dd> <dt>

<span id="Both_XonXoff_and_RTS_CTS"></span><span id="both_xonxoff_and_rts_cts"></span><span id="BOTH_XONXOFF_AND_RTS_CTS"></span>

<span id="Both_XonXoff_and_RTS_CTS"></span><span id="both_xonxoff_and_rts_cts"></span><span id="BOTH_XONXOFF_AND_RTS_CTS"></span>**XOnXOff e RTS/CTS** (5)


</dt> <dd>

XonXoff e RTS/CTS

</dd> </dl>

</dd> <dt>

**NegotiatedDataWidth**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")
</dt> </dl>

Quando várias larguras de dados de barramento ou conexão são possíveis, essa propriedade define a que está em uso entre os dispositivos. A largura dos dados é especificada em bits. Se a largura dos dados não for negociada ou se essas informações não estiverem disponíveis ou importantes para o gerenciamento de dispositivos, a propriedade deverá ser definida como 0 (zero).

Essa propriedade é herdada do [**CIM \_ DeviceConnection**](cim-deviceconnection.md).

</dd> <dt>

**NegotiatedSpeed**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits por segundo")
</dt> </dl>

Quando várias velocidades de barramento ou conexão são possíveis, essa propriedade define a que está sendo usada entre os dispositivos. A velocidade é especificada em bits por segundo. Se as velocidades de conexão ou de barramento não forem negociadas ou se essas informações não estiverem disponíveis ou importantes para o gerenciamento de dispositivos, a propriedade deverá ser definida como 0 (zero).

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

Essa propriedade é herdada do [**CIM \_ DeviceConnection**](cim-deviceconnection.md).

</dd> <dt>

**NumberOfHardResets**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de redefinições de hardware emitidas pelo controlador. Uma reinicialização forçada retorna o dispositivo para seu estado de inicialização ou inicialização. Todos os dados e informações de estado do dispositivo interno são perdidos.

Essa propriedade é herdada do [**CIM \_ ControlledBy**](cim-controlledby.md).

</dd> <dt>

**NumberOfSoftResets**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de redefinições reversível emitidas pelo controlador. Uma redefinição reversível não limpa completamente o estado e os dados atuais do dispositivo. A semântica exata depende do dispositivo e dos protocolos e mecanismos usados para se comunicar com ele.

Essa propriedade é herdada do [**CIM \_ ControlledBy**](cim-controlledby.md).

</dd> <dt>

**NumberOfStopBits**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")
</dt> </dl>

Número de bits de parada a serem transmitidos.

</dd> <dt>

**ParityInfo**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Informações sobre a configuração de paridade para dados transmitidos.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Nenhum** (1)


</dt> <dd></dd> <dt>

<span id="Even"></span><span id="even"></span><span id="EVEN"></span>

**Par** (2)


</dt> <dd></dd> <dt>

<span id="Odd"></span><span id="odd"></span><span id="ODD"></span>

**Odd** (3)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **CIM \_ SerialInterface** é derivada de [**\_ ControlledBy CIM**](cim-controlledby.md).

O WMI não implementa essa classe.

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

[**\_CONTROLLEDBY CIM**](cim-controlledby.md)
</dt> </dl>

 

