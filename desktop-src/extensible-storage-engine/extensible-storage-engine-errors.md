---
description: 'Saiba mais sobre: Erros extensíveis Armazenamento mecanismo'
title: Erros extensíveis Armazenamento mecanismo
TOCTitle: Extensible Storage Engine Errors
ms:assetid: 0c071ed6-0ea2-448b-9f9f-e606c5abf3db
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269184(v=EXCHG.10)
ms:contentKeyID: 32765487
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 0c0ee0a4423d5b37913bd7922af07a7b2196a30176b2a1adca37240e03a28594
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721456"
---
# <a name="extensible-storage-engine-errors"></a>Erros extensíveis Armazenamento mecanismo


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="extensible-storage-engine-errors"></a>Erros extensíveis Armazenamento mecanismo

Todos os erros possíveis retornados pela API ESE (Extensible Armazenamento Engine) são definidos pelo [tipo JET_ERR](./jet-err.md) dados. Para ver uma lista dos sinalizadores de erro definidos para essa API, consulte [Extensible Armazenamento de](./extensible-storage-engine-error-codes.md)erro do mecanismo .

Em toda a documentação da API do ESE, apenas os erros mais importantes são documentados. Esses erros normalmente representam erros de uso de API ou condições de erro muito importantes. Esteja ciente de que qualquer uma dessas APIs de ESE também pode retornar outros erros que não estão documentados para cada API. Nesses casos, o chamador deve simplesmente tratar o erro como faria com qualquer outro erro retornado pela API. O valor de erro específico pode ser usado para fins de diagnóstico, como rastreamento.

Em geral, um valor maior que zero deve ser interpretado como um aviso, um valor de zero deve ser interpretado como êxito e um valor menor que zero deve ser interpretado como um erro. Nenhum outro padrão nesses valores (por exemplo, intervalos de valores) deve ser considerado por um aplicativo.

Quando o ESE encontra alguns dos erros mais sérios, ele cria uma entrada de log de eventos que contém detalhes sobre os erros. O nível de registro em log pode ser controlado pelos [Parâmetros do Log de Eventos](./event-log-parameters.md).

Alguns aplicativos exigem a capacidade [de retornar JET_ERR](./jet-err.md)como HRESULTs. O exemplo C++ a seguir mostra como fazer essa conversão:

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

Para obter informações sobre como configurar parâmetros do sistema para tratamento de erros, consulte [Parâmetros de tratamento de erro](./error-handling-parameters.md).

### <a name="see-also"></a>Consulte Também

[Parâmetros de tratamento de erro](./error-handling-parameters.md)

[Códigos de erro Armazenamento mecanismo extensível](./extensible-storage-engine-error-codes.md)

[JET_ERR](./jet-err.md)
