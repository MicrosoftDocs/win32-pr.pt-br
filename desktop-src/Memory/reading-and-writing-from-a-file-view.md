---
description: Para ler de uma exibição de arquivo, desreferenciar o ponteiro retornado pela função MapViewOfFile, conforme mostrado nos exemplos abaixo.
ms.assetid: c2a3da09-d116-4c2c-9e6c-ec9e80c88b99
title: Lendo e escrevendo de uma exibição de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aee56f1d06e53bdfd6f7571e4ec296da0270ce0a7050b253b5900c4640d6df0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067676"
---
# <a name="reading-and-writing-from-a-file-view"></a>Lendo e escrevendo de uma exibição de arquivo

Para ler de uma exibição de arquivo, desreferenciar o ponteiro retornado pela [**função MapViewOfFile,**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) conforme mostrado nos exemplos abaixo.

Ler ou escrever em uma exibição de arquivo de um arquivo diferente do arquivo de página pode causar uma exceção **EXCEPTION \_ IN PAGE \_ \_ ERROR.** Por exemplo, acessar um arquivo mapeado que reside em um servidor remoto poderá gerar uma exceção se a conexão com o servidor for perdida. Exceções também podem ocorrer devido a um disco completo, uma falha de dispositivo subjacente ou uma falha de alocação de memória. Ao escrever em uma exibição de arquivo, as exceções também podem ocorrer porque o arquivo é compartilhado e um processo diferente travada um intervalo de byte. Para se proteger contra exceções devido a erros de E/S (entrada e saída), todas as tentativas de acessar arquivos mapeados na memória devem ser envolvidas em manipuladores de exceção estruturados. Quando você receber EXCEPTION IN **\_ \_** **PAGE \_ \_ \_ ERROR** no filtro except, certifique-se de que o endereço está dentro do mapeamento que você está acessando no momento. Se sim, recupere ou falhe normalmente; caso contrário, não tratará a exceção.

O exemplo a seguir usa o ponteiro retornado por **MapViewOfFile** para ler da exibição de arquivo:


```C++
  DWORD dwLength;

  __try
  {
    dwLength = *((LPDWORD) lpMapAddress);
  }
  __except(GetExceptionCode()==EXCEPTION_IN_PAGE_ERROR ?
    EXCEPTION_EXECUTE_HANDLER : EXCEPTION_CONTINUE_SEARCH)
  {
    // Failed to read from the view.
  }
```



O exemplo a seguir usa o ponteiro retornado por **MapViewOfFile** para gravar na exibição de arquivo:


```C++
  DWORD dwLength;

  __try
  {
    *((LPDWORD) lpMapAddress) = dwLength;
  }
  __except (GetExceptionCode() == EXCEPTION_IN_PAGE_ERROR ? 
    EXCEPTION_EXECUTE_HANDLER : EXCEPTION_CONTINUE_SEARCH)
  {
    // Failed to write to the view.
  }
```



A [**função FlushViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile) copia o número especificado de bytes da exibição de arquivo para o arquivo físico, sem esperar que a operação de gravação armazenada em cache ocorra:


```C++
  if (!FlushViewOfFile(lpMapAddress, dwBytesToFlush)) 
  {
    printf("Could not flush memory to disk (%d).\n", GetLastError()); 
  }
```



Se você estiver mapeando um arquivo compactado ou esparso em uma partição NTFS, haverá potencial adicional para um erro de E/S ao paginar em uma parte do arquivo. Nesse caso, o espaço de endereço mapeado por [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) pode não ser apoiado pelo espaço em disco alocado. Isso acontece porque um arquivo esparso pode ter regiões de zeros para as quais o NTFS não aloca espaço em disco e um arquivo compactado pode assumir menos espaço em disco do que os dados reais que ele representa. Se você ler ou gravar em uma parte de um arquivo esparso ou compactado que não é apoiado pelo espaço em disco, o sistema operacional poderá tentar alocar espaço em disco. Se o disco estiver cheio, isso poderá resultar em uma exceção que indica um erro de E/S.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tratamento de exceções estruturado](../debug/structured-exception-handling.md)
</dt> </dl>

 

 
