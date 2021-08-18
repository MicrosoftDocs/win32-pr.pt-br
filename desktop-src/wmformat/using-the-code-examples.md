---
title: usando os exemplos de código do SDK do formato de mídia Windows
description: usando os exemplos de código do SDK do formato de mídia Windows
ms.assetid: 1459a438-d42c-4d84-baa8-fc672f5d5d27
keywords:
- Windows SDK do formato de mídia, exemplos de código
- Windows SDK do formato de mídia, código de exemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba6a5b6718bf7665d04fedb5d5a0bad473a632cbeeabdfd756a52877ccdc84ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963935"
---
# <a name="using-the-windows-media-format-sdk-code-examples"></a>usando os exemplos de código do SDK do formato de mídia Windows

Muitas das seções explicativas deste SDK incluem exemplos de código. Os exemplos são escritos para serem tão claros e concisos quanto possível. Ao ler os exemplos, você deve estar ciente das convenções a seguir.

-   Todos os exemplos são presumidos para incluir Windows. h e WMSDK. h. Quaisquer outros arquivos de cabeçalho necessários são mencionados no texto explicativo.
-   A verificação de erros foi restrita à interrupção da função se ocorrer um erro. Em um aplicativo, você deve verificar se há códigos de erro específicos e fornecer algum tipo de relatório de erros.

    Ao verificar valores de retorno de métodos ou funções que retornam um valor **HRESULT** , você deve usar a macro **Failed** para descobrir se o valor de retorno indica falha.

    ```C++
    HRESULT hr;
    hr = SomeFunction();
    if (FAILED(hr))
    {
       // Check for specific error values.
    }
    ```

    

    Muitos dos exemplos nesta documentação usam uma macro chamada GOTO \_ Exit \_ If \_ Failed, que é definida no código a seguir.

    ```C++
    #ifndef GOTO_EXIT_IF_FAILED
    #define GOTO_EXIT_IF_FAILED(hr) if(FAILED(hr)) goto Exit;
    #endif
    ```

    

    Essas funções de exemplo têm uma marca chamada "Exit:", após a qual todas as interfaces e memória alocadas na função são liberadas e o código de erro, se houver, é retornado.

-   Interfaces e memória são liberadas nos exemplos de código usando macros nomeadas de \_ liberação segura e \_ exclusão de matriz segura \_ . Essas macros são definidas no código a seguir:
    ```C++
    #ifndef SAFE_RELEASE
    #define SAFE_RELEASE(x) \
       if(x != NULL)        \
       {                    \
          x->Release();     \
          x = NULL;         \
       }
    #endif

    #ifndef SAFE_ARRAY_DELETE
    #define SAFE_ARRAY_DELETE(x) \
       if(x != NULL)             \
       {                         \
          delete[] x;            \
          x = NULL;              \
       }
    #endif
    ```

    

-   Geralmente, você precisará incluir a lógica de um exemplo em outro exemplo para que o exemplo seja significativo. Nessas instâncias, um comentário TODO é incluído, com uma referência ao exemplo de código apropriado.
-   Para facilitar a leitura do código, nenhuma das funções de exemplo nesta documentação validam seus parâmetros de entrada. Se você copiar qualquer uma dessas funções em seu código, deverá validar quaisquer parâmetros de entrada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Introdução**](getting-started.md)
</dt> </dl>

 

 




