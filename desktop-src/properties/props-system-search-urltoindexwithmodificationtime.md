---
description: Essa propriedade é igual a System. Search. UrlToIndex, exceto pelo fato de que ela inclui a hora em que a URL foi modificada pela última vez.
ms.assetid: 53ca765b-0795-49ab-9946-c3ef101ababd
title: System. Search. UrlToIndexWithModificationTime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fcc83b9796ae2375f10235a08ba0db313fb1958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785262"
---
# <a name="systemsearchurltoindexwithmodificationtime"></a>System. Search. UrlToIndexWithModificationTime

Essa propriedade é igual a [**System. Search. UrlToIndex**](props-system-search-urltoindex.md) , exceto pelo fato de que ela inclui a hora em que a URL foi modificada pela última vez. Essa é uma otimização para o indexador para que ele não precise chamar de volta para o manipulador de protocolo para solicitar essas informações para determinar se o conteúdo precisa ser indexado novamente.

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

Esta propriedade [System. Search. UrlToIndexWithModificationTime]() é a mesma que a propriedade [System. Search. UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)) , exceto que você também passa a hora da última modificação do documento. Se a hora da última modificação for correspondente, o indexador assumirá que o documento já está indexado e lançará a notificação. Essa propriedade é um vetor com dois elementos, um valor de **\_ LPWStr do VT** que contém a URL e um valor de **\_ FILETIME do VT** que contém a hora da última modificação.

[System. Search. UrlToIndexWithModificationTime]() foi chamado \_ de PID GTHR \_ DIRLINK \_ com \_ tempo em versões anteriores do sistema operacional Windows.

Os valores de PKEY são definidos em Propkey. h.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[System. Search. UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85))
</dt> <dt>

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

 

 
