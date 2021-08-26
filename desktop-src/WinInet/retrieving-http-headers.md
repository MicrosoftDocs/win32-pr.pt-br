---
title: Recuperando cabeçalhos HTTP
description: Este tutorial descreve como recuperar informações de cabeçalho de solicitações HTTP.
ms.assetid: 347e4fb3-5f96-488a-bef8-4df0b8d1ade1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba9c1dbae3447d5ae44c8d348394f2dc802ed9d7b4af7d99fde19d0b5d2c3d22
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955506"
---
# <a name="retrieving-http-headers"></a>Recuperando cabeçalhos HTTP

Este tutorial descreve como recuperar informações de cabeçalho de solicitações HTTP.

## <a name="implementation-steps"></a>Etapas de implementação

Há duas maneiras de recuperar as informações de cabeçalho:

-   Use uma das constantes de [**sinalizador de informações de consulta**](query-info-flags.md) associadas ao cabeçalho HTTP que seu aplicativo precisa.
-   Use o \_ sinalizador de \_ atributo personalizado de consulta http e passe o nome do cabeçalho http.

Usar a constante associada ao cabeçalho HTTP que seu aplicativo precisa é mais rápido internamente, mas pode haver cabeçalhos HTTP que não têm uma constante associada a eles. Para esses casos, o método que usa o \_ sinalizador de atributo personalizado de consulta http \_ está disponível.

Ambos os métodos usam a função [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) . [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) usa o identificador [**HINTERNET**](appendix-a-hinternet-handles.md) no qual a solicitação HTTP foi feita, um atributo, um buffer, um valor DWORD que contém o tamanho do buffer e um valor de índice. Um modificador também pode ser adicionado ao atributo passado para [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) para indicar em qual formato os dados devem ser retornados.

### <a name="retrieving-headers-using-a-constant"></a>Recuperando cabeçalhos usando uma constante

Para usar a função [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) para recuperar um cabeçalho HTTP usando uma constante, siga estas etapas:

1.  Chame [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) com uma constante da lista de [**atributos**](query-info-flags.md) , um buffer **nulo** e a variável que mantém o tamanho do buffer definido como zero. Além disso, se seu aplicativo precisar dos dados em um formato específico, você poderá adicionar uma constante da lista de [**modificadores**](query-info-flags.md) .
2.  Se o cabeçalho HTTP solicitado existir, a chamada para [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) deve falhar, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) deve retornar um \_ buffer insuficiente de erro \_ e a variável passada para o parâmetro *lpdwBufferLength* deve ser definida como o número de bytes necessários.
3.  Aloque um buffer com o número de bytes necessários.
4.  Repita a chamada para [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa).

O exemplo a seguir demonstra uma chamada para [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) usando os \_ \_ cabeçalhos brutos de consulta http \_ \_ CRLF constante, que é um valor especial que solicita todos os cabeçalhos HTTP retornados.


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



### <a name="retrieving-headers-using-http_query_custom"></a>Recuperando cabeçalhos usando a \_ consulta http \_ personalizada

Para usar a função [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) para recuperar um cabeçalho HTTP usando a \_ consulta http \_ personalizada, siga estas etapas:

1.  Aloque um buffer que seja grande o suficiente para conter o nome da cadeia de caracteres do cabeçalho HTTP.
2.  Grave o nome da cadeia de caracteres do cabeçalho HTTP no buffer.
3.  Chame [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) com a \_ consulta http \_ personalizada, o buffer que contém o nome da cadeia de caracteres do cabeçalho HTTP e a variável que mantém o tamanho do buffer. Além disso, se seu aplicativo precisar dos dados em um formato específico, você poderá adicionar uma constante da lista de [**modificadores**](query-info-flags.md) .
4.  Se a chamada para [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) falhar e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornar um erro de \_ buffer insuficiente \_ , realoque um buffer com o número de bytes necessário.
5.  Grave o nome da cadeia de caracteres do cabeçalho HTTP no buffer novamente.
6.  Repita a chamada para [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa).

O exemplo a seguir demonstra uma chamada para [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) usando a \_ constante personalizada de consulta http \_ para solicitar o cabeçalho HTTP do tipo de conteúdo.


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
> O WinINet não oferece suporte a implementações de servidor. Além disso, ele não deve ser usado de um serviço. para implementações de servidor ou serviços, use [o Microsoft Windows HTTP services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 