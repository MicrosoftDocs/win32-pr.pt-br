---
title: Elemento EapType (propriedades base do usuário)
description: Saiba mais sobre o elemento EapType. Esse elemento captura a configuração específica do método dentro do elemento Eap. | Elemento EapType (propriedades base do usuário)
ms.assetid: 8ce81848-5b36-441f-967d-02c666ba5c6c
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
ms.openlocfilehash: 7d9cb6afe13b8c0060b26edbf5add618c776518b3b03e5abdc1f9131dbbcabde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118275529"
---
# <a name="eaptype-element-base-user-properties"></a>Elemento EapType (propriedades base do usuário)

O **elemento EapType** captura a configuração específica do método dentro do elemento Eap.

``` syntax
<xs:element name="EapType"
    type="BaseEapTypeParameters"
 />
```

## <a name="remarks"></a>Comentários

O **elemento EapType** é abstrato; cada método deve definir e usar um elemento derivado nos documentos de instância.

## <a name="requirements"></a>Requisitos



| Função | Versão mínima do sistema operacional com suporte |
|-------------------------------------|------------------------------------------------------|
| Cliente<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[EAPHost e esquema herdado](eaphost-schemas.md)
</dt> <dt>

[Esquema baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





