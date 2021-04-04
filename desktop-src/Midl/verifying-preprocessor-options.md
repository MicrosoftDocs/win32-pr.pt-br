---
title: Verificando opções de pré-processador
description: O compilador MIDL chama implicitamente o pré-processador e não exibe suas opções de pré-processador.
ms.assetid: 2f402af4-18d7-480c-a8d2-d16f402ef87a
keywords:
- MIDL do compilador MIDL, verificando opções de pré-processador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19a047980c9f2f9dc8deffdcf85de767e4dc8705
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822721"
---
# <a name="verifying-preprocessor-options"></a>Verificando opções de pré-processador

O compilador MIDL chama implicitamente o pré-processador e não exibe suas opções de pré-processador. Na ausência da opção MIDL [**/cpp \_ opt**](-cpp-opt.md) , a linha de comando do pré-processador é composta de todas as opções [**/I**](-i.md), [**/d**](-d.md) e [**/u**](-u.md) usadas na linha de comando MIDL, bem como opções **/e** e [**/nologo**](-nologo.md) . Para ver as opções passadas para o pré-processador, use a opção [**/Confirm**](-confirm.md) do compilador.

Por exemplo, a linha a seguir

**midl.exe-D \_ Win32 \_ WinNT = 0x501-robusto-DNTENV = 1-ID: \\ NT \\ Public \\ SDK \\ Inc-Confirm-Oicf-env Win32-out x86 stub. idl**

produz a seguinte saída:

``` syntax
32 bit arguments
          input file -  stub.idl
          app_config -  No
               c_ext -  Yes
              client -  stub
                char -  signed
             confirm -  Yes
             cpp_cmd -  cl.exe
             cpp_opt -  -Id:\nt\public\sdk\inc -D_WIN32_WINNT=0x501 -DNTENV=1  -
E -nologo
             msc_ver -  1100
               cstub -  i386\stub_c.c
                   D -  -D_WIN32_WINNT=0x501 -DNTENV=1
                 env -  win32
            append64 -  No
               rpcss -  No
             use_epv -  No
      no_default_epv -  No
               error -  allocation ref bounds_check enum stub_data
              header -  i386\stub.h
                   I -  -Id:\nt\public\sdk\inc
              nologo -  No
              ms_ext -  Yes
            ms_union -  No
       no_format_opt -  No
            oldnames -  No
                 out -  i386\
              server -  stub
               sstub -  i386\stub_s.c
                   O -  interpreted stubs
                   W -  1
                  Zp -  8
```

 

 




