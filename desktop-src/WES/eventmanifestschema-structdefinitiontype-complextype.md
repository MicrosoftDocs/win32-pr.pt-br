---
title: Tipo complexo StructDefinitionType
description: Define uma estrutura que inclui um ou mais itens de dados que você deseja incluir com o evento. | Tipo complexo StructDefinitionType
ms.assetid: eb6b3682-1035-472b-8027-583d43c31748
keywords:
- Log de eventos do tipo complexo StructDefinitionType
topic_type:
- apiref
api_name:
- StructDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 035b8abe5440ffb80b902e1f4b1564b2fb80b77ee34b20f4f068d298b251478a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124246"
---
# <a name="structdefinitiontype-complex-type"></a>Tipo complexo StructDefinitionType

Define uma estrutura que inclui um ou mais itens de dados que você deseja incluir com o evento.

``` syntax
<xs:complexType name="StructDefinitionType"
    mixed="true"
>
    <xs:sequence>
        <xs:element name="data"
            type="DataDefinitionType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="string"
        use="required"
     />
    <xs:attribute name="length"
        type="LengthType"
        use="optional"
     />
    <xs:attribute name="count"
        type="CountType"
        use="optional"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementos filho



| Elemento                                                               | Type                                                                             | Descrição                                                               |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [**data**](eventmanifestschema-data-structdefinitiontype-element.md) | [**Datadefinitiontype**](eventmanifestschema-datadefinitiontype-complextype.md) | Define um item de dados que você deseja incluir na estrutura.<br/> |



## <a name="attributes"></a>Atributos



| Nome   | Tipo                                                            | Descrição                                                                                                                                                                                                                                                                               |
|--------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| count  | [**Número de contagem**](eventmanifestschema-counttype-simpletype.md)   | O número de elementos em uma matriz de estruturas. Esse atributo indica que a estrutura está definindo uma matriz de estruturas. Você pode especificar a contagem real ou o nome de um item de dados fora da estrutura que contém a contagem. <br/>                               |
| comprimento | [**Comprimentotype**](eventmanifestschema-lengthtype-simpletype.md) | Não disponível.<br/> **Windows Server 2008 e Windows Vista:** O comprimento dessa estrutura, em bytes. não disponível a partir do Windows 7.<br/>                                                                                                                            |
| name   | string                                                          | O nome para a estrutura. Você pode usar o nome para fazer referência ao item de dados no fragmento XML se especificar uma seção [**UserData**](eventmanifestschema-userdata-templateitemtype-element.md) em seu modelo.<br/> **Windows Vista:** Esse atributo é opcional.<br/> |



## <a name="remarks"></a>Comentários

Os provedores gravam a estrutura como um blob e não como membros individuais da estrutura. Se a estrutura C que você está escrevendo contiver ponteiros (por exemplo, um ponteiro do tipo LPWSTR), os dados do evento conterão o valor do ponteiro, não os dados desreferenciados.

Você não deve usar estruturas, mas, em vez disso, deve definir itens de dados para cada membro e gravá-los separadamente. Se você decidir usar estrutura, a estrutura deverá conter apenas tipos integrais e você deverá garantir que os membros da estrutura fiquem alinhados a um limite de 8 bytes. Se você não fizer isso, provavelmente receberá erros de alinhamento ao tentar acessar os dados. Considere usar a \# diretiva pragma Pack () para forçar o alinhamento em um limite de 8 bytes.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



 

 





