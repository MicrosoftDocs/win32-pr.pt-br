---
title: Recuperando cabeçalhos HTTP
description: Este tutorial descreve como recuperar informações de cabeçalho de solicitações HTTP.
ms.assetid: 347e4fb3-5f96-488a-bef8-4df0b8d1ade1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5b31043940b8c2127d1cfa1696d2821641d0784
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105749131"
---
# <a name="retrieving-http-headers"></a><span data-ttu-id="f5499-103">Recuperando cabeçalhos HTTP</span><span class="sxs-lookup"><span data-stu-id="f5499-103">Retrieving HTTP Headers</span></span>

<span data-ttu-id="f5499-104">Este tutorial descreve como recuperar informações de cabeçalho de solicitações HTTP.</span><span class="sxs-lookup"><span data-stu-id="f5499-104">This tutorial describes how to retrieve header information from HTTP requests.</span></span>

## <a name="implementation-steps"></a><span data-ttu-id="f5499-105">Etapas de implementação</span><span class="sxs-lookup"><span data-stu-id="f5499-105">Implementation Steps</span></span>

<span data-ttu-id="f5499-106">Há duas maneiras de recuperar as informações de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="f5499-106">There are two ways to retrieve the header information:</span></span>

-   <span data-ttu-id="f5499-107">Use uma das constantes de [**sinalizador de informações de consulta**](query-info-flags.md) associadas ao cabeçalho HTTP que seu aplicativo precisa.</span><span class="sxs-lookup"><span data-stu-id="f5499-107">Use one of the [**Query Info Flag**](query-info-flags.md) constants associated with the HTTP header that your application needs.</span></span>
-   <span data-ttu-id="f5499-108">Use o \_ sinalizador de \_ atributo personalizado de consulta http e passe o nome do cabeçalho http.</span><span class="sxs-lookup"><span data-stu-id="f5499-108">Use the HTTP\_QUERY\_CUSTOM attribute flag and pass the name of the HTTP header.</span></span>

<span data-ttu-id="f5499-109">Usar a constante associada ao cabeçalho HTTP que seu aplicativo precisa é mais rápido internamente, mas pode haver cabeçalhos HTTP que não têm uma constante associada a eles.</span><span class="sxs-lookup"><span data-stu-id="f5499-109">Using the constant associated with the HTTP header that your application needs is faster internally, but there might be HTTP headers that do not have a constant associated with them.</span></span> <span data-ttu-id="f5499-110">Para esses casos, o método que usa o \_ sinalizador de atributo personalizado de consulta http \_ está disponível.</span><span class="sxs-lookup"><span data-stu-id="f5499-110">For those cases, the method using the HTTP\_QUERY\_CUSTOM attribute flag is available.</span></span>

<span data-ttu-id="f5499-111">Ambos os métodos usam a função [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) .</span><span class="sxs-lookup"><span data-stu-id="f5499-111">Both methods use the [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) function.</span></span> <span data-ttu-id="f5499-112">[**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) usa o identificador [**HINTERNET**](appendix-a-hinternet-handles.md) no qual a solicitação HTTP foi feita, um atributo, um buffer, um valor DWORD que contém o tamanho do buffer e um valor de índice.</span><span class="sxs-lookup"><span data-stu-id="f5499-112">[**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) takes the [**HINTERNET**](appendix-a-hinternet-handles.md) handle on which the HTTP request was made, one attribute, a buffer, a DWORD value that contains the buffer size, and an index value.</span></span> <span data-ttu-id="f5499-113">Um modificador também pode ser adicionado ao atributo passado para [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) para indicar em qual formato os dados devem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="f5499-113">A modifier can also be added to the attribute passed to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) to indicate in what format the data should be returned.</span></span>

### <a name="retrieving-headers-using-a-constant"></a><span data-ttu-id="f5499-114">Recuperando cabeçalhos usando uma constante</span><span class="sxs-lookup"><span data-stu-id="f5499-114">Retrieving Headers Using a Constant</span></span>

<span data-ttu-id="f5499-115">Para usar a função [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) para recuperar um cabeçalho HTTP usando uma constante, siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="f5499-115">To use the [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) function to retrieve an HTTP header using a constant, follow these steps:</span></span>

