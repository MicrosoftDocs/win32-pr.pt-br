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
ms.openlocfilehash: 3f2681e5682ad98ab5f4185174996920315d8c3b81dde8ba69d13ca178904ded
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118498782"
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
| Cliente<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>       |
| Servidor<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[EAPHost e esquema herdado](eaphost-schemas.md)
</dt> <dt>

[Esquema baseeapconnectionpropertiesv1](baseeapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





