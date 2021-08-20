---
title: Elemento Eap (propriedades de conexão)
description: Saiba mais sobre o elemento Eap. Esse elemento captura o tipo de método selecionado e a configuração específica do método. | Elemento Eap (propriedades de conexão)
ms.assetid: 4e9f3869-257e-4b03-93f6-2eec94eaacee
keywords:
- Elemento Eap EAPHost
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
ms.openlocfilehash: 7750bdb9a5f3c2d6c187b0f765eeb9d7ad88c015403719c16d0b683637b10027
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118086940"
---
# <a name="eap-element-connection-properties"></a>Elemento Eap (propriedades de conexão)

O **elemento Eap** captura o tipo de método selecionado e a configuração específica do método.

``` syntax
<xs:element name="Eap
          
        "
    type="BaseEapParameters"
 />
```

## <a name="remarks"></a>Comentários

O método pode definir os elementos constituintes dentro do **elemento Eap.** O método também executa a validação de esquema nos elementos no **Eap**.

## <a name="requirements"></a>Requisitos



| Função | Versão mínima do sistema operacional com suporte |
|------|------------------------------|
| Cliente<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[EAPHost e esquema herdado](eaphost-schemas.md)
</dt> <dt>

[Esquema baseeapconnectionpropertiesv1](baseeapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





