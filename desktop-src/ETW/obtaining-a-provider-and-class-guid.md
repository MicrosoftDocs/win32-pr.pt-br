---
description: Para obter um GUID de provedor ou GUIDs de classe de rastreamento de eventos, você pode usar a ferramenta Uuidgen.exe ou Guidgen.exe.
ms.assetid: 07483a78-ee67-4586-a75b-d376aa3351b7
title: Obtendo um provedor e um GUID de classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c12554cdb39459d824bf6622cd9d50e52f8c788d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968040"
---
# <a name="obtaining-a-provider-and-class-guid"></a><span data-ttu-id="34939-103">Obtendo um provedor e um GUID de classe</span><span class="sxs-lookup"><span data-stu-id="34939-103">Obtaining a Provider and Class GUID</span></span>

<span data-ttu-id="34939-104">Para obter um GUID de provedor ou GUIDs de classe de rastreamento de eventos, você pode usar a ferramenta Uuidgen.exe ou Guidgen.exe.</span><span class="sxs-lookup"><span data-stu-id="34939-104">To obtain a provider GUID or event trace class GUIDs, you can use the Uuidgen.exe or Guidgen.exe tool.</span></span>

<span data-ttu-id="34939-105">Se você usar a ferramenta Uuidgen.exe, use a opção-d para criar uma \_ macro definir GUID C, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="34939-105">If you use the Uuidgen.exe tool, use the -d option to create a DEFINE\_GUID C macro, as shown in the following example.</span></span> <span data-ttu-id="34939-106">Para obter informações sobre como usar a ferramenta de Uuidgen.exe, use o-?</span><span class="sxs-lookup"><span data-stu-id="34939-106">For information about using the Uuidgen.exe tool, use the -?</span></span> <span data-ttu-id="34939-107">opção.</span><span class="sxs-lookup"><span data-stu-id="34939-107">option.</span></span> <span data-ttu-id="34939-108">Se você usar a \_ macro definir GUID C para definir o GUID, deverá incluir \# definir Initguid antes das definições de GUID, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="34939-108">If you use the DEFINE\_GUID C macro to define your GUID, you must include \#define INITGUID before your GUID definitions, as shown in the following example.</span></span>

``` syntax
#define INITGUID

DEFINE_GUID (
  ProviderGuid,
  0xf4dc272d, 
  0x88dd, 
  0x4472, 
  0xa3, 0xb1, 0xcb, 0x6d, 0xa4, 0x86, 0xf0, 0xbe
  );
```

<span data-ttu-id="34939-109">O SDK (Software Development Kit) do Microsoft Windows e o Microsoft Visual Studio incluem a ferramenta Guidgen.exe.</span><span class="sxs-lookup"><span data-stu-id="34939-109">The Microsoft Windows Software Development Kit (SDK) and Microsoft Visual Studio include the Guidgen.exe tool.</span></span> <span data-ttu-id="34939-110">A ferramenta de Guidgen.exe tem uma interface do usuário que permite que você selecione vários formatos.</span><span class="sxs-lookup"><span data-stu-id="34939-110">The Guidgen.exe tool has a user interface that lets you select from several formats.</span></span> <span data-ttu-id="34939-111">Você deve usar o formato que cria um GUID de constante estática, como mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="34939-111">You should use the format that creates a static constant GUID, as shown in the following example.</span></span>

``` syntax
// {7C214FB1-9CAC-4b8d-BAED-7BF48BF63BB3}
static const GUID ProviderGuid = 
{ 0x7c214fb1, 0x9cac, 0x4b8d, { 0xba, 0xed, 0x7b, 0xf4, 0x8b, 0xf6, 0x3b, 0xb3 } };
```

 

 



