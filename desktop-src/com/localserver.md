---
title: LocalServer
description: Especifica o caminho completo para um aplicativo de servidor local de 16 bits.
ms.assetid: 6eadadd5-f4d3-4e0d-9491-2ea366861aa7
keywords:
- COM da chave do registro LocalServer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7413f9d7c4d17e9498e80d19b70192fbb21911b6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005862"
---
# <a name="localserver"></a>LocalServer

Especifica o caminho completo para um aplicativo de servidor local de 16 bits.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      LocalServer = path
```

## <a name="remarks"></a>Comentários

Esse é um valor de **\_ sz de reg** que especifica o caminho completo e pode incluir qualquer argumento de linha de comando.

COM anexa o sinalizador "-incorporando" à cadeia de caracteres, portanto, o aplicativo que usa sinalizadores deve analisar toda a cadeia de caracteres e verificar o sinalizador de incorporação.

Para executar um servidor de objetos COM em um espaço de memória separado, altere o valor de **LocalServer** da seguinte maneira:

**cmd/c iniciar** *caminho do/separate * * *. exe**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**LocalServer32**](localserver32.md)
</dt> </dl>

 

 




