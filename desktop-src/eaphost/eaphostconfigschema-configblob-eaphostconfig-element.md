---
title: Elemento ConfigBlob (EapHostConfig)
description: É usado quando a configuração do método está no formato BLOB binário em vez do formato de cadeia de caracteres de texto.
ms.assetid: 2820e0b8-2cd1-40e8-ac0c-a62e73ac3847
keywords:
- Elemento ConfigBlob EAPHost
topic_type:
- apiref
api_name:
- ConfigBlob
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8f0d3b928ebc6cd24a6d7102ea37a8d0ae980c54499f568d25ca224b1121a20b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021636"
---
# <a name="configblob-eaphostconfig-element"></a>Elemento ConfigBlob (EapHostConfig)

O **elemento ConfigBlob (EapHostConfig)** é usado quando a configuração do método está no formato BLOB binário em vez do formato de cadeia de caracteres de texto.

``` syntax
<xs:element name="ConfigBlob"
    type="hexBinary"
 />
```

O **elemento ConfigBlob** é definido pelo [**elemento EapHostConfig.**](eaphostconfigschema-eaphostconfig-element.md)

## <a name="remarks"></a>Comentários

Os [**elementos Config**](eaphostconfigschema-config-eaphostconfig-element.md) e **ConfigBlob** não podem ser usados simultaneamente.

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

 

 





