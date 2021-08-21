---
description: Este exemplo usa as APIs de Áudio Core para implementar uma exibição na tela que mostra alterações de volume no fluxo de saída que é reproduzido por meio do dispositivo de ponto de extremidade de renderização de áudio padrão.
ms.assetid: 33a1e843-f7c7-4da9-a51e-83a3f0a6ac70
title: Osd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17bc0b93214cc547f0491d568abb88d696f76b494f2c562f4805f425acdcfd89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077510"
---
# <a name="osd"></a>Osd

Este exemplo usa as APIs de Áudio Core para implementar uma exibição na tela que mostra alterações de volume no fluxo de saída que é reproduzido por meio do dispositivo de ponto de extremidade de renderização de áudio padrão. A exibição na tela é exibida quando o usuário ajusta o nível de volume no programa de controle de volume do Windows, Sndvol.exe, e desaparece depois que o nível de volume permanece inalterado por um curto período.

Este tópico contém as seções a seguir.

-   [Descrição](#description)
-   [Requirements](#requirements)
-   [Baixando o exemplo](#downloading-the-sample)
-   [Compilando o exemplo](#building-the-sample)
-   [Executando o exemplo](#running-the-sample)
-   [Tópicos relacionados](#related-topics)

## <a name="description"></a>Descrição

Este exemplo demonstra os recursos a seguir.

-   [API MMDevice para](mmdevice-api.md) enumeração e seleção de dispositivo multimídia.
-   Ponto [de Extremidade de Áudio API de Volume](endpointvolume-api.md)

## <a name="requirements"></a>Requisitos



| Produto                                                        | Versão                |
|----------------------------------------------------------------|------------------------|
| [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows Vista ou posterior |
| Visual Studio                                                  | 2005 ou posterior          |



 

## <a name="downloading-the-sample"></a>Baixando o exemplo

Este exemplo está disponível nos locais a seguir.



| Localização    | Caminho/URL                                                                             |
|-------------|--------------------------------------------------------------------------------------|
| SDK do Windows | \\Arquivos de \\ Programas SDKs da Microsoft \\ Windows \\ v7.0 \\ Exemplos de OSD de \\ áudio \\ \\ \\ multimídia... |



 

## <a name="building-the-sample"></a>Compilando o exemplo

1.  Abra o shell do CMD para o SDK Windows e altere para o diretório de exemplo osD.
2.  Execute o comando "start OSD.sln" no diretório OSD para abrir o projeto OSD na janela Visual Studio.
3.  Na janela, selecione a configuração **de solução Depurar** ou Liberar, selecione o menu **Build** na barra de menus e selecione a **opção Build.**  Se você não abrir Visual Studio shell do CMD para o SDK, Visual Studio terá acesso ao ambiente de build do SDK. Nesse caso, o exemplo não será criado, a menos que você de definir explicitamente a variável de ambiente MSSdk, que é usada no arquivo de projeto, OSD.vcproj.

## <a name="running-the-sample"></a>Executando o exemplo

1.  Execute o arquivo executável osD, OSD.exe, no Windows Vista ou posterior. Observe que você não verá um ícone de bandeja do sistema ou uma janela para o aplicativo, mas poderá ver o processo em execução usando TaskMgr.exe.
2.  Execute sndvol.exe para alterar o volume ou o mute ou altere o volume usando controles de teclado ou um controle HID. A interface do usuário osD é exibida.
3.  Para sair do aplicativo, execute TaskMgr.exe, realça o processo OSD.exe e clique em **Encerrar Processo**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplos de SDK que usam as APIs de áudio principais](sdk-samples-that-use-the-core-audio-apis.md)
</dt> </dl>

 

 



