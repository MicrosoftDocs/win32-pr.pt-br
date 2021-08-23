---
description: Identifica a cadeia de caracteres de APN ou de discagem a ser usada para estabelecer uma conexão de dados.
ms.assetid: e791ffa1-b417-480c-adb8-b1dda7547d89
title: Elemento accessstring (contextType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AccessString
api_type:
- Schema
ms.openlocfilehash: 603c4aa04bb3e86891ec121233474fa96ffd792cbcb6880bad9e76599003d979
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975275"
---
# <a name="accessstring-contexttype-element"></a>Elemento accessstring (contextType)

O elemento **accessstring (ContextType)** identifica a cadeia de caracteres de APN ou de discagem a ser usada para estabelecer uma conexão de dados.

Esse elemento pode ter um comprimento máximo de 100 caracteres.

Esse elemento é opcional.

``` syntax
<xs:element name="AccessString">
    <xs:simpleType>
        <xs:restriction
            base="token"
        >
            <xs:minLength
                value="1"
             />
            <xs:maxLength
                value="100"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

O elemento **accessstring** é definido pelo tipo complexo [**ContextType**](schema-contexttype-complextype.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[aplicativos UWP para aplicativos de área de trabalho Windows 7 \|\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                         |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**contextType**](schema-contexttype-complextype.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**Contexto (MBNProfile)**](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 




