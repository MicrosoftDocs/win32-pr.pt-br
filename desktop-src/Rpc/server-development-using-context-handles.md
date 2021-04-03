---
title: Desenvolvimento de servidor usando identificadores de contexto
description: Da perspectiva do desenvolvimento do programa de servidor, um identificador de contexto é um ponteiro não tipado. Os programas de servidor inicializam identificadores de contexto apontando-os em dados na memória ou em alguma outra forma de armazenamento (como arquivos em discos).
ms.assetid: 6a1aabca-4cb9-401c-90c7-0cff7a69b7b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f743a4a6aa4a2aa7b6987bb54dc56e55cffbc76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005962"
---
# <a name="server-development-using-context-handles"></a><span data-ttu-id="ad6ad-104">Desenvolvimento de servidor usando identificadores de contexto</span><span class="sxs-lookup"><span data-stu-id="ad6ad-104">Server Development Using Context Handles</span></span>

<span data-ttu-id="ad6ad-105">Da perspectiva do desenvolvimento do programa de servidor, um identificador de contexto é um ponteiro não tipado.</span><span class="sxs-lookup"><span data-stu-id="ad6ad-105">From the perspective of server program development, a context handle is an untyped pointer.</span></span> <span data-ttu-id="ad6ad-106">Os programas de servidor inicializam identificadores de contexto apontando-os em dados na memória ou em alguma outra forma de armazenamento (como arquivos em discos).</span><span class="sxs-lookup"><span data-stu-id="ad6ad-106">Server programs initialize context handles by pointing them at data in memory or on some other form of storage (such as files on disks).</span></span>

<span data-ttu-id="ad6ad-107">Por exemplo, suponha que um cliente use um identificador de contexto para solicitar uma série de atualizações para um registro em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ad6ad-107">For instance, suppose that a client uses a context handle to request a series of updates to a record in a database.</span></span> <span data-ttu-id="ad6ad-108">O cliente chama um procedimento remoto no servidor e passa a ele uma chave de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="ad6ad-108">The client calls a remote procedure on the server and passes it a search key.</span></span> <span data-ttu-id="ad6ad-109">O programa de servidor pesquisa o banco de dados para a chave de pesquisa e Obtém o número de registro inteiro do registro correspondente.</span><span class="sxs-lookup"><span data-stu-id="ad6ad-109">The server program searches the database for the search key and obtains the integer record number of the matching record.</span></span> <span data-ttu-id="ad6ad-110">Em seguida, o servidor pode apontar um ponteiro para void em um local da memória que contém o número do registro.</span><span class="sxs-lookup"><span data-stu-id="ad6ad-110">The server can then point a pointer to void at a memory location containing the record number.</span></span> <span data-ttu-id="ad6ad-111">Quando ele retorna, o procedimento remoto precisaria retornar o ponteiro como um identificador de contexto por meio de seu valor de retorno ou sua lista de parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ad6ad-111">When it returns, the remote procedure would need to return the pointer as a context handle through its return value or its parameter list.</span></span> <span data-ttu-id="ad6ad-112">O cliente precisaria passar o ponteiro para o servidor cada vez que ele chamou procedimentos remotos para atualizar o registro.</span><span class="sxs-lookup"><span data-stu-id="ad6ad-112">The client would need to pass the pointer to the server each time it called remote procedures to update the record.</span></span> <span data-ttu-id="ad6ad-113">Durante cada uma dessas operações de atualização, o servidor converteria o ponteiro void para ser um ponteiro para um inteiro.</span><span class="sxs-lookup"><span data-stu-id="ad6ad-113">During each of these update operations, the server would cast the void pointer to be a pointer to an integer.</span></span>

