---
title: Informações de registro do provedor
description: Este tópico mostra quais chaves e valores precisam ser definidos ao adicionar um provedor ADSI.
ms.assetid: 87293b63-03ad-4be9-b327-313fdebac611
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 790a80964bdcc6111a4c167056a0b85bda23e147
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363647"
---
# <a name="provider-registry-information"></a>Informações de registro do provedor

O provedor é registrado com ADSI com as seguintes chaves e valores:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         ADs
            Providers
               provider = <provider namespace>
```

O provedor é registrado com o Windows com as seguintes chaves e valores:

```
HKEY_CLASSES_ROOT
   provider
      Clsid
         (Default) = <provider CLSID>
```

```
HKEY_CLASSES_ROOT
   CLSID
      provider CLSID
         (Default) = <friendly display name>
         InProcServer32
            (Default) = <provider DLL filename>
            ThreadingModel = Both
         ProgID = <provider object name>
         TypeLib = <provider TypeLib CLSID>
         Version = <provider version number>
```

O namespace do provedor é registrado com o Windows com as seguintes chaves e valores:

```
HKEY_CLASSES_ROOT
   provider namespace
      Clsid
         (Default) = <provider namespace CLSID>
```

```
HKEY_CLASSES_ROOT
   CLSID
      provider namespace CLSID
         (Default) = <friendly display name>
         InProcServer32
            (Default) = <provider namespace DLL filename>
            ThreadingModel = Both
         ProgID = <provider namespace object name>
         TypeLib = <provider namespace TypeLib CLSID>
         Version = <provider namespace version number>
```

Nos parágrafos anteriores, o *provedor* é o identificador do objeto de nível superior do provedor. O *namespace do provedor* é o identificador do objeto que implementa o namespace do provedor.

Para obter um exemplo específico, consulte [instalando o componente de provedor de exemplo](installing-the-example-provider-component.md).

 

 




