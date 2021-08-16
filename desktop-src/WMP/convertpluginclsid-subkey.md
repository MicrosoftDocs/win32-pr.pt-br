---
title: ConvertPluginCLSID Subkey
description: ConvertPluginCLSID Subkey
ms.assetid: 2bf5b6ad-31e9-40c2-a682-c7ad813e8f7a
keywords:
- Windows Media Player,subkey ConvertPluginCLSID
- Windows Media Player, extensões de nome de arquivo
- Windows Media Player,Registro
- registro, extensões de nome de arquivo
- registry,convertPluginCLSID subkey
- registry,settings for Windows Media Player
- configurações do registro de extensão de nome de arquivo
- Subkey ConvertPluginCLSID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5deeda3e7eb0b5fe465152aa7711717d086c94a06ebed4f9549dc9f6a9b62dd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118341660"
---
# <a name="convertpluginclsid-subkey"></a>ConvertPluginCLSID Subkey

Quando Windows Media Player 11 encontra uma extensão de nome de arquivo personalizada, ele procura uma sub-chave do Registro que corresponde à extensão. A sub-chave é descrita em Registro de Extensão de [Nome de Arquivo Configurações](file-name-extension-registry-settings.md). Em alguns casos, a sub-chave da extensão tem uma sub-chave chamada **ConvertPluginCLSID**.

Por exemplo, suponha que você tenha criado um formato de arquivo personalizado (com extensão de nome de arquivo .xyz) e um plug-in de conversão que converte os arquivos em um formato com suporte pelo Windows Media Player Então, você armazenaria a ID de classe do plug-in em uma ou ambas as sub-chaves a seguir.

**HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Multimedia \\ WMPlayer \\ Extensions \\ .xyz \\ ConvertPluginCLSID**

**HKEY \_ CURRENT \_ USER \\ Software \\ Microsoft \\ MediaPlayer \\ Player \\ Extensions \\ .xyz \\ ConvertPluginCLSID**

A sub-chave **ConvertPluginCLSID** especifica as IDs de classe de plug-ins que o Windows Media Player pode usar para converter um arquivo de mídia de seu formato personalizado em um formato com suporte pelo Player.

A sub-chave **ConvertPluginCLSID** tem as entradas a seguir.

-   Uma entrada padrão que representa o plug-in de conversão padrão.
-   Uma entrada nomeada que representa o plug-in de conversão padrão.
-   Entradas nomeadas adicionais que representam plug-ins de conversão alternativos.

Por exemplo, suponha que um formato de arquivo personalizado tenha um plug-in de conversão padrão e dois plug-ins de conversão alternativos. As entradas do Registro na sub-chave **ConvertPluginCLSID** teriam o formulário a seguir.



| Nome                                                                          | Tipo        | Valor                                                                |
|-------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------|
| Padrão                                                                       | **REG \_ SZ** | A ID da classe, no formato do Registro, do plug-in de conversão padrão. |
| A ID da classe, no formato do Registro, do plug-in de conversão padrão.          | **REG \_ SZ** | O nome amigável do plug-in de conversão padrão.                 |
| A ID da classe, no formato do Registro, do primeiro plug-in de conversão alternativo.  | **REG \_ SZ** | O nome amigável do primeiro plug-in de conversão alternativo.         |
| A ID da classe, no formato do Registro, do segundo plug-in de conversão alternativo. | **REG \_ SZ** | O nome amigável do segundo plug-in de conversão alternativo.        |



 

Observe que o plug-in de conversão padrão é representado por duas entradas do Registro: a entrada padrão e uma entrada nomeada. Windows Media Player usa a entrada padrão para determinar qual plug-in é o plug-in de conversão padrão (primário). Windows Media Player usa as entradas nomeadas para obter nomes amigáveis para todos os plug-ins de conversão, incluindo o plug-in padrão.

O nome amigável de um plug-in de conversão é determinado pela empresa que cria o plug-in. Windows Media Player pode exibir o nome amigável em sua interface do usuário.

Quando Windows Media Player tenta converter um arquivo de um formato personalizado em um formato padrão, ele carrega primeiro o plug-in padrão. Se o plug-in padrão não conseguir converter o arquivo e retornar NS E WMP CONVERT PLUGIN UNKNOWN FILE OWNER, o Player carregará cada plug-in alternativo até que ocorra uma conversão bem-sucedida ou não haja mais \_ \_ \_ \_ \_ \_ \_ plug-ins para tentar. O Player não exibirá uma mensagem de aviso se nenhum plug-in de conversão for encontrado para a extensão de nome de arquivo.

A **entrada do Registro ConvertPluginCLSID** é suportada pelo Windows Media Player 11.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Registro de extensão de nome de arquivo Configurações**](file-name-extension-registry-settings.md)
</dt> <dt>

[**Windows Media Player Plug-ins de conversão**](windows-media-player-conversion-plug-ins.md)
</dt> </dl>

 

 




