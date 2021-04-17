---
title: Elemento servernames (ServerValidationParameters) (TLS)
description: Saiba mais sobre o elemento Servernames (ServerValidationParameters). Esse elemento representa uma lista de nomes de servidor delimitados por ponto e vírgula. | Elemento servernames (ServerValidationParameters) (TLS)
ms.assetid: c6cfcc67-4e6a-4bf0-87d9-37cc1d504598
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
ms.openlocfilehash: ef94bc650432c4fb87abf00a93841d0d4d42e965
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105763462"
---
# <a name="servernames-servervalidationparameters-element-tls"></a>Elemento servernames (ServerValidationParameters) (TLS)

O elemento **servernames (ServerValidationParameters)** representa uma lista de nomes de servidor delimitados por ponto e vírgula.

``` syntax
<xs:element name="ServerNames"
    type="string"
    minOccurs="0"
 />
```

O elemento **servernames** é definido pelo tipo complexo [**ServerValidationParameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md) .

## <a name="remarks"></a>Comentários

Cada nome de servidor é delimitado por ponto e vírgula e pode ser representado por expressões regulares. O elemento **servernames** é opcional.

## <a name="requirements"></a>Requisitos



| Função | Versão mínima do sistema operacional com suporte |
|------|------------------------------|
| Cliente<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**ServerValidationParameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

**Possíveis elementos pai imediatos na instância de esquema**
</dt> <dt>

[**ServerValidation (EapType)**](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost e esquema herdado](eaphost-schemas.md)
</dt> <dt>

[Esquema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Elementos do esquema eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





