---
description: Emitido como verdadeiro por todos os itens filho de um contêiner (como um email ou um arquivo compactado com uma extensão de nome .zip) que emite System. Search. IsClosedDirectory como TRUE. Isso garante que os itens filho sejam incluídos no índice de pesquisa.
ms.assetid: 6da60e89-6956-41f6-8624-063c4d46464d
title: System. Search. IsFullyContained
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ce7f325be26abdb81dcb51da7018f6da786e6ec5f3a31111e4ae3823acf8c78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117864985"
---
# <a name="systemsearchisfullycontained"></a>System. Search. IsFullyContained

Emitido como **verdadeiro** por todos os itens filho de um contêiner (como um email ou um arquivo compactado com uma extensão de nome .zip) que emite [System. Search. IsClosedDirectory](./props-system-search-iscloseddirectory.md) como **true**. Isso garante que os itens filho sejam incluídos no índice de pesquisa.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.Search.IsFullyContained
   shellPKey = PKEY_Search_IsFullyContained
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 24
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
```

## <a name="remarks"></a>Comentários

Os valores de PKEY são definidos em Propkey. h.

A propriedade [System. Search. IsClosedDirectory](./props-system-search-iscloseddirectory.md) ajuda a otimizar o desempenho do indexador, permitindo que o indexador ignore a enumeração dos itens filho de um contêiner. No entanto, esses itens filhos são marcados pelo indexador como não visitado e, como tal, serão excluídos do índice. Emitindo [System. Search. IsFullyContained]() como **true**, um item não é excluído do índice, apesar de não ter sido visitado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[propertyDescription](./propdesc-schema-propertydescription.md)
</dt> <dt>

[searchInfo](./propdesc-schema-searchinfo.md)
</dt> <dt>

[labelInfo](./propdesc-schema-labelinfo.md)
</dt> <dt>

[typeInfo](./propdesc-schema-typeinfo.md)
</dt> <dt>

[displayInfo](./propdesc-schema-displayinfo.md)
</dt> <dt>

[stringFormat](./propdesc-schema-stringformat.md)
</dt> <dt>

[booleanFormat](./propdesc-schema-booleanformat.md)
</dt> <dt>

[numberFormat](./propdesc-schema-numberformat.md)
</dt> <dt>

[dateTimeFormat](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[enumeratedList](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[drawControl](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[editControl](./propdesc-schema-editcontrol.md)
</dt> <dt>

[filterControl](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[queryControl](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
