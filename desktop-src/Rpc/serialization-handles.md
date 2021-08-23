---
title: Alças de serialização
description: Um aplicativo usa os procedimentos de serialização ou as rotinas de suporte de serialização geradas pelo compilador MIDL em conjunto com um conjunto de funções de biblioteca para manipular um alça de serialização.
ms.assetid: 39859846-5b94-447a-a71b-a08b8eb2c4c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12995144e44fa6b4b91f021d544b53c03d732df22d46489ccc2cefe8d34c0fa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925463"
---
# <a name="serialization-handles"></a>Alças de serialização

Um aplicativo usa os procedimentos de serialização ou as rotinas de suporte de serialização geradas pelo compilador MIDL em conjunto com um conjunto de funções de biblioteca para manipular um alça de serialização. Juntas, essas funções fornecem um mecanismo para personalizar a maneira como um aplicativo serializa os dados.

Um alça de serialização é necessário para qualquer operação de serialização e todos os alças de serialização devem ser gerenciados explicitamente por você. Para fazer isso, primeiro crie um handle válido chamando uma das seguintes rotinas:

-   [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)
-   [**MesDecodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodeincrementalhandlecreate)
-   [**MesEncodeDynBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate)
-   [**MesEncodeFixedBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodefixedbufferhandlecreate)
-   [**MesEncodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodeincrementalhandlecreate)

Você libera o handle com uma chamada para [**MesHandleFree.**](/windows/desktop/api/Midles/nf-midles-meshandlefree) Depois que o identificador tiver sido criado ou reinicializado, ele representará um contexto de serialização válido e poderá ser usado para codificar ou decodificar, dependendo do tipo do identificador.

Esta seção descreve os handles de serialização e como usá-los nos tópicos a seguir:

-   [Alças implícitas versus explícitas](implicit-versus-explicit-handles.md)
-   [Estilos de serialização](serialization-styles.md)
-   [Obtendo uma identidade de codificação](obtaining-an-encoding-identity.md)

 

 




