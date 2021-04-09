---
description: A \_ classe CIM PhysicalElementLocation associa um elemento físico a um \_ objeto de local CIM para fins de inventário ou substituição.
ms.assetid: d1698c1a-0eda-4e32-9a29-fb741b987671
ms.tgt_platform: multiple
title: Classe CIM_PhysicalElementLocation
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
ms.openlocfilehash: 5e47460a3563d9b7a86aa6ee65704fcb0a422c39
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089488"
---
# <a name="cim_physicalelementlocation-class"></a>\_Classe CIM PhysicalElementLocation

A classe **CIM \_ PhysicalElementLocation** associa um elemento físico a um objeto de [**\_ local CIM**](cim-location.md) para fins de inventário ou substituição.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

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

A classe **CIM \_ PhysicalElementLocation** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ PhysicalElementLocation** tem essas propriedades.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ físicoelement**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Referência ao elemento físico cujo local está especificado.

</dd> <dt>

**PhysicalLocation**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ local do CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Referência ao local do elemento físico.

</dd> </dl>

## <a name="remarks"></a>Comentários

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



 

