---
title: Elemento EAP (Propriedades de conexão)
description: Saiba mais sobre o elemento EAP. Esse elemento captura o tipo de método selecionado e a configuração específica do método. | Elemento EAP (Propriedades de conexão)
ms.assetid: 4e9f3869-257e-4b03-93f6-2eec94eaacee
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
ms.openlocfilehash: c39812d00ecf9a1183eb81fc03b09b146d751f0e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105790506"
---
# <a name="eap-element-connection-properties"></a>Elemento EAP (Propriedades de conexão)

O elemento **EAP** captura o tipo de método selecionado e a configuração específica do método.

``` syntax
<xs:element name="Eap
          
        "
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

[Esquema baseeapconnectionpropertiesv1](baseeapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





