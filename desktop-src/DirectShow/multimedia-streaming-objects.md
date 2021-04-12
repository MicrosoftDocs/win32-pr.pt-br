---
description: Objetos de streaming multimídia
ms.assetid: 4f5460db-2670-41af-a57f-20cf706827e6
title: Objetos de streaming multimídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05762e4a3d7aa486b8a22b73905fc5d9c1610078
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104297986"
---
# <a name="multimedia-streaming-objects"></a>Objetos de streaming multimídia

> [!Note]  
> Essa API está preterida. Novos aplicativos não devem usá-lo.

 

A tabela a seguir descreve os objetos de streaming de multimídia.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>CLSID</th>
<th>Descrição</th>
<th>Interfaces com suporte</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>CLSID_AMMediaTypeStream</td>
<td>Pode criar amostras de mídia para qualquer tipo de dados com suporte do DirectShow</td>
<td><ul>
<li><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream"><strong>IAMMediaStream</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream"><strong>IMediaStream</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></li>
</ul></td>
</tr>
<tr class="even">
<td>CLSID_AMAudioData</td>
<td>Implementação do objeto de contêiner <a href="/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata"><strong>IAudioData</strong></a> Audio.</td>
<td><ul>
<li><a href="/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata"><strong>IAudioData</strong></a></li>
</ul></td>
</tr>
<tr class="odd">
<td>CLSID_AMDirectDrawStream</td>
<td>O fluxo de mídia do DirectDraw que pode ser adicionado a um fluxo multimídia do DirectShow.</td>
<td><ul>
<li><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream"><strong>IAMMediaStream</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream"><strong>IMediaStream</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream"><strong>IDirectDrawMediaStream</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></li>
</ul></td>
</tr>
<tr class="even">
<td>CLSID_AMMultiMediaStream</td>
<td>Implementação do DirectShow do fluxo de multimídia.</td>
<td><ul>
<li><a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream"><strong>IAMMultiMediaStream</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream"><strong>IMultiMediaStream</strong></a></li>
</ul></td>
</tr>
<tr class="odd">
<td>CLSID_MediaStreamFilter</td>
<td>Fornece a funcionalidade de streaming de multimídia para o objeto CLSID_AMMultiMediaStream por meio da interface <a href="/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream"><strong>IAMMultiMediaStream</strong></a> .</td>
<td><ul>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></li>
</ul></td>
</tr>
<tr class="even">
<td>N/D</td>
<td>Exemplos criados pelo objeto CLSID_AMMediaTypeStream.</td>
<td><ul>
<li><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample"><strong>IStreamSample</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample"><strong>IMediaSample</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample2"><strong>IMediaSample2</strong></a></li>
</ul></td>
</tr>
<tr class="odd">
<td>N/D</td>
<td>Exemplos criados pelo fluxo do DirectDraw.</td>
<td><ul>
<li><a href="/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample"><strong>IStreamSample</strong></a></li>
<li><a href="/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample"><strong>IDirectDrawStreamSample</strong></a></li>
<li><a href="/windows/desktop/api/Strmif/nn-strmif-imediasample"><strong>IMediaSample</strong></a></li>
</ul></td>
</tr>
</tbody>
</table>



 

 

 



