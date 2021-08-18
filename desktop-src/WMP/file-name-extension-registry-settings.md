---
title: Registro de extensão de nome de arquivo Configurações
description: Registro de extensão de nome de arquivo Configurações
ms.assetid: a5c31cf7-e1e1-4f1a-8e94-ed08f99ad973
keywords:
- Windows Media Player,Registro
- Windows Media Player, extensões de nome de arquivo
- registro, extensões de nome de arquivo
- registry,settings for Windows Media Player
- configurações do registro de extensão de nome de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4acea080c59b4f78d4b4053f6ae67e5d1eb2c820d68b4e4702485130d8f33a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996626"
---
# <a name="file-name-extension-registry-settings"></a>Registro de extensão de nome de arquivo Configurações

Se os arquivos de mídia digital têm um formato personalizado, você pode fornecer Windows Media Player informações sobre seu formato personalizado colocando entradas no Registro no computador do usuário. Windows Media Player inspeciona as entradas do Registro para determinar como ele deve manipular seus arquivos. A lista a seguir mostra várias coisas que você pode fazer criando entradas do Registro que pertencem ao formato de arquivo de mídia personalizado.

-   Conceda permissão para o Player reproduzir, copiar ou transcodificar seus arquivos.
-   Especifique a tecnologia subjacente que o Player deve usar para reproduzir seus arquivos.
-   Especifique onde o Player deve exibir seus arquivos em sua exibição de biblioteca.
-   Especifique um plug-in que o Player deve usar para converter seus arquivos em um formato padrão.
-   Especifique um código de formato MTP (Media Transport Protocol) que o Player pode usar para determinar se um dispositivo portátil específico dá suporte ao formato de arquivo.

A maioria das entradas que você fornecer estará em uma sub-chave associada à sua extensão de nome de arquivo personalizado. Você pode criar essa subárvore na subárvore HKEY \_ LOCAL MACHINE e na \_ subárvore HKEY \_ CURRENT \_ USER. Windows Media Player primeiro na subárvore HKEY \_ LOCAL \_ MACHINE. Se ele não encontrar o que precisa lá, ele procurará na subárvore HKEY \_ CURRENT \_ USER. Observe que qualquer código que tentar gravar no Registro no computador do usuário poderá gravar na subárvore HKEY LOCAL MACHINE somente se o usuário atual tiver \_ \_ privilégios administrativos.

Para gravar informações sobre o formato de arquivo personalizado na subárvore HKEY \_ LOCAL \_ MACHINE, crie a sub-chave a seguir.

**HKEY \_ \_Extensões \\ \\ \\ \\ \\ WMPlayer do WMPlayer da Microsoft MACHINE Software LOCAL customExtension \\** 

em *que customExtension* é a extensão de nome de arquivo, incluindo o separador de ponto (.). Por exemplo, se a extensão para o formato de arquivo personalizado for .xyz, crie a sub-chave a seguir.

**Extensões \_ WMPlayer da Microsoft Multimídia do MICROSOFT MACHINE Software \_ \\ \\ \\ \\ HKEY LOCAL \\ \\ .xyz**

Para gravar informações sobre o formato de arquivo personalizado na subárvore HKEY \_ CURRENT \_ USER, crie a sub-chave a seguir.

**HKEY \_ CustomExtension do \_ \\ Microsoft \\ \\ MediaPlayer \\ Player \\ extensions \\** current user software *microsoft*

Você pode escrever uma ou mais das entradas a seguir em sua sub-chave *customExtension.*

-   **Permissões**
-   **Runtime**
-   **FormatCode**

Para especificar plug-ins de conversão para o formato de arquivo de mídia personalizado, crie uma sub-chave **ConvertPluginCLSID** em sua subkey *customExtension.*

Para especificar onde Windows Media Player deve exibir seus arquivos em sua exibição de biblioteca, escreva uma entrada que representa o formato de arquivo personalizado na sub-chave a seguir.

**Extensões do MICROSOFT \_ \_ \\ \\ \\ MediaPlayer \\ MLS do HKEY LOCAL MACHINE Software \\**

Os tópicos a seguir descrevem as sub-chaves e entradas do Registro que fornecem Windows Media Player informações sobre formatos de arquivo de mídia personalizados.

-   [Entrada do Registro de Permissões](permissions-registry-entry.md)
-   [Entrada do Registro em Runtime](runtime-registry-entry.md)
-   [Entrada do Registro FormatCode](formatcode-registry-entry.md)
-   [Entradas do Registro de Classificação de Biblioteca](library-classification-registry-entries.md)
-   [ConvertPluginCLSID Subkey](convertpluginclsid-subkey.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Configurações do Registro**](registry-settings.md)
</dt> <dt>

[**Windows Media Player Plug-ins de conversão**](windows-media-player-conversion-plug-ins.md)
</dt> </dl>

 

 




