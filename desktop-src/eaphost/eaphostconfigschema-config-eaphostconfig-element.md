---
title: Elemento config (EapHostConfig)
description: É usado quando a configuração do método está no formato de texto XML em vez de em um BLOB binário.
ms.assetid: f47bec23-745f-47db-84db-2556beb6a9e9
keywords:
- Elemento de configuração EAPHost
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
ms.openlocfilehash: a81c90063a57a9d55d8ab6d9c18486315c187f0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455297"
---
# <a name="config-eaphostconfig-element"></a>Elemento config (EapHostConfig)

O elemento **config (EapHostConfig)** é usado quando a configuração do método está no formato de texto XML em vez de em um blob binário.

``` syntax
<xs:element name="Config"
    type="BaseEapMethodConfig"
 />
```

O elemento **config** é definido pelo elemento [**EapHostConfig**](eaphostconfigschema-eaphostconfig-element.md) .

## <a name="remarks"></a>Comentários

Os elementos **config** e [**ConfigBlob**](eaphostconfigschema-configblob-eaphostconfig-element.md) não podem ser usados simultaneamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



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

 

 





