---
title: Identificadores de serialização
description: Um aplicativo usa os procedimentos de serialização ou as rotinas de suporte de serialização geradas pelo compilador MIDL em conjunto com um conjunto de funções de biblioteca para manipular um identificador de serialização.
ms.assetid: 39859846-5b94-447a-a71b-a08b8eb2c4c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5585fc3f34b6cc826c1f8157bd59a144070ea081
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005964"
---
# <a name="serialization-handles"></a>Identificadores de serialização

Um aplicativo usa os procedimentos de serialização ou as rotinas de suporte de serialização geradas pelo compilador MIDL em conjunto com um conjunto de funções de biblioteca para manipular um identificador de serialização. Juntas, essas funções fornecem um mecanismo para personalizar a maneira como um aplicativo serializa os dados.

Um identificador de serialização é necessário para qualquer operação de serialização, e todos os identificadores de serialização devem ser gerenciados explicitamente por você. Para fazer isso, primeiro crie um identificador válido chamando uma das seguintes rotinas:

-   [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)
-   [**MesDecodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodeincrementalhandlecreate)
-   [**MesEncodeDynBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate)
-   [**MesEncodeFixedBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodefixedbufferhandlecreate)
-   [**MesEncodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodeincrementalhandlecreate)

Você libera o identificador com uma chamada para [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree). Depois que o identificador tiver sido criado ou reinicializado, ele representará um contexto de serialização válido e poderá ser usado para codificar ou decodificar, dependendo do tipo do identificador.

Esta seção descreve os identificadores de serialização e como usá-los, nos seguintes tópicos:

-   [Identificadores implícitos versus explícitos](implicit-versus-explicit-handles.md)
-   [Estilos de serialização](serialization-styles.md)
-   [Obtendo uma identidade de codificação](obtaining-an-encoding-identity.md)

 

 




