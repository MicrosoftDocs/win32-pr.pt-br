---
title: Usando serviços de serialização
description: MIDL gera um stub de serialização para o procedimento com os atributos \ Encode \ e \ decodificar \.
ms.assetid: b1fce133-32e3-4b5e-9f9d-ffbe60e9d9cd
keywords:
- RPC de chamada de procedimento remoto, tarefas, usando serviços de serialização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 317156a2da954e001b687cca12eb0c6df23ef4ee
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008320"
---
# <a name="using-serialization-services"></a><span data-ttu-id="f2a28-104">Usando serviços de serialização</span><span class="sxs-lookup"><span data-stu-id="f2a28-104">Using Serialization Services</span></span>

<span data-ttu-id="f2a28-105">MIDL gera um stub de serialização para o procedimento com os atributos \[ [**Encode**](/windows/desktop/Midl/encode) \] e \[ [**decodificação**](/windows/desktop/Midl/decode) \] .</span><span class="sxs-lookup"><span data-stu-id="f2a28-105">MIDL generates a serialization stub for the procedure with the attributes \[[**encode**](/windows/desktop/Midl/encode)\] and \[[**decode**](/windows/desktop/Midl/decode)\].</span></span> <span data-ttu-id="f2a28-106">Ao chamar essa rotina, você executa uma chamada de serialização em vez de uma chamada remota.</span><span class="sxs-lookup"><span data-stu-id="f2a28-106">When you call this routine, you execute a serialization call instead of a remote call.</span></span> <span data-ttu-id="f2a28-107">Os argumentos de procedimento são empacotados ou desempacotados de um buffer da maneira usual.</span><span class="sxs-lookup"><span data-stu-id="f2a28-107">The procedure arguments are marshaled to or unmarshaled from a buffer in the usual way.</span></span> <span data-ttu-id="f2a28-108">Em seguida, você tem controle total dos buffers.</span><span class="sxs-lookup"><span data-stu-id="f2a28-108">You then have complete control of the buffers.</span></span>

<span data-ttu-id="f2a28-109">Por outro lado, quando o programa executa a serialização de tipo (um tipo é rotulado com atributos de serialização), o MIDL gera rotinas para dimensionar, codificar e decodificar objetos desse tipo.</span><span class="sxs-lookup"><span data-stu-id="f2a28-109">In contrast, when your program performs type serialization (a type is labeled with serialization attributes), MIDL generates routines to size, encode, and decode objects of that type.</span></span> <span data-ttu-id="f2a28-110">Para serializar dados, você deve chamar essas rotinas da maneira apropriada.</span><span class="sxs-lookup"><span data-stu-id="f2a28-110">To serialize data, you must call these routines in the appropriate way.</span></span> <span data-ttu-id="f2a28-111">A serialização de tipo é uma extensão da Microsoft e, como tal, não está disponível quando você compila no modo de compatibilidade de DCE ([**/OSF**](/windows/desktop/Midl/-osf)).</span><span class="sxs-lookup"><span data-stu-id="f2a28-111">Type serialization is a Microsoft extension and, as such, is not available when you compile in DCE-compatibility ([**/osf**](/windows/desktop/Midl/-osf)) mode.</span></span> <span data-ttu-id="f2a28-112">Usando os atributos de \[ [**codificação**](/windows/desktop/Midl/encode) \] e \[ [**decodificação**](/windows/desktop/Midl/decode) \] como atributos de interface, o RPC aplica a codificação a todos os tipos e rotinas definidos no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="f2a28-112">By using the \[[**encode**](/windows/desktop/Midl/encode)\] and \[[**decode**](/windows/desktop/Midl/decode)\] attributes as interface attributes, RPC applies encoding to all the types and routines defined in the IDL file.</span></span>

<span data-ttu-id="f2a28-113">Você deve fornecer buffers adequadamente alinhados ao usar os serviços de serialização.</span><span class="sxs-lookup"><span data-stu-id="f2a28-113">You must supply adequately aligned buffers when using serialization services.</span></span> <span data-ttu-id="f2a28-114">O início do buffer deve ser alinhado em um endereço que seja múltiplo de 8 ou 8 bytes alinhados.</span><span class="sxs-lookup"><span data-stu-id="f2a28-114">The beginning of the buffer must be aligned at an address that is a multiple of 8, or 8-byte aligned.</span></span> <span data-ttu-id="f2a28-115">Para serialização de procedimento, cada chamada de procedimento deve realizar marshaling ou Unmarshal de uma posição de buffer que esteja alinhada em 8 bytes.</span><span class="sxs-lookup"><span data-stu-id="f2a28-115">For procedure serialization, each procedure call must marshal into or unmarshal from a buffer position that is 8-byte aligned.</span></span> <span data-ttu-id="f2a28-116">Para serialização de tipo, o dimensionamento, a codificação e a decodificação devem começar em uma posição que esteja alinhada em 8 bytes.</span><span class="sxs-lookup"><span data-stu-id="f2a28-116">For type serialization, sizing, encoding, and decoding must start at a position that is 8-byte aligned.</span></span>

<span data-ttu-id="f2a28-117">Uma maneira de seu aplicativo garantir que seus buffers estejam alinhados é gravar a função [**de \_ \_ alocação de usuário MIDL**](/windows/desktop/Midl/midl-user-allocate-1) de forma que ele crie buffers alinhados.</span><span class="sxs-lookup"><span data-stu-id="f2a28-117">One way for your application to ensure that its buffers are aligned is to write the [**midl\_user\_allocate**](/windows/desktop/Midl/midl-user-allocate-1) function such that it creates aligned buffers.</span></span> <span data-ttu-id="f2a28-118">O exemplo de código a seguir demonstra como isso pode ser feito.</span><span class="sxs-lookup"><span data-stu-id="f2a28-118">The following code sample demonstrates how this can be done.</span></span>


```C++
#include <windows.h>

#define ALIGN_TO8(p)   (char *)((unsigned long)((char *)p + 7) & ~7)

void __RPC_FAR *__RPC_USER  MIDL_user_allocate(size_t sizeInBytes)
{
    unsigned char *pcAllocated;
    unsigned char *pcUserPtr;

    pcAllocated = (unsigned char *) malloc( sizeInBytes + 15 );
    pcUserPtr =  ALIGN_TO8( pcAllocated );
    if ( pcUserPtr == pcAllocated )
        pcUserPtr = pcAllocated + 8;

    *(pcUserPtr - 1) = pcUserPtr - pcAllocated;

    return( pcUserPtr );
}
```



<span data-ttu-id="f2a28-119">O exemplo a seguir mostra a [**função \_ \_ gratuita do usuário MIDL**](/windows/desktop/Midl/midl-user-free-1) correspondente.</span><span class="sxs-lookup"><span data-stu-id="f2a28-119">The following example shows the corresponding [**midl\_user\_free**](/windows/desktop/Midl/midl-user-free-1) function.</span></span>


```C++
void __RPC_USER  MIDL_user_free(void __RPC_FAR *f)
{
    unsigned char * pcAllocated;
    unsigned char * pcUserPtr;

    pcUserPtr = (unsigned char *) f;
    pcAllocated = pcUserPtr - *(pcUserPtr - 1);

    free( pcAllocated );
}
```



 

 