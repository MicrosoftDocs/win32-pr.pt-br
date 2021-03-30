---
title: Configurações do registro de extensão de nome de arquivo
description: Configurações do registro de extensão de nome de arquivo
ms.assetid: a5c31cf7-e1e1-4f1a-8e94-ed08f99ad973
keywords:
- Windows Media Player, registro
- Windows Media Player, extensões de nome de arquivo
- registro, extensões de nome de arquivo
- registro, configurações do Windows Media Player
- configurações do registro de extensão de nome de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c526e38ae1b2b76b942e0646df6f8aaa3b8e3417
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636719"
---
# <a name="file-name-extension-registry-settings"></a>Configurações do registro de extensão de nome de arquivo

Se os arquivos de mídia digital tiverem um formato personalizado, você poderá fornecer ao Windows Media Player informações sobre seu formato personalizado colocando entradas no registro no computador do usuário. O Windows Media Player inspeciona as entradas do registro para determinar como ele deve lidar com seus arquivos. A lista a seguir mostra várias coisas que você pode fazer criando entradas do registro que pertencem ao seu formato de arquivo de mídia personalizado.

-   Conceda permissão para que o Player reproduza, copie ou transcodifique seus arquivos.
-   Especifique a tecnologia subjacente que o Player deve usar para reproduzir os arquivos.
-   Especifique onde o Player deve exibir os arquivos em seu modo de exibição de biblioteca.
-   Especifique um plug-in que o Player deve usar para converter os arquivos em um formato padrão.
-   Especifique um código de formato de MTP (protocolo de transporte de mídia) que o Player possa usar para determinar se um dispositivo portátil específico dá suporte ao seu formato de arquivo.

A maioria das entradas que você fornece estará sob uma subchave associada à extensão de nome de arquivo personalizado. Você pode criar essa subchave na \_ \_ subárvore do computador local hKey e na \_ subárvore do usuário atual do hKey \_ . O Windows Media Player primeiro procura na \_ \_ subárvore do computador local HKEY. Se ele não encontrar o que precisa lá, ele procurará na \_ subárvore atual do usuário do hKey \_ . Observe que qualquer código que tente gravar no registro no computador do usuário poderá gravar na \_ subárvore do computador local hKey \_ somente se o usuário atual tiver privilégios administrativos.

Para gravar informações sobre o formato de arquivo personalizado na \_ \_ subárvore do computador local hKey, crie a subchave a seguir.

**HKEY \_ \_Software da máquina local \\ \\ \\ \\ \\ extensões \\ de wmplayer multimídia da Microsoft** *customExtension*

em que *customExtension* é a extensão de nome de arquivo, incluindo o separador de ponto (.). Por exemplo, se a extensão para seu formato de arquivo personalizado for. xyz, crie a subchave a seguir.

**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ multimídia \\ wmplayer \\ Extensions \\ . xyz**

Para gravar informações sobre o formato de arquivo personalizado na \_ subárvore do usuário atual do hKey \_ , crie a subchave a seguir.

**HKEY \_ \_ \\ Software do usuário \\ atual \\ \\ \\ extensões \\ do Microsoft MediaPlayer Player** *customExtension*

Você pode escrever uma ou mais das seguintes entradas em sua subchave *customExtension* .

-   **Permissões**
-   **Runtime**
-   **FormatCode**

Para especificar plug-ins de conversão para seu formato de arquivo de mídia personalizado, crie uma subchave **ConvertPluginCLSID** em sua subchave *customExtension* .

Para especificar onde o Windows Media Player deve exibir os arquivos em seu modo de exibição de biblioteca, escreva uma entrada que represente o formato de arquivo personalizado na subchave a seguir.

**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ MediaPlayer \\ MLS \\ extensões**

Os tópicos a seguir descrevem as subchaves e entradas do registro que fornecem ao Windows Media Player informações sobre formatos de arquivo de mídia personalizados.

-   [Entrada de registro de permissões](permissions-registry-entry.md)
-   [Entrada de registro de tempo de execução](runtime-registry-entry.md)
-   [Entrada do registro FormatCode](formatcode-registry-entry.md)
-   [Entradas do registro de classificação de biblioteca](library-classification-registry-entries.md)
-   [Subchave ConvertPluginCLSID](convertpluginclsid-subkey.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Configurações do registro**](registry-settings.md)
</dt> <dt>

[**Plug-ins de conversão do Windows Media Player**](windows-media-player-conversion-plug-ins.md)
</dt> </dl>

 

 




