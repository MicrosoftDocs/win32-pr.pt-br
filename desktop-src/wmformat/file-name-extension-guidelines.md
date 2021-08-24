---
title: Diretrizes de extensão de nome de arquivo
description: Diretrizes de extensão de nome de arquivo
ms.assetid: 71189ed8-4140-446f-a765-d72f35dd3d88
keywords:
- Windows SDK de Formato de Mídia, extensões de nome de arquivo
- FORMATO DE SISTEMAS Avançados (ASF), extensões de nome de arquivo
- ASF (Formato de Sistemas Avançados), extensões de nome de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ccd8c3b1b4ba27aa7360296fc336625cb0f51c4374bb77c06d349cb70a987c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118703999"
---
# <a name="file-name-extension-guidelines"></a>Diretrizes de extensão de nome de arquivo

Uma extensão de nome de arquivo fornece a um fornecedor de software independente informações sobre os requisitos de renderização de um aplicativo que usa essa extensão específica.

A extensão de nome de arquivo que você deve usar para um arquivo criado por um aplicativo com base no SDK Windows Formato de Mídia é determinada pelo tipo de conteúdo no arquivo. Use a lógica a seguir para determinar a extensão de nome de arquivo que você deve usar.

Se o arquivo contiver fluxos codificados com codecs de terceiros ou dados não compactados sem suporte (incluindo dados arbitrários), o arquivo deverá usar a extensão .asf.

Se o arquivo não contiver fluxos sem suporte e contiver um ou mais fluxos de vídeo descompactados ou codificados com qualquer codec de vídeo Windows Media, o arquivo deverá usar a extensão .wmv. Esses arquivos também podem incluir fluxos de áudio PCM, fluxos de áudio codificados com qualquer codec de áudio Windows Media, fluxos de script e fluxos da Web.

Se o arquivo não contiver fluxos sem suporte e nenhum fluxo de vídeo com suporte e contiver um ou mais fluxos de áudio pcM descompactados ou codificados com qualquer codec de áudio de mídia do Windows, o arquivo deverá usar a extensão .wma. Esses arquivos também podem conter fluxos de script e fluxos da Web.

Se o arquivo contiver apenas fluxos que não são áudio nem vídeo, ele deverá usar a extensão .asf.

Os tipos de vídeo descompactados com suporte incluem RGB8, RGB565, RGB555, RGB24, RGB32, I420, IYUV, YV12, YUY2, UYVY, YVYU e Y LTD9.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Project Considerações**](project-considerations.md)
</dt> </dl>

 

 




