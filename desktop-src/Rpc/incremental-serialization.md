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
# <a name="incremental-serialization"></a><span data-ttu-id="720b7-103">Serialização incremental</span><span class="sxs-lookup"><span data-stu-id="720b7-103">Incremental Serialization</span></span>

<span data-ttu-id="720b7-104">Ao usar a serialização de estilo incremental, você fornece três rotinas para manipular o buffer.</span><span class="sxs-lookup"><span data-stu-id="720b7-104">When using the incremental style serialization, you supply three routines to manipulate the buffer.</span></span> <span data-ttu-id="720b7-105">Essas rotinas são: Alloc, Read e Write.</span><span class="sxs-lookup"><span data-stu-id="720b7-105">These routines are: Alloc, Read, and Write.</span></span> <span data-ttu-id="720b7-106">A rotina de alocação aloca um buffer do tamanho necessário.</span><span class="sxs-lookup"><span data-stu-id="720b7-106">The Alloc routine allocates a buffer of the required size.</span></span> <span data-ttu-id="720b7-107">A rotina de gravação grava os dados no buffer e a rotina de leitura recupera um buffer que contém dados empacotados.</span><span class="sxs-lookup"><span data-stu-id="720b7-107">The Write routine writes the data into the buffer, and the Read routine retrieves a buffer that contains marshaled data.</span></span> <span data-ttu-id="720b7-108">Uma única chamada de serialização pode fazer várias chamadas para essas rotinas.</span><span class="sxs-lookup"><span data-stu-id="720b7-108">A single serialization call can make several calls to these routines.</span></span>

<span data-ttu-id="720b7-109">O estilo incremental de serialização usa as seguintes rotinas:</span><span class="sxs-lookup"><span data-stu-id="720b7-109">The incremental style of serialization uses the following routines:</span></span>

-   [<span data-ttu-id="720b7-110">**MesEncodeIncrementalHandleCreate**</span><span class="sxs-lookup"><span data-stu-id="720b7-110">**MesEncodeIncrementalHandleCreate**</span></span>](/windows/desktop/api/Midles/nf-midles-mesencodeincrementalhandlecreate)
-   [<span data-ttu-id="720b7-111">**MesDecodeIncrementalHandleCreate**</span><span class="sxs-lookup"><span data-stu-id="720b7-111">**MesDecodeIncrementalHandleCreate**</span></span>](/windows/desktop/api/Midles/nf-midles-mesdecodeincrementalhandlecreate)
-   [<span data-ttu-id="720b7-112">**MesIncrementalHandleReset**</span><span class="sxs-lookup"><span data-stu-id="720b7-112">**MesIncrementalHandleReset**</span></span>](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset)
-   [<span data-ttu-id="720b7-113">**MesHandleFree**</span><span class="sxs-lookup"><span data-stu-id="720b7-113">**MesHandleFree**</span></span>](/windows/desktop/api/Midles/nf-midles-meshandlefree)

<span data-ttu-id="720b7-114">Os protótipos para as funções de alocação, leitura e gravação que você deve fornecer são mostrados abaixo:</span><span class="sxs-lookup"><span data-stu-id="720b7-114">The prototypes for the Alloc, Read, and Write functions that you must provide are shown below:</span></span>

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

<span data-ttu-id="720b7-115">A entrada de estado um parâmetro para todas as três funções é o ponteiro definido pelo aplicativo que estava associado ao identificador de serviços de codificação.</span><span class="sxs-lookup"><span data-stu-id="720b7-115">The State input a parameter for all three functions is the application-defined pointer that was associated with the encoding services handle.</span></span> <span data-ttu-id="720b7-116">O aplicativo pode usar esse ponteiro para acessar a estrutura que contém informações específicas do aplicativo, como um identificador de arquivo ou um ponteiro de fluxo.</span><span class="sxs-lookup"><span data-stu-id="720b7-116">The application can use this pointer to access the structure containing application-specific information, such as a file handle or stream pointer.</span></span> <span data-ttu-id="720b7-117">Observe que os stubs não modificam o ponteiro de estado que não seja para passá-lo para as funções de alocação, leitura e gravação.</span><span class="sxs-lookup"><span data-stu-id="720b7-117">Note that the stubs do not modify the State pointer other than to pass it to the Alloc, Read, and Write functions.</span></span> <span data-ttu-id="720b7-118">Durante a codificação, a alocação é chamada para obter um buffer no qual os dados são serializados.</span><span class="sxs-lookup"><span data-stu-id="720b7-118">During encoding, Alloc is called to obtain a buffer into which the data is serialized.</span></span> <span data-ttu-id="720b7-119">Em seguida, Write é chamado para permitir que o aplicativo controle quando e onde os dados serializados são armazenados.</span><span class="sxs-lookup"><span data-stu-id="720b7-119">Then, Write is called to enable the application to control when and where the serialized data is stored.</span></span> <span data-ttu-id="720b7-120">Durante a decodificação, Read é chamado para retornar o número solicitado de bytes de dados serializados de onde o aplicativo o armazenou.</span><span class="sxs-lookup"><span data-stu-id="720b7-120">During decoding, Read is called to return the requested number of bytes of serialized data from where the application stored it.</span></span>

