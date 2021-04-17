---
title: Elemento EapType (Propriedades de usuário base)
description: Saiba mais sobre o elemento EapType. Esse elemento captura a configuração específica do método dentro do elemento EAP. | Elemento EapType (Propriedades de usuário base)
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
ms.openlocfilehash: 5fffa74c69b5ecbf2823cfa79ae376fed524e8ca
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105766475"
---
# <a name="eaptype-element-base-user-properties"></a>Elemento EapType (Propriedades de usuário base)

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
|-------------------------------------|------------------------------------------------------|
| Cliente<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[EAPHost e esquema herdado](eaphost-schemas.md)
</dt> <dt>

[Esquema baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





