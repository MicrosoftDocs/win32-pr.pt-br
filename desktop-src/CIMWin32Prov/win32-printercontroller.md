---
description: A \_ classe WMI de associação PrinterController do Win32 relaciona uma impressora e o dispositivo local ao qual a impressora está conectada. Observe que essa classe só retorna instâncias para impressoras locais.
ms.assetid: fb483b28-11f1-4153-893e-492f71763712
ms.tgt_platform: multiple
title: Classe Win32_PrinterController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterController
- Win32_PrinterController.AccessState
- Win32_PrinterController.Antecedent
- Win32_PrinterController.Dependent
- Win32_PrinterController.NegotiatedDataWidth
- Win32_PrinterController.NegotiatedSpeed
- Win32_PrinterController.NumberOfHardResets
- Win32_PrinterController.NumberOfSoftResets
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1ee38b827aed2dfffe1e7ef4f5049b16eee50791
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826419"
---
# <a name="win32_printercontroller-class"></a>\_Classe Win32 PrinterController

A [classe WMI](../wmisdk/retrieving-a-class.md) de associação **\_ PrinterController do Win32** relaciona uma impressora e o dispositivo local ao qual a impressora está conectada. Observe que essa classe só retorna instâncias para impressoras locais.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class Win32_PrinterController : CIM_ControlledBy
{
  uint16             AccessState;
  CIM_Controller REF Antecedent;
  Win32_Printer  REF Dependent;
  uint32             NegotiatedDataWidth;
  uint64             NegotiatedSpeed;
  uint32             NumberOfHardResets;
  uint32             NumberOfSoftResets;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ PrinterController** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ PrinterController** tem essas propriedades.

<dl> <dt>

**Accessstate**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Estado do acesso do controlador ao dispositivo. Essas informações são necessárias quando um dispositivo lógico pode ser acessado ou acessado por meio de vários controladores.

Essa propriedade é herdada do [**CIM \_ ControlledBy**](cim-controlledby.md).

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Unknown

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Ativo

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Inativo

</dd> </dl>

</dd> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ controlador CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](../wmisdk/standard-qualifiers.md)
</dt> </dl>

Referência à instância [**do \_ controlador CIM**](cim-controller.md) que representa o dispositivo local associado a esta impressora.

Essa propriedade é herdada [**da \_ dependência CIM**](cim-dependency.md).

</dd> <dt>

**Depende**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ impressora Win32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](../wmisdk/standard-qualifiers.md)
</dt> </dl>

Referência à instância [**de \_ impressora do Win32**](win32-printer.md) que representa a impressora associada ao dispositivo local.

Essa propriedade é herdada [**da \_ dependência CIM**](cim-dependency.md).

</dd> <dt>

**NegotiatedDataWidth**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Largura de dados em uso entre os dispositivos (quando várias larguras de dados de conexão ou barramento são possíveis). A largura dos dados é especificada em bits. Se a largura dos dados não for negociada ou se essas informações não estiverem disponíveis ou importantes para o gerenciamento de dispositivos, a propriedade deverá ser definida como 0 (zero).

Essa propriedade é herdada do [**CIM \_ DeviceConnection**](cim-deviceconnection.md).

</dd> <dt>

**NegotiatedSpeed**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Velocidade em uso entre os dispositivos (quando várias velocidades de barramento ou conexão são possíveis). A velocidade é especificada em bits por segundo. Se as velocidades de conexão ou de barramento não forem negociadas ou se essas informações não estiverem disponíveis ou importantes para o gerenciamento de dispositivos, a propriedade deverá ser definida como 0 (zero).

Essa propriedade é herdada do [**CIM \_ DeviceConnection**](cim-deviceconnection.md).

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**NumberOfHardResets**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de redefinições de hardware emitidas pelo controlador.

Essa propriedade é herdada do [**CIM \_ ControlledBy**](cim-controlledby.md).

</dd> <dt>

**NumberOfSoftResets**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de redefinições reversível emitidas pelo controlador.

Essa propriedade é herdada do [**CIM \_ ControlledBy**](cim-controlledby.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **Win32 \_ PrinterController** é derivada de [**CIM \_ ControlledBy**](cim-controlledby.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                      |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>\_Impressora. mof do Win32</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_CONTROLLEDBY CIM**](cim-controlledby.md)
</dt> <dt>

[Classes de hardware do sistema de computador](computer-system-hardware-classes.md)
</dt> </dl>

 

 
