---
description: 'Saiba mais sobre: erros do mecanismo de armazenamento extensível'
title: Erros do mecanismo de armazenamento extensível
TOCTitle: Extensible Storage Engine Errors
ms:assetid: 0c071ed6-0ea2-448b-9f9f-e606c5abf3db
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269184(v=EXCHG.10)
ms:contentKeyID: 32765487
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 55c86d51f44414688897d6450adf214a0478f7d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837363"
---
# <a name="extensible-storage-engine-errors"></a>Erros do mecanismo de armazenamento extensível


_**Aplica-se a:** Windows | Windows Server_

## <a name="extensible-storage-engine-errors"></a>Erros do mecanismo de armazenamento extensível

Todos os erros possíveis retornados pela API do ESE (mecanismo de armazenamento extensível) são definidos pelo tipo de dados [JET_ERR](./jet-err.md) . Para obter uma lista dos sinalizadores de erro definidos para essa API, consulte [códigos de erro do mecanismo de armazenamento extensível](./extensible-storage-engine-error-codes.md).

Em toda a documentação da API do ESE, apenas os erros mais importantes são documentados. Esses erros normalmente representam erros de uso de API ou condições de erro muito importantes. Lembre-se de que qualquer uma dessas APIs ESE também pode retornar outros erros que não estão documentados para cada API. Nesses casos, o chamador deve simplesmente tratar o erro como faria com qualquer outro erro retornado pela API. O valor de erro específico pode então ser usado para fins de diagnóstico, como rastreamento.

Em geral, um valor maior que zero deve ser interpretado como um aviso, um valor de zero deve ser interpretado como êxito e um valor menor que zero deve ser interpretado como um erro. Nenhum outro padrão nesses valores (por exemplo, intervalos de valores) deve ser confiado por um aplicativo.

Quando o ESE encontra alguns dos erros mais graves, ele cria uma entrada de log de eventos que contém detalhes sobre os erros. O nível de registro em log pode ser controlado por [parâmetros de log de eventos](./event-log-parameters.md).

Alguns aplicativos exigem a capacidade de retornar [JET_ERR](./jet-err.md)s como HResults. O exemplo de C++ a seguir mostra como fazer essa conversão:

```cpp
    #ifndef FACILITY_JET_ERR
    #define FACILITY_JET_ERR 0xE5E
    #endif
    #ifndef HRESULT_FROM_JET_ERR
    #define HRESULT_FROM_JET_ERR( __err )
    (
      ( __err ) == JET_errSuccess ?
      S_OK :
      (
        ( __err ) == JET_errOutOfMemory ?
        E_OUTOFMEMORY :
        MAKE_HRESULT
        (
          (
            ( __err ) < 0 ?
            SEVERITY_ERROR :
            SEVERITY_SUCCESS
          ),
          FACILITY_JET_ERR,
          (
            ( __err ) < 0 ?
            -( __err ) :
            ( __err )
          )
          & 0xFFFF
        )
      )
    )
    
    #endif
```

Para obter informações sobre como configurar parâmetros do sistema para tratamento de erros, consulte [parâmetros de tratamento de erros](./error-handling-parameters.md).

### <a name="see-also"></a>Consulte Também

[Parâmetros de tratamento de erros](./error-handling-parameters.md)

[Códigos de erro do mecanismo de armazenamento extensível](./extensible-storage-engine-error-codes.md)

[JET_ERR](./jet-err.md)
