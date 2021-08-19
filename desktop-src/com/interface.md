---
title: Interface (COM)
description: Uma entrada opcional que especifica todas as IDs de interface (IIDs) com suporte pela classe associada.
ms.assetid: 212a6500-14ce-4a9b-9e6a-38d83a5630c8
keywords:
- Chave do Registro de interface COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00d8eaa38b97896f623c8d9f245c48f8d12634f930dc193cba14d5a9217a261e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048113"
---
# <a name="interface-com"></a>Interface (COM)

Uma entrada opcional que especifica todas as IDs de interface (IIDs) com suporte pela classe associada.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Interface
         {IID1} = name1
         {IID2} = name2
         ...
```

## <a name="remarks"></a>Comentários

Se um nome de interface não estiver presente nesta lista, a interface nunca poderá ser suportada por uma instância dessa classe.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Chave de Interface](interface-key.md)
</dt> </dl>

 

 




