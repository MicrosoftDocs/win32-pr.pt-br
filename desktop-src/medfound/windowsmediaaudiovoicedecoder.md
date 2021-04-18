---
description: O decodificador de voz de áudio do Windows Media decodifica os fluxos que foram codificados pelo codificador de voz de áudio do Windows Media.
ms.assetid: 8bb5c8bd-949f-4faa-b679-8854f78076a4
title: Decodificador de voz do Windows Media Audio (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4565a511f2816d2914ec96f3ae89f3af5dd19016
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105785028"
---
# <a name="windows-media-audio-voice-decoder"></a>Decodificador de voz do Windows Media Audio

O decodificador de voz de áudio do Windows Media decodifica os fluxos que foram codificados pelo [**codificador de voz de áudio do Windows Media**](windowsmediaaudiovoiceencoder.md).

## <a name="class-identifier"></a>Identificador de classe

O CLSID (identificador de classe) do decodificador de voz de áudio do Windows Media é representado pela constante **CLSID \_ CWMSPDecMediaObject**. Você pode criar uma instância do decodificador de voz chamando **CoCreateInstance**.

## <a name="input-formats"></a>Formatos de entrada

O conteúdo codificado de voz do Windows Media Audio é identificado pela marca de formato 0x00a.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| Cliente<br/> | Windows XP, Windows Vista ou Windows 7<br/>                                       |
| parâmetro<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Wmspdmod.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de codec](codecobjects.md)
</dt> <dt>

[Usando o codec de voz de áudio do Windows Media](usingthewindowsmediaaudio9voicecodec.md)
</dt> <dt>

[Codificador de voz do Windows Media Audio](windowsmediaaudiovoiceencoder.md)
</dt> </dl>

 

 




