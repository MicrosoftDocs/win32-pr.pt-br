---
title: Elemento EAP (Propriedade User)
description: Saiba mais sobre o elemento EAP. Esse elemento captura o tipo de método selecionado e a configuração específica do método. | Elemento EAP (Propriedade User)
ms.assetid: 4adef133-1d18-444a-baa3-5419b8cbe298
keywords:
- Elemento EAP EAPHost
topic_type:
- apiref
api_name:
- Eap
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 23f00b5162ddb42efd9fae759bab1ea47efc04dc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105787740"
---
# <a name="eap-element-user-property"></a>Elemento EAP (Propriedade User)

O elemento **EAP** captura o tipo de método selecionado e a configuração específica do método.

``` syntax
<xs:element name="Eap"
    type="BaseEapParameters"
 />
```

## <a name="remarks"></a>Comentários

O método pode definir os elementos constituintes dentro do elemento **EAP** . O método também executa a validação de esquema nos elementos no **EAP**.

## <a name="requirements"></a>Requisitos



| Função | Versão mínima do sistema operacional com suporte |
|------|------------------------------|
| Cliente<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[EAPHost e esquema herdado](eaphost-schemas.md)
</dt> <dt>

[Esquema baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





