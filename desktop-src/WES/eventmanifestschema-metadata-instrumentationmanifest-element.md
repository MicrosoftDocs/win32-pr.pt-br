---
title: Elemento Metadata (instrumentationManifest)
description: Contém valores globais que você pode referenciar em outros manifestos.
ms.assetid: 5bf3bb1e-47c9-4d6e-86e3-3316e21b76b3
keywords:
- EventLog de elemento de metadados
topic_type:
- apiref
api_name:
- metadata
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c14dc8772dee66fcce9ff07e9918c11b463aa414
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085189"
---
# <a name="metadata-instrumentationmanifest-element"></a>Elemento Metadata (instrumentationManifest)

Contém valores globais que você pode referenciar em outros manifestos. Para obter um exemplo, consulte o arquivo Winmeta.xml incluído na \\ pasta include do SDK do Windows.

``` syntax
<xs:element name="metadata"
    type="MetadataType"
 />
```

O elemento de **metadados** é definido pelo elemento [**instrumentationManifest**](eventmanifestschema-instrumentationmanifest-element.md) .

## <a name="remarks"></a>Comentários

Embora você possa criar um manifesto que contenha uma seção de metadados, o serviço não o usará; os únicos metadados que o serviço reconhece são os metadados encontrados no arquivo de Winmeta.xml.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Elemento pai**
</dt> <dt>

[**instrumentationManifest**](eventmanifestschema-instrumentationmanifest-element.md)
</dt> </dl>

 

 





