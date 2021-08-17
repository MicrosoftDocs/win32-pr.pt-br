---
title: AuxUserType
description: Especifica o nome de exibição curto de um aplicativo e os nomes de aplicativos.
ms.assetid: 3367eb68-01f4-4cb9-b1d0-27554c28b68d
keywords:
- AuxUserType de chave do registro COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1dbec8e873e6f6cfcb5fdb29468c1f09c0a7a6935280054e129ddac0b49e282
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118550711"
---
# <a name="auxusertype"></a>AuxUserType

Especifica o nome de exibição curto de um aplicativo e os nomes de aplicativos.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      AuxUserType
         2 = ShortDisplayName
         3 = ApplicationName
```

## <a name="remarks"></a>Comentários

O comprimento máximo recomendado para *ShortDisplayName* é de 15 caracteres. Esse nome é usado em menus, incluindo menus pop-up.

*ApplicationName* deve conter o nome real do aplicativo (como "Acme Draw 2,0"). Esse nome é usado no campo **resultados** da caixa de diálogo **colar especial** .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IOleObject:: GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype)
</dt> </dl>

 

 




