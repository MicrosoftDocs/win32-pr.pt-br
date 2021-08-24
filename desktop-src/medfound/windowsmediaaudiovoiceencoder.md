---
description: O Windows media audio voice é otimizado para codificar a voz humana em altas taxas de compactação. Esse é o codificador preferencial para fluxos que consistem principalmente em palavras faladas.
ms.assetid: b3cfa845-4fe1-405f-88e5-4555398639ef
title: Windows Codificador de Voz de Áudio de Mídia (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c107e4e09309ff0ed56e899d3ec2cd0c9d372261b48231b4530ed3222ee3a68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462417"
---
# <a name="windows-media-audio-voice-encoder"></a>Windows Codificador de voz de áudio de mídia

O Windows media audio voice é otimizado para codificar a voz humana em altas taxas de compactação. Esse é o codificador preferencial para fluxos que consistem principalmente em palavras faladas.

## <a name="class-identifier"></a>Identificador de Classe

O CLSID (identificador de classe) do codificador Windows Media Audio Voice é representado pela constante **CLSID \_ CWMSPEncMediaObject2**. Você pode criar uma instância do codificador de voz chamando **CoCreateInstance**.

## <a name="output-formats"></a>Formatos de saída

Windows O conteúdo codificado em Voz de Áudio de Mídia é identificado pela marca de formato 0x00A.

## <a name="encoder-properties"></a>Propriedades do codificador

O codificador Windows Media Audio Voice dá suporte às propriedades a seguir.



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
| Cabeçalho<br/> | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmspdmoe.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos codec](codecobjects.md)
</dt> <dt>

[Usando o codec Windows de áudio de mídia](usingthewindowsmediaaudio9voicecodec.md)
</dt> </dl>

 

 




