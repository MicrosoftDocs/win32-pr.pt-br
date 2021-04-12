---
title: Aplicativo de desktop de exemplo
description: Aplicativo de desktop de exemplo
ms.assetid: 3736dd01-b02f-4056-b19b-0e7cc6c9aa67
keywords:
- Gerenciador de Dispositivos de mídia do Windows, amostras
- Gerenciador de Dispositivos, exemplos
- aplicativos de área de trabalho, exemplos
- Windows Media Gerenciador de Dispositivos, exemplo de aplicativo da área de trabalho
- Gerenciador de Dispositivos, exemplo de aplicativo de desktop
- aplicativo de exemplo wmdmapp
- exemplos, aplicativos de desktop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f4008a25ca4448d4d4be7c9f667c5a9e4f08023
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364052"
---
# <a name="sample-desktop-application"></a>Aplicativo de desktop de exemplo

O Windows Media Gerenciador de Dispositivos é fornecido com um aplicativo de desktop de exemplo chamado wmdmapp. Esse aplicativo tem uma interface gráfica do usuário que permite que você procure dispositivos conectados, crie listas de reprodução no dispositivo e arraste arquivos de mídia para o dispositivo.

Este aplicativo de exemplo consiste em duas partes:

-   wmdapp.exe, um executável que exibe uma janela e executa a maior parte da interface do usuário e a funcionalidade básica do programa, e
-   proghelp.dll, uma DLL auxiliar que executa funções de utilitário para o aplicativo. Você deve registrar essa DLL depois de compilar o projeto.

Para compilar o aplicativo de exemplo, você pode usar o Visual Studio. A seção a seguir descreve como isso é feito:

-   [Compilando o aplicativo de exemplo usando o Visual Studio](compiling-the-sample-application-using-visual-studio.md)

Depois de compilar o projeto, registre o arquivo de proghelp.dll. Para registrar essa DLL, abra um prompt de comando e navegue até o diretório que contém essa DLL e digite `regsvr32 proghelp.dll` .

 

 




