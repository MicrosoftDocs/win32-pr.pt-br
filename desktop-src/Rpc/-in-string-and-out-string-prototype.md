---
title: " no, String e out, protótipo de cadeia de caracteres"
description: O protótipo de função a seguir usa dois parâmetros de um parâmetro \ in, String \ Parameter e an out, String \.
ms.assetid: acb0ec4f-1846-4fa2-98c2-2081b52a8260
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c216197fb33a666029429d98761b3219b27b176
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917619"
---
# <a name="in-string-and-out-string-prototype"></a><span data-ttu-id="4c34f-103">\[no, String \] e \[ out, protótipo de cadeia de caracteres \]</span><span class="sxs-lookup"><span data-stu-id="4c34f-103">\[in, string\] and \[out, string\] Prototype</span></span>

<span data-ttu-id="4c34f-104">O protótipo de função a seguir usa dois parâmetros: um parâmetro \[ [**in**](/windows/desktop/Midl/in), [**String**](/windows/desktop/Midl/string) \] e um \[ parâmetro [**out**](/windows/desktop/Midl/out-idl), **String** \] .</span><span class="sxs-lookup"><span data-stu-id="4c34f-104">The following function prototype uses two parameters: an \[[**in**](/windows/desktop/Midl/in), [**string**](/windows/desktop/Midl/string)\] parameter and an \[[**out**](/windows/desktop/Midl/out-idl), **string**\] parameter.</span></span>

``` syntax
void Analyze(
    [in, string]                       *pszInput,
    [out, string, size_is(STRSIZE)]    *pszOutput);
```

<span data-ttu-id="4c34f-105">O primeiro parâmetro é \[ somente [**no**](/windows/desktop/Midl/in) \] .</span><span class="sxs-lookup"><span data-stu-id="4c34f-105">The first parameter is \[[**in**](/windows/desktop/Midl/in)\] only.</span></span> <span data-ttu-id="4c34f-106">Essa cadeia de caracteres de entrada só é transmitida do cliente para o servidor.</span><span class="sxs-lookup"><span data-stu-id="4c34f-106">This input string is only transmitted from the client to the server.</span></span> <span data-ttu-id="4c34f-107">O servidor usa-o como base para processamento adicional.</span><span class="sxs-lookup"><span data-stu-id="4c34f-107">The server uses it as the basis for further processing.</span></span> <span data-ttu-id="4c34f-108">A cadeia de caracteres não é modificada e não é requerida pelo cliente, portanto, não precisa ser retornada ao cliente.</span><span class="sxs-lookup"><span data-stu-id="4c34f-108">The string is not modified and is not required again by the client, so it does not have to be returned to the client.</span></span>

<span data-ttu-id="4c34f-109">O segundo parâmetro, que representa a resposta do médico, está \[ [**fora**](/windows/desktop/Midl/out-idl) \] apenas.</span><span class="sxs-lookup"><span data-stu-id="4c34f-109">The second parameter, representing the doctor's response, is \[[**out**](/windows/desktop/Midl/out-idl)\] only.</span></span> <span data-ttu-id="4c34f-110">Essa cadeia de caracteres de resposta só é transmitida do servidor para o cliente.</span><span class="sxs-lookup"><span data-stu-id="4c34f-110">This response string is only transmitted from the server to the client.</span></span> <span data-ttu-id="4c34f-111">O tamanho de alocação é fornecido para que os stubs de servidor possam alocar memória para ele.</span><span class="sxs-lookup"><span data-stu-id="4c34f-111">The allocation size is provided so that the server stubs can allocate memory for it.</span></span> <span data-ttu-id="4c34f-112">Como *pszOutput* é um \[ ponteiro de [**referência**](/windows/desktop/Midl/ref) \] , o cliente deve ter memória suficiente alocada para a cadeia de caracteres antes da chamada.</span><span class="sxs-lookup"><span data-stu-id="4c34f-112">Since *pszOutput* is a \[[**ref**](/windows/desktop/Midl/ref)\] pointer, the client must have sufficient memory allocated for the string before the call.</span></span> <span data-ttu-id="4c34f-113">A cadeia de caracteres de resposta é gravada nessa área de memória quando o procedimento remoto retorna.</span><span class="sxs-lookup"><span data-stu-id="4c34f-113">The response string is written into this area of memory when the remote procedure returns.</span></span>

 

 