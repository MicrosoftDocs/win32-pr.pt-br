---
description: Esta seção descreve as interfaces Windows sistema de propriedades.
ms.assetid: d81fe8df-9fd6-4ace-a47f-214cbba6f30c
title: Interfaces (Windows de propriedades)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d608e1b994541667847d755e95966b6ea2770c2d0c73ce86ef8fbd79b8c9dc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600116"
---
# <a name="interfaces-windows-property-system"></a>Interfaces (Windows de propriedades)

Esta seção descreve as interfaces Windows sistema de propriedades.



| Tópico                                                                                        | Sumário                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPropertyChange**](/windows/win32/api/propsys/nn-propsys-ipropertychange)                                                 | Expõe um método que encapsula uma alteração em uma única propriedade.                                                                                                                                                                                                                                                                                                                          |
| [**IPropertyChangeArray**](/windows/win32/api/propsys/nn-propsys-ipropertychangearray)                                       | Expõe métodos para várias operações de alteração que podem ser passadas para [**IFileOperation.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileoperation)                                                                                                                                                                                                                                                                   |
| [**IPropertyDescription**](/windows/win32/api/propsys/nn-propsys-ipropertydescription)                                       | Expõe métodos que enumeram e recuperam detalhes de descrição da propriedade individual.                                                                                                                                                                                                                                                                                                       |
| [**IPropertyDescription2**](/windows/win32/api/propsys/nn-propsys-ipropertydescription2)                                     | Expõe métodos que enumeram e recuperam detalhes de descrição da propriedade individual.                                                                                                                                                                                                                                                                                                       |
| [**IPropertyDescriptionAliasInfo**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionaliasinfo)                     | Expõe métodos para obter as propriedades de colunas "classificar por" para um item. Essa interface é usada por objetos de interface do usuário que querem recuperar as colunas de classificação primária ou secundária para uma determinada propriedade.                                                                                                                                                                                                |
| [**IPropertyDescriptionList**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist)                               | Expõe métodos que extraem informações de uma coleção de descrições de propriedade apresentadas como uma lista.                                                                                                                                                                                                                                                                                   |
| [**IPropertyDescriptionRelatedPropertyInfo**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionrelatedpropertyinfo) | Fornece um método que recupera uma interface [**IPropertyDescription.**](/windows/win32/api/propsys/nn-propsys-ipropertydescription)                                                                                                                                                                                                                                                                                       |
| [**IPropertyDescriptionSearchInfo**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionsearchinfo)                   | Expõe informações relacionadas à pesquisa para uma propriedade. As informações fornecidas por essa interface vêm do esquema [propertyDescription,](./propdesc-schema-propertydescription.md) [elemento searchInfo](./propdesc-schema-searchinfo.md) para uma determinada propriedade. Essas informações são usadas pelo Windows Search Indexer. A maioria dos aplicativos de chamada não precisará chamar essa interface. |
| [**IPropertyEnumType**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype)                                             | Expõe métodos que extraem dados de informações de enumeração. [**IPropertyEnumType**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype) fornece acesso aos elementos [enum](./propdesc-schema-enum.md) e [](./propdesc-schema-entry.md) [enumRange](./propdesc-schema-enumrange.md) no esquema de propriedade de maneira programática em tempo de operação.                                                                 |
| [**IPropertyEnumType2**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype2)                                           | Expõe métodos que extraem dados de informações de enumeração. [**IPropertyEnumType2**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype2) estende [**IPropertyEnumType.**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtype)                                                                                                                                                                                                               |
| [**IPropertyEnumTypeList**](/windows/win32/api/propsys/nn-propsys-ipropertyenumtypelist)                                     | Expõe métodos que enumeram os valores possíveis para uma propriedade .                                                                                                                                                                                                                                                                                                                         |
| [**Ipropertystore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)                                                   | Expõe métodos para enumerar, obter e definir valores de propriedade.                                                                                                                                                                                                                                                                                                                     |
| [**IPropertyStoreCache**](/windows/win32/api/propsys/nn-propsys-ipropertystorecache)                                         | Expõe métodos que permitem que um manipulador gerencie vários estados para cada propriedade.                                                                                                                                                                                                                                                                                                           |
| [**IPropertyStoreCapabilities**](/windows/win32/api/propsys/nn-propsys-ipropertystorecapabilities)                           | Expõe um método que determina se uma propriedade pode ser editada na interface do usuário pelo usuário.                                                                                                                                                                                                                                                                                                   |
| [**IPropertyStoreFactory**](/windows/win32/api/propsys/nn-propsys-ipropertystorefactory)                                     | Expõe métodos para obter um [**objeto IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore)                                                                                                                                                                                                                                                                                                               |
| [**IPropertySystem**](/windows/win32/api/propsys/nn-propsys-ipropertysystem)                                                 | Expõe métodos que têm descrições de propriedade, registram e registram e registram esquemas de propriedade, enumeram descrições de propriedade e formatam valores de propriedade de maneira estrita de tipo.                                                                                                                                                                                                                |
| [**IPropertyUI**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipropertyui)                                                         | Em vez disso, os [**desenvolvedores devem usar IPropertyDescription.**](/windows/win32/api/propsys/nn-propsys-ipropertydescription)                                                                                                                                                                                                                                                                                                      |



 

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

 

 
