---
description: A \_ classe CIM RedundancyComponent associa um grupo de redundância composto por elementos do sistema gerenciado e indica que, juntos, os elementos fornecem redundância.
ms.assetid: 2511ae26-011a-4e0d-ad34-d5fe9c78f0ff
ms.tgt_platform: multiple
title: Classe CIM_RedundancyComponent
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
ms.openlocfilehash: 5bcd1c16417ba0c02e13579f9e471076d4c61818
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826153"
---
# <a name="cim_redundancycomponent-class"></a>\_Classe CIM RedundancyComponent

A classe **CIM \_ RedundancyComponent** associa um grupo de redundância composto por elementos do sistema gerenciado e indica que, juntos, os elementos fornecem redundância. Todos os elementos agregados em um grupo de redundância devem ser instanciações da mesma classe de objeto.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

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

A classe **CIM \_ RedundancyComponent** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ RedundancyComponent** tem essas propriedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ RedundancyGroup**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")
</dt> </dl>

A associação **CIM \_ RedundancyComponent** indica que o "este conjunto de fãs" ou "essas extensões físicas" participam de um único grupo de redundância.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ ManagedSystemElement**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Um [**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md) que descreve o elemento filho na associação.

Esta propriedade é herdada [**do \_ componente CIM**](cim-component.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

**CIM \_ RedundancyComponent** é derivado do [**\_ componente CIM**](cim-component.md).

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

[**\_Componente CIM**](cim-component.md)
</dt> </dl>

 

