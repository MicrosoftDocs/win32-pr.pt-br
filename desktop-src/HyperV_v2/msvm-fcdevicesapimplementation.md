---
description: Msvm_FcDeviceSAPImplementation classe - representa uma associação entre um ponto de acesso de serviço e o dispositivo lógico que o implementa.
ms.assetid: 5510c179-09e6-4762-b9b3-68ed49eafd66
title: Msvm_FcDeviceSAPImplementation classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FcDeviceSAPImplementation
- Msvm_FcDeviceSAPImplementation.Antecedent
- Msvm_FcDeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9aafe3bd029960a0b371c3a3d5ab54b66ad4849210189ab2946df2854656c500
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119523456"
---
# <a name="msvm_fcdevicesapimplementation-class"></a>Classe Msvm \_ FcDeviceSAPImplementation

Representa uma associação entre um ponto de acesso de serviço e o dispositivo lógico que o implementa. A cardinalidade dessa associação é muitos para muitos. Um SAP (ponto de acesso de serviço) pode ser fornecido por mais de um dispositivo lógico, operando em conjunto. Qualquer dispositivo pode fornecer mais de um SAP. Quando muitos dispositivos lógicos estão associados a um único SAP, supõe-se que esses elementos operem em conjunto para fornecer o ponto de acesso. Se existirem implementações diferentes de um SAP, cada uma dessas implementações resultará em instações individuais do objeto SAP. Essas instações individuais teriam associações às implementações exclusivas.

A sintaxe a seguir é simplificada Managed Object Format código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FcDeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  CIM_FCPort      REF Antecedent;
  Msvm_FcEndpoint REF Dependent;
};
```

## <a name="members"></a>Membros

A **classe Msvm \_ FcDeviceSAPImplementation** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe Msvm \_ FcDeviceSAPImplementation** tem essas propriedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ FCPort**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecessor")
</dt> </dl>

Uma referência a uma classe derivada de **CIM \_ FCPort** que representa o dispositivo lógico.

</dd> <dt>

**Dependente**
</dt> <dd> <dl> <dt>

Tipo de dados: **Msvm \_ FcEndpoint**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependente")
</dt> </dl>

Uma referência a uma instância da [**classe \_ FcEndpoint Msvm**](msvm-fcendpoint.md) que representa o SAP que está usando o **Antecessor.**

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                                    |
| Namespace<br/>                | Virtualização \\ raiz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

