---
title: Interface (COM)
description: Uma entrada opcional que especifica todas as IDs de interface (IIDs) com suporte pela classe associada.
ms.assetid: 212a6500-14ce-4a9b-9e6a-38d83a5630c8
keywords:
- Chave do registro de interface COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 990c06285d60067c9a26faffabffc70cbdd283d1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105793346"
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

Se um nome de interface não estiver presente nessa lista, a interface nunca poderá ser suportada por uma instância dessa classe.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Chave de Interface](interface-key.md)
</dt> </dl>

 

 




