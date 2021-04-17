---
description: Monitor de Rede passa todos os quadros de uma captura para os analisadores e, em seguida, começa a chamar a função de cancelamento de registro para todos os protocolos que ele identifica. Cada DLL do analisador deve implementar uma função de cancelamento de registro para cada protocolo compatível com a DLL do analisador.
ms.assetid: 936d5b00-b0ee-4a29-9396-1e2a7a91a2dd
title: Implementando cancelamento de registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ee07c5b6b3c746e9c29811332b9e7674e49db26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105747939"
---
# <a name="implementing-deregister"></a>Implementando cancelamento de registro

Monitor de Rede passa todos os quadros de uma captura para os analisadores e, em seguida, começa a chamar a função de [**cancelamento de registro**](deregister.md) para todos os protocolos que ele identifica. Cada DLL do analisador deve implementar uma função de **cancelamento de registro** para cada protocolo compatível com a DLL do analisador.

Cada implementação da função de [**cancelamento de registro**](deregister.md) deve chamar a função [**DestroyProtocolDatabase**](destroypropertydatabase.md) para liberar os recursos que são usados para criar o banco de dados.

O procedimento a seguir identifica a única etapa necessária para implementar o [**cancelamento de registro**](deregister.md).

**Para implementar o cancelamento de registro para um protocolo**

-   Chame [**DestroyProtocolDatabase**](destroypropertydatabase.md) para liberar os recursos do banco de dados.

A seguir está uma implementação básica do [**cancelamento do registro**](deregister.md). Observe que o exemplo de código mostra a versão dos recursos que são usados para criar um banco de dados de propriedade.

``` syntax
#include <windows.h>

VOID WINAPI MyProtocolDeregister (HPROTOCOL hProtocol)
{
  DestroyPropertyDatabase (hProtocol);
}
```

 

 