<span data-ttu-id="ad6ad-114">Depois que o programa do servidor apontar o identificador de contexto nos dados de contexto, o identificador será considerado aberto.</span><span class="sxs-lookup"><span data-stu-id="ad6ad-114">After the server program points the context handle at context data, the handle is considered opened.</span></span> <span data-ttu-id="ad6ad-115">Identificadores contendo um valor **nulo** são fechados.</span><span class="sxs-lookup"><span data-stu-id="ad6ad-115">Handles containing a **NULL** value are closed.</span></span> <span data-ttu-id="ad6ad-116">O servidor mantém um identificador de contexto aberto até que o cliente chame um procedimento remoto que o feche.</span><span class="sxs-lookup"><span data-stu-id="ad6ad-116">The server maintains an opened context handle until the client calls a remote procedure that closes it.</span></span> <span data-ttu-id="ad6ad-117">Se a sessão do cliente for encerrada enquanto o identificador estiver aberto, o tempo de execução do RPC chamará a rotina de execução do servidor para liberar o identificador.</span><span class="sxs-lookup"><span data-stu-id="ad6ad-117">If the client session terminates while the handle is open, the RPC run time calls the server run-down routine to free the handle.</span></span>

<span data-ttu-id="ad6ad-118">O fragmento de código a seguir demonstra como um servidor pode implementar um identificador de contexto.</span><span class="sxs-lookup"><span data-stu-id="ad6ad-118">The following code fragment demonstrates how a server might implement a context handle.</span></span> <span data-ttu-id="ad6ad-119">Neste exemplo, o servidor mantém um arquivo de dados que o cliente grava para usar procedimentos remotos.</span><span class="sxs-lookup"><span data-stu-id="ad6ad-119">In this example, the server maintains a data file that the client writes to using remote procedures.</span></span> <span data-ttu-id="ad6ad-120">As informações de contexto são um identificador de arquivo que controla o local atual no arquivo em que o servidor gravará os dados.</span><span class="sxs-lookup"><span data-stu-id="ad6ad-120">The context information is a file handle that keeps track of the current location in the file where the server will write data.</span></span> <span data-ttu-id="ad6ad-121">O identificador de arquivo é empacotado como um identificador de contexto na lista de parâmetros para chamadas de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="ad6ad-121">The file handle is packaged as a context handle in the parameter list to remote procedure calls.</span></span> <span data-ttu-id="ad6ad-122">Uma estrutura contém o nome do arquivo e o identificador do arquivo.</span><span class="sxs-lookup"><span data-stu-id="ad6ad-122">A structure contains the file name and the file handle.</span></span> <span data-ttu-id="ad6ad-123">A definição de interface para este exemplo é mostrada em [desenvolvimento de interface usando identificadores de contexto](interface-development-using-context-handles.md).</span><span class="sxs-lookup"><span data-stu-id="ad6ad-123">The interface definition for this example is shown in [Interface Development Using Context Handles](interface-development-using-context-handles.md).</span></span>


```C++
/* cxhndlp.c (fragment of file containing remote procedures) */
typedef struct 
{
     FILE* hFile;
     char   achFile[256];
} FILE_CONTEXT_TYPE;
```



<span data-ttu-id="ad6ad-124">A função RemoteOpen abre um arquivo no servidor:</span><span class="sxs-lookup"><span data-stu-id="ad6ad-124">The function RemoteOpen opens a file on the server:</span></span>


```C++
short RemoteOpen(
    PPCONTEXT_HANDLE_TYPE pphContext,
    unsigned char *pszFileName)
{
    FILE               *hFile;
    FILE_CONTEXT_TYPE  *pFileContext;
 
    if ((hFile = fopen(pszFileName, "r")) == NULL) 
    {
        *pphContext = (PCONTEXT_HANDLE_TYPE) NULL;
        return(-1);
    }
    else 
    {
        pFileContext = (FILE_CONTEXT_TYPE *) 
                       MIDL_user_allocate(sizeof(FILE_CONTEXT_TYPE));
        pFileContext->hFile = hFile;
        // check if pszFileName is longer than 256 and if yes, return
        // an error
        strcpy_s(pFileContext->achFile, srlen(pszFileName), pszFileName);
        *pphContext = (PCONTEXT_HANDLE_TYPE) pFileContext;
        return(0);
    }
}
```



