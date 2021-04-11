---
description: Especifica o esquema de codificação.
ms.assetid: a26951d6-67fb-43fb-849f-331416e9d7c2
title: Propriedade AVEncCodecType (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8643c0624b7d82381e2008f2adbd6804e9af9881
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104296048"
---
# <a name="avenccodectype-property"></a>Propriedade AVEncCodecType

Especifica o esquema de codificação.

Esta propriedade é de leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**BSTR** (**VT \_ BSTR**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVEncCodecType**

## <a name="property-value"></a>Valor da propriedade

O valor dessa propriedade é um **BSTR** que contém a representação de cadeia de caracteres de um GUID. Os GUIDs a seguir são definidos.



| GUID                                      | Descrição                                        |
|-------------------------------------------|----------------------------------------------------|
| CODECAPI \_ GUID \_ AVEncDolbyDigitalConsumer | Áudio Dolby Digital Consumer                       |
| CODECAPI \_ GUID \_ AVEncDolbyDigitalPlus     | Áudio Dolby Digital Plus                           |
| CODECAPI \_ GUID \_ AVEncDolbyDigitalPro      | Áudio Dolby Digital pro                            |
| CODECAPI \_ GUID \_ AVEncDTS                  | Áudio DTS                                          |
| CODECAPI \_ GUID \_ AVEncDTSHD                | DTS-áudio de HD                                       |
| CODECAPI \_ GUID \_ AVEncDV                   | Vídeo DV                                           |
| CODECAPI \_ GUID \_ AVEncH264Video            | Vídeo H. 264                                        |
| CODECAPI \_ GUID \_ AVEncMLP                  | Áudio de empacotamento sem perdas de meridiano (MLP)              |
| CODECAPI \_ GUID \_ AVEncMPEG1Audio           | Áudio MPEG-1                                       |
| CODECAPI \_ GUID \_ AVEncMPEG1Video           | Vídeo MPEG-1                                       |
| CODECAPI \_ GUID \_ AVEncMPEG2Audio           | Áudio MPEG-2                                       |
| CODECAPI \_ GUID \_ AVEncMPEG2Video           | Vídeo MPEG-2                                       |
| CODECAPI \_ GUID \_ AVEncPCM                  | Áudio PCM                                          |
| CODECAPI \_ GUID \_ AVEncSDDS                 | Áudio de som digital dinâmico (SDDS) da Sony            |
| CODECAPI \_ GUID \_ AVEncWMALossless          | Áudio do Windows Media 9 sem perdas               |
| CODECAPI \_ GUID \_ AVEncWMAPro               | Áudio do Windows Media Audio 9 Professional (WMA pro) |
| CODECAPI \_ GUID \_ AVEncWMAVoice             | Áudio do Windows Media áudio 9 Voice                  |
| CODECAPI \_ GUID \_ AVEncWMV                  | Vídeo do Windows Media                                |
| CODECAPI \_ GUID \_ AVEndMPEG4Video           | Vídeo MPEG-4                                       |



 

## <a name="remarks"></a>Comentários

Os aplicativos podem definir essa propriedade para especificar qual esquema de codificação usar. Os codecs também podem retornar essa propriedade como um recurso.

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

 

 




