---
description: Esta seção descreve as interfaces do sistema de propriedades do Windows.
ms.assetid: d81fe8df-9fd6-4ace-a47f-214cbba6f30c
title: Interfaces (sistema de propriedades do Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5003458683fb9b2443df0301676b601901817d54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768353"
---
# <a name="interfaces-windows-property-system"></a>Interfaces (sistema de propriedades do Windows)

Esta seção descreve as interfaces do sistema de propriedades do Windows.



| Tópico                                                                                        | Sumário                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPropertyChange**](/windows/win32/api/propsys/nn-propsys-ipropertychange)                                                 | Expõe um método que encapsula uma alteração em uma única propriedade.                                                                                                                                                                                                                                                                                                                          |
| [**IPropertyChangeArray**](/windows/win32/api/propsys/nn-propsys-ipropertychangearray)                                       | Expõe métodos para várias operações de várias alterações que podem ser passadas para [**IFileOperation**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileoperation).                                                                                                                                                                                                                                                                   |
| [**IPropertyDescription**](/windows/win32/api/propsys/nn-propsys-ipropertydescription)                                       | Expõe métodos que enumeram e recuperam detalhes da descrição da propriedade individual.                                                                                                                                                                                                                                                                                                       |
| [**IPropertyDescription2**](/windows/win32/api/propsys/nn-propsys-ipropertydescription2)                                     | Expõe métodos que enumeram e recuperam detalhes da descrição da propriedade individual.                                                                                                                                                                                                                                                                                                       |
| [**IPropertyDescriptionAliasInfo**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionaliasinfo)                     | Expõe métodos para obter as propriedades da coluna "classificar por" de um item. Essa interface é usada por objetos de interface do usuário que desejam recuperar as colunas de classificação primária ou secundária para uma determinada propriedade.                                                                                                                                                                                                |
| [**IPropertyDescriptionList**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist)                               | Expõe métodos que extraem informações de uma coleção de descrições de propriedades apresentadas como uma lista.                                                                                                                                                                                                                                                                                   |
| [**IPropertyDescriptionRelatedPropertyInfo**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionrelatedpropertyinfo) | Fornece um método que recupera uma interface [**IPropertyDescription**](/windows/win32/api/propsys/nn-propsys-ipropertydescription) .                                                                                                                                                                                                                                                                                       |
| [**IPropertyDescriptionSearchInfo**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionsearchinfo)                   | Expõe informações relacionadas à pesquisa de uma propriedade. As informações fornecidas por essa interface vêm do esquema [propertyDescription](./propdesc-schema-propertydescription.md) , do elemento [searchInfo](./propdesc-schema-searchinfo.md) para uma determinada propriedade. Essas informações são usadas pelo indexador do Windows Search. A maioria dos aplicativos de chamada não precisará chamar essa interface. |
| [**IPropertyEnumType**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype)                                             | Expõe métodos que extraem dados de informações de enumeração. O [**IPropertyEnumType**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype) dá acesso aos elementos [enum](./propdesc-schema-enum.md) e [enumRange](./propdesc-schema-enumrange.md) no [esquema de propriedade](./propdesc-schema-entry.md) de forma programática em tempo de execução.                                                                 |
| [**IPropertyEnumType2**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype2)                                           | Expõe métodos que extraem dados de informações de enumeração. [**IPropertyEnumType2**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype2) estende [**IPropertyEnumType**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype).                                                                                                                                                                                                               |
| [**IPropertyEnumTypeList**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtypelist)                                     | Expõe métodos que enumeram os valores possíveis para uma propriedade.                                                                                                                                                                                                                                                                                                                         |
| [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)                                                   | Expõe métodos para enumerar, obter e definir valores de propriedade.                                                                                                                                                                                                                                                                                                                     |
| [**IPropertyStoreCache**](/windows/win32/api/propsys/nn-propsys-ipropertystorecache)                                         | Expõe métodos que permitem que um manipulador gerencie vários Estados para cada propriedade.                                                                                                                                                                                                                                                                                                           |
| [**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities)                           | Expõe um método que determina se uma propriedade pode ser editada na interface de usuário pelo usuário.                                                                                                                                                                                                                                                                                                   |
| [**IPropertyStoreFactory**](/windows/win32/api/propsys/nn-propsys-ipropertystorefactory)                                     | Expõe métodos para obter um objeto [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) .                                                                                                                                                                                                                                                                                                               |
| [**IPropertySystem**](/windows/win32/api/propsys/nn-propsys-ipropertysystem)                                                 | Expõe métodos que obtêm descrições de propriedade, registram e cancelam o registro de esquemas de propriedade, enumeram descrições de propriedade e formatam valores de propriedade de forma de tipo estrito.                                                                                                                                                                                                                |
| [**IPropertyUI**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipropertyui)                                                         | Os desenvolvedores devem usar o [**IPropertyDescription**](/windows/win32/api/propsys/nn-propsys-ipropertydescription) em vez disso.                                                                                                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propriedades do Windows](props.md)
</dt> <dt>

[Esquema de descrição da propriedade](property-description-schema.md)
</dt> <dt>

[Conjuntos de propriedades](property-sets.md)
</dt> <dt>

[Funções](functions.md)
</dt> <dt>

[Estruturas](structures.md)
</dt> <dt>

[Constantes, enumerações e sinalizadores](constants--enumerations--and-flags.md)
</dt> </dl>

 

 
