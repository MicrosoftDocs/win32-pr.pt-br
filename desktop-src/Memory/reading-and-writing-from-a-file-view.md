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
# <a name="reading-and-writing-from-a-file-view"></a><span data-ttu-id="e792d-103">Leitura e gravação de uma exibição de arquivo</span><span class="sxs-lookup"><span data-stu-id="e792d-103">Reading and Writing From a File View</span></span>

<span data-ttu-id="e792d-104">Para ler de uma exibição de arquivo, desfaça referência ao ponteiro retornado pela função [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) , conforme mostrado nos exemplos abaixo.</span><span class="sxs-lookup"><span data-stu-id="e792d-104">To read from a file view, dereference the pointer returned by the [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) function as shown in the examples below.</span></span>

<span data-ttu-id="e792d-105">Ler ou gravar em uma exibição de arquivo de um arquivo que não seja o arquivo de paginação pode causar uma **exceção \_ na exceção de \_ \_ erro de página** .</span><span class="sxs-lookup"><span data-stu-id="e792d-105">Reading from or writing to a file view of a file other than the page file can cause an **EXCEPTION\_IN\_PAGE\_ERROR** exception.</span></span> <span data-ttu-id="e792d-106">Por exemplo, o acesso a um arquivo mapeado que reside em um servidor remoto pode gerar uma exceção se a conexão com o servidor for perdida.</span><span class="sxs-lookup"><span data-stu-id="e792d-106">For example, accessing a mapped file that resides on a remote server can generate an exception if the connection to the server is lost.</span></span> <span data-ttu-id="e792d-107">As exceções também podem ocorrer devido a um disco cheio, a uma falha de dispositivo subjacente ou a uma falha de alocação de memória.</span><span class="sxs-lookup"><span data-stu-id="e792d-107">Exceptions can also occur because of a full disk, an underlying device failure, or a memory allocation failure.</span></span> <span data-ttu-id="e792d-108">Ao gravar em uma exibição de arquivo, as exceções também podem ocorrer porque o arquivo é compartilhado e um processo diferente bloqueou um intervalo de bytes.</span><span class="sxs-lookup"><span data-stu-id="e792d-108">When writing to a file view, exceptions can also occur because the file is shared and a different process has locked a byte range.</span></span> <span data-ttu-id="e792d-109">Para proteger contra exceções devido a erros de e/s (entrada e saída), todas as tentativas de acessar arquivos mapeados na memória devem ser encapsuladas em manipuladores de exceção estruturada.</span><span class="sxs-lookup"><span data-stu-id="e792d-109">To guard against exceptions due to input and output (I/O) errors, all attempts to access memory mapped files should be wrapped in structured exception handlers.</span></span> <span data-ttu-id="e792d-110">Quando você receber **exceção \_ em \_ um \_ erro de página** no filtro **\_ \_ Except** , certifique-se de que o endereço está dentro do mapeamento que você está acessando atualmente.</span><span class="sxs-lookup"><span data-stu-id="e792d-110">When you receive **EXCEPTION\_IN\_PAGE\_ERROR** in your **\_\_except** filter, make sure that the address is within the mapping you are currently accessing.</span></span> <span data-ttu-id="e792d-111">Nesse caso, recupere ou falhe normalmente; caso contrário, não manipule a exceção.</span><span class="sxs-lookup"><span data-stu-id="e792d-111">If so, recover or fail gracefully; otherwise, do not handle the exception.</span></span>

<span data-ttu-id="e792d-112">O exemplo a seguir usa o ponteiro retornado por **MapViewOfFile** para ler a partir da exibição de arquivo:</span><span class="sxs-lookup"><span data-stu-id="e792d-112">The following example uses the pointer returned by **MapViewOfFile** to read from the file view:</span></span>


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



<span data-ttu-id="e792d-113">O exemplo a seguir usa o ponteiro retornado por **MapViewOfFile** para gravar na exibição do arquivo:</span><span class="sxs-lookup"><span data-stu-id="e792d-113">The following example uses the pointer returned by **MapViewOfFile** to write to the file view:</span></span>


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



<span data-ttu-id="e792d-114">A função [**FlushViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile) copia o número especificado de bytes da exibição de arquivo para o arquivo físico, sem esperar que a operação de gravação em cache ocorra:</span><span class="sxs-lookup"><span data-stu-id="e792d-114">The [**FlushViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile) function copies the specified number of bytes of the file view to the physical file, without waiting for the cached write operation to occur:</span></span>


```C++
  if (!FlushViewOfFile(lpMapAddress, dwBytesToFlush)) 
  {
    printf("Could not flush memory to disk (%d).\n", GetLastError()); 
  }
```



<span data-ttu-id="e792d-115">Se você estiver mapeando um arquivo compactado ou esparso em uma partição NTFS, haverá um potencial adicional para um erro de e/s durante a paginação em uma parte do arquivo.</span><span class="sxs-lookup"><span data-stu-id="e792d-115">If you are mapping a compressed or sparse file on an NTFS partition, there is additional potential for an I/O error when paging in a portion of the file.</span></span> <span data-ttu-id="e792d-116">Nesse caso, o espaço de endereço mapeado pelo [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) pode não ser apoiado pelo espaço em disco alocado.</span><span class="sxs-lookup"><span data-stu-id="e792d-116">In this case, the address space mapped by [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) may not be backed by allocated disk space.</span></span> <span data-ttu-id="e792d-117">Isso ocorre porque um arquivo esparso pode ter regiões de zeros para as quais o NTFS não aloca espaço em disco e um arquivo compactado pode ocupar menos espaço em disco do que os dados reais que ele representa.</span><span class="sxs-lookup"><span data-stu-id="e792d-117">This is because a sparse file can have regions of zeros for which NTFS does not allocate disk space, and a compressed file can take up less disk space than the actual data that it represents.</span></span> <span data-ttu-id="e792d-118">Se você ler ou gravar em uma parte de um arquivo esparso ou compactado que não é apoiado por espaço em disco, o sistema operacional poderá tentar alocar espaço em disco.</span><span class="sxs-lookup"><span data-stu-id="e792d-118">If you read from or write to a portion of a sparse or compressed file that is not backed by disk space, the operating system may try to allocate disk space.</span></span> <span data-ttu-id="e792d-119">Se o disco estiver cheio, isso poderá resultar em uma exceção indicando um erro de e/s.</span><span class="sxs-lookup"><span data-stu-id="e792d-119">If the disk is full, this can result in an exception indicating an I/O error.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e792d-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e792d-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e792d-121">Tratamento de exceções estruturado</span><span class="sxs-lookup"><span data-stu-id="e792d-121">Structured Exception Handling</span></span>](../debug/structured-exception-handling.md)
</dt> </dl>

 

 
