---
description: Especifica o formato de entrada atual para o decodificador.
ms.assetid: 8fddf8c3-268e-4706-9003-e4bfb03d5278
title: Propriedade AVDecCommonInputFormat (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 187e923be9c53cebbb55663d55ec6351be38f84c33f8c03277f587d61a4db719
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079486"
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
| **CODECAPI \_ GUID \_ AVDecAudioInputWMAPro**           | Windows Professional de áudio de mídia 9 (WMA Pro)   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | aplicativos Windows 2000 Professional \[ desktop aplicativos \| UWP\]<br/>                     |
| Servidor mínimo com suporte<br/> | Windows \[ aplicativos da área de trabalho do servidor 2000 \| aplicativo UWP\]<br/>                           |
| Cabeçalho<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades da API do codec](codec-api-properties.md)
</dt> <dt>

[**Interface ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




