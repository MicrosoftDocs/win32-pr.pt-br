---
title: Comandos de script
description: Comandos de script
ms.assetid: b8d7d4d3-c0d3-4b09-b5dd-1c6bbc3f2020
keywords:
- SDK do Windows Media Format, comandos de script
- ASF (Advanced Systems Format), comandos de script
- ASF (formato de sistemas avançados), comandos de script
- SDK do Windows Media Format, fluxos de script
- ASF (Advanced Systems Format), fluxos de script
- ASF (formato de sistemas avançados), fluxos de script
- SDK do Windows Media Format, fluxos
- ASF (Advanced Systems Format), fluxos
- ASF (formato de sistemas avançados), fluxos
- scripts, comandos
- scripts, fluxos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e57ab446a216624dc8f844f54298aeeaee358ac3
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104008570"
---
# <a name="script-commands"></a>Comandos de script

Os comandos de script com suporte no Windows Media Format SDK são pares de nome e cadeia de caracteres de valor simples. Por exemplo, um comando de script comum é "URL", que é usado pelo Windows Media Player e outros aplicativos de reprodução para abrir páginas da Web. A outra metade do par de scripts para o comando "URL" contém um Uniform Resource Locator (URL) válido, como `https://www.adatum.com` . Nenhum suporte é fornecido pelos objetos deste SDK para comandos específicos; seu aplicativo deve incluir lógica para lidar com quaisquer comandos que você usar. Você pode usar os comandos com suporte do Windows Media Player para manter a compatibilidade com a maioria dos players.

Comandos de script podem ser entregues de uma das duas maneiras: em um fluxo de script ou no cabeçalho do arquivo.

## <a name="script-streams"></a>Fluxos de script

Você pode fornecer comandos de script em seu próprio fluxo em um arquivo ASF. Cada exemplo em um fluxo de script contém as duas cadeias de caracteres do par nome/valor. A vantagem de usar um fluxo de script é que os comandos serão entregues no momento da apresentação correto.

## <a name="script-commands-in-the-file-header"></a>Comandos de script no cabeçalho do arquivo

Comandos de script podem ser incluídos no cabeçalho do arquivo para recuperação no momento da reprodução. O aplicativo de reprodução é responsável por executar os comandos de script no momento adequado. A vantagem de usar comandos de script no cabeçalho do arquivo é que todos os comandos de script estão disponíveis antes de começar a receber exemplos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Recursos de arquivo ASF**](asf-file-features.md)
</dt> <dt>

[**Usando comandos de script**](using-script-commands.md)
</dt> </dl>

 

 




