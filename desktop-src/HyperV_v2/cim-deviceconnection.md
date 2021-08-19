---
description: Uma relação que indica que dois ou mais dispositivos estão conectados.
ms.assetid: 84282740-f60f-46fa-95b7-b52a7e6efcc4
title: CIM_DeviceConnection classe (gerenciamento do Hyper-V)
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
ms.openlocfilehash: 81ec2826339e27d956750360b280fcafd7b55e6264a6bcab83ebc1cb41a1ddee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117812840"
---
# <a name="cim_deviceconnection-class-hyper-v-management"></a>CIM_DeviceConnection classe (gerenciamento do Hyper-V)

Uma relação que indica que dois ou mais dispositivos estão conectados.

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

A **classe \_ DeviceConnection CIM** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ DeviceConnection cim** tem essas propriedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de dados: **Cim \_ LogicalDevice**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecessor")
</dt> </dl>

Um dispositivo.

</dd> <dt>

**Dependente**
</dt> <dd> <dl> <dt>

Tipo de dados: **Cim \_ LogicalDevice**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependente")
</dt> </dl>

Um segundo dispositivo que está conectado ao outro dispositivo.

</dd> <dt>

**NegotiatedDataWidth**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Associação de porta do Barramento DMTF \| \| 001.3"), **PUnit** ("bit")
</dt> </dl>

Quando várias larguras de dados de conexão e barramento são possíveis, a propriedade NegotiatedDataWidth define aquela que está em uso entre os Dispositivos. A largura dos dados é especificada em bits. Se a largura dos dados não for negociada ou se essas informações não estão disponíveis ou não são importantes para o Gerenciamento de dispositivos, a propriedade deve ser definida como 0.

</dd> <dt>

**NegotiatedSpeed**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits por Segundo"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Associação de porta do Barramento DMTF \| \| 001.2"), **PUnit** ("bit/segundo")
</dt> </dl>

Quando várias velocidades de conexão e barramento são possíveis, essa propriedade define a velocidade que está em uso entre os dispositivos, em bits por segundo. Se as velocidades de conexão ou barramento não são negociadas ou se essas informações não estão disponíveis ou não são importantes para o gerenciamento de dispositivos, a propriedade deve ser definida como "0".

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | Virtualização \\ raiz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Dependência cim \_**](cim-dependency.md)
</dt> </dl>

 

