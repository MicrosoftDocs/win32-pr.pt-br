---
title: Extensões de nome de arquivo
description: Extensões de nome de arquivo
ms.assetid: c17bf4e5-b469-45b6-bc22-2b451723d85e
keywords:
- Metaarquivos do Windows Media, extensões
- Metaarquivos do Windows Media, extensões de nome de arquivo
- metaarquivos, extensões
- metaarquivos, extensões de nome de arquivo
- Windows Media, metaarquivos
- extensões de nome de arquivo para os metaarquivos do Windows Media
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d95d5bcba9bbad5f04b0d085ba712d5b9306c8b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105811100"
---
# <a name="file-name-extensions"></a>Extensões de nome de arquivo

Há diretrizes específicas para o uso de extensões de nome de arquivo para os metaarquivos do Windows Media. As extensões de nome de metarquivo do Windows Media são usadas para identificar os diferentes tipos de arquivos de mídia do Windows. Uma extensão de nome de arquivo fornece um fornecedor de software independente (ISV) com informações sobre os requisitos de renderização de um aplicativo que usa uma extensão específica e permite que os autores de conteúdo direcionem tipos gerais de players de mídia.

As diretrizes de extensão de nome de arquivo são listadas na tabela a seguir. É recomendável que o tipo MIME de um arquivo, localizado no cabeçalho do arquivo, seja usado para a identificação do tipo de arquivo.



| Extensão de nome de arquivo | tipo MIME      | Conteúdo do arquivo                                                                                                                                                                            |
|---------------------|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| .wma                | áudio/x-MS-WMA | Arquivo de mídia do Windows com conteúdo de áudio apenas. Normalmente usado para baixar e reproduzir arquivos ou transmitir conteúdo.                                                                             |
| .wmv                | vídeo/x-MS-WMV | Arquivo de mídia do Windows com conteúdo de áudio e/ou vídeo. Normalmente usado para baixar e reproduzir arquivos ou transmitir conteúdo.                                                                     |
| .asf                | vídeo/x-ms-asf | Conteúdo herdado. Normalmente usado para baixar e reproduzir arquivos ou transmitir conteúdo. Pode conter conteúdo de áudio e/ou vídeo. Normalmente usado para baixar e reproduzir arquivos ou transmitir conteúdo. |
| .wm                 | vídeo/x-MS-WM  | Reservado                                                                                                                                                                                |
| . Wax                | áudio/x-MS-Wax | Os metaarquivos que fazem referência a arquivos de mídia do Windows com extensões de nome de arquivo. ASF,. WMA ou. Wax.                                                                                             |
| .wvx                | vídeo/x-MS-wvx | Os metaarquivos que fazem referência a arquivos de mídia do Windows com extensões de nome de arquivo. WMA,. wmv,. wvx ou. Wax.                                                                                       |
| .asx                | vídeo/x-ms-asf | Os metaarquivos que fazem referência a arquivos de mídia do Windows com extensões de nome de arquivo. WMA,. Wax,. wmv,. WVX,. ASF ou. asx.                                                                           |
| . WMX                | vídeo/x-MS-wvx | Reservado.                                                                                                                                                                               |



 

## <a name="remarks"></a>Comentários

O script e o DRM (gerenciamento de direitos digitais) devem ser suportados por qualquer aplicativo que processe arquivos de mídia do Windows.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de elementos de metarquivo do Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Guia de metarquivo do Windows Media**](windows-media-metafile-guide.md)
</dt> <dt>

[**Referência do metarquivo do Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 




