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
ms.openlocfilehash: e9d02b77b4a36bac26d52d7bf8d849eab8731d27
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086338"
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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



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

 

 





