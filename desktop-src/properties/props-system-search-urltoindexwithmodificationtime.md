---
description: Essa propriedade é a mesma que System.Search.UrlToIndex, exceto que ela inclui a hora em que a URL foi modificada pela última vez.
ms.assetid: 53ca765b-0795-49ab-9946-c3ef101ababd
title: System.Search.UrlToIndexWithModificationTime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7869005084379db1bdf288c6237a420666634c349eee47ca7942af2bb271a39d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118464766"
---
# <a name="systemsearchurltoindexwithmodificationtime"></a>System.Search.UrlToIndexWithModificationTime

Essa propriedade é a mesma [**que System.Search.UrlToIndex,**](props-system-search-urltoindex.md) exceto que ela inclui a hora em que a URL foi modificada pela última vez. Essa é uma otimização para o indexador para que ele não precise chamar novamente no manipulador de protocolo para solicitar essas informações para determinar se o conteúdo precisa ser indexado novamente.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.Search.UrlToIndexWithModificationTime
   shellPKey = PKEY_Search_UrlToIndexWithModificationTime
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 12
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Multivalue Any
```

## <a name="remarks"></a>Comentários

Essa [propriedade System.Search.UrlToIndexWithModificationTime]() é a mesma que a propriedade [System.Search.UrlToIndex,](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)) exceto que você também passa a hora da última modificação do documento. Se a hora da última modificação for a mesma, o indexador assumirá que o documento já está indexado e lançará a notificação. Essa propriedade é um vetor com dois elementos, um **valor \_ LPWSTR de VT** que contém a URL e um **valor \_ filetime de VT** que contém a hora da última modificação.

[System.Search.UrlToIndexWithModificationTime]() era chamado PID GTHR DIRLINK WITH TIME em versões anteriores \_ do sistema operacional Windows sistema \_ \_ \_ operacional.

Os valores PKEY são definidos em Propkey.h.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System.Search.UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85))
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

 

 
