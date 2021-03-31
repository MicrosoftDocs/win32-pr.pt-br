---
description: Uma classe abstrata para subclasses que representam uma coleção de \_ objetos CIM ManagedSystemElement. Essas coleções permitem que os elementos do sistema gerenciado sejam agrupados para fins de identificação e para simplificar a associação de definições e configurações.
ms.assetid: f47bf1d6-6d89-4d9f-82d1-99a7343481bc
title: Classe CIM_CollectionOfMSEs (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectionOfMSEs
- CIM_CollectionOfMSEs.CollectionID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e467e775c78364718f25cc732d6689d9fb2b9da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827891"
---
# <a name="cim_collectionofmses-class-hyper-v-management"></a>Classe CIM_CollectionOfMSEs (gerenciamento do Hyper-V)

Uma classe abstrata para subclasses que representam uma coleção de objetos [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) . Essas coleções permitem que os elementos do sistema gerenciado sejam agrupados para fins de identificação e para simplificar a associação de definições e configurações.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Collection"), AMENDMENT]
class CIM_CollectionOfMSEs : CIM_Collection
{
  string CollectionID;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ CollectionOfMSEs** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ CollectionOfMSEs** tem essas propriedades.

<dl> <dt>

**CollectionID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

A identificação do objeto de coleção. Quando uma subclasse, a propriedade **CollectionId** pode ser substituída como uma propriedade de chave.

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

[**\_Coleção CIM**](cim-collection.md)
</dt> </dl>

 

