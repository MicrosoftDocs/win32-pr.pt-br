---
title: MiscStatus
description: Especifica como criar e exibir um objeto.
ms.assetid: 585b2d1e-3edb-494e-a61e-bbfa6eae2ba1
keywords:
- MiscStatus de chave do registro COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abee49776577df61dc8b7d4e94a0621dfdd8b216
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005746"
---
# <a name="miscstatus"></a>MiscStatus

Especifica como criar e exibir um objeto.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      MiscStatus
         (Default) = value
         aspect = value
```

## <a name="remarks"></a>Comentários

Para obter mais informações, consulte a enumeração [**OLEMISC**](/windows/win32/api/oleidl/ne-oleidl-olemisc) e [**IOleObject:: GetMiscStatus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus).

Se nenhuma subchave correspondente a um DVASPECT for encontrada, o valor padrão de **MiscStatus** será usado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IOleObject::GetMiscStatus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus)
</dt> </dl>

 

 




