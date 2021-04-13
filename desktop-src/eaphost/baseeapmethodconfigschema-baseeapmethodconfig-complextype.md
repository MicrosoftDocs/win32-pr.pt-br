---
title: Tipo complexo BaseEapMethodConfig
description: Saiba mais sobre o tipo complexo BaseEapMethodConfig. Esse tipo é um elemento de espaço reservado para a configuração do método.
ms.assetid: 9aafd6ad-2342-4882-99d3-2f2e6c3d67b5
keywords:
- BaseEapMethodConfig tipo complexo EAPHost
topic_type:
- apiref
api_name:
- BaseEapMethodConfig
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ac7d628b554696fffd254a45b9b1021d68e2a55e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104366729"
---
# <a name="baseeapmethodconfig-complex-type"></a>Tipo complexo BaseEapMethodConfig

O tipo complexo **BaseEapMethodConfig** é um elemento de espaço reservado para a configuração do método.

``` syntax
<xs:complexType name="BaseEapMethodConfig">
    <xs:sequence>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##any"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="remarks"></a>Comentários

O método EAP executa a validação de esquema no conteúdo do elemento **BaseEapMethodConfig** .

## <a name="requirements"></a>Requisitos



| Função | Versão mínima do sistema operacional com suporte |
|------|------------------------------|
| Cliente<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[EAPHost e esquema herdado](eaphost-schemas.md)
</dt> <dt>

[Esquema baseeapmethodconfig](baseeapmethodconfigschema-schema.md)
</dt> </dl>

 

 





