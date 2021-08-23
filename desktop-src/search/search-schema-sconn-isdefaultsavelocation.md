---
description: O elemento booliano opcional <isDefaultSaveLocation> especifica se o local descrito no conector de pesquisa deve ser usado como o local de salvamento padrão. Este elemento não tem elementos filho e nenhum atributo.
ms.assetid: 4a33f411-d71e-41d3-b5fd-018a92dceeac
title: Elemento isDefaultSaveLocation (esquema do conector de pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e94cfe2f620dd7c4ccac2bed27dd87511e9174861aeb74dce9ac5737263e9275
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119597476"
---
# <a name="isdefaultsavelocation-element-search-connector-schema"></a>Elemento isDefaultSaveLocation (esquema do conector de pesquisa)

O elemento booliano opcional <isDefaultSaveLocation> especifica se o local descrito no conector de pesquisa deve ser usado como o local de salvamento padrão. Este elemento não tem elementos filho e nenhum atributo.

## <a name="syntax"></a>Syntax


```
<!-- isDefaultSaveLocation -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="isDefaultSaveLocation" type="xs:boolean" minOccurs="0"/>
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

quando um usuário opta por salvar um item, o Windows Explorer salva o item no local especificado no <simpleLocation> elemento. Os usuários podem alterar essa configuração usando a caixa de diálogo Propriedades do conector de pesquisa.

## <a name="example"></a>Exemplo


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <isDefaultSaveLocation>true</isDefaultSaveLocation>
    ...
</searchConnectionDescription>
```



 

 



