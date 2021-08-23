---
description: Classe Msvm_EthernetDeviceSAPImplementation – representa uma associação entre um ponto de acesso de serviço e o dispositivo lógico que o implementa.
ms.assetid: C0DDB199-AD97-4DD7-8056-BD6BD0CECFA8
title: Classe Msvm_EthernetDeviceSAPImplementation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetDeviceSAPImplementation
- Msvm_EthernetDeviceSAPImplementation.Antecedent
- Msvm_EthernetDeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0cabf80b7e55513fc5fc31b744db8cbc973ccd15bcda170804c754850d65dbfa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119524976"
---
# <a name="msvm_ethernetdevicesapimplementation-class"></a>\_Classe Msvm EthernetDeviceSAPImplementation

Representa uma associação entre um ponto de acesso de serviço e o dispositivo lógico que o implementa. A cardinalidade dessa associação é muitos-para-muitos. Um SAP (ponto de acesso A serviços) pode ser fornecido por mais de um dispositivo lógico, operando em conjunto. Qualquer dispositivo pode fornecer mais de um SAP. Quando muitos dispositivos lógicos são associados a um único SAP, supõe-se que esses elementos operam em conjunto para fornecer o ponto de acesso. Se diferentes implementações de um SAP existirem, cada uma dessas implementações resultaria em instanciações individuais do objeto SAP. Essas instanciações individuais teriam associações para as implementações exclusivas.

A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetDeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  CIM_EthernetPort REF Antecedent;
  Msvm_LANEndpoint REF Dependent;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ EthernetDeviceSAPImplementation** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ EthernetDeviceSAPImplementation** tem essas propriedades.

<dl> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Uma referência a uma classe derivada do [**CIM \_ EthernetPort**](/previous-versions/windows/desktop/iscsitarg/cim-ethernetport) que representa o dispositivo lógico.

</dd> <dt>

**Depende**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **Msvm \_ LANEndpoint**](msvm-lanendpoint.md)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")
</dt> </dl>

Uma referência a uma instância da classe [**Msvm \_ LANEndpoint**](msvm-lanendpoint.md) que representa o SAP que está usando o **Antecedent**.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

