---
title: Informações do Registro do Provedor
description: Este tópico mostra quais chaves e valores precisam ser definidos ao adicionar um provedor ADSI.
ms.assetid: 87293b63-03ad-4be9-b327-313fdebac611
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 813ad37d77d532e3c9bec91bcc3eda1f0aaf703f09dd3cf1b61ac059d7d7493b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838862"
---
# <a name="provider-registry-information"></a>Informações do Registro do Provedor

O provedor é registrado com ADSI com as seguintes chaves e valores:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         ADs
            Providers
               provider = <provider namespace>
```

O provedor é registrado com Windows com as seguintes chaves e valores:

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

O namespace do provedor é registrado com Windows com as seguintes chaves e valores:

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

Para um exemplo específico, consulte [Instalando o componente de provedor de exemplo](installing-the-example-provider-component.md).

 

 




