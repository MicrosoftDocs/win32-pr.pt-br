---
title: NONREDIST
description: Adiciona nomes à lista de arquivos que não devem ser exportados quando aplicativos COM+ são empacotados para instalação em outros computadores. Observe que essa é uma subchave, não um valor.
ms.assetid: c50e20e4-1a25-4978-ab84-8f7b4b2f6069
keywords:
- COM valor do registro NONREDIST COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d537208ecaf98cec46591966e4ae7d9c205850a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006209"
---
# <a name="nonredist"></a>NONREDIST

Adiciona nomes à lista de arquivos que não devem ser exportados quando aplicativos COM+ são empacotados para instalação em outros computadores. Observe que essa é uma subchave, não um valor.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   NONREDIST
      name1
      name2
```

## <a name="remarks"></a>Comentários

Os arquivos que você adiciona à lista são representados por pares de nome/valor armazenados nessa chave. Em cada par de nome/valor, o nome é o nome do arquivo e o valor é reservado.

 

 




