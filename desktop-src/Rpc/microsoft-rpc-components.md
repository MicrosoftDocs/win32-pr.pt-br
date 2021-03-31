---
title: Componentes RPC
description: Componentes de RPC (chamada de procedimento remoto).
ms.assetid: 7caaf01a-7f20-470f-afcf-478146cae5eb
keywords:
- RPC de chamada de procedimento remoto, descrito, componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c715a4f454ef28db20ee527e5e8f33f66200b2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916326"
---
# <a name="rpc-components"></a>Componentes RPC

O RPC inclui os seguintes componentes principais:

-   Compilador de MIDL
-   Bibliotecas de tempo de execução e arquivos de cabeçalho
-   Provedor de serviço de nome (às vezes chamado de localizador)
-   Mapeador de ponto de extremidade (às vezes chamado de mapeador de porta)

No modelo de RPC, você pode especificar formalmente uma interface para os procedimentos remotos usando uma linguagem projetada para essa finalidade. Esse idioma é chamado de linguagem de definição de interface, ou IDL. A implementação da Microsoft desse idioma é chamada de linguagem IDL da Microsoft ou MIDL.

Depois de criar uma interface, você deve passá-la por meio do compilador MIDL. Esse compilador gera os stubs que convertem chamadas de procedimento local em chamadas de procedimento remoto. Os stubs são funções de espaço reservado que fazem as chamadas para as funções de biblioteca de tempo de execução, que gerenciam a chamada de procedimento remoto. A vantagem dessa abordagem é que a rede se torna quase completamente transparente para seu aplicativo distribuído. O programa cliente chama o que parece ser procedimentos locais; o trabalho de transformá-los em chamadas remotas é feito automaticamente para você. Todo o código que traduz dados, acessa a rede e recupera os resultados é gerado para você pelo compilador MIDL e é invisível para seu aplicativo.

 

 




