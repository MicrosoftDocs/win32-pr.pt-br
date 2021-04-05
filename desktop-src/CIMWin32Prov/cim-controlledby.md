---
description: O \_ relacionamento CIM ControlledBy indica quais dispositivos são incluídos no comando ou acessados por meio do dispositivo lógico do controlador.
ms.assetid: 6aa4e088-32a0-4c88-bb82-341b6ab53b4c
ms.tgt_platform: multiple
title: Classe CIM_ControlledBy (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ControlledBy
- CIM_ControlledBy.NegotiatedDataWidth
- CIM_ControlledBy.NegotiatedSpeed
- CIM_ControlledBy.Dependent
- CIM_ControlledBy.Antecedent
- CIM_ControlledBy.AccessState
- CIM_ControlledBy.NumberOfHardResets
- CIM_ControlledBy.NumberOfSoftResets
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 315eea9fa207a92c3aa1add6fe021127dc3949d5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826346"
---
# <a name="cim_controlledby-class-cimwin32-wmi-providers"></a>Classe CIM_ControlledBy (provedores WMI CIMWin32)

O relacionamento **CIM \_ ControlledBy** indica quais dispositivos são incluídos no comando ou acessados por meio do dispositivo lógico do controlador.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, UUID("{8502C53D-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ControlledBy : CIM_DeviceConnection
{
  uint32                NegotiatedDataWidth;
  uint64                NegotiatedSpeed;
  CIM_LogicalDevice REF Dependent;
  CIM_Controller    REF Antecedent;
  uint16                AccessState;
  uint32                NumberOfHardResets;
  uint32                NumberOfSoftResets;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ ControlledBy** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ ControlledBy** tem essas propriedades.

<dl> <dt>

**Accessstate**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se o controlador está ativando ou acessando ativamente o dispositivo. Essas informações são necessárias quando um dispositivo lógico pode ser acessado ou acessado por meio de vários controladores.

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

Tipo de dados **: \_ controlador CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Um [**\_ controlador CIM**](cim-controller.md) que representa o controlador.

</dd> <dt>

**Depende**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ LogicalDevice CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")
</dt> </dl>

Um [**\_ LogicalDevice CIM**](cim-logicaldevice.md) que representa o dispositivo controlado.

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

</dd> <dt>

**NumberOfSoftResets**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de redefinições reversível emitidas pelo controlador. Uma redefinição reversível não limpa completamente o estado e os dados atuais do dispositivo. A semântica exata depende do dispositivo e dos protocolos e mecanismos usados para se comunicar com ele.

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **CIM \_ ControlledBy** é derivada de [**\_ DeviceConnection CIM**](cim-deviceconnection.md).

O WMI não implementa essa classe. Para obter mais informações sobre classes derivadas de **CIM \_ ControlledBy**, consulte [classes Win32](win32-provider.md).

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

[**\_DEVICECONNECTION CIM**](cim-deviceconnection.md)
</dt> </dl>

 

