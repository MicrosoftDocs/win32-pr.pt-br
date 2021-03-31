---
title: Compilando e vinculando
description: O makefile a seguir mostra as dependências entre os arquivos necessários para compilar os aplicativos cliente e servidor e vinculá-los à biblioteca de tempo de execução do RPC e à biblioteca de tempo de execução padrão do C.
ms.assetid: 9182baea-7307-4db0-8d66-7fba14227ac9
keywords:
- Chamada de procedimento remoto RPC, tarefas, compilação e vinculação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1991e39cc028c01066cd8f13344765787374fa08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916334"
---
# <a name="compiling-and-linking"></a>Compilando e vinculando

O makefile a seguir mostra as dependências entre os arquivos necessários para compilar os aplicativos cliente e servidor e vinculá-los à biblioteca de tempo de execução do RPC e à biblioteca de tempo de execução padrão do C.

Esse makefile pode ser usado para criar aplicativos de cliente e servidor do código-fonte neste tutorial. Os stubs e cabeçalhos mostrados aqui foram gerados com o MIDL versão 2,0. Os comandos e os argumentos do compilador e do vinculador podem ser diferentes para a configuração do computador. Consulte a documentação do compilador para obter mais informações.

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

 

 




