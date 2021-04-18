---
description: Emitido como verdadeiro por um item de contêiner para indicar que seus itens filho não precisam ser enumerados por um indexador se o item de contêiner não foi alterado desde o último rastreamento de verificação de índice incremental.
ms.assetid: 8bb487b9-4a51-4a6b-939e-946a8aad85de
title: System. Search. IsClosedDirectory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea97aeb8d0192eea7d71ca65fd0ec109780702f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105814592"
---
# <a name="systemsearchiscloseddirectory"></a>System. Search. IsClosedDirectory

Emitido como **verdadeiro** por um item de contêiner para indicar que seus itens filho não precisam ser enumerados por um indexador se o item de contêiner não foi alterado desde o último rastreamento de verificação de índice incremental. Isso contribui para a otimização do desempenho do indexador. Nesses casos de contêiner (exemplos são um email com anexos ou um arquivo compactado com uma extensão de nome. zip), os itens filho são inseparáveis de seu item pai. Por exemplo, se a propriedade [System. DateModified](./props-system-datemodified.md) de um item contido for alterada, o valor System. DateModified do contêiner será alterado para Matching. Além disso, se um item pai for excluído, todos os itens filho também serão excluídos. Portanto, se o contêiner não tiver sido alterado, o indexador saberá que nada dentro dele foi alterado e não precisa abrir o contêiner para examinar o conteúdo individualmente.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a>Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista

```
propertyDescription
   name = System.Search.IsClosedDirectory
   shellPKey = PKEY_Search_IsClosedDirectory
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 23
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
```

## <a name="remarks"></a>Comentários

Os valores de PKEY são definidos em Propkey. h.

> [!IMPORTANT]
> Se um item emitir **true** para essa propriedade, cada um de seus itens filho deverá emitir a propriedade [System. Search. IsFullyContained](./props-system-search-isfullycontained.md) como **true** para impedir que esses itens sejam excluídos do índice.

 

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

 

 
