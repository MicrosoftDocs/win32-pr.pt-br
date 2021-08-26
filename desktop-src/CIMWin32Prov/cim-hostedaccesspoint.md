---
description: A classe Cim HostedAccessPoint representa uma associação entre um SAP (ponto de acesso de serviço) e o sistema no \_ qual ele é fornecido. Cada sistema pode hospedar muitos SAPs.
ms.assetid: 7da9b781-a5cb-42f5-b03c-4fc818c94e88
ms.tgt_platform: multiple
title: CIM_HostedAccessPoint classe (Provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedAccessPoint
- CIM_HostedAccessPoint.Dependent
- CIM_HostedAccessPoint.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 60903662ba915ede6fd344ab0c9db36685823da3202ea9dd6d762c8e652bf6e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921706"
---
# <a name="cim_hostedaccesspoint-class-cimwin32-wmi-providers"></a>CIM_HostedAccessPoint classe (Provedores WMI CIMWin32)

A **classe \_ Cim HostedAccessPoint** representa uma associação entre um SAP (ponto de acesso de serviço) e o sistema no qual ele é fornecido. Cada sistema pode hospedar muitos SAPs.

> [!IMPORTANT]
> As classes CIM (Distributed Management Task Force) do DMTF (Distributed Management Task Force) modelo CIM são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos esquemas de versão [do CIM 2.x.](https://dmtf.org/standards/cim/schemas)

 

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, UUID("{576C3C56-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_HostedAccessPoint : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Dependent;
  CIM_System             REF Antecedent;
};
```

## <a name="members"></a>Membros

A **classe \_ Cim HostedAccessPoint** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ Cim HostedAccessPoint** tem essas propriedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de dados: **Sistema CIM \_**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecessor"), Máx.(1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1) [](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Um [**sistema CIM \_ que**](cim-system.md) descreve o sistema de hospedagem.

</dd> <dt>

**Dependente**
</dt> <dd> <dl> <dt>

Tipo de dados: **\_ Serviço CIMAccessPoint**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependente"), [**Fraco**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Um [**Serviço \_ CIMAccessPoint**](cim-serviceaccesspoint.md) que descreve os SAP(s) hospedados nesse sistema.

</dd> </dl>

## <a name="remarks"></a>Comentários

**CIM \_ HostedAccessPoint** é derivado da [**\_ Dependência CIM.**](cim-dependency.md)

O WMI não implementa essa classe.

Esta documentação é derivada das descrições da classe CIM publicadas pelo DMTF. A Microsoft pode ter feito alterações para corrigir erros secundários, estar em conformidade com os padrões de documentação do SDK da Microsoft ou fornecer mais informações.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | RAIZ \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Dependência cim \_**](cim-dependency.md)
</dt> </dl>

 

