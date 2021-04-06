---
description: O <dateCreated> elemento opcional identifica a data e a hora em que esse conector de pesquisa foi criado, usando o padrão ISO 8601. Ele não tem nenhum elemento filho e nenhum atributo.
ms.assetid: 96d8b067-b5ab-4d36-a8d7-1d084a9f661d
title: Elemento dateCreated (esquema do conector de pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6017c0555d464a49192c4fe8cb7e347bbab0e367
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646860"
---
# <a name="datecreated-element-search-connector-schema"></a>Elemento dateCreated (esquema do conector de pesquisa)

O <dateCreated> elemento opcional identifica a data e a hora em que esse conector de pesquisa foi criado, usando o padrão ISO 8601. Ele não tem nenhum elemento filho e nenhum atributo.

## <a name="syntax"></a>Syntax


```
<!-- dateCreated -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="dateCreated" type="xs:dateTime" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>Informações do elemento



| Elemento pai                                                                                                   | Elementos filho |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [Elemento searchConnectorDescriptionType (esquema do conector de pesquisa)](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a>Comentários

O formato do valor desse elemento segue o padrão ISO 8601. Um uso comum seria um dos seguintes:

-   \[Aaaa \] - \[ mm \] - \[ DD \] T \[ hh \] : \[ mm \] : \[ SS \] ± \[ hh \] : \[ mm \] ("1981-04-05T14:30:30-05:00")
-   \[AAAA \] \[ mm \] \[ DD \] T \[ hh \] \[ mm \] \[ SS \] Z ("19810405T193030Z")

## <a name="example"></a>Exemplo


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <dateCreated>2009-04-05T12:00:00-05:00</dateCreated>
    ...
</searchConnectionDescription>
```



 

 



