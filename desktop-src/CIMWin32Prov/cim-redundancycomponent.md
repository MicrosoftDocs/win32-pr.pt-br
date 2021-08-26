---
description: A classe CIM RedundancyComponent associa um grupo de redundância composto por elementos do sistema gerenciado e indica que, juntos, os elementos fornecem \_ redundância.
ms.assetid: 2511ae26-011a-4e0d-ad34-d5fe9c78f0ff
ms.tgt_platform: multiple
title: CIM_RedundancyComponent classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RedundancyComponent
- CIM_RedundancyComponent.GroupComponent
- CIM_RedundancyComponent.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bf2264d88a36f684c1ae198224a6e5543063bbf86ed3da77b0211f066eb080d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920786"
---
# <a name="cim_redundancycomponent-class"></a>Classe CIM \_ RedundancyComponent

A **classe CIM \_ RedundancyComponent** associa um grupo de redundância composto por elementos do sistema gerenciado e indica que, juntos, os elementos fornecem redundância. Todos os elementos agregados em um grupo de redundância devem ser instaências da mesma classe de objeto.

> [!IMPORTANT]
> As classes CIM (Distributed Management Task Force) do DMTF (Distributed Management Task Force) modelo CIM são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos esquemas de versão [do CIM 2.x.](https://dmtf.org/standards/cim/schemas)

 

A sintaxe a seguir é simplificada Managed Object Format código (MOF) e inclui todas as suas propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, UUID("{FB9D6E62-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_RedundancyComponent : CIM_Component
{
  CIM_RedundancyGroup      REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
};
```

## <a name="members"></a>Membros

A **classe CIM \_ RedundancyComponent** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe CIM \_ RedundancyComponent** tem essas propriedades.

<dl> <dt>

**Groupcomponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **\_ Cim RedundancyGroup**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")
</dt> </dl>

A **associação \_ CIM RedundancyComponent** indica que 'este conjunto de ventiladores' ou 'essas extensão físicas' participam de um único grupo de redundância.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **Cim \_ ManagedSystemElement**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Um [**\_ ManagedSystemElement cim**](cim-managedsystemelement.md) que descreve o elemento filho na associação.

Essa propriedade é herdada do [**componente CIM \_**](cim-component.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

**CIM \_ RedundancyComponent** é derivado do [**componente CIM \_**](cim-component.md).

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

[**Componente \_ CIM**](cim-component.md)
</dt> </dl>

 

