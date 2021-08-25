---
description: A \_ classe CIM SAPSAPDependency é uma associação entre dois SAPs (pontos de acesso ao serviço), o que indica que o segundo SAP é necessário para que o primeiro SAP se conecte ao seu serviço.
ms.assetid: ba5f47d9-ebe5-4dcb-8a6d-0974acf67385
ms.tgt_platform: multiple
title: Classe CIM_SAPSAPDependency (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SAPSAPDependency
- CIM_SAPSAPDependency.Dependent
- CIM_SAPSAPDependency.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 34b02a77f5dc67d1149f07e66f5740d6b99ab73e4c0dfbc637d387d47b8c54fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920236"
---
# <a name="cim_sapsapdependency-class-cimwin32-wmi-providers"></a>Classe CIM_SAPSAPDependency (provedores WMI CIMWin32)

A classe **CIM \_ SAPSAPDependency** é uma associação entre dois SAPs (pontos de acesso ao serviço), o que indica que o segundo SAP é necessário para que o primeiro SAP se conecte ao seu serviço. Por exemplo, para imprimir em uma impressora de rede, os pontos de acesso à impressora local devem usar SAPs subjacentes relacionados à rede, ou pontos de extremidade de protocolo, para enviar a solicitação de impressão.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[UUID("{422D175A-E3D5-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SAPSAPDependency : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Dependent;
  CIM_ServiceAccessPoint REF Antecedent;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ SAPSAPDependency** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ SAPSAPDependency** tem essas propriedades.

<dl> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ ServiceAccessPoint**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Um [**\_ ServiceAccessPoint CIM**](cim-serviceaccesspoint.md) que descreve o ponto de acesso de serviço necessário.

</dd> <dt>

**Depende**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ ServiceAccessPoint**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")
</dt> </dl>

Um [**\_ ServiceAccessPoint CIM**](cim-serviceaccesspoint.md) que descreve o ponto de acesso de serviço que é dependente de um SAP subjacente.

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **CIM \_ SAPSAPDependency** é derivada da [**\_ dependência CIM**](cim-dependency.md).

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

 

