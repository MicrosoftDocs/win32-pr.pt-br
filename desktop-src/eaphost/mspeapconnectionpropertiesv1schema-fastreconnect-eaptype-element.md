---
title: Elemento FastReconnect (EapType)
description: Saiba mais sobre o elemento FastReconnect (EapType). Esse elemento indica se uma reconexão rápida deve ser executada.
ms.assetid: 075285b0-7b1b-4d3c-af27-a718f3c20394
keywords:
- Elemento FastReconnect EAPHost
topic_type:
- apiref
api_name:
- FastReconnect
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1bda956d698ebefef956e85557c6d940baa02f6bcc9ef7cca0081fd668107e18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119238716"
---
# <a name="fastreconnect-eaptype-element"></a>Elemento FastReconnect (EapType)

O elemento **FastReconnect (EapType)** indica se uma reconexão rápida deve ser executada.

``` syntax
<xs:element name="FastReconnect"
    type="boolean"
 />
```

O elemento **FastReconnect** é definido pelo elemento [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) .

## <a name="remarks"></a>Comentários

Se o elemento **FastReconnect** for true, o PEAP tentará executar uma reconexão rápida; Se for FALSE, o PEAP executará a autenticação completa. O elemento **FastReconnect** é opcional.

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

 

 





