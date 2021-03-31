---
description: Gerenciamento de qualidade de vídeo
ms.assetid: 3617adf2-ed7b-4788-abce-58bc22a14511
title: Gerenciamento de qualidade de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 233ccd54cfcb98742abef9a91241e903c07ba549
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921206"
---
# <a name="video-quality-management"></a>Gerenciamento de qualidade de vídeo

Este tópico descreve algumas melhorias no pipeline de vídeo no Windows 7, tanto para Microsoft Media Foundation quanto para o Microsoft DirectShow.

Em um mundo perfeito, o vídeo nunca falharia, independentemente da resolução de vídeo ou da carga de CPU/GPU. Na realidade, é claro que o pipeline de vídeo deve ser capaz de lidar com os recursos de hardware finitos e deve adaptar a reprodução adaptável ao ambiente do sistema. As metas para o gerenciamento de qualidade de vídeo são:

-   Reduzir a falha (quadros descartados ou atrasados).
-   Reduza o uso de memória, especialmente na GPU.
-   Reduza o consumo de energia, especialmente em laptops em execução com energia da bateria.
-   Obtenha a melhor qualidade de imagem possível, dadas as restrições de recursos.
-   Mantenha o vídeo sincronizado com áudio.

Algumas dessas metas são contrárias, especialmente em sistemas low-end. Geralmente, há uma compensação entre velocidade e qualidade. A falha é mais censurável do que as reduções moderadas na qualidade visual. A importância relativa do consumo de energia varia de acordo com o ambiente; em um laptop em execução com baterias, é muito importante.

No Windows 7, o processador de vídeo avançado (EVR) tem melhor suporte para o gerenciamento de qualidade de vídeo. O pipeline de Media Foundation e o pipeline do DirectShow foram atualizados para aproveitar esses recursos. Uma abordagem de duas pontas é usada:

-   Antes de iniciar a reprodução, o pipeline pode executar otimizações estáticas, com base nas configurações de gerenciamento de energia do usuário e informações sobre o hardware.
-   Depois que a reprodução é iniciada, o pipeline pode aplicar otimizações dinâmicas com base no desempenho em tempo de execução.

## <a name="quality-management-in-media-foundation"></a>Gerenciamento de qualidade no Media Foundation

Para habilitar otimizações estáticas, defina o atributo de [ \_ \_ \_ \_ otimizações de reprodução estática da topologia MF](mf-topology-static-playback-optimizations.md) na topologia parcial antes de resolver a topologia. O carregador de topologia consulta esse atributo em seu método [**IMFTopoLoader:: Load**](/windows/desktop/api/mfidl/nf-mfidl-imftopoloader-load) .

Se você habilitar otimizações estáticas, deverá definir dois outros atributos na topologia:



| Atributo                                                                                                                                      | Descrição                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="MF_TOPOLOGY_PLAYBACK_MAX_DIMS"></span><span id="mf_topology_playback_max_dims"></span>\_ \_ esmaecimento máximo da reprodução da topologia MF \_ \_<br/>   | Especifica o tamanho máximo da janela de reprodução de vídeo.<br/> |
| <span id="MF_TOPOLOGY_PLAYBACK_FRAMERATE"></span><span id="mf_topology_playback_framerate"></span>\_taxa de \_ quadros de reprodução da topologia MF \_<br/> | Especifica a taxa de atualização do monitor.<br/>                      |



 

Esses dois atributos ajudam o pipeline a calcular a configuração mais efetiva para o gerenciamento de qualidade.

As otimizações dinâmicas são executadas pelo Gerenciador de qualidade. Você não precisa fazer nada para habilitar o Gerenciador de qualidade; Ele é habilitado automaticamente. O Gerenciador de qualidade existia no Windows Vista; no Windows 7, o EVR pode responder melhor às mensagens do Gerenciador de qualidade.

## <a name="quality-management-in-directshow"></a>Gerenciamento de qualidade no DirectShow

O DirectShow dá suporte a otimizações estáticas e dinâmicas para reprodução de DVD. Para habilitar essas otimizações em um aplicativo de reprodução de DVD, defina os seguintes sinalizadores no parâmetro *dwFlags* do método **IDvdGraphBuilder:: RenderDvdVideoVolume** :



| Sinalizador                  | Descrição                    |
|-----------------------|--------------------------------|
| \_grafo de \_ adaptação de DVD am \_ | Habilita otimizações estáticas.  |
| \_ \_ EVR QoS de DVD am \_     | Habilita otimizações dinâmicas. |



 

