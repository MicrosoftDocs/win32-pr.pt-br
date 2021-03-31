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
# <a name="generating-the-stub-files"></a>Gerando os arquivos stub

Depois de definir a interface do cliente/servidor, você geralmente desenvolve os arquivos de origem do cliente e do servidor. Em seguida, use um único makefile para gerar os arquivos de stub e de cabeçalho. Compile e vincule os aplicativos cliente e servidor. No entanto, se essa for sua primeira exposição ao ambiente de computação distribuída, talvez você queira invocar o compilador MIDL agora para ver o que o MIDL gera antes de continuar. O compilador MIDL (Midl.exe) é instalado automaticamente quando você instala o SDK (Software Development Kit) da plataforma.

Ao compilar esses arquivos, verifique se Hello. idl e Hello. ACF estão no mesmo diretório. O comando a seguir gerará o arquivo de cabeçalho Hello. h e os stubs de cliente e de servidor, Olá \_ c. c e Hello \_ s.c.

**MIDL Olá. idl**

Observe que Hello. h contém protótipos de função para HelloProc e Shutdown, bem como declarações de encaminhamento para duas funções de gerenciamento de memória, **\_ \_ alocação de usuário de MIDL** e usuário de **MIDL \_ \_ gratuito**. Você fornecerá essas duas funções no aplicativo de servidor. Se os dados estavam sendo transmitidos do servidor para o cliente (por meio de um parâmetro de \[ **saída** \] ), você também precisaria fornecer essas duas funções de gerenciamento de memória no aplicativo cliente.

Observe as definições para a variável de identificador global, Olá \_ IfHandle e os nomes de identificador de interface de cliente e de servidor, Olá \_ v1 \_ 0 \_ c \_ ifspec e Olá \_ v1 \_ 0 \_ s \_ ifspec. Os aplicativos cliente e servidor usarão os nomes de identificador de interface em chamadas em tempo de execução.

Neste ponto, você não precisa fazer nada com os arquivos de stub Olá \_ c. c e Olá \_ s.c.

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

 

 




