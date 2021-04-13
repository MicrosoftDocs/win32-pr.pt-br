---
title: Sobre o monitoramento de pastas
description: Sobre o monitoramento de pastas
ms.assetid: d3d83e60-ecc7-4501-a6dd-15f7680a6ec9
keywords:
- Windows Media Player, monitoramento de pastas
- Modelo de objeto do Windows Media Player, monitoramento de pastas
- modelo de objeto, monitoramento de pasta
- Controle ActiveX do Windows Media Player, monitoramento de pastas
- Controle ActiveX, monitoramento de pastas
- Controle ActiveX móvel do Windows Media Player, monitoramento de pastas
- Windows Media Player Mobile, monitoramento de pasta
- monitoramento de pastas
- pastas de monitoramento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c3d6af341df706cd85c4158197b27babad09c86
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104365526"
---
# <a name="about-folder-monitoring"></a>Sobre o monitoramento de pastas

O Windows Media Player pode monitorar pastas que contêm arquivos de mídia digital e atualizar a biblioteca quando os arquivos são adicionados ou removidos. Essa funcionalidade de monitoramento de pasta é fornecida pela interface [IWMPFolderMonitorServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices) .

Para usar os serviços de monitoramento de pasta, você deve criar o objeto do Player em um estado remoto. Para obter mais informações sobre comunicação remota, consulte [comunicação remota do controle do Windows Media Player](remoting-the-windows-media-player-control.md). Depois de criar uma instância remota do Player, obtenha um ponteiro para a interface **IWMPFolderMonitorServices** chamando **QueryInterface** na interface [IWMPPlayer](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer) .

O Windows Media Player mantém uma lista de pastas que estão sendo monitoradas. Para obter uma lista de pastas monitoradas, use os métodos [IWMPFolderMonitorServices:: get \_ Count](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_count) e [IWMPFolderMonitorServices:: item](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-item) . Para adicionar pastas à lista ou removê-las da lista, use os métodos [IWMPFolderMonitorServices:: Add](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-add) e [Remove](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-remove) , respectivamente.

**Iniciando uma verificação**

O monitoramento de pastas normalmente é um processo em segundo plano que não precisa ser chamado explicitamente. Se você quiser examinar ativamente uma pasta, chame [IWMPFolderMonitorServices:: startScan](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-startscan). Você pode interromper uma verificação em andamento com o método [IWMPFolderMonitorServices:: stopScan](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-stopscan) .

**Recuperando o status de monitoramento da pasta**

O **IWMPFolderMonitorServices** fornece a funcionalidade para recuperar o status do processo de monitoramento de pasta.

A verificação de pasta é feita em duas passagens. Na primeira passagem, o Player examina as pastas nomeadas na lista pastas monitoradas uma por uma e cria uma lista de arquivos a serem adicionados à biblioteca. Na segunda passagem, ele passa pela lista de arquivos e adiciona os arquivos à biblioteca e também remove todos os itens de mídia da biblioteca cujos arquivos físicos correspondentes foram excluídos do sistema de arquivos.

O evento [FolderScanStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-folderscanstatechange) é usado para notificar seu programa sempre que o jogador alternar para um novo estado. Você também pode recuperar o estado atual chamando [Get \_ scanState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scanstate). Quando a primeira passagem é iniciada, o valor do estado atual é wmpfssScanning. Durante a segunda passagem, o estado muda para wmpfssUpdating. Depois que o processo for concluído, o estado será alterado para wmpfssStopped.

Enquanto o Player estiver verificando as pastas monitoradas na primeira passagem, chame [Get \_ scannedFilesCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scannedfilescount) para verificar quantos arquivos foram verificados. O método [Get \_ currentFolder](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_currentfolder) informará qual pasta está sendo verificada no momento.

Depois que a segunda passagem for iniciada, chame [Get \_ addedFilesCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_addedfilescount) para verificar quantos arquivos foram adicionados à biblioteca. O método [Get \_ updateProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_updateprogress) informará o progresso da segunda passagem, como uma porcentagem de 0 a 100.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre o modelo de objeto do Player**](about-the-player-object-model.md)
</dt> <dt>

[**Interface IWMPFolderMonitorServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)
</dt> </dl>

 

 




