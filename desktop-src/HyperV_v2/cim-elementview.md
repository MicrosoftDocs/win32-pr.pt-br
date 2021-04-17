---
description: Representa e associação entre uma exibição e uma instância que representa a exibição normalizada de um recurso gerenciado.
ms.assetid: 9c6eb3d5-7366-4954-9e64-12f889c64114
title: Classe CIM_ElementView
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementView
- CIM_ElementView.Antecedent
- CIM_ElementView.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b6ffc0e4b69667800b1880cae1a992a207cc95a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755117"
---
# <a name="cim_elementview-class"></a>\_Classe CIM ElementView

Representa e associação entre uma exibição e uma instância que representa a exibição normalizada de um recurso gerenciado.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, Association, Experimental, Version("2.21.1"), UMLPackagePath("CIM::Core::CoreElements")]
class CIM_ElementView : CIM_Dependency
{
  CIM_ManagedElement REF Antecedent;
  CIM_View           REF Dependent;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ ElementView** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ ElementView** tem essas propriedades.

<dl> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ managedelement**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecessor")
</dt> </dl>

A instância que representa a exibição normalizada do recurso gerenciado.

</dd> <dt>

**Depende**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ exibição CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")
</dt> </dl>

A exibição que representa uma exibição de não normalizada ou agregada do recurso gerenciado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Dependência CIM**](cim-dependency.md)
</dt> </dl>

 

