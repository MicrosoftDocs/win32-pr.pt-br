---
description: Filtro do mixer de sobreposição 2
ms.assetid: 3d3871ac-518c-45a1-9e64-031f344f4527
title: Filtro do mixer de sobreposição 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f22976a58b272cf04c098c102d32d154e361b8b9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105789827"
---
# <a name="overlay-mixer-2-filter"></a>Filtro do mixer de sobreposição 2

O filtro Overlay Mixer 2 é idêntico ao filtro de [mixer de sobreposição](overlay-mixer-filter.md) , exceto:

-   Ele dá suporte apenas a tipos de mídia com formatos [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) .
-   Ele tem um mérito maior, o que permite que ele seja adicionado automaticamente a um grafo de filtro.

O mixer de sobreposição 2 é fornecido para que o Gerenciador do grafo de filtro o adicione ao grafo quando ele renderiza um vídeo MPEG-2 diferente de DVD. A opção de usar o mixer de sobreposição ou o mixer de sobreposição 2 é tratada pelo componente que cria o grafo, o Gerenciador de gráficos de filtro, o construtor de gráficos de captura ou o construtor de gráficos de DVD. Da perspectiva do aplicativo, eles são o mesmo filtro, com as mesmas interfaces e funcionalidade.

A tabela a seguir contém informações específicas para o mixer de sobreposição 2. Para todos os outros dados de filtro, consulte a documentação do mixer de sobreposição.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Tipos de mídia de pino de entrada</td>
<td>Tipo de formato: Format_VIDEOINFO2</td>
</tr>
<tr class="even">
<td>CLSID do filtro</td>
<td>CLSID_OverlayMixer2</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Núcleo</a></td>
<td><ul>
<li>MERIT_UNLIKELY</li>
<li>Windows Vista ou posterior: MERIT_DO_NOT_USE</li>
</ul></td>
</tr>
</tbody>
</table>



 

No Windows Vista ou posterior, o mérito do filtro Overlay Mixer 2 é um mérito \_ \_ não \_ usado, pois os renderizadores de vídeo mais recentes (VMR-7, VMR-9 e EVR) dão suporte a formatos **VIDEOINFOHEADER2** e, portanto, não é necessário usar o mixer de sobreposição.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filtros do DirectShow](directshow-filters.md)
</dt> </dl>

 

 



