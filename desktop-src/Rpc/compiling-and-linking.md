---
title: Compilando e vinculando
description: O makefile a seguir mostra as dependências entre os arquivos necessários para compilar os aplicativos cliente e servidor e vinculá-los à biblioteca em tempo de run time RPC e à biblioteca de tempo de run time C padrão.
ms.assetid: 9182baea-7307-4db0-8d66-7fba14227ac9
keywords:
- RPC de Chamada de Procedimento Remoto , tarefas, compilação e vinculação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2500a763db149eca914060dd7920548883fa57fbd5642485a41f5a55c65cd2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118931709"
---
# <a name="compiling-and-linking"></a>Compilando e vinculando

O makefile a seguir mostra as dependências entre os arquivos necessários para compilar os aplicativos cliente e servidor e vinculá-los à biblioteca em tempo de run time RPC e à biblioteca de tempo de run time C padrão.

Esse makefile pode ser usado para criar aplicativos cliente e servidor do código-fonte neste tutorial. Os stubs e os headers mostrados aqui foram gerados com MIDL versão 2.0. Os comandos e os argumentos do compilador e do vinculador podem ser diferentes para a configuração do computador. Confira a documentação do compilador para obter mais informações.

``` syntax
#makefile for helloc.exe and hellos.exe
#link refers to the linker
#conflags refers to flags for console applications
#conlibs refers to libraries for console applications
 
!include <ntwin32.mak>
 
all : helloc hellos
 
# Make the client side application helloc
helloc : helloc.exe
helloc.exe : helloc.obj hello_c.obj
    $(link) $(linkdebug) $(conflags) -out:helloc.exe \
        helloc.obj hello_c.obj \
        rpcrt4.lib $(conlibs)
 
# helloc main program
helloc.obj : helloc.c hello.h
    $(cc) $(cdebug) $(cflags) $(cvars) $*.c
 
# helloc stub
hello_c.obj : hello_c.c hello.h
    $(cc) $(cdebug) $(cflags) $(cvars) $*.c
 
# Make the server side application
hellos : hellos.exe
hellos.exe : hellos.obj hellop.obj hello_s.obj
    $(link) $(linkdebug) $(conflags) -out:hellos.exe \
        hellos.obj hello_s.obj hellop.obj \
        rpcrt4.lib $(conlibsmt)
 
# hello server main program
hellos.obj : hellos.c hello.h
    $(cc) $(cdebug) $(cflags) $(cvarsmt) $*.c
 
# remote procedures
hellop.obj : hellop.c hello.h
    $(cc) $(cdebug) $(cflags) $(cvarsmt) $*.c
 
# hellos stub file
hello_s.obj : hello_s.c hello.h
    $(cc) $(cdebug) $(cflags) $(cvarsmt) $*.c
 
# Stubs and header file from the IDL file
hello.h hello_c.c hello_s.c : hello.idl hello.acf
    midl hello.idl
```

 

 




