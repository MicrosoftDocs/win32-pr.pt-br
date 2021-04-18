---
description: O codificador de voz do Windows Media Audio é otimizado para codificar a voz humana em altas taxas de compactação. Esse é o codificador preferencial para fluxos que consistem principalmente em palavras faladas.
ms.assetid: b3cfa845-4fe1-405f-88e5-4555398639ef
title: Codificador de voz do Windows Media Audio (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bef79f2c3d0c48fee8ec33e08bfb9fdf21c3656b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763855"
---
# <a name="windows-media-audio-voice-encoder"></a>Codificador de voz do Windows Media Audio

O codificador de voz do Windows Media Audio é otimizado para codificar a voz humana em altas taxas de compactação. Esse é o codificador preferencial para fluxos que consistem principalmente em palavras faladas.

## <a name="class-identifier"></a>Identificador de classe

O CLSID (identificador de classe) do codificador de voz do Windows Media Audio é representado pelo **CLSID \_ CWMSPEncMediaObject2** de constantes. Você pode criar uma instância do codificador de voz chamando **CoCreateInstance**.

## <a name="output-formats"></a>Formatos de saída

O conteúdo codificado de voz do Windows Media Audio é identificado pela marca de formato 0x00a.

## <a name="encoder-properties"></a>Propriedades do codificador

O codificador de voz do Windows Media Audio oferece suporte às propriedades a seguir.



<table>
<thead>
<tr class="header">
<th>Propriedade</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mfpkey-wmavoice-enc-bufferwindowproperty.md">MFPKEY_WMAVOICE_ENC_BufferWindow</a></td>
<td>Especifica a janela de buffer, em milissegundos, usada para o codec de voz.<br/> <dl> Windows XP e posterior.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmavoice-enc-decoderdelayproperty.md">MFPKEY_WMAVOICE_ENC_DecoderDelay</a></td>
<td>Especifica a latência do codificador em unidades de pacote.<br/> <dl> Windows XP e posterior.<br />
Somente gravação.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmavoice-enc-edlproperty.md">MFPKEY_WMAVOICE_ENC_EDL</a></td>
<td>Especifica as partes do conteúdo a serem codificadas como música pelo codec de voz.<br/> <dl> Windows XP e posterior.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md">MFPKEY_WMAVOICE_ENC_MusicSpeechClassMode</a></td>
<td>Especifica o modo do codec de voz.<br/> <dl> Windows XP e posterior.<br />
Leitura/gravação.<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| Cliente<br/> | Windows XP, Windows Vista ou Windows 7<br/>                                       |
| parâmetro<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmspdmoe.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de codec](codecobjects.md)
</dt> <dt>

[Usando o codec de voz de áudio do Windows Media](usingthewindowsmediaaudio9voicecodec.md)
</dt> </dl>

 

 




