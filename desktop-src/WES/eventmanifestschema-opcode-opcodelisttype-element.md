---
title: Elemento opcode (OpcodeListType)
description: Contém um valor numérico que identifica a atividade ou um ponto dentro de uma atividade que o aplicativo estava executando quando ele gerou o evento (por exemplo, inicialização ou fechamento).
ms.assetid: 8c5cfbd3-6a74-452c-a12f-41d663426e2c
keywords:
- EventLog do elemento opcode
topic_type:
- apiref
api_name:
- opcode
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c10d7ae91d29f3bee72ef43b11b9f30f6229d4a43df4ace213d943b333bffd3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136239"
---
# <a name="opcode-opcodelisttype-element"></a>Elemento opcode (OpcodeListType)

Contém um valor numérico que identifica a atividade ou um ponto dentro de uma atividade que o aplicativo estava executando quando ele gerou o evento (por exemplo, inicialização ou fechamento).

``` syntax
<xs:element name="opcode"
    type="OpcodeType"
 />
```

O elemento **opcode** é definido pelo tipo complexo [**OpcodeListType**](eventmanifestschema-opcodelisttype-complextype.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Elementos pai**
</dt> <dt>

[**opcodes (TaskType)**](eventmanifestschema-opcodes-tasktype-element.md)
</dt> <dt>

[**opcodes (ProviderType)**](eventmanifestschema-opcodes-providertype-element.md)
</dt> <dt>

[**opcodes (MetadataType)**](eventmanifestschema-opcodes-metadatatype-element.md)
</dt> </dl>

 

 





