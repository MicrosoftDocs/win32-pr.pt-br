---
description: Esta seção descreve como gravar uma Media Foundation de transformação personalizada (MFT).
ms.assetid: a95828d3-afc5-4f6b-aedd-5b6a72621e0e
title: Gravando uma MFT personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d15b9d5ae655ba67d4a526aeb8a82eb9d3912da9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828615"
---
# <a name="writing-a-custom-mft"></a>Gravando uma MFT personalizada

Esta seção descreve como gravar uma Media Foundation de transformação personalizada (MFT).

## <a name="mft-checklist"></a>Lista de verificação de MFT

Ao implementar um MFT personalizado, use a seguinte lista de verificação para determinar os requisitos:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Todos os MFTs</td>
<td>Todos os MFTs devem implementar <a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform"><strong>IMFTransform</strong></a>.<br/> Os tópicos a seguir fornecem mais informações sobre como implementar essa interface:
<ul>
<li><a href="basic-mft-processing-model.md">Modelo de processamento de MFT básico</a></li>
<li><a href="time-stamps-and-durations.md">Carimbos de data/hora e durações</a></li>
<li><a href="handling-stream-changes.md">Manipulando alterações de fluxo</a></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>Codificadores e decodificadores</td>
<td>Requisitos: consulte <a href="implementing-a-codec-mft.md">implementando um codec de MFT</a>.<br/> Recomendado: implemente <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise"><strong>IMFQualityAdvise</strong></a> ou <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2"><strong>IMFQualityAdvise2</strong></a>para dar suporte a notificações de QoS (qualidade de serviço).<br/></td>
</tr>
<tr class="odd">
<td>Decodificadores de vídeo e processadores de vídeo</td>
<td>Opcional: suporte para aceleração de vídeo do DirectX.<br/>
<ul>
<li><a href="direct3d-aware-mfts.md">MFTs com reconhecimento de Direct3D</a></li>
<li><a href="supporting-dxva-2-0-in-media-foundation.md">Suporte a DXVA 2,0 no Media Foundation</a></li>
</ul></td>
</tr>
<tr class="even">
<td>Codecs de hardware</td>
<td>Consulte <a href="hardware-mfts.md">hardware MFTs</a>.</td>
</tr>
<tr class="odd">
<td>Para tornar seu MFT detectável por aplicativos...</td>
<td>Consulte <a href="registering-and-enumerating-mfts.md">registrando e enumerando MFTs</a>.</td>
</tr>
<tr class="even">
<td>Processamento de dados assíncronos</td>
<td>O modelo de MFT padrão usa chamadas síncronas (de bloqueio) para processar dados. Para alguns MFTs, o processamento assíncrono pode ser mais eficiente. No entanto, também é mais complexo implementar.<br/> Para obter mais informações, consulte <a href="asynchronous-mfts.md">assíncrona MFTs</a>.<br/></td>
</tr>
<tr class="odd">
<td>Controle de taxa, modo de truque ou reprodução reversa</td>
<td>Consulte <a href="implementing-rate-control.md">implementando o controle de taxa</a>.</td>
</tr>
<tr class="even">
<td>Se o MFT criar threads...</td>
<td>Implemente a interface <a href="/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient"><strong>IMFRealTimeClient</strong></a> .</td>
</tr>
<tr class="odd">
<td>Se a MFT tiver restrições de licenciamento...</td>
<td>Considere o uso do mecanismo de campo de uso. Consulte o <a href="field-of-use-restrictions.md">campo de restrições de uso</a>.</td>
</tr>
<tr class="even">
<td>Se você estiver portando um objeto de mídia DirectX existente (DMO)...</td>
<td>Consulte <a href="comparison-of-mfts-and-dmos.md">comparação de MFTs e DMOs</a>.</td>
</tr>
</tbody>
</table>



 

Esta seção contém os seguintes tópicos:

-   [Carimbos de data/hora e durações](time-stamps-and-durations.md)
-   [Manipulando alterações de fluxo](handling-stream-changes.md)
-   [Implementando uma MFT do codec](implementing-a-codec-mft.md)
-   [MFTs com reconhecimento de Direct3D](direct3d-aware-mfts.md)
-   [MFTs de hardware](hardware-mfts.md)
-   [Mérito do codec](codec-merit.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Transformações de Media Foundation](media-foundation-transforms.md)
</dt> </dl>

 

 




