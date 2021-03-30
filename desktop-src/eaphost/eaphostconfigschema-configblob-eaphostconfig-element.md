---
title: Elemento ConfigBlob (EapHostConfig)
description: É usado quando a configuração do método está em formato de BLOB binário em vez de formulário de cadeia de caracteres de texto.
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
ms.openlocfilehash: b220c74c6439b4b2cbb0d05a1d540d673e1bd17b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644198"
---
# <a name="configblob-eaphostconfig-element"></a>Elemento ConfigBlob (EapHostConfig)

O elemento **ConfigBlob (EapHostConfig)** é usado quando a configuração do método está em formato de blob binário em vez de formulário de cadeia de texto.

``` syntax
<xs:element name="ConfigBlob"
    type="hexBinary"
 />
```

O elemento **ConfigBlob** é definido pelo elemento [**EapHostConfig**](eaphostconfigschema-eaphostconfig-element.md) .

## <a name="remarks"></a>Comentários

Os elementos [**config**](eaphostconfigschema-config-eaphostconfig-element.md) e **ConfigBlob** não podem ser usados simultaneamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Consulte também

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

 

 





