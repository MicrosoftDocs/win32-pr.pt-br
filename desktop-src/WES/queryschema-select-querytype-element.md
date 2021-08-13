---
title: Selecionar elemento (QueryType)
description: Uma consulta XPath que identifica os eventos a serem incluídos no conjunto de resultados da consulta.
ms.assetid: b6aa747b-3586-460b-b51c-52fb112739c3
keywords:
- Selecionar EventLog do elemento
topic_type:
- apiref
api_name:
- Select
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b38a4f24746425bcdbea845b1c23ea5dadfdbcbefa41ebc5fa502147aba2ec67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118587399"
---
# <a name="select-querytype-element"></a>Selecionar elemento (QueryType)

Uma consulta XPath que identifica os eventos a serem incluídos no conjunto de resultados da consulta.

``` syntax
<xs:element name="Select">
    <xs:complexType
        mixed="true"
    >
        <xs:attribute name="Path"
            type="anyURI"
         />
    </xs:complexType>
</xs:element>
```

O elemento **Select** é definido pelo tipo complexo [**QueryType**](queryschema-querytype-complextype.md) .

## <a name="attributes"></a>Atributos



| Nome | Tipo   | Descrição                                                                              |
|------|--------|------------------------------------------------------------------------------------------|
| Caminho | anyURI | O nome do canal ou o caminho para o arquivo de log que contém os eventos.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Aplicativos de aplicativos UWP do vista desktop \|\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Aplicativos da área de trabalho do servidor 2008 \| aplicativo UWP\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Elemento pai**
</dt> <dt>

[**Consulta (QueryListType)**](queryschema-query-querylisttype-element.md)
</dt> </dl>

 

 





