---
title: Configuração do ambiente
description: O SDK (Kit de Desenvolvimento de Software) da Plataforma instalado fornece um arquivo Setenv.bat localizado no diretório raiz do SDK da Plataforma que você pode executar para configurar seu ambiente para a criação de aplicativos que usam o SDK da Plataforma.
ms.assetid: 2dec3d7a-acac-4ff7-9d4a-d3540e6d441d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c1b7de27bfc015726786011376c821c5ae0e86a07d95f03098ed376dd022cca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739386"
---
# <a name="environment-setup"></a>Configuração do ambiente

O SDK (Kit de Desenvolvimento de Software) da Plataforma instalado fornece um arquivo Setenv.bat localizado no diretório raiz do SDK da Plataforma que você pode executar para configurar seu ambiente para a criação de aplicativos que usam o SDK da Plataforma.

## <a name="settings-and-variables"></a>Configurações e variáveis

Você também pode configurar manualmente seu ambiente adicionando algo como o seguinte ao arquivo Autoexec.bat arquivo. Usando Windows, você pode editar o arquivo Autoexec.bat para incluir esses comandos. Usando Windows Server 2003, Windows XP, Windows 2000 ou Windows NT, você pode editar ou adicionar essas configurações às variáveis de ambiente usando a caixa de diálogo Sistema que você pode executar no Painel de Controle.


```cmd
  SET INCLUDE=D:\MSSDK\INCLUDE;C:\MSDEV\INCLUDE;C:\MSDEV\ATL\INCLUDE
  SET LIB=D:\MSSDK\LIB;C:\MSDEV\LIB
  SET MSSDK=D:\MSSDK
  SET MSTOOLS=D:\MSSDK
  SET CPU=i386
  SET PATH=C:\WIN95;C:\WIN95\COMMAND;C:\DOS;D:\MSSDK\BIN;C:\MSDEV\BIN
```



Essas configurações são apropriadas para uma plataforma Intel 80386 ou posterior que executa o Windows Me, Windows 98 ou Windows 95 com o Microsoft Visual C++ e o SDK da Plataforma instalados. Por exemplo, nesse sistema, Visual C++ versão 5.0 é instalada no diretório C: \\ MSDEV. O SDK da Plataforma é instalado no diretório D: \\ MSSDK. A configuração do disco pode ser diferente. Os diretórios do SDK da Plataforma (para este exemplo, aqueles com D: \\ MSSDK neles) são todos anteriores em cada sequência de caminho. Essa sequência presume que as compilações de linha de comando devem ser executados na janela prompt de comando e que os arquivos de biblioteca .h include e .lib no SDK da Plataforma são preferenciais para essas compilações.

A variável de ambiente de CPU é definida para controlar os builds do Win32, dependendo da plataforma. Os valores possíveis atuais incluem i386, MIPS, ALPHA e PPC. Para obter mais informações, consulte o arquivo Win32.mak fornecido no SDK da Plataforma no diretório INCLUDE do \\ MSSDK. \\ Todos os makefiles de exemplo de código do tutorial COM incluem Win32.mak.

 

 




