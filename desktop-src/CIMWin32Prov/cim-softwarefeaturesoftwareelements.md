---
description: A associação CIM \_ SoftwareFeatureSoftwareElements identifica os elementos de software que comem um recurso de software específico.
ms.assetid: 933586c5-b85e-4136-b557-5151a48abc32
ms.tgt_platform: multiple
title: CIM_SoftwareFeatureSoftwareElements classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareFeatureSoftwareElements
- CIM_SoftwareFeatureSoftwareElements.PartComponent
- CIM_SoftwareFeatureSoftwareElements.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5ff4f7f9fb0457ccf490a7c2066556c4c5e2537c77f005d86bb140c6eb7fdb6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118421108"
---
# <a name="cim_softwarefeaturesoftwareelements-class"></a>Classe CIM \_ SoftwareFeatureSoftwareElements

A **associação CIM \_ SoftwareFeatureSoftwareElements** identifica os elementos de software que comem um recurso de software específico.

> [!IMPORTANT]
> As classes CIM (Distributed Management Task Force) modelo CIM DMTF são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos esquemas de versão [do CIM 2.x.](https://dmtf.org/standards/cim/schemas)

 

A sintaxe a seguir é simplificada do Managed Object Format (MOF) e inclui todas as suas propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[UUID("{A91081E2-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SoftwareFeatureSoftwareElements : CIM_Component
{
  CIM_SoftwareElement REF PartComponent;
  CIM_SoftwareFeature REF GroupComponent;
};
```

## <a name="members"></a>Membros

A **classe CIM \_ SoftwareFeatureSoftwareElements** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe CIM \_ SoftwareFeatureSoftwareElements** tem essas propriedades.

<dl> <dt>

**Groupcomponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **\_ Software CIMFeature**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **agregação**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

O componente de grupo.

Essa propriedade é herdada do [**componente CIM \_**](cim-component.md).

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ SoftwareElement**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O componente de parte.

Essa propriedade é herdada do [**componente CIM \_**](cim-component.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

A **associação CIM \_ SoftwareFeatureSoftwareElements** é derivada do [**componente CIM \_**](cim-component.md).

O WMI não implementa essa classe. Para classes WMI derivadas de **SOFTWARE \_ CIMFeatureSoftwareElements**, consulte [Classes Win32](win32-provider.md).

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

[**Componente \_ CIM**](cim-component.md)
</dt> </dl>

 

