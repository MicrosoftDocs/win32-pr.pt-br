---
description: Para ler de uma exibição de arquivo, desfaça referência ao ponteiro retornado pela função MapViewOfFile, conforme mostrado nos exemplos abaixo.
ms.assetid: c2a3da09-d116-4c2c-9e6c-ec9e80c88b99
title: Leitura e gravação de uma exibição de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d98ec50dc6cd8b0224f2ba33a17ba80c7b0fc658
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105789786"
---
# <a name="reading-and-writing-from-a-file-view"></a>Leitura e gravação de uma exibição de arquivo

Para ler de uma exibição de arquivo, desfaça referência ao ponteiro retornado pela função [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) , conforme mostrado nos exemplos abaixo.

Ler ou gravar em uma exibição de arquivo de um arquivo que não seja o arquivo de paginação pode causar uma **exceção \_ na exceção de \_ \_ erro de página** . Por exemplo, o acesso a um arquivo mapeado que reside em um servidor remoto pode gerar uma exceção se a conexão com o servidor for perdida. As exceções também podem ocorrer devido a um disco cheio, a uma falha de dispositivo subjacente ou a uma falha de alocação de memória. Ao gravar em uma exibição de arquivo, as exceções também podem ocorrer porque o arquivo é compartilhado e um processo diferente bloqueou um intervalo de bytes. Para proteger contra exceções devido a erros de e/s (entrada e saída), todas as tentativas de acessar arquivos mapeados na memória devem ser encapsuladas em manipuladores de exceção estruturada. Quando você receber **exceção \_ em \_ um \_ erro de página** no filtro **\_ \_ Except** , certifique-se de que o endereço está dentro do mapeamento que você está acessando atualmente. Nesse caso, recupere ou falhe normalmente; caso contrário, não manipule a exceção.

O exemplo a seguir usa o ponteiro retornado por **MapViewOfFile** para ler a partir da exibição de arquivo:


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



O exemplo a seguir usa o ponteiro retornado por **MapViewOfFile** para gravar na exibição do arquivo:


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



A função [**FlushViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile) copia o número especificado de bytes da exibição de arquivo para o arquivo físico, sem esperar que a operação de gravação em cache ocorra:


```C++
  if (!FlushViewOfFile(lpMapAddress, dwBytesToFlush)) 
  {
    printf("Could not flush memory to disk (%d).\n", GetLastError()); 
  }
```



Se você estiver mapeando um arquivo compactado ou esparso em uma partição NTFS, haverá um potencial adicional para um erro de e/s durante a paginação em uma parte do arquivo. Nesse caso, o espaço de endereço mapeado pelo [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) pode não ser apoiado pelo espaço em disco alocado. Isso ocorre porque um arquivo esparso pode ter regiões de zeros para as quais o NTFS não aloca espaço em disco e um arquivo compactado pode ocupar menos espaço em disco do que os dados reais que ele representa. Se você ler ou gravar em uma parte de um arquivo esparso ou compactado que não é apoiado por espaço em disco, o sistema operacional poderá tentar alocar espaço em disco. Se o disco estiver cheio, isso poderá resultar em uma exceção indicando um erro de e/s.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tratamento de exceções estruturado](../debug/structured-exception-handling.md)
</dt> </dl>

 

 
