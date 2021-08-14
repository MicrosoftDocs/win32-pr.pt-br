---
title: usando os exemplos de código de cliente do Microsoft Windows Media DRM
description: usando os exemplos de código de cliente do Microsoft Windows Media DRM
ms.assetid: 75db2663-9eb8-406d-b1a9-8f6092c95f9d
keywords:
- Windows SDK do formato de mídia, exemplos de código
- Windows SDK do formato de mídia, código de exemplo
- Windows SDK do formato de mídia, exemplos de código DRM
- DRM (gerenciamento de direitos digitais), exemplos de código
- DRM (gerenciamento de direitos digitais), exemplos de código
- DRM (gerenciamento de direitos digitais), código de exemplo
- DRM (gerenciamento de direitos digitais), código de exemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e14ef7e1d003dec8270bb4cfb63d5b4ead7f11751eb94dd09cd771ebd34b3ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118704209"
---
# <a name="using-the-microsoft-windows-media-drm-client-code-examples"></a>usando os exemplos de código de cliente do Microsoft Windows Media DRM

Os exemplos de código estão incluídos nesta documentação para ilustrar o uso de componentes. Os exemplos são escritos para serem tão claros e concisos quanto possível. Ao ler os exemplos, você deve estar ciente das convenções a seguir.

-   Todos os exemplos são presumidos para incluir Windows. h e wmdrmsdk. h. O exemplo incluirá uma observação se precisar de outros cabeçalhos para compilar.
-   A verificação de erros foi restrita à interrupção da função se ocorrer um erro. Em um aplicativo, você deve verificar se há códigos de erro específicos e fornecer algum tipo de relatório de erros.
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

    

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Introdução**](drm-getting-started.md)
</dt> </dl>

 

 




