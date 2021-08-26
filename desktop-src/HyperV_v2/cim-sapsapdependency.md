---
description: Representa uma associação entre dois SAP (pontos de acesso de serviço), nos quais um SAP depende do outro para utilizar ou se conectar a um serviço.
ms.assetid: fba4144b-833f-469f-93df-e8a79aa37811
title: CIM_SAPSAPDependency classe (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SAPSAPDependency
- CIM_SAPSAPDependency.Antecedent
- CIM_SAPSAPDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ae8b1e45d1685204b15cf359f36cfced321fb75c099b7be76e0ece2ce3f836de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119980856"
---
# <a name="cim_sapsapdependency-class-hyper-v-management"></a>CIM_SAPSAPDependency classe (gerenciamento do Hyper-V)

Representa uma associação entre dois SAP (pontos de acesso de serviço), nos quais um SAP depende do outro para utilizar ou se conectar a um serviço. Por exemplo, para imprimir em uma impressora de rede, os pontos de acesso de impressão local devem utilizar SAPs subjacentes relacionados à rede para enviar a solicitação de impressão.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_SAPSAPDependency : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a>Membros

A **classe \_ CIM SAPSAPDependency** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ CIM SAPSAPDependency** tem essas propriedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de dados: **\_ Serviço CIMAccessPoint**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecessor")
</dt> </dl>

Uma referência ao SAP necessário.

</dd> <dt>

**Dependente**
</dt> <dd> <dl> <dt>

Tipo de dados: **\_ Serviço CIMAccessPoint**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependente")
</dt> </dl>

Uma referência ao SAP dependente.

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

 