<span data-ttu-id="ad6ad-125">A função RemoteRead lê um arquivo no servidor.</span><span class="sxs-lookup"><span data-stu-id="ad6ad-125">The function RemoteRead reads a file on the server.</span></span>


```C++
short RemoteRead(
    PCONTEXT_HANDLE_TYPE phContext, 
    unsigned char *pbBuf, 
    short *pcbBuf) 
{ 
    FILE_CONTEXT_TYPE *pFileContext; 
    printf("in RemoteRead\n"); 
    pFileContext = (FILE_CONTEXT_TYPE *) phContext; 
    *pcbBuf = (short) fread(pbBuf, sizeof(char), 
                            BUFSIZE, 
                            pFileContext->hFile); 
    return(*pcbBuf); 
}
```



<span data-ttu-id="ad6ad-126">A função RemoteClose fecha um arquivo no servidor.</span><span class="sxs-lookup"><span data-stu-id="ad6ad-126">The function RemoteClose closes a file on the server.</span></span> <span data-ttu-id="ad6ad-127">Observe que o aplicativo de servidor precisa atribuir **NULL** ao identificador de contexto como parte da função close.</span><span class="sxs-lookup"><span data-stu-id="ad6ad-127">Note that the server application has to assign **NULL** to the context handle as part of the close function.</span></span> <span data-ttu-id="ad6ad-128">Isso se comunica com o stub do servidor e a biblioteca de tempo de execução RPC que o identificador de contexto foi excluído.</span><span class="sxs-lookup"><span data-stu-id="ad6ad-128">This communicates to the server stub and the RPC run-time library that the context handle has been deleted.</span></span> <span data-ttu-id="ad6ad-129">Caso contrário, a conexão será mantida aberta e, eventualmente, uma execução de contexto ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="ad6ad-129">Otherwise, the connection will be kept open and eventually a context run-down will occur.</span></span>


```C++
void RemoteClose(PPCONTEXT_HANDLE_TYPE pphContext)
{
    FILE_CONTEXT_TYPE *pFileContext;
 
    if (*pphContext == NULL)
    {
        //Log error, client tried to close a NULL handle.
        return;
    }
    pFileContext = (FILE_CONTEXT_TYPE *)*pphContext;
    printf("File %s closed.\n", pFileContext->achFile);
    fclose(pFileConext->hFile);
    MIDL_user_free(pFileContext);
 
    // This tells the run-time, when it is marshalling the out 
    // parameters, that the context handle has been closed normally.
    *pphContext = NULL;
}
```



> [!Note]  
> <span data-ttu-id="ad6ad-130">Embora seja esperado que o cliente passe um identificador de contexto válido para uma chamada com \[ \] atributos direcionais in, out, o RPC não rejeita identificadores de contexto **nulo** para essa combinação de atributos direcionais.</span><span class="sxs-lookup"><span data-stu-id="ad6ad-130">While it is expected the client passes a valid context handle to a call with \[in, out\] directional attributes, RPC does not reject **NULL** context handles for this combination of directional attributes.</span></span> <span data-ttu-id="ad6ad-131">O identificador de contexto **nulo** é passado para o servidor como um ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="ad6ad-131">The **NULL** context handle is passed to the server as a **NULL** pointer.</span></span> <span data-ttu-id="ad6ad-132">O código do servidor para chamadas contendo um \[ identificador de contexto in, out \] deve ser escrito para evitar uma violação de acesso quando um ponteiro **NULL** é recebido.</span><span class="sxs-lookup"><span data-stu-id="ad6ad-132">The server code for calls containing an \[in, out\] context handle should be written to avoid an access violation when a **NULL** pointer is received.</span></span>

 

 

 




