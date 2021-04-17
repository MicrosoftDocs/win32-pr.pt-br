---
description: Uma relação que indica que dois ou mais dispositivos estão conectados juntos.
ms.assetid: 84282740-f60f-46fa-95b7-b52a7e6efcc4
title: Classe CIM_DeviceConnection (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceConnection
- CIM_DeviceConnection.Antecedent
- CIM_DeviceConnection.Dependent
- CIM_DeviceConnection.NegotiatedSpeed
- CIM_DeviceConnection.NegotiatedDataWidth
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f58c66199abeb5b3586f52e91828b8b194bdbbd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770229"
---
# <a name="cim_deviceconnection-class-hyper-v-management"></a>Classe CIM_DeviceConnection (gerenciamento do Hyper-V)

Uma relação que indica que dois ou mais dispositivos estão conectados juntos.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::DeviceElements"), AMENDMENT]
class CIM_DeviceConnection : CIM_Dependency
{
  CIM_LogicalDevice REF Antecedent;
  CIM_LogicalDevice REF Dependent;
  uint64                NegotiatedSpeed;
  uint32                NegotiatedDataWidth;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ DeviceConnection** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ DeviceConnection** tem essas propriedades.

<dl> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ LogicalDevice CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Um dispositivo.

</dd> <dt>

**Depende**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ LogicalDevice CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")
</dt> </dl>

Um segundo dispositivo que está conectado a outro dispositivo.

</dd> <dt>

**NegotiatedDataWidth**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Associação de porta do barramento DMTF \| 1,3 "), **PUnit** (" bit ")
</dt> </dl>

Quando várias larguras de dados de conexão e barramento são possíveis, a propriedade NegotiatedDataWidth define aquela que está em uso entre os dispositivos. A largura dos dados é especificada em bits. Se a largura dos dados não for negociada ou se essas informações não estiverem disponíveis ou não forem importantes para o gerenciamento de dispositivos, a propriedade deverá ser definida como 0.

</dd> <dt>

**NegotiatedSpeed**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits por segundo"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Associação de porta do barramento DMTF \| 1,2 "), **PUnit** (" bit/segundo ")
</dt> </dl>

Quando várias velocidades de barramento e conexão são possíveis, essa propriedade define a velocidade em uso entre os dispositivos, em bits por segundo. Se as velocidades de conexão ou de barramento não forem negociadas, ou se essas informações não estiverem disponíveis ou não forem importantes para o gerenciamento de dispositivos, a propriedade deverá ser definida como "0".

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Dependência CIM**](cim-dependency.md)
</dt> </dl>

 

