---
title: Definindo pipes em arquivos IDL
description: Quando um pipe é definido em um arquivo IDL, o compilador MIDL gera uma estrutura de controle de pipe cujos membros são ponteiros para procedimentos de push, pull e alocação, bem como uma variável de estado que coordena esses procedimentos.
ms.assetid: f6c282e4-3056-48c4-bd12-dfcae6d238d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 115be7fc5d00458d13df102afebe9ba5b55de070
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366383"
---
# <a name="defining-pipes-in-idl-files"></a><span data-ttu-id="3194c-103">Definindo pipes em arquivos IDL</span><span class="sxs-lookup"><span data-stu-id="3194c-103">Defining Pipes in IDL Files</span></span>

<span data-ttu-id="3194c-104">Quando um pipe é definido em um arquivo IDL, o compilador MIDL gera uma estrutura de controle de pipe cujos membros são ponteiros para procedimentos de push, pull e alocação, bem como uma variável de estado que coordena esses procedimentos.</span><span class="sxs-lookup"><span data-stu-id="3194c-104">When a pipe is defined in an IDL file, the MIDL compiler generates a pipe control structure whose members are pointers to push, pull, and alloc procedures as well as a state variable that coordinates these procedures.</span></span> <span data-ttu-id="3194c-105">O aplicativo cliente Inicializa os campos na estrutura de controle de pipe, mantém sua variável de estado e gerencia a transferência de dados com suas próprias funções Push, pull e Alloc.</span><span class="sxs-lookup"><span data-stu-id="3194c-105">The client application initializes the fields in the pipe control structure, maintains its state variable, and manages the data transfer with its own push, pull, and alloc functions.</span></span> <span data-ttu-id="3194c-106">O código stub do cliente chama essas funções de aplicativo em loops durante a transferência de dados.</span><span class="sxs-lookup"><span data-stu-id="3194c-106">The client stub code calls these application functions in loops during data transfer.</span></span> <span data-ttu-id="3194c-107">Para um pipe de entrada, o stub do cliente realiza marshaling dos dados de transferência e os transmite para o stub do servidor.</span><span class="sxs-lookup"><span data-stu-id="3194c-107">For an input pipe, the client stub marshals the transfer data and transmits it to the server stub.</span></span> <span data-ttu-id="3194c-108">Para um pipe de saída, o stub do cliente desempacota os dados em um buffer e passa um ponteiro para esse buffer de volta para o aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="3194c-108">For an output pipe, the client stub unmarshals the data into a buffer and passes a pointer to that buffer back to the client application.</span></span>

<span data-ttu-id="3194c-109">O código stub do servidor inicializa os campos da estrutura de controle de pipe para uma variável de estado, bem como ponteiros para as rotinas de push e pull.</span><span class="sxs-lookup"><span data-stu-id="3194c-109">The server stub code initializes the fields of the pipe control structure to a state variable, as well as pointers to push and pull routines.</span></span> <span data-ttu-id="3194c-110">O stub do servidor mantém o estado e gerencia seu armazenamento privado para os dados de transferência.</span><span class="sxs-lookup"><span data-stu-id="3194c-110">The server stub maintains the state and manages its private storage for the transfer data.</span></span> <span data-ttu-id="3194c-111">O aplicativo de servidor chama as rotinas de pull e Push em loops durante a chamada de procedimento remoto, pois recebe e desempacota dados do stub do cliente, ou realiza marshaling e transmite dados para o stub do cliente.</span><span class="sxs-lookup"><span data-stu-id="3194c-111">The server application calls the pull and push routines in loops during the remote procedure call as it receives and unmarshals data from the client stub, or marshals and transmits data to the client stub.</span></span>

<span data-ttu-id="3194c-112">O arquivo IDL de exemplo a seguir define um pipe longo de tipo de pipe \_ , cujo tamanho de elemento é definido como **longo**.</span><span class="sxs-lookup"><span data-stu-id="3194c-112">The following example IDL file defines a pipe type LONG\_PIPE, whose element size is defined as **long**.</span></span> <span data-ttu-id="3194c-113">Ele também declara protótipos de função para o procedimento remoto chamar inpipe e outpipe, para enviar e receber dados, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="3194c-113">It also declares function prototypes for the remote procedure calls InPipe and OutPipe, to send and receive data, respectively.</span></span> <span data-ttu-id="3194c-114">Quando o compilador MIDL processa o arquivo IDL, ele gera o arquivo de cabeçalho mostrado no exemplo.</span><span class="sxs-lookup"><span data-stu-id="3194c-114">When the MIDL compiler processes the IDL file, it generates the header file shown in the example.</span></span>

## <a name="example"></a><span data-ttu-id="3194c-115">Exemplo</span><span class="sxs-lookup"><span data-stu-id="3194c-115">Example</span></span>

``` syntax
// File: pipedemo.idl
typedef pipe long LONG_PIPE;
void InPipe( [in] LONG_PIPE pipe_data );
void OutPipe( [out] LONG_PIPE *pipe_data ); 
//end pipedemo.idl
 
// File: pipedemo.h (fragment)
// Generated by the MIDL compiler from pipedemo.idl
typedef struct pipe_LONG_PIPE
{
    void (__RPC_FAR * pull) (
        char __RPC_FAR * state,
        long __RPC_FAR * buf,
        unsigned long esize,
        unsigned long __RPC_FAR * ecount );
    void (__RPC_FAR * push) (
        char __RPC_FAR * state,
        long __RPC_FAR * buf,
        unsigned long ecount );
    void (__RPC_FAR * alloc) (
        char __RPC_FAR * state,
        unsigned long bsize,
        long __RPC_FAR * __RPC_FAR * buf,
        unsigned long __RPC_FAR * bcount );
    char __RPC_FAR * state;
} LONG_PIPE;
 
void InPipe( 
    /* [in] */ LONG_PIPE pipe_data);
void OutPipe( 
    /* [out] */ LONG_PIPE __RPC_FAR *pipe_data);
//end pipedemo.h
```

## <a name="related-topics"></a><span data-ttu-id="3194c-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3194c-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3194c-117">pipe</span><span class="sxs-lookup"><span data-stu-id="3194c-117">pipe</span></span>](/windows/desktop/Midl/pipe)
</dt> <dt>

[<span data-ttu-id="3194c-118">**/Oi**</span><span class="sxs-lookup"><span data-stu-id="3194c-118">**/Oi**</span></span>](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 