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
# <a name="obtaining-a-provider-and-class-guid"></a>Obtendo um provedor e um GUID de classe

Para obter um GUID de provedor ou GUIDs de classe de rastreamento de eventos, você pode usar a ferramenta Uuidgen.exe ou Guidgen.exe.

Se você usar a ferramenta Uuidgen.exe, use a opção-d para criar uma \_ macro definir GUID C, conforme mostrado no exemplo a seguir. Para obter informações sobre como usar a ferramenta de Uuidgen.exe, use o-? opção. Se você usar a \_ macro definir GUID C para definir o GUID, deverá incluir \# definir Initguid antes das definições de GUID, conforme mostrado no exemplo a seguir.

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

O SDK (Software Development Kit) do Microsoft Windows e o Microsoft Visual Studio incluem a ferramenta Guidgen.exe. A ferramenta de Guidgen.exe tem uma interface do usuário que permite que você selecione vários formatos. Você deve usar o formato que cria um GUID de constante estática, como mostrado no exemplo a seguir.

``` syntax
// {7C214FB1-9CAC-4b8d-BAED-7BF48BF63BB3}
static const GUID ProviderGuid = 
{ 0x7c214fb1, 0x9cac, 0x4b8d, { 0xba, 0xed, 0x7b, 0xf4, 0x8b, 0xf6, 0x3b, 0xb3 } };
```

 

 



