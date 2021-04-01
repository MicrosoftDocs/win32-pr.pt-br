---
description: A \_ classe CIM SoftwareFeatureSAPImplementation representa uma associação entre um ponto de acesso de serviço (SAP) e como ele é implementado no software.
ms.assetid: d9a5a747-b37b-4005-a661-2bfc6a83bbb2
ms.tgt_platform: multiple
title: Classe CIM_SoftwareFeatureSAPImplementation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareFeatureSAPImplementation
- CIM_SoftwareFeatureSAPImplementation.Dependent
- CIM_SoftwareFeatureSAPImplementation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4130163ce90aea7a72b4d76a5c6c20b0631edf3b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826150"
---
# <a name="cim_softwarefeaturesapimplementation-class"></a>\_Classe CIM SoftwareFeatureSAPImplementation

A classe **CIM \_ SoftwareFeatureSAPImplementation** representa uma associação entre um ponto de acesso de serviço (SAP) e como ele é implementado no software. Um SAP pode ser fornecido por mais de um recurso de software para operar em conjunto com um do outro. Além disso, um recurso de software pode fornecer mais de um SAP. Quando muitos recursos de software estão associados a um único SAP, supõe-se que os elementos operam em conjunto para fornecer o ponto de acesso. Se diferentes implementações de um SAP existirem, cada implementação resultaria em instanciações individuais do objeto SAP. As instanciações individuais teriam associações para as implementações exclusivas.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[UUID("{7EFCC186-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SoftwareFeatureSAPImplementation : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Dependent;
  CIM_SoftwareFeature    REF Antecedent;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ SoftwareFeatureSAPImplementation** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ SoftwareFeatureSAPImplementation** tem essas propriedades.

<dl> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ SoftwareFeature**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Um [**\_ SoftwareFeature CIM**](cim-softwarefeature.md) que descreve o recurso de software Antecedent.

</dd> <dt>

**Depende**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ ServiceAccessPoint**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")
</dt> </dl>

Um [**\_ ServiceAccessPoint CIM**](cim-serviceaccesspoint.md) que descreve o ponto de acesso do serviço dependente.

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **CIM \_ SoftwareFeatureSAPImplementation** é derivada da [**\_ dependência CIM**](cim-dependency.md).

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

[**\_Dependência CIM**](cim-dependency.md)
</dt> </dl>

 

