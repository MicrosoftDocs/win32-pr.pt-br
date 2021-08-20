---
description: Emitido por um IFilter de contêiner para cada URL filho dentro do contêiner. Os filhos eventualmente serão rastreados pelo indexador se eles estão dentro do escopo.
ms.assetid: e864b3fa-6d43-40fe-9556-474953098947
title: System.Search.UrlToIndex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb964f146831561174f3713d5b827a2c736c59f93e034ac8494f86a0fc6584bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117864762"
---
# <a name="systemsearchurltoindex"></a>System.Search.UrlToIndex

Emitido por um [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) de contêiner para cada URL filho dentro do contêiner. Os filhos eventualmente serão rastreados pelo indexador se eles estão dentro do escopo.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.Search.UrlToIndex
   shellPKey = PKEY_Search_UrlToIndex
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 2
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
```

## <a name="remarks"></a>Comentários

Essa propriedade contém uma URL e é emitida por um manipulador de protocolo para cada URL filho ou directoy na URL atual. O indexador chama de volta para o manipulador de protocolo e solicita que esse documento seja indexado. [System.Search.UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)) era chamado dirLINK PID GTHR em versões anteriores do \_ \_ Windows operacional.

Os valores PKEY são definidos em Propkey.h.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System.Search.UrlToIndexWithModificationTime](./props-system-search-urltoindexwithmodificationtime.md)
</dt> <dt>

[Propertydescription](./propdesc-schema-propertydescription.md)
</dt> <dt>

[searchInfo](./propdesc-schema-searchinfo.md)
</dt> <dt>

[labelInfo](./propdesc-schema-labelinfo.md)
</dt> <dt>

[Typeinfo](./propdesc-schema-typeinfo.md)
</dt> <dt>

[displayInfo](./propdesc-schema-displayinfo.md)
</dt> <dt>

[Stringformat](./propdesc-schema-stringformat.md)
</dt> <dt>

[booleanFormat](./propdesc-schema-booleanformat.md)
</dt> <dt>

[Numberformat](./propdesc-schema-numberformat.md)
</dt> <dt>

[dateTimeFormat](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[enumeratedList](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[drawControl](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[editControl](./propdesc-schema-editcontrol.md)
</dt> <dt>

[Filtercontrol](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[queryControl](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
