---
title: Elemento suprimir (QueryType)
description: Uma consulta XPath que identifica os eventos a serem excluídos do conjunto de resultados da consulta.
ms.assetid: 41304a3c-bde1-49c3-8cb3-e95fc428bd96
keywords:
- Suprimir log de elemento
topic_type:
- apiref
api_name:
- Suppress
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3a1d7fcec98d32167155ebcafc4f13d2a727d59a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086439"
---
# <a name="suppress-querytype-element"></a>Elemento suprimir (QueryType)

Uma consulta XPath que identifica os eventos a serem excluídos do conjunto de resultados da consulta.

``` syntax
<xs:element name="Suppress">
    <xs:complexType
        mixed="true"
    >
        <xs:attribute name="Path"
            type="anyURI"
         />
    </xs:complexType>
</xs:element>
```

O elemento **suprimir** é definido pelo tipo complexo [**QueryType**](queryschema-querytype-complextype.md) .

## <a name="attributes"></a>Atributos



| Nome | Tipo   | Descrição                                                                              |
|------|--------|------------------------------------------------------------------------------------------|
| Caminho | anyURI | O nome do canal ou o caminho para o arquivo de log que contém os eventos.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Elemento pai**
</dt> <dt>

[**Consulta (QueryListType)**](queryschema-query-querylisttype-element.md)
</dt> </dl>

 

 





