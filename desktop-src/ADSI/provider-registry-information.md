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
# <a name="provider-registry-information"></a><span data-ttu-id="af4d1-103">Informações de registro do provedor</span><span class="sxs-lookup"><span data-stu-id="af4d1-103">Provider Registry Information</span></span>

<span data-ttu-id="af4d1-104">O provedor é registrado com ADSI com as seguintes chaves e valores:</span><span class="sxs-lookup"><span data-stu-id="af4d1-104">The provider is registered with ADSI with the following keys and values:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         ADs
            Providers
               provider = <provider namespace>
```

<span data-ttu-id="af4d1-105">O provedor é registrado com o Windows com as seguintes chaves e valores:</span><span class="sxs-lookup"><span data-stu-id="af4d1-105">The provider is registered with Windows with the following keys and values:</span></span>

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

<span data-ttu-id="af4d1-106">O namespace do provedor é registrado com o Windows com as seguintes chaves e valores:</span><span class="sxs-lookup"><span data-stu-id="af4d1-106">The provider namespace is registered with Windows with the following keys and values:</span></span>

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

<span data-ttu-id="af4d1-107">Nos parágrafos anteriores, o *provedor* é o identificador do objeto de nível superior do provedor.</span><span class="sxs-lookup"><span data-stu-id="af4d1-107">In the previous paragraphs, the *provider* is the identifier of the provider's top-level object.</span></span> <span data-ttu-id="af4d1-108">O *namespace do provedor* é o identificador do objeto que implementa o namespace do provedor.</span><span class="sxs-lookup"><span data-stu-id="af4d1-108">The *provider namespace* is the identifier of the object which implements the provider's namespace.</span></span>

<span data-ttu-id="af4d1-109">Para obter um exemplo específico, consulte [instalando o componente de provedor de exemplo](installing-the-example-provider-component.md).</span><span class="sxs-lookup"><span data-stu-id="af4d1-109">For a specific example, see [Installing the Example Provider Component](installing-the-example-provider-component.md).</span></span>

 

 




