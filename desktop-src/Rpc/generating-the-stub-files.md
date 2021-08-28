---
title: Gerando os arquivos stub
description: Depois de definir a interface de cliente/servidor, você geralmente desenvolve os arquivos de origem do cliente e do servidor.
ms.assetid: e4d08bee-ab9a-4426-a1af-72a7d763797f
keywords:
- RPC de Chamada de Procedimento Remoto , tarefas, gerando arquivos stub
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c03fbffb165e94b89e6801c212d0a8b63cd4e77fab28ad4a4afc4b4243ae0e79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020876"
---
# <a name="generating-the-stub-files"></a>Gerando os arquivos stub

Depois de definir a interface de cliente/servidor, você geralmente desenvolve os arquivos de origem do cliente e do servidor. Em seguida, use um único makefile para gerar os arquivos de stub e de header. Compile e vincule os aplicativos cliente e servidor. No entanto, se essa for sua primeira exposição ao ambiente de computação distribuída, talvez você queira invocar o compilador MIDL agora para ver o que o MIDL gera antes de continuar. O compilador MIDL (Midl.exe) é instalado automaticamente quando você instala o SDK (Kit de Desenvolvimento de Software de Plataforma).

Ao compilar esses arquivos, certifique-se de que Hello.idl e Hello.acf estão no mesmo diretório. O comando a seguir gerará o arquivo de header Hello.h e os stubs de cliente e servidor, Hello \_ c.c e Hello \_ s.c.

**midl hello.idl**

Observe que Hello.h contém protótipos de função para HelloProc e Shutdown, bem como declarações de encaminhamento para duas funções de gerenciamento de **memória, \_ \_** alocação de usuário médio e usuário médio **\_ \_ livre.** Você fornecerá essas duas funções no aplicativo de servidor. Se os dados fossem transmitidos do servidor para o cliente (por meio de um parâmetro out), você também precisaria fornecer essas duas funções de gerenciamento de memória no \[  \] aplicativo cliente.

Observe as definições para a variável de alça global, hello IfHandle e os nomes de alça da interface do cliente e do \_ servidor, hello \_ v1 \_ 0 c ifspec e \_ hello \_ \_ v1 \_ 0 \_ s \_ ifspec. Os aplicativos cliente e servidor usarão os nomes de alça de interface em chamadas em tempo de executar.

Neste ponto, você não precisa fazer nada com os arquivos stub Hello \_ c.c e hello \_ s.c.

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

 

 




