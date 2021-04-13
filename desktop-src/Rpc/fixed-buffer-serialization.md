---
title: Serialização de buffer fixa
description: Serialização de buffer fixa.
ms.assetid: 3432f468-89f2-48e2-8d86-15ba549f0fc7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c87e3cad0a272ccd493cf9088fedeb272f1206b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364078"
---
# <a name="fixed-buffer-serialization"></a><span data-ttu-id="a1a60-103">Serialização de buffer fixa</span><span class="sxs-lookup"><span data-stu-id="a1a60-103">Fixed Buffer Serialization</span></span>

<span data-ttu-id="a1a60-104">Ao usar o estilo de buffer fixo, especifique um buffer que seja grande o suficiente para acomodar as operações de codificação (Marshalling) executadas com o identificador.</span><span class="sxs-lookup"><span data-stu-id="a1a60-104">When using the fixed buffer style, specify a buffer that is large enough to accommodate the encoding (marshalling) operations performed with the handle.</span></span> <span data-ttu-id="a1a60-105">Ao desempacotamento, você fornece o buffer que contém todos os dados a serem decodificados.</span><span class="sxs-lookup"><span data-stu-id="a1a60-105">When unmarshaling, you provide the buffer that contains all of the data to decode.</span></span>

<span data-ttu-id="a1a60-106">O estilo de buffer fixo da serialização usa as seguintes rotinas:</span><span class="sxs-lookup"><span data-stu-id="a1a60-106">The fixed buffer style of serialization uses the following routines:</span></span>

-   [<span data-ttu-id="a1a60-107">**MesEncodeFixedBufferHandleCreate**</span><span class="sxs-lookup"><span data-stu-id="a1a60-107">**MesEncodeFixedBufferHandleCreate**</span></span>](/windows/desktop/api/Midles/nf-midles-mesencodefixedbufferhandlecreate)
-   [<span data-ttu-id="a1a60-108">**MesDecodeBufferHandleCreate**</span><span class="sxs-lookup"><span data-stu-id="a1a60-108">**MesDecodeBufferHandleCreate**</span></span>](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)
-   [<span data-ttu-id="a1a60-109">**MesBufferHandleReset**</span><span class="sxs-lookup"><span data-stu-id="a1a60-109">**MesBufferHandleReset**</span></span>](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset)
-   [<span data-ttu-id="a1a60-110">**MesHandleFree**</span><span class="sxs-lookup"><span data-stu-id="a1a60-110">**MesHandleFree**</span></span>](/windows/desktop/api/Midles/nf-midles-meshandlefree)

<span data-ttu-id="a1a60-111">A função **MesEncodeFixedBufferHandleCreate** aloca a memória necessária para o identificador de codificação e, em seguida, inicializa-a.</span><span class="sxs-lookup"><span data-stu-id="a1a60-111">The **MesEncodeFixedBufferHandleCreate** function allocates the memory needed for the encoding handle, and then initializes it.</span></span> <span data-ttu-id="a1a60-112">O aplicativo pode chamar [**MesBufferHandleReset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset) para reinicializar o identificador ou pode chamar [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) para liberar a memória do identificador.</span><span class="sxs-lookup"><span data-stu-id="a1a60-112">The application can call [**MesBufferHandleReset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset) to reinitialize the handle, or it can call [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) to free the handle's memory.</span></span> <span data-ttu-id="a1a60-113">Para criar um identificador de decodificação correspondente ao identificador de codificação de estilo fixo, você deve usar [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate).</span><span class="sxs-lookup"><span data-stu-id="a1a60-113">To create a decoding handle corresponding to the fixed style–encoding handle, you must use [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate).</span></span>

<span data-ttu-id="a1a60-114">O aplicativo chama [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) para liberar o identificador de buffer de codificação ou decodificação.</span><span class="sxs-lookup"><span data-stu-id="a1a60-114">The application calls [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) to free the encoding or decoding buffer handle.</span></span>

## <a name="examples-of-fixed-buffer-encoding"></a><span data-ttu-id="a1a60-115">Exemplos de codificação de buffer fixo</span><span class="sxs-lookup"><span data-stu-id="a1a60-115">Examples of Fixed Buffer Encoding</span></span>

<span data-ttu-id="a1a60-116">A seção a seguir fornece um exemplo de como usar um estilo de buffer fixo – identificador de serialização para codificação de procedimento.</span><span class="sxs-lookup"><span data-stu-id="a1a60-116">The following section provides an example of how to use a fixed buffer style–serializing handle for procedure encoding.</span></span>

``` syntax
/*This is a fragment of the IDL file defining MooProc */

...
void __RPC_USER
MyProc( [in] handle_t Handle, [in,out] MyType * pMyObject,
        [in, out] ThisType * pThisObject);
...

/*This is an ACF file. MyProc is defined in the IDL file */

[
    explicit_handle
]
interface regress
{
    [ encode,decode ] MyProc();
}
```

<span data-ttu-id="a1a60-117">O trecho a seguir representa uma parte de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a1a60-117">The following excerpt represents a part of an application.</span></span>

``` syntax
if (MesEncodeFixedBufferHandleCreate (
        Buffer, BufferSize, 
        pEncodedSize, &Handle) == RPC_S_OK)
{
    ...
    /* Manufacture a MyObject and a ThisObject */
    ...
    /* The serialization works from the beginning of the buffer because 
   the handle is in the initial state. The function MyProc does the    
   following when called with an encoding handle:
     - sizes all the parameters for marshalling,
     - marshalls into the buffer (and sets the internal state 
    appropriately) 
    */

    MyProc ( Handle, pMyObject, pThisObject );
    ...
    MesHandleFree ();
}
if (MesDecodeBufferHandleCreate (Buffer, BufferSize, &Handle) ==
    RPC_S_OK)
{

    /* The MooProc does the following for you when called with a decoding 
    handle:
     - unmarshalls the objects from the buffer into *pMooObject and 
       *pBarObject
*/

MyProc ( Handle, pMyObject, pThisObject);
...
MesHandleFree ( Handle );
}
```

<span data-ttu-id="a1a60-118">A seção a seguir fornece um exemplo de como usar um estilo de buffer fixo – identificador de serialização para codificação de tipo.</span><span class="sxs-lookup"><span data-stu-id="a1a60-118">The following section provides an example of how to use a fixed buffer style–serializing handle for type encoding.</span></span>

``` syntax
/* This is an ACF file. MyType is defined in the IDL file */

[    
    explicit_handle
]
interface regress
{
    typedef [ encode,decode ] MyType;
}
```

<span data-ttu-id="a1a60-119">O trecho a seguir representa os fragmentos de aplicativo relevantes.</span><span class="sxs-lookup"><span data-stu-id="a1a60-119">The following excerpt represents the relevant application fragments.</span></span>


```C++
if (MesEncodeFixedBufferHandleCreate (Buffer, BufferSize, 
    pEncodedSize, &Handle) == RPC_S_OK)
{
    //...
    /* Manufacture a MyObject and a pMyObject */
    //...
    MyType_Encode ( Handle, pMyObject );
    //...
    MesHandleFree ();
}
if (MesDecodeBufferHandleCreate (Buffer, BufferSize, &Handle) ==
    RPC_S_OK )
{
    MooType_Decode (Handle, pMooObject);
    //...
    MesHandleFree ( Handle );
}
```



 

 




