---
title: Configuração do ambiente
description: O SDK (Software Development Kit) da plataforma instalado fornece um arquivo Setenv.bat localizado no diretório raiz do SDK da plataforma que você pode executar para configurar seu ambiente para a criação de aplicativos que usam o SDK da plataforma.
ms.assetid: 2dec3d7a-acac-4ff7-9d4a-d3540e6d441d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f752872b96e4b02cbfd1724d8a4a99ca1de13f0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105755302"
---
# <a name="environment-setup"></a>Configuração do ambiente

O SDK (Software Development Kit) da plataforma instalado fornece um arquivo Setenv.bat localizado no diretório raiz do SDK da plataforma que você pode executar para configurar seu ambiente para a criação de aplicativos que usam o SDK da plataforma.

## <a name="settings-and-variables"></a>Configurações e variáveis

Você também pode configurar manualmente seu ambiente adicionando algo semelhante ao seguinte ao seu arquivo de Autoexec.bat. Usando o Windows, você pode editar o arquivo de Autoexec.bat para incluir esses comandos. Usando o Windows Server 2003, o Windows XP, o Windows 2000 ou o Windows NT, você pode editar ou adicionar essas configurações às suas variáveis de ambiente usando a caixa de diálogo do sistema que pode ser executada no painel de controle.


```cmd
  SET INCLUDE=D:\MSSDK\INCLUDE;C:\MSDEV\INCLUDE;C:\MSDEV\ATL\INCLUDE
  SET LIB=D:\MSSDK\LIB;C:\MSDEV\LIB
  SET MSSDK=D:\MSSDK
  SET MSTOOLS=D:\MSSDK
  SET CPU=i386
  SET PATH=C:\WIN95;C:\WIN95\COMMAND;C:\DOS;D:\MSSDK\BIN;C:\MSDEV\BIN
```



Essas configurações são apropriadas para uma plataforma Intel 80386 ou posterior que executa o Windows me, o Windows 98 ou o Windows 95 com o Microsoft Visual C++ e o SDK da plataforma instalados. Por exemplo, neste sistema, Visual C++ versão 5,0 é instalada no diretório C: \\ MSDEV O SDK da plataforma é instalado no diretório D: \\ MSSDK Sua configuração de disco pode ser diferente. Os diretórios do Platform SDK (para este exemplo, aqueles com D: \\ MSSDK neles) são todos anteriores em cada sequência de caminho. Essa sequência pressupõe que as compilações de linha de comando devem ser executadas na janela de prompt de comando e que os arquivos de biblioteca. h include e. lib no SDK da plataforma sejam preferidos para essas compilações.

A variável de ambiente CPU é definida para controlar as compilações do Win32, dependendo da plataforma. Os valores possíveis atuais incluem i386, MIPS, alfa e PPC. Para obter mais informações, consulte o arquivo Win32. Mak fornecido no SDK da plataforma no \\ \\ diretório MSSDK include. Todos os exemplos de makefile de código do tutorial do COM incluem Win32. Mak.

 

 




