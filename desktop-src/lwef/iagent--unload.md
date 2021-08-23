---
title: Descarregamento de IAgent
description: Descarregamento de IAgent
ms.assetid: 560301b3-c038-4c6e-b3f1-1203b618b67d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20e6e457e2acc33c5b34800b8378d82a50d5c4aa6a139366ca1c0d241f676f9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610136"
---
# <a name="iagentunload"></a>IAgent:: UnLoad

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT UnLoad(
   long * dwCharID  //character ID
);
```

Descarrega os dados de caractere do caractere especificado da coleção de [**caracteres**](/windows/desktop/lwef/the-characters-object) .

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

A ID do caractere.

</dd> </dl>

Use esse método quando não precisar mais de um caractere, para liberar memória usada para armazenar informações sobre o caractere. Se você acessar o caractere novamente, use o método [**Load**](load-method.md) .

## <a name="see-also"></a>Consulte Também

[**IAgent:: Load**](iagent--load.md)


 

 