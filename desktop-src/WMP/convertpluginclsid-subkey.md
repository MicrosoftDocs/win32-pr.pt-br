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
- registro, configurações para Windows Media Player
- configurações do registro de extensão de nome de arquivo
- Subchave ConvertPluginCLSID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5deeda3e7eb0b5fe465152aa7711717d086c94a06ebed4f9549dc9f6a9b62dd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118341660"
---
# <a name="convertpluginclsid-subkey"></a>Subchave ConvertPluginCLSID

quando Windows Media Player 11 encontra uma extensão de nome de arquivo personalizada, ele procura uma subchave do registro que corresponda à extensão. a subchave é descrita em [Configurações do registro de extensão de nome de arquivo](file-name-extension-registry-settings.md). Em alguns casos, a subchave da extensão tem uma subchave chamada **ConvertPluginCLSID**.

por exemplo, suponha que você tenha criado um formato de arquivo personalizado (com a extensão de nome de arquivo. xyz) e um plug-in de conversão que converta os arquivos em um formato com suporte pelo Windows Media Player, em seguida, você armazenaria a ID de classe do plug-in em uma ou ambas as subchaves a seguir.

**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ multimídia \\ wmplayer \\ Extensions \\ . xyz \\ ConvertPluginCLSID**

**HKEY \_ Current \_ user \\ software \\ Microsoft \\ MediaPlayer \\ Player \\ Extensions \\ . xyz \\ ConvertPluginCLSID**

a subchave **ConvertPluginCLSID** especifica as IDs de classe dos plug-ins que Windows Media Player podem usar para converter um arquivo de mídia de seu formato personalizado em um formato suportado pelo Player.

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



 

Observe que o plug-in de conversão padrão é representado por duas entradas do registro: a entrada padrão e uma entrada nomeada. Windows Media Player usa a entrada padrão para determinar qual plug-in é o plug-in de conversão padrão (primário). Windows Media Player usa as entradas nomeadas para obter nomes amigáveis para todos os plug-ins de conversão, incluindo o plug-in padrão.

O nome amigável de um plug-in de conversão é determinado pela empresa que cria o plug-in. Windows Media Player pode exibir o nome amigável em sua interface do usuário.

quando Windows Media Player tenta converter um arquivo de um formato personalizado em um formato padrão, ele primeiro carrega o plug-in padrão. Se o plug-in padrão não converter o arquivo e retornar o proprietário do arquivo desconhecido do plug-in de conversão do NS \_ e \_ WMP \_ \_ \_ \_ \_ , o Player carregará cada plug-in alternativo até que ocorra uma conversão bem-sucedida ou que não haja mais plug-ins para tentar. O Player não exibirá uma mensagem de aviso se nenhum plug-in de conversão for encontrado para a extensão de nome de arquivo.

a entrada do registro **ConvertPluginCLSID** tem suporte no Windows Media Player 11.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Configurações de registro de extensão de nome de arquivo**](file-name-extension-registry-settings.md)
</dt> <dt>

[**Windows Media Player Plug-ins de conversão**](windows-media-player-conversion-plug-ins.md)
</dt> </dl>

 

 