1.  <span data-ttu-id="f5499-116">Chame [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) com uma constante da lista de [**atributos**](query-info-flags.md) , um buffer **nulo** e a variável que mantém o tamanho do buffer definido como zero.</span><span class="sxs-lookup"><span data-stu-id="f5499-116">Call [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) with a constant from the [**Attributes**](query-info-flags.md) list, a **NULL** buffer, and the variable that holds the buffer size set to zero.</span></span> <span data-ttu-id="f5499-117">Além disso, se seu aplicativo precisar dos dados em um formato específico, você poderá adicionar uma constante da lista de [**modificadores**](query-info-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="f5499-117">Also, if your application needs the data in a particular format, you can add a constant from the [**Modifiers**](query-info-flags.md) list.</span></span>
2.  <span data-ttu-id="f5499-118">Se o cabeçalho HTTP solicitado existir, a chamada para [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) deve falhar, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) deve retornar um \_ buffer insuficiente de erro \_ e a variável passada para o parâmetro *lpdwBufferLength* deve ser definida como o número de bytes necessários.</span><span class="sxs-lookup"><span data-stu-id="f5499-118">If the requested HTTP header exists, the call to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) should fail, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) should return ERROR\_INSUFFICIENT\_BUFFER, and the variable passed for the *lpdwBufferLength* parameter should be set to the number of bytes required.</span></span>
3.  <span data-ttu-id="f5499-119">Aloque um buffer com o número de bytes necessários.</span><span class="sxs-lookup"><span data-stu-id="f5499-119">Allocate a buffer with the number of bytes required.</span></span>
4.  <span data-ttu-id="f5499-120">Repita a chamada para [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa).</span><span class="sxs-lookup"><span data-stu-id="f5499-120">Retry the call to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa).</span></span>

<span data-ttu-id="f5499-121">O exemplo a seguir demonstra uma chamada para [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) usando os \_ \_ cabeçalhos brutos de consulta http \_ \_ CRLF constante, que é um valor especial que solicita todos os cabeçalhos HTTP retornados.</span><span class="sxs-lookup"><span data-stu-id="f5499-121">The following sample demonstrates a call to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) using the HTTP\_QUERY\_RAW\_HEADERS\_CRLF constant, which is a special value that requests all of the returned HTTP headers.</span></span>


```C++
// Retrieving Headers Using a Constant
BOOL SampleCodeOne(HINTERNET hHttp)
{
   LPVOID lpOutBuffer=NULL;
   DWORD dwSize = 0;

retry:

   // This call will fail on the first pass, because
   // no buffer is allocated.
   if(!HttpQueryInfo(hHttp,HTTP_QUERY_RAW_HEADERS_CRLF,
      (LPVOID)lpOutBuffer,&dwSize,NULL))
   {
      if (GetLastError()==ERROR_HTTP_HEADER_NOT_FOUND)
      {
         // Code to handle the case where the header isn't available.
         return TRUE;
      }
      else
      {
        // Check for an insufficient buffer.
        if (GetLastError()==ERROR_INSUFFICIENT_BUFFER)
        {
            // Allocate the necessary buffer.
            lpOutBuffer = new char[dwSize];

            // Retry the call.
            goto retry;
        }
        else
        {
            // Error handling code.
            if (lpOutBuffer)
            {
               delete [] lpOutBuffer;
            }
            return FALSE;
        }
      }
   }

   if (lpOutBuffer)
   {
      delete [] lpOutBuffer;
   }

   return TRUE;
}
```



### <a name="retrieving-headers-using-http_query_custom"></a><span data-ttu-id="f5499-122">Recuperando cabeçalhos usando a \_ consulta http \_ personalizada</span><span class="sxs-lookup"><span data-stu-id="f5499-122">Retrieving Headers Using HTTP\_QUERY\_CUSTOM</span></span>

<span data-ttu-id="f5499-123">Para usar a função [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) para recuperar um cabeçalho HTTP usando a \_ consulta http \_ personalizada, siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="f5499-123">To use the [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) function to retrieve an HTTP header using HTTP\_QUERY\_CUSTOM, follow these steps:</span></span>

