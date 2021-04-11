---
description: Escolhendo um codec de vídeo
ms.assetid: 3a4b925a-4fb4-4189-a571-8083454fed0e
title: Escolhendo um codec de vídeo (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9186c7e7e60f5822ec2e50e3e5c7e16e96b91839
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164216"
---
# <a name="choosing-a-video-codec-microsoft-media-foundation"></a>Escolhendo um codec de vídeo (Microsoft Media Foundation)

O codificador do Windows Media Video 9 dá suporte a três categorias de saída codificada: perfil principal, perfil avançado e imagem. A categoria de perfil principal fornece compactação de vídeo geral para conteúdo de vídeo complexo, como filmes ou vídeos de música. Os recursos do perfil principal fornecem uma ampla gama de configurações de codificação. Você pode usar o perfil principal para criar vídeo com taxas de bits muito baixas para entrega em dispositivos portáteis ou, na outra extremidade do espectro, você pode usá-lo para criar vídeo de alta definição para cinema digital.

A ênfase dos algoritmos de codificação no perfil principal é o conteúdo de vídeo dinâmico, mas eles são adequados para outros conteúdos de vídeo também. O perfil principal deve ser sua categoria padrão para conteúdo de vídeo. Para atender a necessidades específicas, você pode usar a categoria de perfil avançado, a categoria de imagem ou um codificador separado chamado de codificador de tela do Windows Media Video 9. A tabela a seguir lista as quatro opções.



<table>
<thead>
<tr class="header">
<th>Finalidade</th>
<th>Codec</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Codificação de vídeo de uso geral</td>
<td><a href="windowsmediavideo9encoder.md">Codificador do Windows Media Video 9</a><dl> Perfil Principal<br />
</dl></td>
</tr>
<tr class="even">
<td>Codificando vídeo de alta definição ou vídeo que está de acordo com o padrão SMPTE do perfil avançado VC-1</td>
<td><a href="windowsmediavideo9encoder.md">Codificador do Windows Media Video 9</a><dl> Perfil avançado<br />
</dl></td>
</tr>
<tr class="odd">
<td>Convertendo imagens de bitmap em vídeo dinâmico</td>
<td><a href="windowsmediavideo9encoder.md">Codificador do Windows Media Video 9</a><dl> Imagem<br />
</dl></td>
</tr>
<tr class="even">
<td>Codificação de vídeo de aplicativo de computador (captura de tela) ou outro vídeo altamente estático</td>
<td><a href="windowsmediavideo9screenencoder.md"><strong>Codificador de tela do Windows Media Video 9</strong></a></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com vídeo](workingwithvideo.md)
</dt> </dl>

 

 



