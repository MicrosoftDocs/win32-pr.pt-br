---
title: Diretrizes de extensão de nome de arquivo
description: Diretrizes de extensão de nome de arquivo
ms.assetid: 71189ed8-4140-446f-a765-d72f35dd3d88
keywords:
- SDK do Windows Media Format, extensões de nome de arquivo
- ASF (Advanced Systems Format), extensões de nome de arquivo
- ASF (formato de sistemas avançados), extensões de nome de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bed1fb59379644711a3954dc5eb82707e0e42f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916226"
---
# <a name="file-name-extension-guidelines"></a>Diretrizes de extensão de nome de arquivo

Uma extensão de nome de arquivo fornece um fornecedor de software independente com informações sobre os requisitos de renderização de um aplicativo que usa essa extensão específica.

A extensão de nome de arquivo que você deve usar para um arquivo criado por um aplicativo baseado no Windows Media Format SDK é determinada pelo tipo de conteúdo no arquivo. Use a lógica a seguir para determinar a extensão de nome de arquivo que você deve usar.

Se o arquivo contiver fluxos codificados com codecs de terceiros ou quaisquer dados descompactados sem suporte (incluindo dados arbitrários), o arquivo deverá usar a extensão. ASF.

Se o arquivo não contiver fluxos sem suporte e contiver um ou mais fluxos de vídeo descompactados ou codificados com qualquer codec de vídeo do Windows Media, o arquivo deverá usar a extensão. wmv. Esses arquivos também podem incluir fluxos de áudio PCM, fluxos de áudio codificados com qualquer codec de áudio do Windows Media, fluxos de script e fluxos da Web.

Se o arquivo não contiver fluxos sem suporte e fluxos de vídeo com suporte e contiver um ou mais fluxos de áudio não compactados PCM ou codificados com qualquer codec de áudio do Windows Media, o arquivo deverá usar a extensão. WMA. Esses arquivos também podem conter fluxos de script e fluxos da Web.

Se o arquivo contiver apenas fluxos que não sejam áudio nem vídeo, ele deverá usar a extensão. ASF.

Os tipos de vídeo descompactados com suporte incluem RGB8, RGB565, RGB555, RGB24, RGB32, I420, IYUV, YV12, YUY2, UYVY, YVYU e YVU9.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Considerações sobre o projeto**](project-considerations.md)
</dt> </dl>

 

 




