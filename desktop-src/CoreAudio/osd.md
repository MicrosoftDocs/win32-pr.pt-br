---
description: Este exemplo usa as APIs de áudio principais para implementar uma exibição na tela que mostra as alterações de volume no fluxo de saída que é executado por meio do dispositivo de ponto de extremidade de renderização de áudio padrão.
ms.assetid: 33a1e843-f7c7-4da9-a51e-83a3f0a6ac70
title: OSD Feature
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89c4c04daf5d2dd333a25150821a831695e06a06
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010220"
---
# <a name="osd"></a>OSD Feature

Este exemplo usa as APIs de áudio principais para implementar uma exibição na tela que mostra as alterações de volume no fluxo de saída que é executado por meio do dispositivo de ponto de extremidade de renderização de áudio padrão. A exibição na tela é exibida quando o usuário ajusta o nível de volume no programa de controle de volume do Windows, Sndvol.exe e desaparece depois que o nível do volume permanece inalterado por um curto período de tempo.

Este tópico contém as seções a seguir.

-   [Descrição](#description)
-   [Requirements](#requirements)
-   [Baixando o exemplo](#downloading-the-sample)
-   [Compilando o exemplo](#building-the-sample)
-   [Executando o exemplo](#running-the-sample)
-   [Tópicos relacionados](#related-topics)

## <a name="description"></a>Descrição

Este exemplo demonstra os recursos a seguir.

-   [API MMDevice](mmdevice-api.md) para enumeração e seleção de dispositivo de multimídia.
-   [API EndpointVolume](endpointvolume-api.md) de áudio

## <a name="requirements"></a>Requisitos



| Produto                                                        | Versão                |
|----------------------------------------------------------------|------------------------|
| [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows Vista ou posterior |
| Visual Studio                                                  | 2005 ou posterior          |



 

## <a name="downloading-the-sample"></a>Baixando o exemplo

Este exemplo está disponível nos locais a seguir.



| Local    | Caminho/URL                                                                             |
|-------------|--------------------------------------------------------------------------------------|
| SDK do Windows | \\Arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ amostras \\ áudio multimídia \\ \\ OSD \\ ... |



 

## <a name="building-the-sample"></a>Compilando o exemplo

1.  Abra o Shell CMD para o SDK do Windows e altere para o diretório de exemplo OSD.
2.  Execute o comando "Start OSD. sln" no diretório OSD para abrir o projeto OSD na janela do Visual Studio.
3.  De dentro da janela, selecione a configuração da solução de **depuração** ou **versão** , selecione o menu **Compilar** na barra de menus e selecione a opção **Compilar** . Se você não abrir o Visual Studio a partir do Shell CMD para o SDK, o Visual Studio não terá acesso ao ambiente de compilação do SDK. Nesse caso, o exemplo não será compilado, a menos que você defina explicitamente a variável de ambiente MSSdk, que é usada no arquivo de projeto, OSD. vcproj.

## <a name="running-the-sample"></a>Executando o exemplo

1.  Execute o arquivo executável OSD, OSD.exe, no Windows Vista ou posterior. Observe que você não verá um ícone de bandeja do sistema ou uma janela para o aplicativo, mas poderá ver o processo em execução usando TaskMgr.exe.
2.  Execute sndvol.exe para alterar o volume ou mudo, ou altere o volume usando controles de teclado ou um controle HID. A interface do usuário do OSD é exibida.
3.  Para sair do aplicativo, execute TaskMgr.exe, realce o processo de OSD.exe e clique em **encerrar processo**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplos de SDK que usam as APIs de áudio principal](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



