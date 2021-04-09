---
title: Makefile de exemplo assíncrono
description: Este é o makefile para o aplicativo de exemplo assíncrono.
ms.assetid: 5d5b5578-6a2e-4311-9bf7-9b7818eb23ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 613dd67ab66819bd7f717ddc282ced1de63eff87
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822395"
---
# <a name="asynchronous-example-makefile"></a>Makefile de exemplo assíncrono

Este é o makefile para o [aplicativo de exemplo assíncrono](asynchronous-example-application.md).

``` syntax
#----- Include the SDK's WIN32.MAK to pick up defines-------------------
!include <win32.mak>

all:    $(OUTDIR) $(OUTDIR)\async.exe 

$(OUTDIR)\async.exe:     $(OUTDIR)\async.obj
    $(link) $(ldebug) /OUT:$(OUTDIR)\async.exe $(conlflags) /PDB:$(OUTDIR)\async.pdb /MACHINE:$(CPU) $(OUTDIR)\async.obj wininet.lib $(baselibs)

$(OUTDIR)\async.obj:    async.c
    $(cc) $(cflags) $(cdebug) $(cvars) /EHsc /Fo"$(OUTDIR)\\" /Fd"$(OUTDIR)\\" /D"_CONSOLE" /D"UNICODE" /D"_UNICODE" async.c
        
#----- If OUTDIR does not exist, then create directory
$(OUTDIR) :
    if not exist "$(OUTDIR)/$(NULL)" mkdir $(OUTDIR)

clean:
     $(CLEANUP)
```

 

 