<span data-ttu-id="720b7-121">Um recurso importante do estilo incremental é que o identificador mantém o ponteiro de estado para você.</span><span class="sxs-lookup"><span data-stu-id="720b7-121">An important feature of the incremental style is that the handle keeps the state pointer for you.</span></span> <span data-ttu-id="720b7-122">Esse ponteiro mantém o estado e nunca é tocado pelas funções RPC, exceto ao passar o ponteiro para a função Alloc, Write ou Read.</span><span class="sxs-lookup"><span data-stu-id="720b7-122">This pointer maintains the state and is never touched by the RPC functions, except when passing the pointer to Alloc, Write, or Read function.</span></span> <span data-ttu-id="720b7-123">O identificador também mantém um estado interno que torna possível codificar e decodificar várias instâncias de tipo para o mesmo buffer, adicionando preenchimento conforme necessário para alinhamento.</span><span class="sxs-lookup"><span data-stu-id="720b7-123">The handle also maintains an internal state that makes it possible to encode and decode several type instances to the same buffer by adding padding as needed for alignment.</span></span> <span data-ttu-id="720b7-124">A função [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) redefine um identificador para seu estado inicial para habilitar a leitura ou gravação a partir do início do buffer.</span><span class="sxs-lookup"><span data-stu-id="720b7-124">The [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) function resets a handle to its initial state to enable reading or writing from the beginning of the buffer.</span></span>

<span data-ttu-id="720b7-125">As funções de alocação e gravação, juntamente com um ponteiro definido pelo aplicativo, são associadas a um identificador de serviços de codificação por uma chamada para a função [**MesEncodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodeincrementalhandlecreate) .</span><span class="sxs-lookup"><span data-stu-id="720b7-125">The Alloc and Write functions, along with an application-defined pointer, are associated with an encoding-services handle by a call to the [**MesEncodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodeincrementalhandlecreate) function.</span></span> <span data-ttu-id="720b7-126">**MesEncodeIncrementalHandleCreate** aloca a memória necessária para o identificador e, em seguida, inicializa-a.</span><span class="sxs-lookup"><span data-stu-id="720b7-126">**MesEncodeIncrementalHandleCreate** allocates the memory needed for the handle and then initializes it.</span></span>

<span data-ttu-id="720b7-127">O aplicativo pode chamar [**MesDecodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodeincrementalhandlecreate) para criar um identificador de decodificação, [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) para reinicializar o identificador ou [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) para liberar a memória do identificador.</span><span class="sxs-lookup"><span data-stu-id="720b7-127">The application can call [**MesDecodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodeincrementalhandlecreate) to create a decoding handle, [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) to reinitialize the handle, or [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) to free the handle's memory.</span></span> <span data-ttu-id="720b7-128">A função de leitura, juntamente com um parâmetro definido pelo aplicativo, é associada a um identificador de decodificação por uma chamada para a rotina **MesDecodeIncrementalHandleCreate** .</span><span class="sxs-lookup"><span data-stu-id="720b7-128">The Read function, along with an application-defined parameter, is associated with a decoding handle by a call to the **MesDecodeIncrementalHandleCreate** routine.</span></span> <span data-ttu-id="720b7-129">A função cria o identificador e o inicializa.</span><span class="sxs-lookup"><span data-stu-id="720b7-129">The function creates the handle and initializes it.</span></span>

<span data-ttu-id="720b7-130">Os parâmetros UserState, Alloc, Write e Read de [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) podem ser **nulos** para não indicar nenhuma alteração.</span><span class="sxs-lookup"><span data-stu-id="720b7-130">The UserState, Alloc, Write, and Read parameters of [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) can be **NULL** to indicate no change.</span></span>

 

 




