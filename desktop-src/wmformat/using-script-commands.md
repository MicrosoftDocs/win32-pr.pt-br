---
title: Usando comandos de script
description: Usando comandos de script
ms.assetid: be8a2d22-35cb-4b8d-ad00-e8a45bb85b39
keywords:
- SDK do Windows Media Format, comandos de script
- ASF (Advanced Systems Format), comandos de script
- ASF (formato de sistemas avançados), comandos de script
- scripts, comandos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad2e840a677e58a1be528e84e4ed1b4be7fe3619
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005601"
---
# <a name="using-script-commands"></a>Usando comandos de script

O SDK do Windows Media Format dá suporte ao uso de comandos de script para comunicar ações de aplicativos em arquivos ASF. Cada comando de script é composto de duas cadeias de caracteres, a primeira cadeia é o tipo de comando, a segunda é os dados de comando. Por exemplo, você pode usar o tipo de script "URL" e passar uma URL de Internet válida como os dados de comando. Quando um aplicativo de leitura que dá suporte a comandos de script do tipo "URL" receber esse comando, ele abrirá o endereço especificado em uma janela do navegador.

O SDK do Windows Media Format fornece duas opções para a entrega de script em arquivos ASF. Você pode criar um fluxo de script ou pode incluir comandos de script no cabeçalho do arquivo. Fluxos de script são úteis porque os comandos de script são entregues na ordem de tempo da apresentação. Se você usar comandos de script no cabeçalho do arquivo, seu aplicativo precisará recuperar todos os comandos de script antes de iniciar a reprodução. Você deve manter o controle dos tempos de apresentação dos comandos de script e respondê-los no momento certo.

As seções a seguir descrevem como incluir comandos de script em um arquivo ASF.



| Seção                                                                                                                | Descrição                                                  |
|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| [Para usar um fluxo de script](to-use-a-script-stream.md)                                                                   | Descreve como incluir comandos de script em um fluxo de script. |
| [Para adicionar dados de script ao cabeçalho](to-add-script-data-to-the-header.md)                                               | Descreve como incluir comandos de script no cabeçalho do arquivo. |
| [Usando comandos de script com suporte no Windows Media Player](using-script-commands-supported-by-windows-media-player.md) | Descreve os comandos de script usados pelo Windows Media Player.  |



 

> [!Note]  
> Nas versões anteriores do SDK do Windows Media Format, os fluxos de script eram usados para abrir endereços Web correspondentes ao conteúdo de um arquivo ASF. Agora você pode usar fluxos da Web para trabalhar com páginas da Web sincronizadas. Para obter mais informações. consulte [fluxos da Web](web-streams.md).

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Comandos de script**](script-commands.md)
</dt> <dt>

[**Guia de programação**](programming-guide.md)
</dt> </dl>

 

 




