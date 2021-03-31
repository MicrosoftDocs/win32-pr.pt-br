---
title: Elemento EapType (Propriedade de conexão de esquema v1)
description: Saiba mais sobre o elemento EapType. Esse elemento captura a configuração específica do método dentro do elemento EAP. | Elemento EapType (Propriedade de conexão de esquema v1)
ms.assetid: f953e150-64cf-41b2-937f-410799be4602
keywords:
- Elemento EapType EAPHost
topic_type:
- apiref
api_name:
- EapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 88361931946f8a209c5b1c41bd17fcbd0e44096d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103663876"
---
# <a name="eaptype-element-v1-schema-connection-property"></a>Elemento EapType (Propriedade de conexão de esquema v1)

O elemento **EapType** captura a configuração específica do método dentro do elemento EAP.

``` syntax
<xs:element name="EapType"
    type="BaseEapTypeParameters"
 />
```

## <a name="remarks"></a>Comentários

O elemento **EapType** é abstrato; cada método deve definir e usar um elemento derivado nos documentos da instância.

## <a name="requirements"></a>Requisitos



| Função | Versão mínima do sistema operacional com suporte |
|------|------------------------------|
| Cliente<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[EAPHost e esquema herdado](eaphost-schemas.md)
</dt> <dt>

[Esquema baseeapconnectionpropertiesv1](baseeapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





