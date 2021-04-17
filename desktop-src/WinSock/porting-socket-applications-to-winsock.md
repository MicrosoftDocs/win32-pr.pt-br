---
description: Esta seção descreve as considerações de portabilidade do Winsock.
ms.assetid: 41c0c98e-3990-4600-ab9f-fa87edbea402
title: Portando aplicativos de soquete para Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e2b3480d5572405d33b3a3532892a48633caa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811728"
---
# <a name="porting-socket-applications-to-winsock"></a><span data-ttu-id="d4383-103">Portando aplicativos de soquete para Winsock</span><span class="sxs-lookup"><span data-stu-id="d4383-103">Porting Socket Applications to Winsock</span></span>

<span data-ttu-id="d4383-104">Esta seção descreve as considerações de portabilidade do Winsock.</span><span class="sxs-lookup"><span data-stu-id="d4383-104">This section describes Winsock porting considerations.</span></span>

<span data-ttu-id="d4383-105">Há um número limitado de instâncias em que o Windows Sockets diverteu da adesão estrita às convenções de Berkeley, geralmente devido a dificuldades de implementação no ambiente do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="d4383-105">There are a limited number of instances where Windows Sockets has diverted from strict adherence to the Berkeley conventions, usually due to implementation difficulties in the Microsoft Windows environment.</span></span>

<span data-ttu-id="d4383-106">Quando um desvio das convenções de Berkeley ocorre no Windows Sockets, o desvio é especificamente indicado e claramente anotado.</span><span class="sxs-lookup"><span data-stu-id="d4383-106">When a deviation from Berkeley conventions occurs in Windows Sockets, the deviation is specifically and clearly noted.</span></span> <span data-ttu-id="d4383-107">Por exemplo, se uma função for específica para o Windows Sockets, esse desvio será especificado com uma frase na descrição da função semelhante à seguinte:</span><span class="sxs-lookup"><span data-stu-id="d4383-107">For example, if a function is specific to Windows Sockets, that deviation is specified with a phrase in the function description similar to the following:</span></span>

<span data-ttu-id="d4383-108">A função **\[ Function- \] Name** é uma extensão específica da Microsoft para a API do Windows Sockets 2.</span><span class="sxs-lookup"><span data-stu-id="d4383-108">The **\[function-name\]** function is a Microsoft-specific extension to the Windows Sockets 2 API.</span></span>

<span data-ttu-id="d4383-109">Esta seção fornece informações sobre portabilidade de aplicativos de soquete UNIX do Berkeley (BSD) para Winsock:</span><span class="sxs-lookup"><span data-stu-id="d4383-109">This section provides information about porting Berkeley (BSD) UNIX socket applications to Winsock:</span></span>

-   [<span data-ttu-id="d4383-110">Tipo de dados Socket</span><span class="sxs-lookup"><span data-stu-id="d4383-110">Socket Data Type</span></span>](socket-data-type-2.md)
-   [<span data-ttu-id="d4383-111">Macros Select, FD \_ set e FD \_ xxx</span><span class="sxs-lookup"><span data-stu-id="d4383-111">Select, FD\_SET, and FD\_XXX Macros</span></span>](select-and-fd---2.md)
-   [<span data-ttu-id="d4383-112">Códigos de erro-errno, h \_ errno e WSAGetLastError</span><span class="sxs-lookup"><span data-stu-id="d4383-112">Error Codes - errno, h\_errno and WSAGetLastError</span></span>](error-codes-errno-h-errno-and-wsagetlasterror-2.md)
-   [<span data-ttu-id="d4383-113">Ponteiros</span><span class="sxs-lookup"><span data-stu-id="d4383-113">Pointers</span></span>](pointers-2.md)
-   [<span data-ttu-id="d4383-114">Funções renomeadas</span><span class="sxs-lookup"><span data-stu-id="d4383-114">Renamed Functions</span></span>](renamed-functions-2.md)
-   [<span data-ttu-id="d4383-115">Número máximo de soquetes com suporte</span><span class="sxs-lookup"><span data-stu-id="d4383-115">Maximum Number of Sockets Supported</span></span>](maximum-number-of-sockets-supported-2.md)
-   [<span data-ttu-id="d4383-116">Incluir arquivos</span><span class="sxs-lookup"><span data-stu-id="d4383-116">Include Files</span></span>](include-files-2.md)
-   [<span data-ttu-id="d4383-117">Valores de retorno em falha de função</span><span class="sxs-lookup"><span data-stu-id="d4383-117">Return Values on Function Failure</span></span>](return-values-on-function-failure-2.md)
-   [<span data-ttu-id="d4383-118">Soquetes brutos</span><span class="sxs-lookup"><span data-stu-id="d4383-118">Raw Sockets</span></span>](service-provided-raw-sockets-2.md)
-   [<span data-ttu-id="d4383-119">Ordenação de bytes</span><span class="sxs-lookup"><span data-stu-id="d4383-119">Byte Ordering</span></span>](byte-ordering-2.md)
-   [<span data-ttu-id="d4383-120">Rotinas de conversão de Byte-Order estendidas</span><span class="sxs-lookup"><span data-stu-id="d4383-120">Extended Byte-Order Conversion Routines</span></span>](extended-byte-order-conversion-routines-2.md)

## <a name="related-topics"></a><span data-ttu-id="d4383-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d4383-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4383-122">Manipulando erros do Winsock</span><span class="sxs-lookup"><span data-stu-id="d4383-122">Handling Winsock Errors</span></span>](handling-winsock-errors.md)
</dt> <dt>

[<span data-ttu-id="d4383-123">Portando aplicativos de soquete para Winsock</span><span class="sxs-lookup"><span data-stu-id="d4383-123">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="d4383-124">Códigos de erro do Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="d4383-124">Windows Sockets Error Codes</span></span>](windows-sockets-error-codes-2.md)
</dt> <dt>

[<span data-ttu-id="d4383-125">Considerações sobre programação do Winsock</span><span class="sxs-lookup"><span data-stu-id="d4383-125">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> </dl>

 

 



