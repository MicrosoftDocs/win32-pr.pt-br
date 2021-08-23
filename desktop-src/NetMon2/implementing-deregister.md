---
description: Monitor de Rede passa todos os quadros de uma captura para os analisadores e, em seguida, começa a chamar a função Deregister para todos os protocolos que identifica. Cada DLL do analisador deve implementar uma função Deregister para cada protocolo compatível com a DLL do analisador.
ms.assetid: 936d5b00-b0ee-4a29-9396-1e2a7a91a2dd
title: Implementando o desregistro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 444502ba3ab19921a6372d4cda872aed85e879cbbdadc2f0176a7187bfc24491
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890476"
---
# <a name="implementing-deregister"></a>Implementando o desregistro

Monitor de Rede passa todos os quadros de uma captura para os analisadores e, em seguida, começa a chamar a função [**Deregister**](deregister.md) para todos os protocolos que identifica. Cada DLL do analisador deve implementar uma **função Deregister** para cada protocolo compatível com a DLL do analisador.

Cada implementação da função [**Deregister**](deregister.md) deve chamar a função [**DestroyProtocolDatabase**](destroypropertydatabase.md) para liberar os recursos usados para criar o banco de dados.

O procedimento a seguir identifica a única etapa necessária para implementar [**o Desregistro**](deregister.md).

**Para implementar o Deregister para um protocolo**

-   Chame [**DestroyProtocolDatabase para**](destroypropertydatabase.md) liberar os recursos do banco de dados.

A seguir está uma implementação básica [**do Deregister**](deregister.md). Observe que o exemplo de código mostra a versão dos recursos usados para criar um banco de dados de propriedade.

``` syntax
#include <windows.h>

VOID WINAPI MyProtocolDeregister (HPROTOCOL hProtocol)
{
  DestroyPropertyDatabase (hProtocol);
}
```

 

 



