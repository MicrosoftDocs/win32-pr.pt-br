---
title: Tipo complexo BaseEapMethodUserCredentials
description: Saiba mais sobre o tipo complexo BaseEapMethodUserCredentials. Esse tipo é um elemento de espaço reservado para dados de credencial de método.
ms.assetid: ebbf813d-657a-4ff2-acf2-c18ce694b564
keywords:
- Tipo complexo BaseEapMethodUserCredentials EAPHost
topic_type:
- apiref
api_name:
- BaseEapMethodUserCredentials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8102f095ca7d4b1ada6db3c21fbe55e73a98ed6d06d2d6b99032f1a21a344527
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120094416"
---
# <a name="baseeapmethodusercredentials-complex-type"></a>Tipo complexo BaseEapMethodUserCredentials

O **tipo complexo BaseEapMethodUserCredentials** é um elemento de espaço reservado para dados de credencial de método.

``` syntax
<xs:complexType name="BaseEapMethodUserCredentials">
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

O método EAP executa a validação de esquema no conteúdo **de BaseEapMethodUserCredentials**.

## <a name="requirements"></a>Requisitos



| Função | Versão mínima do sistema operacional com suporte |
|------|------------------------------|
| Cliente<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[EAPHost e esquema herdado](eaphost-schemas.md)
</dt> <dt>

[Esquema baseeapmethethethercredentials](baseeapmethodusercredentialsschema-schema.md)
</dt> </dl>

 

 