Outros aplicativos do DirectShow podem habilitar otimizações dinâmicas chamando o método [**IEVRFilterConfigEx:: SetConfigPrefs**](/windows/desktop/api/evr/nf-evr-ievrfilterconfigex-setconfigprefs) diretamente no filtro EVR. Especifique o sinalizador **EVRFilterConfigPrefs \_ EnableQoS** .

> [!Note]  
> Otimizações estáticas no DirectShow são limitadas à reprodução de DVD.

 

## <a name="quality-management-in-the-evr"></a>Gerenciamento de qualidade no EVR

O EVR dá suporte a alguns novos sinalizadores de configuração para gerenciamento de qualidade. Se você habilitar as otimizações de gerenciamento de qualidade descritas anteriormente, não precisará definir esses sinalizadores diretamente. No entanto, eles são documentados para aplicativos que desejam um controle mais granular sobre o EVR.

Defina os seguintes sinalizadores no mixer EVR chamando o método [**IMFVideoMixerControl2:: SetMixingPrefs**](/windows/desktop/api/evr/nf-evr-imfvideomixercontrol2-setmixingprefs) :



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Flags</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><strong>MFVideoMixPrefs_ForceHalfInterlace</strong></li>
<li><strong>MFVideoMixPrefs_AllowDropToHalfInterlace</strong></li>
</ul></td>
<td>Ignore o segundo campo de cada quadro entrelaçado.</td>
</tr>
<tr class="even">
<td><ul>
<li><strong>MFVideoMixPrefs_AllowDropToBob</strong></li>
<li><strong>MFVideoMixPrefs_ForceBob</strong></li>
</ul></td>
<td>Use Bob deentrelaçando, mesmo que o driver dê suporte a um modo de desentrelaçamento de qualidade superior.</td>
</tr>
</tbody>
</table>



 

Defina os seguintes sinalizadores no apresentador EVR chamando o método [**IMFVideoDisplayControl:: SetRenderingPrefs**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setrenderingprefs) :



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Flags</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><strong>MFVideoRenderPrefs_ForceOutputThrottling</strong></li>
<li><strong>MFVideoRenderPrefs_AllowOutputThrottling</strong></li>
</ul></td>
<td>Limite a saída para corresponder à largura de banda da GPU.</td>
</tr>
<tr class="even">
<td><ul>
<li><strong>MFVideoRenderPrefs_ForceBatching</strong></li>
<li><strong>MFVideoRenderPrefs_AllowBatching</strong></li>
</ul></td>
<td>O Direct3D do lote apresenta chamadas. Essa otimização permite que o sistema entre em Estados ociosos com mais frequência, o que pode reduzir o consumo de energia.</td>
</tr>
<tr class="odd">
<td><ul>
<li>MFVideoRenderPrefs_ForceScaling</li>
<li>MFVideoRenderPrefs_AllowScaling</li>
</ul></td>
<td>Execute a mistura de vídeo usando um retângulo menor do que o retângulo de saída. Dimensione o resultado para o tamanho de saída correto.</td>
</tr>
</tbody>
</table>



 

Além disso, o coletor de mídia EVR dá suporte a atributos de configuração que correspondem a cada um desses sinalizadores:

-   [EVRConfig \_ AllowBatching](evrconfig-allowbatching.md)
-   [EVRConfig \_ AllowDropToBob](evrconfig-allowdroptobob.md)
-   [EVRConfig \_ AllowDropToHalfInterlace](evrconfig-allowdroptohalfinterlace.md)
-   [EVRConfig \_ AllowScaling](evrconfig-allowscaling.md)
-   [EVRConfig \_ AllowDropToThrottle](evrconfig-allowdroptothrottle.md)
-   [EVRConfig \_ ForceBatching](evrconfig-forcebatching.md)
-   [EVRConfig \_ ForceBob](evrconfig-forcebob.md)
-   [EVRConfig \_ ForceHalfInterlace](evrconfig-forcehalfinterlace.md)
-   [EVRConfig \_ ForceScaling](evrconfig-forcescaling.md)
-   [EVRConfig \_ ForceThrottle](evrconfig-forcethrottle.md)

Antes de iniciar a reprodução, você pode definir esses atributos diretamente no coletor de mídia do EVR, como uma alternativa para chamar os métodos [**IMFVideoMixerControl2**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol2) e [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) . Para definir esses atributos, consulte o coletor de mídia do EVR para [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sessão de mídia](media-session.md)
</dt> </dl>

 

 




