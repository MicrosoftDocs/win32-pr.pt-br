---
title: Elemento servernames (ServerValidationParameters) (PEAP)
description: Saiba mais sobre o elemento Servernames (ServerValidationParameters). Esse elemento representa uma lista de nomes de servidor delimitados por ponto e vírgula. | Elemento servernames (ServerValidationParameters) (PEAP)
ms.assetid: 2595daa1-9f1b-40cf-9219-0e7295fdd5c3
keywords:
- Elemento servernames EAPHost
topic_type:
- apiref
api_name:
- ServerNames
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f3f9de6ee28077b5206a9783ef7722864a479e1e5f26b78e4402ac79c6e4be5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984006"
---
# <a name="servernames-servervalidationparameters-element-peap"></a>Elemento servernames (ServerValidationParameters) (PEAP)

O elemento **servernames (ServerValidationParameters)** representa uma lista de nomes de servidor delimitados por ponto e vírgula.

``` syntax
<xs:element name="ServerNames"
    type="string"
    minOccurs="0"
 />
```

O elemento **servernames** é definido pelo tipo complexo [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) .

## <a name="remarks"></a>Comentários

Cada nome de servidor é delimitado por ponto e vírgula e pode ser representado por expressões regulares. O elemento **servernames** é opcional.

## <a name="requirements"></a>Requisitos



| Função | Versão mínima do sistema operacional com suporte |
|------|------------------------------|
| Cliente<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

**Possíveis elementos pai imediatos na instância de esquema**
</dt> <dt>

[**ServerValidation (EapType)**](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost e esquema herdado](eaphost-schemas.md)
</dt> <dt>

[Esquema mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Elementos do esquema mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





