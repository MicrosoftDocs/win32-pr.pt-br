---
title: Descarregamento de IAgent
description: Descarregamento de IAgent
ms.assetid: 560301b3-c038-4c6e-b3f1-1203b618b67d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc30d6c4c06c1d292a26a2f503477dcca651dd18
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104294031"
---
# <a name="iagentunload"></a>IAgent:: UnLoad

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

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


 

 