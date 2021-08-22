---
description: Especifica o formato de saída para o decodificador.
ms.assetid: fdccdbfa-2814-4d21-9a7f-4121b79718e6
title: Propriedade AVDecCommonOutputFormat (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 129f9a1171c5870eab243108fc0ed6992be4993b886cbd36d72fe91988f321b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586746"
---
# <a name="avdeccommonoutputformat-property"></a>Propriedade AVDecCommonOutputFormat

Especifica o formato de saída para o decodificador.

Essa propriedade é leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**BSTR** (**VT \_ BSTR**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVDecCommonOutputFormat**

## <a name="property-value"></a>Valor da propriedade



| GUID                                                               | Descrição                                                                                                                                                                                                         |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ PCM                        | Áudio PCM, usando qualquer número de canais                                                                                                                                                                             |
| CodeCAPI \_ GUID \_ AVDecAudioOutputFormat \_ PcM \_ Headsets            | Áudio PCM estéreo, usando downmix somente para a esquerda/direita (Lo/Ro)                                                                                                                                                        |
| CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ PCM \_ Estéreo \_ Auto          | Áudio PCM estéreo, usando a seleção automática do modo downmix estéreo (Lo/Ro ou Lt/Rt). Você pode usar esse valor para formatos de áudio nos quais o fluxo de entrada define o modo downmix preferencial, como Dolby AC-3. |
| CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ Matriz Estéreo do \_ PCMEncodificado \_ | Áudio PCM estéreo, usando downmix estéreo codificado em matriz (Lt/Rt)                                                                                                                                                       |
| BITstream \_ \_ DO CODECAPI GUID AVDecAudioOutputFormat \_ SPDIF \_           | Bitstream compactado S/PDIF (Formato de Interface Digital Da Chicago/Philips), conforme definido por IEC-60958                                                                                                                        |
| CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ SPDIF \_ PCM                 | S/PDIF PCM estéreo, conforme definido por IEC-60958                                                                                                                                                                          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[ aplicativos UWP da área de \| trabalho\]<br/>                     |
| Servidor mínimo com suporte<br/> | Windows aplicativos da área de trabalho do servidor 2000 \[ \| aplicativos UWP\]<br/>                           |
| Cabeçalho<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades da API do Codec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI Interface**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




