---
title: Elemento Suppress (QueryType)
description: Uma consulta XPath que identifica os eventos a excluir do conjunto de resultados da consulta.
ms.assetid: 41304a3c-bde1-49c3-8cb3-e95fc428bd96
keywords:
- Suprimir elemento EventLog
topic_type:
- apiref
api_name:
- Suppress
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2612a98c282627154a9107f2f9f77a3ddb52c191e00dbcb394c8db4d7c796b79
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032006"
---
# <a name="suppress-querytype-element"></a>Elemento Suppress (QueryType)

Uma consulta XPath que identifica os eventos a excluir do conjunto de resultados da consulta.

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

O **elemento Suppress** é definido pelo tipo complexo [**QueryType.**](queryschema-querytype-complextype.md)

## <a name="attributes"></a>Atributos



| Nome | Tipo   | Descrição                                                                              |
|------|--------|------------------------------------------------------------------------------------------|
| Caminho | anyURI | O nome do canal ou o caminho para o arquivo de log que contém os eventos.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Elemento pai**
</dt> <dt>

[**Consulta (QueryListType)**](queryschema-query-querylisttype-element.md)
</dt> </dl>

 

 





