---
title: Usando comandos de script
description: Usando comandos de script
ms.assetid: be8a2d22-35cb-4b8d-ad00-e8a45bb85b39
keywords:
- Windows SDK de Formato de Mídia, comandos de script
- FORMATO DE SISTEMAS Avançados (ASF), comandos de script
- ASF (Formato de Sistemas Avançados), comandos de script
- scripts, comandos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88b77de3e892d4f7b479822442a2637849df3d4bcd56273deb952246fba14f28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118195782"
---
# <a name="using-script-commands"></a>Usando comandos de script

O Windows SDK de Formato de Mídia oferece suporte ao uso de comandos de script para comunicar ações de aplicativo em arquivos ASF. Cada comando de script é feito de duas cadeias de caracteres, a primeira cadeia de caracteres é o tipo de comando, o segundo são os dados de comando. Por exemplo, você pode usar o tipo de script "URL" e passar uma URL de Internet válida como os dados de comando. Quando um aplicativo de leitura que dá suporte a comandos de script do tipo "URL" recebe esse comando, ele abrirá o endereço especificado em uma janela do navegador.

O Windows SDK de Formato de Mídia fornece duas opções para fornecer script em arquivos ASF. Você pode criar um fluxo de script ou incluir comandos de script no header do arquivo. Os fluxos de script são úteis porque os comandos de script são entregues em ordem de tempo de apresentação. Se você usar comandos de script no header de arquivo, seu aplicativo precisará recuperar todos os comandos de script antes de iniciar a reprodução. Você deve manter o controle dos tempos de apresentação dos comandos de script e responder a eles no momento certo.

As seções a seguir descrevem como incluir comandos de script em um arquivo ASF.



| Seção                                                                                                                | Descrição                                                  |
|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Para usar um fluxo de script](to-use-a-script-stream.md)                                                                   | Descreve como incluir comandos de script em um fluxo de script. |
| [Para adicionar dados de script ao header](to-add-script-data-to-the-header.md)                                               | Descreve como incluir comandos de script no header do arquivo. |
| [Usando comandos de script com suporte Windows Media Player](using-script-commands-supported-by-windows-media-player.md) | Descreve os comandos de script usados pelo Windows Media Player.  |



 

> [!Note]  
> Nas versões anteriores do SDK Windows Formato de Mídia, os fluxos de script eram usados para abrir endereços Web correspondentes ao conteúdo de um arquivo ASF. Agora você pode usar fluxos da Web para trabalhar com páginas da Web sincronizadas. Para obter mais informações. consulte [Web Fluxos](web-streams.md).

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Comandos de script**](script-commands.md)
</dt> <dt>

[**Guia de programação**](programming-guide.md)
</dt> </dl>

 

 




