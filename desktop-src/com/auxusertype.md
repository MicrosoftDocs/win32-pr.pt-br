---
title: AuxUserType
description: Especifica o nome de exibição curto de um aplicativo e os nomes de aplicativos.
ms.assetid: 3367eb68-01f4-4cb9-b1d0-27554c28b68d
keywords:
- AuxUserType de chave do registro COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c66fcfbcdc2886e93d08040659b39c42d47c291
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634746"
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

 

 




