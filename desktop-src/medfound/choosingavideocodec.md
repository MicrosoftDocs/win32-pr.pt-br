---
description: Escolhendo um codec de vídeo
ms.assetid: 3a4b925a-4fb4-4189-a571-8083454fed0e
title: Escolhendo um codec de vídeo (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b560666ddeebb88fc3bb720cbc9f1be26308e7ecd8a4ad872fbb1f0991826fe2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035364"
---
# <a name="choosing-a-video-codec-microsoft-media-foundation"></a>Escolhendo um codec de vídeo (Microsoft Media Foundation)

O codificador Windows Media Video 9 dá suporte a três categorias de saída codificada: Perfil Principal, Perfil Avançado e Imagem. A categoria Perfil Principal fornece compactação geral de vídeo para conteúdo de vídeo complexo, como filmes ou vídeos de música. Os recursos do Perfil Principal fornecem uma ampla variedade de configurações de codificação. Você pode usar o Perfil Principal para criar vídeo com taxas de bits muito baixas para entrega em dispositivos portáteis ou, na outra extremidade do espectro, você pode usá-lo para criar vídeo de alta definição para o ambiente digital.

A ênfase dos algoritmos de codificação no Perfil Principal está no conteúdo de vídeo dinâmico, mas eles também são adequados para outros conteúdos de vídeo. O Perfil Principal deve ser sua categoria padrão para conteúdo de vídeo. Para atender às necessidades específicas, você pode usar a categoria Perfil Avançado, a categoria Imagem ou um codificador separado chamado codificador de tela Windows Media Video 9. A tabela a seguir lista as quatro opções.



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
<td><a href="windowsmediavideo9encoder.md">Windows Codificador de Vídeo de Mídia 9</a><dl> Perfil Principal<br />
</dl></td>
</tr>
<tr class="even">
<td>Vídeo ou vídeo de alta definição de codificação que está em conformidade com o padrão SMPTE de Perfil Avançado vc-1</td>
<td><a href="windowsmediavideo9encoder.md">Windows Codificador de Vídeo de Mídia 9</a><dl> Perfil Avançado<br />
</dl></td>
</tr>
<tr class="odd">
<td>Convertendo imagens bitmapped em vídeo dinâmico</td>
<td><a href="windowsmediavideo9encoder.md">Windows Codificador de Vídeo de Mídia 9</a><dl> Imagem<br />
</dl></td>
</tr>
<tr class="even">
<td>Codificação de vídeo de aplicativo de computador (captura de tela) ou outro vídeo altamente estático</td>
<td><a href="windowsmediavideo9screenencoder.md"><strong>Windows Codificador de tela do Vídeo de Mídia 9</strong></a></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com vídeo](workingwithvideo.md)
</dt> </dl>

 

 



