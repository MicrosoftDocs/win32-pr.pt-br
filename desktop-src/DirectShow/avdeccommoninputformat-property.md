---
description: Especifica o formato de entrada atual para o decodificador.
ms.assetid: 8fddf8c3-268e-4706-9003-e4bfb03d5278
title: Propriedade AVDecCommonInputFormat (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7432d2a48727ec144d4206d4a11bfe65ce2c5d2a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456765"
---
# <a name="avdeccommoninputformat-property"></a>Propriedade AVDecCommonInputFormat

Especifica o formato de entrada atual para o decodificador.

Esta propriedade é somente para leitura.

## <a name="data-type"></a>Tipo de dados

**BSTR** (**VT \_ BSTR**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVDecCommonInputFormat**

## <a name="property-value"></a>Valor da propriedade

O valor dessa propriedade é um **BSTR** que contém a representação de cadeia de caracteres de um GUID. Os GUIDs a seguir são definidos.



| **GUID**                                            | Descrição                                    |
|-----------------------------------------------------|------------------------------------------------|
| **CODECAPI \_ GUID \_ AVDecAudioInputAAC**              | AAC (codificação de áudio avançada)                    |
| **CODECAPI \_ GUID \_ AVDecAudioInputDolbyDigitalPlus** | Áudio Dolby Digital Plus                       |
| **CODECAPI \_ GUID \_ AVDecAudioInputDolby**            | Áudio Dolby                                    |
| **CODECAPI \_ GUID \_ AVDecAudioInputDTS**              | Áudio DTS                                      |
| **CODECAPI \_ GUID \_ AVDecAudioInputHEAAC**            | Codificação de áudio avançada High-Efficiency (HE-AAC) |
| **CODECAPI \_ GUID \_ AVDecAudioInputMPEG**             | Áudio MPEG                                     |
| **CODECAPI \_ GUID \_ AVDecAudioInputPCM**              | Áudio PCM                                      |
| **CODECAPI \_ GUID \_ AVDecAudioInputWMA**              | Áudio do Windows Media                            |
| **CODECAPI \_ GUID \_ AVDecAudioInputWMAPro**           | Windows Media Audio 9 Professional (WMA pro)   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]<br/>                     |
| Servidor mínimo com suporte<br/> | Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]<br/>                           |
| parâmetro<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades da API do codec](codec-api-properties.md)
</dt> <dt>

[**Interface ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