1.  <span data-ttu-id="f5499-124">Aloque um buffer que seja grande o suficiente para conter o nome da cadeia de caracteres do cabeçalho HTTP.</span><span class="sxs-lookup"><span data-stu-id="f5499-124">Allocate a buffer that is large enough to hold the string name of the HTTP header.</span></span>
2.  <span data-ttu-id="f5499-125">Grave o nome da cadeia de caracteres do cabeçalho HTTP no buffer.</span><span class="sxs-lookup"><span data-stu-id="f5499-125">Write the string name of the HTTP header into the buffer.</span></span>
3.  <span data-ttu-id="f5499-126">Chame [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) com a \_ consulta http \_ personalizada, o buffer que contém o nome da cadeia de caracteres do cabeçalho HTTP e a variável que mantém o tamanho do buffer.</span><span class="sxs-lookup"><span data-stu-id="f5499-126">Call [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) with HTTP\_QUERY\_CUSTOM, the buffer that contains the string name of the HTTP header, and the variable that holds the buffer size.</span></span> <span data-ttu-id="f5499-127">Além disso, se seu aplicativo precisar dos dados em um formato específico, você poderá adicionar uma constante da lista de [**modificadores**](query-info-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="f5499-127">Also, if your application needs the data in a particular format, you can add a constant from the [**Modifiers**](query-info-flags.md) list.</span></span>
4.  <span data-ttu-id="f5499-128">Se a chamada para [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) falhar e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornar um erro de \_ buffer insuficiente \_ , realoque um buffer com o número de bytes necessário.</span><span class="sxs-lookup"><span data-stu-id="f5499-128">If the call to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) fails and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER, reallocate a buffer with the number of bytes required.</span></span>
5.  <span data-ttu-id="f5499-129">Grave o nome da cadeia de caracteres do cabeçalho HTTP no buffer novamente.</span><span class="sxs-lookup"><span data-stu-id="f5499-129">Write the string name of the HTTP header into the buffer again.</span></span>
6.  <span data-ttu-id="f5499-130">Repita a chamada para [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa).</span><span class="sxs-lookup"><span data-stu-id="f5499-130">Retry the call to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa).</span></span>

<span data-ttu-id="f5499-131">O exemplo a seguir demonstra uma chamada para [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) usando a \_ constante personalizada de consulta http \_ para solicitar o cabeçalho HTTP do tipo de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="f5499-131">The following sample demonstrates a call to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) using the HTTP\_QUERY\_CUSTOM constant to request the Content-Type HTTP header.</span></span>


```C++
// Retrieving Headers Using HTTP_QUERY_CUSTOM
BOOL SampleCodeTwo(HINTERNET hHttp)
{
    DWORD dwSize = 20;
    LPVOID lpOutBuffer = new char[dwSize];

    StringCchPrintfA((LPSTR)lpOutBuffer,dwSize,"Content-Type");

retry:

    if(!HttpQueryInfo(hHttp,HTTP_QUERY_CUSTOM,
        (LPVOID)lpOutBuffer,&dwSize,NULL))
    {
        if (GetLastError()==ERROR_HTTP_HEADER_NOT_FOUND)
        {
            // Code to handle the case where the header isn't available.
            delete [] lpOutBuffer;
            return TRUE;
        }
        else
        {
            // Check for an insufficient buffer.
            if (GetLastError()==ERROR_INSUFFICIENT_BUFFER)
            {
                // Allocate the necessary buffer.
                delete [] lpOutBuffer;
                lpOutBuffer = new char[dwSize];

                // Rewrite the header name in the buffer.
                StringCchPrintfA((LPSTR)lpOutBuffer,
                                 dwSize,"Content-Type");

                // Retry the call.
                goto retry;
            }
            else
            {
                // Error handling code.
                delete [] lpOutBuffer;
                return FALSE;
            }
        }
    }

   return TRUE;
}
```



> [!Note]  
> <span data-ttu-id="f5499-132">O WinINet não oferece suporte a implementações de servidor.</span><span class="sxs-lookup"><span data-stu-id="f5499-132">WinINet does not support server implementations.</span></span> <span data-ttu-id="f5499-133">Além disso, ele não deve ser usado de um serviço.</span><span class="sxs-lookup"><span data-stu-id="f5499-133">In addition, it should not be used from a service.</span></span> <span data-ttu-id="f5499-134">Para implementações de servidor ou serviços, use [o Microsoft Windows http Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="f5499-134">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 