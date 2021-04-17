---
title: Elemento AcceptServerName
description: Indica se o nome do servidor é validado em relação à cadeia de caracteres de nome especificada no elemento Servernames (ServerValidationParameters). | Elemento AcceptServerName
ms.assetid: 307b2d2a-1678-4aa9-82ed-46d401cf0e0f
keywords:
- Elemento AcceptServerName EAPHost
topic_type:
- apiref
api_name:
- AcceptServerName
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b48c43bce2bd71f4d761ea58fcdf5e0632107f87
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105763481"
---
# <a name="acceptservername-element"></a>Elemento AcceptServerName

O elemento **AcceptServerName (EapType)** indica se o nome do servidor é validado em relação à cadeia de caracteres de nome especificada no elemento [**servernames (ServerValidationParameters)**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) .

``` syntax
<xs:element name="AcceptServerName"
    type="xs:boolean"
 />
```

O elemento **AcceptServerName** é definido pelo elemento [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) .

## <a name="remarks"></a>Comentários

O elemento **AcceptServerName** é opcional.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost e esquema herdado](eaphost-schemas.md)
</dt> <dt>

[eaptlsconnectionpropertiesv2](eaptlsconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[Elementos do esquema eaptlsconnectionpropertiesv2](eaptlsconnectionpropertiesv2schema-elements.md)
</dt> <dt>

[**AcceptServerName (EapType)**](eaptlsconnectionpropertiesv1schema-tlsextensionstype-peapextensionstype-element.md)
</dt> </dl>

 

 





