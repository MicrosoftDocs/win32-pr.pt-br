---
description: Em aplicativos Winsock, um descritor de soquete não é um descritor de arquivo e deve ser usado com as funções do Winsock.
ms.assetid: bc434b35-9231-4b03-bc8f-cf59aaeb821e
title: Tipo de dados Socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea031032e0d05abc02f7c3c948477c7fe9a1d1de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297062"
---
# <a name="socket-data-type"></a><span data-ttu-id="80407-103">Tipo de dados Socket</span><span class="sxs-lookup"><span data-stu-id="80407-103">Socket Data Type</span></span>

<span data-ttu-id="80407-104">Em aplicativos Winsock, um descritor de soquete não é um descritor de arquivo e deve ser usado com as funções do Winsock.</span><span class="sxs-lookup"><span data-stu-id="80407-104">In Winsock applications, a socket descriptor is not a file descriptor and must be used with the Winsock functions.</span></span>

<span data-ttu-id="80407-105">No UNIX, um descritor de soquete é representado por um descritor de arquivo padrão.</span><span class="sxs-lookup"><span data-stu-id="80407-105">In UNIX, a socket descriptor is represented by a standard file descriptor.</span></span> <span data-ttu-id="80407-106">Como resultado, um descritor de soquete no UNIX pode ser passado para qualquer uma das funções de e/s de arquivo padrão (leitura e gravação, por exemplo).</span><span class="sxs-lookup"><span data-stu-id="80407-106">As a result, a socket descriptor on UNIX may be passed to any of the standard file I/O functions (read and write, for example).</span></span>

<span data-ttu-id="80407-107">Além disso, todos os identificadores no UNIX, incluindo identificadores de soquete, são inteiros pequenos, não negativos e alguns aplicativos fazem suposições de que isso será verdade.</span><span class="sxs-lookup"><span data-stu-id="80407-107">Furthermore, all handles in UNIX, including socket handles, are small, non-negative integers, and some applications make assumptions that this will be true.</span></span>

<span data-ttu-id="80407-108">Os identificadores do Windows Sockets não têm restrições, além de que o valor do \_ soquete inválido não é um soquete válido.</span><span class="sxs-lookup"><span data-stu-id="80407-108">Windows Sockets handles have no restrictions, other than that the value INVALID\_SOCKET is not a valid socket.</span></span> <span data-ttu-id="80407-109">Os identificadores de soquete podem pegar qualquer valor no intervalo de 0 a um \_ soquete inválido – 1.</span><span class="sxs-lookup"><span data-stu-id="80407-109">Socket handles may take any value in the range 0 to INVALID\_SOCKET–1.</span></span>

<span data-ttu-id="80407-110">Como o tipo de **soquete** não é assinado, a compilação do código-fonte existente de, por exemplo, um ambiente UNIX pode levar a avisos do compilador sobre incompatibilidades de tipos de dados assinados/não-assinados.</span><span class="sxs-lookup"><span data-stu-id="80407-110">Because the **SOCKET** type is unsigned, compiling existing source code from, for example, a UNIX environment may lead to compiler warnings about signed/unsigned data type mismatches.</span></span>

<span data-ttu-id="80407-111">Isso significa, por exemplo, que a verificação de erros quando o [**soquete**](/windows/desktop/api/Winsock2/nf-winsock2-socket) e a [**aceitação**](/windows/desktop/api/Winsock2/nf-winsock2-accept) das funções retorna não deve ser feita comparando o valor de retorno com – 1 ou vendo se o valor é negativo (abordagens comuns e legais no UNIX).</span><span class="sxs-lookup"><span data-stu-id="80407-111">This means, for example, that checking for errors when the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) and [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) functions return should not be done by comparing the return value with –1, or seeing if the value is negative (both common and legal approaches in UNIX).</span></span> <span data-ttu-id="80407-112">Em vez disso, um aplicativo deve usar o soquete de constante inválida do manifesto, \_ conforme definido no arquivo de cabeçalho *Winsock2. h* .</span><span class="sxs-lookup"><span data-stu-id="80407-112">Instead, an application should use the manifest constant INVALID\_SOCKET as defined in the *Winsock2.h* header file.</span></span> <span data-ttu-id="80407-113">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="80407-113">For example:</span></span>

<span data-ttu-id="80407-114">Estilo UNIX do BSD típico</span><span class="sxs-lookup"><span data-stu-id="80407-114">Typical BSD UNIX Style</span></span>


```C++
s = socket(...);
if (s == -1)    /* or s < 0 */
    {/*...*/}
```



<span data-ttu-id="80407-115">Estilo preferencial</span><span class="sxs-lookup"><span data-stu-id="80407-115">Preferred Style</span></span>


```C++
s = socket(...);
if (s == INVALID_SOCKET)
    {/*...*/}
```



## <a name="related-topics"></a><span data-ttu-id="80407-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="80407-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80407-117">Portando aplicativos de soquete para Winsock</span><span class="sxs-lookup"><span data-stu-id="80407-117">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="80407-118">Considerações sobre programação do Winsock</span><span class="sxs-lookup"><span data-stu-id="80407-118">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> </dl>

 

 



