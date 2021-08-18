---
title: Elemento InnerEapOptional (EapType)
description: Saiba mais sobre o elemento InnerEapOptional (EapType). Este elemento indica se o acesso de convidado deve ser realizado.
ms.assetid: 2d314c89-5415-407f-84c3-c4c5c8957b39
keywords:
- Elemento InnerEapOptional EAPHost
topic_type:
- apiref
api_name:
- InnerEapOptional
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 372163b39ea788b5c03bd25aedcc44aee172d58080fb94e3333a029a514962a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119404586"
---
# <a name="innereapoptional-eaptype-element"></a>Elemento InnerEapOptional (EapType)

O elemento **InnerEapOptional (EapType)** indica se o acesso ao convidado deve ser realizado.

``` syntax
<xs:element name="InnerEapOptional"
    type="boolean"
 />
```

O elemento **InnerEapOptional** é definido pelo elemento [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) .

## <a name="remarks"></a>Comentários

Se o elemento **InnerEapOptional** for true, o elemento [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md) deverá estar presente e descrever o método interno e sua configuração; Se for FALSE, o PEAP executará o acesso de convidado. O elemento **InnerEapOptional** é opcional.

## <a name="requirements"></a>Requisitos



| Função | Versão mínima do sistema operacional com suporte |
|------|------------------------------|
| Cliente<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost e esquema herdado](eaphost-schemas.md)
</dt> <dt>

[Esquema mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Elementos do esquema mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





