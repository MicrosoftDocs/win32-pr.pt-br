---
title: NONREDIST
description: Adiciona nomes à lista de arquivos que não devem ser exportados quando aplicativos COM+ são empacotados para instalação em outros computadores. Observe que essa é uma sub-chave, não um valor.
ms.assetid: c50e20e4-1a25-4978-ab84-8f7b4b2f6069
keywords:
- Valor do Registro NONREDIST COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b303c145ea48a51f72d6ee21078b5f29a6b6d4fabc7184d4a37e980a2bbb2e4b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678456"
---
# <a name="nonredist"></a>NONREDIST

Adiciona nomes à lista de arquivos que não devem ser exportados quando aplicativos COM+ são empacotados para instalação em outros computadores. Observe que essa é uma sub-chave, não um valor.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   NONREDIST
      name1
      name2
```

## <a name="remarks"></a>Comentários

Os arquivos que você adiciona à lista são representados por pares de nome/valor armazenados nessa chave. Em cada par nome/valor, o nome é o nome do arquivo e o valor é reservado.

 

 




