---
description: Essa propriedade representa um status de compartilhamento mais permissivo para o arquivo/pasta especificado pelo provedor de armazenamento. Os status de compartilhamento da maioria para menos permissiva são Propriedade de > > Público > Compartilhado > Private.StorageProviderSharingStatus é uma propriedade readonly.
ms.assetid: c3b93159-4279-4b27-b006-ab73e0beee9c
title: System.StorageProviderSharingStatus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cde6e48cd8870e23801b8cccd8340f8146305ec5d350d71f9ccb27893530c22a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119095663"
---
# <a name="systemstorageprovidersharingstatus"></a>System.StorageProviderSharingStatus

Essa propriedade representa um status de compartilhamento mais permissivo para o arquivo/pasta especificado pelo provedor de armazenamento. Os status de compartilhamento da maioria para menos permissiva são Propriedade de > > Público > Compartilhado > Private.StorageProviderSharingStatus é uma propriedade readonly.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81"></a>Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1

```
propertyDescription
   name = System.StorageProviderSharingStatus
   shellPKey = PKEY_StorageProviderSharingStatus
   formatID = FCEFF153-E839-4CF3-A9E7-EA22832094B8
   propID = 117
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt32
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = NotShared
            value = 0
            text
            defineToken = STORAGE_PROVIDER_SHARINGSTATUS_NOTSHARED
         enum
            name = Shared
            value = 1
            text = Shared
            defineToken = STORAGE_PROVIDER_SHARINGSTATUS_SHARED
         enum
            name = Private
            value = 2
            text
            defineToken = STORAGE_PROVIDER_SHARINGSTATUS_PRIVATE
         enum
            name = Public
            value = 3
            text = Public
            defineToken = STORAGE_PROVIDER_SHARINGSTATUS_PUBLIC
         enum
            name = SharedOwned
            value = 4
            text = Shared (co-owned, owner)
            defineToken = STORAGE_PROVIDER_SHARINGSTATUS_SHARED_OWNED
         enum
            name = SharedCoOwned
            value = 5
            text = Shared (co-owned)
            defineToken = STORAGE_PROVIDER_SHARINGSTATUS_SHARED_COOWNED
         enum
            name = PublicOwned
            value = 6
            text = Public (co-owned, owner)
            defineToken = STORAGE_PROVIDER_SHARINGSTATUS_PUBLIC_OWNED
         enum
            name = PublicCoOwned
            value = 7
            text = Public (co-owned)
            defineToken = STORAGE_PROVIDER_SHARINGSTATUS_PUBLIC_COOWNED
```

## <a name="remarks"></a>Comentários

Os valores PKEY são definidos em Propkey.h.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

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

 

 
