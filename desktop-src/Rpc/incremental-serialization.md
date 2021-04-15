---
title: Serialização incremental
description: Ao usar a serialização de estilo incremental, você fornece três rotinas para manipular o buffer.
ms.assetid: c7383b4d-94d1-4edd-ac29-c11fb5343156
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 409f8da0881719ec9273f4dd12cc99e3d36c35a3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498787"
---
# <a name="incremental-serialization"></a>Serialização incremental

Ao usar a serialização de estilo incremental, você fornece três rotinas para manipular o buffer. Essas rotinas são: Alloc, Read e Write. A rotina de alocação aloca um buffer do tamanho necessário. A rotina de gravação grava os dados no buffer e a rotina de leitura recupera um buffer que contém dados empacotados. Uma única chamada de serialização pode fazer várias chamadas para essas rotinas.

O estilo incremental de serialização usa as seguintes rotinas:

-   [**MesEncodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodeincrementalhandlecreate)
-   [**MesDecodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodeincrementalhandlecreate)
-   [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset)
-   [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree)

Os protótipos para as funções de alocação, leitura e gravação que você deve fornecer são mostrados abaixo:

``` syntax
void __RPC_USER Alloc (
   void *State,          /* application-defined pointer */
   char **pBuffer,       /* returns pointer to allocated buffer */
   unsigned int *pSize); /* inputs requested bytes; outputs 
                         /* pBuffer size */

void __RPC_USER Write (
   void *State,          /* application-defined pointer */
   char *Buffer,         /* buffer with serialized data */
   unsigned int Size);   /* number of bytes to write from Buffer */

void __RPC_USER Read (
   void *State,          /* application-defined pointer */
   char **pBuffer,       /* returned pointer to buffer with data */
   unsigned int *pSize); /* number of bytes to read into pBuffer */
```

A entrada de estado um parâmetro para todas as três funções é o ponteiro definido pelo aplicativo que estava associado ao identificador de serviços de codificação. O aplicativo pode usar esse ponteiro para acessar a estrutura que contém informações específicas do aplicativo, como um identificador de arquivo ou um ponteiro de fluxo. Observe que os stubs não modificam o ponteiro de estado que não seja para passá-lo para as funções de alocação, leitura e gravação. Durante a codificação, a alocação é chamada para obter um buffer no qual os dados são serializados. Em seguida, Write é chamado para permitir que o aplicativo controle quando e onde os dados serializados são armazenados. Durante a decodificação, Read é chamado para retornar o número solicitado de bytes de dados serializados de onde o aplicativo o armazenou.

Um recurso importante do estilo incremental é que o identificador mantém o ponteiro de estado para você. Esse ponteiro mantém o estado e nunca é tocado pelas funções RPC, exceto ao passar o ponteiro para a função Alloc, Write ou Read. O identificador também mantém um estado interno que torna possível codificar e decodificar várias instâncias de tipo para o mesmo buffer, adicionando preenchimento conforme necessário para alinhamento. A função [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) redefine um identificador para seu estado inicial para habilitar a leitura ou gravação a partir do início do buffer.

As funções de alocação e gravação, juntamente com um ponteiro definido pelo aplicativo, são associadas a um identificador de serviços de codificação por uma chamada para a função [**MesEncodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodeincrementalhandlecreate) . **MesEncodeIncrementalHandleCreate** aloca a memória necessária para o identificador e, em seguida, inicializa-a.

O aplicativo pode chamar [**MesDecodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodeincrementalhandlecreate) para criar um identificador de decodificação, [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) para reinicializar o identificador ou [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) para liberar a memória do identificador. A função de leitura, juntamente com um parâmetro definido pelo aplicativo, é associada a um identificador de decodificação por uma chamada para a rotina **MesDecodeIncrementalHandleCreate** . A função cria o identificador e o inicializa.

Os parâmetros UserState, Alloc, Write e Read de [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) podem ser **nulos** para não indicar nenhuma alteração.

 

 




