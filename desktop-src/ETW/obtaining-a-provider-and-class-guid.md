---
description: Para obter GUIDs de classe de guid ou de rastreamento de evento do provedor, você pode usar a ferramenta Uuidgen.exe ou Guidgen.exe eventos.
ms.assetid: 07483a78-ee67-4586-a75b-d376aa3351b7
title: Obtendo um provedor e um GUID de classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c480a45a5a826d3f258ab267e39db87bc85fad799fef5d7397a7c900f4872f22
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914346"
---
# <a name="obtaining-a-provider-and-class-guid"></a>Obtendo um provedor e um GUID de classe

Para obter GUIDs de classe de guid ou de rastreamento de evento do provedor, você pode usar a ferramenta Uuidgen.exe ou Guidgen.exe eventos.

Se você usar a Uuidgen.exe, use a opção -d para criar uma \_ macro DEFINE GUID C, conforme mostrado no exemplo a seguir. Para obter informações sobre como usar a Uuidgen.exe, use -? opção. Se você usar a macro DEFINIR GUID C para definir seu GUID, deverá incluir \_ definir INITGUID antes de suas definições de GUID, conforme \# mostrado no exemplo a seguir.

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

O Microsoft Windows SDK (Software Development Kit) e o Microsoft Visual Studio incluem a Guidgen.exe software. A Guidgen.exe tem uma interface do usuário que permite selecionar entre vários formatos. Você deve usar o formato que cria um GUID constante estático, conforme mostrado no exemplo a seguir.

``` syntax
// {7C214FB1-9CAC-4b8d-BAED-7BF48BF63BB3}
static const GUID ProviderGuid = 
{ 0x7c214fb1, 0x9cac, 0x4b8d, { 0xba, 0xed, 0x7b, 0xf4, 0x8b, 0xf6, 0x3b, 0xb3 } };
```

 

 



