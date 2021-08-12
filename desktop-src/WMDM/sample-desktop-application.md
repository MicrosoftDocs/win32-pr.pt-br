---
title: Aplicativo de desktop de exemplo
description: Aplicativo de desktop de exemplo
ms.assetid: 3736dd01-b02f-4056-b19b-0e7cc6c9aa67
keywords:
- Windows Gerenciador de Dispositivos de mídia, amostras
- Gerenciador de Dispositivos, exemplos
- aplicativos de área de trabalho, exemplos
- Windows Gerenciador de Dispositivos de mídia, exemplo de aplicativo da área de trabalho
- Gerenciador de Dispositivos, exemplo de aplicativo de desktop
- aplicativo de exemplo wmdmapp
- exemplos, aplicativos de desktop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a14e8037ccf963f26637711cd6d0e77ea7d2b4ff3cede72fcbded6600226d36c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118584238"
---
# <a name="sample-desktop-application"></a>Aplicativo de desktop de exemplo

o Gerenciador de Dispositivos de mídia Windows é fornecido com um aplicativo de desktop de exemplo chamado wmdmapp. Esse aplicativo tem uma interface gráfica do usuário que permite que você procure dispositivos conectados, crie listas de reprodução no dispositivo e arraste arquivos de mídia para o dispositivo.

Este aplicativo de exemplo consiste em duas partes:

-   wmdapp.exe, um executável que exibe uma janela e executa a maior parte da interface do usuário e a funcionalidade básica do programa, e
-   proghelp.dll, uma DLL auxiliar que executa funções de utilitário para o aplicativo. Você deve registrar essa DLL depois de compilar o projeto.

Para compilar o aplicativo de exemplo, você pode usar Visual Studio. A seção a seguir descreve como isso é feito:

-   [Compilando o aplicativo de exemplo usando Visual Studio](compiling-the-sample-application-using-visual-studio.md)

Depois de compilar o projeto, registre o arquivo de proghelp.dll. Para registrar essa DLL, abra um prompt de comando e navegue até o diretório que contém essa DLL e digite `regsvr32 proghelp.dll` .

 

 




