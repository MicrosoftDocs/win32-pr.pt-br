---
description: A \_ classe CIM PExtentRedundancyComponent representa as extensões físicas que participam de um grupo de redundância de armazenamento.
ms.assetid: 5a4bb1e8-7b99-410a-bba5-2c63beabd00e
ms.tgt_platform: multiple
title: Classe CIM_PExtentRedundancyComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PExtentRedundancyComponent
- CIM_PExtentRedundancyComponent.PartComponent
- CIM_PExtentRedundancyComponent.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d19d1c9fa504b30f7a87dcd1402f47376a0f4613095e9f2ee25d196cd60ae581
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118678650"
---
# <a name="cim_pextentredundancycomponent-class"></a>\_Classe CIM PExtentRedundancyComponent

A classe **CIM \_ PExtentRedundancyComponent** representa as extensões físicas que participam de um grupo de redundância de armazenamento.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, UUID("{AD3C1FA2-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_PExtentRedundancyComponent : CIM_RedundancyComponent
{
  CIM_PhysicalExtent         REF PartComponent;
  CIM_StorageRedundancyGroup REF GroupComponent;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ PExtentRedundancyComponent** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ PExtentRedundancyComponent** tem essas propriedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ StorageRedundancyGroup**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")
</dt> </dl>

Um [**\_ StorageRedundancyGroup CIM**](cim-storageredundancygroup.md) que descreve o grupo de redundância de armazenamento.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ PhysicalExtent**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Um [**\_ PhysicalExtent CIM**](cim-physicalextent.md) que descreve a extensão física que participa do grupo de redundância.

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **CIM \_ PExtentRedundancyComponent** é derivada de [**\_ RedundancyComponent CIM**](cim-redundancycomponent.md).

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



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**\_REDUNDANCYCOMPONENT CIM**](cim-redundancycomponent.md)
</dt> </dl>

 

