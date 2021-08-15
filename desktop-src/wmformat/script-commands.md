---
title: Comandos de script
description: Comandos de script
ms.assetid: b8d7d4d3-c0d3-4b09-b5dd-1c6bbc3f2020
keywords:
- Windows SDK de Formato de Mídia, comandos de script
- FORMATO DE SISTEMAS Avançados (ASF), comandos de script
- ASF (Formato de Sistemas Avançados), comandos de script
- Windows SDK de formato de mídia, fluxos de script
- ASF (Advanced Systems Format), fluxos de script
- ASF (Formato de Sistemas Avançados), fluxos de script
- Windows SDK de Formato de Mídia, fluxos
- ASF (Advanced Systems Format), streams
- ASF (Formato de Sistemas Avançados), fluxos
- scripts, comandos
- scripts, fluxos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a6f6487958db820892f57af2b1348dcd4304031976aaaf56ddeb6233e1b8a87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118197523"
---
# <a name="script-commands"></a>Comandos de script

Os comandos de script com suporte do SDK Windows Formato de Mídia são pares de cadeias de caracteres de nome e valor simples. Por exemplo, um comando de script comum é "URL", que é usado por Windows Media Player e outros aplicativos em reprodução para abrir páginas da Web. A outra metade do par de scripts para o comando "URL" contém uma URL (uniform resource locator) válida, como `https://www.adatum.com` . Nenhum suporte é fornecido pelos objetos desse SDK para comandos específicos; seu aplicativo deve incluir lógica para lidar com os comandos que você usar. Você pode usar os comandos com suporte do Windows Media Player para manter a compatibilidade com a maioria dos jogadores.

Os comandos de script podem ser entregues de duas maneiras: em um fluxo de script ou no header do arquivo.

## <a name="script-streams"></a>Script Fluxos

Você pode entregar comandos de script em seu próprio fluxo em um arquivo ASF. Cada exemplo em um fluxo de script contém as duas cadeias de caracteres do par nome/valor. A vantagem de usar um fluxo de script é que os comandos serão entregues no momento correto da apresentação.

## <a name="script-commands-in-the-file-header"></a>Comandos de script no header de arquivo

Os comandos de script podem ser incluídos no header de arquivo para recuperação no momento da reprodução. O aplicativo em execução é responsável por executar os comandos de script no momento apropriado. A vantagem de usar comandos de script no header de arquivo é que todos os comandos de script estão disponíveis antes de começar a receber exemplos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos de arquivo ASF**](asf-file-features.md)
</dt> <dt>

[**Usando comandos de script**](using-script-commands.md)
</dt> </dl>

 

 




