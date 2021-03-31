---
title: Gerando os arquivos stub
description: Depois de definir a interface do cliente/servidor, você geralmente desenvolve os arquivos de origem do cliente e do servidor.
ms.assetid: e4d08bee-ab9a-4426-a1af-72a7d763797f
keywords:
- Chamada de procedimento remoto RPC, tarefas, gerando arquivos stub
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e092663711be60a3a0dc0dd8a4e99c0fa92a3ef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822594"
---
# <a name="generating-the-stub-files"></a><span data-ttu-id="cc5fc-104">Gerando os arquivos stub</span><span class="sxs-lookup"><span data-stu-id="cc5fc-104">Generating the Stub Files</span></span>

<span data-ttu-id="cc5fc-105">Depois de definir a interface do cliente/servidor, você geralmente desenvolve os arquivos de origem do cliente e do servidor.</span><span class="sxs-lookup"><span data-stu-id="cc5fc-105">After defining the client/server interface, you usually develop your client and server source files.</span></span> <span data-ttu-id="cc5fc-106">Em seguida, use um único makefile para gerar os arquivos de stub e de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="cc5fc-106">Next use a single makefile to generate the stub and header files.</span></span> <span data-ttu-id="cc5fc-107">Compile e vincule os aplicativos cliente e servidor.</span><span class="sxs-lookup"><span data-stu-id="cc5fc-107">Compile and link the client and server applications.</span></span> <span data-ttu-id="cc5fc-108">No entanto, se essa for sua primeira exposição ao ambiente de computação distribuída, talvez você queira invocar o compilador MIDL agora para ver o que o MIDL gera antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="cc5fc-108">However, if this is your first exposure to the distributed computing environment, you may want to invoke the MIDL compiler now to see what MIDL generates before you continue.</span></span> <span data-ttu-id="cc5fc-109">O compilador MIDL (Midl.exe) é instalado automaticamente quando você instala o SDK (Software Development Kit) da plataforma.</span><span class="sxs-lookup"><span data-stu-id="cc5fc-109">The MIDL compiler (Midl.exe) is automatically installed when you install the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="cc5fc-110">Ao compilar esses arquivos, verifique se Hello. idl e Hello. ACF estão no mesmo diretório.</span><span class="sxs-lookup"><span data-stu-id="cc5fc-110">When you compile these files, make sure that Hello.idl and Hello.acf are in the same directory.</span></span> <span data-ttu-id="cc5fc-111">O comando a seguir gerará o arquivo de cabeçalho Hello. h e os stubs de cliente e de servidor, Olá \_ c. c e Hello \_ s.c.</span><span class="sxs-lookup"><span data-stu-id="cc5fc-111">The following command will generate the header file Hello.h, and the client and server stubs, Hello\_c.c and Hello\_s.c.</span></span>

<span data-ttu-id="cc5fc-112">**MIDL Olá. idl**</span><span class="sxs-lookup"><span data-stu-id="cc5fc-112">**midl hello.idl**</span></span>

<span data-ttu-id="cc5fc-113">Observe que Hello. h contém protótipos de função para HelloProc e Shutdown, bem como declarações de encaminhamento para duas funções de gerenciamento de memória, **\_ \_ alocação de usuário de MIDL** e usuário de **MIDL \_ \_ gratuito**.</span><span class="sxs-lookup"><span data-stu-id="cc5fc-113">Notice that Hello.h contains function prototypes for HelloProc and Shutdown, as well as forward declarations for two memory management functions, **midl\_user\_allocate** and **midl\_user\_free**.</span></span> <span data-ttu-id="cc5fc-114">Você fornecerá essas duas funções no aplicativo de servidor.</span><span class="sxs-lookup"><span data-stu-id="cc5fc-114">You will provide these two functions in the server application.</span></span> <span data-ttu-id="cc5fc-115">Se os dados estavam sendo transmitidos do servidor para o cliente (por meio de um parâmetro de \[ **saída** \] ), você também precisaria fornecer essas duas funções de gerenciamento de memória no aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="cc5fc-115">If data were being transmitted from the server to the client (by means of an \[**out**\] parameter) you would also need to provide these two memory management functions in the client application.</span></span>

<span data-ttu-id="cc5fc-116">Observe as definições para a variável de identificador global, Olá \_ IfHandle e os nomes de identificador de interface de cliente e de servidor, Olá \_ v1 \_ 0 \_ c \_ ifspec e Olá \_ v1 \_ 0 \_ s \_ ifspec.</span><span class="sxs-lookup"><span data-stu-id="cc5fc-116">Note the definitions for the global handle variable, hello\_IfHandle, and the client and server interface handle names, hello\_v1\_0\_c\_ifspec and hello\_v1\_0\_s\_ifspec.</span></span> <span data-ttu-id="cc5fc-117">Os aplicativos cliente e servidor usarão os nomes de identificador de interface em chamadas em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="cc5fc-117">The client and server applications will use the interface handle names in run-time calls.</span></span>

<span data-ttu-id="cc5fc-118">Neste ponto, você não precisa fazer nada com os arquivos de stub Olá \_ c. c e Olá \_ s.c.</span><span class="sxs-lookup"><span data-stu-id="cc5fc-118">At this point, you don't need to do anything with the stub files Hello\_c.c and hello\_s.c.</span></span>

``` syntax
/*file: hello.h */
/* this ALWAYS GENERATED file contains the definitions for the interfaces */
/* File created by MIDL compiler version 3.00.06 
/* at Tue Feb 20 11:33:32 1996 */
/* Compiler settings for hello.idl:
    Os, W1, Zp8, env=Win32, ms_ext, c_ext
    error checks: none */
//@@MIDL_FILE_HEADING(  )
#include "Rpc.h"
#include "rpcndr.h"
 
#ifndef __hello_h_
#define __hello_h_
 
#ifdef __cplusplus
extern "C"{
#endif 
 
/* Forward Declarations */ 
 
void __RPC_FAR * __RPC_USER MIDL_user_allocate(size_t);
void __RPC_USER MIDL_user_free( void __RPC_FAR * ); 
 
#ifndef __hello_INTERFACE_DEFINED__
#define __hello_INTERFACE_DEFINED__
 
/****************************************
 * Generated header for interface: hello
 * at Tue Feb 20 11:33:32 1996
 * using MIDL 3.00.06
 ****************************************/
/* [implicit_handle][version][uuid] */ 
 
            /* size is 0 */
void HelloProc( 
    /* [string][in] */ unsigned char __RPC_FAR *pszString);
    /* size is 0 */
void Shutdown( void);
extern handle_t hello_IfHandle;
 
extern RPC_IF_HANDLE hello_v1_0_c_ifspec;
extern RPC_IF_HANDLE hello_v1_0_s_ifspec;
#endif /* __hello_INTERFACE_DEFINED__ */
 
/* Additional Prototypes for ALL interfaces */
/* end of Additional Prototypes */
#ifdef __cplusplus
}
#endif
#endif
```

 

 




