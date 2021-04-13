---
description: Especifica o formato de saída para o decodificador.
ms.assetid: fdccdbfa-2814-4d21-9a7f-4121b79718e6
title: Propriedade AVDecCommonOutputFormat (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b69c536b3c9f1bf75e2a5741d0cdd16569b3dd8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500657"
---
# <a name="avdeccommonoutputformat-property"></a>Propriedade AVDecCommonOutputFormat

Especifica o formato de saída para o decodificador.

Esta propriedade é de leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**BSTR** (**VT \_ BSTR**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVDecCommonOutputFormat**

## <a name="property-value"></a>Valor da propriedade



| GUID                                                               | Descrição                                                                                                                                                                                                         |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ PCM                        | Áudio PCM, usando qualquer número de canais                                                                                                                                                                             |
| CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ PCM \_ fone de ouvido            | Áudio PCM estéreo, usando somente à esquerda/à direita (lo/ro) downmix                                                                                                                                                        |
| CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ PCM \_ estéreo \_ auto          | Áudio PCM estéreo, usando a seleção automática do modo estéreo downmix (lo/ro ou lt/RT). Você pode usar esse valor para formatos de áudio nos quais o fluxo de entrada define o modo downmix preferencial, como Dolby AC-3. |
| CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ PCM \_ estéreo \_ MatrixEncoded | Áudio PCM estéreo, usando estéreo downmix codificado em matriz (LT/RT)                                                                                                                                                       |
| CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ SPDIF \_ fragmentado           | S/PDIF (formato de interface digital Sony/Philips) fragmentado compactados, conforme definido pelo IEC-60958                                                                                                                        |
| CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ SPDIF \_ PCM                 | Estéreo PCM S/PDIF, conforme definido por IEC-60958                                                                                                                                                                          |



 

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

 

 




