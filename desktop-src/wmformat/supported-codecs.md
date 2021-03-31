---
title: Codecs com suporte
description: Codecs com suporte
ms.assetid: d5907d38-2e26-442e-a0d1-1d7e267b9948
keywords:
- SDK do Windows Media Format, codecs com suporte
- SDK do Windows Media Format, interface IWMCodecInfo3
- codecs, com suporte
- IWMCodecInfo3, sobre
- codecs, interface IWMCodecInfo3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5ac06ad3d58d066254fa666f96283dca9b8b6ae
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103640168"
---
# <a name="supported-codecs"></a>Codecs com suporte

O Windows Media Format SDK fornece suporte para os seguintes codecs que são incluídos quando você instala o SDK.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Codec</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Áudio do Windows Media</td>
<td>Codec de áudio para uso geral na codificação de áudio complexo, como música. As versões mais recentes desse codec são o codec do Windows Media Audio 9 e o codec do Windows Media Audio 9,1.<br/></td>
</tr>
<tr class="even">
<td>Windows Media Audio Professional</td>
<td>Codec de áudio para áudio complexo, como música. Dá suporte à codificação multicanal e de 24 bits. Há duas versões deste codec:<br/>
<ul>
<li>Áudio do Windows Media 9 Professional</li>
<li>Windows Media Audio 9,1 Professional</li>
</ul></td>
</tr>
<tr class="odd">
<td>Windows Media Audio sem perdas</td>
<td>Codec de áudio para codificação sem perdas. Há duas versões deste codec:<br/>
<ul>
<li>Áudio do Windows Media 9 sem perdas</li>
<li>Áudio do Windows Media 9,1 sem perdas</li>
</ul></td>
</tr>
<tr class="even">
<td>Voz do Windows Media Audio 9</td>
<td>Codec de áudio otimizado para codificar a voz humana em altas taxas de compactação. Esse é o codec preferencial para fluxos que consistem principalmente em palavras faladas. Para conteúdo que é música e fala mista, esse codec pode alterar dinamicamente o algoritmo de codificação usado para obter a qualidade ideal.</td>
</tr>
<tr class="odd">
<td>Vídeo do Windows Media 9</td>
<td>Codec de vídeo para uso geral na codificação de vídeo complexo, como filmes.</td>
</tr>
<tr class="even">
<td>Perfil avançado do Windows Media Video 9</td>
<td>Codec de vídeo que incorpora recursos de codificação avançados, incluindo codificação entrelaçada.</td>
</tr>
<tr class="odd">
<td>Tela do Windows Media Video 9</td>
<td>Codec de vídeo otimizado para codificação de capturas de tela sequenciais. Esse codec é geralmente usado para treinamento de software ou suporte ao gravar imagens de monitor conforme os aplicativos de computador são usados.</td>
</tr>
<tr class="even">
<td>Imagem de vídeo do Windows Media</td>
<td>Codec de vídeo para converter imagens de bitmap com informações de reformação em vídeo compactado. Há duas versões desse Codec:<br/>
<ul>
<li>Imagem do Windows Media Video 9</li>
<li>Imagem do Windows Media Video 9 v2</li>
</ul></td>
</tr>
</tbody>
</table>



 

Versões diferentes dos codecs de vídeo e áudio do Windows Media estão disponíveis para codificação, dependendo da versão do SDK do Windows Media Format que você instalar. Quando você usar os métodos se a interface [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3) para enumerar codecs e formatos de codec, somente as versões mais recentes com suporte serão enumeradas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Escolhendo um método de codificação**](choosing-an-encoding-method.md)
</dt> <dt>

[**Recursos do codec**](codec-features.md)
</dt> </dl>

 

 





