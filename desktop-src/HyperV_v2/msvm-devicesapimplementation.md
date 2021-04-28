---
description: Classe de Msvm_DeviceSAPImplementation – uma associação entre um ponto de acesso de serviço (SAP) e como ele é implementado.
ms.assetid: 36108521-A699-4498-A962-DC0801D9EE81
title: Classe Msvm_DeviceSAPImplementation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DeviceSAPImplementation
- Msvm_DeviceSAPImplementation.Antecedent
- Msvm_DeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6fbe3c9b85e0a8c9f0c6a07d1db03784c4ac15e6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112094"
---
# <a name="msvm_devicesapimplementation-class"></a>\_Classe Msvm DeviceSAPImplementation

Uma associação entre um ponto de acesso de serviço (SAP) e como ele é implementado. A cardinalidade dessa associação é muitos-para-muitos. Um SAP pode ser fornecido por mais de um dispositivo lógico, operando em conjunto. Qualquer dispositivo pode fornecer mais de um SAP. Quando muitos dispositivos lógicos são associados a um único SAP, supõe-se que esses elementos operam em conjunto para fornecer o ponto de acesso. Se diferentes implementações de um SAP existirem, cada uma dessas implementações resultaria em instanciações individuais do objeto SAP. Essas instanciações individuais teriam associações para as implementações exclusivas.

A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  CIM_LogicalDevice      REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ DeviceSAPImplementation** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ DeviceSAPImplementation** tem essas propriedades.

<dl> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **\_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O dispositivo lógico. Essa propriedade é herdada do [**CIM \_ DeviceSAPImplementation**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation).

</dd> <dt>

**Depende**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **CIM \_ ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O ponto de acesso ao serviço implementado usando o dispositivo lógico. Essa propriedade é herdada do [**CIM \_ DeviceSAPImplementation**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation).

</dd> </dl>

## <a name="remarks"></a>Comentários

O acesso à classe **Msvm \_ DeviceSAPImplementation** pode ser restringido pela filtragem do UAC. Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="examples"></a>Exemplos

Consulte [consultando objetos de rede](querying-networking-objects.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**\_DEVICESAPIMPLEMENTATION CIM**](cim-devicesapimplementation.md)
</dt> <dt>

[**\_DEVICESAPIMPLEMENTATION CIM**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation)
</dt> </dl>

 

