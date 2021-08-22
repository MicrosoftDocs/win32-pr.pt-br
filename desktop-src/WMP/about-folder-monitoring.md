---
title: Sobre o monitoramento de pastas
description: Sobre o monitoramento de pastas
ms.assetid: d3d83e60-ecc7-4501-a6dd-15f7680a6ec9
keywords:
- Windows Media Player, monitoramento de pastas
- Windows Media Player modelo de objeto, monitoramento de pasta
- modelo de objeto, monitoramento de pasta
- Windows Media Player ActiveX controle, monitoramento de pastas
- ActiveX controle, monitoramento de pasta
- Windows Media Player Controle de ActiveX móvel, monitoramento de pastas
- Windows Media Player Móvel, monitoramento de pastas
- monitoramento de pastas
- pastas de monitoramento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1206defcdc387659567ceedcf7347a3ab99ca45d9926a9bd32c4f75280a8a46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055504"
---
# <a name="about-folder-monitoring"></a>Sobre o monitoramento de pastas

Windows Media Player pode monitorar pastas que contêm arquivos de mídia digital e atualizar a biblioteca quando os arquivos são adicionados ou removidos. Essa funcionalidade de monitoramento de pasta é fornecida pela interface [IWMPFolderMonitorServices.](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)

Para usar os serviços de monitoramento de pasta, você deve criar o objeto Player em um estado remoto. Para obter mais informações sobre a remoting, consulte [Remoting the Windows Media Player Control](remoting-the-windows-media-player-control.md). Depois de criar uma instância remota do player, obtenha um ponteiro para a interface **IWMPFolderMonitorServices** chamando **QueryInterface** na interface [IWMPPlayer.](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer)

Windows Media Player mantém uma lista de pastas que estão sendo monitoradas. Para obter uma lista de pastas monitoradas, use os métodos [IWMPFolderMonitorServices::get \_ count](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_count) e [IWMPFolderMonitorServices::item.](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-item) Para adicionar pastas à lista ou removê-las da lista, use os métodos [IWMPFolderMonitorServices::add](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-add) e [remove,](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-remove) respectivamente.

**Iniciando uma verificação**

O monitoramento de pastas normalmente é um processo em segundo plano que não precisa ser chamado explicitamente. Se você quiser verificar ativamente uma pasta, chame [IWMPFolderMonitorServices::startScan](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-startscan). Você pode interromper uma verificação em andamento com o [método IWMPFolderMonitorServices::stopScan.](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-stopscan)

**Recuperando o status de monitoramento de pasta**

**IWMPFolderMonitorServices** fornece funcionalidade para recuperar o status do processo de monitoramento de pasta.

A verificação de pasta é feita em duas passagens. Na primeira passagem, o Player examina as pastas nomeadas na lista de pastas monitoradas uma a uma e cria uma lista de arquivos a serem adicionados à biblioteca. Na segunda passagem, ele passa pela lista de arquivos e adiciona os arquivos à biblioteca e também remove todos os itens de mídia da biblioteca cujos arquivos físicos correspondentes foram excluídos do sistema de arquivos.

O [evento FolderScanStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-folderscanstatechange) é usado para notificar seu programa sempre que o Player alterna para um novo estado. Você também pode recuperar o estado atual chamando [get \_ scanState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scanstate). Quando a primeira passagem é iniciada, o valor de estado atual é wmpfssScanning. Durante a segunda passagem, o estado alterna para wmpfssUpdating. Depois que o processo é concluído, o estado muda para wmpfssStopped.

Enquanto o Player estiver digitalizando as pastas monitoradas na primeira passagem, chame [get \_ scannedFilesCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scannedfilescount) para verificar quantos arquivos foram verificados. O [método \_ get currentFolder](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_currentfolder) dirá qual pasta está sendo digitalizada no momento.

Após o início da segunda passagem, chame [get \_ addedFilesCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_addedfilescount) para verificar quantos arquivos foram adicionados à biblioteca. O [método \_ get updateProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_updateprogress) lhe dirá o progresso da segunda passagem, como um percentual de 0 a 100.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre o modelo de objeto do player**](about-the-player-object-model.md)
</dt> <dt>

[**IWMPFolderMonitorServices Interface**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)
</dt> </dl>

 

 




