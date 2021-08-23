---
title: Elemento metadata (instrumentationManifest)
description: Contém valores globais que você pode referenciar em outros manifestos.
ms.assetid: 5bf3bb1e-47c9-4d6e-86e3-3316e21b76b3
keywords:
- Elemento de metadados EventLog
topic_type:
- apiref
api_name:
- metadata
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eaa22cc13c611b90ace42a2a71517fe0771d6e9ed03d6d964f11a4e4c93cda43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136319"
---
# <a name="metadata-instrumentationmanifest-element"></a>Elemento metadata (instrumentationManifest)

Contém valores globais que você pode referenciar em outros manifestos. Para ver um exemplo, consulte o arquivo Winmeta.xml incluído na \\ pasta Incluir do SDK do Windows.

``` syntax
<xs:element name="metadata"
    type="MetadataType"
 />
```

O **elemento de** metadados é definido pelo elemento [**instrumentationManifest.**](eventmanifestschema-instrumentationmanifest-element.md)

## <a name="remarks"></a>Comentários

Embora você possa criar um manifesto que contém uma seção de metadados, o serviço não o usará; os únicos metadados que o serviço reconhece são os metadados encontrados no arquivo Winmeta.xml dados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Elemento pai**
</dt> <dt>

[**instrumentationManifest**](eventmanifestschema-instrumentationmanifest-element.md)
</dt> </dl>

 

 





