---
description: A classe CIM PhysicalElementLocation associa um elemento físico a um objeto Local CIM para fins de inventário \_ \_ ou substituição.
ms.assetid: d1698c1a-0eda-4e32-9a29-fb741b987671
ms.tgt_platform: multiple
title: CIM_PhysicalElementLocation classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalElementLocation
- CIM_PhysicalElementLocation.Element
- CIM_PhysicalElementLocation.PhysicalLocation
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4ab75b4f7bd6e7aaff262445a33d412c587c1a9ba179f873c597a4cca3485323
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118678177"
---
# <a name="cim_physicalelementlocation-class"></a>Classe CIM \_ PhysicalElementLocation

A **classe \_ CIM PhysicalElementLocation** associa um elemento físico a um objeto [**Local CIM \_**](cim-location.md) para fins de inventário ou substituição.

> [!IMPORTANT]
> As classes CIM (Distributed Management Task Force) modelo CIM DMTF são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos esquemas de versão [do CIM 2.x.](https://dmtf.org/standards/cim/schemas)

 

A sintaxe a seguir é simplificada do Managed Object Format (MOF) e inclui todas as suas propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, Association, UUID("{FAF76B68-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalElementLocation
{
  CIM_PhysicalElement REF Element;
  CIM_Location        REF PhysicalLocation;
};
```

## <a name="members"></a>Membros

A **classe \_ CIM PhysicalElementLocation** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ Cim PhysicalElementLocation** tem essas propriedades.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Tipo de dados: **Cim \_ PhysicalElement**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Referência ao elemento físico cujo local é especificado.

</dd> <dt>

**PhysicalLocation**
</dt> <dd> <dl> <dt>

Tipo de dados: **Localização cim \_**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Máx.**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Referência ao local do elemento físico.

</dd> </dl>

## <a name="remarks"></a>Comentários

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



 

