---
description: Os exemplos a seguir usam a função SetStringInBlob para criar entradas de BLOB especiais.
ms.assetid: 4a921b0d-9934-48e2-8837-be0bd7b7fa7a
title: Entradas de BLOB especiais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cfc40029e0a0f88c2f7bd242881b0d750a5dfa1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647318"
---
# <a name="special-blob-entries"></a><span data-ttu-id="733fa-103">Entradas de BLOB especiais</span><span class="sxs-lookup"><span data-stu-id="733fa-103">Special BLOB Entries</span></span>

<span data-ttu-id="733fa-104">Os exemplos a seguir usam a função [**SetStringInBlob**](setstringinblob.md) para criar entradas de blob especiais.</span><span class="sxs-lookup"><span data-stu-id="733fa-104">The following examples use the [**SetStringInBlob**](setstringinblob.md) function to create special BLOB entries.</span></span>

## <a name="npp-name"></a><span data-ttu-id="733fa-105">Nome do NPP</span><span class="sxs-lookup"><span data-stu-id="733fa-105">NPP Name</span></span>

``` syntax
SetStringInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_LOCATION,
   TAG_NAME,
   "My NPP Name"); 
```

## <a name="npp-class-identifier"></a><span data-ttu-id="733fa-106">Identificador de classe NPP</span><span class="sxs-lookup"><span data-stu-id="733fa-106">NPP Class Identifier</span></span>

``` syntax
SetClassIDInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_LOCATION,
   TAG_CLASSID,
   &CLSID_ThisNPP);
```

## <a name="cfgproc-procedure-name"></a><span data-ttu-id="733fa-107">Nome do procedimento CFGPROC</span><span class="sxs-lookup"><span data-stu-id="733fa-107">CFGPROC Procedure Name</span></span>

``` syntax
SetStringInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_FINDER,
   TAG_PROCNAME,
   "MyGetNPPBlobs");
```

## <a name="tree-root-name-for-finder-ui"></a><span data-ttu-id="733fa-108">Nome raiz da árvore para a interface do usuário do localizador</span><span class="sxs-lookup"><span data-stu-id="733fa-108">Tree Root Name for Finder UI</span></span>

``` syntax
SetStringInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_FINDER,
   TAG_ROOT,
   "My Tree Root name");
```

## <a name="display-string-for-finder-ui"></a><span data-ttu-id="733fa-109">Exibir cadeia de caracteres para a interface do usuário do Finder</span><span class="sxs-lookup"><span data-stu-id="733fa-109">Display String for Finder UI</span></span>

``` syntax
SetStringInBlob(
   hBlob,
   OWNER_NPP,
   CATEGORY_FINDER,
   TAG_DISP_STRING,
   "Double click to select my UI");
```

## <a name="interface-tags"></a><span data-ttu-id="733fa-110">Marcas de interface</span><span class="sxs-lookup"><span data-stu-id="733fa-110">Interface Tags</span></span>

<span data-ttu-id="733fa-111">Este exemplo inclui todas as interfaces suportadas pelo NPP.</span><span class="sxs-lookup"><span data-stu-id="733fa-111">This example includes every interface supported by the NPP.</span></span>

``` syntax
SetBoolInBlob(  
   hBlob,
   OWNER_NPP,
   CATEGORY_CONFIG,
   TAG_INTERFACE_REALTIME_CAPTURE,
   TRUE);
```

 

 



