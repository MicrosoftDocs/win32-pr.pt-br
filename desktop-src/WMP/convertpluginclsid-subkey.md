---
title: Subchave ConvertPluginCLSID
description: Subchave ConvertPluginCLSID
ms.assetid: 2bf5b6ad-31e9-40c2-a682-c7ad813e8f7a
keywords:
- Windows Media Player, subchave ConvertPluginCLSID
- Windows Media Player, extensões de nome de arquivo
- Windows Media Player, registro
- registro, extensões de nome de arquivo
- registro, subchave ConvertPluginCLSID
- registro, configurações do Windows Media Player
- configurações do registro de extensão de nome de arquivo
- Subchave ConvertPluginCLSID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4229617c3999708d89fac976e94b2747b5a69145
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005611"
---
# <a name="convertpluginclsid-subkey"></a>Subchave ConvertPluginCLSID

Quando o Windows Media Player 11 encontra uma extensão de nome de arquivo Personalizada, ele procura uma subchave do registro que corresponda à extensão. A subchave é descrita em [configurações de registro de extensão de nome de arquivo](file-name-extension-registry-settings.md). Em alguns casos, a subchave da extensão tem uma subchave chamada **ConvertPluginCLSID**.

Por exemplo, suponha que você tenha criado um formato de arquivo personalizado (com a extensão de nome de arquivo. xyz) e um plug-in de conversão que converta os arquivos em um formato suportado pelo Windows Media Player. em seguida, você armazenaria a ID de classe do plug-in em uma ou ambas as subchaves a seguir.

**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ multimídia \\ wmplayer \\ Extensions \\ . xyz \\ ConvertPluginCLSID**

**HKEY \_ Current \_ user \\ software \\ Microsoft \\ MediaPlayer \\ Player \\ Extensions \\ . xyz \\ ConvertPluginCLSID**

A subchave **ConvertPluginCLSID** especifica as IDs de classe de plug-ins que o Windows Media Player pode usar para converter um arquivo de mídia de seu formato personalizado em um formato suportado pelo Player.

A subchave **ConvertPluginCLSID** tem as entradas a seguir.

-   Uma entrada padrão que representa o plug-in de conversão padrão.
-   Uma entrada nomeada que representa o plug-in de conversão padrão.
-   Entradas nomeadas adicionais que representam plug-ins alternativos de conversão.

Por exemplo, suponha que um formato de arquivo personalizado tenha um plug-in de conversão padrão e dois plug-ins alternativos de conversão. As entradas do registro na subchave **ConvertPluginCLSID** teriam o seguinte formato.



| Nome                                                                          | Tipo        | Valor                                                                |
|-------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------|
| Padrão                                                                       | **REG \_ sz** | A ID da classe, no formato do registro, do plug-in de conversão padrão. |
| A ID da classe, no formato do registro, do plug-in de conversão padrão.          | **REG \_ sz** | O nome amigável do plug-in de conversão padrão.                 |
| A ID da classe, no formato do registro, do primeiro plug-in de conversão alternativo.  | **REG \_ sz** | O nome amigável do primeiro plug-in de conversão alternativo.         |
| A ID da classe, no formato do registro, do segundo plug-in de conversão alternativo. | **REG \_ sz** | O nome amigável do segundo plug-in de conversão alternativo.        |



 

Observe que o plug-in de conversão padrão é representado por duas entradas do registro: a entrada padrão e uma entrada nomeada. O Windows Media Player usa a entrada padrão para determinar qual plug-in é o plug-in de conversão padrão (primário). O Windows Media Player usa as entradas nomeadas para obter nomes amigáveis para todos os plug-ins de conversão, incluindo o plug-in padrão.

O nome amigável de um plug-in de conversão é determinado pela empresa que cria o plug-in. O Windows Media Player pode exibir o nome amigável em sua interface do usuário.

Quando o Windows Media Player tenta converter um arquivo de um formato personalizado em um formato padrão, ele primeiro carrega o plug-in padrão. Se o plug-in padrão não converter o arquivo e retornar o proprietário do arquivo desconhecido do plug-in de conversão do NS \_ e \_ WMP \_ \_ \_ \_ \_ , o Player carregará cada plug-in alternativo até que ocorra uma conversão bem-sucedida ou que não haja mais plug-ins para tentar. O Player não exibirá uma mensagem de aviso se nenhum plug-in de conversão for encontrado para a extensão de nome de arquivo.

A entrada do registro **ConvertPluginCLSID** tem suporte do Windows Media Player 11.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Configurações do registro de extensão de nome de arquivo**](file-name-extension-registry-settings.md)
</dt> <dt>

[**Plug-ins de conversão do Windows Media Player**](windows-media-player-conversion-plug-ins.md)
</dt> </dl>

 

 




