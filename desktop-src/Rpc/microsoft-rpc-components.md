---
title: Componentes RPC
description: Componentes de RPC (chamada de procedimento remoto).
ms.assetid: 7caaf01a-7f20-470f-afcf-478146cae5eb
keywords:
- RPC de chamada de procedimento remoto, descrito, componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44b3416589eccf865b70d3da82fa7494631ab7592f172bb46c10eccb1d96fad1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928115"
---
# <a name="rpc-components"></a>Componentes RPC

O RPC inclui os seguintes componentes principais:

-   Compilador de MIDL
-   Bibliotecas de tempo de execução e arquivos de cabeçalho
-   Provedor de serviço de nome (às vezes chamado de localizador)
-   Mapeador de ponto de extremidade (às vezes chamado de mapeador de porta)

No modelo de RPC, você pode especificar formalmente uma interface para os procedimentos remotos usando uma linguagem projetada para essa finalidade. Esse idioma é chamado de linguagem de definição de interface, ou IDL. A implementação da Microsoft desse idioma é chamada de linguagem IDL da Microsoft ou MIDL.

Depois de criar uma interface, você deve passá-la por meio do compilador MIDL. Esse compilador gera os stubs que convertem chamadas de procedimento local em chamadas de procedimento remoto. Os stubs são funções de espaço reservado que fazem as chamadas para as funções de biblioteca de tempo de execução, que gerenciam a chamada de procedimento remoto. A vantagem dessa abordagem é que a rede se torna quase completamente transparente para seu aplicativo distribuído. O programa cliente chama o que parece ser procedimentos locais; o trabalho de transformá-los em chamadas remotas é feito automaticamente para você. Todo o código que traduz dados, acessa a rede e recupera os resultados é gerado para você pelo compilador MIDL e é invisível para seu aplicativo.

 

 




