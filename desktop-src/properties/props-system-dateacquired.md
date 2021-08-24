---
description: A data de aquisição do arquivo ou da mídia.
ms.assetid: 7c673d21-5243-4e41-91df-c5d84aaf620a
title: System. DateAcquired
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1a78ae9ccfe938551ab6c4a265972e48c3aad1c1791f02cfa933c583c6d4b0d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119599176"
---
# <a name="systemdateacquired"></a>System. DateAcquired

A data de aquisição do arquivo ou da mídia. Essa propriedade está relacionada a um usuário ou grupo de usuários específico. Por exemplo, esses dados são usados como o principal eixo de classificação para a pasta virtual **nova música**, o que permite às pessoas procurar as últimas adições à sua coleção.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.DateAcquired
   shellPKey = PKEY_DateAcquired
   formatID = 2CBAA8F5-D81F-47CA-B17A-F8D822300131
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = DateTime
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.DateAcquired
   shellPKey = PKEY_DateAcquired
   formatID = 2CBAA8F5-D81F-47CA-B17A-F8D822300131
   propID = 100
   SearchInfo
      IsColumn = true
   typeInfo
      type = DateTime
```

## <a name="remarks"></a>Comentários

Os valores de PKEY são definidos em Propkey. h.

[DateAcquired]() é armazenado como um valor no fluxo principal do arquivo, mas talvez nem sempre esteja presente. Nessas instâncias, a data de aquisição pode ser aproximada com base em outras datas conhecidas para o conteúdo. O manipulador de metadados deve usar um conjunto de regras para determinar a data a ser retornada. O exemplo a seguir demonstra isso para arquivos de música.

-   Para música adquirida, o tempo de criação do arquivo deve ser usado se nenhuma data de aquisição estiver presente. No entanto, o provedor de download deve definir a propriedade [DateAcquired]() no arquivo.
-   Para arquivos de música que o usuário ou o grupo "copiou" (copiando música ou vídeo de um CD ou DVD para um disco rígido), a data de aquisição deve ser a data em que a ação foi realizada. Por exemplo, o atributo [WM/encodingtime](../wmp/wm-encodingtime-attribute.md) .
-   Para música copiada de outro local, a hora de criação do arquivo deve ser usada como a data de aquisição.

Exemplos de [System. DateAcquired]() são a data e a hora em que as imagens são adquiridas de uma câmera ou quando a música é comprada online. Isso não é o mesmo que [System. DateImported](./props-system-dateimported.md).

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

 

 
