---
title: Serialização de buffer fixa
description: Serialização de buffer fixa.
ms.assetid: 3432f468-89f2-48e2-8d86-15ba549f0fc7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ce58d3bdf92673c97ae8dc9fbbf8f366cb4a59a9e3ce114431de1581af30ec2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021206"
---
# <a name="fixed-buffer-serialization"></a>Serialização de buffer fixa

Ao usar o estilo de buffer fixo, especifique um buffer que seja grande o suficiente para acomodar as operações de codificação (Marshalling) executadas com o identificador. Ao desempacotamento, você fornece o buffer que contém todos os dados a serem decodificados.

O estilo de buffer fixo da serialização usa as seguintes rotinas:

-   [**MesEncodeFixedBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodefixedbufferhandlecreate)
-   [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)
-   [**MesBufferHandleReset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset)
-   [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree)

A função **MesEncodeFixedBufferHandleCreate** aloca a memória necessária para o identificador de codificação e, em seguida, inicializa-a. O aplicativo pode chamar [**MesBufferHandleReset**](/windows/desktop/api/Midles/nf-midles-mesbufferhandlereset) para reinicializar o identificador ou pode chamar [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) para liberar a memória do identificador. Para criar um identificador de decodificação correspondente ao identificador de codificação de estilo fixo, você deve usar [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate).

O aplicativo chama [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) para liberar o identificador de buffer de codificação ou decodificação.

## <a name="examples-of-fixed-buffer-encoding"></a>Exemplos de codificação de buffer fixo

A seção a seguir fornece um exemplo de como usar um estilo de buffer fixo – identificador de serialização para codificação de procedimento.

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

O trecho a seguir representa uma parte de um aplicativo.

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

A seção a seguir fornece um exemplo de como usar um estilo de buffer fixo – identificador de serialização para codificação de tipo.

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

O trecho a seguir representa os fragmentos de aplicativo relevantes.


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



 

 




