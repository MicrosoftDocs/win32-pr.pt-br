---
title: Elemento Config (EapHostConfig)
description: É usado quando a configuração do método está em formato de texto XML em vez de um BLOB binário.
ms.assetid: f47bec23-745f-47db-84db-2556beb6a9e9
keywords:
- Elemento Config EAPHost
topic_type:
- apiref
api_name:
- Config
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ba798afaa418e5de49c48abdc8dac242a300a7228ffe27a76241f4cbabed5833
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739076"
---
# <a name="config-eaphostconfig-element"></a>Elemento Config (EapHostConfig)

O **elemento Config (EapHostConfig)** é usado quando a configuração do método está no formato de texto XML em vez de um BLOB binário.

``` syntax
<xs:element name="Config"
    type="BaseEapMethodConfig"
 />
```

O **elemento Config** é definido pelo [**elemento EapHostConfig.**](eaphostconfigschema-eaphostconfig-element.md)

## <a name="remarks"></a>Comentários

Os **elementos Config** e [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) não podem ser usados simultaneamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Contexto de definição do elemento no esquema**
</dt> <dt>

[**EapHostConfig**](eaphostconfigschema-eaphostconfig-element.md)
</dt> <dt>

**Possível elemento pai imediato na instância de esquema**
</dt> <dt>

[**EapHostConfig**](eaphostconfigschema-eaphostconfig-element.md)
</dt> <dt>

[EAPHost e esquema herdado](eaphost-schemas.md)
</dt> <dt>

[Esquema eaphostconfig](eaphostconfigschema-schema.md)
</dt> </dl>

 

 





