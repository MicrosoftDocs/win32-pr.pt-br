---
title: Extensões de nome de arquivo
description: Extensões de nome de arquivo
ms.assetid: c17bf4e5-b469-45b6-bc22-2b451723d85e
keywords:
- Windows Metadados de mídia, extensões
- Windows Metadados de mídia, extensões de nome de arquivo
- metafiles,extensions
- metafiles, extensões de nome de arquivo
- Windows Mídia, metadados
- extensões de nome de arquivo Windows metadados de mídia
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6c69c36a5865b3496cf63e8cc08d73b9187f5107b14bf0bbb0d52b462e90c88a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054984"
---
# <a name="file-name-extensions"></a>Extensões de nome de arquivo

Há diretrizes específicas para o uso de extensões de nome de arquivo para metadados Windows Mídia. Windows As extensões de nome de metadados de mídia são usadas para identificar os diferentes tipos de arquivos Windows Mídia. Uma extensão de nome de arquivo fornece um ISV (Fornecedor Independente de Software) com informações sobre os requisitos de renderização de um aplicativo que usa uma extensão específica e permite que os autores de conteúdo sejam destinados a tipos gerais de players de mídia.

As diretrizes de extensão de nome de arquivo são listadas na tabela a seguir. É recomendável que o tipo MIME de um arquivo, localizado no header do arquivo, seja usado para identificação de tipo de arquivo.



| Extensão de nome de arquivo | tipo MIME      | Conteúdo do arquivo                                                                                                                                                                            |
|---------------------|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| .wma                | audio/x-ms-wma | Windows Arquivo de mídia somente com conteúdo de áudio. Normalmente usado para baixar e reproduzir arquivos ou transmitir conteúdo.                                                                             |
| .wmv                | video/x-ms-wmv | Windows Arquivo de mídia com conteúdo de áudio e/ou vídeo. Normalmente usado para baixar e reproduzir arquivos ou transmitir conteúdo.                                                                     |
| .asf                | video/x-ms-asf | Conteúdo herddo. Normalmente usado para baixar e reproduzir arquivos ou transmitir conteúdo. Pode conter conteúdo de áudio e/ou vídeo. Normalmente usado para baixar e reproduzir arquivos ou transmitir conteúdo. |
| .wm                 | video/x-ms-wm  | Reservado                                                                                                                                                                                |
| .9                | audio/x-ms-audio | Metadados que fazem referência Windows de mídia com extensões de nome de arquivo .asf, .wma ou .file.                                                                                             |
| .wvx                | video/x-ms-wvx | Metadados que fazem referência Windows arquivos de mídia com extensões de nome de arquivo .wma, .wmv, .wvx ou .file.                                                                                       |
| .asx                | video/x-ms-asf | Metadados que fazem referência Windows arquivos de mídia com extensões de nome de arquivo .wma, .wmv, .wmv, .asf ou .asx.                                                                           |
| .wmx                | video/x-ms-wvx | Reservado.                                                                                                                                                                               |



 

## <a name="remarks"></a>Comentários

Scripts e DRM (gerenciamento de direitos digitais) devem ser suportados por qualquer aplicativo que renderiza Windows de Mídia.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Windows Referência de elementos de metadados de mídia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Guia de metadados de mídia**](windows-media-metafile-guide.md)
</dt> <dt>

[**Windows Referência de metadados de mídia**](windows-media-metafile-reference.md)
</dt> </dl>

 

 




